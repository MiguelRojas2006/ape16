## Código funcional

```c

import java.util.Scanner;

class APE {
    private static final int FILAS = 2;
    private static final int COLUMNAS = 3;

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[][] matrizA = new int[FILAS][COLUMNAS];
        int[][] matrizB = new int[FILAS][COLUMNAS];
        int[][] resultado = new int[FILAS][COLUMNAS];
        completarMatrices(matrizA, matrizB, scanner);
        sumaMatriz(matrizA, matrizB, resultado);
        mostrarResultado(resultado, "SUMA (A + B)");
        restaMatriz(matrizA, matrizB, resultado);
        mostrarResultado(resultado, "RESTA (A - B)");
        multiplicacionMatriz(matrizA, matrizB, resultado);
        mostrarResultado(resultado, "MULTIPLICACION (A * B)");
        scanner.close();
    }

    public static void completarMatrices(int[][] matrizA, int[][] matrizB, Scanner scanner) {
        System.out.println("Ingrese los datos para la Matriz A");
        for (int i = 0; i < FILAS; i++) {
            for (int j = 0; j < COLUMNAS; j++) {
                System.out.printf("Posicion [%d] [%d]: ", i, j);
                matrizA[i][j] = scanner.nextInt();
            }
        }
        System.out.println("Ingrese los datos de la Matriz B");
        for (int i = 0; i < FILAS; i++) {
            for (int j = 0; j < COLUMNAS; j++) {
                System.err.printf("Posicion [%d][%d]:", i, j);
                matrizB[i][j] = scanner.nextInt();
            }
        }
        System.out.println();
    }

    public static void sumaMatriz(int[][] matrizA, int[][] matrizB, int[][] resultado) {
        for (int i = 0; i < FILAS; i++) {
            for (int j = 0; j < COLUMNAS; j++) {
                resultado[i][j] = matrizA[i][j] + matrizB[i][j];
            }
        }
    }

    public static void restaMatriz(int[][] matrizA, int[][] matrizB, int[][] resultado) {
        for (int i = 0; i < FILAS; i++) {
            for (int j = 0; j < COLUMNAS; j++) {
                resultado[i][j] = matrizA[i][j] - matrizB[i][j];
            }
        }
    }

    public static void multiplicacionMatriz(int[][] matrizA, int[][] matrizB, int[][] resultado) {
        for (int i = 0; i < FILAS; i++) {
            for (int j = 0; j < COLUMNAS; j++) {
                resultado[i][j] = matrizA[i][j] * matrizB[i][j];
            }
        }
    }

    public static void mostrarResultado(int[][] matriz, String nombreOperacion) {
        System.out.println("Resultado de: " + nombreOperacion);
        for (int i = 0; i < FILAS; i++) {
            System.out.print("[");
            for (int j = 0; j < COLUMNAS; j++) {
                System.out.print(matriz[i][j] + "");
            }
            System.out.println("]");
        }
        System.out.println();
    }
}

```
