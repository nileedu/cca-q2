# CCA-Q2 — Briefing do Projeto

> Curso preparatorio para Claude Certified Architect com aprendizado progressivo e formatos interativos.

---

## Contexto

O CCA-Q1 foi criado espelhando a estrutura do exame (5 dominios tecnicos em paginas HTML estaticas). Funciona para revisao, mas nao e a melhor forma de aprender do zero. O CCA-Q2 resolve isso com duas mudancas fundamentais:

1. **Reorganizacao por dificuldade crescente** (em vez de por dominio)
2. **Formatos interativos** (em vez de leitura passiva)

---

## Parte 1: Aprendizado em Espiral

Em vez de "dominio por dominio", o conteudo e reorganizado em camadas de complexidade crescente, onde cada camada reutiliza o que foi aprendido antes.

### Camada 1 — Fundamentos (Semana 1)
- O que e o Claude, API basica, uma chamada simples
- O loop agentico (o conceito mais fundamental — tudo depende dele)
- Primeira ferramenta: fazer Claude chamar uma tool e ver o resultado
- **Projeto pratico:** chatbot simples que consulta uma API

### Camada 2 — Estrutura (Semana 2)
- CLAUDE.md e como configurar o ambiente
- Commands e skills (usar o que ja existe)
- Few-shot e saida estruturada (JSON)
- **Projeto pratico:** extrator de dados de documentos com output JSON

### Camada 3 — Confiabilidade (Semana 3)
- Hooks vs prompts (a regra de ouro)
- Validacao e retry loops
- Erros estruturados (nunca retornar "falhou" generico)
- Gerenciamento de contexto (lost in the middle)
- **Projeto pratico:** agente de suporte com regras de compliance via hooks

### Camada 4 — Escala (Semana 4)
- Multi-agente (hub-and-spoke)
- MCP servers e integracao
- CI/CD com Claude Code
- Revisao independente (segunda instancia)
- **Projeto pratico:** sistema multi-agente de pesquisa com coordenador

### Camada 5 — Simulado (Semana 5)
- Revisao das 5 regras de ouro
- Cenarios do exame com quiz
- Mock exam completo

### Diferenca vs CCA-Q1

| CCA-Q1 | CCA-Q2 |
|--------|--------|
| Organizado por dominio do exame | Organizado por dificuldade crescente |
| Teoria pesada, pratica no final | Projeto pratico a cada semana |
| Pode comecar em qualquer trilha | Cada camada depende da anterior |
| Bom para quem ja sabe e quer revisar | Bom para quem esta aprendendo |
| 30 modulos densos | Mesmo conteudo em espiral — revisitado com mais profundidade |

### O pulo do gato
Cada projeto pratico acumula — o chatbot da semana 1 ganha JSON na semana 2, hooks na semana 3, vira multi-agente na semana 4. O aluno termina com um sistema completo e esta pronto para o exame.

---

## Parte 2: Formatos de Apresentacao

### O problema do formato atual
Paginas HTML estaticas com topicos expansiveis. Funciona, mas e essencialmente leitura passiva — o aluno abre, le, fecha.

### 3 Formatos Combinados

| Momento | Formato | Por que |
|---------|---------|---------|
| Primeiro contato | **Mapa visual interativo** | Da visao do todo sem assustar |
| Aprendizado | **Simulador de cenarios** | Ensina pelo fazer, nao pelo ler |
| Fixacao | **Flashcards** com repeticao espacada | Garante retencao de longo prazo |

### Formato 1: Mapa Visual Interativo
- Uma pagina unica com o mapa completo dos 5 dominios
- Cada conceito e um no clicavel que expande
- Conexoes visuais entre conceitos (ex: "hooks" conecta com "compliance" e "Agent SDK")
- O aluno ve o todo e navega pelo que interessa
- Formato: SVG/Canvas interativo ou mind map HTML

### Formato 2: Simulador de Cenarios (Choose Your Path)
- Os 6 cenarios do exame viram narrativas interativas
- "Voce e o arquiteto. O cliente pede reembolso de R$50k. O que voce faz?"
- Cada escolha leva a um resultado diferente com explicacao
- Ensina julgamento, nao memorizacao — exatamente o que a prova cobra

### Formato 3: Flashcards Interativos (Spaced Repetition)
- Cada conceito vira um card frente/verso
- O aluno marca "sabia" / "nao sabia" — o sistema repete os dificeis com mais frequencia
- Perfeito para os 30 task statements e as 5 regras de ouro
- Formato: app web single-page com localStorage para progresso

### Paginas de conteudo (referencia)
As paginas HTML de conteudo do CCA-Q1 viram material de referencia — o aluno consulta quando erra um flashcard ou quer se aprofundar no cenario.

### Principio central
Inverter o fluxo: em vez de **ler -> testar**, vai para **testar -> errar -> aprender -> fixar**.

---

## Dados do Exame CCA-F

| Item | Detalhe |
|------|---------|
| Nome | Claude Certified Architect — Foundations (CCA-F) |
| Formato | 60 questoes multipla escolha (cenarios), 120 minutos, proctored |
| Nota minima | 720 / 1.000 |
| Custo | US$ 99 por tentativa (gratis para primeiros 5.000 do Partner Network) |
| Registro | Via Claude Partner Network em anthropic.skilljar.com |
| Publico | Arquitetos com 6+ meses construindo com Claude API, Agent SDK, Claude Code e MCP |

### 5 Dominios

| Dominio | Peso |
|---------|------|
| Arquitetura Agentica e Orquestracao | 27% |
| Design de Ferramentas e Integracao MCP | 18% |
| Configuracao e Fluxos do Claude Code | 20% |
| Engenharia de Prompt e Saida Estruturada | 20% |
| Gerenciamento de Contexto e Confiabilidade | 15% |

### 6 Cenarios do Exame (4 aleatorios por prova)
1. Agente de Suporte ao Cliente
2. Geracao de Codigo com Claude Code
3. Sistema Multi-Agente de Pesquisa
4. Produtividade do Desenvolvedor com Claude
5. Claude Code para CI/CD
6. Extracao de Dados Estruturados

### 5 Regras de Ouro
1. **Hooks > Prompts** — Imposicao programatica para compliance 100%
2. **Erros Estruturados Sempre** — Inclua o que quebrou, tentou e alternativas
3. **4-5 Ferramentas por Agente** — Menos opcoes = decisoes melhores
4. **Revisao Independente** — Segunda instancia percebe o que a primeira nao percebe
5. **Exemplos > Instrucoes** — 2-3 exemplos few-shot vencem paragrafos de regras

---

## Estrutura de Arquivos Planejada

```
cca-q2/
├── index.html                    # Landing page com mapa visual
├── doc/
│   ├── BRIEFING_CURSO.md         # Este documento
│   └── (materiais de referencia)
├── mapa/
│   └── index.html                # Mapa interativo dos 5 dominios
├── cenarios/
│   ├── index.html                # Hub dos 6 cenarios
│   ├── cenario-1.html            # Suporte ao Cliente (interativo)
│   ├── cenario-2.html            # Geracao de Codigo
│   ├── cenario-3.html            # Multi-Agente Pesquisa
│   ├── cenario-4.html            # Produtividade Dev
│   ├── cenario-5.html            # CI/CD
│   └── cenario-6.html            # Extracao Estruturada
├── flashcards/
│   └── index.html                # App de flashcards com spaced repetition
└── camadas/
    ├── index.html                # Visao geral das 5 camadas
    ├── camada-1/                 # Fundamentos
    ├── camada-2/                 # Estrutura
    ├── camada-3/                 # Confiabilidade
    ├── camada-4/                 # Escala
    └── camada-5/                 # Simulado
```
