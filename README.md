## Seminario de Administración de Sistemas  
**Clase:** Sistemas Operativos  
**Nombre:** Erick Daniel López Calderón 
**Carné:** 1890-20-3191  

---
## Introducción:
---
**Webmin** Es una herramienta basada en web para la administración de sistemas Unix/Linux. Proporciona una interfaz gráfica amigable que permite configurar servicios y recursos del sistema como usuarios, discos, servicios de red, Apache, DNS, entre otros, sin necesidad de utilizar la línea de comandos. Su enfoque es facilitar la administración remota y centralizada de servidores.

---
## Desarrollo:
---
> A continuación, se ejecutarán los pasos a realizar para poder instalar Nginx y NodeJS para el proyecto en cuestión.

# Comandos a utilizar para instalar Nginx:   
## 1. Actualizar paquetes con el siguiente comando: 
>Sudo apt update (o solo apt update si da error con el anterior).
## 2. Instalar Nginx:
>Sudo apt install nginx -y (o sin el sudo si da error con el anterior).
## 3. Para ver si Nginx se instaló sin errores, utilizar el siguiente comando:
>Sudo sistemctl status nginx.

## (Opcional) Si Nginx aparece como inactivo o no está corriendo, ejecutar los siguientes comandos: 

>Sudo systemctl enable nginx 
>Sudo systemctl start nginx.  

## Para verificar si funciona, ejecutar lo siguiente:
Sudo systemctl is-active nginx 
(debe aparecer “active” nada más al ejecutar este comando)

## Para ver si sí está instalado, debemos irnos a la parte de File Manager y buscar la carpeta “etc”. Dentro de esta, encontraremos la carpeta de nginx
---
##Pasos para instalar NodeJS en el servidor: 
---
# Comandos a utilizar para instalar NodeJS:   
## 1. Actualizar paquetes con el siguiente comando: 
>Sudo apt update (o solo apt update si da error con el anterior).
## 2. Instalar NodeJS y NPM con:
>Sudo apt install nodejs npm -y (o sin el sudo si da error con el anterior).
## 3. verificamos versiones instaladas con el siguiente comando:
>Node --version 
>Npm –version

## (Opcional) para ver si funciona NodeJS, vamos a crear un proyecto de prueba: 

>Echo ‘console.log(“Node.js está funcionando!”);’ > test.js 
>Node test.js   

## Para verificar si funciona, ejecutar lo siguiente:
Sudo sysxtemctl is-active nginx 
(debe aparecer “active” nada más al ejecutar este comando)

## Ya al verificar que el proyecto de prueba funcionó, podemos limpiarlo con: 
>Rm test.js

---
## Conclusión
---
Durante la realización de esta actividad, entendí de qué manera una aplicación como **Webmin** puede facilitar en gran medida la gestión de un sistema operativo Linux. Tuve la oportunidad de observar de manera práctica cómo manejar varios servicios del sistema a través de una interfaz web, lo que elimina la obligación de memorizar comandos complicados. Asimismo, fortalecí lo que sé acerca de la organización de archivos, usuarios y servicios internos del sistema.

---

## Observaciones Adicionales

- La instalación de Webmin requiere considerar temas de seguridad, especialmente si se expone a internet. Es recomendable trabajar sobre HTTPS y restringir el acceso por IP como se hizo en esta practica.
- Nunca exponer Node.js directamente - Solo el puerto 80/443 debe estar abierto.
- Configurar firewall correctamente - Denegar acceso directo al puerto 3000.
- No ejecutar Node.js como root - Crear usuario específico para la aplicación.
- Instalar SSL/HTTPS para producción usando Certbot.
  
