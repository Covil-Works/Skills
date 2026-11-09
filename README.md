# Covil Skills

Repositório centralizado de **skills** customizadas para agentes de IA (Antigravity e ferramentas compatíveis), desenvolvidas e mantidas pela Covil.

---

## 📂 Como este repositório está organizado

Cada skill possui sua própria pasta na raiz:

```text
skills/
├── README.md                          # Este catálogo geral
└── <nome-da-skill>/                   # Diretório da skill
    ├── README.md                      # O que faz, pré-requisitos e instruções de uso
    └── <nome-da-skill>/               # 📦 Pasta pronta para copiar e colar
        ├── SKILL.md                   # Instruções e metadados lidos pelo agente
        ├── scripts/                   # (Opcional) Scripts auxiliares executáveis
        ├── references/                # (Opcional) Manuais e documentações
        └── resources/                 # (Opcional) Templates e arquivos estáticos
```

Essa estrutura permite que você simplesmente copie a pasta interna `<nome-da-skill>` e a cole diretamente no seu projeto ou na sua configuração global.

---

## ⚡ Como instalar uma skill no seu repositório

### Método 1: Via Terminal com `npx degit` (Mais rápido e recomendado)

Instale direto no terminal sem precisar clonar ou baixar o repositório manualmente:

```bash
# No seu projeto atual:
npx degit Covil-Works/Skills/<nome-da-skill>/<nome-da-skill> .agents/skills/<nome-da-skill>

# Globalmente na sua máquina (Linux/macOS):
npx degit Covil-Works/Skills/<nome-da-skill>/<nome-da-skill> ~/.gemini/config/skills/<nome-da-skill>
```

---

### Método 2: Manualmente (Copiar e colar)

1. Entre na pasta da skill desejada neste repositório.
2. Copie a pasta interna da skill (aquela que contém o `SKILL.md`).
3. Cole no seu destino:
   - **No seu projeto (recomendado para versionar com o time):**
     Coloque em `.agents/skills/<nome-da-skill>/`
   - **Globalmente na sua máquina:**
     Coloque em `~/.gemini/config/skills/<nome-da-skill>/`

---

## 🛠️ Catálogo de Skills

| Skill | Descrição | Status |
| :--- | :--- | :---: |
| [`docxt`](./docxt/README.md) | Inicializa e governa a documentação do repositório em `/docs` usando `AGENTS.md`, índice temático e regras com IDs sequenciais únicos. | 🟢 Disponível |
| [`memorycard`](./memorycard/README.md) | Gerencia tarefas e projetos via CLI (`memorycard`) e board visual com alinhamento prévio reativo antes de codificar. | 🟢 Disponível |

---

## ➕ Adicionando uma nova skill

1. Crie uma nova pasta com o nome da skill: `/<nome-da-skill>/`.
2. Adicione o `README.md` da skill explicando o objetivo e como usar.
3. Adicione a pasta interna `<nome-da-skill>/` contendo o `SKILL.md` e seus arquivos auxiliares.
4. Adicione a nova skill na tabela do catálogo acima.
