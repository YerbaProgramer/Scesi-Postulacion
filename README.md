#Trabajo Individual 
Kevin Antonio Antezana Florero

##Clase 1
### ¿Que es GIT?

Es un sistema de control de versiones distribuido(VCS).
Permite guardar archivos y las versiones de estos.

### ¿Quien creo GIT?

Linus Torvalds es el creador de GIT.
Tardo de 2-3 semanas en crear el programa original (Lo hizo en un estado de ira)

### Instalacion de GIT en Linux Ubuntu 

sudo apt install git

Se discutio sobre el sistema de puntuacion del curso.

##Clase 2

###Estados del GIT

Modificado:Untacked y Unmodified
Stage Area:git add<archivo>,git add
Repositorio Local:git commit -m "mensaje" y git reset --soft Head~1

###Buenas Practicas

¿Cada cuanto debo hacer un commit?
-commits atomicos
Escribir Buenos Commits
-Usar verbos imperativos(Add,Change,Fix,Remove)
-No uses punto final ni puntos suspencivos en tus mensajes
-Usa como maximo 50 caracteres:
-Usa un prefijo para tus commits para hacerlos mas semanticos
-Añade todo el contexto que sea necesario en el cuerpo del commit

##Clase 3

###Github y SSH

###¿Que es Github?

Plataforma en la nube y red social para desarrolladores.

Permite alojar,gestionar y colaborar en proyectos de sofware.

###Git vs Github

-Git es un sistema de control de versiones(Crea puntos de guardado)
-Github es un servidor donde esos puntos se almacenan

###SSH vs HTTPS

Si queremos clonar y queremos usar un repositorio con HTTPS nos pedira autenticarnos con un token(Puede llegar a ser molesto).

Si configuramos nuestro equipo con SSH para comunicarnos con Github mediante una key que sera permanente.

Resumen siempre usar SSH

###Configuracion SSH

ssh-keygen -t ed25519 -c "tu-correo@email.com"

cat ~/ .ssh/id_ed25519.pub

Copiar la key de nuestro perfil de Github en configuracion.

ssh -T git@github.com

###Crear un repositorio en Github

1.En Github en repositorios hacer click en "New"

2.Colocar nombre al repositorio y opcionalmente una descripcion y hacer click en "Create Repository"

##Clase 4

###Remote SSH multiple y checkout

###Git Remote

Es el comando que permite gestionar nuestras conexiones con los repositorios remotos, le dice a GIT local donde enviar o donde traer la informacion
-git remote -v(Permite ver las URLs exactas donde apunta nuestro repositorio)
-git remote add <apodo> "url"(Vincula nuestro repo local con uno en la nube)
-git remote set-url <apodo> "url" (Cambia la url de nuestro repo)

###Multiples SSH

Multiples llaves de acceso para acceder a diferentes repositorios.

###Configurar Multiples SSH

Paso 1:Generamos el SSHKey

Paso 2:Creamos un archivo config para que no choquen con las key

Paso 3:Verificar si funciona 

###Configuraciones Locales 

Esta configuracion se impone a las globales y solo funcionan con el repositorio en el que se aplica
git config user.name"Mi nuevo Name"
git config user.email"micorreo@gmail.com"

###Git Checkout

Es un comando que permite desplazar el HEAD (lector actual) hacia un punto especifico del historial o una rama distinta.

¿Para que sirve?
-Inspeccionar
-Restaurar
-Experimental
-Cambiar

##Clase 5

###Ramas y Gitflow Basico

La base del trabajo remoto y en equipo

###¿Que son las ramas?

Son una de las principales utilidades que disponemos en GIT para llevar un mejor control del codigo.

###Git Branch

Comando que permite gestionar las ramas que tiene o tendra el proyecto

1."git branch"Permite listar ramas disponibles y nos muestra la posicion del HEAD.

2."git branch <rama>"Crea una rama a partir de la rama que estamos posicionados.

3."git branch -D <rama>"Borra la rama.

###Git Checkout enfocado en ramas

-git checkout <rama> :Cambia de ramas

-git checkout -b <rama> :Crea una rama y te mueve a ella directamente.

###Git Checkout VS. Git Switch

Originalmente "git checkout" estaba sobrecargado:Cambio de rama, viajar a commits antiguos y restaurar archivos.

En 2019 se introdujo "git switch" para separar la navegacion de ramas del resto de funciones.

git checkout:Multiproposito.

git switch:Especializado unicamente en ramas y evita errores accidentales.

###Gitflow Basico

Flujo de trabajo el cual nos permite trabajar de manera ordenada nuestras ramas, pues atraves de ciertas consignas y reglas establecidas,nos permite trabajar ordenadamente con ramas y versiones y unafacil adadtacion para cualquiera que quiera aportar en nuestro proyecto.
