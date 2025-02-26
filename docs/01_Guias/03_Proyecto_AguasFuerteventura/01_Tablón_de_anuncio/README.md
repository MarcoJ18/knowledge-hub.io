# Añadir publicaciones en AguasFuerteventura

Web a la que se le hace referencia: [tablóndeanuncios](https://www.aguasfuerteventura.com/tablon.php)

## Añadir un anuncio nuevo

Ir a la siguiente ruta dentro del `Cpanel > Administración de Archivos`:

![image](https://github.com/user-attachments/assets/c9022c0d-1063-47d9-ad4f-e014e494aefe)

En el fichero `/public_html/tablon_anuncios/anuncios.json` abra un json en el cual podras subir el correspondiente anuncio que nos pasa el usuario:

![image](https://github.com/user-attachments/assets/909e46e9-f1d2-4249-9375-89888f0ed406)

El usuario nos pasara un fichero donde pondra titulo del anuncio con un PDF, lo que tenemos que hacer es completar el contenido del Word al JSON:

![image](https://github.com/user-attachments/assets/35f368d0-e141-4063-9f4b-4ea031d4e8ae)

El usuario nos pasara un PDF ese hay que subirlo a la carpeta:`/public_html/documentos`:

![image](https://github.com/user-attachments/assets/c1f80550-d0eb-44e2-b8dd-eed5461fa34e)


> [!CAUTION]
> Cuando se añade una publicación nueva, debes agregar una nueva linea en el json.<br>
> Ejemplo:
> ```json
>[
>    {
>        "_comentario":"Publicación ejemolo",
>        "titulo": "ejemplo",
>        "texto": "ejemplo",
>        "archivo": "documentos/ejemplo.pdf"
>    },
>    {
>        "_comentario":"Publicación ejemolo",
>        "titulo": "ejemplo",
>        "texto": "ejemplo",
>        "archivo": "documentos/ejemplo.pdf"
>    },
>      {
>        "_comentario":"Publicación ejemolo",
>        "titulo": "ejemplo",
>        "texto": "ejemplo",
>        "archivo": "documentos/ejemplo.pdf"
>    }
>    
>]
> ```


