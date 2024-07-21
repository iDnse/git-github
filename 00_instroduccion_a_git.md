# Git

  Sistema de control de versiones, registra los cambios realizados sobre el archivo o conjunto de archivo a lo largo del tiempo

  Este sistema permite realizar un seguimiento de las modificaciones realizadas por cada uno de los colaboradores del proyecto

  Revertir los cambios a un estado anterior o incluso el proyecto entero

  Mas sencillo detectar el error y quien lo genero

  En caso de perdida se puede es facil y sencillo recuperarlo

  Es de codigo abierto.

## Sistema de control de versiones

  1. Locales, la base de datos o de registro estan en local

  2. Centrales, la base o registro estan en un servidor central
  
  Los sistema de control replican completamente el repositorio, si un servidor muere, y estos tienen colaboradores, atraves de el cualquier repositorio se puede restaurar en otro servidor.

  Cada ves que descargues en realidad se hace una copia de seguridad completa de todos los datos, esto permite establecer varios tipos de flujos de trabajo 

## Git que es?

  - Creado por linus trovals
  - Control de versiones distribuida
  - Moderno y popular
  - Cada copia del repositorio es en verdad una copia de todo el proyecto
  - Funciona bien en entornos de integracion continua y entrega

## Fundamentos de Git

  1. Fotografia: git modela sus datos como un conjunto de fotos de un sistema de archivos y guarda una referencia a esa foto. Para ser eficiente, si los archivos no se han modificado, git no almacena el archivo dde nuevo, sino un enlace al archivo anterior que ya tiene almacenado.

  2. Operador locales: la mayoria de los operaciones de git solo necesitan archivos y recursos locales para operar, se tiene toda la historia del proyecto en el disco, de manera que podemos trabajar sin conexion durante largos periodos de tiempo.

  3. Informacion: todas las acciones forman parte de la base de datos de git.

  4. Integridad: git realiza una suma de comprobacion antes de almacenar cualquier archivo esta funcion se le conoce como (checksum) y por lo cual hace imposible modificar o eliminar archivos sin que git lo sepa.
  
  5. Usa el metodo HASH sha-1, de manera de que no se guarda por nombre de archivo, si no en base del valor de hash que almacena git

## Estados de git (staged,modified,committed).

  - Staged: preparado, significa que has marcado un archivo modificado en su version actual para que vaya en tu proxima confirmacion.
  - Modified: significa que has modificado un archivo pero todavia no lo has confirmado en la base de datos.
  - Committed: los archivos estan almacenados de manera segura en la base de datos local.

## Secciones de git (consistene en tres secciones)

  1. Directorio git, es donde Git almacena los metadatos y la base de datos de objetos para tu proyecto. Es la parte más importante de Git, y es lo que se copia cuando clonas un repositorio desde otro ordenador.

  2. Directorio de trabajo, es una copia de una versión del proyecto.

  3. Area de preparacion, es un sencillo archivo, generalmente contenido en tu directorio de Git, que almacena información acerca de lo que va a ir en tu próxima confirmación.

## Ventajas

  - Rendimiento

  - Seguridad
  
  - Flexibilidad

## Git se maneja a traves de la line de comando (terminal):

  - ls , listar archivos.
  - cd , movernos por los directorios.
  - cd .. , me muevo a un directorio anterior.
  - pwd , en que lugar estoy , muestra la ruta absoluta.
  - mkadir , para crear directorio.
  - touch , crear archivo.
  - clear, limipiar la consola.

## Configuracion de git.

  Todo lo que hagamos tiene que estar asociado ha alguien. Por ello vamos a configurar el nombre de usuario y nombre de email

  - git config --global user.name , modifica el nombre de usuario
  - git config --global user.email, modifica el email de usuario

  Cada accion que hagas una vez iniciado el git, tu nombre y email aparecera asociado

## Inicio Git

  - git init , donde estes inicia el control de versiones.

  Crea una carpeta de extencion .git y adicional crea la primera rama es master , pendiente de cambiar el nombre de la rama para coocordar con la de github o al git remoto. Ojo antes se usaba master , ahora se llama main.

## Ramas o brach de git

  Son ramas del proyecto , comenzamos con la principal y depues podemos añadir, modificar, renombrar o borrar, son diferente areas de trabajo donde uno no afecta al otro hasta que hace un fecth o merge es decir que se una.

- git branch -m main , renombra la rama donde estes posicionado.

## Status

  - git status , muestra como estan los archivos, modificados en staged o ya committed.

## Add y commit

  Si lo que queeremos sacar la primera fotografia del git primero tenemos que pasarla staged, para hacerlo usamos:

  - git add . , con el punto inicamos todos los archivos en el directorio, si lo queremos hacer individual colocariamos el nombre del archivo junto con su extension.

  - git commit -m "" , sube del staged al commit , es decir pasar ya a la base de datos.

## check out y reset

  - git checkout , es situarnos a un punto completo, puedes ir a una modificacion anterior
  - git reset , refresa las modificaciones antes del staged , cuidado puede devolver commits.

## git log

  Revisa el historial de los commit con su codigo de historia y comentario ademas de detalles como la fecha del commit o quien lo hizo
  - git log ,lista con solo los que quepan en la pantalla del terminal
  - git log --graph , muestra de manera mas grafica
  - git log --graph --pretty=oneline , mas corto y todos los commit en una sola linea por commit
  - git log --graph --decorate --all --oneline, mas simple a la vista

## Alias

  se crea un areas de un comando declarado.
  git config alias.tree "git log --graph --decorate --all --oneline"

## Git ignore

  Sacar un archivo que no queremos que este en nuestro git
  - Se agrega un archivo sin nombre pero con extension de .gitignore y se agrega **/ junto con el nombre del archico que se quiera ignorar

## Diff

  Comprar las versiones de commit o ramas
  - git diff

## reset hard y reflog

  En reset tambien no podemos mover en id de commit y regresar a un estado anterior , pero ciuando hago reset hard borro los commit en el log , git los sigue guardando pero en el log no van aparecer :

  - git reset --hard a88d0bb

  El reflog para referenciar a las lineas id que estan guardadas en el git pero que no se ven en el log.

  - git reflog

## TAG

  Etiquetas, hace referencia a algo, en el git se coloca en commit, son lo referente a las versiones
  -git tag ""

## Branch y switch

  Se trabaja en la rama main que es la principal, pero se puede trabajar el mismo proyecto en varias ramas y despues unirlas a la principal.

  - git branch , crea una rama adicional , se tiene que colocar nombre a la nueva rama si nom  solo se muestra las ramas disponibles.

  - git switch , se usa para cambiar de rama a rama colocando el nombre despues del switch.

## Merge 

  Donde estemos llamamos la palabra reservada merge para traer una rama a otra.

  - git merge , de donde estmos trae a la ramma que tengamos nombrandola con todas sus modificaciones.
  google

## Show
  Muestra la ultima modificacion que se le hizo al archivo.
  - git show 

## ls-files
  muy parecido al ls en la terminal.
  - git ls-files , lista los archivos que git a guardado en la base de datos ya comitiados.
  