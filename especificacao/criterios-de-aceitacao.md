# Critérios de Aceitação

Sistema de Gestão de Eventos — Empresa Eventus

Estrutura adotada (Unidade III): **Dado** (contexto) — **Quando** (ação) — **Então** (comportamento esperado), no estilo BDD.

Apenas as histórias com comportamento verificável bem definido foram detalhadas. Onde a regra depende de uma definição em aberto (ver `analise/duvidas-e-lacunas.md`), o critério registra a **premissa assumida** — a ser confirmada com os stakeholders.

## HU-02 — Inscrever-se em um evento

| Dado | Quando | Então |
|------|--------|-------|
| O participante está autenticado e o evento gratuito tem vagas disponíveis | Solicita a inscrição | O sistema confirma a inscrição, decrementa uma vaga e emite o comprovante |
| O evento não tem vagas disponíveis | Solicita a inscrição | O sistema não confirma a inscrição e oferece entrada na lista de espera |
| A inscrição foi confirmada | A confirmação é concluída | O sistema disponibiliza o comprovante ao participante logo em seguida |

## HU-03 — Inscrever-se em vários workshops

*Premissa assumida: horários conflitantes bloqueiam a inscrição (a confirmar — lacuna 7).*

| Dado | Quando | Então |
|------|--------|-------|
| O participante já está inscrito em um workshop | Tenta se inscrever em outro no mesmo dia, sem conflito de horário | O sistema confirma a segunda inscrição |
| O participante já está inscrito em um workshop | Tenta se inscrever em outro com horário conflitante | O sistema impede a inscrição e informa o conflito |

## HU-04 — Acompanhar minhas inscrições

| Dado | Quando | Então |
|------|--------|-------|
| O participante possui inscrições registradas | Acessa a área de inscrições | O sistema lista cada inscrição com seu status (confirmada, pendente de pagamento, em lista de espera) |
| O participante não possui inscrições | Acessa a área de inscrições | O sistema informa que não há inscrições disponíveis para consulta |

## HU-05 — Cancelar inscrição

*Premissa assumida: cancelamento permitido apenas dentro do prazo e para eventos que o aceitam (a confirmar — lacunas 1 e 6).*

| Dado | Quando | Então |
|------|--------|-------|
| A inscrição pertence a um evento que permite cancelamento e está dentro do prazo | Solicita o cancelamento | O sistema cancela a inscrição e libera a vaga |
| O evento não permite cancelamento (ou o prazo encerrou) | Solicita o cancelamento | O sistema impede o cancelamento e informa o motivo |
| Uma vaga é liberada por cancelamento e há lista de espera | O cancelamento é concluído | O sistema trata a promoção do próximo da lista de espera |

## HU-06 — Entrar na lista de espera

| Dado | Quando | Então |
|------|--------|-------|
| O evento está lotado | Solicita a inscrição | O sistema oferece entrada na lista de espera |
| O participante aceita entrar na lista de espera | Confirma a entrada | O sistema registra sua posição e o notifica caso uma vaga seja liberada |

## HU-09 — Controlar vagas automaticamente

| Dado | Quando | Então |
|------|--------|-------|
| O evento tem uma vaga restante e dois participantes tentam se inscrever ao mesmo tempo | As duas inscrições são solicitadas simultaneamente | O sistema confirma apenas uma e encaminha a outra para a lista de espera (nunca ultrapassa o limite) |
| O evento atingiu o limite de vagas | Uma nova inscrição é solicitada | O sistema não confirma a inscrição direta e oferece lista de espera |

## HU-10 — Acompanhar inscritos em tempo real

*Premissa assumida: latência de poucos segundos (valor exato a confirmar — lacuna 10).*

| Dado | Quando | Então |
|------|--------|-------|
| O organizador está visualizando o painel do evento | Uma nova inscrição é confirmada | O sistema atualiza a contagem de inscritos em tempo quase real |

## HU-12 — Confirmar pagamento antes de liberar inscrição

| Dado | Quando | Então |
|------|--------|-------|
| O evento é pago e exige confirmação de pagamento | O participante solicita a inscrição | O sistema registra a inscrição como pendente de pagamento e não a confirma até o pagamento ser confirmado |
| O pagamento de uma inscrição pendente é confirmado | A confirmação é registrada | O sistema confirma a inscrição e emite o comprovante |
