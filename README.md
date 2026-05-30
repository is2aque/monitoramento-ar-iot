Monitoramento de Qualidade do Ar IoT - ESP32
Este projeto apresenta o desenvolvimento de um sistema de monitoramento ambiental inteligente, projetado para medir a qualidade do ar e condições térmicas em tempo real, utilizando a plataforma ESP32 e o protocolo MQTT para comunicação IoT.

1. Funcionamento e Uso
O sistema realiza a leitura contínua de sensores ambientais. Caso os níveis de gás ou temperatura ultrapassem os limites de segurança configurados, o sistema aciona um alarme sonoro (Buzzer) local e publica um alerta de telemetria em um broker MQTT na nuvem.

Como reproduzir:

Montagem: Conecte o sensor MQ-135 (analógico), o sensor DHT22 (digital) e o Buzzer ao microcontrolador ESP32 seguindo o esquema de pinagem validado.

Configuração: Abra o arquivo projeto_final.ino na Arduino IDE.

Conexão: Insira as credenciais da sua rede Wi-Fi local nas constantes ssid e password do código.

Execução: Compile e carregue o código no ESP32. O sistema iniciará a publicação dos dados no broker público broker.hivemq.com através do tópico mackenzie/projeto/gas.

2. Software e Documentação de Código
Ambiente de Desenvolvimento: Arduino IDE (versão 2.x).

Linguagem: C++.

Bibliotecas utilizadas: * PubSubClient: Gerenciamento da conexão e comunicação MQTT.

DHT sensor library: Leitura e calibração dos dados do sensor DHT22.

Código-fonte: O arquivo projeto_final.ino contido neste repositório inclui toda a lógica de processamento e comunicação.

3. Descrição do Hardware
O protótipo foi projetado com componentes de baixo custo e alta eficiência para cenários de Cidades Inteligentes (Smart Cities):

Plataforma de Desenvolvimento: ESP32 (Microcontrolador com Wi-Fi/Bluetooth integrado e alta capacidade de processamento).

Sensores:

MQ-135: Sensor eletroquímico para detecção de gases poluentes (NH₃, CO₂, fumaça, álcool).

DHT22 (AM2302): Sensor digital de alta precisão para medição de temperatura e umidade relativa do ar.

Atuadores: * Buzzer Ativo 5V: Utilizado para fornecer resposta acústica imediata em casos de níveis críticos detectados.

Estrutura: A montagem foi validada virtualmente no simulador Wokwi, assegurando a precisão das conexões elétricas e a integridade do circuito.

4. Interfaces, Protocolos e Módulos de Comunicação
Protocolo de Transporte: MQTT (Message Queuing Telemetry Transport).

Broker: Utilização do broker público HiveMQ (broker.hivemq.com), que atua como o servidor central de mensagens seguindo o modelo publish/subscribe.

Comunicação: Os dados são publicados em tópicos específicos (mackenzie/projeto/gas, mackenzie/projeto/alerta), permitindo a visualização da telemetria e o monitoramento em tempo real por qualquer cliente MQTT configurado.

Projeto desenvolvido como parte da disciplina de IoT - 2026.
