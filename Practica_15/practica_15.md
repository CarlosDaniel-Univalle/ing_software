# Practica 15
## Carlos Daniel Menchaca Arauz

**Identificar y Clasificar Patrones Creacionales:**

Los patrones creacionales son un conjunto de patrones de diseño que se utilizan para la creación de objetos en el desarrollo de software. Algunos de los patrones creacionales más comunes son:

1. **Singleton:** Este patrón garantiza que una clase tenga una única instancia y proporciona un punto de acceso global a esa instancia. Es útil cuando se necesita una única instancia para coordinar acciones en todo el sistema.

2. **Factory Method:** El patrón Factory Method define una interfaz para la creación de objetos, pero deja la implementación concreta de la creación a las subclases. Esto permite que una clase delegue la responsabilidad de instanciar objetos a sus subclases.

3. **Abstract Factory:** Proporciona una interfaz para crear familias de objetos relacionados o dependientes sin especificar sus clases concretas. Es útil cuando se necesita garantizar que los objetos creados sean coherentes entre sí.

4. **Builder:** Este patrón se utiliza para construir un objeto complejo paso a paso. Permite construir diferentes representaciones de un objeto utilizando el mismo código de construcción.

5. **Prototype:** El patrón Prototype se utiliza para crear nuevos objetos copiando un objeto existente (prototipo). Esto es útil cuando la creación de un objeto es costosa en términos de rendimiento o recursos.

**Evaluación de Escenarios de Uso:**

Los patrones creacionales se aplican en diversos escenarios de desarrollo de software:

1. **Singleton:** Puede aplicarse cuando se necesita una única instancia de una clase para gestionar recursos compartidos, como una conexión a una base de datos o un registro de eventos en una aplicación.

2. **Factory Method:** Útil cuando se necesita extender una clase para crear objetos concretos específicos. Por ejemplo, en un videojuego, cada tipo de enemigo puede ser creado por su propia fábrica.

3. **Abstract Factory:** Se aplica cuando se requiere una familia de objetos relacionados, como una interfaz gráfica de usuario (UI) que se adapta a diferentes sistemas operativos (Windows, Linux, etc.).

4. **Builder:** En situaciones donde se necesita crear objetos complejos con muchas configuraciones posibles, como la construcción de documentos con múltiples secciones y formatos.

5. **Prototype:** Útil en editores gráficos, donde los usuarios pueden duplicar objetos (por ejemplo, formas) y modificar las copias sin afectar al objeto original.

**Comparación de Patrones:**

La elección del patrón creacional depende del contexto y las necesidades específicas del proyecto. La comparación se basa en factores como eficiencia, mantenibilidad y aplicabilidad:

- **Singleton vs. Factory Method:** El Singleton es eficiente en términos de acceso global a una única instancia, pero puede ser difícil de extender. El Factory Method es más flexible y permite crear múltiples instancias, pero agrega complejidad.

- **Factory Method vs. Abstract Factory:** El Factory Method se utiliza para crear un solo tipo de objeto, mientras que el Abstract Factory crea familias de objetos relacionados. La elección depende de la complejidad del sistema.

- **Builder vs. Prototype:** El Builder se utiliza para construir objetos complejos paso a paso, lo que es útil en la creación de objetos con múltiples configuraciones. El Prototype se usa cuando la creación de objetos es costosa y se necesita una copia rápida.

**Determinar Mejores Prácticas:**

Las mejores prácticas para la selección e implementación de patrones de creación incluyen:

- Comprender las necesidades del proyecto: Elija el patrón que mejor se adapte a los requisitos específicos del sistema y la escalabilidad.

- Mantenibilidad: Los patrones deben hacer que el código sea fácil de mantener y extender, evitando acoplamiento excesivo.

- Eficiencia: Evalúe el rendimiento de cada patrón en función de los requisitos de la aplicación. Algunos patrones pueden introducir sobrecarga.

- Documentación: Documente el uso de patrones en el código para que otros desarrolladores puedan comprender y mantener el sistema.

**Casos de Estudio:**

1. **Singleton**:
   - Podrías usar el patrón Singleton para crear una instancia única de un servicio que necesites en toda tu aplicación, como una instancia de Firebase para la autenticación o una instancia de gestión del estado global. Esto asegura que haya una única instancia compartida en toda la aplicación.

2. **Factory Method**:
   - Puedes utilizar el patrón Factory Method para crear instancias de componentes o servicios específicos. Por ejemplo, si tienes diferentes tipos de páginas en tu plataforma de turismo, podrías tener fábricas que creen instancias de estas páginas en función de los datos recibidos.

3. **Abstract Factory**:
   - El patrón Abstract Factory podría ser útil si necesitas crear familias de componentes relacionados. Por ejemplo, podrías tener una fábrica abstracta para crear componentes de interfaz de usuario que sigan un diseño coherente en toda la plataforma.

4. **Builder**:
   - Puedes aplicar el patrón Builder para construir objetos complejos, como formularios de búsqueda o filtros personalizados. Un constructor podría ayudar a los usuarios a crear estos objetos paso a paso y luego utilizarlos para recuperar datos de la base de datos de Firebase.

5. **Prototype**:
   - En el contexto de una plataforma de turismo, podrías usar el patrón Prototype para clonar objetos complejos, como itinerarios de viaje o reservas. En lugar de crear estos objetos desde cero, puedes copiar prototipos existentes y personalizarlos para el usuario.
