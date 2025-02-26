<img src="https://github.com/user-attachments/assets/b082bb20-05be-4ed1-bb10-3b06a82ca046" alt="Texto alternativo" width="300" height="300">


## Como añadir que wordpress permita subir archivos SVG

#### Dirígete a public_html → wp-includes. Desplázate hacia abajo hasta que encuentres functions.php y edita el archivo

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
> [!IMPORTANT]
> #### Guarda el archivo y recarga el administrador de Worpress
