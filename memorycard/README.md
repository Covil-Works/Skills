# memorycard

Skill para gerenciamento ágil de tarefas e projetos via CLI local, integrada ao fluxo de trabalho de agentes de IA.

> 🔗 **Repositório oficial da ferramenta:** [Covil-Works/MemoryCard](https://github.com/Covil-Works/MemoryCard)

---

## 🎯 O que faz

A **memorycard** permite que o agente gerencie o ciclo de vida completo de tarefas diretamente do terminal ou board visual:
- **Alinhamento prévio reativo:** Antes de iniciar qualquer feature ou refatoração, o agente verifica tarefas existentes ou oferece criar uma nova task.
- **Operação de tarefas via CLI:** Criação, checklists (`todo`), status (`in-progress`, `done`), comentários e consulta rápida de contexto.
- **Board em tempo real:** Interface visual no navegador acionada via `memorycard open` sincronizada por Server-Sent Events (SSE).

---

## ⚙️ Pré-requisito: Ferramenta MemoryCard CLI

Para que o agente consiga operar esta skill, o comando `memorycard` deve estar acessível no terminal:

```bash
# 1. Clone o repositório da ferramenta (caso ainda não tenha)
git clone https://github.com/Covil-Works/MemoryCard.git
cd MemoryCard

# 2. Instale as dependências e registre globalmente no sistema
npm install
npm link

# 3. Teste se está funcionando
memorycard --version
```

---

## 🚀 Comandos Rápidos da CLI

| Comando | Descrição |
| :--- | :--- |
| `memorycard current` | Exibe a task atualmente em andamento. |
| `memorycard create "<título>" -d "<descrição>"` | Cria uma nova task no projeto. |
| `memorycard list` | Lista todas as tarefas cadastradas. |
| `memorycard todo add <id> "<passo>"` | Adiciona um item ao checklist da task. |
| `memorycard todo done <id> <n>` | Conclui o item `n` (1-based) do checklist. |
| `memorycard move <id> <status>` | Move a task de coluna (`todo`, `in-progress`, `done`). |
| `memorycard open` | Abre a interface visual do board no navegador. |

---

## 📦 Como Instalar esta Skill

### ⚡ Instalação Rápida via Terminal (Recomendado)

Você pode instalar a skill com um único comando no terminal, sem precisar clonar ou baixar o repositório manualmente:

#### No seu projeto (em `.agents/skills/memorycard`):
```bash
npx degit Covil-Works/Skills/memorycard/memorycard .agents/skills/memorycard
```

*(Ou diretamente do repositório da ferramenta: `npx degit covil-works/memorycard/skills/memorycard .agents/skills/memorycard`)*

#### Globalmente na sua máquina:
- **Linux/macOS:**
  ```bash
  npx degit Covil-Works/Skills/memorycard/memorycard ~/.gemini/config/skills/memorycard
  ```
- **Windows (PowerShell):**
  ```powershell
  npx degit Covil-Works/Skills/memorycard/memorycard "$HOME/.gemini/config/skills/memorycard"
  ```

---

### 📂 Instalação Manual (Copiar e Colar)

Caso prefira baixar ou copiar os arquivos manualmente:

#### Opção 1: No seu projeto
Copie a pasta interna `memorycard/` para a pasta de skills do seu repositório:
```text
seu-projeto/
└── .agents/
    └── skills/
        └── memorycard/         <-- Cole a pasta aqui (contendo o SKILL.md)
```

#### Opção 2: Globalmente na sua máquina
Copie a pasta interna `memorycard/` para a pasta de configurações de skills do seu usuário:
- **Windows**: `%USERPROFILE%\.gemini\config\skills\memorycard\`
- **Linux/macOS**: `~/.gemini/config/skills/memorycard/`

---

## 📂 Estrutura desta pasta

```text
memorycard/
├── README.md                  # Este manual de uso e instalação
└── memorycard/                # 📦 Pasta plug-and-play da skill
    └── SKILL.md               # Instruções e rotinas lidas pelo agente
```
