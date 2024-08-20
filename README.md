def calcular_precio_con_porcentaje(precio, porcentaje):
    # Calcula el incremento basado en el porcentaje
    incremento = precio * (porcentaje / 100)
    # Calcula el precio final
    precio_final = precio + incremento
    return precio_final

def calculadora():
    print("Calculadora de incremento de precio")
    
    # Solicita el precio al cliente
    try:
        precio = float(input("Ingrese el precio original: "))
    except ValueError:
        print("Por favor, ingrese un valor numérico válido.")
        return
    
    # Solicita el porcentaje al cliente dentro del rango permitido
    try:
        porcentaje = float(input("Ingrese el porcentaje a aplicar (entre 20 y 30): "))
    except ValueError:
        print("Por favor, ingrese un valor numérico válido.")
        return
    
    if porcentaje < 20 or porcentaje > 30:
        print("El porcentaje debe estar entre 20 y 30.")
        return
    
    # Calcula el precio final
    precio_final = calcular_precio_con_porcentaje(precio, porcentaje)
    
    # Muestra el resultado
    print(f"El precio final con un {porcentaje}% aplicado es: {precio_final:.2f}")

# Ejecutar la calculadora
calculadora()
