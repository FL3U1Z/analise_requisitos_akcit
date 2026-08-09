# Dúvidas, Ambiguidades e Lacunas

Sistema de Gestão de Eventos — Empresa Eventus

Este documento reúne os pontos que **ainda precisam ser esclarecidos junto aos stakeholders** antes que os requisitos possam ser especificados de forma completa, consistente e verificável. A maior parte foi levantada explicitamente na seção 4 (Observações) do documento de elicitação; alguns itens adicionais surgiram da análise crítica.

## 1. Cancelamento de inscrição

- Até quando o participante pode cancelar? (prazo-limite — RN-06)
- Quais eventos permitem cancelamento e quais não? Como o organizador define isso? (RN-04)
- O cancelamento libera automaticamente a vaga para a lista de espera?

## 2. Reembolso

- Em quais situações há direito a reembolso e em quais não? (RN-05)
- O reembolso é total ou parcial? Depende da antecedência do cancelamento?
- Quem opera o reembolso — automático pelo sistema ou manual pela equipe financeira?

## 3. Lista de espera

- Como a lista de espera funciona? Ordem de chegada?
- Quando uma vaga é liberada, o próximo da fila é promovido automaticamente ou é apenas notificado com prazo para confirmar?
- Há limite de tamanho para a lista de espera?

## 4. Certificados

- A emissão é automática ou depende de confirmação de presença? (RN-08)
- Como a presença é confirmada (check-in, lista manual, etc.)?
- Há prazo para emissão após o evento?

## 5. Notificações e comprovantes

- Por qual canal os comprovantes e notificações são enviados? (e-mail, app, SMS?)
- O participante pode escolher o canal?
- Há notificações para além do comprovante (lembrete, confirmação de pagamento, promoção na lista de espera)?

## 6. Reserva de vaga x pagamento

- A vaga é reservada quando o participante inicia o pagamento ou apenas após a confirmação? (RN-09)
- Se reservada no início, por quanto tempo fica bloqueada aguardando o pagamento?

## 7. Conflito de horários entre workshops

- Como o sistema deve tratar a tentativa de inscrição em atividades com horários conflitantes? (RN-07)
- Bloqueia, alerta e permite, ou apenas registra?

## 8. Visibilidade de dados para palestrantes

- Quais informações dos participantes o palestrante pode ver? (RN-10)
- Há implicação de privacidade/LGPD nessa exposição? (relaciona-se a RNF-04)

## 9. Requisitos não funcionais não levantados

O documento registra que **não foram levantados** requisitos de segurança, desempenho, disponibilidade, acessibilidade e privacidade. Todos os itens propostos em `requisitos-nao-funcionais.md` precisam ser validados e quantificados (definir valores concretos para torná-los verificáveis).

## 10. Ambiguidades de linguagem

- "Em tempo real" (acompanhamento de inscritos): qual a latência aceitável? Segundos? Minutos?
- "Determinadas inscrições" que exigem confirmação de pagamento: quais exatamente?

---

> Estratégia sugerida: agrupar esses pontos por stakeholder responsável (financeiro → reembolso/pagamento; organizadores → cancelamento/lista de espera/certificados; TI → notificações/privacidade) e levá-los a uma rodada de refinamento antes de fechar a especificação.
