# docxt

Skill para inicialização e governança contínua de documentação técnica e regras de projeto em `/docs`, orientada a agentes de IA.

---

## 🎯 O que faz

A **docxt** padroniza a gestão de contexto e diretrizes do repositório através de:
- **`AGENTS.md` raiz**: Ponto de entrada obrigatório para agentes, garantindo que consultem a documentação antes de implementar qualquer funcionalidade.
- **Índice temático central (`/docs/index.md`)**: Visão geral de alta legibilidade com tópicos e escopos mapeados em `kebab-case`.
- **Regras com IDs únicos sequenciais**: Cada instrução ou convenção recebe um identificador do tipo `[nome-do-arquivo]-[001]`, prevenindo duplicidades e facilitando referências diretas.
- **Governança não-destrutiva**: Tratamento explícito de conflitos de regras, exigindo aprovação antes de qualquer alteração ou substituição.

---

## 🚀 Modos de Uso

| Comando / Gatilho | Ação |
| :--- | :--- |
| `/docxt init` ou *"inicia a documentação"* | Cria o scaffold inicial (`AGENTS.md` na raiz, pasta `/docs`, `/docs/index.md` e `/docs/AGENTS.md`). |
| `/docxt add <instrução>` ou *"anota essa regra"* | Registra uma nova convenção no arquivo temático correto com numeração sequencial de 3 dígitos. |
| *Detecção automática de conflito* | Se uma instrução futura contradisser `/docs`, a IA pausa e cita o ID conflitante para decisão. |

---

## 📦 Como Instalar

Para usar esta skill no seu projeto ou ambiente:

### Opção 1: No seu projeto (Recomendado)
Copie a pasta interna `docxt/` para a pasta de skills do seu repositório:
```text
seu-projeto/
└── .agents/
    └── skills/
        └── docxt/         <-- Cole a pasta aqui (contendo o SKILL.md)
```

### Opção 2: Globalmente na sua máquina
Copie a pasta interna `docxt/` para a pasta de configurações de skills do seu usuário:
- **Windows**: `%USERPROFILE%\.gemini\config\skills\docxt\`
- **Linux/macOS**: `~/.gemini/config/skills/docxt/`

---

## 📂 Estrutura desta pasta

```text
docxt/
├── README.md              # Este manual de uso e instalação
└── docxt/                 # 📦 Pasta plug-and-play da skill
    └── SKILL.md           # Definição e instruções executadas pelo agente
```
