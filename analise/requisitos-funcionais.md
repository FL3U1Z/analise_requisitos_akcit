# Requisitos Funcionais

Sistema de Gestão de Eventos — Empresa Eventus

Os requisitos abaixo descrevem **o que o sistema deve fazer**, derivados do documento de elicitação. Foram organizados por área de interesse do stakeholder correspondente. O identificador segue o padrão `RF-XX`.

> Observação: alguns pontos ainda dependem de esclarecimento junto aos stakeholders (ver `duvidas-e-lacunas.md`). Onde um requisito depende de uma definição em aberto, isso está sinalizado.

## Participantes

| ID | Requisito |
|----|-----------|
| RF-01 | O sistema deve permitir que o participante visualize, em um único lugar, todos os eventos disponíveis. |
| RF-02 | O sistema deve permitir que o participante se inscreva em um evento. |
| RF-03 | O sistema deve permitir que o participante se inscreva em mais de um workshop, inclusive quando ocorrerem no mesmo dia (respeitando a regra de conflito de horários — ver RN e lacunas). |
| RF-04 | O sistema deve emitir um comprovante de inscrição ao participante logo após a conclusão da inscrição. |
| RF-05 | O sistema deve permitir que o participante acompanhe o status de suas inscrições. |
| RF-06 | O sistema deve permitir que o participante cancele a própria inscrição, sem necessidade de contato com a organização (quando o evento permitir cancelamento). |
| RF-07 | O sistema deve permitir que o participante emita seu certificado após o evento. |
| RF-08 | O sistema deve permitir que o participante entre em uma lista de espera quando o evento estiver lotado. |

## Organizadores

| ID | Requisito |
|----|-----------|
| RF-09 | O sistema deve permitir que o organizador crie eventos. |
| RF-10 | O sistema deve controlar automaticamente o número de vagas de cada evento. |
| RF-11 | O sistema deve permitir que o organizador acompanhe a quantidade de inscritos em tempo real. |
| RF-12 | O sistema deve gerenciar uma lista de espera quando o evento atingir o limite de vagas. |
| RF-13 | O sistema deve permitir que o organizador defina se um evento aceita ou não cancelamento de inscrição. |
| RF-14 | O sistema deve permitir que o organizador gerencie os participantes de seus eventos. |
| RF-15 | O sistema deve garantir que workshops agendados no mesmo horário possam ocorrer simultaneamente (não são mutuamente exclusivos do ponto de vista da programação). |

## Equipe Financeira

| ID | Requisito |
|----|-----------|
| RF-16 | O sistema deve permitir a configuração de eventos gratuitos e eventos pagos. |
| RF-17 | O sistema deve permitir a confirmação de pagamento antes de liberar determinadas inscrições. |
| RF-18 | O sistema deve controlar reembolsos de acordo com as regras aplicáveis a cada evento. |

## Palestrantes

| ID | Requisito |
|----|-----------|
| RF-19 | O sistema deve permitir que o palestrante consulte a programação de suas atividades. |
| RF-20 | O sistema deve permitir que o palestrante consulte a lista de participantes inscritos em suas atividades (o escopo dos dados visíveis ainda precisa ser definido — ver lacunas). |

## Notificações e Certificados (transversal)

| ID | Requisito |
|----|-----------|
| RF-21 | O sistema deve enviar comprovantes de inscrição e demais notificações aos participantes (o canal ainda precisa ser definido — ver lacunas). |
| RF-22 | O sistema deve emitir certificados aos participantes (a regra de emissão — automática ou condicionada à confirmação de presença — ainda precisa ser definida). |
