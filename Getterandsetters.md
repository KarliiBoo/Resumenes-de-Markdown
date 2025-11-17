#  Resumen Completo en Formato Markdown  
Incluye: **Herencia • Constructores • Override • Clases Abstractas • Getters y Setters**

---

#  1. Herencia en el Proyecto  
La herencia permite que una clase hija tome los atributos y métodos de una clase padre, reutilizando código y organizando las jerarquías lógicas. En el proyecto, `Colibri`, `Pato` y `Correcamino` heredan de `Ave`, compartiendo características como `nombre`, `tamano`, `tieneAla`, `sexo`, `tienePata` y `claveSecreta`.  
Cada clase hija puede **añadir métodos**, **especializar funciones** o **modificar comportamientos**, lo que la vuelve más específica sin perder la base común.

###  Comportamientos del Colibrí  
- `presentarse()`  
- `volar(int tiempo)`  
- `comer(Flor flor)`

###  Comportamientos del Pato  
- `presentarse()`  
- `volar()`  
- `comer()`  
- `comer(String comida)`  

Aun siendo todas aves, cada una redefine o amplía ciertas capacidades, demostrando polimorfismo y especialización.

---

#  2. Constructores  
Los constructores son métodos especiales que se ejecutan cuando se crea un objeto con `new`. Su objetivo es inicializar los atributos para que el objeto empiece en un estado válido.

En `Ave` hay varios constructores:

###  Constructor por defecto  
Inicializa todo con valores predefinidos:
```java
public Ave() {
    this.nombre = "Sin nombre";
    this.tamano = 0F;
    this.tieneAla = true;
    this.sexo = 'M';
    this.tienePata = true;
    this.claveSecreta = "NoSeasSapo";
}
```
#  3. Override (Sobreescritura)
El override permite que una clase hija redefina un método heredado manteniendo el mismo nombre, tipo de retorno y parámetros. Esto permite personalizar comportamientos sin alterar la clase padre. En el proyecto, cada ave redefine métodos como `presentarse()` o `volar()` para adaptarlos a su especie. El polimorfismo ocurre cuando diferentes objetos responden de manera distinta al mismo método heredado.

**Ejemplos:**
- El Colibrí redefine `presentarse()` para sonar como un colibrí.
- El Pato redefine `volar()` para limitar su vuelo.
- El Correcamino puede redefinir métodos según sus características.

---

#  4. Override aplicado a las aves
Cada clase hija implementa su propia versión de los métodos heredados:

###  Colibrí
- `presentarse()` imprime un sonido distintivo.
- `volar(int tiempo)` retorna verdadero si puede volar durante ese tiempo.
- `comer(Flor flor)` modela la alimentación con néctar.

###  Pato
- `presentarse()` imprime un sonido distinto.
- `volar()` evalúa si puede volar dependiendo de su condición.
- `comer()` y `comer(String comida)` permiten comportamientos variados.

Los métodos vienen de la clase `Ave` pero cada hijo los **especializa** según sus capacidades.

---

#  5. Clases Abstractas
Una clase abstracta sirve como modelo general y no puede ser instanciada directamente. En el proyecto, `Ave` es abstracta porque representa un concepto genérico del que no deben crearse objetos directamente. Solo las aves reales (Colibrí, Pato, Correcamino) pueden instanciarse.

**Propiedades clave:**
- Puede contener métodos completos y métodos abstractos.
- Evita la creación de objetos sin sentido (como `new Ave()`).
- Refuerza la estructura de herencia.
- Forza a las clases hijas a implementar determinados métodos si fueran abstractos.

Esto organiza la jerarquía y garantiza que solo existan instancias de clases concretas.

---

#  6. Getters y Setters
Los atributos de `Ave` son privados para mantenerlos protegidos. Por eso se necesitan getters y setters: métodos que permiten leer o modificar esos atributos de manera segura. Así, las clases hijas no acceden directamente a los datos, sino mediante métodos controlados.

###  Getters
Permiten leer valores como:
- `getNombre()`
- `getTamano()`
- `getTieneAla()`
- `getSexo()` (incluye lógica propia)
- `getTienePata()`
- `getClaveSecreta()`

###  Setters
Permiten actualizar atributos con validación, por ejemplo:
- `setNombre(String nombre)`
- `setTamano(Float tamano)`
- `setTieneAla(Boolean tieneAla)`
- `setSexo(Character sexo)` (valida 'M', 'H' o 'F')
- `setClaveSecreta(String claveSecreta)`

Estos métodos controlan el estado interno del objeto, evitando errores y manteniendo encapsulación.

---
