# Sensor FX-S50

Sensor digital de oponentes compacto e rápido, ideal para detectar oponentes em competições de mini ou micro sumô. Além de uma saída digital simples para detecção imediata, ele possui um pino para configuração e leitura que permite a conexão com até 32 sensores usando apenas um único fio, facilitando a integração e o controle em robôs que utilizam muitos sensores.

Além disso, o sensor possui um modo "Shell", que possibilita conectá-lo a um computador através de um conversor USB-Serial. Esse modo permite a leitura de dados e a configuração detalhada dos parâmetros diretamente pelo terminal.

![Alt text](foto_frente.png)

**Video demonstrativo:** ...  

## Características Técnicas

| Característica         | Valor                 |
|------------------------|-----------------------|
| Tipo de sensor         | Obstaculos digital     |
| Faixa de medição       | 5 a 45cm (*)  |
| Tensão de operação     | 3,3 a 5V      |
| Corrente de operação   | 12 a 16mA     |
| Interface de comunicação | saida digital e Pino Fox Wire |
| Dimensões                | 11,4 x 12,4 x 16,2 mm    |
| Peso        | 4,9 g  |

(*) Em testes chegou a alcançar até 70cm na configuração mais sensivel.  

![Alt text](vistas_resumo_borda.png)

![Alt text](vistas_resumo_cor.png)

![Alt text](foto_vistas.png)

### Modelo 3D

[Modelo 3D STEP](./SensorMini_3dmodel.step)

## Comparação com outros sensores

![Alt text](comparando.png)

## Pinagem

- Pino GND
- Pino Vcc (Alimentação de 3,3V a 5V)
- Pino S de saida digital ( HIGH detectado, LOW não detectado )
- Pino Fox Wire (Configuração e leitura)

![Pinagem](diagrama_funcional.png)

## Configuração do sensor

Este sensor é configuravel, a tabela abaixo apresenta os principais parâmetros.

| Parametros          | Descrição                 |
|---------------------|-----------------------|
| Endereço Fox Wire   | Endereço do dispositivo para o protocoolo Fox Wire     |
| Potência do Emissor | Potência do emissor, quanto maior maior o alcance. Varia de 10 a 100 |
| Frequência do Emissor | Frequência do emissor, pode ser util para ajustar o alcance ou melhorar o desempenho de sensores proximos (*). valor normalizado de 0 a 255  |
| Trig e Filter_len | Ajuste de filtragem do sinal usando um integrador e um "schmitt trigger". Quanto maior a filtragem mais limpo o sinal, porém menor a frequencia de atualização. O usuario pode fazer o ajuste fino para determinar a melhor configuração |

(*) Na deteção a longa distância a luz emitida por dois sensore um ao lado do outro a luz emitida por cada um pode causar interferencia destrutiva, reduzindo o alcalce de cada um. Usar frequências um pouco diferentes pode ajudar nisso.

### Como configurar usando o modo Shell

O modo Shell é usado para se comunicar diretamente com o sensor usando comandos de texto. Esse modo só permite a comunicação com um unico sensor por vez (Para configurar varios sensores simultaneamente use Fox Wire).

- Conecte o sensor ao computador usando um conversor USB-Serial ou um arduino ([Conexão usando Fox Wire com Conversor USB Serial](#FxSerial)).
- Abra algum aplicativo de comunicação Serial, como Putty ou o proprio Serial Monitor do Arduino. Configure com baudrate de 115200. No Serial Monitor pode escolher qualquer placa desde que seja a COM correta, por simplicidade selecionei um Arduino.  
![Alt text](shell_serial_monitor_1.png)
<br>  

- Digite "FOX-SHELL" para o sensor entrar no modo Shell. O sensor irá responder enviando "FOX-SHELL INIT!".  
![Alt text](shell_serial_monitor_2.png)
<br>  

- Com o modo Shell iniciado você pode configurar o sensor ou realizar medições. Digite o comando "help" para exibir a lista de comandos disponiveis.
![Alt text](shell_serial_monitor_3.png)
<br>  

- O comando "dump" exibe os valores de configuração do sensor.
![Alt text](shell_serial_monitor_4.png)
<br>  

- <span style="color: red;">**Ao final envie o comando "save" para salvar as configurações, caso contrario, ao desligar as alterações são perdidas!**</span>

## Diagrama Esquematimo

### Conexão usando Saida digital Simples

![conexão_dogital](sch_digital.png)

### Conexão usando Fox Wire

![Alt text](sch_fox_wire.png)

<h3 id="FxSerial">Conexão usando Fox Wire com Conversor USB Serial</h3>

![Alt text](sch_shell.png)

## Exemplo de código usando a saida digital simples

```c++

// Codigo simples usando a saida digital

#define SENSOR_PIN 8

void setup(){
    Serial.begin(115200);
    pinMode(SENSOR_PIN,INPUT);
}

void loop() {
    Serial.print( "Leitura do sensor: " );
    Serial.println( digitalRead(SENSOR_PIN) );
    delay(300);
}
```

---

<p align="center">
  <img src="LogoFox.png" alt="Logo da Empresa" width="200px">
</p>

<!--- [Alt text](LogoFox.png) -->