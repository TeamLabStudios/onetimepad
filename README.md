# One-Time Pad en VB.NET

Este proyecto implementa el cifrado y descifrado utilizando el algoritmo **One-Time Pad (OTP)** en **VB.NET**. El OTP es uno de los métodos de cifrado más seguros cuando se cumplen las condiciones de clave aleatoria, longitud igual al mensaje, y uso único de la clave.

## Características

- Cifrado y descifrado seguro usando XOR bit a bit.
- Generación de claves completamente aleatorias.
- Código simple y fácil de integrar en aplicaciones VB.NET.

## Requisitos

- **Visual Studio** 2019 o superior.
- .NET Framework 4.7.2 o superior (puedes ajustarlo según tu necesidad).

## Uso

1. Clona este repositorio:
    ```bash
    git clone https://github.com/TeamLabStudios/onetimepad.git
    ```

2. Abre el proyecto en Visual Studio.

3. Usa la clase `OneTimePad` para cifrar y descifrar mensajes en tu aplicación:

### Ejemplo de Código

```vb
' Importar la clase OneTimePad
Dim mensaje As String = "Hola Mundo"
Dim clave As String = OneTimePad.GenerateKey(mensaje.Length)

Console.WriteLine("Mensaje Original: " & mensaje)
Console.WriteLine("Clave Generada: " & clave)

' Cifrar el mensaje
Dim mensajeCifrado As String = OneTimePad.EncryptDecrypt(mensaje, clave)
Console.WriteLine("Mensaje Cifrado: " & mensajeCifrado)

' Descifrar el mensaje
Dim mensajeDescifrado As String = OneTimePad.EncryptDecrypt(mensajeCifrado, clave)
Console.WriteLine("Mensaje Descifrado: " & mensajeDescifrado)
```

### Salida esperada:
```
Mensaje Original: Hola Mundo
Clave Generada: wQp3$8z0n
Mensaje Cifrado: ▒▒#Té▒
Mensaje Descifrado: Hola Mundo
```

## Funcionalidades Principales

1. **EncryptDecrypt(input As String, key As String)**  
   Cifra o descifra un mensaje aplicando XOR entre cada carácter del texto y la clave.

2. **GenerateKey(length As Integer)**  
   Genera una clave completamente aleatoria de la misma longitud que el mensaje.

## Limitaciones

- La longitud de la clave debe ser igual a la del mensaje.
- La seguridad depende de mantener la clave completamente aleatoria y utilizarla solo una vez.

## Contribuciones

¡Contribuciones son bienvenidas! Si deseas agregar nuevas funcionalidades o mejorar el código, realiza un fork del repositorio y crea un pull request.

## Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

## Autor

- **LAB TEAM STUDIOS**  
  [GitHub](https://github.com/TeamLabStudios) | [Linktr](https://linktr.ee/labteamstudios)

---
¡Gracias por usar este proyecto! 😊

