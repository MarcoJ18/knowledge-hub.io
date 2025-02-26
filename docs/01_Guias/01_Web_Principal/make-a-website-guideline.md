# Pasos para crear una web de kit digital desde cero.

- ### Conseguir dominio
    - [dominio.es](https://www.dominios.es/es)
- ### Instalar Wordpress desde Fuertehost
- ### Activar el Divi
    - Mandar ticket a "sered"? para que activen la licencia de Divi.
- ### Crear las cuentas de correo necesarias desde el CPanel
    - Redireccionar correo (info@[dominio].es)
  
      ![image](https://github.com/user-attachments/assets/d7710535-4b3d-4bed-95c3-b4348188f1b2)
      ![image](https://github.com/user-attachments/assets/85f0d51e-9d6f-4f87-b646-172f90c3f357)

- ### Revisar actualizaciones de plugins
    - Actualizar si hace falta los plugins que vienen instalados por defecto

        ![image](https://github.com/user-attachments/assets/411d1395-ee46-4a01-9174-ff2cd228fea8)

- ### Una vez activado el divi, crear las páginas
    - Al menos una estructura principal mínima según lo que haya pedido el cliente
      
        ![image](https://github.com/user-attachments/assets/5072a59b-e826-4607-be06-510919721a2f)

- ### Cambiar los enlaces permanentes
    - Ajustes > Enlaces permanentes > Nombre de la entrada
      
      ![image](https://github.com/user-attachments/assets/03c4c88f-58f4-4c02-9453-ff1f169a3ca9)

- Crear menú
- Añadir el footer.json
    1. Descargar Footeer.js dle repositorio
    2. Ir a theme Builder de divi
    3. Clicar en la imagen de importar (ver abajo)
    5. Importar desde archivo y se importará solo el footer
    6. Guardar Cambios
- Seleccionar la página de inicio como la que inicia el sitio
    1. Apariencia -> Personalizar
    2. Ajustes de página de inicio
    3. Seleccionar una página estática
    4. Y seleccionar como página de Inicio "Inicio"
- Editar encabezado
    1. Apariencia -> Personalizar
    2. Cambiar encabezado a gusto
- Empezar a editar con Divi
      1. Elegir un diseño para empezar

- Para formularios añadir reCaptcha v3
      1. buscarlo en google
      2. Entrar y añadir el sitio
      3. Copiar claves y añadirlas al form
  Si uso ContactForm 7 -> Contacto -> integración -> reCaptcha ->

- Completar Yoast SEO
    1. Ir al apartado de Yoast SEO y seguir con la foniguración inicial
    2. Ir a "editar" en la página de inicio y rellenar el apartado de Yoast SEO debajo
    3. Rellenar también "Básicos del sitio" y "Representación del sitio"

- Añadir idiomas
    1. Ir a plugis -> Gtranslate -> Ajustes
    2. En ajustes configurarlo como la siguiente imagen
     ![image](https://github.com/user-attachments/assets/79e5b09b-f520-459a-8a98-8695849a9bb5)
    4. Añadir el css personalizado al final
         ```css
       @media (min-width:1200px){
        .gtranslate_wrapper{
            display: flex;
            align-items:center;
            gap: 5px;}
    6. Vamos a menú -> Seleccionamos menú principal
    7. Añadimos un Enlace personalizado
    8. En url ponemos [gtranslate]
    9. Añadimos al menú
    10. Editamos la etiqueta de navegación y le ponemos [gtranslate] también
- Google My Business
- Indexación
    1. Google Search console
          - Añadir link de la Web
          - Copiar HTML tag
          - Ir a Yoast SEO -> Ajustes -> "General" - Conexiones del sitio
          - Pegar el HTML tag copiado
          - Ir a Search console y darle a verificar HTML tag
          - Realizar captura de que se añadió correctamente para la justificación
          - Compartir el Search console con Marco y Cristian
    2. Bing
          - Añadir link de la Web
          - Copiar HTML tag
          - Ir a Yoast SEO -> Ajustes -> "General" - Conexiones del sitio
          - Pegar el HTML tag copiado
          - Ir a Bing y darle a verificar HTML tag
          - Realizar captura de que se añadió correctamente para la justificación
          - Compartir el Search console con Marco
    3. Cylex
    4. Firmania
    5. Encuentre Abierto

- Justificación

Imagen importar:

![image](https://github.com/user-attachments/assets/09990795-580c-4b9d-9d1e-158a1ae0f401)
