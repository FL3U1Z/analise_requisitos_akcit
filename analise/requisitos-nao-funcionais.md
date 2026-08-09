# Requisitos Não Funcionais

Sistema de Gestão de Eventos — Empresa Eventus

O documento de elicitação registra explicitamente (seção 4, Observações) que **não foram levantados requisitos relacionados a segurança, desempenho, disponibilidade, acessibilidade e privacidade dos dados**. Portanto, os requisitos abaixo são em sua maioria **propostos** a partir de necessidades implícitas típicas desse domínio, e precisam ser validados junto aos stakeholders antes de serem incorporados à especificação.

O identificador segue o padrão `RNF-XX`. A categoria segue as classes de qualidade discutidas na Unidade I (desempenho, segurança, confiabilidade, disponibilidade, usabilidade, escalabilidade, conformidade).

| ID | Categoria | Requisito | Origem |
|----|-----------|-----------|--------|
| RNF-01 | Desempenho | A contagem de inscritos exibida ao organizador deve refletir o estado real em tempo quase real (atualização em até poucos segundos), já que há a necessidade explícita de acompanhar inscrições "em tempo real". | Derivado de fala do organizador |
| RNF-02 | Confiabilidade / Concorrência | O controle de vagas deve impedir que o número de inscrições confirmadas ultrapasse o limite do evento, mesmo sob inscrições simultâneas. | Implícito no controle automático de vagas |
| RNF-03 | Segurança | O acesso às funcionalidades deve exigir autenticação, e cada perfil (participante, organizador, financeiro, palestrante, TI) deve ter acesso apenas às informações e ações pertinentes. | Implícito (perfis distintos) |
| RNF-04 | Privacidade | O tratamento dos dados pessoais dos participantes deve estar em conformidade com a legislação aplicável (ex.: LGPD), especialmente quanto ao que é exposto a palestrantes. | Implícito / regulatório |
| RNF-05 | Disponibilidade | O sistema deve permanecer disponível durante os períodos de inscrição, evitando indisponibilidade em picos de acesso próximos à abertura de eventos concorridos. | Implícito |
| RNF-06 | Usabilidade | A visualização de todos os eventos em um único lugar e o fluxo de inscrição devem ser simples e diretos, minimizando etapas para o participante. | Derivado de fala do participante |
| RNF-07 | Confiabilidade | A emissão de certificados e comprovantes deve ser consistente: um comprovante/certificado emitido deve corresponder a uma inscrição/participação válida. | Implícito |
| RNF-08 | Escalabilidade | O sistema deve suportar o crescimento do número de eventos e de participantes, motivador declarado do próprio projeto. | Contexto do projeto |

> Nota de análise: nenhum valor numérico (tempo de resposta exato, percentual de disponibilidade, etc.) foi fornecido na elicitação. Os limites concretos precisam ser negociados com os stakeholders para que estes requisitos se tornem **verificáveis**, conforme as características de qualidade da Unidade III.
