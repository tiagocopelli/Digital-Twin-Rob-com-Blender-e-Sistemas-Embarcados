## Projeto Final - Residência Tecnológica em Desenvolvimento de Software Embarcado - EmbarcaTech

## 🤖 Robô com Digital Twin no Blender usando FreeRTOS

Este projeto consiste no desenvolvimento de um sistema embarcado para controle de um braço robótico, integrado a um Digital Twin no software Blender. O sistema utiliza FreeRTOS para gerenciamento de tarefas concorrentes e comunicação bidirecional em tempo real entre o robô físico e o ambiente virtual.


## 📖 Visão Geral

O robô pode ser controlado de múltiplas formas:
- Botões físicos (placa BitControl)
- Interface gráfica no Blender (Add-on)
- Controle gestual por giroscópio
- Comunicação via rede (UDP)
- Comunicação serial (UART)

Todas as formas de controle atuam de maneira sincronizada, alterando simultaneamente o robô físico e o robô virtual no Blender.


## ⚙️ Funcionalidades

- Controle de servomotores via PCA9685
- Execução concorrente com FreeRTOS
- Comunicação UDP bidirecional com Blender
- Digital Twin em tempo real
- Interface gráfica local com display ST7920
- Leitura de sensor de distância VL53L0X
- Controle gestual via MPU6050
- Interface física de botões via PCF8575
- Comunicação serial via UART


## 🧩 Arquitetura do Sistema

O sistema é baseado em múltiplas tarefas do FreeRTOS, cada uma responsável por uma funcionalidade específica, como:
- Comunicação de rede
- Controle dos servos
- Atualização do display
- Leitura de sensores
- Processamento de botões
- Comunicação UART

Os comandos são organizados por meio de filas e protegidos por mutexes, garantindo operação segura e determinística.


## 🛠️ Hardware Utilizado

- Placa BitDogLab
- Microcontrolador Raspberry Pi Pico W (RP2040)
- Driver de servos PCA9685
- Expansor de portas I2C PCF8575
- Display gráfico ST7920
- Sensor de distância VL53L0X
- Giroscópio MPU6050
- Servomotores

⚠️ Observação: O teclado matricial e a garra física não são utilizados neste projeto.


## 💻 Software Utilizado

- Raspberry Pi Pico SDK
- FreeRTOS
- Blender
- Python (Add-on do Blender)
- Protocolo UDP
- Arduino IDE / CMake (dependendo do build)

## 🎥 Demonstração
![Demonstração do projeto](Demonstracao.gif)
