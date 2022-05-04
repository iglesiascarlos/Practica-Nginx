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

1. Lo primero que haremos será dirigirnos a la carpeta de sites-availeble, ahí lo que encontraremos será el archivo de bienvenida default, aquí crearemos los dos archivos para las dos páginas que queremos desplegar
```BASH
 > cd /etc/nginx/sites-available/
```
<img width="741" alt="Captura de Pantalla 2022-05-04 a las 17 13 12" src="https://user-images.githubusercontent.com/91618773/166712954-80c3fd70-b723-49e6-a673-a11402c12d04.png">

```BASH
 > sudo cp default clock.minimalist.com
 > sudo cp default asci.camera.com
 > sudo rm default
```
2. una vez creado las carpetas para dichas páginas veremos que la carpeta nos queda algo así:
 <img width="838" alt="Captura de Pantalla 2022-05-04 a las 17 19 55" src="https://user-images.githubusercontent.com/91618773/166714368-bad1ca36-6b9f-45ba-a209-9077b4a8bd05.png">
 
3. A continuación 
