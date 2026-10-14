# atendimento-whatsapp-n8n

Fluxo de n8n que recebe o primeiro contato de um lead no WhatsApp, qualifica a conversa com IA, registra o lead em planilha e avisa o time por Telegram. Construído para a operação de uma ótica em Belém e publicado aqui em versão sanitizada.

## Problema

Mensagens chegavam a qualquer hora, inclusive fora do expediente. Sem registro central, o lead esfriava antes de alguém responder e não havia como saber quantos contatos viravam atendimento.

## Como funciona

**1. Entrada.** Um webhook recebe a mensagem do WhatsApp e normaliza o payload.

**2. Qualificação.** Um nó de IA classifica a intenção do contato e extrai nome e necessidade em formato estruturado.

**3. Registro.** O lead é gravado em planilha com data, canal, intenção e status.

**4. Notificação.** Quando a intenção é de compra ou agendamento, o resumo vai para o time por Telegram.

**5. Resposta.** O lead recebe uma mensagem de acolhimento com o próximo passo.

## Stack

n8n · WhatsApp Business API · LLM · Google Sheets · Telegram Bot API

## Como usar

Importe `workflow.json` no seu n8n, copie `.env.example` para `.env` e preencha as credenciais. Nenhuma credencial está versionada neste repositório.

## Sanitização

Este repositório não contém tokens, URLs de webhook, números de telefone, dados de clientes nem nomes de empresas. Os exemplos são fictícios.
