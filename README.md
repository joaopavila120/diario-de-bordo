# Diário de Bordo

Protótipo de aplicativo para o diário e o checklist das máquinas da fazenda. O operador escaneia o QR code da máquina, lança o diário com o horímetro, e o dono acompanha a frota e as revisões num painel.

**Acesse:** https://joaopavila120.github.io/diario-de-bordo/

## O que tem

**Operador (celular)**
- Início com "Olá", leitura de QR code e lista de máquinas.
- **Diário**: horímetro, nível do óleo do motor, nível do óleo hidráulico e água do radiador.
- **Checklist pré-safra**: conferência completa antes da safra (na plantadeira, a lista de plantabilidade).
- Registrar revisão (óleo, filtros, valores medidos), histórico, dicas de operação e últimas atividades.
- Alerta de revisão pelo horímetro: avisa quantas horas faltam para a próxima troca.

**Dono (painel)**
- Visão geral, máquinas, diários e checklists recebidos e revisões a fazer.
- Adicionar veículo e gerar a etiqueta com QR code.
- Adicionar revisões (só marcar, número ou texto) e itens ao diário e ao checklist de cada máquina.

**Sem internet**
- Depois do primeiro acesso, o app abre e salva sem sinal. O que for lançado offline fica na fila e é enviado quando o sinal volta.
- No celular, dá para instalar na tela inicial: no Chrome, menu ⋮ → "Instalar app"; no iPhone, Compartilhar → "Adicionar à Tela de Início".

## Como publicar no GitHub Pages

1. Envie os arquivos desta pasta para a branch `main` do repositório.
2. No GitHub, abra **Settings → Pages**.
3. Em **Build and deployment**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`, e clique em **Save**.
4. Em 1 ou 2 minutos o site fica no ar em https://joaopavila120.github.io/diario-de-bordo/

## Etiquetas QR

Cada etiqueta abre o app direto na máquina, por exemplo `https://joaopavila120.github.io/diario-de-bordo/#plt-01`. Baixe as etiquetas no painel do dono, em **Etiquetas QR** ou na tela de cada máquina.

## Limitações do protótipo

- Os dados ficam no navegador de cada aparelho. O celular do operador e o painel do dono não se sincronizam entre si; para demonstrar, use as abas **Operador** e **Dono** no mesmo aparelho.
- Máquinas, leituras e revisões são dados de exemplo. O botão **Reiniciar demonstração** volta ao começo do dia.
- O aviso no WhatsApp do dono é só indicado na tela, não é enviado.

## Arquivos

| Arquivo | Para que serve |
| --- | --- |
| `index.html` | O app inteiro (telas, estilos e lógica) |
| `sw.js` | Guarda o app no aparelho para funcionar sem internet |
| `manifest.webmanifest` | Nome, cores e ícones para instalar na tela inicial |
| `icons/` | Ícones do app |
