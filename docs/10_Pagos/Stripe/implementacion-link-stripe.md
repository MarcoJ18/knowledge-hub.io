---
title: "Stripe con Links (sin plugin)"
description: "Este tutorial explica cómo integrar Stripe en tu sitio WordPress utilizando enlaces de pago, sin necesidad de instalar el plugin oficial de Stripe. Aprenderás a crear, configurar y gestionar enlaces de pago directamente desde el dashboard de Stripe."
tags:
  - Pagos
  - Stripe
author: "Víctor Lourenco"
date: "07 Abril 2025"
---

<div class="metadata" style="font-size: 0.9em; color: #555; margin-bottom: 0.5rem; line-height: 1.4;">
  <span><strong>Autor:</strong> {{ page.meta.author }}</span> &nbsp;|&nbsp;
  <span><strong>Fecha:</strong> {{ page.meta.date }}</span> &nbsp;|&nbsp;
  <span><strong>Etiquetas:</strong> {{ page.meta.tags | join(", ") }}</span>
</div>

# {{ page.meta.title }}

{{ page.meta.description }}

---

## Creación del Link de Stripe

Stripe es una pasarela de pago que permite ser implementada en una web de diferentes formas. Aquí aprenderás cómo hacerlo en WordPress **sin plugins**.

!!! tip "Consejo"
    Para que el cliente pueda autogestionar los productos y enlaces de pago, se recomienda que la cuenta de Stripe utilizada sea la del propio cliente.

1. Accede a tu cuenta de Stripe y entra al <span class="custom-highlight">Dashboard</span>.
2. Haz clic en el botón `+` y selecciona <span class="custom-highlight">Enlace de pago</span> en el submenú.

    <img src="../../../images/stripe/image.webp" alt="Imagen del dashboard de Stripe destacando el menú de opciones." style="display: block; margin: auto; max-width: 100%; height: auto;">
    <br/><sup>Seleccionar la opción para Crear un Enlace de Pago</sup>

3. Se abrirá la página para crear el enlace de pago:

    <img src="../../../images/stripe/image-2.webp" alt="Imagen del dashboard de Stripe." style="display: block; margin: auto; max-width: 100%; height: auto;">
    <br/><sup>Página de Creación del Enlace de Pago</sup>

### Apartados principales

#### Elegir Tipo

Por regla general, el tipo de producto más habitual es **Productos o suscripciones**. La opción **Los clientes deciden qué pagar** es útil para donaciones o propinas.

<img src="../../../images/stripe/image-3.webp" alt="Imagen del dashboard de Stripe." style="display: block; margin: auto; max-width: 100%; height: auto;">
<br/><sup>Elegir el tipo de Enlace de Pago</sup>

#### Opciones

Aquí puedes seleccionar opciones como **Cobrar impuestos automáticamente**, según las necesidades del cliente y del proyecto.

<img src="../../../images/stripe/image-4.webp" alt="Imagen del dashboard de Stripe." style="display: block; margin: auto; max-width: 100%; height: auto;">
<br/><sup>Opciones del Enlace de Pago</sup>

#### Opciones Avanzadas

Opciones técnicas adicionales (opcional).

<img src="../../../images/stripe/image-5.webp" alt="Imagen del dashboard de Stripe." style="display: block; margin: auto; max-width: 100%; height: auto;">
<br/><sup>Opciones Avanzadas del Enlace de Pago</sup>

#### Producto

Selecciona un producto existente o crea uno nuevo.

---

## Configurar un nuevo Producto

La primera vez que uses Stripe para este tipo de implementación, probablemente no haya productos creados. Selecciona <span class="custom-button">+ Añadir un Producto Nuevo</span>.

<img src="../../../images/stripe/image-6.webp" alt="Imagen del dashboard de Stripe." style="display: block; margin: auto; max-width: 100%; height: auto;">
<br/><sup>Página de Creación del Producto</sup>

### Nombre, descripción e imagen

El **nombre** es obligatorio, pero es recomendable añadir también descripción e imagen para un producto más completo.

<img src="../../../images/stripe/image-7.webp" alt="Imagen del dashboard de Stripe." style="display: block; margin: auto; max-width: 100%; height: auto;">
<br/><sup>Datos principales del Producto</sup>

### Más opciones

Si lo necesitas, despliega **Más opciones** para configurar detalles técnicos como Stripe Tax, descripción en extracto bancario, etiquetas, metadatos o funciones de marketing.

### Importe

Elige si el producto es de pago <span class="custom-highlight">Puntual</span> o recurrente <span class="custom-highlight">Suscripción</span> y especifica el importe y la divisa.

<img src="../../../images/stripe/image-8.webp" alt="Imagen del dashboard de Stripe." style="display: block; margin: auto; max-width: 100%; height: auto;">
<br/><sup>Opciones del Producto Creado</sup>

Puedes añadir precios por divisa y configurar opciones avanzadas de precios. Haz clic en <span class="custom-button">Añadir producto</span> para incluirlo en el enlace de pago.

### Vista previa

En la columna de **Vista Previa** puedes ver cómo quedarán los cambios en la página de pago.

<img src="../../../images/stripe/image-9.webp" alt="Imagen del dashboard de Stripe." style="display: block; margin: auto; max-width: 100%; height: auto;">
<br/><sup>Vista Previa de la Página a la que llevará el Enlace de Pago</sup>

Cuando termines, haz clic en **Crear enlace**.

---

## Revisar y probar el enlace de Stripe

Al crear el enlace, aparecerá la sección <span class="custom-highlight">Payment Links</span> en la barra lateral del Dashboard. Aquí puedes gestionar todos los enlaces y sus productos.

<img src="../../../images/stripe/image-10.webp" alt="Imagen del dashboard de Stripe." style="display: block; margin: auto; max-width: 100%; height: auto;">
<br/><sup>Datos del Enlace de Pago creado</sup>

<img src="../../../images/stripe/image-11.webp" alt="Imagen del dashboard de Stripe." style="display: block; margin: auto; max-width: 100%; height: auto;">
<br/><sup>Detalles del Enlace de Pago Creado</sup>

Copia el enlace y pégalo en tu web (botón, texto o enlace).

<img src="../../../images/stripe/image-12.webp" alt="Imagen del dashboard de Stripe." style="display: block; margin: auto; max-width: 100%; height: auto;">
<br/><sup>Acceder a la página del enlace de pago</sup>

!!! info "Nota"
    Si ves el mensaje "Entornos de prueba predeterminado", significa que estás usando una cuenta de pruebas de Stripe.

---

## Acciones sobre el enlace

En la sección **Payment Links**, haz clic en los tres puntos (`...`) junto a un enlace para ver opciones como **Editar** o **Desactivar**.

![](https://cdn.mathpix.com/cropped/2025_04_25_cc5e5b5dc8dbe82bb967g-13.jpg?height=636&width=1293&top_left_y=647&top_left_x=387)
<br/><sup>Acciones Disponibles sobre el Enlace de Pago</sup>

---

## Editar un enlace

Selecciona **Editar** para modificar el enlace. Se abrirá la misma página de creación para realizar los cambios necesarios.

![](https://cdn.mathpix.com/cropped/2025_04_25_cc5e5b5dc8dbe82bb967g-13.jpg?height=789&width=872&top_left_y=1810&top_left_x=598)
<br/><sup>Página para editar el enlace de pago</sup>

![](https://cdn.mathpix.com/cropped/2025_04_25_cc5e5b5dc8dbe82bb967g-14.jpg?height=783&width=961&top_left_y=308&top_left_x=553)
<br/><sup>Vista previa de los cambios realizados</sup>

Haz clic en **Actualizar Enlace** para guardar los cambios.

---

## Desactivar un enlace

Selecciona **Desactivar** para inhabilitar el enlace. Confirma la acción en la ventana emergente.

!!! warning "Cuidado"
    Stripe no permite eliminar enlaces de pago, solo desactivarlos. Puedes reactivar el enlace más adelante si lo necesitas.

---

## Notas finales

- Puedes incluir el enlace de pago en tu web como texto, botón o enlace dentro de una frase.
- Gestiona productos y enlaces fácilmente desde el dashboard de Stripe.
- Utiliza las opciones avanzadas solo si realmente lo necesitas.

---

¡Listo! Ahora puedes integrar pagos con Stripe en tu WordPress de forma sencilla y sin plugins.
