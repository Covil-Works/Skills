# memorycard

Skill para agentes de IA gerenciarem tarefas e preservarem o contexto operacional do projeto utilizando a ferramenta [MemoryCard](https://github.com/Covil-Works/MemoryCard).

Esta skill ensina o agente a operar o MemoryCard para você, alinhando tarefas antes de codificar, atualizando checklists e registrando o histórico de desenvolvimento.

---

## O que a Skill faz

Quando instalada no seu projeto, a skill orienta o agente a:
- **Alinhamento prévio automático:** Antes de iniciar qualquer feature ou refatoração, o agente verifica tarefas em aberto ou pergunta se você deseja registrar uma task para acompanhar o trabalho.
- **Gerenciamento contínuo de tarefas:** Sob seu comando, o agente cria tasks, move status (`todo`, `in-progress`, `done`), marca checklists de progresso e insere comentários técnicos.
- **Verificação de ambiente:** Se a CLI do [MemoryCard](https://github.com/Covil-Works/MemoryCard) não estiver instalada na máquina, o agente detecta e orienta os passos necessários para habilitá-la.

---

## Como usar a Skill no chat com o Agente

Você pode acionar o comportamento da skill conversando normalmente com o agente:

| O que você fala | O que a skill faz |
| :--- | :--- |
| *"Onde a gente parou?"* / *"Qual o status do trabalho?"* | Consulta a tarefa ativa e o contexto recente no MemoryCard. |
| *"Cria uma task para [X]"* | Cria uma nova tarefa com título e descrição. |
| *"Vamos detalhar os passos dessa task"* | Adiciona itens ao checklist da tarefa em andamento. |
| *"Marca o passo 1 como feito"* | Atualiza o checklist da tarefa. |
| *"Finaliza a task"* | Move a tarefa para concluída (`done`). |
| *"Abre o board no navegador"* | Inicia o servidor local e abre o painel visual do MemoryCard. |

---

## Como Instalar

### Via Terminal com npx degit (Recomendado)

Instale no diretório de skills do seu projeto:

```bash
npx degit Covil-Works/Skills/memorycard/memorycard .agents/skills/memorycard
```

---

### Manualmente (Copiar e Colar)

Copie a pasta interna `memorycard/` para a pasta de skills do seu repositório:

```text
seu-projeto/
└── .agents/
    └── skills/
        └── memorycard/         <-- Cole a pasta aqui (contendo o SKILL.md)
```
