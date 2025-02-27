---
title: Eliminar Barra Lateral Divi
description: Tutorial para Eliminar la barra lateral en Divi cuando usamos Woocomerce y no hay forma de eliminarla más que con CSS personalizado
date: 2025-02-27
author: Adrián González
---

!!! bug

    Cuando en divi añadimos Woocomerce, este creará las páginas de tienda, productos, etc con una barra lateral que nos será prácticamente imposible de eliminar.
    Podemos vaciarla pero nos seguirá sin dar el acceso al ancho completo de la página.

### Paso 1. Acceder al Divi

- Para solucionar esto debemos eliminar por CSS personalizado la barra lateral.
- Accedemos a Divi -> Opciones del Tema -> CSS Personalizado (abajo del todo).

  ![image](https://github.com/user-attachments/assets/fd4a35df-ef3d-4b1a-8ea5-5362d4c8f5e9)

### Paso 2. Añadimos el código

- Añadimos el siguiente código personalizado al cuadro de texto que aparece en la imagen.
```css
*** 
 * ELIMINAR SIDEBAR Y AGRANDAR LEFT-BAR
 * Take out the divider line between content and sidebar 
***/
#main-content .container:before {background: none;}
  
/*** Hide Sidebar ***/
#sidebar {display:none;}
  
/*** Expand the content area to fullwidth ***/
@media (min-width: 981px){
#left-area {
    width: 100%;
    padding: 23px 0px 0px !important;
    float: none !important;
}
}
```

### Paso 3. Guardar

- Guardar cambios

  ![image](https://github.com/user-attachments/assets/b7f2a638-d1d7-4747-937c-2ee26b248f9e)
