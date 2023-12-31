# Diaz_Virginia.zip

## Virginia Diaz Quilez 
### https://github.com/vdiazqui/Diaz_Virginia.zip.git

**1º Explica que es un “Pull Request” en Github. *(1 pts)***

La traducción literal de "Request' es "petición' y "Pull" hemos visto que significa coger el código de otra persona para editarlo tú: por ejemplo, cuando trabajamos en nuestra consola y utilizamos el comando "git pull" estamos cogiendo los cambios que otro compañero ha subido al remoto e incoporándolos a nuestro local. 
Lo que hacen los Pull Requests es permitirte coger el código de otra persona y así eres capaz de trabajar de manera conjunta con los que estén creando un código que te pueda servir a ti. Es por esto que se dice que UNIX es un sistema operativo de código libre (open source), ya que todo el mundo se puede ayudar uno a otros. Además es bidireccional, porque luego esas personas podrán hacerte un Pull Request a ti y trabajar con tu código. 

**2º ¿Qué es un conflicto de fusión (merge conflict) en Git? Explica como resolverías este conflicto. *(1 pts)***

Para explicar lo que es un conflicto de fusión debemos introducir brevemente ciertos conceptos. Cuando estamos escribiendo código en Git, en ocasiones, se trabaja en más de una rama (también denominada "branch"): la rama principal, suele ser nombrada main o master y es donde el código es estable y listo para producción; además, se pueden crear más ramas para que otras personas puedan crear codigo sin modificar el main. 
El conflicto tiene lugar cuando queremos fusionar (en inglés merge) varias ramas, es decir, integrar los cambios realizados en otra rama en tu rama actual. Un merge conflict o conflicto de fusión se daría cuando los cambios realizados en una rama afectan directamente a los cambios realizados en la otra. Por ejemplo, en una rama puedes estar eliminando un comando y en la otra estar utilizando ese mismo comando, algo inconcevible. Para asegurar que la integración final de ramas sea estable y funcional se deben manejar los posibles conflictos de fusión previamente explicados. En este caso hipotetico, para resolver el conflicto de fusión se tendría que decidir que cambios son a los que se da prioridad ya que juntos se contradicen.


**3º Imaginemos que tenemos dos ramas, la principal llamada “main” y la rama “examen_parcial”. ¿Qué procedimiento se debería seguir para fusionar (merge) ambas ramas? *(0.5 pts)***

Si nuestro objetivo es fusionar los cambios de la rama "examen_parcial" en nuestra rama actual que es la principal llamada "main" se debería utilizar el comando "git merge examen_parcial"
También se debe mencionar que hay varios comandos que resultan muy útil cuando estamos trabajando con ramas: "git checkout" sirve para cambiar de una rama a otra y "git branch" se utiliza para listar todas las ramas que hay, la que sale en un color diferente será aquella en la que te encuentres. El procedimiento que se debe utilizar es primero saber que ramas tienes utilizando "git branch", después con "git checkout main" estarías en tu rama principal y una vez allí puedes escribir el comando "git merge examen_parcial" para fusionar ambas ramas.

**4º Has realizado un commit, pero luego descubres un error importante en los cambios que has incluido. Necesitas revertir este último commit para regresar tu proyecto al estado anterior, pero deseas mantener los cambios realizados en tu área de trabajo. Explica el comando de Git que utilizarías para llevar a cabo esta acción. *(0.5 pts)***

Es esencial que se pueda revertir commits para volver al estado anterior de tu proyecto ya que siempre puede haber algún error que no hemos percibido antes. El comando de Git que utilizaría para llevar a cabo esta acción es "git reset --hard". Esta acción lo que hace es revertir los cambios realizados en tu consola es decir los cambios locales. 

**5º ¿Cómo se realiza un fork de un repositorio en GitHub y para qué se utiliza comúnmente esta acción? *(1 pts).***

Cuando estas en un repositorio en GitHub del que tu no eres creador arriba a la derecha aparece un botón llamado "fork" (la traduccion literal es tenedor) haciendo click en ese botón sale un enlace que debe ser copiado. Esta acción se utiliza cuando queremos clonar un repositorio ajeno en nuestra consola para trabajar en él en nuestro local y luego subir los cambios al remoto. El comando utilizado es git clone y se copia el fork que hemos creado.

**6º Te encuentras trabajando en un proyecto y necesitas llegar a un archivo específico llamado "archivo.txt". Este archivo está ubicado dentro de una estructura de directorios en tu sistema.**

**a)      Desde tu posición actual en el directorio raíz (home) de tu proyecto, ¿cómo llegarías al directorio que contiene "archivo.txt", el cual está dentro del directorio "UAX", el cual a su vez está dentro del directorio "Universidad", que se encuentra dentro del directorio "Nombre_del_alumno (raíz)"? Proporciona el comando exacto que usarías y especifica qué tipo de ruta es. *(0.5 pts)***

El comando exacto que usaría es "cd". Cd significa change directory, en español cambiar directorio. Partiendo de "Nombre_del_alumno" escribiría "cd Universidad" y presionaría enter. Como el directorio "UAX" está dentro de "Universidad" volvería a escribir "cd UAX" enter y una vez dentro de UAX tendría que escribir "cd archivo.txt" enter para acceder a dicho directorio.
Debido a que la posición actual es el directorio raiz (home) se trata de una ruta absoluta. 

**b)       Si te encuentras actualmente dentro del directorio "Universidad", ¿cómo accederías al directorio que contiene "archivo.txt"? Proporciona el comando exacto que usarías y especifica qué tipo de ruta es. *(0.5 pts)***

Como dentro de "Universidad" está el directorio "UAX", volvería a escribir "cd UAX" y una vez dentro de UAX tendría que escribir "cd archivo.txt" para acceder a dicho directorio.
Debido a que la posición inicial no es el directorio raiz, sino que es un directorio dentro de este, se trata de una ruta relativa.


**7º Te han asignado la tarea de trabajar en un proyecto de código abierto alojado en GitHub. Como nuevo colaborador, se espera que sigas las mejores prácticas para el manejo del código fuente utilizando Git. Que comandos de Git utilizaría para las siguientes tareas: *(2 pts) (0.2 cada pregunta):***

**1) Clonar el Repositorio:**

b) git clone

**2) Crear una Nueva Rama:**

a) git branch

**3) Cambiar entre Ramas:**

c) git checkout

**4) Añadir Cambios al Área de Preparación (Staging):**

b) git add

**5) Realizar un Commit:**

b) git commit

**6) Publicar la Rama en el Repositorio Remoto:**

b) git push

**7) Actualizar tu Rama Local con Cambios del Remoto:**

c) git pull

**8) Fusionar Cambios de otra Rama a tu Rama Actual:**

d) git merge

**9) Revertir Cambios Locales:**

a) git reset --hard

**10) Revisar el Historial de Commits:**

c) git log

**8º Eres parte de un equipo de desarrollo trabajando en un proyecto de software matemático. La estructura de ramas de tu proyecto en Git se ve de la siguiente manera:**

·         **main: La rama principal donde el código es estable y listo para producción.**

·         **develop: Una rama de desarrollo donde se integran las nuevas características antes de pasar a main.**

·         **matemáticas: Una rama donde tú y tu equipo están trabajando en resolver un problema.**

·         **Diseño UX: Una rama donde el equipo de diseño trabaja en desarrollar la vista de las integraciones por parte del equipo de matemáticas.**

**Durante el desarrollo, tu equipo ha completado una serie de algoritmos importantes en la rama matemáticas y está listo para integrarlos en la rama develop. Simultáneamente, el equipo de diseño ha hecho cambios significativos en la rama diseño-UX, que también deben ser integrados en develop.**

**Tu tarea es coordinar la integración de estas dos ramas en develop asegurándote de que se manejen adecuadamente los conflictos, se mantenga la calidad del código y se respete la funcionalidad tanto del lado matemático como del diseño UX.**

**Describe detalladamente los pasos y consideraciones que tomarías para lograr esta tarea, incluyendo cómo manejarías los posibles conflictos de fusión y cómo asegurarías que la integración final en develop sea estable y funcional. *(2 pts)***

Antes de poder describir detalladamente los pasos y consideraciones que seguiría para llevar a cabo dicha labor se debe contextualizar la situación y analizar el punto de partida. 
En este escenario no entra en juego la rama main aún, ya que ahí es donde se pasarán los nuevos cambios implementados primero en la rama de desarrollo denominada develop. Sin embargo, sí que tenemos otras dos ramas en las que hemos implementado cambios con información altamente importante de las cuales no podemos priorizar ninguna sino que queremos respetar la funcionalidad de ambas ramas. El procedimiento que llevaría a cabo es realizar un comand para mergear las ramas, es decir fusionarlas. En el caso de que surgiera algún conflicto de fusión este debería ser resuelto de la manera más eficiente posible.

**9º Pregunta práctica del módulo 3: Repositorios local y remoto**

**Recientemente, has completado una práctica en la que creaste un repositorio tanto local como remoto para una calculadora web sencilla. La práctica implicaba varios pasos clave, incluyendo la creación del repositorio, la adición y el registro de cambios, y finalmente la subida del repositorio local al remoto en GitHub.**


**Considerando los pasos realizados durante la práctica, responde la siguiente pregunta:**

**¿Cuál de las siguientes afirmaciones describe mejor el proceso que seguiste para añadir el botón de "x^4" a tu calculadora web y subir los cambios al repositorio remoto? *(1 pts)*** 

C) Añadiste el botón "x^4" al archivo "index.html" en tu repositorio local, creaste un commit con los cambios y luego subiste el repositorio local al remoto en la rama principal (master).


