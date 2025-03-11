# Herencia en Java

La **herencia** es un mecanismo en Java que permite a una clase adquirir las propiedades y comportamientos de otra clase. Facilita la reutilización de código y la creación de jerarquías de clases.

## Definición de Herencia
En Java, la herencia se implementa utilizando la palabra clave `extends`. La clase que hereda se llama **subclase** y la clase de la que se hereda se llama **superclase**.

### Sintaxis:
```java
class SuperClase {
    // Código de la superclase
}

class SubClase extends SuperClase {
    // Código de la subclase
}
```

## Tipos de Herencia en Java

| Tipo de Herencia | Descripción |
|-----------------|-------------|
| **Herencia Simple** | Una subclase hereda de una sola superclase. |
| **Herencia Multinivel** | Una clase hereda de otra clase, que a su vez hereda de otra clase. |
| **Herencia Jerárquica** | Varias subclases heredan de una misma superclase. |

!!! warning "Cuidado" 
    Java **no soporta herencia múltiple** (una clase no puede heredar de más de una clase a la vez), pero se puede lograr mediante interfaces.

## Ejemplo de Herencia en Java
```java
// Superclase
class Animal {
    String nombre;
    
    void hacerSonido() {
        System.out.println("Haciendo un sonido...");
    }
}

// Subclase que hereda de Animal
class Perro extends Animal {
    
    void ladrar() {
        System.out.println("Guau Guau!");
    }
}

public class Main {
    public static void main(String[] args) {
        Perro miPerro = new Perro();
        miPerro.nombre = "Firulais";
        miPerro.hacerSonido(); // Método heredado de Animal
        miPerro.ladrar(); // Método propio de Perro
    }
}
```

## Uso de super
La palabra clave `super` se usa para:
1. Llamar al **constructor** de la superclase.
2. Acceder a métodos o atributos de la superclase.

Ejemplo:
```java
class Animal {
    Animal() {
        System.out.println("Animal creado");
    }
}

class Perro extends Animal {
    Perro() {
        super(); // Llama al constructor de Animal
        System.out.println("Perro creado");
    }
}
```

## Beneficios de la Herencia
**Reutilización de código**: Evita la duplicación de código.
**Mantenibilidad**: Facilita modificaciones y mejoras.
**Organización**: Permite estructurar el código de forma jerárquica.

La herencia es una característica clave en la **Programación Orientada a Objetos (POO)** que ayuda a mejorar la modularidad y eficiencia del código en Java.
