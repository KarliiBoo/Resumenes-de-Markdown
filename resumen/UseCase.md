#  Resumen: Use Case (Caso de Uso)

##  ¿Qué es un Use Case?
Un **Use Case** o **Caso de Uso** es una descripción de cómo un usuario (actor) interactúa con un sistema para lograr un objetivo específico. Se usa para entender cómo debe comportarse un sistema desde el punto de vista del usuario.

---

##  Elementos principales
- **Actor:** Usuario o sistema externo que interactúa con el sistema.
- **Objetivo:** Lo que el actor quiere conseguir.
- **Sistema:** La aplicación que responde a las acciones del actor.
- **Flujo principal:** Pasos normales para lograr el objetivo.
- **Flujos alternativos:** Situaciones especiales o errores posibles.

---

##  ¿Para qué sirve?
- Para **describir requisitos** del sistema.
- Para **organizar funciones** y entender cómo se usa el sistema.
- Para **diseñar correctamente** la interacción.
- Para **crear casos de prueba**.

---

##  Estructura típica de un Caso de Uso
# Caso de Uso: <Nombre>

**Actor:** <actor principal>  
**Objetivo:** <objetivo del actor>  
**Precondiciones:** <condiciones antes de iniciar>  

**Flujo Principal:**
1. Paso 1  
2. Paso 2  
3. ...

**Flujos Alternativos:**
- A1: Descripción del caso alterno
- A2: Descripción del caso alterno

**Postcondiciones:** <estado final después del caso de uso>

---

##  Ejemplo (Tema: Animales)
# Caso de Uso: Registrar un Animal en el Refugio

**Actor:** Cuidador del refugio  
**Objetivo:** Agregar un nuevo animal a la base de datos del refugio  

**Precondiciones:**  
- El cuidador debe estar autenticado en el sistema.  
- El animal debe haber sido recibido físicamente en el refugio.  

**Flujo Principal:**
1. El cuidador selecciona la opción "Registrar nuevo animal".
2. El cuidador ingresa datos del animal (especie, nombre, edad, estado de salud).
3. El cuidador confirma la información.
4. El sistema guarda los datos del animal.
5. El sistema muestra un mensaje de registro exitoso.

**Flujos Alternativos:**
- **A1:** Falta un dato obligatorio → El sistema muestra un error y pide completar la información.
- **A2:** El sistema no puede guardar la información → Muestra un mensaje de fallo y sugiere reintentar.

**Postcondiciones:**  
- El animal queda registrado en la base de datos con un ID único.

