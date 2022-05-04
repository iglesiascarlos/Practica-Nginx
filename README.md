# Instalación y configuración del servidor web Nginx
A continuación vamos a explicar por encima como se realiza la instalación de Nginx en una máquina ubuntu y profundizaremos en la configuración que hay que realizar para poder hacer funcionar nginx y desplegar dos proyectos (HTML + CSS) haciendo que cada uno este desplegado en subdominios diferentes

## Instalación de Nginx
* Para iniciar la instalación de Nginx lo que haremos será abrir la consola e introducir el siguiente comando:
```BASH
 > sudo apt-get install nginx
```
* Con este comando conseguiremos instalar nginx en nuestro ordenador linux o maquina virtual (como es en mi caso)

<img width="699" alt="Captura de Pantalla 2022-05-04 a las 16 53 41" src="https://user-images.githubusercontent.com/91618773/166708404-fe7bbdd8-d653-4bb4-a598-06480da67ea8.png">

* Una vez esta instalado Nginx podemos abrir mozilla y si ponemos nuestro localhost podremos ver la página sin configurar de Nginx "Welcome to nginx"
<img width="702" alt="Captura de Pantalla 2022-05-04 a las 16 55 36" src="https://user-images.githubusercontent.com/91618773/166708839-ffa927af-0b17-4524-9c1d-d67e893ad5db.png">

## Configuración
* Una vez tenemos instalado Nginx podemos proceder a configurarlo y empezar a prepararlo para desplegar en dos subdominios diferentes los dos proyectos HTML + CSS

