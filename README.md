#  AURORA-1 — Sistema de Monitoramento Energético Espacial

Projeto desenvolvido para o **Global Solution 2026** da FIAP — Ciência da Computação.  
O tema é **Soluções em Energias Renováveis e Sustentáveis**, aplicado ao contexto de missões espaciais experimentais.

---

##  Descrição do Projeto

O **AURORA-1** é um sistema de monitoramento energético para uma missão espacial simulada. Ele recebe, interpreta e exibe dados simulados dos módulos operacionais da nave, gerando alertas automáticos e tomando decisões básicas diante de situações críticas.

A solução foi desenvolvida em **HTML, CSS e JavaScript puro**, sem necessidade de instalação de frameworks ou bibliotecas externas (exceto Chart.js, carregado via CDN).

---

##  Requisitos Técnicos Atendidos

| Requisito | Como foi implementado |
|---|---|
| Monitoramento de dados simulados | Dados atualizados a cada 2 segundos com variações aleatórias realistas |
| Geração de alertas | Log de telemetria com alertas automáticos por tipo (crítico, atenção, info, ok) |
| Tomada de decisão básica | 6 regras lógicas `if/else` que ativam respostas automáticas quando limites são ultrapassados |
| Visualização dos dados | Dashboard com cards, barras de progresso, gráficos de linha e badges de status |

---

##  Módulos Monitorados

-  **Painel Solar** — eficiência e geração de energia (kW)
-  **Sistema Térmico** — temperatura interna e rejeição de calor
-  **Comunicação** — sinal RF e uptime
-  **Bateria / Armazenamento** — carga e saúde da bateria
-  **Propulsão** — nível de combustível e empuxo
-  **Suporte de Vida** — nível de O₂ e pressão da cabine

---

##  Tomada de Decisão Automática

O sistema monitora continuamente as condições e aciona respostas automáticas:

```
se solar < 30%       → Ativar bateria de reserva
se temp_interna > 60°C → Acionar resfriamento emergencial
se sinal < 40%       → Redirecionar antena auxiliar
se bateria < 20%     → Ativar modo economia de energia
se O₂ < 50%          → Ligar gerador de O₂ backup
se pressão < 85 kPa  → Selar compartimento afetado
```

---

##  Como Executar

Não precisa instalar nada. Basta abrir o arquivo no navegador:

1. Faça o download ou clone este repositório
2. Abra o arquivo `aurora1_monitor.html` em qualquer navegador moderno (Chrome, Firefox, Edge)
3. O sistema já começa a simular automaticamente

```bash
# Opcional: rodar com servidor local (para evitar restrições de CORS)
npx serve .
# ou
python -m http.server 5500
```

---

##  Controles do Dashboard

| Botão | O que faz |
|---|---|
| ▶ Pausar simulação | Para ou retoma a atualização dos dados |
| ⚡ Falha no painel solar | Simula queda de eficiência do painel solar |
| 🌡️ Sobreaquecimento | Simula aumento crítico de temperatura interna |
| 📡 Perda de sinal | Simula degradação do sinal de comunicação RF |
| 🔋 Dreno de bateria | Simula consumo acelerado da bateria |
| ↺ Resetar tudo | Volta todos os módulos ao estado inicial |

---

##  Estrutura do Projeto

```
aurora1_monitor.html   ← arquivo principal (toda a solução em um único arquivo)
README.md              ← este arquivo
```

---

##  Tecnologias Utilizadas

- **HTML5** — estrutura da página
- **CSS3** — estilização e animações
- **JavaScript (ES6+)** — lógica de simulação, alertas e tomada de decisão
- **Chart.js** — gráficos de linha (carregado via CDN)
- **Google Fonts** — fontes Inter e JetBrains Mono

---

##  Integrantes do Grupo

| Nome | RM |
|---|---|
| Brenno Ferreira Gomes dos Santos | RM 570525 |
| Eduardo Moreira Silva | RM 569923 |

---
