CyberMoodSec by ViajaTech ¡Encripta tus Archivos con Tus Emociones Faciales!
-------
![](https://github.com/viajatech/CyberMoodSec/blob/main/CyberMoodSec%20GUI%20%20.png)
-------
![](https://github.com/viajatech/CyberMoodSec/blob/main/CyberMoodSec%20Main.png)
-------
A continuación se detallan sus principales características y funcionalidades:

Interfaz de Usuario (GUI) con Tkinter:

Pantalla Principal: Ofrece opciones para Iniciar Sesión, Registrarse y Ver Logs.
Ventanas Secundarias: Para registro de usuarios, inicio de sesión, gestión de notas, encriptación/desencriptación de carpetas y visualización de logs.
Registro y Autenticación Facial:

Registro de Usuario: Captura y almacena la codificación facial del usuario mediante la cámara web. Se asegura de que la captura sea consistente y no "neutral" para mayor seguridad.
Inicio de Sesión: Verifica la identidad del usuario comparando la captura facial actual con la almacenada durante el registro.

Detección de Emociones con DeepFace:

Captura de Emoción: Antes de realizar acciones sensibles (como encriptar/desencriptar o guardar notas), la aplicación captura la emoción facial del usuario.
Consistencia de Emoción: Requiere que la misma emoción se detecte de manera consistente durante varios segundos para proceder, evitando detecciones erróneas.

Encriptación y Desencriptación Basadas en Emociones:
Encriptación de Carpetas: Permite al usuario seleccionar una carpeta para encriptar. La clave de encriptación se deriva de la emoción facial capturada.
Desencriptación de Carpetas: Desencripta carpetas previamente encriptadas, verificando que la emoción facial actual coincida con la utilizada durante la encriptación.
Gestión de Notas: Los usuarios pueden guardar y cargar notas protegidas por emociones, asegurando que solo puedan ser accedidas con la emoción correcta.

Seguridad Avanzada:
Derivación de Claves: Utiliza PBKDF2HMAC para derivar claves AES-256 a partir de las emociones detectadas, garantizando una encriptación robusta.
Almacenamiento Seguro: Las emociones y codificaciones faciales se manejan de manera segura, sin almacenar directamente las claves.

Gestión de Logs:
Registro de Eventos: Registra todas las acciones y errores en un archivo de log (cybermoodsec.log) y también muestra los logs en una ventana dentro de la aplicación para facilitar la supervisión y depuración.
Dependencias y Requisitos:

Bibliotecas Utilizadas: Tkinter, OpenCV, DeepFace, NumPy, scikit-learn, Pillow, cryptography, SQLite3, entre otras.
Instalación de Dependencias: Se proporcionan comandos pip install para instalar todas las dependencias necesarias.
Flujo de Uso Principal:

Registro:
El usuario se registra proporcionando un nombre de usuario y capturando su rostro con una emoción específica.
La emoción capturada se utiliza para derivar una clave de encriptación única.
Inicio de Sesión:

El usuario inicia sesión ingresando su nombre de usuario y capturando su rostro con la misma emoción registrada.
Si la verificación es exitosa, se accede al dashboard principal.

Encriptar/Desencriptar Carpetas y Notas:
Para encriptar, el usuario selecciona una carpeta y captura una emoción consistente.
Para desencriptar, selecciona la carpeta encriptada y debe capturar la misma emoción utilizada previamente.
Similarmente, al guardar o cargar notas, se requiere la captura de la emoción correspondiente.

Gestión de Notas:
Las notas se encriptan y almacenan en una base de datos SQLite, protegidas por la emoción facial del usuario.

-------
