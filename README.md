monitoramento-ar-iot
Monitoramento de Qualidade do Ar IoT - ESP32
Este repositório contém a documentação e o código-fonte do projeto de monitoramento ambiental IoT, desenvolvido para medir níveis de gases e condições térmicas, com alerta sonoro local e transmissão de dados via protocolo MQTT.

1. Funcionamento e Uso
O sistema coleta dados de gases (MQ-135) e temperatura/umidade (DHT22), processa as informações localmente e transmite os dados via protocolo MQTT para um broker público na nuvem.

Para reproduzir:

Monte o circuito conectando os sensores e o buzzer ao ESP32 conforme o esquema do projeto (disponível no simulador Wokwi).

Configure as credenciais da sua rede Wi-Fi no arquivo projeto_final.ino.

O sistema utiliza o broker público broker.hivemq.com para o transporte das mensagens MQTT.

Utilize a Arduino IDE para compilar e carregar o código.

2. Software e Documentação de Código
O software foi desenvolvido na Arduino IDE (versão 2.x) utilizando linguagem C++. O arquivo com o código-fonte está disponível neste repositório como projeto_final.ino.

3. Descrição do Hardware
Plataforma: Microcontrolador ESP32 (conectividade Wi-Fi/Bluetooth integrada).

Sensores:

MQ-135: Detecção de gases poluentes (NH₃, CO₂, fumaça, álcool).

DHT22: Medição de temperatura e umidade relativa.

Atuador: Buzzer Ativo 5V (alerta sonoro local para condições críticas).

4. Interfaces e Protocolos
Protocolo: MQTT (Message Queuing Telemetry Transport).

Broker: Integração com o broker público HiveMQ (broker.hivemq.com) para transporte de mensagens em tempo real. O monitoramento pode ser validado através de qualquer cliente MQTT (como o HiveMQ Web Client) utilizando os tópicos definidos no código.
