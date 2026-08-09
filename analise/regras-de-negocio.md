# Regras de Negócio

Sistema de Gestão de Eventos — Empresa Eventus

As regras abaixo representam **condições, políticas e restrições** que orientam o comportamento das funcionalidades, mas não são funcionalidades em si (conforme distinção da Unidade I: *se a regra continua válida mesmo sem o sistema, é uma regra de negócio*). O identificador segue o padrão `RN-XX`.

Muitas dessas regras estão **parcialmente definidas** na elicitação — o documento deixa claro que existem casos "em que sim, em que não", sem detalhar os critérios. Onde a regra existe mas os critérios estão em aberto, isso está sinalizado como *parâmetro a definir*.

| ID | Regra de Negócio | Situação |
|----|------------------|----------|
| RN-01 | Um evento possui um número máximo de vagas; ao atingir esse limite, novas inscrições não são confirmadas diretamente e passam para lista de espera. | Definida |
| RN-02 | Eventos podem ser gratuitos ou pagos. | Definida |
| RN-03 | Para eventos pagos, a inscrição só é confirmada após a confirmação do pagamento. | Definida (aplica-se a "determinadas inscrições" — quais exatamente é *parâmetro a definir*) |
| RN-04 | Nem todos os eventos permitem cancelamento de inscrição; essa permissão é definida por evento. | Definida |
| RN-05 | O direito a reembolso depende do evento: em alguns casos há reembolso, em outros não. | Parcialmente definida — critérios de reembolso são *parâmetro a definir* |
| RN-06 | Existe um prazo-limite para cancelamento de inscrição pelo participante. | Existência confirmada; o prazo em si é *parâmetro a definir* |
| RN-07 | Workshops que ocorrem no mesmo horário são simultâneos; portanto, um participante não pode se inscrever em dois workshops com horários conflitantes. | Regra implícita, precisa de validação (ver lacunas) |
| RN-08 | A emissão de certificado pode estar condicionada à confirmação de presença do participante. | *Parâmetro a definir* — pode ser automática ou condicionada |
| RN-09 | A reserva de vaga em evento pago pode ocorrer no início do pagamento ou apenas após sua confirmação. | *Parâmetro a definir* |
| RN-10 | O conjunto de informações dos participantes visível ao palestrante é restrito. | *Parâmetro a definir* — quais dados exatamente |

> Nota: RN-05, RN-06, RN-08 e RN-09 aparecem como regras cuja **existência** é conhecida, mas cujos **critérios** não foram definidos na elicitação. São candidatas naturais a rodadas de refinamento com os stakeholders (equipe financeira e organizadores).
