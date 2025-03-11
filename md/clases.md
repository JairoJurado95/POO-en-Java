# Clases en Java

En Java, una **clase** es una plantilla para crear objetos. Define atributos y métodos que los objetos pueden utilizar.

## Definición de una Clase

Aquí tienes un ejemplo simple de una clase `Persona` en Java:

```java
class Persona {
    // Atributos de la clase
    String nombre;
    int edad;
    
    // Constructor
    Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
    
    // Método para mostrar información
    void mostrarInformacion() {
        System.out.println("Nombre: " + nombre + ", Edad: " + edad);
    }
}
```

## Creación de un Objeto

Para crear un objeto de la clase `Persona`, hacemos lo siguiente:

```java
public class Main {
    public static void main(String[] args) {
        Persona persona1 = new Persona("Carlos", 30);
        persona1.mostrarInformacion();
    }
}
```

!!! tip "Consejo"
    Recuerda que en Java, cada clase debe guardarse en un archivo con el mismo nombre de la clase y la extensión `.java`.


Este código imprimirá:

```
Nombre: Carlos, Edad: 30
```

Así es como se define y usa una clase en Java.