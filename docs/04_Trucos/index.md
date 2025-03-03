---
title: Recorte de Imágenes por CSS
description: Tutorial sobre como cortar imágenes con CSS personalizado en Divi y Wordpress
date: 2025-02-27
author: Adrián González
---
# Cortar Imágenes

!!! warning

    En móvil se rompe bastante revisarlo bien o meterle !important a todo

### Paso 1. Añadir la clase al ccs

La clase dependerá de la relación aspecto que queramos, pero siempre tendrá el formato

- pa-image-[primer aspect-ratio]-[segundo aspect-ratio]
    - Ejemplo -> Para ratio 16:9 -> pa-image-16-9 

![image](https://github.com/user-attachments/assets/2370d003-c609-409e-aa5f-e5b9aeede262)

### Paso 2. Añadir código a la imagen

- Añadir el código que queramos usar dependiendo del aspect-ratio que queramos en el apartado de css personalizado

![image](https://github.com/user-attachments/assets/5e9b32a0-646b-4e67-a14a-1663215d4e2a)


## Square 1:1 
– Proporción 1 / 1 = 1.00 = 100%
```css
/*image aspect ratio square 1:1*/
.pa-image-1-1 .et_pb_image_wrap {
  padding-top: 100%;
  display: block;
}
.pa-image-1-1 .et_pb_image_wrap img {
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  object-fit: cover;
}
```
![image](https://github.com/user-attachments/assets/b7e54dfd-cc2d-44f5-b19c-c50831bf7710)


## Landscape 16:9 
– Proporción 9 / 16 = 0.5625 = 56.25%
```css
/*image aspect ratio landscape 16:9*/
  .pa-image-16-9 .et_pb_image_wrap {
    padding-top: 56.25%;
    display: block;
  }
  .pa-image-16-9 .et_pb_image_wrap img {
    position: absolute;
    height: 100%;
    width: 100%;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    object-fit: cover;
  }
```
![image](https://github.com/user-attachments/assets/f5807382-c952-4079-b9ee-ecf97edc105f)


## Landscape 4:3 
– Proporción 3 / 4 = 0.75 = 75%
```css
/*image aspect ratio landscape 4:3*/
.pa-image-4-3 .et_pb_image_wrap {
  padding-top: 75%;
  display: block;
}
.pa-image-4-3 .et_pb_image_wrap img {
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  object-fit: cover;
}
```
![image](https://github.com/user-attachments/assets/b0b5835b-dd1e-4a9f-9ae9-278af92b20bc)


## Landscape 3:2 
– Proporción 2 / 3 = 0.6667 = 66.67%
```css
/*image aspect ratio landscape 3:2*/
.pa-image-3-2 .et_pb_image_wrap {
  padding-top: 66.66%;
  display: block;
}
.pa-image-3-2 .et_pb_image_wrap img {
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  object-fit: cover;
}
```
![image](https://github.com/user-attachments/assets/d1ef914c-749b-4fb3-aaad-4570ad8091a6)


## Portrait 9:16  
– Proporción 16 /9 = 1.7778 = 177.78%
```css
/*image aspect ratio landscape 9:16*/
.pa-image-9-16 .et_pb_image_wrap {
  padding-top: 177.77%;
  display: block;
}
.pa-image-9-16 .et_pb_image_wrap img {
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  object-fit: cover;
}
```
![image](https://github.com/user-attachments/assets/5d1945e1-5190-43cd-a229-0cf594736d3f)


## Portrait 3:4  
– Proporción 4 / 3 = 1.3334 = 133.34%
```css
/*image aspect ratio landscape 3:4*/
.pa-image-3-4 .et_pb_image_wrap {
  padding-top: 133.33%;
  display: block;
}
.pa-image-3-4 .et_pb_image_wrap img {
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  object-fit: cover;
}
```
![image](https://github.com/user-attachments/assets/6c4ad30b-7703-45a0-b235-775d4fa319bd)


## Portrait 2:3  
– Proporción 3 / 2 = 1.5 = 150%
```css
/*image aspect ratio landscape 2:3*/
.pa-image-2-3 .et_pb_image_wrap {
  padding-top: 150%;
  display: block;
}

.pa-image-2-3 .et_pb_image_wrap img {
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  object-fit: cover;
}
```
![image](https://github.com/user-attachments/assets/8ca18fad-3765-40db-8c9d-c3f89900f7c5)


### Problemas con móviles 

!!! warning
      
      Cuando no funcione en móvil, una opción un poco bruta pero efectiva es ponerle !important a todos los ajustes.

!!! tip

    Después de hacer varias pruebas nos dimos cuenta de que algo en Divi estropeaba la compatibilidad del código o lo  sobreescribía y no se aplica

Ejemplo:

  ```css
  /*image aspect ratio landscape 16:9*/
  .pa-image-16-9 .et_pb_image_wrap {
    padding-top: 56.25% !important;
    display: block !important;
  }
  .pa-image-16-9 .et_pb_image_wrap img {
    position: absolute !important;
    height: 100% !important;
    width: 100% !important;
    top: 0 !important;
    left: 0 !important;
    right: 0 !important;
    bottom: 0 !important;
    object-fit: cover !important;
  }
  ```
