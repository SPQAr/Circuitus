# Relatório Técnico e Funcional do Circuito de captura de amostras

## **Introdução**
Este relatório apresenta a análise técnica e funcional de um circuito que faz parte de um projeto de Internet das Coisas (IoT) para monitoramento da qualidade do ar. O objetivo central é registrar dados de concentração de poluentes atmosféricos em uma área específica e transmitir essas informações para uma API, onde serão processados e exibidos em tempo real em uma plataforma web.

---

## **Descrição Geral do Circuito**
O circuito foi desenvolvido no **Tinkercad**, contendo os seguintes componentes principais:

1. **Resistores (R1 a R11)**  
   - Controlam o fluxo de corrente elétrica no circuito, protegendo componentes como LEDs e sensores contra danos por sobrecarga.
   - Resistências variam de 220 ohms (para LEDs) a 4.7k ohms (para ajustes em outros componentes).

2. **LEDs (D1 a D5)**  
   - Representam indicadores visuais da qualidade do ar:
     - **Vermelho (D4, D5)**: Alta concentração de poluentes.
     - **Verde (D3)**: Qualidade do ar dentro de níveis aceitáveis.
     - **Amarelo (D1, D2)**: Níveis moderados de poluição.

3. **Potenciômetro (P1)**  
   - Permite ajustes de precisão no circuito, como controle do brilho dos LEDs ou calibração do sensor de gás.

4. **Sensor de Gás (GAS1)**  
   - Detecta concentrações específicas de gases poluentes no ambiente, enviando sinais analógicos para processamento.
   - Atua como a principal entrada de dados para o sistema.

5. **Circuito Integrado (U1)**  
   - Gerencia a lógica do circuito, processando os sinais do sensor e ativando os LEDs correspondentes.
   - Facilita o envio de dados capturados para o sistema externo.

6. **Fonte de Alimentação (VCC e GND)**  
   - Fornece energia ao circuito. O polo positivo (VCC) distribui energia aos componentes, e o polo negativo (GND) completa o ciclo elétrico.

---

## **Funcionamento Técnico**
### **1. Captura de Dados**
- O sensor de gás (GAS1) detecta a concentração de gases no ar.  
- Ele converte a quantidade de gás em sinais elétricos, enviando-os para o circuito integrado (U1).  

### **2. Processamento de Sinais**
- O U1 interpreta os sinais recebidos e ativa os LEDs correspondentes para indicar o nível de poluição:
  - **Alta poluição**: LEDs vermelhos (D4, D5).  
  - **Poluição moderada**: LEDs amarelos (D1, D2).  
  - **Boa qualidade do ar**: LED verde (D3).

### **3. Ajustes e Calibração**
- O potenciômetro (P1) ajusta a sensibilidade do circuito, permitindo calibrar o sensor para diferentes níveis de poluição.  
- Isso é essencial para manter precisão em áreas com condições ambientais diversas.

---

## **Aplicações no Contexto do Projeto**
O circuito descrito desempenha um papel crucial no monitoramento da qualidade do ar:
- **Coleta de Dados Ambientais**: Detecta e registra informações críticas sobre poluentes atmosféricos em locais específicos da cidade de São Paulo.
- **Feedback em Tempo Real**: Indica visualmente as condições do ar por meio dos LEDs, permitindo rápida identificação de mudanças no ambiente.
- **Integração IoT**: Dados capturados são transferidos para uma API, onde podem ser analisados e disponibilizados ao público por meio de uma interface web.

---

## **Integração no Sistema IoT**
### **Fluxo de Trabalho**
1. **Coleta Local de Dados**
   - O sensor GAS1 detecta a concentração de gases.  
   - LEDs fornecem feedback visual imediato.  

2. **Processamento Externo**
   - O circuito envia os dados capturados para uma API externa via módulo adicional (não presente no circuito atual).  

3. **Exibição em Tempo Real**
   - A API processa e envia os dados para um site, exibindo informações sobre a qualidade do ar em tempo real.

---

## **Conclusão**
O circuito projetado é uma solução eficiente para capturar e indicar a qualidade do ar em tempo real. Sua simplicidade facilita a expansão e integração com sistemas mais complexos, como plataformas IoT. Além disso, o uso de indicadores visuais (LEDs) e um sensor de gás robusto permite obter resultados claros e imediatos, essenciais para projetos relacionados à saúde pública e sustentabilidade.
