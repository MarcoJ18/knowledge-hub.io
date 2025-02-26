# Crear un SLIDER para la página de inicio de la web
> [!NOTE]
> También se puede usar en otro lado de la web pero es recomendable en el Inicio

#### Documentación
Tutorial de Youtube: [🔴🔴🔴](https://youtu.be/RxnnBYeceDM?si=0eIahohWAFFlJMr_)

Página del código: [📄](https://ovdivi.com/como-crear-un-background-slideshow-con-efectos-de-animacion-y-transicion-en-divi-sin-plugins/)


### Paso 1.

- [ ] Colocar el elemento código en la sección donde queramos añadirlo

- [ ] En la zona del código pegaremos lo siguiente:

      <link rel="stylesheet" href="https://jaysalvat.github.io/vegas/releases/latest/vegas.min.css">
      <script src="https://jaysalvat.github.io/vegas/releases/latest/vegas.js"></script>
      
      <script>
      jQuery(document).ready(function($){
      $("#ovSlideshow").vegas({
        overlay: true,
        transition: 'fade',
        transitionDuration: 2000,
        delay: 5000,
        animation: 'random',
        animationDuration: 10000,
        slides: [
          { src: "https://undofisioterapia.es/wp-content/uploads/2025/01/pexels-karolina-grabowska-4506169-scaled.jpg" },
          { src: "https://undofisioterapia.es/wp-content/uploads/2025/01/pexels-yankrukov-5794024-scaled.jpg" },
          { src: "https://undofisioterapia.es/wp-content/uploads/2025/01/pexels-ryutaro-5473177-scaled.jpg" },
          ]
      });
      });
      </script>

- [ ] Para cambiar las imágenes de que aparecen, simplemente cambiar la parte de
      ```html

      slides: [
          { src: "https://undofisioterapia.es/wp-content/uploads/2025/01/pexels-karolina-grabowska-4506169-scaled.jpg" },
          { src: "https://undofisioterapia.es/wp-content/uploads/2025/01/pexels-yankrukov-5794024-scaled.jpg" },
          { src: "https://undofisioterapia.es/wp-content/uploads/2025/01/pexels-ryutaro-5473177-scaled.jpg" },
          ]
      ```

### Paso 2.

- [ ] Ahora añadimos el ID de Clase al bloque "ovSlideshow"
      
  ![image](https://github.com/user-attachments/assets/51bd1f22-999c-4e46-821f-291dd0b10222)

- [ ] Guardamos y salimos del editor, se recargará la página y podremos ver el slider en funiconamiento

>[!NOTE]
> ¿No ves bien las imágenes? Es probable que el tamaño del bloque sea demasiado pequeño, aumentale la altura a la que desees y las imágenes se redimencionarán
