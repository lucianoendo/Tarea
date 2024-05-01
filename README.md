# Control de versiones en GIT con el código fuente

## Ubicación del código fuente
El código fuente se encuentra en el archivo `SRC/Tarea.java`.

## Código fuente en Java

```java
import java.util.Scanner;

public class Tarea {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Ingrese la cantidad de empleados que consumieron combustible durante el mes:");
        int cantidadEmpleados = scanner.nextInt();

        double consumoAnualTotal = 0;

        for (int i = 1; i <= cantidadEmpleados; i++) {
            System.out.println("Ingrese el consumo de combustible al mes del empleado " + i + " en litros:");
            double consumoEmpleado = scanner.nextDouble();
            consumoAnualTotal += consumoEmpleado;
        }

        double consumoAnualPromedio = consumoAnualTotal / cantidadEmpleados;

        System.out.println("El consumo mensual total de combustible es: " + consumoAnualTotal + " litros");
        System.out.println("El consumo mensual promedio por empleado es: " + consumoAnualPromedio + " litros");

        scanner.close();
    }
}
