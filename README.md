# StartUp-Bots-wssp-


<h1>Nombre del producto</h1> <br>
<hr>

<h2>🦉Product Owner - Requisitos</h2>
<h4>Problema que resuelve:</h4>
 <p>*Lentitud y confusiones al momento de realizar una venta</p> 
<h4>Publico objetivo:</h4>
 <p>*Medianas y pequeñas empresas dedicadas al comercio</p>
<h4>3 Funcionalidades clave</h4>
<ls>
   <li>Interaccion con el inventario de la empresa</li>
   <li>Panel de opcion multiple que muestre el catalogo de la empresa</li>
   <li>Recoleccion de datos del cliente, para su envio posterior a la empresa</li>
</ls>

<h2>📊Analista - Analisis</h2>

<h4>Tareas:</h4>
   <li>Crear un sistema del inventario de la empresa a tiempo real</li>
   <li>Configurar paneles de opcion multiple al bot los cuales permitan la interaccion facil con el usuario</li>
   <li>Realizar una encuesta de datos del cliente para finalizar el pedido y enviar un ticket unico a la empresa</li>

<h4>Dificultad estimada</h4>
<ls>
   <li>Inventario: Alta</li>
   <li>Paneles de bot: Baja</li>
   <li>Encuesta/ticket unico: Alta</li>
</ls>

<h4>Restricciones</h4>
<ls>
   <li>Necesitaremos que el cliente mantenga su inventario actualizado en orden del buen funcionamiento del bot</li>
   <li>El bot no realizara transacciones de dinero</li>
</ls>

<h2>⚙️Desarrollador - Implementacion</h2>
<ls>
   <li>Feature implementada:</li>
   <li>Pseudocódigo:</li>
   
    Dimensionar inventario[10], Disponibles[10]
    Definir i, opcion Como Entero
    Definir Continuar Como Cadena
    Continuar<-"Si"

    inventario[1] <- "Buso blanco estampado de itachi"
    Disponibles[1] <- "2"

    inventario[2] <- "Camisa gris oversize estampado anime"
    Disponibles[2] <- "4"

    inventario[3] <- "Buso blanco ultima cena akatsuki"
    Disponibles[3] <- "2"

    inventario[4] <- "Buso blanco minecraft"
    Disponibles[4] <- "1"

    inventario[5] <- "Camiseta básica estampada NIKE"
    Disponibles[5] <- "0"

    Escribir "Bienvenido al catalogo de productos"
    Escribir "Aqui encontraras los productos disponibles:"

    Mientras Continuar="Si" Hacer
    Para i <- 1 Hasta 5 Hacer
        Si ConvertirANumero(Disponibles[i]) > 0 Entonces
            Escribir i, ". ", inventario[i], " (Disponibles: ", Disponibles[i], ")"
        FinSi
    FinPara

    Escribir ""
    Escribir "Seleccione el número del producto que desea agregar a su pedido:"
    Leer opcion

    Si ConvertirANumero(Disponibles[opcion]) > 0 Entonces
        Escribir "Producto ", inventario[opcion], " a sido agregado exitosamente."
        Disponibles[opcion] <- ConvertirATexto(ConvertirANumero(Disponibles[opcion]) - 1)
    Sino
        Escribir "Lo sentimos, el producto no está disponible en este momento."
    FinSi
    Escribir "Deseas agregar otro articulo a tu compra? Si/No"
    Leer Continuar
    FinMientras

    Escribir "Redireccionando al proceso de pago, gracias por elegirnos!"

    FinProceso
</ls>

<h2>🕵️QA Tester - Pruebas</h2>

<h4>Caso 1 </h4>
   <li>buen funcionamiento del panel de opción múltiple del catálogo de la empresa. </li>
<h4>Caso 2</h4>
   <li>al no responder al Bot en un periodo 10 minutos, se finaliza la sesión.</li>
<h4>Caso 3</h4>
   <li>si se interrumpen la sección inesperadamente el Bot mantiene un historial de conversación de la última charla iniciada.</li>

<h4>Anticipar posibles errores</h4>
    
   <li>Si el usuario pregunta caracteristicas extras del producto, la interaccion finaliza</li>
   <li>Si el usuario no copia correctamente la opcion de Si/No, la interaccion finaliza</li>
