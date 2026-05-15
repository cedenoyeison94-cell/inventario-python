# Matriz de inventario
# [Código, Nombre, Stock Actual, Stock Mínimo]

inventario = [
    [101, "Cuadernos", 15, 20],
    [102, "Lápices", 50, 30],
    [103, "Borradores", 8, 15],
    [104, "Marcadores", 12, 12],
    [105, "Reglas", 5, 10]
]

# Función para calcular cantidad a pedir
def calcular_pedido(stock_actual, stock_minimo):
    if stock_actual < stock_minimo:
        return stock_minimo - stock_actual
    else:
        return 0

# Mostrar lista de pedidos
print("LISTA DE PEDIDOS\n")

for articulo in inventario:
    codigo = articulo[0]
    nombre = articulo[1]
    stock_actual = articulo[2]
    stock_minimo = articulo[3]

    cantidad_pedir = calcular_pedido(stock_actual, stock_minimo)

    print(f"Artículo: {nombre}")
    print(f"Código: {codigo}")
    print(f"Cantidad a pedir: {cantidad_pedir}\n")
    
