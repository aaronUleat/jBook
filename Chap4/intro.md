#CONCEPTOS BASICOS DE LA PROGRAMACION ORIENTADA A OBJETOS.

Como usted vio en el capitulo , la programacion orientada a objetos es un paradigma de programacion donde los conceptos 
en el programa son representados por *objetos*. Cada *objeto* es una instancia de una clase, que puede ser como una 
huella o un template de las caracteristicas de un objeto. Al contrario de del la programacion procesal, estas 
caracteristicas incluyen data--atributos o variables describiendo el estado del objeto -- y comportamientos -- los 
metodos o procedimientos  describen acciones que un objeto puede realizar.

Un ejemplo simple que nos puede ayudar a explicar esto. Imaginese que usted esta desarrollando una aplicacion para 
mantener el rastreo de los cursos y el registro de un estudiante. En la programcion procesal, su primer tarea seria 
realizar una estructura de datos que represente el concepto con el cual esta lideando. Usted talvez definira dos listas 
-- uno para mantener a los estudiantes y otro para mantener los cursos. Cada lista contendra un diccionario de valores 
representando un solo estudiante o un solo curso. Esto talvez se pueda ver como lo siguiente.

```
STUDENTS = [
{id : 'S0001', last: 'Demmick', first: 'Larry', birthdate: '1989-05-13'},
{id : 'S0002', last: 'Newandyke', first: 'Freddy', birthdate: '1991-01-05'},
...
]
COURSES = [
{id : 'C00A', name: 'Introduction to Java'},
{id : 'C00B', name: 'Advanced Data Base Management'},
...
]
```
No le preste atencion a la sintaxis que estamos utilizando aqui -- es solo un pseudo-codigo para ilustrar el punto. El 
siguiente paso define una serie de operaciones -- procedimientos -- que usted quiere ejecutar en sus conceptos.
Por ejemplo, usted va a necesitar un procedimiento para agregar al estudiante.

```
procedure add_student(i, n, fn, bd) {
STUDENTS += {id : i, name: n, firstname: fn, birthdate: bd}
}
```

Procedimientos similares pueden ser creados para agregar cursos y para remover o midificar estudiantes o cursos. Usted 
talvez quiera darle siguimiento de cuales estudiantes estan registrados en cuales cursos. Posibilidades multiples existen 
como poder manejar esto: usted podria agregar a una lista de cursos IDs para cada estudiante ( representando los 
cursos a los cuales el estudiante esta matriculando ), o una lista de estudiantes IDs para cada curso ( representando 
los estudiantes registrado a este curso). Otro modo para realizar esto es crear una estructura de dato adicional 
estructurada -- REGISTRACIONES -- para mantener el rastreo de las registraciones.

La programacion procesal tiene muchos incovenientes desde el punto de vista de mantenimiento. Para uno, cuando la 
definicion una definicion de una estructura de dato cambia, todos los procedimientos utilizando esta estructura necesita 
ser revisado y actualizado acordemente. Segundo. cuando las estrucuturas de datos estan vinculados, se necesita tener 
cuidado al estado del programa y que se mantenga valido a todo momento. Cuando borramos un curso en este ejemplo, 
por ejemplo, usted tambien va a necesitar para asegurar que todas las registraciones por este curso que tambien fue 
removido. La desventaja mas grande viene del hecho que toda la data esta guardada en estructuras globales, las cuales 
son accesibles para todos los procedimientos. Para programa grandes, se vuelve pesado mantener un rastreo de que 
procedimiento esta utilizando cual estructura, como poder modificarlas, y que efecto y cambio enun procedimiento o 
estructura va a tener en otras partes del programa.

Cuando se utiliza la programacion orientada a bojetos, los objetos son encapsulados solamente en data local, en cual es 
por default accesible solo por ese objeto. Antes de que tengamos que pensar en la data y el codigo, son dos conceptos 
separados, un programa orientado a objetos fuciona los dos en el concepto de un objeto.  Esto incrementa el entendimiento 
( analistas y programadores pueden considerar objetos de interes sin ir muy profundo trabajo de un programa completo ) 
y es mas facil de mantener.

Para darse cuenta de esto, la programcion orientada a objetos aplica dos conceptos conocidos como *encapsulacion* y 
*esconder informacion*. Una de las mayores fuentes  de errores en los programas es cuando algunas partes del programa 
estan interferiendo con otras partes. La programcion Orientada a Objetos resuelve este problema al encapsular los dos, 
la data y el comportamiento dentro de un objeto.

Sin embargo, esto en si mismo no es suficiente para garantisar mantenimiento de los programas, usted tambien va a necesitar 
prevenir que un objeto pueda ser accesado directamente por otros objetos. Por lo tanto, la Programcion Orientada a Objetos 
tambien enfatiza el concepto de esconder informacion. donde un objeto puede por default ser accesada solo por metodos 
contenidos en el mismo objeto. Cuando los elementos data de un objeto necesitar ser usado por otro objeto, este ultimo 
llama a un metodo public, basicamente solicitando al "objeto que contiene" que ejecute un cambio en su data.
Tal como, la programcion orientada a objetos anima a los programadores a poner data donde no es directamete accesible 
o modificada para el resto del sistema. En vez de eso, la data es accesible a travez de metodos, lo cuales tambien pueden 
incluir checks y proteccion para asegurarnos que el request que cambia es permitido para el objeto que lo contiene.

La programcion orientada a objetos tambien define conceptos para ayudarnos con la estructuracion de los programas entonces 
que puedan ser facilmente extendidos y evolucionado. Estos conceptos son poliformismo, el cual es la habilidad de trtar 
los objetos de diferente tipo en una manera similar, y la herencia, el cual es un concepto para permitir para extender 
objetos y habilitar el codigo reutilizable. Usted va a revisitar estos conceptos en mas detalles en el capitulo 8, cuando 
usted ahonde mas a fondo en el concepto de la programcion orientada a objetos. Por ahora, usted va a ver como los conceptos 
de la programacion orientada a objetos que usted tiene hasta ahora 