---
title: Como añadir que wordpress permita subir archivos SVG
description: Tutorial para añadir que wordpress permita subir archivos SVG en Wordpress
date: 2025-02-26
author: Adrián González
---

<img src="https://github.com/user-attachments/assets/ede2c287-3910-4121-b8b3-69ead620f5ae" alt="Texto alternativo" width="100" height="100">

# Como añadir que wordpress permita subir archivos SVG en Wordpress

### Paso 1. Entrar en el archivo
- Entra al administrador de archivos del CPanel.
- Dirígete a public_html → wp-includes. Desplázate hacia abajo hasta que encuentres functions.php y edita el archivo

#### Al final del código añade el siguiente código
```php
/**
 * Funcion para habilitar svg
 */
function add_file_types_to_uploads($file_types){
    $new_filetypes = array();
    $new_filetypes['svg'] = 'image/svg+xml';
    $file_types = array_merge($file_types, $new_filetypes );
    return $file_types;
  }
add_filter('upload_mimes', 'add_file_types_to_uploads');
```

!!! danger

    Guarda el archivo y recarga el administrador de Worpress para que funcione.
