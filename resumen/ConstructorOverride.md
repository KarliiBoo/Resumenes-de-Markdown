##  1. ¿Qué son los constructores?
Los constructores son métodos especiales que se ejecutan al crear un objeto con `new`. Su función es inicializar los atributos y asegurar que cada instancia comience en un estado válido. En una clase base como `Ave`, es común encontrar varios constructores sobrecargados: un constructor por defecto que asigna valores iniciales a los atributos (`nombre`, `tamano`, `tieneAla`, `sexo`), un constructor que recibe solo el nombre y reutiliza el constructor base mediante `this()`, y otro con dos parámetros que inicializa nombre y sexo encadenando constructores para evitar duplicar código. Esta técnica, conocida como **sobrecarga de constructores**, permite crear objetos con distintos niveles de detalle y garantiza una inicialización consistente. Los constructores no poseen tipo de retorno y deben llamarse igual que la clase, lo cual los distingue de los métodos normales.

---

##  2. Constructores en clases hijas
Cuando una clase hereda de otra, como `Colibri` y `Pato` que extienden de `Ave`, los constructores no se heredan directamente, pero pueden invocarse mediante `super()`. Esto permite que la sección heredada del objeto se inicialice correctamente antes de configurar los atributos propios de la clase hija. Por ejemplo, un constructor de `Colibri` puede llamar a `super(nombre, sexo)` para reutilizar la lógica de inicialización definida en `Ave`. Si una clase hija no define constructores, Java proporciona uno por defecto que invoca automáticamente al constructor vacío de la clase padre. De esta forma, **la herencia y los constructores trabajan en conjunto** para garantizar objetos bien formados y coherentes desde su creación.

---

##  3. ¿Qué es el Override?
El override ocurre cuando una clase hija **redefine** un método heredado de la clase padre manteniendo la misma firma (nombre, parámetros y tipo de retorno), pero cambiando su implementación. Esto permite ajustar el comportamiento a las necesidades específicas de la clase hija. Un override válido mantiene la visibilidad del método o la amplía, nunca la reduce. Además, puede utilizar la anotación `@Override` para mayor claridad. Gracias a este mecanismo, diferentes clases pueden compartir la misma estructura en sus métodos pero reaccionar de forma distinta, lo que habilita uno de los principios fundamentales de la POO: el **polimorfismo**.

---

##  4. Override aplicado al Colibrí
La clase `Colibri` redefine varios métodos heredados para adaptarlos a sus características propias. Su versión de `presentarse()` ofrece un mensaje personalizado, `volar(int tiempo)` implementa un comportamiento específico según la duración del vuelo, y `comer(Flor flor)` permite una interacción directa con la flor para alimentarse mediante néctar. Aunque estos métodos tienen su origen en `Ave`, la clase `Colibri` los especializa para reproducir de manera más precisa su comportamiento real dentro del ecosistema.

---

##  5. Override aplicado al Pato
La clase `Pato` también sobrescribe métodos heredados y además utiliza sobrecarga para ofrecer variantes de un mismo comportamiento. Su método `presentarse()` tiene un estilo propio, `volar()` refleja las capacidades particulares del pato, `comer()` modela una alimentación sencilla, y `comer(String comida)` es una versión sobrecargada que permite especificar el tipo de alimento. Este conjunto de redefiniciones y sobrecargas demuestra cómo una clase hija puede ampliar o modificar el comportamiento heredado sin perder la estructura base que la clase padre proporciona.

---

##  6. Representación de esto en UML
En UML, la herencia se representa mediante una flecha con un triángulo apuntando hacia la clase padre, indicando que una clase hija extiende la funcionalidad de la base. Los constructores aparecen como operaciones con el mismo nombre que la clase, mientras que los métodos sobrescritos pueden mostrarse tanto en la clase padre como en la hija con su implementación especializada. UML permite visualizar qué métodos se heredan, cuáles se modifican y cómo se organiza la jerarquía, ofreciendo una visión clara de las relaciones y responsabilidades entre clases.

---

##  7. ¿Qué logra la combinación de constructores + override?
Los constructores aseguran que cada objeto inicie con valores adecuados, mientras que el override permite que las clases hijas adapten el comportamiento heredado a sus propias necesidades. Cuando se crean instancias como `new Colibri("Piquito")` o `new Pato("Donald")` y se invocan métodos como `presentarse()` o `comer()`, cada objeto responde de manera distinta aunque compartan la misma estructura de clase padre. Esta combinación de herencia, inicialización especializada y sobreescritura de métodos permite crear sistemas flexibles, organizados y fáciles de extender, donde el diseño en UML se refleja directamente en la implementación final en Java.


