---
title: "Corregir los textos del menú al usar GTranslate (versión gratuita)"
description: "Solución para corregir los textos del menú al usar GTranslate (versión gratuita)"
tags:
  - Web
  - Traducción
  - Gratis
author: "Adrián González"
date: "14 Abril 2025"
---
<div class="metadata" style="font-size: 0.9em; color: #555; margin-bottom: 0.5rem; line-height: 1.4;">
  <span><strong>Autor:</strong> {{ page.meta.author }}</span> &nbsp;|&nbsp;
  <span><strong>Fecha:</strong> {{ page.meta.date }}</span> &nbsp;|&nbsp;
  <span><strong>Etiquetas:</strong> {{ page.meta.tags | join(", ") }}</span>
</div>

# 🌟{{ page.meta.title }}

🧬 {{ page.meta.description }}

## 🧹 Problema
Cuando se usa el plugin GTranslate (gratuito) en WordPress, los textos del menú se traducen automáticamente de forma literal y fuera de contexto.

Por ejemplo:

- **"Inicio"** se traduce como **"Start"** (en lugar de "Home")

- **"Equipo"** como **"Equipment"** (en vez de "Team")

- **"Actualidad"** como **"Present"** (en lugar de "News")

Además, como la versión gratuita no permite usar subdirectorios (/en/, /fr/, etc.), no es posible detectar el idioma para cambiar el menú de forma tradicional usando plugins como Conditional Menus.

## ✅ Solución (sin plugins de pago)
Reemplazar dinámicamente los textos del menú con JavaScript, según el idioma seleccionado por el usuario en GTranslate.

---

## 🛠 Pasos para implementar la solución

### 1. Usa solo un menú en tu sitio (por ejemplo, el menú en español)
- Ve a **Apariencia > Menús**.
- Deja los textos originales en español:
  - Inicio – Equipo – Servicios – Casos – Actualidad – Contacto
- Asigna ese menú como el menú principal del sitio.

### 2. Añade el siguiente código JavaScript personalizado

#### Opcion 1 – Si usas Elementor:
- Ve a **Elementor > Código personalizado**.
- Crea un nuevo bloque llamado, por ejemplo, *Corrección de menú por idioma*.
- Pega el siguiente código y selecciona "Cargar en todo el sitio" y en el área `<head>` o `<footer>`.

#### Opcion 2 – Si no usas Elementor:
- Usa un plugin gratuito como **Simple Custom CSS and JS**.
- Crea un nuevo bloque de código JS y pégalo.

---

## ✅ Código:
```html
<script>
  document.addEventListener("DOMContentLoaded", function() {
    const translations = {
      "Inicio": "Home",
      "Equipo": "Team",
      "Servicios": "Services",
      "Casos": "Cases",
      "Actualidad": "News",
      "Contacto": "Contact"
    };

    const reverseTranslations = Object.fromEntries(
      Object.entries(translations).map(([es, en]) => [en, es])
    );

    function updateMenuText(currentLang) {
      document.querySelectorAll("nav a, .elementor-nav-menu a").forEach(link => {
        const text = link.textContent.trim();
        if (currentLang === "en" && translations[text]) {
          link.textContent = translations[text];
        } else if (currentLang === "es" && reverseTranslations[text]) {
          link.textContent = reverseTranslations[text];
        }
      });
    }

    function detectLanguage() {
      const hashLang = location.hash.match(/#googtrans\/[a-z]{2}\/[a-z]{2}/);
      const currentLang = hashLang ? hashLang[1] : document.documentElement.lang || "es";
      updateMenuText(currentLang);
    }

    const observer = new MutationObserver(function() {
      detectLanguage();
    });

    observer.observe(document.body, { childList: true, subtree: true });
    detectLanguage();
  });
</script>
```

---

## 💡 ¿Qué hace este código?
- Detecta el idioma seleccionado por GTranslate.
- Reemplaza solo los textos del menú definidos por ti.
- Si el usuario vuelve a cambiar a español, restaura automáticamente los textos originales.

---

## 📋 Personalización
Puedes editar las traducciones fácilmente en esta parte del código:

```javascript
const translations = {
  "Inicio": "Home",
  "Equipo": "Team",
  "Servicios": "Services",
  "Casos": "Cases",
  "Actualidad": "News",
  "Contacto": "Contact"
};
```
Agrega o modifica lo que necesites.

---

## 🧪 Prueba final

1. Carga tu sitio en español: deberías ver los textos originales.
2. Cambia a inglés con GTranslate: deberías ver los textos corregidos como "Home", "Team", etc.
3. Vuelve a español: los textos vuelven automáticamente a "Inicio", "Equipo", etc.

---

## ✅ Ventajas de esta solución
- 100% gratuita
- No requiere versiones premium ni subdirectorios
- Totalmente personalizable
- Funciona con GTranslate gratuito

