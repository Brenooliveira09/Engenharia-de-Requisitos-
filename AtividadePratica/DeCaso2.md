# 10. Regras de Negócio

| Código | Regra de Negócio | Origem |
|---|---|---|
| RN01 | O paciente precisa estar cadastrado para poder realizar um agendamento. | Processo atual |
| RN02 | Não pode haver dois pacientes marcados para o mesmo médico no mesmo horário. | Problema de conflito de horários |
| RN03 | O agendamento só pode ser feito quando houver horário disponível na agenda do médico. | Processo atual |
| RN04 | Quando uma consulta for cancelada, o horário deve ficar disponível novamente. | Processo de cancelamento |
| RN05 | O paciente deve receber uma confirmação após o agendamento da consulta. | Necessidade da clínica |
| RN06 | O sistema deve enviar um lembrete ao paciente antes da consulta. | Problema com faltas |
| RN07 | Os dados do paciente devem ser armazenados em um cadastro único, evitando que ele precise informar os mesmos dados várias vezes. | Problema de retrabalho |
| RN08 | Quando houver alteração na agenda do médico, os pacientes afetados devem ser avisados. | Problema de alteração de agenda |
| RN09 | Somente horários disponíveis na agenda podem ser escolhidos para novos agendamentos. | Controle da agenda |
| RN10 | O atendimento realizado deve ser registrado após a consulta. | Processo atual |
| RN11 | O sistema deve registrar cancelamentos e faltas para que a clínica possa acompanhar esses dados. | Necessidade de indicadores |
| RN12 | A agenda do médico deve ser atualizada sempre que houver um novo agendamento, cancelamento ou alteração. | Problema de informações desatualizadas |

---

# ETAPA 11 – IDENTIFICAÇÃO DOS PROBLEMAS

A análise do processo atual da **Clínica Vida+ Saúde** permitiu identificar diversos problemas relacionados principalmente à utilização de ferramentas separadas e à dependência de atividades manuais.

Esses problemas geram retrabalho, falhas de comunicação e dificuldades no gerenciamento dos agendamentos.

| Problema | Causa provável | Impacto | Prioridade |
|---|---|---|---|
| **1. Conflitos de horários** | As recepcionistas utilizam registros próprios e as informações nem sempre são atualizadas imediatamente. | Dois pacientes podem ser agendados para o mesmo horário, causando conflitos na agenda. | 🔴 Alta |
| **2. Retrabalho no cadastro dos pacientes** | Pacientes que já possuem cadastro precisam fornecer novamente seus dados pessoais. | Aumenta o tempo de atendimento e reduz a produtividade da recepção. | 🔴 Alta |
| **3. Duplicidade de informações** | Cada recepcionista mantém seus próprios registros em diferentes planilhas. | Pode gerar informações inconsistentes e dificultar a localização dos dados corretos. | 🔴 Alta |
| **4. Falhas na confirmação dos agendamentos** | A confirmação pode ser enviada pelo WhatsApp, mas o registro pode não aparecer na planilha utilizada pela recepcionista. | O paciente pode comparecer à clínica sem que seu agendamento seja localizado. | 🔴 Alta |
| **5. Ausência de lembretes automáticos** | Atualmente não existe um mecanismo automático para lembrar os pacientes das consultas. | Pode aumentar a quantidade de pacientes que não comparecem às consultas. | 🟡 Média |
| **6. Dificuldade no gerenciamento de cancelamentos** | Quando ocorre um cancelamento, a recepcionista precisa verificar a agenda e procurar manualmente outro paciente. | Horários podem permanecer vagos e há maior gasto de tempo da equipe. | 🟡 Média |
| **7. Dificuldade na alteração da agenda médica** | Quando o médico altera sua agenda, a recepcionista precisa entrar em contato individualmente com os pacientes afetados. | Processo demorado e sujeito a falhas de comunicação. | 🟡 Média |
| **8. Informações do atendimento armazenadas separadamente** | Após a consulta, o médico registra as informações em um sistema diferente. | As informações ficam fragmentadas, dificultando o acesso e o gerenciamento dos dados. | 🟡 Média |

---

## Fluxograma do Processo

```mermaid
graph TD
    A([Início: Paciente solicita consulta]) --> B[Recepcionista busca cadastro do paciente]
    B --> C{Possui cadastro?}
    
    C -- Não --> D[Cadastrar dados do paciente]
    D --> E[Verificar disponibilidade de agenda]
    C -- Sim --> E
    
    E --> F{Horário disponível?}
    F -- Não --> G[Oferecer novos horários]
    G --> H{Paciente aceita?}
    H -- Não --> I([Fim: Agendamento não realizado])
    H -- Sim --> E
    
    F -- Sim --> J{Atendimento por Convênio?}
    J -- Sim --> K[Validar elegibilidade com Plano de Saúde]
    K --> L{Autorizado?}
    L -- Não --> M[Informar paciente / Solicitar pagamento particular]
    M --> N{Aceita pagamento?}
    N -- Não --> I
    N -- Sim --> O[Confirmar Agendamento]
    L -- Sim --> O
    J -- Não --> O
    
    O --> P[Paciente comparece na data agendada]
    P --> Q[Médico realiza a consulta e atualiza prontuário]
    Q --> R([Fim: Consulta realizada e faturamento gerado])

    | Problema                                             | Melhoria proposta                                                                                       | Benefício esperado                                                                        |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| **Conflito de horários**                             | Criar uma agenda única e atualizada para todos os atendentes.                                           | Evitar que dois pacientes sejam marcados no mesmo horário.                                |
| **Cadastro duplicado**                               | Utilizar um cadastro único de pacientes.                                                                | Diminuir o retrabalho e facilitar o atendimento.                                          |
| **Falta de lembretes**                               | Enviar lembretes automáticos pelo sistema, como por WhatsApp ou outro canal disponível.                 | Reduzir o número de pacientes que esquecem da consulta.                                   |
| **Confirmações que não aparecem na agenda**          | Registrar o agendamento diretamente no sistema no momento da confirmação.                               | Evitar divergência entre o que foi informado ao paciente e o que aparece para a recepção. |
| **Cancelamentos feitos manualmente**                 | Permitir que o cancelamento seja registrado diretamente no sistema e liberar o horário automaticamente. | Facilitar o controle da agenda e permitir o reaproveitamento do horário.                  |
| **Alteração na agenda do médico**                    | Criar uma função para alterar a agenda e avisar automaticamente os pacientes afetados.                  | Diminuir o trabalho da recepção e melhorar a comunicação.                                 |
| **Dificuldade para acompanhar os dados**             | Criar uma área com indicadores do processo.                                                             | Facilitar o acompanhamento dos resultados da clínica.                                     |
| **Informações espalhadas em diferentes ferramentas** | Centralizar pacientes, médicos, especialidades, consultas e atendimentos em um único sistema.           | Melhorar a organização e facilitar o acesso às informações.                               |
| **Muitos pacientes faltando**                        | Enviar lembretes e permitir confirmação antecipada da consulta.                                         | Diminuir a quantidade de faltas.                                                          |
| **Dificuldade para encontrar horários**              | Disponibilizar uma consulta de horários livres por médico e especialidade.                              | Tornar o agendamento mais rápido e facilitar o trabalho da recepcionista.                 |
