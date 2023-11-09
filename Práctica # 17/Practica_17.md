# Practica #17

## 1. Identificación y clasificación de patrones de comportamiento:

   - **Observer Pattern (Patrón Observador):** Este patrón se utiliza cuando un objeto, denominado "sujeto", mantiene una lista de objetos dependientes, llamados "observadores", y notifica a ellos cualquier cambio en su estado. Por ejemplo, en una aplicación de chat, cuando un usuario envía un mensaje, todos los usuarios que están en la misma conversación son notificados y ven el mensaje en tiempo real.

   - **Strategy Pattern (Patrón Estrategia):** Permite definir una familia de algoritmos, encapsular cada uno y hacerlos intercambiables. Por ejemplo, en una aplicación de procesamiento de imágenes, se pueden tener diferentes estrategias de compresión de imágenes que pueden ser seleccionadas en tiempo de ejecución.

   - **Command Pattern (Patrón Comando):** Encapsula una solicitud como un objeto, lo que permite parametrizar a los clientes con colas, solicitudes y operaciones. En un editor de texto, se pueden usar comandos para representar acciones como copiar, cortar o pegar, y el historial de comandos para realizar operaciones de deshacer y rehacer.

   - **State Pattern (Patrón Estado):** Permite que un objeto cambie su comportamiento cuando su estado interno cambia. En una máquina de estados, este patrón se usa para representar los diferentes estados y transiciones de un objeto.

   - **Chain of Responsibility Pattern (Patrón Cadena de Responsabilidad):** Se utiliza para pasar solicitudes a través de una cadena de manejadores. Cada manejador decide si procesa la solicitud o la pasa al siguiente en la cadena. Por ejemplo, en un sistema de procesamiento de correos electrónicos, varios filtros pueden procesar los correos entrantes, y si uno de los filtros lo marca como spam, los siguientes filtros pueden ignorarlo.

   - **Memento Pattern (Patrón Memento):** Captura y externaliza un estado interno de un objeto para que este pueda ser restaurado posteriormente. Este patrón se utiliza en editores de texto para implementar operaciones de deshacer/rehacer.

   - **Interpreter Pattern (Patrón Intérprete):** Define una gramática para un lenguaje y proporciona un intérprete para evaluar sentencias en ese lenguaje. Se usa en sistemas que requieren procesamiento de lenguaje natural, como motores de búsqueda.

## 2. Evaluación de escenarios de uso:

   - **Observer Pattern:** En aplicaciones de monitoreo en tiempo real, como sistemas de control de tráfico aéreo, donde múltiples sistemas deben estar informados de los cambios en tiempo real.
   
   - **Strategy Pattern:** En motores de juegos, donde se pueden cambiar estrategias de renderizado o física según las preferencias del jugador o las capacidades del hardware.

   - **Command Pattern:** En aplicaciones de diseño gráfico, donde los comandos representan acciones del usuario y se pueden deshacer/rehacer.

   - **State Pattern:** En aplicaciones de comercio electrónico, donde el estado del carrito de compras puede cambiar según las acciones del usuario.

   - **Chain of Responsibility Pattern:** En sistemas de seguridad, donde diferentes niveles de autorización pueden procesar solicitudes de acceso a recursos.

   - **Memento Pattern:** En editores de texto, para permitir el deshacer/rehacer de operaciones.

   - **Interpreter Pattern:** En sistemas de procesamiento de lenguaje natural, como chatbots o motores de búsqueda semántica.

## 3. Comparación de patrones:

   - **Eficiencia:** Algunos patrones pueden introducir sobrecarga debido a la estructura adicional que agregan al código. Por ejemplo, el patrón Observer puede resultar en notificaciones innecesarias si no se gestiona adecuadamente.

   - **Mantenibilidad:** La elección del patrón correcto puede hacer que el código sea más fácil de mantener y extender. Por ejemplo, el patrón State permite agregar nuevos estados sin modificar el código existente.

   - **Aplicabilidad:** La elección del patrón debe basarse en los requisitos del proyecto. No todos los patrones son necesarios en todos los proyectos, y algunos pueden ser excesivos.

## 4. Determinación de mejores prácticas:

   - **Comprender el problema:** Antes de aplicar un patrón, es crucial comprender completamente el problema que se está tratando de resolver y asegurarse de que un patrón sea la solución adecuada.

   - **Documentación:** Es importante documentar el uso de patrones en el código para que otros desarrolladores puedan entender su propósito y funcionamiento.

   - **Evaluación de necesidad:** No todos los problemas requieren un patrón de comportamiento. A veces, la simplicidad es preferible.

   - **Coherencia:** Mantener la coherencia en la aplicación de patrones en todo el proyecto para facilitar la comprensión y el mantenimiento del código.

## 5. Casos de Estudio:

**Caso de Estudio 1: Aplicación del Observer Pattern en la Actualización en Tiempo Real**

*Patrón utilizado: Observer Pattern*

**Problema:** La plataforma de turismo necesita notificar a los usuarios cuando se agregan nuevas rutas turísticas o cuando hay cambios en las rutas existentes.

**Solución:** Se aplica el Observer Pattern para mantener una lista de usuarios interesados en recibir actualizaciones de rutas turísticas. Cada vez que se agrega o modifica una ruta, se notifica a todos los usuarios registrados interesados en esa ruta.

**Impacto en la calidad del software:**

- *Tiempo real*: Los usuarios obtienen información actualizada en tiempo real, lo que mejora la experiencia del usuario y aumenta la retención de usuarios.
- *Escalabilidad*: El sistema es escalable, ya que se pueden agregar más observadores sin modificar el código existente.
- *Mantenibilidad*: Cambios futuros en la notificación de rutas son más fáciles de implementar sin afectar otras partes del sistema.

**Caso de Estudio 2: Implementación del Strategy Pattern en la Creación de Rutas Turísticas**

*Patrón utilizado: Strategy Pattern*

**Problema:** La plataforma permite a los usuarios crear sus propias rutas turísticas, y se necesitan diferentes estrategias para calcular la duración y la dificultad de las rutas en función de las preferencias del usuario.

**Solución:** Se aplica el Strategy Pattern para encapsular las diferentes estrategias de cálculo de rutas. Los usuarios pueden elegir la estrategia que mejor se adapte a sus preferencias (por ejemplo, rutas más cortas o rutas más escénicas).

**Impacto en la calidad del software:**

- *Flexibilidad*: Los usuarios pueden personalizar sus rutas según sus preferencias, lo que mejora la satisfacción del usuario.
- *Mantenibilidad*: Agregar nuevas estrategias de cálculo es sencillo sin afectar otras partes del sistema.
- *Reutilización de código*: Las estrategias de cálculo se pueden reutilizar en otros contextos dentro de la plataforma.

**Caso de Estudio 3: Uso del Command Pattern en la Gestión de Rutas Turísticas Guardadas**

*Patrón utilizado: Command Pattern*

**Problema:** La plataforma permite a los usuarios guardar sus rutas turísticas personalizadas y realizar operaciones de deshacer y rehacer en su historial de rutas.

**Solución:** Se aplica el Command Pattern para representar las acciones del usuario, como guardar una ruta, eliminar una ruta o restaurar una ruta anterior en el historial.

**Impacto en la calidad del software:**

- *Operaciones de deshacer/rehacer*: Los usuarios pueden revertir cambios no deseados en sus rutas, lo que mejora la usabilidad y evita la pérdida de datos.
- *Mantenibilidad*: Agregar nuevas acciones o modificar las existentes es más sencillo sin afectar la lógica principal de la aplicación.
- *Registro de acciones*: Se registra el historial de acciones, lo que facilita el seguimiento y la auditoría de las actividades de los usuarios.
