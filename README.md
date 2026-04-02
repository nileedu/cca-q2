# CCA-Q2 — Claude Certified Architect — Preparatorio Interativo

Curso preparatorio para a certificacao Claude Certified Architect (CCA-F) com aprendizado progressivo e formatos interativos.

## Estrutura do Projeto

```
cca-q2/
├── index.html                     # Landing page
├── css/style.css                  # Design system (dark theme, Anthropic palette)
├── mapa/index.html                # Mapa SVG interativo dos 5 dominios
├── cenarios/
│   ├── index.html                 # Hub dos 6 cenarios
│   └── cenario-1..6.html          # 6 simulacoes interativas (4 decisoes cada)
├── flashcards/index.html          # 55 flashcards com repeticao espacada (SM-2)
└── camadas/
    ├── index.html                 # Timeline das 5 camadas
    ├── camada-1/index.html        # Fundamentos
    ├── camada-2/index.html        # Estrutura
    ├── camada-3/index.html        # Confiabilidade
    ├── camada-4/index.html        # Escala
    └── camada-5/index.html        # Simulado (quiz 15 questoes)
```

## Formatos de Aprendizado

| Formato | Descricao |
|---------|-----------|
| **Mapa Visual** | Mapa conceitual SVG interativo com conexoes entre os 5 dominios e 30 task statements |
| **Cenarios** | 6 simulacoes "choose your path" com 24 decisoes arquiteturais no total |
| **Flashcards** | 55 cards com repeticao espacada (SM-2) e progresso salvo em localStorage |
| **Camadas** | 5 camadas de complexidade crescente com checklists interativos |

## 5 Dominios do Exame

| Dominio | Peso |
|---------|------|
| Arquitetura Agentica e Orquestracao | 27% |
| Design de Ferramentas e Integracao MCP | 18% |
| Configuracao e Fluxos do Claude Code | 20% |
| Engenharia de Prompt e Saida Estruturada | 20% |
| Gerenciamento de Contexto e Confiabilidade | 15% |

## 5 Regras de Ouro

1. **Hooks > Prompts** — Imposicao programatica para compliance 100%
2. **Erros Estruturados Sempre** — Inclua o que quebrou, tentou e alternativas
3. **4-5 Ferramentas por Agente** — Menos opcoes = decisoes melhores
4. **Revisao Independente** — Segunda instancia percebe o que a primeira nao percebe
5. **Exemplos > Instrucoes** — 2-3 exemplos few-shot vencem paragrafos de regras

## Dados do Exame

- **Formato:** 60 questoes multipla escolha, 120 minutos, proctored
- **Nota minima:** 720 / 1.000
- **Custo:** US$ 99 (gratis para primeiros 5.000 do Partner Network)
- **Registro:** anthropic.skilljar.com

## Tecnologia

- HTML/CSS/JS puro (sem frameworks)
- Dark theme responsivo
- Progresso salvo em localStorage
- Google Fonts (Inter)
