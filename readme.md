# Configuración e Instalación de las herramientas
## Probado en Ubuntu 18
### Instalando el IDE y puesta en marcha del proyecto
1. También instalo Git, Virtualenv y algunas utilidades
```
sudo apt-get install git virtualenv python3-pip software-properties-common
```
2. Personalmente utilizo la versión Community de PyCharm y funciona que es un encanto ;)
```
sudo snap install pycharm-community --classic
```
3. Una vez instalado PyCharm, creo una carpeta de espacio de trabajo y dentro una de proyectos
```
mkdir ~/workspace
mkdir ~/workspace/projects
```
4. Con PyCharm, dentro de la carpeta `projects`, creo la carpeta del proyecto (asegurarse que cree un entorno virtual) y lo enlazo a un repositorio de Github. 

### Instalando Quasar Framework
1. Agregar el PPA de NodeJS (ejecutarlo textualmente)
```
wget -qO- https://deb.nodesource.com/setup_10.x | sudo -E bash -
```
2. Instalar NodeJS normalente
```
sudo apt-get install -y nodejs
```
3. Instalar Quasar Framework
```
sudo npm install -g quasar-cli
```
4. Hay que instalar @vue/cli y @vue/cli-init de forma global también
```
sudo npm install -g @vue/cli
sudo npm install -g @vue/cli-init
```
5. Dentro de la carpeta del projecto creo el directorio para el Frontend con Quasar
```
quasar init [nombre_del_directorio]
```
### Instalando Django
1. Abro el PyCharm y abro el proyecto que creamos anteriormente, abro la consola y me aseguro que este el ambiente virtual activo
```
pip install django
django-admin startproject [nombre_del_proyecto_django]
cd [nombre_del_proyecto_django]
pip freeze > requirements.txt
./manage.py startapp [nombre_de_la_app]
```
2. Finalmente hacemos el primer commit a Github.
