#  Herencia en Programación Orientada a Objetos (POO)

La **herencia** es un mecanismo que permite que una clase “hija” reutilice y extienda las características de una clase “padre”. Esto evita repetir código, organiza mejor los programas y ayuda a modelar objetos del mundo real.

En el ejemplo del profesor, se trabaja con un pequeño ecosistema formado por **aves** y **plantas**, representado mediante clases y diagramas UML.

---

##  1. Clase Padre: `Ave`
La clase `Ave` agrupa las características generales que comparten todas las aves:

- **Atributos comunes**
  - `nombre : String`
  - `tamano : Float`
  - `tieneAla : Boolean`
  - `sexo : char`

- **Constructores**
  - Constructor por defecto → inicializa atributos
  - Constructor con nombre
  - Constructor con nombre y sexo

La clase `Ave` funciona como una plantilla base sobre la cual se construyen aves específicas.

---

##  2. Clases Hijas: `Colibri` y `Pato`
Las clases hijas **extienden** a `Ave`:

```java
public class Colibri extends Ave { }
public class Pato extends Ave { }
```
Esto significa que las clases hijas heredan automáticamente **todos los atributos y métodos** de la clase padre, y además pueden:

- **Añadir nuevos métodos**
- **Modificar comportamientos**
- **Especializar funciones**

---

##  Comportamientos del *Colibrí*
- `presentarse()`
- `volar(int tiempo)`
- `comer(Flor flor)`

---

##  Comportamientos del *Pato*
- `presentarse()`
- `volar()`
- `comer()`
- `comer(String comida)`

---

Cada clase define sus propias acciones, aunque ambas sean aves gracias al uso de **herencia**, lo que permite reusar código y especializar comportamientos según la especie.

---
##  Clase *Flor* (interacción con el Colibrí)

La clase `Flor` no forma parte de la herencia de aves, pero es importante en el ecosistema porque interactúa directamente con el Colibrí. Sus principales comportamientos son:

- `crecer()`
- `florear(int tiempo)`
- `darNectar()`

La interacción se da cuando el Colibrí utiliza estos métodos para alimentarse. Esto demuestra que, además de la herencia, en POO también existen **asociaciones entre clases**, es decir, objetos que colaboran entre sí sin compartir una jerarquía.

---
##  Relación entre clases en el UML

En el diagrama UML presentado por el profesor se observa:

- **Herencia:**  
  - `Colibri` ← `Ave`  
  - `Pato` ← `Ave`

- **Asociación:**  
  - `Colibri` usa a `Flor` para alimentarse.

- **Coordinación:**  
  - La clase `Controller` crea los objetos e invoca sus métodos.

- **Ejecución:**  
  - La clase `App` contiene el `main`, que sirve como punto de inicio del programa.

El UML permite visualizar cómo se conectan las clases entre sí antes de escribir el código, ayudando a organizar la estructura y roles de cada una.

---
##  Herencia en acción (código final del proyecto)

```java
Flor flor1 = new Flor("Rosa");
Colibri colibri1 = new Colibri("Piquito", 'H');
Pato pato1 = new Pato("Donald", 'M');

pato1.presentarse();
colibri1.presentarse();

flor1.crecer();
flor1.florear(10);

colibri1.volar();
colibri1.comer(flor1);
```

En este fragmento se observa que:

Tanto Colibri como Pato pueden usar atributos heredados desde Ave.

Cada clase aplica sus propios comportamientos especializados.

Los objetos colaboran entre sí mostrando el uso práctico de herencia, asociaciones y métodos personalizados.

Este ejemplo une herencia, especialización, asociación y polimorfismo, demostrando cómo las ideas del UML pasan a convertirse en código real.

![alt text](image-1.png)