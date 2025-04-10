# StartUp-Bots-wssp-


<h1>🤖SalesIqBot💸 (SIB)</h1> <br>
<hr>

<h2>🦉Product Owner - Requisitos</h2>
<h4>Problema que resuelve:</h4>
 <p>*Lentitud y confusiones al momento de realizar una venta</p> 
<h4>Publico objetivo:</h4>
 <p>*Medianas y pequeñas empresas dedicadas al comercio</p>
<h4>3 Funcionalidades clave</h4>

 <ol>
   <li>Interaccion de facil comprension Usuario y Bot y promover el sitio oficial de los clientes<lo></li>
   <li>Panel de opcion multiple que muestre el catalogo de la empresa y Interaccion con el inventario de la empresa</li>
   <li>Recoleccion de datos del cliente, para su envio posterior a la empresa</li>
 </ol>   

  <h2>📊Analista - Analisis</h2>

<h4>Tareas:</h4>

<ul>
  <ol>
   <li>Crear un sistema del inventario de la empresa a tiempo real</li>
   <li>Configurar paneles de opcion multiple al bot los cuales permitan la interaccion facil con el usuario</li>
   <li>Realizar una encuesta de datos del cliente para finalizar el pedido y enviar un ticket unico a la empresa</li>
  </ol>
</ul>
<h4>Dificultad estimada</h4>
<ul>
   <li>Inventario: Alta</li>
   <li>Paneles de bot: Baja</li>
   <li>Encuesta/ticket unico: Alta</li>
</ul>

<h4>Restricciones</h4>
<ul>
   <li>Necesitaremos que el cliente mantenga su inventario actualizado en orden del buen funcionamiento del bot</li>
   <li>El bot no realizara transacciones de dinero</li>
</ul>

<h2>🎨Diseñador - UX/UI - Bocetos y flujo</h2>

<h4>Link a la pagina oficial de los clientes</h4>

![image](https://github.com/user-attachments/assets/f958c047-3cb7-43d3-896a-db0f4c4054b7)

<h4>Simulacion de conversacion con el bot</h4>

 
![image](https://github.com/user-attachments/assets/96a60f76-718d-4292-8a74-96d3413a848d)
![image](https://github.com/user-attachments/assets/e859a417-6a1d-4dee-b42e-a46f65cbaa04)
 
<h4>Diagrama de flujo</h4>


 <div style="display: flex; justify-content: center;">

 ![image](https://github.com/user-attachments/assets/57d1a9df-f06b-46c4-8092-71594220b83d)

</div>

<h2>⚙️Desarrollador - Implementacion</h2>
<ul>
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
</ul>

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

<h2>🔜DevOps/Mantenimiento - Despliegue</h2>
<h4>Despliegue y Mantenimiento</h4>

   <li>El bot se despliega en servidores Linux (Ubuntu Server).</li>

   <li>Se automatiza el despliegue y configuraciones con scripts Bash.</li>

   <li>Se monitorean logs y uso de recursos con herramientas del sistema como journalctl y top.</li>

<h4>Mejoras/Futuras propuestas</h4>

   <li>Dockerización del bot: Para facilitar el despliegue, portabilidad y estandarización del entorno.</li>
   <li>Sistema de monitoreo con alertas: Para detectar caídas o errores en tiempo real.</li>

 
