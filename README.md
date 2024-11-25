Ejemplo de Explotación en un Controlador de Dominio

Este repositorio documenta el proceso realizado en un entorno de pruebas enfocado en vulnerar un Controlador de Dominio previamente configurado con datos ficticios y rutas específicas. El objetivo era explorar y aplicar técnicas comunes de ataque en entornos Active Directory, siguiendo principios éticos y en un laboratorio controlado.

Descripción del Proyecto

En este ejercicio, llevamos a cabo una serie de ataques orientados a demostrar vulnerabilidades comunes en la configuración y administración de controladores de dominio. Las técnicas utilizadas incluyeron:

Password Spraying: Intentos masivos de autenticación con combinaciones comunes de contraseñas.

AS-REP Roasting: Extracción de hashes de contraseñas de cuentas con preautenticación deshabilitada en Kerberos.

Kerberoasting: Obtención de hashes de contraseñas vinculadas a cuentas de servicios de Kerberos.

DCSync: Simulación de un controlador de dominio para replicar datos sensibles como hashes de contraseñas.

Pass-the-Hash (PTH): Uso de hashes en lugar de contraseñas para autenticación.

Pass-the-Ticket (PTT): Uso de tickets Kerberos comprometidos para acceder a recursos.

Ataques Externos con Rubeus: Algunos participantes simularon ataques desde fuera del dominio utilizando herramientas como Rubeus, para la obtención y explotación de tickets Kerberos.

Estas técnicas se aplicaron únicamente en un entorno de pruebas, con fines educativos y de fortalecimiento de habilidades en ciberseguridad.


Requisitos del Entorno

Sistema Operativo: Kali Linux

Entorno de Pruebas: Controlador de Dominio preconfigurado con cuentas ficticias

Herramientas Principales:

Impacket

Mimikatz

Hashcat

Kerbrute

CrackMapExec

Rubeus

Propósito

Este proyecto busca proporcionar una referencia técnica para estudiantes y profesionales que deseen profundizar en ataques a controladores de dominio en un laboratorio controlado. No debe utilizarse en entornos productivos ni con fines malintencionados.

Nota de Ética
Todas las pruebas fueron realizadas en un entorno controlado con permisos explícitos. Se recomienda aplicar estas técnicas únicamente en laboratorios diseñados para este propósito y respetar siempre las leyes locales y los principios éticos de la ciberseguridad.
