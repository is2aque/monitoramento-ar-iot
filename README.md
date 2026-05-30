Monitoramento de Qualidade do Ar IoT - ESP32
Este projeto apresenta um sistema de monitoramento ambiental inteligente, desenvolvido com ESP32, capaz de medir níveis de gases poluentes (MQ-135) e condições térmicas (DHT22), acionando alertas locais e enviando telemetria via protocolo MQTT.

1. Funcionamento e Uso
O sistema opera realizando a leitura cíclica dos sensores. Caso os níveis de gás ou temperatura excedam os limites de segurança configurados, o sistema aciona um alarme sonoro (Buzzer) e publica um alerta no broker MQTT.

Como reproduzir:

Montagem: Conecte o sensor MQ-135 (analógico), DHT22 (digital) e o Buzzer ao ESP32 seguindo o esquema de pinagem no Wokwi.

Configuração: Abra o código projeto_final.ino na Arduino IDE.

Conexão: Insira as credenciais da sua rede Wi-Fi local nas constantes ssid e password.

Execução: Compile e carregue o código no seu ESP32. O sistema iniciará a publicação automática de dados no broker público broker.hivemq.com no tópico mackenzie/projeto/gas.

2. Software e Documentação
Ambiente de Desenvolvimento: Arduino IDE (versão 2.x).

Linguagem: C++.

Bibliotecas Principais: * PubSubClient (para comunicação MQTT).

DHT sensor library (para leitura do sensor de temperatura/umidade).

Código-fonte: Disponível no arquivo projeto_final.ino neste repositório.

3. Descrição do Hardware
O projeto utiliza componentes de baixo custo e alta eficiência para o ecossistema IoT:

Microcontrolador: ESP32 (processador de 32 bits com Wi-Fi/Bluetooth integrado).

Sensor de Gás (MQ-135): Detector eletroquímico para NH₃, NOₓ, fumaça, álcool e CO₂.

Sensor de Temperatura e Umidade (DHT22): Sensor digital de alta precisão (AM2302).

Atuador: Buzzer Ativo 5V para alertas sonoros.

Prototipagem: O modelo de montagem e as conexões elétricas foram validados no ambiente Wokwi.

4. Interfaces, Protocolos e Comunicação
Protocolo de Transporte: MQTT (Message Queuing Telemetry Transport).

Broker: Utiliza o broker público HiveMQ (broker.hivemq.com) para o modelo de publish/subscribe.

Comunicação: Os dados são publicados em tópicos específicos (mackenzie/projeto/gas, mackenzie/projeto/alerta), garantindo latência mínima e interoperabilidade com outros dispositivos IoT.

Projeto desenvolvido como parte da disciplina de IoT - 2026.
