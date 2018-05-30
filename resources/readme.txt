1.- Settings – Se usa para las variables globales, elementos de configuración (Si usamos pre procesador, si no, podemos saltarnos esta capa)
2.- Tools – Mixins y Funciones (solo si usamos preprocesadores)
3.- Generic – Estilos CSS: reset, box-sizing, normalize.css…
4.- Base – Elementos HTML sin clases, selectores.
5.- Objects – Patrones de diseño, la estructura. Solo si usamos CSS dirigido a objetos (OOCSS)
6.- Components – Carruseles, calendarios… y sets de UI… Aquí metemos nuestros estilos concretos, para una lista concreta de un producto, por ejemplo.
7.- Trumps – Ayudas y lo que usamos para sobreescribir. La capa de los importants, la más específica de todas. Aquí habrá código muy concreto, para partes del DOM muy específicas.

No se trata de llamar de una manera específica a nuestras clases, para eso ya tenemos BEM. Es la manera en que vamos a llamar al archivo .css en función de a qué parte pertenece (y por tanto, que estilos hemos incluido en ella).

Todo el css que incluyamos en nuestro proyecto tiene que formar parte de alguna de estas capas. Nos obliga a pensar a qué pertenece cada línea de código antes de incluirla.

* Las media queries van incluidas en la css del elemento al que estamos dando estilos.

La nomenclatura para la css seguirá la pauta:

Nombre de la capa en la que nos hayamos + nombre de la css concreta:
· base .links.css
· components .carousel.css

El objetivo:
– Afectar al DOM de general a concreto.
– La especificidad aumenta de manera progresiva.
– Nunca se deshace, solo se añade.

No es un universo cerrado. En función de nuestra necesidades podemos añadir capas. Lo importante es seguir el orden de pirámide invertida:
– Escribir CSS en orden de especificidad
– Ser fieles al ‘Gráfico de especificidad’ evitando en la medida de lo posible, los picos.
– El orden en el que creamos las capas tiene que ser lógico. Por ejemplo, para una test AB podemos añadir la capa TEST entre Components y Trumps. O la capa THEME (también entre Components y Trumps).