# Resumen general del proyecto `Mujer`

## 1. Estructura del proyecto

- Carpeta `src/`
  - **`App.java`** → Clase principal con el método `main`, donde se ejecuta el programa.
  - **`Mujer.java`** → Clase que modela a una mujer con atributos y comportamientos.

---

## 2. Clase `Mujer`

### 2.1. Atributos (estado del objeto)

Dentro de `Mujer.java` se definen varios atributos:

- `public String nombre;`  
- `private Integer edad;`  
- `private Float estatura;`  
- `private Float peso;`  

Esto quiere decir:

- Qué es el **estado de un objeto** (los datos que guarda).
- Qué son los **modificadores de acceso**:
  - `public`: se puede acceder desde cualquier clase.
  - `private`: solo se puede acceder desde dentro de la misma clase.
  - Esto se relaciona con la **encapsulación**.

### 2.2. Constructor

En el código no se escribe un constructor de forma explícita, por lo que:

- Java crea automáticamente un **constructor por defecto**:  
  `public Mujer() { }`
- El profe aprovecha esto para explicar que:
  - El **constructor** sirve para **crear e inicializar** objetos.
  - Si no declaras ninguno, Java genera uno vacío.
  - Si luego se agrega un constructor con parámetros, el por defecto deja de crearse automáticamente.

---

## 3. Métodos de la clase `Mujer`

La clase tiene varios métodos que representan acciones (comportamientos):

### 3.1. `public Boolean bailar(int tiempo, String cancion)`

- **Tipo de retorno:** `Boolean` (devuelve `true` o `false`).
- **Parámetros:**
  - `int tiempo` → minutos que va a bailar.
  - `String cancion` → nombre de la canción.
- **Qué hace:**
  - Muestra un mensaje en consola, por ejemplo:  
    `"Estoy bailando Salsa coque por 30 minutos"`.
  - Devuelve `true` para indicar que sí pudo bailar.
- Aquí el profe explica:
  - Qué es un **método con retorno**.
  - Qué son los **parámetros** y cómo se pasan valores al llamar al método.
  - Uso de `System.out.println` para imprimir mensajes.

### 3.2. `protected void chismearAmiga()`

- **Tipo de retorno:** `void` (no devuelve nada).
- **Parámetros:** no tiene.
- **Acceso:** `protected` (se puede usar en la misma clase, en el mismo paquete y en subclases).
- **Qué hace:** imprime un mensaje como `"Estoy chismeando"`.

Sirve para explicar:

- Métodos **sin retorno** (`void`).
- Otro modificador de acceso: `protected`.

### 3.3. `private void estudiar(String tema)`

- **Tipo de retorno:** `void`.
- **Parámetros:** `String tema` → tema que está estudiando.
- **Acceso:** `private`, solo puede ser usado dentro de la clase `Mujer`.
- **Qué hace:** imprime un mensaje como `"Estoy estudiando POO"`.

Se lo usa para:

- Mostrar métodos **privados**, que suelen ser funciones internas de apoyo.
- Reforzar la idea de encapsulación.

### 3.4. (Versión del video) `private String banar(int tiempo)`

- **Tipo de retorno:** `String`.
- **Parámetros:** `int tiempo`.
- **Qué hace (idea general):**
  - Si el tiempo es mayor que 0, devuelve un texto tipo
    `"Bañándome por X minutos"`.
  - Si no, devuelve un mensaje de error como
    `"No puedo bañarme por un tiempo negativo o cero"`.
- Se usa para explicar:
  - Métodos que **devuelven texto (`String`)**.
  - Uso de **condicionales `if` / `else`**.
  - Validación de parámetros.

---

## 4. Clase `App` (método `main`)

En `App.java` está el punto de entrada del programa:

```java
public class App {
    public static void main(String[] args) throws Exception {
        Mujer m1 = new Mujer();
        m1.nombre = "Ana";
        m1.bailar(30, "Salsa coque");
    }
}
```
Se crea un objeto:
`Mujer m1 = new Mujer();`

Se asigna un valor al atributo público:
`m1.nombre = "Ana";`

Se llama a un método con parámetros:
`m1.bailar(30, "Salsa coque");`