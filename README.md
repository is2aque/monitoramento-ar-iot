# monitoramento-ar-iot
# Monitoramento de Qualidade do Ar IoT - ESP32

Este repositório contém a documentação e o código-fonte do projeto de monitoramento ambiental IoT.

## 1. Funcionamento e Uso
O sistema coleta dados de gases (MQ-135) e temperatura/umidade (DHT22), processa as informações localmente e transmite os dados via protocolo MQTT para a nuvem.
**Para reproduzir:**
1. Conecte os sensores e o buzzer ao ESP32 seguindo o esquema do projeto.
2. Configure as credenciais Wi-Fi e o Token da Ubidots no arquivo `projeto_final.ino.txt`.
3. Utilize a Arduino IDE para compilar e carregar o código.

## 2. Software e Documentação de Código
O software foi desenvolvido na **Arduino IDE (versão 2.x)** utilizando linguagem C++. O arquivo com o código-fonte está disponível neste repositório como `projeto_final.ino.txt`.

## 3. Descrição do Hardware
* **Plataforma:** Microcontrolador ESP32 (conectividade Wi-Fi/Bluetooth integrada).
* **Sensores:**
    * **MQ-135:** Detecção de gases poluentes (NH₃, CO₂, fumaça, álcool).
    * **DHT22:** Medição de temperatura e umidade relativa.
* **Atuador:** Buzzer Ativo 5V (alerta sonoro local para condições críticas).

## 4. Interfaces e Protocolos
* **Protocolo:** MQTT (Message Queuing Telemetry Transport).
* **Módulos de Comunicação:** Integração com a plataforma industrial **Ubidots** (Broker MQTT) para gerenciamento de mensagens e visualização em dashboards em tempo real.
