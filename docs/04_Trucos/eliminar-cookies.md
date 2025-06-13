---
title: "Eliminar Menú flotante CookieYes"
description: "Tutorial sobre cómo eliminar el menú flotante del plugin CookieYes usando CSS."
tags:
  - Plugin
  - CSS
  - Eliminar
author: "David Morales"
date: "28 Abril 2025"
---

<div class="metadata" style="font-size: 0.9em; color: #555; margin-bottom: 0.5rem; line-height: 1.4;">
  <span><strong>Autor:</strong> {{ page.meta.author }}</span> &nbsp;|&nbsp;
  <span><strong>Fecha:</strong> {{ page.meta.date }}</span> &nbsp;|&nbsp;
  <span><strong>Etiquetas:</strong> {{ page.meta.tags | join(", ") }}</span>
</div>

# 🍪{{ page.meta.title }}

{{ page.meta.description }}

<img src="../../../images/cookieYes/image1.webp" alt="Imagen del editor de Betheme mostrando como añadir un botón" style="display: block; margin: auto; max-width: 100%; height: auto;">
Nuestro objetivo será eliminar el menú flotante que aparece después de aceptar las cookies

<strong>Lo haremos usando el siguiente código de JS:</strong>

## Código JS
```javascript
document.addEventListener("DOMContentLoaded", function () {
    function getCookie(name) {
        const value = `; ${document.cookie}`;
        const parts = value.split(`; ${name}=`);
        if (parts.length === 2) return parts.pop().split(';').shift();
    }

    function hideCookieRevisitButton() {
        const revisitButton = document.querySelector(".cky-btn-revisit-wrapper");
        if (revisitButton) {
            revisitButton.style.display = "none";
        }
    }

    function checkConsentAndHide() {
        const consent = getCookie("cookieyes-consent");
        if (consent && consent.includes("yes")) {
            hideCookieRevisitButton();
        }
    }

   
    checkConsentAndHide();
    const observer = new MutationObserver(checkConsentAndHide);
    observer.observe(document.body, {
        childList: true,
        subtree: true,
    });
});
```

!!! warning 
    Funciona en la version 3.2.9, es posible que si en versiones futuras se cambie el nombre de las variables o el funcionamiento del plugin haya que arreglarlo


## Añadir código JS
<img src="../../../images/cookieYes/image3.webp" alt="Imagen del editor de Betheme mostrando como añadir un botón" style="display: block; margin: auto; max-width: 100%; height: auto;">

Ahora nos desplazamos al editor que estemos usando en ese momento en este caso se está haciendo con el editor Betheme:

- Nos dirigimos al apartado general y nos desplazamos al final
- Seleccionamos Custom CSS & JS
- Añadimos el código JS

!!! warning
    Importante purgar el caché de la página.

<img src="../../../images/cookieYes/image2.webp" alt="Imagen del editor de Betheme mostrando como añadir un botón" style="display: block; margin: auto; max-width: 100%; height: auto;">

✅ Comprobamos que el menú flotante ha desaparecido
