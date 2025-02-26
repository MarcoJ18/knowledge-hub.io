Sí, hay problemas al enviar o recibir email desde la web, tras la migración. 
Tener en cuenta esto. Hay que configurar manualmente el SMTP, tanto en PrestaShop o WordPress o cualquier CMS.

## Wordpress

Instalar e activar el plugin **WP Mail SMTP**

1. Saltar la configuración inicial
2. Ir al ajustes -> general
3. Añadir lo correspondiente:

![image](https://github.com/user-attachments/assets/02668945-b35e-4ab1-a6e6-01675a8d3d60)

4. Añadir el servidor con el usuario y constraseña del correo:
   
![image](https://github.com/user-attachments/assets/dd4f9c52-452a-49e0-ad92-dc0ad47fff22)

5. Generar correo de prueba:
   
![image](https://github.com/user-attachments/assets/3b71fe34-16ce-4e10-8786-b2f7a3162ed7)

6. Resultado:

![image](https://github.com/user-attachments/assets/9fd2d413-b3e9-4635-a384-19fcb08b1a08)

## Prestashop

PrestaShop en el apartado de la **configuración avanzada** > **email**. 
El cifrado debe ser **TLS**, por el **puerto 587**
  
