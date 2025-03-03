---
title: Error Web Mail

---

!!! note

    Sí, hay problemas al enviar o recibir email desde la web, tras la migración. 
    Tener en cuenta esto. Hay que configurar manualmente el SMTP, tanto en PrestaShop o WordPress o cualquier CMS.

## Error Web Mail

### Paso 1. Instalar Plugin

1. Instalar e activar el plugin **WP Mail SMTP**
2. Saltar la configuración inicial
3. Ir al ajustes -> general

### Paso 2. Añadir información correspondiente

- Añadir lo correspondiente según la imagen y el correo del cliente:

  ![image](https://github.com/user-attachments/assets/a978e353-1874-4d2b-b2cb-3fb6c49f84dd)


- Añadir el servidor con el usuario y constraseña del correo:
   
  ![image](https://github.com/user-attachments/assets/97d00ece-d676-47c5-8b29-3ec8a7b83320)

### Paso 3. Probar el funcionamiento
!!! tip

    WPMail tiene una herramienta que nos permite probar que todo funcione bien, la usaremos para corroborar que el funcionamiento es correcto.

- Vamos a Herramientas -> Correo de prueba -> ponemos ahí nuestro correo para ver si nos llega
   
  ![image](https://github.com/user-attachments/assets/fb6dcaa6-049e-4b38-bfbd-2a26938b34eb)

- Nos tiene que llegar al correo que hemos puesto algo así:

  ![image](https://github.com/user-attachments/assets/83027a41-199d-4b95-b252-c1e554803fac)

### Prestashop
!!! warning

    En el caso de usar PrestaShop, en el apartado de la **configuración avanzada** > **email**. 
    El cifrado debe ser **TLS**, por el **puerto 587**
  
