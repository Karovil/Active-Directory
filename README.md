**Pass-the-Ticket (PTT):** Uso de tickets Kerberos comprometidos para acceder a recursos.

El ataque de Pass the Ticket se basa en Kerberos y permite a un atacante usar un ticket
Kerberos obtenido, como si fuera un usuario legítimo, para acceder a los recursos y
servicios en la red. En el caso de DCsync, si un atacante tiene acceso a tickets TGT
(Ticket Granting Ticket) de un usuario o de una cuenta privilegiada, puede usar estos
tickets para obtener acceso a otros servicios sin necesidad de credenciales adicionales.

Mediante Rubeus podemos realizar el ataque Pass the Ticket utilizando el siguiente comando:
.\Rubeus.exe asktgt /user:Administrador/aes256:adbc3ed526ed66b5633a9eec27b4cccbc4d6a1903aedfd6923437af3da26a87b/domain:cs.org /dc:172.16.1.51 /ptt

![alt text](https://github.com/Karovil/Active-Directory/blob/Andr%C3%A9s-Arbel%C3%A1ez/ptt1.png)

Una vez obtenido el ticket, podemos verificar su validez con klist, que muestra los
tickets activos de Kerberos en la memoria de la máquina:

![alt text](https://github.com/Karovil/Active-Directory/blob/Andr%C3%A9s-Arbel%C3%A1ez/ptt2.png)

Finalmente, con el ticket de Kerberos, podemos realizar una prueba de acceso a
recursos compartidos en la red. Usamos el siguiente comando para listar los contenidos
de la carpeta administrativa en un servidor remoto

ls \\SERVER.cs.org\C$

![alt text](https://github.com/Karovil/Active-Directory/blob/Andr%C3%A9s-Arbel%C3%A1ez/ptt3.png)

Este comando nos permite acceder al recurso compartido C$ en el servidor
SERVER.cs.org, utilizando el ticket Kerberos sin necesidad de autenticarnos con la
contraseña del usuario Administrador
