# Métodos en Java

Los **métodos** en Java representan el comportamiento de una clase. Son bloques de código que se ejecutan cuando se invocan y pueden recibir parámetros, devolver valores o ejecutar acciones específicas.

## Modificadores de Acceso
Los métodos, al igual que los atributos, pueden tener distintos modificadores de acceso.

| Modificador  | Descripción |
|-------------|-------------|
| `public`    | El método es accesible desde cualquier otra clase. |
| `private`   | El método solo es accesible dentro de la misma clase. |
| `protected` | El método es accesible dentro de la misma clase, subclases y clases del mismo paquete. |
| (Sin modificador) | **Package-private**, el método es accesible solo dentro del mismo paquete. |

## Tipos de Métodos
| Tipo  | Descripción |
|-------------|-------------|
| Métodos con retorno | Devuelven un valor especificado con un tipo de dato (ej. `int`, `String`, etc.). |
| Métodos `void` | No devuelven ningún valor, solo ejecutan acciones. |
| Métodos estáticos | Se declaran con `static` y pertenecen a la clase en lugar de a una instancia. |
| Métodos de instancia | Son específicos de cada objeto creado de la clase. |

## Ejemplo de Métodos en Java
```java
public class Calculadora {
    // Método con retorno
    public int sumar(int a, int b) {
        return a + b;
    }

    // Método void
    public void mostrarMensaje() {
        System.out.println("¡Bienvenido a la calculadora!");
    }
}
```

## Métodos Estáticos vs Métodos de Instancia
```java
public class Utilidades {
    // Método estático
    public static int multiplicar(int a, int b) {
        return a * b;
    }
}

public class Main {
    public static void main(String[] args) {
        // Llamada a un método estático
        int resultado = Utilidades.multiplicar(4, 5);
        System.out.println("Resultado: " + resultado);
    }
}
```

## Buenas Prácticas
- **Usar nombres descriptivos** para los métodos.
- **Seguir la convención camelCase** (`calcularPromedio`, `obtenerDatos`).
- **Evitar métodos muy largos**, dividiéndolos en otros más pequeños si es necesario.
- **Documentar los métodos** usando JavaDoc.

!!! tip "Consejo"
    Se dice que un metodo es ideal cuando su código es facilmente legible y no precisamos de hacer scroll para ver todo el código que contiene.