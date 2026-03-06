Packet Tracer - Creación de una red simple

## Objetivos

En esta actividad, creará una red simple en Packet Tracer en el Espacio de trabajo lógico.

Parte 1: Crear una red simple

Parte 2: Configurar los dispositivos finales y verificar la conectividad

## Instrucciones

## Parte 1: Construya una red simple

En esta parte, creará una red simple mediante la implementación y la conexión de los dispositivos de red en el Espacio de trabajo lógico.

### Paso 1: Agregue dispositivos de red al espacio de trabajo.

En este paso, agregará un PC, un portátil y un cable módem al espacio de trabajo lógico.

Un cable módem es un dispositivo de hardware que permite las comunicaciones con un Proveedor de servicios de Internet (ISP). El cable coaxial del ISP está conectado al cable módem y también se conecta un cable Ethernet de la red local. El cable módem convierte la conexión coaxial en una conexión Ethernet.

Mediante el cuadro de Device-Type Selection (selección de Tipo de dispositivo), añada los siguientes dispositivos al espacio de trabajo. La categoría y la subcategoría asociadas al dispositivo se enumeran a continuación:

=   **PC**: End Devices > End Devices > PC

=   **Laptop**: End Devices > End Devices > Laptop

=   **Cable Modem**: Network Devices > WAN Emulation > Cable Modem

### Paso 2: Cambie los nombres en pantalla de los dispositivos de red.

a.    Para cambiar los nombres de los dispositivos de red, haga clic en el icono del dispositivo en el Espacio de trabajo lógico (Logical Workspace).

b.    Haga clic en la ventana de **Config** en la ventana de configuración del dispositivo.

c.    Ingrese el nuevo nombre del dispositivo recién agregado en el campo **Display Name** : PC, Laptop, and Cable Modem.

### Paso 3: Agregue el cableado físico entre los dispositivos en el espacio de trabajo.

Con el cuadro de Device-Type Selection (selección de tipo de dispositivos), agregue el cableado físico entre los dispositivos en el espacio de trabajo.

a.    La PC necesita un cable de cobre de conexión directa para conectarse al router inalámbrico. En el cuadro de Device-Type Selection (selección de Tipo de dispositivo), haga clic en **Connections** (icono de rayo). Seleccione el cable de cobre de conexión de conexión directa en el cuadro de selección de dispositivos, y conéctelo a la interfaz **FastEthernet0** de la PC y la interfaz **Ethernet 1** del router inalámbrico.

b.     El router inalámbrico necesita un cable de cobre de conexión directa para conectarse al cable módem. Seleccione el cable de cobre de conexión directa en el cuadro de selección de dispositivos, y conéctelo a la interfaz de Internet del router inalámbrico y a la interfaz de **Puerto 1** del cable módem.

c.     El cable módem necesita un Cable coaxial para conectarse a la nube de Internet. Seleccione el cable coaxial en el cuadro de selección de dispositivos, y conéctelo a la interfaz de **Puerto 0** del cable módem y a la interfaz **Coaxial 7** de la nube de Internet.

## Parte 2: Configurar los dispositivos finales y verificar la conectividad

En esta parte, conectará una PC y una computadora portátil al enrutador inalámbrico. La PC se conectará a la red mediante un cable Ethernet. Para la computadora portátil, reemplazará la tarjeta de interfaz de red (NIC) Ethernet con cable por una NIC inalámbrica y conectará la computadora portátil al enrutador de forma inalámbrica.

Una vez que ambos dispositivos finales estén conectados a la red, verificará la conectividad a cisco.srv. A la PC y al portátil se les asignará una dirección IP (Protocolo de Internet). El Protocolo de Internet es un conjunto de reglas para enrutar y direccionar datos en Internet. Las direcciones IP se utilizan para identificar los dispositivos en una red y permitir que los dispositivos se conecten y transfieran datos en una red.

### Paso 1: Configure la PC.

En este paso, configurará el PC para la red cableada.

a.     Haga clic en la **PC**. En la pestaña **Desktop**, vaya a **IP Configuration** para verificar que DHCP esté habilitado y que el equipo haya recibido una dirección IP.

Seleccione **DHCP** para el encabezado Configuración de IP si no ve una dirección IP para el Campo dirección IPv4. Observe el proceso mientra la PC recibe una dirección IP del servidor DHCP.

DHCP significa protocolo de configuración dinámica de host Este protocolo asigna direcciones IP a los dispositivos de forma dinámica. En esta sencilla red, el enrutador inalámbrico está configurado para asignar direcciones IP a los dispositivos que solicitan direcciones IP. Si DHCP está deshabilitado, deberá asignar una dirección IP y configurar toda la información necesaria para comunicarse con otros dispositivos de la red e Internet.

b.     Cierre la ventana de **Configuración IP**. En la pestaña **Escritorio**, haga clic en el **Símbolo del sistema**.

c.    En el prompt, escriba **ipconfig /all** para revisar la información de direcciones IPv4 del servidor DHCP. La PC debe recibir una dirección IPv4 en el rango de 192.168.0.x.

**Nota:** Hay dos tipos de direcciones IP: IPv4 e IPv6. Una dirección IPv4 (protocolo de Internet versión 4) es una cadena de números en forma de x.x.x.x tal como ha estado utilizando en este laboratorio. A medida que crecía Internet, se hizo mayor la necesidad de nuevas direcciones IP. Por lo tanto, IPv6 (protocolo de Internet versión 6) se introdujo a finales de la década de 1990 para abordar las limitaciones de IPv4. Los detalles del direccionamiento IPv6 están fuera del alcance de esta actividad.

d.    Pruebe la conectividad al servidor Cisco.srv en la PC. Desde el símbolo del sistema, emita el comando **ping cisco.srv** Puede tardar unos minutos para el retorno del ping. Se deben recibir cuatro respuestas, como se muestra en la figura.

### Paso 2: Configure la computadora portátil.

En este paso, configure la computadora portátil para acceder a la red inalámbrica.

a.    Haga clic en **Laptop** y seleccione la pestaña Physicial **(Físico)**.

b.     En la pestaña **Physical** , debe quitar el módulo Ethernet de cobre y reemplazarlo por el módulo inalámbrico WPC300N.

1)    Apague la **Laptop** haciendo clic en el botón de encendido que se encuentra a un costado de la computadora portátil.

2)    Quite el módulo de Ethernet de cobre instalado actualmente haciendo clic en el módulo al costado de la computadora portátil, y arrástrelo al panel **Módulos** a la izquierda de la ventana de la computadora portátil.

3)   Instale el módulo inalámbrico **WPC300N** haciendo clic en él en el panel **Módulos** , y arrástrelo al puerto del módulo vacío al costado de la computadora portátil.

4)   Vuelva a encender la **Laptop** haciendo clic en el botón de Laptop Power (encendido de la Computadora portátil).

c.    Con el módulo inalámbrico instalado, conecte la computadora portátil a la red inalámbrica. Haga clic en la pestaña **Escritorio** y luego haga clic en **Computadora inalámbrica**.

d.    Seleccione la pestaña **Connect** (Conectar). Después de un ligero retraso, la red inalámbrica **HomeNetwork** estará visible en la lista de redes inalámbricas. Si es necesario haga clic en **Actualizar** para ver la lista de redes disponibles. Seleccione **HomeNetwork**. Haga clic en **Conectar**.

e.    Cierra la**PC Wireless (PC Inalambrica)**. Seleccione **Navegador web** en la pestaña Escritorio.

f.      En el Navegador web, acceda a **cisco.srv**.

## Reflexión

Ahora que ha verificado la conectividad a cisco.srv, use el comando **ipconfig** del Command Prompt para completar la tabla de direcciones IP a continuación:

![[Pasted image 20251210223910.png]]

Las direcciones IP de los dispositivos finales pueden oscilar entre 192.168.0.2 y 192.168.0.254. Cada adaptador de red (NIC) obtendrá una dirección IP única en la misma red.

La máscara de subred IPv4 (o la longitud del prefijo) se usa para diferenciar la porción de red de la porción de host de una dirección IPv4. Puede relacionar la dirección IP con la dirección de su calle. La máscara de subred define la longitud del nombre de la calle. La parte de la red de la dirección es su calle, 192.168.0. El número de casa es el puerto de host de la dirección IP. Para la dirección IP 192.168.0.2, el número de casa es el 2 y la calle es 192.168.0. Si hay más de una casa en la misma calle, por ejemplo, la casa número 3, tendrá una dirección 192.168.0.3. El número máximo de casas en esta calle es de 253, que varía entre 2 y 254.

La puerta de enlace predeterminada es análoga a la entrada de una calle. El tráfico de la calle 192.168.0 tiene que salir a través de la intersección con otra calle. Otra calle es otra red. En esta red, la puerta de enlace predeterminada es el enrutador inalámbrico que dirige el tráfico desde la red local al cable módem y, a continuación, el tráfico se envía al ISP.