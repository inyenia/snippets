## Snippets de código

Script para buscar snippets de código en el código fuente de la aplicación y generar de forma automática ficheros en formato markdown con cada uno de los snippets encontrados.

La idea de este script es facilitar la generación de documentación y facilitar su actualización. Puede ser una buena idea crear snippets de código a partir de los test de tu aplicación.

### Bloques de código como snippets

Para crear un snippet tenemos que añadir lo siguiente para crear un fichero llamado HelloWorld_example1.md con el código entre los marcadores //BEGIN-SNIPPET y //END-SNIPPET

```java
//BEGIN-SNIPPET: HelloWorld_example1
System.out.println("Hello, World 1");
//END-SNIPPET
```

### Búsqueda de snippets y generación de ficheros en formato markdown

```
usage: ./snippets.sh param1 param2 param3
param1:	programming language [java|js]
param2:	input path
param3:	output path
```

Ejemplo de uso

```
./snippets.sh java examples doc/snippets
```

### Incluir snippets en formato markdown

```
!INCLUDE "doc/snippets/HelloWorld_example1.md"
```
