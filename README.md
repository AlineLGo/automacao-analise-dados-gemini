# 📊 Automação de Análise de Dados Executiva com Gemini AI & Google Sheets

Este projeto apresenta uma solução completa de pipeline automatizado para a geração de relatórios executivos estratégicos a partir de dados brutos. Utilizando **Python**, **Pandas** e a **API do Google Gemini**, o sistema analisa métricas de negócios, identifica tendências e gera conclusões acionáveis para a tomada de decisão.

---

## 🔄 Duas Formas de Automação Implementadas

Para atender a diferentes necessidades do dia a dia corporativo, o projeto contempla **duas abordagens de integração**:

1. **📁 Abordagem 1: Processamento Local via Arquivo CSV (Google Colab)**
   - Ideal para análises rápidas com datasets estáticos ou arquivos locais.
   - Gera e processa arquivos `.csv` diretamente no ambiente do Colab, transformando tabelas brutas em relatórios formatados em Markdown (`.md`).

2. **☁️ Abordagem 2: Conexão Dinâmica com Google Sheets em Tempo Real**
   - Leitura automatizada de planilhas hospedadas na nuvem.
   - Sempre que novos dados são adicionados ou alterados na planilha do Google Sheets, o script lê as atualizações em tempo real e regera o relatório executivo sem a necessidade de reexportar arquivos manualmente.

---

## 🚀 Funcionalidades e Destaques Técnicos

- **Análise Qualitativa por IA:** Transformação de dados tabulares em relatórios executivos estruturados contendo *Resumo Geral*, *Destaques de Desempenho*, *Pontos de Atenção* e *Recomendações Práticas*.
- **Resiliência e Tolerância a Falhas:** Lógica de *fallback* automático entre múltiplos modelos da família Gemini (`gemini-3.8-flash`, `gemini-3.5-flash`, `gemini-3.7-flash,`, `gemini-3.5 - flash - lite,` ) para garantir a continuidade do serviço mesmo em momentos de alta demanda da API.
- **Segurança de Credenciais:** Proteção da chave de API utilizando a biblioteca `google.colab.userdata` (Secrets do Colab), garantindo que dados sensíveis não fiquem expostos no código público.
- **Exportação Persistente:** Gravação automática dos relatórios finais em arquivos `.md`, prontos para uso em documentações, Notion ou envio por e-mail.

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** Python 3
- **Manipulação de Dados:** `pandas`, `tabulate`
- **Inteligência Artificial:** SDK `google-genai` (Google Gemini API)
- **Integração em Nuvem:** Google Sheets (via exportação CSV dinâmica)
- **Ambiente de Execução:** Google Colab

---

## 📈 Como Executar o Projeto

1. **Clone ou abra o notebook no Google Colab.**
2. **Configuração da Chave de API:**
   - Obtenha sua chave gratuita no [Google AI Studio](https://aistudio.google.com/).
   - No menu lateral do Colab, acesse **Segredos** (🔑) e crie o segredo `GEMINI_API_KEY` com a sua chave. Ative a permissão *"Acesso ao notebook"*.
3. **Escolha o Fluxo de Execução:**
   - **Fluxo CSV Local:** Execute as células de criação e leitura do arquivo `vendas_exemplo.csv`.
   - **Fluxo Google Sheets:** Insira o URL da sua planilha na variável `url_planilha` e execute a leitura em tempo real.
4. **Resultado:** O relatório executivo será impresso na tela e salvo automaticamente como um arquivo `.md` no ambiente.
