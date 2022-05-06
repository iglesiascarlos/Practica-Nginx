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
 
3. A continuación entraremos al archivo clock.minimalist.com y asci.camera.com y cambiaremos los siguientes parámetros:
```BASH
 > sudo nano clock.minimalist.com
 > sudo nano asci.camera.com
```
<img width="486" alt="Captura de Pantalla 2022-05-06 a las 21 45 14" src="https://user-images.githubusercontent.com/91618773/167207130-d3cb846c-c771-4213-940d-6f12be6f2a4e.png">
<img width="515" alt="Captura de Pantalla 2022-05-06 a las 21 46 20" src="https://user-images.githubusercontent.com/91618773/167207174-faed43a7-20eb-48da-9878-840a3915ca4e.png">

4. Una vez tenemos estos cambios, usaremos los siguientes comandos para crear un link simbólico que apunte a los archivos creados y modificados de nuestras dos webs.

<img width="1161" alt="Captura de Pantalla 2022-05-06 a las 21 49 52" src="https://user-images.githubusercontent.com/91618773/167207476-f86d8e8e-3bf9-45d9-bae8-52f3569269c6.png">

5. Despues de haber creado estos links simbólicos iremos a /var/www/ y ahí crearemos las dos carpetas necesarias: carlos y carlos2, cada una para su respectiva web. Una vez creadas las carpetas entramos en cada una de ellas, creamos el archivo index.html y pegamos el código de cada web respectivamente.
```BASH
 > cd var/www
 > mkdir carlos
 > mkdir carlos2
 > cd carlos
 > sudo nano index.html
 > cd ../carlos2
 > sudo nano index.html
```
<img width="781" alt="Captura de Pantalla 2022-05-06 a las 22 02 56" src="https://user-images.githubusercontent.com/91618773/167209078-ec0ae275-e75b-41bf-829f-68e6ab03afa4.png">

6. Por último iremos a la carpeta /etc y entraremos al archivo host para añadir las direcciones de las páginas, reiniciaremos nginx y ya podríamos visitar nuestras dos webs.

<img width="626" alt="Captura de Pantalla 2022-05-06 a las 22 06 27" src="https://user-images.githubusercontent.com/91618773/167209652-9f5e505f-4036-4aff-874e-40ebc1d11e1b.png">

<img width="340" alt="Captura de Pantalla 2022-05-06 a las 22 06 19" src="https://user-images.githubusercontent.com/91618773/167209675-fea49342-62d3-470a-b69a-a180fd0dbe77.png">
