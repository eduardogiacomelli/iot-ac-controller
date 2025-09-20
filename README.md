# SmartAC - IoT Air Conditioner Controller

[![Status do Projeto](https://img.shields.io/badge/status-em%20desenvolvimento-yellowgreen)](https://shields.io) 



## 📖 Sobre o Projeto

Este é um projeto de Internet das Coisas (IoT) desenvolvido para transformar um ar condicionado convencional da marca LG em um dispositivo inteligente. Utilizando um microcontrolador ESP8266, sensores de ambiente e uma plataforma de nuvem, este projeto permite o controle remoto completo do ar condicionado, além de coletar e analisar dados de temperatura e umidade para otimizar o conforto e a eficiência energética.


---

## ✨ Funcionalidades

* **Controle Remoto Total:** Ligar/Desligar, ajustar a temperatura e definir timers de qualquer lugar do mundo através de uma interface web e mobile.
* **Monitoramento em Tempo Real:** Coleta e visualização de dados de temperatura e umidade do ambiente em gráficos históricos.
* **Análise de Dados Inteligente:** Cálculo de "sensação térmica" (índice de calor) e exportação de dados para análise de padrões de uso e condições climáticas.
* **Automações:** Regras inteligentes baseadas em condições do ambiente (ex: ligar o AC automaticamente se a temperatura ultrapassar 25°C).
* **Notificações:** Alertas via push no celular para eventos importantes (ex: temperatura crítica).

---

## 🛠️ Stack Tecnológica e Componentes

### Hardware
* **Microcontrolador:** NodeMCU V3 (ESP8266)
* **Sensor de Ambiente:** DHT11 (Temperatura e Umidade)
* **Atuador:** LED Infravermelho (IR) Emissor
* **Driver do Atuador:** Transistor NPN (S8050 / 2N2222)
* **Receptor (para captura de códigos):** Receptor de IR (VS1838B)
* **Protoboard e Jumpers**

### Software & Nuvem
* **Firmware:** C++ no framework Arduino
* **IDE:** Arduino IDE
* **Plataforma de Prototipagem:** Blynk IoT (Plano Free)
* **Bibliotecas Principais:**
    * `BlynkSimpleEsp8266.h`
    * `DHT.h`
    * `IRremoteESP8266.h`

---

## 🚀 Como Começar

Para replicar este projeto, siga os passos abaixo.

### Pré-requisitos
1.  Tenha a [Arduino IDE](https://www.arduino.cc/en/software) instalada.
2.  Configure o suporte para placas ESP8266 na IDE.
3.  Instale as bibliotecas mencionadas acima através do Gerenciador de Bibliotecas.
4.  Crie uma conta gratuita no [Blynk IoT](https://blynk.cloud/).

### Montagem do Hardware
O esquemático completo do circuito estará disponível neste repositório em breve. As conexões principais envolvem ligar o sensor DHT11 e o circuito do LED emissor de IR ao NodeMCU.
<img width="1096" height="462" alt="image" src="https://github.com/user-attachments/assets/f3062d83-f97d-4186-9e92-e4498faa537a" />

### Configuração do Software
1.  Clone este repositório
2.  Configure seu Template e Device no Blynk IoT para obter as chaves de autenticação.
3.  Insira suas chaves do Blynk e suas credenciais de Wi-Fi no arquivo de código principal.
4.  Carregue o firmware no seu NodeMCU.

---

## 📈 Roadmap Futuro

-   [ ] **Fase 1:** Protótipo funcional com Blynk (Concluído)
-   [ ] **Fase 2:** Migração do firmware para comunicação via MQTT.
-   [ ] **Fase 3:** Desenvolvimento do backend customizado com Python, FastAPI e Docker.
-   [ ] **Fase 4:** Criação de um banco de dados (PostgreSQL/TimescaleDB) para armazenamento de séries temporais.
-   [ ] **Fase 5:** Desenvolvimento de um aplicativo web/mobile customizado.
