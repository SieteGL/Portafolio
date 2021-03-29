

Proyecto base para portafolio caso 5 Linda sonrisa.


Explicación de uso e instalacion de todo lo necesario para el funcionamiento.


Instalar Python https://www.python.org/downloads/releases recomiendo que todos tengamos la version 3.7.4 July 8, 2019


Luego de instalar python, crearemos una carpeta para guardar nuestro trabajo, dentro de esta crearemos 2 carpetas una llamada entorno y otra llamada LindaSonrisa
Dentro de linda sonrisa realizaremos la clonacion desde github.


Abrir CMD y dirigirse a la carpeta entorno.  Dentro de esta dirección ejecutaremos el comando |  python -m venv "nombre del entorno virtual". Ahora ejecutamos... cd nombre del entorno virtual    cd scripts     activate  (revisar que al inicio de la linea de comando entre parentesis aparezca el nombre del entorno virtual esto nos mostrara que esta activo.     Ahora ejecutamos el comando    pip install django.  esto instalara el framework django en nuestro entorno.


Ahora regresamos a la raiz donde estan las carpetas entorno y LindaSonrisa.


ingresamos a lindasonrisa mediante un cd  luego ejecutamos otro cd para ingresar a requirements  (dentro de esta carpeta se encuentran 2 archivos con extension .txt que uno es para el entorno local y otro para el de producción, se crea esta carpeta para ir actualizando los paquetes que se usan mediante pip, para que al momento de ejecutar no de mayores problemas).    una vez dentro de la carpeta requirements ejecutamos el comando   pip install -r local.txt esto descargara todos los pip desde el txt.


Ahora una vez todo descargado y listo para usar haremos un cd.. hasta llegar a LindaSonrisa donde se encuentran las 2 carpetas Lindasonrisa y requirements ahora realizaremos un cd para entrar en lindasonrisa y ahora podremos ejecutar nuestro proyecto.  python manage.py runserver   como saber si todo funciono, tendremos que tener acceso al link http://127.0.0.1:8000/ donde este mostrara la pantalla de django.


---------

*__init__.py — Un fichero vacío creado aquí para que Django/Python reconozca la carpeta como un Paquete Python y te permita usar sus objetos dentro de otras partes del proyecto.

Explicación de los archivos que componen el proyecto.

Tenemos 4 carpetas principales que se ven en la raíz y un archivo .py y un jsnon

1° Json-- Creado para ocultar información sensible para cuando es subida a repositorios, este deberia ser acompañado de un gitignore. Este contiene una KEY,DB_name,User,Password.

2° manage.py-- Este archivo nos permitira hacer las interacciones requeridas por la aplicacion desde la conexion a DB hasta el levantamiento.

3°LindaSonrisa-- Este archivo es el base del proyecto donde se encuentran los settings.py  pero por buena practica el archivo settings.py puede ser sub-dividido en 3 por esto creando la carpeta settings que en su interior cuenta con __init__.py  base.py local.py prod.py... Siendo en base.py donde se encuentran los django apps, local apps, thid party apps. siendo aqui donde informaremos de cambios en nuestros modulos. Local.py aca realizaremos la conexion con la base de datos en nuestro entorno local, tambien podremos realizar varias tareas mas.

4°Static-- Contiene los archivos estaticos de siempre.

5°Templates-- Templates necesarios para nuestro proyecto, puede servir para pruebas, ya que, sera un backend en API REST

6°Applications-- esta carpeta se crea para almacenar los modulos de nuestro proyecto y se crea de forma convencional no asi sus sub carpetas que van por line de comando.
para crear estas carpetas la linea de comando es...  django-admin startapp "nombre" esto nos traera una carpeta con sus archivos .py correspondientes en este caso users tiene extra urls-serializers-mixins-managers-forms(no es necesario para API)








