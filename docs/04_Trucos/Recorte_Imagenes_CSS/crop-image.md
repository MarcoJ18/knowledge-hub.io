# CROP IMAGES

> [!CAUTION]
> En móvil se rompe bastante revisarlo bien o meterle !important a todo

## Añadir la clase al ccs
La clase dependerá de la relación aspecto que queramos, pero siempre tendrá el formato
#### pa-image-[primer aspect-ratio]-[segundo aspect-ratio]
##### Ejemplo -> Para ratio 16:9 -> pa-image-16-9 
![image](https://github.com/user-attachments/assets/99ae4d6c-1444-4e91-b9c4-8410232146a6)

## Añadir código a la imagen
#### Añadir el código que queramos usar dependiendo del aspect-ratio que queramos en el apartado de css personalizado
![image](https://github.com/user-attachments/assets/42aec466-0960-412f-9e4f-4c71efa02d54)


## Square 1:1 – 1 / 1 = 1.00 = 100%
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
![image](https://github.com/user-attachments/assets/d0232069-fb36-49bd-82b6-0cbd09784b1d)


## Landscape 16:9 – 9 / 16 = 0.5625 = 56.25%
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
![image](https://github.com/user-attachments/assets/a8fb2d6e-475a-4bd1-8f5c-7bbe1cb570bb)


## Landscape 4:3 – 3 / 4 = 0.75 = 75%
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
![image](https://github.com/user-attachments/assets/4ae9f525-c518-4efc-9224-0dfe844b1bb2)


## Landscape 3:2 – 2 / 3 = 0.6667 = 66.67%
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
![image](https://github.com/user-attachments/assets/5b84ea25-ec64-4687-a96e-9cbde6f00be3)


## Portrait 9:16 – 16 /9 = 1.7778 = 177.78%
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
![image](https://github.com/user-attachments/assets/1a445083-b4eb-4155-8b7b-8afa6ead3786)


## Portrait 3:4 – 4 / 3 = 1.3334 = 133.34%
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
![image](https://github.com/user-attachments/assets/ced2e9de-2e36-48d7-b495-dc44398b9497)


## Portrait 2:3 – 3 / 2 = 1.5 = 150%
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
![image](https://github.com/user-attachments/assets/1534f2b4-efe9-4ae3-85ad-70840f3d7b52)


## Cuando no funcione en móvil, una opción un poco bruta pero efectiva es ponerle !important a todos los ajustes
- Después de hacer varias pruebas nos dimos cuenta de que algo en Divi estropeaba la compatibilidad del código o lo  sobreescribía y no se aplica

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
