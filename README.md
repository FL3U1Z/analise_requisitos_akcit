# Engenharia de Requisitos com GenAI — Exercício Prático (Unidade III)

Análise e especificação de requisitos do **Sistema de Gestão de Eventos** da empresa Eventus, produzidos a partir do documento de elicitação fornecido na atividade 3.4.

## Estrutura

```
engenharia-requisitos-genai/
├── README.md
├── analise/
│   ├── requisitos-funcionais.md
│   ├── requisitos-nao-funcionais.md
│   ├── regras-de-negocio.md
│   └── duvidas-e-lacunas.md
└── especificacao/
    ├── historias-de-usuario.md
    ├── criterios-de-aceitacao.md
    └── caso-de-uso-inscricao.md
```

## Reflexão sobre o uso da Inteligência Artificial

### Qual ferramenta de GenAI foi utilizada
Foi utilizado o Claude (assistente baseado em LLM) como apoio à análise das informações de elicitação e à elaboração dos artefatos de especificação.

### Como a IA apoiou as diferentes etapas
- **Análise:** apoio na separação das informações do documento em requisitos funcionais, não funcionais, regras de negócio e lacunas; e na identificação de necessidades implícitas (especialmente os requisitos não funcionais, que o próprio documento registra como não levantados).
- **Refinamento:** sugestão de perguntas de esclarecimento para os pontos em aberto, consolidadas em `duvidas-e-lacunas.md`.
- **Especificação:** apoio na redação das histórias de usuário, dos critérios de aceitação no formato Dado–Quando–Então e do caso de uso do fluxo de inscrição.

### Quais sugestões foram aceitas
- Organizar os requisitos por stakeholder.
- Tratar o controle de vagas + lista de espera + pagamento como o fluxo mais complexo e documentá-lo como caso de uso.
- Registrar os requisitos não funcionais como propostos e a validar, já que não foram levantados na elicitação.

### Quais sugestões foram descartadas ou modificadas e por quê
- Exemplo a validar: a premissa de que horários conflitantes bloqueiam a inscrição foi assumida nos critérios de aceitação, mas ainda **não foi confirmada** com os stakeholders — pode ser ajustada.

### Por que os artefatos escolhidos foram considerados os mais adequados
Optou-se por **histórias de usuário + critérios de aceitação** como base, complementadas por **um caso de uso** para o fluxo mais complexo:

- As **histórias de usuário** comunicam de forma simples o valor entregue a cada perfil (participante, organizador, financeiro, palestrante) e favorecem a priorização incremental — adequado a um sistema com muitos stakeholders e vários pontos ainda em aberto.
- Os **critérios de aceitação** (Dado–Quando–Então) tornam o comportamento verificável e servem de base para testes, ajudando a expor as premissas assumidas onde há lacunas.
- O **caso de uso** foi reservado ao fluxo de inscrição, que concentra fluxos alternativos (sem vagas, evento pago, conflito de horário) e se beneficia da estrutura mais detalhada — sem impor o custo de documentar todo o sistema nesse nível.

Um documento de especificação totalmente formal (estilo tradicional) foi considerado excessivo para o estágio atual, em que muitos requisitos ainda dependem de esclarecimento; protótipos não foram incluídos por dependerem de definições de interface ainda não disponíveis.

### Observação sobre o papel da IA
Conforme o objetivo da atividade, a IA foi usada como **apoio à decisão e ao refinamento**, não como produtora automática da documentação. 