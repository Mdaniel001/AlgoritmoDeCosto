# AlgoritmoDeCosto
//definimos las variables necesarias 
    definir precioOriginal, descuento, iva, cantidad, peso, costoEnvio, costoFinal, precioConDescuento Como Real
    Definir  destino Como Cadena
		
    // Leer los datos del producto y cliente
    Escribir "Ingrese el precio original del producto: "
    Leer precioOriginal
    
    Escribir "Ingrese el descuento (en porcentaje, 0 si no hay descuento): "
    Leer descuento
    
    Escribir "Ingrese la cantidad de productos: "
    Leer cantidad
    
    Escribir "Ingrese el peso del paquete (en kg): "
    Leer peso
    
    Escribir "Ingrese el destino del envío: "
    Leer destino
    
    // Calcular el precio con descuento
    precioConDescuento = precioOriginal - (precioOriginal * (descuento / 100))
    
    // Aplicar el IVA
    iva = precioConDescuento * 0.12
    
    // Aplicar descuento por cantidad
    Si cantidad > 1 Entonces
        precioConDescuento = precioConDescuento - (precioConDescuento * 0.05)
    Fin Si
    
    // Calcular el costo de envío
    costoEnvio = 10 + (2 * peso)
    
    // Calcular el costo final del producto
    costoFinal = (precioConDescuento * cantidad) + costoEnvio + iva
    
    // Mostrar el desglose de costos
    Escribir "Costo del producto sin descuento: $" , precioOriginal
	
    Escribir "Descuento aplicado: $" , (precioOriginal - precioConDescuento)
    Escribir "Precio con descuento: $" , precioConDescuento
    Escribir "Impuestos (IVA): $",iva
    Escribir "Descuento por cantidad: $", (precioConDescuento * 0.05)
    Escribir "Costo de envío: $" ,costoEnvio
    Escribir "Costo final del producto: $", costoFinal
	

proyecto Modulo1
