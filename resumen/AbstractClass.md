# 🔷 Constructores, Override y Clases Abstractas — Resumen Completo

##  1. ¿Qué son los constructores?
Los constructores son métodos especiales que se ejecutan automáticamente al crear un objeto con `new`. Su función es inicializar los atributos y preparar la instancia con un estado válido. En una clase base como `Ave`, pueden existir varios constructores sobrecargados: uno por defecto que asigna valores iniciales, otro que recibe solamente el nombre utilizando `this()` para reutilizar lógica, y un tercero que recibe nombre y sexo encadenando la inicialización. Esta técnica, llamada **sobrecarga de constructores**, permite crear objetos de distintas formas manteniendo coherencia y evitando duplicación de código. Los constructores no tienen tipo de retorno y deben llamarse igual que la clase.

---

##  2. Constructores en clases hijas
Las clases hijas como `Colibri` y `Pato` no heredan directamente los constructores de la clase padre, pero pueden invocarlos mediante `super()`. Esto permite que la parte heredada del objeto se inicialice antes de configurar los atributos específicos de la clase hija. Si una clase hija no define sus propios constructores, Java genera uno por defecto que llama al constructor vacío de la clase padre. De esta forma, constructores y herencia trabajan en conjunto para garantizar que cada objeto se construya correctamente desde su origen.

---

##  3. ¿Qué es el Override?
El override ocurre cuando una clase hija redefine un método heredado conservando su firma (nombre, parámetros y tipo de retorno), pero proporcionando una nueva implementación. Esto permite que el comportamiento del método se adapte específicamente a la clase hija. Para que el override sea válido, no puede reducir la visibilidad del método y puede usar `@Override` para mayor claridad. Gracias al override, diferentes clases pueden reaccionar de forma distinta a un mismo mensaje, lo que habilita el principio del **polimorfismo** dentro de la programación orientada a objetos.

---

##  4. Override aplicado al Colibrí
La clase `Colibri` sobrescribe métodos heredados para adaptarlos a su comportamiento particular. Su implementación de `presentarse()` muestra un mensaje propio de la especie, `volar(int tiempo)` ajusta la acción al tiempo de vuelo y `comer(Flor flor)` permite simular su alimentación mediante néctar. Aunque estos métodos provienen de la estructura heredada, el colibrí los especializa para reflejar de forma más precisa cómo actúa este tipo de ave.

---

##  5. Override aplicado al Pato
La clase `Pato` también redefine métodos heredados y combina override con sobrecarga. `presentarse()` ofrece un mensaje personalizado, `volar()` representa su estilo de vuelo característico, `comer()` modela una acción básica y `comer(String comida)` añade una variación sobrecargada que permite especificar un alimento. Esta mezcla de override y sobrecarga permite que el pato comparta estructura común con otras aves y, al mismo tiempo, mantenga comportamientos únicos y diferenciados.

---

##  6. ¿Qué es una clase abstracta?
Una clase abstracta es una clase que no puede instanciarse directamente y se utiliza como modelo conceptual para otras clases. Puede contener métodos concretos y métodos abstractos, estos últimos sin implementación y obligatorios para las clases hijas. Las clases abstractas permiten definir atributos y comportamientos generales, evitando la creación de objetos que no representan entidades específicas. Representan ideas más amplias que sirven como base para desarrollar clases concretas.

---

##  7. Uso de clases abstractas en jerarquías
Una clase abstracta como `Ave` puede contener atributos comunes (nombre, tamaño, sexo) y métodos concretos como `volar()`. Además, puede incluir métodos abstractos como `presentarse()`, que obligan a las clases hijas a implementar su propia versión. Esto garantiza una estructura uniforme mientras se permite la especialización necesaria en cada clase hija.

```java
public abstract class Ave {
    String nombre;
    Float tamano;
    Boolean tieneAla;
    char sexo;

    public void volar() {
        System.out.println("El ave está volando.");
    }

    public abstract void presentarse();
}
```
##  8. Representación en UML

En UML, una clase abstracta se representa con su nombre en cursiva, así como sus métodos abstractos. La herencia se muestra mediante una flecha con triángulo apuntando hacia la clase base. Esta representación permite visualizar qué clases son abstractas, cuáles son concretas, qué métodos deben implementarse obligatoriamente y cómo se organiza la jerarquía interna del sistema.

## 9. Conexión entre constructores, override y clases abstractas

Las clases abstractas definen la estructura general; los constructores garantizan que cada objeto se inicialice con valores correctos; y el override permite que las clases hijas personalicen o reemplacen comportamientos heredados. Al crear objetos como new Colibri("Piquito") o new Pato("Donald"), los constructores establecen el estado inicial y los métodos sobrescritos determinan comportamientos únicos. La combinación de herencia, abstracción, sobrecarga, constructores y override permite construir sistemas flexibles, organizados y escalables siguiendo los principios fundamentales de la programación orientada a objetos.