# Instalar TPV como método de pago para Comercio electrónico

### Necesario:
- El cliente debe solicitar los datos del TPV al banco y pasarnoslo para añadirlo

>[!NOTE]
> Tener en cuenta que primero se añade en el entorno de pruebas y luego nos darán acceso a producción

### Paso 1 - Instalación del plugin
- [ ] Descargar el módulo específico de la tienda desde la página de Redsys: [Link↗️](https://pagosonline.redsys.es/desarrolladores-inicio/documentacion-tipos-de-integracion/modulos-pago/)

![image](https://github.com/user-attachments/assets/80a4f58b-b997-41f6-a0d7-5b4cd2023d54)

- [ ] Añadimos el plugin a Wordpress

### Paso 2 - Ajustes del Plugin
- [ ] Entramos en los ajustes del plugin "Pasarela de pago"
- [ ] Activamos la opción "Redirección a pasarela unificada de Redsys" (y algún otor como bizum si el cliente así lo quisiera)

![image](https://github.com/user-attachments/assets/07c81f6a-43fe-4d6f-ae9d-5c10468dcab5)

- [ ] Y le damos a "Finalizar configuración"
- [ ] Nos aparecerá un formulario donde debemos rellenar los datos del cliente en los 3 siguientes campos y guardar

![image](https://github.com/user-attachments/assets/97e71886-31b5-4ed0-b395-024a5b4dca9c)

### Paso 3 - Probamos la compra
- [ ] Con la tarjeta de prueba que nos proporcionaron probar a hacer una compra y realizar captura de cada paso.

![chrome_L5DvrLlMpx](https://github.com/user-attachments/assets/12dd3f5d-8c4e-4e44-897f-b1b7d451b1ea)

![chrome_XtgZPbQuVL](https://github.com/user-attachments/assets/a146fc95-abab-4c96-bc96-81d97b58c5f2)

### PAso 4 - Notificar el pase a producción a Redsys
-  [ ] Enviaremos un correo a Redsys al mail que nos indican en el manual:
       
     ```
     virtualtpv@comerciaglobalpay.com
     ```
![chrome_vjtPd9Ua5z](https://github.com/user-attachments/assets/c4301d03-ddfc-4e4f-b6a4-115bc700e107)

- [ ] Añadiremos el siguiente texto, donde el nº de comercio sea el del cliente y añadirle capturas de verificación correspondientes
```
Nº de Comercio: [nº de comercio correspondiente]

Hemos realizado las pruebas con éxito y solicitamos el paso a producción. Adjuntamos capturas de verificación

```

- [ ] Enviamos y esperamos la respuesta.
