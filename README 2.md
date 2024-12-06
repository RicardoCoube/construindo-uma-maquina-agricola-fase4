# **Integração do Serial Plotter**

Este projeto demonstra como o **Serial Plotter** no Wokwi responde às mudanças nas leituras dos sensores, mostrando o monitoramento em tempo real de variáveis como temperatura, umidade, luminosidade e distância.

---

## **1. Introdução**

Nesta seção, introduzimos o Serial Plotter como uma ferramenta essencial para a análise em tempo real no projeto **FarmTech Solutions**, desenvolvido na Fase 4. O Serial Plotter, integrado ao Arduino IDE, permite a visualização gráfica de variáveis monitoradas, como temperatura, umidade, luminosidade e distância.

Este recurso foi utilizado no contexto do Wokwi, uma plataforma de simulação de circuitos, para validar o comportamento dos sensores e a lógica de irrigação automatizada implementada no ESP32. Seu objetivo é facilitar a depuração e o acompanhamento visual das condições do sistema em tempo real, contribuindo para um processo de desenvolvimento mais eficiente.

---

## **2. Descrição do Circuito**

O circuito do projeto foi desenvolvido utilizando o **ESP32**, integrado a sensores e um display LCD. Ele simula um sistema automatizado de irrigação, monitorando variáveis ambientais em tempo real. Cada componente tem um papel específico no funcionamento do sistema:

- **DHT22 (Temperatura e Umidade):** Mede a temperatura e a umidade do ambiente, parâmetros essenciais para decidir quando ativar o sistema de irrigação.
- **LDR (Resistor Dependente de Luz):** Monitora a luminosidade do ambiente, fornecendo informações que podem influenciar a evaporação do solo.
- **Sensor Ultrassônico:** Mede a distância até objetos, garantindo a segurança do sistema ao evitar ativações indesejadas em áreas próximas.
- **Display LCD (I2C):** Mostra em tempo real as principais métricas, como temperatura, umidade e distância, para facilitar a validação do sistema diretamente no hardware.

Além disso, o código implementado no ESP32 envia os dados coletados ao Serial Plotter para análise gráfica e monitoramento. O uso da plataforma Wokwi possibilitou a simulação do circuito, permitindo testes antes da implementação física.

---

## **3. Demonstração com Capturas de Tela**

A demonstração foi realizada no Wokwi, utilizando o **Serial Plotter** para monitorar variáveis como temperatura, umidade, luminosidade e distância em tempo real. Durante os testes, diferentes condições foram simuladas, e as alterações nos sensores foram refletidas nos gráficos, permitindo uma análise visual imediata.

### **Tabela Resumo das Variáveis**

| **Captura** | **Temperatura (°C)** | **Umidade (%)** | **Luminosidade (%)** | **Distância (cm)** |
|-------------|-----------------------|------------------|-----------------------|--------------------|
| 1           | 10,1                 | 55,0             | 30                    | 87                 |
| 2           | 30,4                 | 68,5             | 50                    | 87                 |
| 3           | 41,2                 | 73,0             | 70                    | 197                |

---

### **Captura 1**
![Gráfico Captura 1](imagens/captura1.png) <!-- Substituir pelo link correto da imagem -->
- **Contexto:** A temperatura está baixa (10,1°C) e a umidade está moderada (55%).
- **Observação no Gráfico:** A linha da temperatura é quase constante, enquanto a da umidade apresenta pequenas oscilações devido à estabilização dos sensores.

---

### **Captura 2**
![Gráfico Captura 2](imagens/captura2.png) <!-- Substituir pelo link correto da imagem -->
- **Contexto:** Temperatura elevada (30,4°C) e aumento significativo na umidade (68,5%).
- **Observação no Gráfico:** As curvas de temperatura e umidade apresentam inclinação ascendente.

---

### **Captura 3**
![Gráfico Captura 3](imagens/captura3.png) <!-- Substituir pelo link correto da imagem -->
- **Contexto:** O sensor ultrassônico detecta um objeto a 197 cm, enquanto a temperatura e a umidade permanecem estáveis.
- **Observação no Gráfico:** A linha da distância mostra uma transição clara ao atingir o novo valor.

---

## **4. Observações**

- O **Serial Plotter** demonstrou capacidade de refletir alterações nos sensores em tempo real, facilitando a análise.
- Os valores normalizados no código garantiram gráficos consistentes e de fácil leitura.

### **Análises Relevantes**
1. **Temperatura e Umidade:** Alterações refletidas imediatamente no gráfico, permitindo avaliar a precisão e a estabilidade dos dados coletados.
2. **Luminosidade:** Alterações simuladas no sensor LDR apresentaram transições suaves no gráfico, indicando que o sistema é capaz de lidar com variações contínuas sem perda de precisão.
3. **Distância:** O sensor ultrassônico capturou mudanças de forma consistente, validando a lógica de segurança implementada no código.

### **Limitações Observadas**
- **Resolução do Serial Plotter:** Embora eficiente para análises visuais, pode apresentar limitações em projetos mais complexos com múltiplas variáveis.
- **Escalabilidade:** Ideal para protótipos, mas sistemas maiores podem exigir soluções mais robustas, como dashboards interativos.

---

## **5. Conclusão**

O uso do Serial Plotter no projeto **FarmTech Solutions**, desenvolvido na Fase 4, demonstrou ser uma ferramenta eficiente para o monitoramento e a depuração de variáveis em tempo real. Através das simulações realizadas no Wokwi, foi possível validar o comportamento do sistema de irrigação automatizado e otimizar sua lógica de operação.

**Pontos Principais:**
- Identificação de padrões e anomalias nos dados de sensores.
- Validação da lógica de operação do sistema.
- Geração de insights para ajustes e melhorias futuras.

**Perspectivas Futuras:**
Na continuidade do projeto, os dados monitorados pelo Serial Plotter podem ser integrados ao modelo preditivo desenvolvido com **Scikit-learn**, contribuindo para decisões de irrigação mais inteligentes. Além disso, a interface interativa planejada com o **Streamlit** complementará o Serial Plotter, oferecendo uma solução mais robusta e escalável para o monitoramento.

---