# Caso de Uso: Inscrever-se em Evento

Sistema de Gestão de Eventos — Empresa Eventus

Este é o fluxo mais complexo do sistema — envolve controle de vagas, lista de espera e, para eventos pagos, confirmação de pagamento. Por reunir múltiplos fluxos alternativos, foi documentado como caso de uso (formato da Unidade III), complementando a história de usuário HU-02.

| Campo | Descrição |
|-------|-----------|
| **Nome** | Inscrever-se em evento |
| **Objetivo** | Permitir que o participante se inscreva em um evento, tratando disponibilidade de vagas e pagamento quando aplicável |
| **Ator principal** | Participante |
| **Atores secundários** | Equipe Financeira (na confirmação de pagamento) |
| **Pré-condição** | O participante está autenticado e o evento está disponível para inscrição |
| **Fluxo principal** | 1. O participante acessa a lista de eventos disponíveis.<br>2. O participante seleciona um evento e solicita a inscrição.<br>3. O sistema verifica se há vagas disponíveis.<br>4. O sistema verifica se o evento é gratuito ou pago.<br>5. (Evento gratuito) O sistema confirma a inscrição e decrementa uma vaga.<br>6. O sistema emite o comprovante de inscrição.<br>7. O sistema disponibiliza o comprovante ao participante. |
| **Fluxo alternativo A — Evento pago** | No passo 4, se o evento for pago e exigir confirmação de pagamento: o sistema registra a inscrição como *pendente de pagamento*, aguarda a confirmação (equipe financeira / meio de pagamento) e só então confirma a inscrição e emite o comprovante. |
| **Fluxo alternativo B — Sem vagas** | No passo 3, se não houver vagas, o sistema oferece ao participante a entrada na lista de espera; se aceito, registra sua posição e o notifica caso uma vaga seja liberada. |
| **Fluxo alternativo C — Conflito de horário** | Se o item for um workshop com horário conflitante com outra inscrição do participante, o sistema impede a inscrição e informa o conflito. *(Regra a confirmar — ver lacuna 7.)* |
| **Pós-condição** | A inscrição fica registrada com status adequado (confirmada, pendente de pagamento ou em lista de espera) e o comprovante é disponibilizado quando confirmada |

> Pontos deste caso de uso que dependem de definição em aberto: momento da reserva da vaga em eventos pagos (lacuna 6), tratamento de conflito de horário (lacuna 7) e regras da lista de espera (lacuna 3).
