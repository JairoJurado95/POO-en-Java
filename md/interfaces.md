# Interfaces en Java

Las **interfaces** en Java son un mecanismo que permite definir un contrato que las clases pueden implementar. Proporcionan una forma de especificar métodos que deben ser implementados por las clases, sin proporcionar la implementación de esos métodos.

## Definición de Interfaces
En Java, una interfaz se define utilizando la palabra clave `interface`. Las interfaces pueden contener métodos abstractos (sin implementación) y constantes.

### Sintaxis:
```java
interface MiInterfaz {
    void metodo1();
    int metodo2(int parametro);
}
```

## Características de las Interfaces en Java
| Características | Descripción |
|-----------------|-------------|
| **Métodos Abstractos** | Los métodos en una interfaz son, por defecto, abstractos y públicos. |
| **Múltiples Implementaciones** | Una clase puede implementar múltiples interfaces, lo que permite simular herencia múltiple. |
| **Constantes** | Las variables en una interfaz son, por defecto, public, static y final. |

!!! warning "Cuidado" 
    Las interfaces no pueden contener métodos con implementación (a menos que sean métodos estáticos o métodos por defecto, introducidos en Java 8).

## Ejemplo de Interfaces en Java
```java
interface Animal {
    void hacerSonido();
}

class Perro implements Animal {
    public void hacerSonido() {
        System.out.println("Guau Guau!");
    }
}

class Gato implements Animal {
    public void hacerSonido() {
        System.out.println("Miau Miau!");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal miPerro = new Perro();
        Animal miGato = new Gato();
        
        miPerro.hacerSonido(); // Salida: Guau Guau!
        miGato.hacerSonido();  // Salida: Miau Miau!
    }
}
```

## Métodos por Defecto en Interfaces
Desde Java 8, se pueden definir métodos por defecto en las interfaces, lo que permite proporcionar una implementación predeterminada.

Ejemplo:
```java
interface Vehiculo {
    void conducir();
    
    default void encender() {
        System.out.println("El vehículo está encendido.");
    }
}

class Coche implements Vehiculo {
    public void conducir() {
        System.out.println("Conduciendo el coche.");
    }
}

public class Main {
    public static void main(String[] args) {
        Coche miCoche = new Coche();
        miCoche.encender(); // Salida: El vehículo está encendido.
        miCoche.conducir(); // Salida: Conduciendo el coche.
    }
}
```

## Beneficios de las Interfaces
1. Flexibilidad: Permiten que diferentes clases implementen el mismo conjunto de métodos, facilitando la interoperabilidad. 
2. Desacoplamiento: Promueven un diseño más limpio y modular, separando la definición de métodos de su implementación. 
3. Múltiples Herencias: Permiten que una clase implemente múltiples interfaces, superando la limitación de la herencia simple.

Las interfaces son una parte fundamental de la Programación Orientada a Objetos (POO) en Java, permitiendo un diseño más flexible y escalable del software.