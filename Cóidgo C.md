## CÓDIGO FUNCIONAL

```c

#include <stdio.h>
#define FILAS 2
#define COLUMNAS 3
void completarMatrices(int matrizA[FILAS][COLUMNAS], int matrizB[FILAS][COLUMNAS]);
void sumaMatriz(int matrizA[FILAS][COLUMNAS], int matrizB[FILAS][COLUMNAS], int resultado[FILAS][COLUMNAS]);
void restaMatriz(int matrizA[FILAS][COLUMNAS], int matrizB[FILAS][COLUMNAS], int resultado[FILAS][COLUMNAS]);
void multiplicacionMatriz(int matrizA[FILAS][COLUMNAS], int matrizB[FILAS][COLUMNAS], int resultado[FILAS][COLUMNAS]);
void mostrarResultado(int matriz[FILAS][COLUMNAS], const char *nombreOperacion);
int main()
{
    int matrizA[FILAS][COLUMNAS];
    int matrizB[FILAS][COLUMNAS];
    int resultado[FILAS][COLUMNAS];
    completarMatrices(matrizA, matrizB);
    sumaMatriz(matrizA, matrizB, resultado);
    mostrarResultado(resultado, "SUMA (A + B)");
    restaMatriz(matrizA, matrizB, resultado);
    mostrarResultado(resultado, "RESTA (A - B)");
    multiplicacionMatriz(matrizA, matrizB, resultado);
    mostrarResultado(resultado, "MULTIPLICACION (A * B)");
    return 0;
}
void completarMatrices(int matrizA[FILAS][COLUMNAS], int matrizB[FILAS][COLUMNAS])
{
    int i, j;
    printf("--- Ingrese los datos de la Matriz A ---\n");
    for (i = 0; i < FILAS; i++)
    {
        for (j = 0; j < COLUMNAS; j++)
        {
            printf("Posicion [%d][%d]: ", i, j);
            scanf("%d", &matrizA[i][j]);
        }
    }
    printf("\n--- Ingrese los datos de la Matriz B ---\n");
    for (i = 0; i < FILAS; i++)
    {
        for (j = 0; j < COLUMNAS; j++)
        {
            printf("Posicion [%d][%d]: ", i, j);
            scanf("%d", &matrizB[i][j]);
        }
    }
    printf("\n");
}
void sumaMatriz(int matrizA[FILAS][COLUMNAS], int matrizB[FILAS][COLUMNAS], int resultado[FILAS][COLUMNAS])
{
    for (int i = 0; i < FILAS; i++)
    {
        for (int j = 0; j < COLUMNAS; j++)
        {
            resultado[i][j] = matrizA[i][j] + matrizB[i][j];
        }
    }
}
void restaMatriz(int matrizA[FILAS][COLUMNAS], int matrizB[FILAS][COLUMNAS], int resultado[FILAS][COLUMNAS])
{
    for (int i = 0; i < FILAS; i++)
    {
        for (int j = 0; j < COLUMNAS; j++)
        {
            resultado[i][j] = matrizA[i][j] - matrizB[i][j];
        }
    }
}
void multiplicacionMatriz(int matrizA[FILAS][COLUMNAS], int matrizB[FILAS][COLUMNAS], int resultado[FILAS][COLUMNAS])
{
    for (int i = 0; i < FILAS; i++)
    {
        for (int j = 0; j < COLUMNAS; j++)
        {
            resultado[i][j] = matrizA[i][j] * matrizB[i][j];
        }
    }
}
void mostrarResultado(int matriz[FILAS][COLUMNAS], const char *nombreOperacion)
{
    printf("Resultado de: %s\n", nombreOperacion);
    for (int i = 0; i < FILAS; i++)
    {
        printf("[ ");
        for (int j = 0; j < COLUMNAS; j++)
        {
            printf("%d ", matriz[i][j]);
        }
        printf("]\n");
    }
    printf("\n");
}

```
