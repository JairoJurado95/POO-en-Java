# Excepciones en Java

Las **excepciones** en Java son eventos que ocurren durante la ejecución de un programa y que interrumpen el flujo normal de las instrucciones. Java proporciona un mecanismo robusto para manejar estas situaciones, permitiendo a los desarrolladores gestionar errores de manera controlada.

## Definición de Excepciones
Una excepción es un objeto que representa un error o una condición excepcional que ocurre en un programa. Las excepciones pueden ser generadas por el propio programa o por el entorno de ejecución.

### Sintaxis:
```java
try {
    // Código que puede lanzar una excepción
} catch (TipoDeExcepcion e) {
    // Manejo de la excepción
} finally {
    // Código que se ejecuta siempre, haya o no una excepción
}
```

## Tipos de Excepciones en Java
| Tipo de Excepción | Descripción |
|-----------------|-------------|
| Excepciones Comprobadas | Deben ser declaradas en la firma del método o manejadas con un bloque try-catch. Ejemplo: IOException. |
| Excepciones No Comprobadas | No necesitan ser declaradas ni manejadas. Ejemplo: NullPointerException. |
| Errores | Representan condiciones serias que no se pueden manejar. Ejemplo: OutOfMemoryError. |

!!! warning "Cuidado" 
    Las excepciones comprobadas son aquellas que el compilador obliga a manejar, mientras que las no comprobadas son aquellas que pueden ocurrir en tiempo de ejecución.

## Ejemplo de Manejo de Excepciones en Java
```java
public class Main {
    public static void main(String[] args) {
        try {
            int resultado = 10 / 0; // Esto lanzará una ArithmeticException
        } catch (ArithmeticException e) {
            System.out.println("Error: División por cero.");
        } finally {
            System.out.println("Este bloque se ejecuta siempre.");
        }
    }
}
```

## Creación de Excepciones Personalizadas
Puedes crear tus propias excepciones extendiendo la clase Exception o RuntimeException.

Ejemplo:

```java
class MiExcepcion extends Exception {
    public MiExcepcion(String mensaje) {
        super(mensaje);
    }
}

public class Main {
    public static void main(String[] args) {
        try {
            throw new MiExcepcion("Esta es una excepción personalizada.");
        } catch (MiExcepcion e) {
            System.out.println(e.getMessage());
        }
    }
}
```

## Beneficios del Manejo de Excepciones
* Control de Errores: Permite manejar errores de manera controlada y predecible. 
* Separación de Código: Facilita la separación del código de manejo de errores del código de lógica de negocio.
* Mejor Mantenibilidad: Mejora la legibilidad y mantenibilidad del código al centralizar el manejo de errores.

El manejo de excepciones es una parte esencial de la Programación Orientada a Objetos (POO) en Java, permitiendo a los desarrolladores crear aplicaciones más robustas y resilientes frente a errores.