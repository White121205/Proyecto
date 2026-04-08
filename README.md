ESPECIFICACIONES DEL TRABAJO DE 
INVESTIGACIÓN: GNS3 + HIPERVISORES

1_ Arquitectura de Virtualización en Windows 11

 .Aislamiento de Núcleo y VBS: Explicar el impacto de las funciones de seguridad de Windows 11 en la virtualización:
Mayor seguridad para máquinas virtuales
Protección contra malware avanzado
Aislamiento de procesos sensibles
• Activación de VT-x/AMD-V: Procedimiento para habilitar el soporte de hardware y cómo verificarlo desde el sistema operativo.
Reiniciar la PC
Entrar al BIOS
Activar “Virtualization” o “SVM Mode”
Guardar cambios
Para verificar en Windows
En Administrador de tareas → CPU aparece “Virtualización: habilitada”
O usando msinfo32 o systeminfo

2. GNS3 VM: El Motor de Simulación

• KVM (Kernel-based Virtual Machine): Investigar qué es y por qué es obligatorio que aparezca como "True" en el servidor GNS3 para un rendimiento profesional.
Garantiza rendimiento óptimo:
Permite usar equipos virtuales reales
Evita errores y limitaciones
• Configuración de Recursos: Definir criterios para asignar CPU y RAM a la GNS3 VM sin desestabilizar Windows 11.
No usar todos los recursos
Asignación de CPU
Asignación de RAM
No sobrecargar la VM
Mantener equilibrio entre sistema y GNS3
Ajustar según el tamaño del laboratorio

3. Integración con VirtualBox (Local)

• Configuración de Red: Pasos para crear y configurar el adaptador Host-Only para la comunicación GUI-Server.
Crear el adaptador Host-Only:
Crear adaptador Host-Only
Asignar IP
Configurarlo en la VM
Activarlo en GNS3
Verificar conexión
• Modo Promiscuo: Explicar técnicamente por qué es necesario para el tráfico de Capa 2:
Permite tráfico de Capa 2 (Ethernet)
Hace posible la simulación realista de redes
Conecta correctamente la GUI con el servidor
4. Integración con VMware ESXi (Remoto):

• Arquitectura Cliente-Servidor: Cómo conectar el GUI de GNS3 de la laptop a un servidor ESXi físico.
Configurar ESXi para GNS3
Configurar GNS3 VM en ESXi
Configurar la GUI de GNS3 en tu laptop
Verificar conexión
• Seguridad en Switch: Investigar la configuración de "Políticas de Seguridad" (Promiscuous mode, MAC address changes) en el port group de ESXi.
Promiscuous Mode → ver todo el tráfico
MAC Address Changes → cambiar MAC de la VM
Forged Transmits → enviar paquetes con MAC distinta

5. Matriz de Solución de Errores (Troubleshooting)

Crear una tabla con al menos 3 errores comunes (ej: KVM not available, uBridge 
permissions, Firewall blocking port 3080) y su solución técnica. 











