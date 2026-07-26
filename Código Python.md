
FILAS = 2
COLUMNAS = 3
def completar_matrices():
    matriz_a = []
    matriz_b = []
    print("--- Ingrese los datos de la Matriz A ---")
    for i in range(FILAS):
        fila = []
        for j in range(COLUMNAS):
            val = int(input(f"Posicion [{i}][{j}]: "))
            fila.append(val)
        matriz_a.append(fila)
    print("\n--- Ingrese los datos de la Matriz B ---")
    for i in range(FILAS):
        fila = []
        for j in range(COLUMNAS):
            val = int(input(f"Posicion [{i}][{j}]: "))
            fila.append(val)
        matriz_b.append(fila)       
    print()
    return matriz_a, matriz_b
def suma_matriz(matriz_a, matriz_b):
    resultado = []
    for i in range(FILAS):
        fila = []
        for j in range(COLUMNAS):
            fila.append(matriz_a[i][j] + matriz_b[i][j])
        resultado.append(fila)
    return resultado
def resta_matriz(matriz_a, matriz_b):
    resultado = []
    for i in range(FILAS):
        fila = []
        for j in range(COLUMNAS):
            fila.append(matriz_a[i][j] - matriz_b[i][j])
        resultado.append(fila)
    return resultado
def multiplicacion_matriz(matriz_a, matriz_b):
    # Nota: Realiza la multiplicación elemento a elemento (Hadamard product)
    # exactamente igual que en tu código original de C.
    resultado = []
    for i in range(FILAS):
        fila = []
        for j in range(COLUMNAS):
            fila.append(matriz_a[i][j] * matriz_b[i][j])
        resultado.append(fila)
    return resultado
def mostrar_resultado(matriz, nombre_operacion):
    print(f"Resultado de: {nombre_operacion}")
    for fila in matriz:
        print("[ " + " ".join(str(val) for val in fila) + " ]")
    print()
def main():
    matriz_a, matriz_b = completar_matrices()
    resultado_suma = suma_matriz(matriz_a, matriz_b)
    mostrar_resultado(resultado_suma, "SUMA (A + B)")
    resultado_resta = resta_matriz(matriz_a, matriz_b)
    mostrar_resultado(resultado_resta, "RESTA (A - B)")
    resultado_mult = multiplicacion_matriz(matriz_a, matriz_b)
    mostrar_resultado(resultado_mult, "MULTIPLICACION (A * B)")
if __name__ == "__main__":
    main()
