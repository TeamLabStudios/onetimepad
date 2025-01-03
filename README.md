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
