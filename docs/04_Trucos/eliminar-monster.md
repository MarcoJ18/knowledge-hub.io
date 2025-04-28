---
title: "Eliminar Banner Monster Insight"
description: "Tutorial sobre cómo eliminar el logotipo de MonsterInsights (versión gratuita) usando CSS"
tags:
  - Plugin
  - CSS
  - Eliminar
author: "David Morales"
date: "04 Abril 2025"
---

<div class="metadata" style="font-size: 0.9em; color: #555; margin-bottom: 0.5rem; line-height: 1.4;">
  <span><strong>Autor:</strong> {{ page.meta.author }}</span> &nbsp;|&nbsp;
  <span><strong>Fecha:</strong> {{ page.meta.date }}</span> &nbsp;|&nbsp;
  <span><strong>Etiquetas:</strong> {{ page.meta.tags | join(", ") }}</span>
</div>

# 🚀{{ page.meta.title }}

{{ page.meta.description }}

## 👣 Pasos a seguir: 

1. Abre la página web donde aparece el logotipo de MonsterInsights.
2. Presiona **F12** para abrir las herramientas de desarrollador (modo inspección).
3. Selecciona la herramienta de selección (el ícono de una flecha o cursor arriba a la izquierda).
4. Haz clic sobre el banner o logotipo de MonsterInsights que quieres eliminar.
5. Dentro de la sección de código:
   - Haz **clic derecho** sobre el elemento seleccionado.
   - Elige **Copiar** > **Copiar selector**.

---

## 🧾 Añadir CSS personalizado: 

1. En tu panel de administración de WordPress, ve a **Divi** en el menú lateral.
2. Desplázate hasta el final de las opciones y entra en **CSS Personalizado**.
3. Pega el selector que copiaste y añade el siguiente código:

```css
.body > div:nth-child(45) {
  display: none !important;
}
```

4. Guarda los cambios.

---

✅ **Resultado esperado:**  
El logotipo de MonsterInsights ya no debería mostrarse en tu sitio web.

---

## ⚠️ Consideraciones importantes 

- El selector `.body > div:nth-child(45)` depende de la estructura específica de la página.
- Si la estructura cambia (por ejemplo, en otras páginas), el selector podría dejar de funcionar porque el número de elementos hijos cambia.

---

## ✅ Solución recomendada para evitar problemas futuros: ➡

Usa un selector más estable basado en atributos. Añade este CSS en lugar del anterior:

```css
div[style*="text-align: center"] a[href*="monsterinsights.com"] {
  display: none !important;
}
```

### 💻 ¿Qué hace este código?
- Selecciona cualquier `div` que tenga un `style` que incluya `text-align: center`.
- Luego selecciona cualquier `a` (enlace) dentro de ese `div` cuyo `href` contenga "monsterinsights.com".
- Aplica `display: none` de forma forzada.

---

## 🎯 Resultado final
Con este método, **el logotipo de MonsterInsights desaparecerá de todas las páginas** de manera más confiable, sin importar si cambia el número de elementos de la estructura de la página.

