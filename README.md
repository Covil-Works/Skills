# Covil Skills

Repositório centralizado de skills customizadas para agentes de IA (Antigravity e ferramentas compatíveis), desenvolvidas e mantidas pela Covil.

---

## Organização

Cada pasta na raiz deste repositório contém uma skill individual.

---

## Como instalar uma skill no seu repositório

### Via Terminal com npx degit (Recomendado)

Instale direto no seu projeto com um único comando:

```bash
npx degit Covil-Works/Skills/<nome-da-skill>/<nome-da-skill> .agents/skills/<nome-da-skill>
```

### Manualmente (Copiar e colar)

1. Entre na pasta da skill desejada neste repositório.
2. Copie a pasta interna `<nome-da-skill>` (aquela que contém o `SKILL.md`).
3. Cole em `.agents/skills/<nome-da-skill>/` no seu projeto.

---

## Catálogo de Skills

| Skill | Descrição | Status |
| :--- | :--- | :---: |
| [`docxt`](./docxt/README.md) | Inicializa e governa a documentação do repositório em `/docs` usando `AGENTS.md`, índice temático e regras com IDs sequenciais únicos. | Disponível |
| [`memorycard`](./memorycard/README.md) | Permite que agentes de IA operem a ferramenta MemoryCard para gerenciar tarefas e contexto do projeto. | Disponível |

---

## Adicionando uma nova skill

1. Crie uma nova pasta com o nome da skill: `/<nome-da-skill>/`.
2. Adicione o `README.md` da skill explicando o objetivo e como usar.
3. Adicione a pasta interna `<nome-da-skill>/` contendo o `SKILL.md` e seus arquivos auxiliares.
4. Adicione a nova skill na tabela do catálogo acima.
