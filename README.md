# 🛣️ Monitoramento de Vegetação em Rodovias - Dashboard de Manutenção

> **Solução de apoio à tomada de decisão para concessionárias rodoviárias.**  
> Projeto desenvolvido como evolução da Sprint para análise automática e priorização de intervenções na vegetação ao longo da via.

---

## 📌 Sobre o Projeto

O grande volume de dados coletados ao longo dos trechos rodoviários torna inviável a análise manual de cada ponto monitorado. Esta aplicação automatiza esse processo: os dados referentes à altura da vegetação são processados por um motor de regras que os classifica dinamicamente e determina a prioridade de atendimento para as equipes de manutenção.

A interface apresenta um **Dashboard interativo** com indicadores estatísticos, código de cores por nível de criticidade e ações recomendadas automaticamente para cada trecho.

---

## ⚙️ Regras de Classificação e Negócio

Para garantir a segurança viária e a visibilidade das sinalizações, a aplicação utiliza as seguintes faixas de altura da vegetação:

| Nível de Condição | Faixa de Altura (cm) | Ação Recomendada | Cor Indicativa | Prioridade |
| :--- | :--- | :--- | :--- | :---: |
| **Monitorado** | Até 30 cm | Manter rotina regular de monitoramento. | Verde (`#2ecc71`) | 1 |
| **Atenção** | 31 cm a 60 cm | Programar vistoria visual na próxima quinzena. | Amarelo (`#f39c12`) | 2 |
| **Intervenção Programada** | 61 cm a 100 cm | Agendar roçada mecânica em até 7 dias úteis. | Laranja (`#d35400`) | 3 |
| **Intervenção Prioritária** | Acima de 100 cm | Enviar equipe de corte imediatamente (Risco iminente à visibilidade). | Vermelho (`#c0392b`) | 4 |

---

## 🛠️ Tecnologias Utilizadas

* **HTML5:** Estruturação semântica do Dashboard.
* **CSS3:** Estilização responsiva, layout em Grid e Flexbox, utilização de variáveis CSS e sinalização visual por cores.
* **JavaScript (ES6+):** 
  * Armazenamento e manipulação de arrays de objetos;
  * Lógica condicional para classificação de risco;
  * Métodos funcionais de array (`.map()`, `.filter()`, `.sort()`, `.forEach()`);
  * Renderização dinâmica do DOM.

---

## 🚀 Funcionalidades Implementadas

- [x] **Processamento Automático:** Classificação da condição da vegetação com base na altura monitorada.
- [x] **Ações Recomendadas Automáticas:** Indicação clara do procedimento correto para cada ponto.
- [x] **Painel de Indicadores (KPIs):** Resumo numérico dos pontos totais, críticos e programados.
- [x] **Filtros Dinâmicos:** Possibilidade de isolar apenas os pontos com criticidade mais alta.
- [x] **Ordenação Flexível:** Permite ordenar por maior prioridade, maior altura ou ordem dos quilômetros (Km).
- [x] **Destaque Visual:** Cartões com bordas e badges coloridas conforme a condição.

---

## 📂 Como Executar o Projeto

Como a aplicação foi desenvolvida em formato web nativo, **não é necessária a instalação de dependências ou servidores**.

1. Faça o download ou clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/monitor-vegetacao-rodovias.git
   ```
2. Navegue até a pasta do projeto e abra o arquivo `index.html` (ou `dashboard.html`) diretamente no seu navegador de preferência (Chrome, Edge, Firefox, etc.).

---

## 📹 Vídeo de Demonstração

O link com a apresentação e demonstração funcional do sistema encontra-se no arquivo `Link do video.txt` na raiz do projeto.