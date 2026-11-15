# Study Agent — Skill e Templates para Plano de Estudos

Repositório de instruções e modelos da skill `plano-de-estudos`, desenhada para organizar cronogramas de estudo e gerar um arquivo CSV compatível com importação no Google Agenda.

> **Observação:** este repositório armazena as especificações de comportamento (`AGENTS.md`, `SKILL.md`), referências metodológicas e templates em Markdown utilizados pelo agente. Não inclui um runtime Python empacotado.

## Como funciona o fluxo da skill

Antes de montar um cronograma, o agente coleta quatro informações obrigatórias do usuário:

1. Objetivo de estudo.
2. Data de início e prazo final.
3. Dias da semana e horas disponíveis por dia.
4. Nível atual no assunto.

Com os dados definidos, as instruções em `skills/plano-de-estudos/references/` orientam a divisão em módulos, sessões de revisão e formatação em CSV (`plano-de-estudos.csv`) para importação manual na agenda.

## Estrutura do repositório

```text
├── AGENTS.md                          # Regras gerais e checklist do agente
├── README.md                          # Documentação do repositório
└── skills/
    └── plano-de-estudos/
        ├── SKILL.md                   # Definição de gatilho e etapas da skill
        ├── assets/
        │   ├── exemplo_plano.md       # Exemplo de saída
        │   └── plano_template.md      # Modelo padrão do plano
        └── references/
            ├── salvar_agenda.md       # Formato de colunas para o CSV do Google Agenda
            ├── tecnicas.md            # Técnicas de estudo e revisão espaçada
            └── workflow.md            # Fluxo de decisão do plano
```

## Como importar o CSV gerado no Google Agenda

1. Acesse o Google Agenda no navegador.
2. Abra **Configurações** -> **Importar e exportar**.
3. Envie o arquivo `plano-de-estudos.csv` gerado a partir do modelo e escolha a agenda de destino.
