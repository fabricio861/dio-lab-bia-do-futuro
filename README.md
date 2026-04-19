# 🎓 Tiago - Educador Financeiro Inteligente
> Agente de IA Generativa que ensina conceitos de finanças pessoais de forma simples e personalizada, usando os próprios dados do cliente como exemplos práticos.

## 💡 O Que é o Tiago?
O Tiago é um educador financeiro que **ensina**, não recomenda. Ele explica conceitos como reserva de emergência, tipos de investimentos e análise de gastos usando uma abordagem didática e exemplos concretos baseados no perfil do cliente.

**O que o Tiago faz:**
- ✅ Explica conceitos financeiros de forma simples
- ✅ Usa dados do cliente como exemplos práticos
- ✅ Responde dúvidas sobre produtos financeiros
- ✅ Analisa padrões de gastos de forma educativa

**O que o Tiago NÃO faz:**
- ❌ Não recomenda investimentos específicos
- ❌ Não acessa dados bancários sensíveis
- ❌ Não substitui um profissional certificado

## 🏗️ Arquitetura
flowchart TD
    A[Usuário] --> B[Streamlit]
    B --> C[Ollama - LLM Local]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Resposta Educativa]

**Stack:**
- Interface: Streamlit
- LLM: Ollama (modelo local gpt-oss)
- Dados: JSON/CSV mockados

## 📁 Estrutura do Projeto
├── data/
│   ├── perfil_investidor.json
│   ├── transacoes.csv
│   ├── historico_atendimento.csv
│   └── produtos_financeiros.json
├── docs/
│   ├── 01-documentacao-agente.md
│   ├── 02-base-conhecimento.md
│   ├── 03-prompts.md
│   ├── 04-metricas.md
│   └── 05-pitch.md
└── src/
    └── app.py

## 🚀 Como Executar
1. Instalar Ollama
- Baixar em: ollama.com
- ollama pull gpt-oss
- ollama serve

2. Instalar Dependências
- pip install streamlit pandas requests

3. Rodar o Tiago
- streamlit run src/app.py

## 🎯 Exemplo de Uso
Pergunta: "O que é CDI?"
Tiago: "CDI é uma taxa de referência usada pelos bancos. Quando um investimento rende '100% do CDI', significa que ele acompanha essa taxa. Hoje o CDI está próximo da Selic. Quer que eu explique a diferença entre os dois?"

Pergunta: "Onde estou gastando mais?"
Tiago: "Olhando suas transações de outubro, sua maior despesa é moradia (R$ 1.380), seguida de alimentação (R$ 570). Juntas, representam quase 80% dos seus gastos. Isso é bem comum! Quer que eu explique algumas estratégias de organização?"

## 📊 Métricas de Avaliação
- Assertividade: O agente responde o que foi perguntado?
- Segurança: Evita inventar informações (anti-alucinação)?
- Coerência: A resposta é adequada ao perfil do cliente?

## 🎬 Diferenciais
- Personalização: Usa os dados do próprio cliente nos exemplos
- 100% Local: Roda com Ollama, sem enviar dados para APIs externas
- Educativo: Foco em ensinar, não em vender produtos
- Seguro: Estratégias de anti-alucinação documentadas
