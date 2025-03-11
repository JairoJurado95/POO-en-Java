# Atributos en Java

Los **atributos** en Java son variables que pertenecen a una clase y determinan su estado. Se definen dentro de la clase y pueden tener diferentes modificadores de acceso.

## Modificadores de Acceso
Los modificadores de acceso determinan la visibilidad de los atributos dentro y fuera de la clase.

| Modificador  | Descripción |
|-------------|-------------|
| `public`    | El atributo es accesible desde cualquier otra clase. |
| `private`   | El atributo solo es accesible dentro de la misma clase. |
| `protected` | El atributo es accesible dentro de la misma clase, subclases y clases del mismo paquete. |
| (Sin modificador) | También conocido como **package-private**, el atributo es accesible solo dentro del mismo paquete. |

## Ejemplo de Atributos en Java
```java
public class Persona {
    public String nombre;    // Visible en cualquier parte
    private int edad;        // Solo accesible dentro de esta clase
    protected String genero; // Accesible dentro del paquete y subclases
    String direccion;        // Package-private (sin modificador de acceso)
}
```

## Buenas Prácticas
- Es recomendable **mantener los atributos privados** y utilizar **métodos getter y setter** para acceder y modificar su valor.
- Utilizar `final` si el atributo no debe cambiar después de su inicialización.

## Ejemplo con Getters y Setters
```java
public class Persona {
    private String nombre;

    // Getter
    public String getNombre() {
        return nombre;
    }

    // Setter
    public void setNombre(String nombre) {
        this.nombre = nombre;
    }
}
```

!!! warning "Cuidado"
    Recuerda que si los atributos son privados para acceder a ellos o modificarlos precisaras de estos Getters y Setters como hemos mencionado anteriormente.