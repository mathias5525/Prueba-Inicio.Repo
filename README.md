# Comienza el Readme
---
# Clase 1
---

Ha comenzado el repositorio. 

```sh
    cd Documents
    mkdir Proyectos
    git clone https://github.com/mathias5525/Prueba-Inicio.Repo.git
    cd Prueba-Inicio.Repo
    git pull origin main
    git fetch
    git branch  # veran que esta la rama main por defecto
    touch README.md  # creamos el readme
    git staus
    git add .
    git commit -m "Creacion del readme"
```

## Agregamos este trabajo en el readme online

> ¿Como hacemos este?

Ingresamos al repositorio y luego solo presionamos punto <br>

```sh
    .
```

Ingresamos toda esta informacion y terminamos.

---
# Clase 2
---

# Cargar la llave SSH pública en GitHub

## Generar y copiar la llave SSH pública

Para copiar la llave pública, debes ir a la carpeta `.ssh` en tu computadora.  
Allí encontrarás un archivo con extensión `.pub` (por ejemplo, `id_rsa.pub`).

Puedes abrir este archivo con un editor de texto (como el Bloc de notas o VS Code) y copiar todo el contenido que contiene.

---

## Agregar la llave SSH a GitHub

1. Inicia sesión en tu cuenta de **GitHub**.  
2. Ve a **Settings → SSH and GPG keys**.  
3. Crea una nueva clave haciendo clic en **New SSH Key**.  
4. Asigna un nombre descriptivo (por ejemplo, el nombre del ordenador donde estás trabajando).  
5. Pega el contenido de la llave pública en el campo correspondiente.  
6. Guarda los cambios.  

> 💡 **Consejo:** Es recomendable que cada computadora o dispositivo tenga su propia llave SSH para acceder a tu cuenta de GitHub.

---

## Comandos básicos de Git

```bash
git branch  # Ver en qué rama estamos actualmente
git checkout master  # Cambiar a la rama master
git branch -M main  # Cambiar el nombre de la rama master a main
git remote add origin git@github.com:n  # Agregar el repositorio remoto
git remote -v  # Verificar si el repositorio remoto está correctamente conectado
git merge segunda  # Fusionar los cambios de la rama segunda en main
git commit -am "Uso de GitHub parte 20" #  Realizar un commit con un mensaje descriptivo
git push origin main  # Subir los cambios a GitHub
```

Cambio de nombre de rama principal en GitHub

Cuando renombramos la rama master a main, puede ocurrir que en el repositorio de GitHub se creen dos ramas: master y main.

Para corregirlo:

Ve al repositorio en GitHub.

Entra a Settings → Branches.

Cambia la rama principal (default branch) a main.

Luego de esto, puedes eliminar la rama master.

---
# Clase 3
---
Cambios en GitHub: de master a main

El escritor Argentino Julio Cortázar afirma que las palabras tienen color y peso. Por otro lado, los sinónimos existen por definición, pero no expresan lo mismo. Feo no es lo mismo que desagradable, ni aromático es lo mismo que oloroso.


Por lo anterior, podemos afirmar que los sinónimos no expresan lo mismo, no tienen el mismo “color” ni el mismo “peso”.

Sí, esta lectura es parte de la enseñanza profesional de Git & GitHub.

Desde el 1 de octubre de 2020 GitHub cambió el nombre de la rama principal: ya no es “master” -como aprenderás aquí- sino main.

Este derivado de una profunda reflexión ocasionada por el movimiento #BlackLivesMatter.

La industria de la tecnología lleva muchos años usando términos como master, slave, blacklist o whitelist y esperamos pronto puedan ir desapareciendo.

Y sí, las palabras importan.

Por lo que de aquí en adelante cada vez que me escuches mencionar “master” debes saber que hago referencia a “main”.

¿Cuando es que sigue siendo master y cuando sigue siendo main?
Cuando se crea un repositorio desde git bash en nuestro ordenador a través de git init, sigue siendo el estandar como master. ¿Qué hacer con esto? Debes cambiar el nombre de la rama master a main con el comando:

```bash
git branch -M main
```

O cambiando la asignación por default con este otro comando:

```bash
git config --global init.defaultBranch main
```

A partir de este comando siempre que ingreses git init será la rama main.

Ahora cuando creamos un repositorio desde la nube, osea desde GitHub, ya verás que la rama principal tiene por default el nombre de main y al clonar a nuestro ordenador seguira teniendo este nombre y no será necesario ningun cambio.
Otro comando que deben saber es:

```bash
gitk
```

Si no te funciona el comando gitk es posible no lo tengas instalado por defecto.
Para instalar gitk debemos ejecutar los siguientes comandos:

```bash
sudo apt-get update

sudo apt-get install gitk
```

Recuerda que podemos ver gráficamente nuestro entorno y flujo de trabajo local con Git utilizando el comando gitk. Gitk fue el primer visor gráfico que se desarrolló para ver de manera gráfica el historial de un repositorio de Git.

---
# Clase 4
---

Tu primer push
La creación de las SSH es necesario solo una vez por cada computadora. Aquí conocerás cómo conectar a GitHub usando SSH.

Luego de crear nuestras llaves SSH podemos entregarle la llave pública a GitHub para comunicarnos de forma segura y sin necesidad de escribir nuestro usuario y contraseña todo el tiempo.

Para esto debes entrar a la Configuración de Llaves SSH en GitHub, crear una nueva llave con el nombre que le quieras dar y el contenido de la llave pública de tu computadora.

Ahora podemos actualizar la URL que guardamos en nuestro repositorio remoto, solo que, en vez de guardar la URL con HTTPS, vamos a usar la URL con SSH:

```bash
ssh
git remote set-url origin url-ssh-del-repositorio-en-github
```

Comandos para copiar la llave SSH:

ESTAS SON LAS RUTAS DEL SSH PUBLICO

-Mac:
```bash
pbcopy < ~/.ssh/id_rsa.pub
```

Windows (Git Bash):
```bash
clip < ~/.ssh/id_rsa.pub
```

Linux (Ubuntu):
```bash
cat ~/.ssh/id_rsa.pub
```

Importante

Las buenas costumbres nos enseñan que antes de hacer un push, siempre debemos hacer un pull, un fetch, esto para que si alguien ya hizo algún cambio, no se genere un conflicto.

Invitar a un colaborador

Para invitar a un colaborador debemos ir a GitHub y seleccionar:
setting -> colaborators -> ingresar contraseña o un F2A de verificación y enviar la invitación escribiendo el nombre de usuario.

Del otro lado el usuario invitado solo debe aceptar y listo, ya puede participar del proyecto haciendo commit.

---
Clase 5
---

Git tag y versiones en GitHub

En Git, las etiquetas o Git tags tienen un papel importante al asignar versiones a los commits más significativos de un proyecto. Aprender a utilizar el comando git tag, entender los diferentes tipos de etiquetas, cómo crearlas, eliminarlas y compartirlas, es esencial para un flujo de trabajo eficiente.

Creación de etiquetas en Git

```sh
git tag -a v1.0 -m "Product release"

git tag -a ronburgundy -m "Brick killed a guy with a trident."
```

Sustituye con un identificador semántico que refleje el estado del repositorio en el momento de la creación. Git admite etiquetas anotadas y ligeras.

Listado de etiquetas
Para obtener una lista de etiquetas en el repositorio, ejecuta el siguiente comando:

```sh
git tag
```

Para crear una etiqueta, ejecuta el siguiente comando:

Las etiquetas anotadas almacenan información adicional como la fecha, etiquetador y correo electrónico, y son ideales para publicaciones públicas. Las etiquetas ligeras son más simples y se emplean como “marcadores” de una confirmación específica.


git tag

Esto mostrará una lista de las etiquetas existentes, como:

v1.0

v1.1

v1.2

Para perfeccionar la lista, puedes utilizar opciones adicionales, como -l con una expresión comodín.

Uso compartido de etiquetas

Compartir etiquetas requiere un enfoque explícito al usar el comando git push. Por defecto, las etiquetas no se envían automáticamente. Para enviar etiquetas específicas, utiliza:

```bash
git push origin
```

Para enviar varias etiquetas a la vez, usa:

```bash
git push origin --tags
```

Eliminación de etiquetas
Para eliminar una etiqueta, usa el siguiente comando:

```bash
git tag -d
```

Esto eliminará la etiqueta identificada por en el repositorio local.

En resumen, las etiquetas en Git son esenciales para asignar versiones y capturar instantáneas importantes en el historial de un proyecto. Aprender a crear, listar, compartir y eliminar etiquetas mejorará tu flujo de trabajo con Git.

---
Clase 6
---