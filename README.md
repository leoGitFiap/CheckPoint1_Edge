Para criar um sistema de controle de porcentagem de iluminação utilizando Arduino, você precisará de alguns componentes básicos e uma programação simples para ajustar a intensidade de luz de acordo com a porcentagem desejada. Abaixo estão os passos detalhados para criar este sistema.

Componentes necessários:

1 Arduino (UNO, Nano, etc.)

1 LED ou uma lâmpada (com dimmer)

1 potenciômetro (ou um controle de entrada, como um botão, sensor ou até interface digital)

1 resistor de 220 ohms (caso use um LED)

Fios de conexão

Protoboard (opcional)

Conceito básico:

O sistema vai utilizar o controle por PWM (Pulse Width Modulation) do Arduino, que permite variar a intensidade de um sinal de forma analógica através de um sinal digital. Isso é útil para controlar a intensidade de um LED ou lâmpada com base em um valor de porcentagem.

Passo a passo:

Montagem do circuito:
Conecte o terminal positivo do LED ao pino PWM do Arduino (por exemplo, pino 9).

Conecte o terminal negativo do LED a um resistor de 220 ohms e o outro lado do resistor ao GND do Arduino.

Conecte o potenciômetro entre 5V e GND do Arduino, e o pino central do potenciômetro em uma das entradas analógicas do Arduino (por exemplo, A0).

Programação:
O código abaixo lê o valor do potenciômetro e converte em uma porcentagem para ajustar a intensidade do LED. O Arduino tem saídas PWM em vários pinos (3, 5, 6, 9, 10, 11), permitindo controlar a intensidade de saída de 0 a 255, onde 0 é totalmente desligado e 255 é brilho máximo.

Explicação do código:

analogRead(pinoPot);: Lê o valor do potenciômetro, que varia de 0 a 1023.

map(valorPot, 0, 1023, 0, 255);: Converte o valor lido (de 0 a 1023) em um valor apropriado para o PWM (de 0 a 255), o que ajusta a intensidade do LED.

analogWrite(pinoLed, brilho);: Aplica o valor de PWM no LED, controlando sua luminosidade.

Monitor Serial (opcional): Serve para exibir a porcentagem da iluminação no monitor serial, ajudando a verificar o valor.

Ajuste por porcentagem:

Caso deseje controlar diretamente por porcentagem ao invés de usar o potenciômetro, você pode adicionar uma interface de entrada (como botões ou uma comunicação via interface serial). O valor de PWM seria ajustado em função da porcentagem desejada.

Conclusão:

Esse sistema simples de controle de iluminação por porcentagem com Arduino é versátil e pode ser aplicado em diversos projetos, como automação residencial, iluminação ajustável, ou até em displays visuais interativos. O uso de PWM torna o controle de brilho eficiente e direto.

https://www.tinkercad.com/things/38jSfaiDiwa-cp1-sensorluminosidade
https://youtu.be/IaTyqm_42HI
