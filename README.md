# 🌡️ Monitoramento de Temperatura IoT com Cálculo Metrológico

Sistema IoT simples e robusto para monitoramento de temperatura em tempo real com *ESP32*, *DS18B20* e *Supabase*, incluindo cálculo automático de **Incerteza Combinada** para validação metrológica (**Inmetro/GUM**).

---

## 🚀 Funcionalidades
- 🔄 **Tempo Real:** Recebe e exibe leituras de temperatura automaticamente via Supabase.
- 📐 **Incerteza Sem Zero:** Calcula a Incerteza Combinada ($u_c$), garantindo que o valor nunca seja zero ao incluir a resolução do sensor ($12\text{ bits} = 0,0625^\circ\text{C}$).
- 📈 **Gráfico e Estatísticas:** Histórico visual, registro de máximas/mínimas e horários das leituras.
- ⚠️ **Alerta Off-line:** Notifica se o ESP32 ficar mais de 5 minutos sem enviar dados.
- 🔒 **Limpeza Segura:** Função para resetar o banco de dados protegida por senha.

---

## 📐 Fórmula da Incerteza
O cálculo combina a variação estatística com a limitação física do sensor:

$$u_c = \sqrt{u_a^2 + u_b^2}$$

- **Tipo A ($u_a$):** Desvio padrão da média das amostras ($s / \sqrt{N}$).
- **Tipo B ($u_b$):** Resolução do sensor ($a / \sqrt{3} \approx 0,018^\circ\text{C}$).

---

## 🛠️ Tecnologias
- **Hardware:** ESP32 + Sensor DS18B20 (GPIO 23)
- **Backend:** Supabase (Database & Realtime)
- **Frontend:** HTML5, CSS3, JavaScript e Chart.js

---

## 👨‍💻 Autor
**Raphael Furtado da Silva** Bolsista **CNPq** | Projeto focado em diretrizes do **Inmetro** (2026)# termo-monitor
