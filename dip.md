# Principio de Inversión de Dependencias (DIP)
En el sistema de gestión de turnos médicos, algunos módulos importantes estaban conectados directamente a servicios específicos, como una base de datos concreta o un sistema particular de envío de correos. Esto significaba que cualquier cambio en esos servicios afectaba directamente a todo el sistema, generando errores y dificultando la evolución o migración hacia nuevas tecnologías.

Este principio propone invertir las dependencias: en lugar de que la lógica principal del sistema dependa directamente de servicios concretos, se trabaja con abstracciones (por ejemplo, "servicio de notificación" en lugar de "servicio de correo"). Así, se pueden cambiar o reemplazar los servicios reales sin tocar el funcionamiento principal del sistema. Esto hace que el sistema sea mucho más flexible, reutilizable y fácil de adaptar con el tiempo.

## Motivación

En el sistema de gestión de turnos médicos, uno de los mayores problemas era que los módulos de alto nivel, como la lógica principal que gestiona las citas y asigna médicos, dependían directamente de componentes de bajo nivel, como bases de datos específicas o sistemas de notificación como el correo electrónico.
Esto significaba que cualquier cambio en estos elementos de bajo nivel afectaba toda la aplicación.

Al aplicar el principio de inversión de dependencias (DIP), el sistema se reorganizó para que la lógica principal dependiera de abstracciones (como interfaces de notificación, bases de datos y servicios), en lugar de depender de implementaciones concretas.
Por ejemplo, en lugar de que el sistema de turnos dependiera de un servicio específico de correo electrónico, se creó una interfaz común llamada "Servicio de Notificación", y el sistema solo interactúa con esa interfaz sin preocuparse por qué servicio de notificación se utiliza realmente. 
Esto permitió cambiar o reemplazar el sistema de notificación sin alterar el resto del sistema. El código de alto nivel se desacopló de los detalles de implementación, lo que hizo el sistema más flexible, fácil de probar y mantener a largo plazo.


Ejemplo del mundo real :

En la arquitectura de un sistema de notificaciones. Un módulo de alto nivel (el servicio de notificaciones) depende de una interfaz abstracta que define el método de envío de mensajes. Las clases de bajo nivel (notificador de correo electrónico, notificador de SMS) implementan esta interfaz, permitiendo al servicio de notificaciones cambiar el método de envío sin modificar su código. 
