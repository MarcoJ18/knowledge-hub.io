---
title: "Botón Imprimir Página"
description: "Guía para crear un botón que escanee la página y la prepare para imprimirla (también se podría descargar en PDF directamente)."
tags:
  - Trucos
  - CSS
  - Impresión
  - JavaScript
author: "David Morales"
date: "4 Abril 2025"
---

<div class="metadata" style="font-size: 0.9em; color: #555; margin-bottom: 0.5rem; line-height: 1.4;">
  <span><strong>Autor:</strong> {{ page.meta.author }}</span> &nbsp;|&nbsp;
  <span><strong>Fecha:</strong> {{ page.meta.date }}</span> &nbsp;|&nbsp;
  <span><strong>Etiquetas:</strong> {{ page.meta.tags | join(", ") }}</span>
</div>

# {{ page.meta.title }}

{{ page.meta.description }}


## 🔴 Crear Botón y Configurar

- Lo primero será añadir un botón a la página web, se puede hacer usando el editor ya sea divi, elementor, betheme etc o mediante el uso de código html en en este caso será un botón normal de betheme.

<img src="../../../images/imprimir-web/image1.webp" alt="Imagen del editor de Betheme mostrando como añadir un botón" style="display: block; margin: auto; max-width: 100%; height: auto;">

- En el link de botón escribimos javascript:void(0); para que el navegador interprete el botón como código y no como un enlace evitando su carga o que se desplace al principio de la página.


## 💻 Añadir JS Personalizado

- Ahora nos dirigimos al editor que estemos usando en este caso Betheme, y nos desplazamos hasta el apartado de JS y CSS.

<img src="../../../images/imprimir-web/image3.webp" alt="Imagen del editor de Betheme mostrando como añadir un botón" style="display: block; margin: auto; max-width: 100%; height: auto;">

- Dentro de JS pegamos el código:

```javascript
document.addEventListener("DOMContentLoaded", function() {
    document.querySelector(".imprimir-boton").addEventListener("click", function() {
        window.print();
    });
});
```


- Con este código conseguimos que el botón imprima la página web es lo mismo que Ctrl + P o Clic Derecho Imprimir.

## 🎨 Añadir CSS Personalizado 

Ahora vamos con la parte del formateo, debemos eliminar todos el contenido que no nos sea necesario y formatearlo correctamente para que la salida de la impresión sea la correcta.

<img src="../../../images/imprimir-web/image2.webp" alt="Imagen del editor de Betheme mostrando como añadir un botón" style="display: block; margin: auto; max-width: 100%; height: auto;">

<strong>El código es el siguiente:</strong>

```css
@media print {
    /* Elimina márgenes y paddings generales */
    html, body {
        margin: 0 !important;
        padding: 0 !important;
        width: 100% !important;
        height: auto !important;
        display: block !important;
    }

    /* Mantiene la estructura pero elimina espacios innecesarios */
    #Wrapper, #Content, .section_wrapper {
        margin: 0 !important;
        padding: 0 !important;
        width: 100% !important;
        display: block !important;
        position: relative !important;
    }



    /* Mueve el título "Inox" al principio y lo centra */
    #Content > div > main > div > section.section.mcb-section.mfn-default-section.mcb-section-l33bd1u8g > div.section_wrapper.mfn-wrapper-for-wraps.mcb-section-inner.mcb-section-inner-l33bd1u8g > div.wrap.mcb-wrap.mcb-wrap-4ah1s7kh6.one-second.tablet-one-second.laptop-one-second.mobile-one.clearfix > div > div.column.mcb-column.mcb-item-onjzy6iw.one.laptop-one.tablet-one.mobile-one.column_heading > div > h2 {
        width: 100% !important;
        text-align: center !important;
        font-size: 24px !important;
        font-weight: bold !important;
        margin-bottom: 20px !important; /* Aumenta el margen inferior para separarlo del contenido */
        position: relative !important;
        z-index: 10 !important; /* Asegura que esté por encima de todo */
        order: -1 !important; /* Lo coloca al principio */
    }

    /* Mantiene la estructura en columnas */
    .section_wrapper {
        display: flex !important;
        flex-wrap: wrap !important;
        align-items: flex-start !important;
        justify-content: space-between !important;
    }

    .column {
        width: auto !important;
        display: inline-block !important;
        vertical-align: top !important;
    }

    /* Corrige espacios superiores */
    .section_wrapper:first-child, .wrap:first-child, .column:first-child {
        margin-top: 0 !important;
        padding-top: 0 !important;
    }

    /* Elimina header, footer y elementos innecesarios */
    header, footer, .mfn-header-sticky, .header_placeholder {
        display: none !important;
    }

    /* Evita márgenes de impresión */
    @page {
        margin: 10;
    }

    /* Oculta secciones y elementos específicos */
    #Content > div > main > div > section.section.mcb-section.mfn-default-section.mcb-section-gqd29o6z6.full-width,
    body > div:nth-child(90) > div,
    #Content > div > main > div > section.section.mcb-section.mfn-default-section.mcb-section-c5w0imeg3 > div.section_wrapper.mfn-wrapper-for-wraps.mcb-section-inner.mcb-section-inner-c5w0imeg3 > div > div > div.column.mcb-column.mcb-item-d9yd7mwc.one.laptop-one.tablet-one.mobile-one.column_button.imprimir-boton > div {
        display: none !important;
    }
}
```
Hay que ajustar las variables a las que utilice los elementos de nuestra página web para hacer eso inspeccionamos la página.

## 🔷 Seleccionar Elemento (F12) 

<img src="../../../images/imprimir-web/image5.webp" alt="Imagen del editor de Betheme mostrando como añadir un botón" style="display: block; margin: auto; max-width: 100%; height: auto;">

Nos posicionamos encima del elemento o contenedor que queramos eliminar y pinchamos sobre él.

<img src="../../../images/imprimir-web/image4.webp" alt="Imagen del editor de Betheme mostrando como añadir un botón" style="display: block; margin: auto; max-width: 100%; height: auto;">

Luego hacemos clic derecho encima del elemento y damos clic en copiar selector y así podremos ir eliminando los componentes que no queramos utilizar por lo general con:

```css	
@media print{
	[variable]{display:none ! important
}
}

```

Se eliminará el elemento de la página web a la hora de imprimirlo.
