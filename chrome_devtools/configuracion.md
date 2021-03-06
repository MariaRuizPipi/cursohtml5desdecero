# Configuración

Ahora vamos a ver cómo podemos configurar Google Chrome para poder modificar ficheros que se encuentren en nuestro disco duro.

Para hacer esto usaremos los "**Workspaces**", estos nos permitirán realizar cambios [persistentes](https://es.wikipedia.org/wiki/Persistencia_(inform%C3%A1tica) en nuestro código sin tener que ejecutar otro editor de código.

Para ello vamos a seguir los siguientes pasos:
1. Creamos una carpeta (de prueba) en nuestro disco duro (por ejemplo "*html*").
2. Creamos un fichero vacío dentro de la carpeta llamado: "*index.html*"<sup>1</sup>
3. Abrimos el fichero con Google Chrome
4. Abrimos las DevTools y nos vamos a la pestaña "**Sources**"
5. Hacemos clic en el panel izquierdo sobre la ruta del directorio y seleccionamos "**Add Folder to Workspace**":
[![](../images/workspace.png)](../images/workspace.png)
6. Y por último pulsamos "**Allow**" para autorizar a DevTools a realizar cambios persistentes en el disco duro: [![](../images/allow_workspace.png)](../images/allow_workspace.png)

> **Nota**:<br>
> Si nos equivocamos al añadir un directorio al Workspace podremos eliminarlo simplemente pulsando con el botón derecho sobre el directorio y seleccionando la opción "**Remove Folder from Workspace**".

Ahora tenemos que "mapear" (vincular) el recurso que ha obtenido el navegador con el fichero del disco duro que queremos modificar (osea, con él mismo), para ello:
1. Hacemos clic con el botón derecho sobre el nombre del fichero (*index.html* que cuelga de "file://")
2. Elegimos la opción "**Map to File System Resource**":
[![](../images/workspace_map_to_filesystem.png)](../images/workspace_map_to_filesystem.png)
3. Seleccionamos el fichero dentro del espacio de trabajo (Workspace).
4. Y refrescamos la página.

Y ya estamos listos para empezar a programar usando las Chrome DevTools.

También puedes consultar las [limitaciones](https://developers.google.com/web/tools/setup/setup-workflow#limitations) de los "**Workspaces**", pero no te preocupes por ellas ya que no nos afectarán en este curso; por ejemplo,  los cambios en la pestaña "**Elements**" no serán persistentes (lógico ya que lo que estamos cambiando es el *DOM*, que como vimos anteriormente es dinámico, osea que va cambiando).

## Gestión de ficheros
Una vez hecho todo esto podemos añadir y eliminar ficheros directamente desde DevTools:
1. Añadir ficheros: pulsando con el botón derecho sobre la carpeta y seleccionando "**New File**".
2. Eliminar ficheros: pulsando con el botón derecho y seleccionando "**Delete**"
 
Sin embargo no podemos crear y eliminar directorios, esto lo tendremos que hacer directamente desde la carpeta que hemos creado en nuestro disco duro.


<small>Aclaraciones:</small><br>
<small>1. A pesar de que no vamos a usar aún un servidor web, lo llamaremos así para ir acostumbrándonos a este nombre. Por defecto los servidores web cuando reciben la petición de un recurso y no se indica explícitamente el nombre del recurso, busca en la carpeta un fichero con nombre "index.html", y lo devuelve en caso de encontrarlo.</small><br>
