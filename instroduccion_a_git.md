# Git

  Sistema de control de versiones, registra los cambios realizados sobre el archivo o conjunto de archivo a lo largo del tiempo

  Este sistema permite realizar un seguimiento de las modificaciones realizadas por cada uno de los colaboradores del proyecto

  Revertir los cambios a un estado anterior o incluso el proyecto entero

  Mas sencillo detectar el error y quien lo genero

  En caso de perdida se puede es facil y sencillo recuperarlo

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