# 🃏 Juego de Cartas Multijugador en Red

Un juego de cartas implementado en C++ con arquitectura cliente-servidor para partidas en red local.

## 🚀 Características

- **Modo servidor**: Gestiona la lógica del juego y conexiones
- **Múltiples clientes**: 2-4 jugadores en diferentes dispositivos
- **Sistema de turnos**: Con validación de jugadas
- **Interfaz de texto**: Colorida y fácil de usar
- **Registro de partidas**: Historial de resultados

![image](https://github.com/user-attachments/assets/f01ec017-b67a-4b11-8134-f595294b6131)
![image](https://github.com/user-attachments/assets/b1cdaae5-1436-46f9-97d5-3ecda28ca4bd)

## 🛠 Requisitos

- Dev-C++ 6.3 o superior
- Compilador compatible con C++11
- Bibliotecas de red de Windows (Winsock2)

## 🔧 Compilación

### Servidor
```bash
g++ servidor/*.cpp comun/*.cpp -o servidor.exe -lws2_32 -static-libstdc++

Cliente
bash
g++ cliente/*.cpp comun/Carta.cpp -o cliente.exe -lws2_32 -static-libstdc++
🎮 Cómo jugar
Iniciar servidor:

bash
./servidor.exe [puerto]
Conectar clientes:

bash
./cliente.exe [IP_servidor] [puerto]
Comandos disponibles:

REGISTRAR [nombre] - Unirse a la partida

TIRAR_CARTA [índice] - Jugar una carta

CHAT [mensaje] - Enviar mensaje

SALIR - Abandonar partida

📌 Protocolo de Comunicación
El servidor y clientes se comunican mediante mensajes de texto con formatos específicos:

JUEGO_INICIADO
CARTA_TIRADA [jugador] [color] [número]
JUGADOR_REGISTRADO [nombre]
