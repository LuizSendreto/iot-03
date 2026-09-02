# Arduino - Sensor de Movimento com LED

Discente: Luiz Felipe

Docente: Amanda Paul Dull

Esse repositório apresenta um projeto desenvolvido para a disciplina de IoT, utilizando uma placa Arduino UNO, um sensor de movimento PIR e um LED. O objetivo é demonstrar o funcionamento de um sensor como entrada para controlar um LED como saída.

##  Simulação no Tinkercad

[![Simular no Tinkercad](https://img.shields.io/badge/Simular%20no-Tinkercad-orange?style=for-the-badge&logo=autodesk)](https://www.tinkercad.com/things/ejosMMb5AMS/editel?returnTo=%2Fdashboard&sharecode=vkeBGJvBj57vnxSYEiPh2tgVvan2H5nlIgpDY4kX2EU)

##  Enunciado: Sensor de movimento com LED

O projeto consiste em utilizar um **sensor de movimento PIR** como dispositivo de entrada para controlar um **LED** conectado ao Arduino UNO.

Quando o sensor detecta movimento ou presença, ele envia um sinal de nível lógico **HIGH** para o Arduino. Ao receber esse sinal, o Arduino acende o LED durante 1 segundo.

Quando não há movimento detectado, o sensor envia um sinal **LOW** e o Arduino mantém o LED desligado.

O projeto demonstra como sensores podem ser utilizados para detectar eventos do ambiente e controlar dispositivos de saída.

###  Ligações utilizadas

- O sensor de movimento PIR está conectado ao **pino digital 7** do Arduino.
- O LED está conectado ao **pino digital 6**.
- O sensor PIR funciona como uma **entrada digital**.
- O LED funciona como uma **saída digital**.
- O circuito é alimentado pelo Arduino UNO.

##  Materiais necessários

| Qtd | Componente |
|-----|------------|
| 1 | Placa Arduino UNO |
| 1 | Cabo USB |
| 1 | Protoboard |
| 1 | Sensor de movimento PIR |
| 1 | LED |
| 1 | Resistor de 220 Ω |
| — | Fios de jumper macho-macho |

##  Funcionamento

O sensor PIR é responsável por detectar movimentação no ambiente. Quando uma movimentação é identificada, o sensor altera seu sinal de saída para **HIGH**.

O Arduino monitora continuamente esse sinal através do **pino digital 7**.

Quando o Arduino identifica que o sensor está em HIGH, ele envia um sinal HIGH para o **pino 6**, fazendo com que o LED acenda.

Depois disso, o programa aguarda **1 segundo** através do comando `delay(1000)`.

Caso o sensor não esteja detectando movimento, seu sinal permanece em LOW e o LED é desligado.

### Comportamento do circuito

| Estado do sensor | Pino 7 | Estado do LED | Pino 6 |
|------------------|--------|---------------|--------|
| Movimento detectado | HIGH | Ligado | HIGH |
| Sem movimento | LOW | Desligado | LOW |


