# FXDevices - Dispositivos para Robótica e Automação

Este repositório contém exemplos e documentação dos dispositivos da Fox Dynamics, projetados para robótica educacional, competições e automação. Cada seção apresenta detalhes técnicos, exemplos de código, esquemáticos e instruções para uso dos dispositivos. Este repositório serve como um ponto de referência para desenvolvedores, estudantes e entusiastas que trabalham com sistemas embarcados e eletrônicos voltados para automação e controle.
<!--Sensores, modulos e placas controladoras da Fox Dynamics.-->

<!--
## Índice

- [Dispositivo 1: Sensor Mini Sumo](#Dispositivo-1:-Sensor-Mini-Sumo)
- [Dispositivo 2: Módulo Start](#Dispositivo-2:-Módulo-Start)
- [Dispositivo 3: Sensor de Linha Mini Sumo](#Dispositivo-3:-Sensor-de-linha-mini-sumo)
- [Dispositivo 4: ESC 2 motores Brushed](#Dispositivo-4:-ESC-2-motores-Brushed)
---
-->

# Sensores

## Sensor FX-S50

[Saiba mais sobre](./Sensor_FXS50/README.md)

Sensor digital de obstáculos compacto, rápido e configurável. Possui uma saída digital para detecção imediata, e um pino para configuração ou leitura via protocolo FoxWire, permitindo a conexão  simultânea de até 32 sensores em paralelo (compartilhando o mesmo fio).

Além disso, o sensor possui um modo "Shell", que possibilita conectá-lo a um computador através de um conversor USB-Serial. Esse modo permite a leitura de dados e a configuração detalhada dos parâmetros.

![Alt text](Sensor_FXS50/imagens/frente.png)

**Video demonstrativo:** [https://www.youtube.com/watch?v=7ljwJTxrwXw](https://www.youtube.com/watch?v=7ljwJTxrwXw) 

**Datasheet:** [Datasheet_FXS50](Sensor_FXS50/Datashet_FX_S50.pdf) 

| Característica         | Valor                 |
|------------------------|-----------------------|
| Tipo de sensor         | Obstaculos digital ajustavel    |
| Faixa de medição       | 0 a 50cm (*)  |
| Tensão de operação     | 3,3 a 5V      |
| Corrente de operação   | 12 a 16mA     |
| Interface de comunicação | Saida digital e pino Fox Wire |
| Dimensões                | 11,4 x 12,4 x 16,2 mm    |
| Peso        | 4,9 g  |

(*) Medição na configuração padrão. Em testes, chegou a alcançar até 70cm na configuração mais sensivel. Os resultados podem variar em função da cor, inclinação e tamanho do objeto detectado. Ajuste a sensibilidade em função da aplicação.

---

## Sensor de Linha Mini

[Saiba mais sobre](./Sensor_linha/README.md)

Pequeno sensor de linha ideal para robôs de Sumô 3kg, Mini, micro ou nano ou em seguidores de linha, principalmente como sensor de marcação lateral.

![Alt text](Sensor_linha/imagens/sensor_linha.png)

| Característica         | Valor                 |
|------------------------|-----------------------|
| Tipo de sensor         | Sensor de linha analógico  |
| Tensão de operação     | 3,3 a 5V      |
| Dimensões                | 8 x 6,5 x 3,3 mm    |
| Peso        | 0,15 g  |

---

## Sensor digital TOF
Em breve...

## Módulo Start
Em breve...

# ESCs

em breve...

| ESCs     | Tipo |  Motores | Tensão | Corrente Maxima | sensor |
|---|---|---|---|---|---|
| FX-M1 LP | brushed | 1 | 2S | 1,5A | sim |
| FX-M1 HP | brushed | 1 | 2 a 4S | 3A | sim |
| FX-M2 LP | brushed | 2 | 2S | 1,5A | sim |
| FX-M2 HP | brushed | 1 | 2 a 4S | 3A | sim |
| FX-M1 UHP | brushed | 1 | 2 a 6S | 40A | sim |  
| FX-FOC Mini | Brushless | 1 | 1 a 3S | 3A | sim |  
  
# Placas Controladoras

em breve...

| Controladora | Microcontrolador | Tensão | USB | Radio |  Motores | Sensores | Aplicação |
|---|---|---|---|---|---|---|---|
| Fox Nano War  | - | 2S | Não | FlySky | 2 Brushed 1,5A | Medição de bateria e IMU (opcional) | Combate Fada ou Ant |
| Fox Nano  | Atmega328 | 2S | Não | Não possui | 2 Brushed 1,5A | Medição de bateria, 5 entradas, receptor IR (opcinal) e IMU (opcional) | Combate Fada ou Ant |
| Fox Nano W | ESP32-C3 | 2S | Não | WIFI, BLE ou ESPNOW | 2 Brushed 1,5A | Medição de bateria, 4 entradas, receptor IR (opcinal) e IMU (opcional) | Combate Fada ou Ant e Mini ou Micro Sumo |
| Fox Mini | Atmega328 | 2S a 4S | Sim | Não possui | 2 Brushed 3A | Medição de bateria, 8 entradas, receptor IR e IMU (opcional) | Combate Ant ou Beeatle e Mini Sumo e Seguidor |
| Fox Mini W | ESP32 | 2S a 4S | Sim | WIFI, BLE ou ESPNOW | 2 Brushed 3A | Medição de bateria, 10 entradas, receptor IR e IMU (opcional) | Combate Ant ou Beeatle e Mini Sumo e Seguidor |

# Outras placas

## Conversor Rádio ESPNOW

Conecte este módulo a saida "trainer" PPM de um radio para torna-lo compativel com transmissão ESPNOW.

em breve...

---   


<p align="center">
  <img src="LogoFox.png" alt="Logo da Empresa" width="200px">
</p>

<!--- [Alt text](LogoFox.png) -->