# Comandos de github explicados

## 1. Configuracion inicial (SOLO LA PRIMERA VEZ)-git config

1. Configuracion de tu nombre de usuario 

``` markdown
git config --global user.name "Tu nombre"
```


2. configuracion de tu correo electronico

``` markdown
git config --global user.email "email.com"
```

## 2. Crear un nuevo repositorio-git init

### inicializar un nuevo repositorio

``` markdown
git init
```

- El comando git init se utiliza para crear un repositorio en tu computadora

- Un repositorio es un lugar donde se guarda y se controla el historial de versiones

- Al ejecutar git init le dices a github que quieres que la carpeta donde la ejecutaste sea administrado por git 

### Explicacion

1. Inicia Git en un directorio: Cuando corres el comando git init dentro de una carpeta, Git configura esa carpeta para que sea un repositorio. Esto significa que a partir de ese momento, Git puede rastrear los cambios que hagas en los archivos dentro de esa carpeta.

2. Crea una carpeta oculta: Git crea una subcarpeta oculta llamada .git dentro de la carpeta donde ejecutaste el comando. Esta subcarpeta contiene todos los archivos y datos necesarios para el funcionamiento del repositorio, como el historial de cambios, configuraciones, etc.

3. No modifica tus archivos: Ejecutar git init no cambia ni mueve los archivos que ya están en la carpeta. Simplemente prepara el entorno para que puedas empezar a rastrear los cambios con Git.

4. Punto de partida: Después de ejecutar git init, puedes empezar a añadir archivos al repositorio, hacer commits (guardar instantáneas de tu trabajo), y utilizar todos los comandos y funcionalidades de Git para manejar tu proyecto.

## 3. Preparar archivos que quieres subir a tu repositorio-git add .

``` markdown
git add .
```

``` markdown
git add "archivo especifico"
```

git add se utiliza para preparar o stagear archivos que quieres incluir en tu proximo commit en git.

-  un commit es donde se indica que cambios se subiran a el repositorio

### ¿Qué hace exactamente git add?

Cuando haces cambios en los archivos de tu proyecto, Git detecta esos cambios, pero no los incluye automáticamente en el próximo commit. Primero necesitas usar git add para decirle a Git cuáles archivos y cambios quieres que sean parte del próximo commit.

## Confirmar los cambios con un mensaje descriptivo de que se hizo-git commit

para confirmar y guardar los cambios que haras tienes que usar

```markdown
git commit -m "Mensaje de lo que se hizo"
```

## Para subir los cambios al repositorio remoto-git push

Una vez ya hecho ```git add .``` para agregar los cambios realizados y luego hacer el
```git commit -m "mensaje de lo que se hizo" ``` para confirmar y guardar los cambios toca hacer ```git push```

``` markdonw
git push
```
este se utiliza para subir los archivos a tu repositorio en la nube 

## Crear nueva rama de trabajo-git checkout

Crear una nueva rama de trabajo podria servir para hacer testeos sin afectar al producto final ver como se verian cosas diferentes que no seran implementadas entre otras cosas

### crear nueva rama

``` markdown
git checkout -b nombre-de-la-rama
```

### cambiar de rama

``` markdonw
git checkout nombre-de-la-rama
```

### Subir una nueva rama al repositorio remoto:

``` markdown
git push -u origin nombre-de-la-rama
```
##  Actualizar tu Repositorio Local con Cambios Remotos-git fetch
git fetch es un comando de Git que se utiliza para obtener los últimos cambios y actualizaciones del repositorio remoto, pero sin fusionarlos automáticamente en tu rama actual. Es decir, git fetch descarga los datos de los commits, ramas y etiquetas del repositorio remoto para que puedas verlos y decidir qué hacer con ellos, pero no altera tu código local ni tu historial de commits.

``` markdown   
git fetch
```
esto actualizara todas las ramas remotas, si quieres btener cambios de una rama especifica haz 

```markdown
git fetch origin main
```
