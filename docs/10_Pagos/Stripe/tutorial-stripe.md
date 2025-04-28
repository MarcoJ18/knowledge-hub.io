---
title: "Instalar y Configurar Stripe en WordPress"
description: "Este tutorial explica cómo instalar y configurar la pasarela de pago **Stripe** mediante su plugin oficial en un sitio web hecho con WordPress."
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


## 📥 Instalación del plugin Stripe

1. En el panel de WordPress, ve a **Plugins > Añadir nuevo**.
2. En el buscador de plugins, escribe:  
   ```
   Accept Stripe Payment
   ```
3. Asegúrate de elegir el correcto (por ejemplo, de `mra13` o `Tips and Tricks HQ`).
4. Haz clic en **Instalar Ahora** y luego en **Activar**.

---

## 🔑 Obtener las claves de Stripe

1. Entra en [https://dashboard.stripe.com](https://dashboard.stripe.com).
2. Inicia sesión y ve a la sección **Desarrolladores > Claves API**.
3. Copia las 4 claves (clave pública y secreta de prueba y producción).
4. Durante el desarrollo, **usa solo las claves de prueba**.

!!! bug "IMPORTANTE"

      Durante el desarrollo es importante que guardemos todas las claves en un sitio accesible, porque una vez cambiemos de pestaña, para poder volver a acceder a ellas, necesitaremos acceder de nuevo con la contraseña. Esto es un problema cuando el cliente tiene verificación de 2 pasos (2FA) en su cuenta ya que nos retrasará mucho el desarrollo.
---

## ⚙️ Configuración general del plugin en WordPress

   Stripe tiene 4 grandes secciones de configuración: Ajustes Generales, de Correo Electrónico, Avanzados y del Captcha.

1. Ve a **Stripe Payments > Ajustes**.
2. En la sección *Ajustes Generales*:
   - Asegúrate de que las URLs generadas por Stripe coincidan con las páginas existentes en WordPress.
   - Selecciona la moneda (ej. Euro `€`).
   - Configura las credenciales de API (usa las de prueba en esta etapa).

> 💡 No elimines `%s` en el formato del precio. Representa el valor del producto.

---

## 📧 Ajustes de Correo Electrónico

Activa los siguientes correos automáticos:

- ✅ Al comprador tras la compra.
- ✅ Al vendedor tras la compra.
- ✅ Al vendedor si falla la compra.
- ✅ Al vendedor si se supera el límite diario (opcional).

Si queremos dedicarle un poco de tiempo a que queden mejor los correos que se envían, podemos personalizarlos desde la sección de **Cuerpo del Correo Electrónico**.

---

## 🛠 Ajustes Avanzados

- Cambia la posición del símbolo de la moneda si lo deseas.
- Activa la casilla de **aceptar Términos y Condiciones** antes de comprar.
- Edita la URL del enlace a los Términos modificando el `href` a la que hemos creado en las políticas (Términos y condiciones).

---

## 🔐 Configuración de Captcha

1. Selecciona el tipo **reCAPTCHA v2 (No soy un robot)**.
2. Obtén las claves desde [https://www.google.com/recaptcha](https://www.google.com/recaptcha).
3. Usa el mismo dominio que el del sitio.

> ⚠️ Stripe solo funciona bien con **Captcha v2**, no v3.

---

## 🛒 Crear Productos en Stripe Payments

1. Ve a **Stripe Payments > Añadir nuevo producto**.
2. Completa:
    - Nombre del producto.
    - Descripción corta y larga.
    - Precio y moneda.
    - Cantidad e inventario.
    - Gastos de envío, URL de descarga, miniatura del producto.
3. En *Apariencia*, puedes añadir una **clase CSS personalizada** al botón del producto.

---

## 🔧 Implementar productos en una página

1. Usa el **shortcode del producto** que te da el plugin.
2. Inserta el shortcode en un módulo de texto de cualquier página.

---

## 🎨 Estilizar el producto

1. Ve a **Apariencia > Personalizar > CSS adicional**.
2. Usa CSS personalizado para aplicar estilos a los botones, contenedores, etc.

> 🧠 Usa el inspector del navegador para identificar clases o IDs del producto y personalizar mejor.

---

## 📚 Webgrafía

- [🌐Stripe.com](https://stripe.com)
- [🌐Documentación del plugin Accept Stripe Payments](https://es.wordpress.org/plugins/accept-stripe-payments/)
- [🔴Videotutorial sobre Stripe + WordPress](https://www.youtube.com/watch?v=TqpTfKKxA0I)

---

Cualquier duda contactar con [Marco](https://www.youtube.com/watch?v=xvFZjo5PgG0) 😎