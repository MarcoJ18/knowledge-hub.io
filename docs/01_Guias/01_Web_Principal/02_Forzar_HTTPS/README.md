---
title: Forzar HTTPS 
description: Se detallan los pasos a seguir para instalar y renovar automáticamente el certificado SSL y para forzar el HHTPS.
author: Adrián / Anna
date: 18/03/2025
---

# Forzar HTTPS


!!! note

    Debemos realizar esto cuando tengamos la web o si da algún problema de HTTP

### Paso 1. Acceder al Cpanel > Ir al apartado de SSL
Herramientas > Seguridad > SSL/TLS Status

![image](https://github.com/user-attachments/assets/69756033-f880-46df-a5f8-e48f11f4db1b)

!!! warning

    Selecinar el domino principal se muestra en en este apartado:
    ![image](https://github.com/user-attachments/assets/1752ac6c-1a84-4051-8db4-d7d585c62e40)

Luego seleccionamos dicho dominio y ejecutamos AutoSSL
![image](https://github.com/user-attachments/assets/7e81bfe9-0e53-4440-a2df-2f3491a0b8a6)



### Paso 2. Forzar HTTPS en Dominio.
Herramientas > Dominos > Dominios 

![image](https://github.com/user-attachments/assets/299285f8-6070-4600-a978-18da8e456de2)


Activar **forzar hhtps**, tal y como se vé en la captura de pantalla.

![image](https://github.com/user-attachments/assets/7abdefe4-167e-4160-b273-34fbd2423795)




