1.- Settings � Se usa para las variables globales, elementos de configuraci�n (Si usamos pre procesador, si no, podemos saltarnos esta capa)
2.- Tools � Mixins y Funciones (solo si usamos preprocesadores)
3.- Generic � Estilos CSS: reset, box-sizing, normalize.css�
4.- Base � Elementos HTML sin clases, selectores.
5.- Objects � Patrones de dise�o, la estructura. Solo si usamos CSS dirigido a objetos (OOCSS)
6.- Components � Carruseles, calendarios� y sets de UI� Aqu� metemos nuestros estilos concretos, para una lista concreta de un producto, por ejemplo.
7.- Trumps � Ayudas y lo que usamos para sobreescribir. La capa de los importants, la m�s espec�fica de todas. Aqu� habr� c�digo muy concreto, para partes del DOM muy espec�ficas.

No se trata de llamar de una manera espec�fica a nuestras clases, para eso ya tenemos BEM. Es la manera en que vamos a llamar al archivo .css en funci�n de a qu� parte pertenece (y por tanto, que estilos hemos incluido en ella).

Todo el css que incluyamos en nuestro proyecto tiene que formar parte de alguna de estas capas. Nos obliga a pensar a qu� pertenece cada l�nea de c�digo antes de incluirla.

* Las media queries van incluidas en la css del elemento al que estamos dando estilos.

La nomenclatura para la css seguir� la pauta:

Nombre de la capa en la que nos hayamos + nombre de la css concreta:
� base .links.css
� components .carousel.css

El objetivo:
� Afectar al DOM de general a concreto.
� La especificidad aumenta de manera progresiva.
� Nunca se deshace, solo se a�ade.

No es un universo cerrado. En funci�n de nuestra necesidades podemos a�adir capas. Lo importante es seguir el orden de pir�mide invertida:
� Escribir CSS en orden de especificidad
� Ser fieles al �Gr�fico de especificidad� evitando en la medida de lo posible, los picos.
� El orden en el que creamos las capas tiene que ser l�gico. Por ejemplo, para una test AB podemos a�adir la capa TEST entre Components y Trumps. O la capa THEME (tambi�n entre Components y Trumps).