# Clinica+Saúde

## Levantamento Inicial de Requisitos

**Disciplina:** Engenharia de Requisitos  
**Atividade:** Levantamento Inicial de Requisitos  
**Data:** 01/09/2026
**Turma:** Turma A - Engenharia de Software

---

## 1. Identificação do Grupo

| Informação | Preenchimento |
|---|---|
| Turma | Turma A - Engenharia de Software |
| Nome do projeto | Clinica+Saúde |
| Integrante 1 | Pedro Damasceno |
| Integrante 2 | Nathan Andrade |
| Integrante 3 | Breno Cavalcante |
| Integrante 4 | Eduardo Sá |
| Integrante 5 | Rogerio Cruvinel |

---

## 2. Contexto do Projeto

### 2.1 Qual problema o sistema pretende resolver?

Atualmente, o atendimento e o agendamento são realizados de forma fragmentada, com uso de planilhas, telefone, WhatsApp e atendimento presencial.

Isso gera conflitos de agenda, retrabalho, duplicidade e desatualização de informações, falhas de comunicação, dificuldades para controlar cancelamentos e alterações e ausência de lembretes aos pacientes.

### 2.2 Quem é afetado pelo problema?

Pacientes, recepcionistas, médicos, gestão da clínica, direção, equipe administrativa, TI e financeiro.

Também podem ser afetados planos de saúde e órgãos reguladores.

### 2.3 Como esse problema é resolvido atualmente?

O paciente solicita o atendimento por telefone, WhatsApp ou presencialmente.

A recepcionista consulta a disponibilidade em planilhas, registra o horário e confirma com o paciente.

As recepcionistas mantêm registros separados e existe ainda um sistema separado utilizado pelos médicos para o atendimento.

### 2.4 Quais são as principais dificuldades do processo atual?

- Conflitos de horários;
- Retrabalho e duplicidade de informações;
- Dados desatualizados;
- Falhas de comunicação;
- Dificuldade para registrar e controlar cancelamentos e alterações;
- Ausência de lembretes;
- Dificuldade para reorganizar a agenda;
- Dificuldade para acompanhar indicadores.

### 2.5 Qual resultado se espera alcançar com o novo sistema?

Organizar e centralizar as informações de pacientes, médicos, especialidades, consultas e atendimentos.

Além disso, espera-se:

- Reduzir conflitos;
- Reduzir retrabalho;
- Manter a agenda atualizada;
- Facilitar confirmações;
- Enviar lembretes;
- Facilitar cancelamentos;
- Facilitar alterações;
- Permitir o acompanhamento de indicadores.

---

## 3. Identificação dos Stakeholders

| ID | Stakeholder | Necessidade/Interesse | Influência |
|---|---|---|---|
| ST01 | Paciente | Solicita, confirma e realiza consultas sem conflitos e sem repetir dados. | Alta |
| ST02 | Recepcionista | Realiza agendamentos com agilidade, consultando uma agenda centralizada e atualizada. | Alta |
| ST03 | Médico | Precisa de agenda organizada, sem conflitos, e de informações atualizadas. | Alta |
| ST04 | Gestão da clínica | Busca eficiência operacional e acompanhamento do tempo de espera e indicadores. | Média |
| ST05 | Direção | Busca maior ocupação da agenda, redução de faltas e apoio à tomada de decisões. | Média |

### Stakeholder Principal: Paciente

**Por quê?**

Porque é o principal beneficiário do processo de agendamento e atendimento e é diretamente afetado por conflitos, falhas de comunicação, cancelamentos e dificuldades no processo atual.

---

## 4. Perguntas para o Levantamento

| Pergunta | Resposta |
|---|---|
| O que esse usuário precisa fazer? | O paciente precisa solicitar, agendar, confirmar, cancelar ou alterar uma consulta; a recepção precisa cadastrar, consultar disponibilidade e organizar a agenda; o médico precisa consultar sua agenda e registrar o atendimento. |
| Qual problema ele enfrenta atualmente? | Conflitos de agenda, informações duplicadas ou desatualizadas, retrabalho, falhas de comunicação, dificuldade com cancelamentos e alterações e ausência de lembretes. |
| Quais informações ele precisa consultar? | Cadastro do paciente, telefone, CPF, data de nascimento, e-mail, disponibilidade dos médicos, consultas agendadas, cancelamentos, alterações e informações do atendimento. |
| Quais informações ele precisa cadastrar ou alterar? | Dados cadastrais do paciente, informações da consulta, cancelamento ou alteração de horário e informações necessárias ao atendimento. |
| Quais tarefas são repetitivas? | Cadastro e consulta de dados, verificação de disponibilidade, registro de agendamentos, confirmações, cancelamentos e reorganização da agenda. |
| Quais tarefas consomem mais tempo? | Consultar planilhas, localizar dados do paciente, verificar disponibilidade e reorganizar a agenda, especialmente quando há cancelamentos ou alterações. |
| Quais erros acontecem atualmente? | Conflitos de horário, duplicidade de informações, dados desatualizados, falhas de comunicação e erros no controle de cancelamentos. |
| O usuário precisa receber notificações? | Sim. O usuário precisa receber confirmação da consulta, lembretes e avisos quando houver cancelamento ou alteração de horário. |
| O sistema precisará gerar documentos ou relatórios? | Sim. O sistema deverá apoiar relatórios/indicadores como número de consultas, cancelamentos, faltas, tempo médio de atendimento, ocupação da agenda e tempo médio de agendamento. |
| Existem informações que precisam ser protegidas? | Sim. Dados pessoais e informações de atendimento precisam ser protegidos, com controle de acesso, confidencialidade e observância da LGPD. |
| O sistema precisará se comunicar com outro sistema? | Sim. Deve ser considerada a comunicação/integração com o sistema separado utilizado pelos médicos para o atendimento. |
| Existem regras que precisam obrigatoriamente ser respeitadas? | Sim. O paciente deve estar cadastrado para agendar; não pode haver dois pacientes no mesmo horário para o mesmo médico; o agendamento deve ocorrer somente em horários disponíveis; cancelamentos devem liberar o horário. |
| O que faria o usuário considerar a solução satisfatória? | A solução será satisfatória se reduzir conflitos e retrabalho, manter a agenda atualizada, facilitar agendamentos/cancelamentos, enviar confirmações e lembretes e permitir melhor acompanhamento do processo. |

---

## 5. Necessidades Identificadas

| ID | Stakeholder | Necessidade Identificada | Problema Relacionado |
|---|---|---|---|
| N01 | Paciente | Cadastro único do paciente, evitando repetição de dados. | Retrabalho e duplicidade de informações. |
| N02 | Recepcionista | Agenda centralizada e atualizada em tempo real. | Conflitos de agenda e dados desatualizados. |
| N03 | Paciente | Confirmação e lembrete da consulta. | Falhas de confirmação e faltas. |
| N04 | Recepcionista | Registrar cancelamento e liberar o horário. | Dificuldade no controle de cancelamentos. |
| N05 | Médico | Consultar e acompanhar a própria agenda. | Dificuldade para visualizar alterações e organizar horários. |
| N06 | Clínica/Direção | Centralizar pacientes, médicos, consultas e atendimentos. | Informações espalhadas em diferentes meios. |
| N07 | Gestão/Direção | Acompanhar indicadores do processo. | Dificuldade para medir desempenho e ocupação. |
| N08 | TI/Clínica | Proteger dados pessoais e informações de atendimento. | Risco de acesso indevido e necessidade de privacidade. |

---

## 6. Levantamento dos Requisitos Funcionais

**Pergunta-chave:** O que o sistema deve permitir que seus usuários façam?

| ID | Requisito Funcional | Stakeholder/Fonte | Necessidade Relacionada | Prioridade |
|---|---|---|---|---|
| RF01 | O sistema deve permitir cadastrar pacientes com seus dados de identificação e contato. | Paciente/Recepcionista | N01 | Alta |
| RF02 | O sistema deve permitir consultar e localizar o cadastro do paciente. | Paciente/Recepcionista | N01 | Alta |
| RF03 | O sistema deve permitir cadastrar médicos e suas informações profissionais. | Recepcionista/Gestão | N06 | Média |
| RF04 | O sistema deve permitir cadastrar e consultar especialidades. | Recepcionista/Gestão | N06 | Média |
| RF05 | O sistema deve permitir consultar os horários disponíveis por médico. | Recepcionista/Médico | N02/N05 | Alta |
| RF06 | O sistema deve permitir realizar agendamento somente em horários disponíveis. | Paciente/Recepcionista | N02 | Alta |
| RF07 | O sistema deve permitir cancelar uma consulta e liberar o horário correspondente. | Paciente/Recepcionista | N04 | Alta |
| RF08 | O sistema deve enviar confirmação e lembrete da consulta ao paciente. | Paciente/Recepcionista | N03 | Alta |

**Total: 8 Requisitos Funcionais**

---

## 7. Levantamento dos Requisitos de Qualidade

**Pergunta-chave:** Além de funcionar, quais características o sistema precisa apresentar para ser considerado adequado pelos stakeholders?

| ID | Característica de Qualidade | Requisito Mensurável | Como Verificar? |
|---|---|---|---|
| RQ01 | Desempenho | O sistema deve apresentar a disponibilidade de horários em até 3 segundos em pelo menos 95% das consultas. | Teste de tempo de resposta. |
| RQ02 | Segurança | O sistema deve exigir autenticação para acesso a dados administrativos e informações protegidas. | Testar acesso sem autenticação e com perfis autorizados. |
| RQ03 | Usabilidade/Interação | O usuário deve conseguir consultar a agenda em no máximo 4 etapas após entrar na função de agendamento. | Teste de usabilidade com usuários. |
| RQ04 | Confiabilidade | O sistema deve impedir a confirmação de dois agendamentos para o mesmo médico e horário. | Teste com tentativas simultâneas de agendamento. |
| RQ05 | Compatibilidade/Portabilidade | O sistema deve funcionar nas versões suportadas dos navegadores Chrome, Edge e Firefox. | Executar testes nos três navegadores. |

**Total: 5 Requisitos de Qualidade**

---

## 8. Levantamento das Restrições

| ID | Restrição | Categoria | Justificativa/Fonte |
|---|---|---|---|
| RES01 | Os dados pessoais e informações de atendimento devem ser tratados de acordo com os requisitos legais aplicáveis, incluindo a LGPD. | Legal | Necessidade de proteção, confidencialidade e privacidade dos dados dos pacientes. |
| RES02 | O projeto deve considerar a existência do sistema separado utilizado pelos médicos para o atendimento. | Processo | O processo atual utiliza um sistema distinto para registrar o atendimento médico. |
| RES03 | A solução deve considerar os recursos e procedimentos já utilizados pela clínica, como computadores, telefone, WhatsApp e atendimento presencial. | Processo/Outra | Esses recursos fazem parte do processo atual e não podem ser simplesmente desconsiderados. |

**Total: 3 Restrições**

---

## 9. Regras de Negócio Identificadas

| ID | Regra de Negócio | Fonte |
|---|---|---|
| RN01 | O paciente deve estar cadastrado para realizar um agendamento. | Processo atual / grupo |
| RN02 | Não podem existir dois pacientes agendados para o mesmo médico no mesmo horário. | Regra do processo |
| RN03 | O agendamento somente pode ser realizado quando houver horário disponível para o médico. | Regra do processo |

**Total: 3 Regras de Negócio**

---

## 10. Matriz Consolidada de Requisitos

| ID | Descrição | Tipo | Stakeholder/Fonte | Prioridade |
|---|---|---|---|---|
| RF01 | Permitir cadastro de pacientes. | Funcional | Paciente/Recepcionista | Alta |
| RF05 | Permitir consulta dos horários disponíveis por médico. | Funcional | Recepcionista/Médico | Alta |
| RF06 | Permitir agendamento somente em horários disponíveis. | Funcional | Paciente/Recepcionista | Alta |
| RF07 | Permitir cancelamento e liberação do horário. | Funcional | Paciente/Recepcionista | Alta |
| RF08 | Enviar confirmação e lembrete da consulta. | Funcional | Paciente/Recepcionista | Alta |
| RQ01 | Disponibilidade apresentada em até 3 segundos em 95% das consultas. | Qualidade | Recepcionista | Alta |
| RQ02 | Exigir autenticação para dados protegidos. | Qualidade | TI/Clínica | Alta |
| RQ04 | Impedir dois agendamentos para o mesmo médico e horário. | Qualidade | Recepcionista/Médico | Alta |
| RES01 | Cumprir requisitos legais de proteção de dados, incluindo LGPD. | Restrição | TI/Clínica | Alta |
| RES02 | Considerar o sistema separado utilizado pelos médicos. | Restrição | Clínica/IT | Média |

---

## 11. Revisão por Pares - Caça à Ambiguidade

Durante a revisão, devem ser identificados termos vagos, como:

- Rápido;
- Amigável;
- Adequado;
- Melhor;
- Robusto;
- Muitos;
- Poucos;
- Quando possível;
- Se necessário.

| ID | Problema Encontrado | Sugestão do Grupo Revisor |
|---|---|---|
| - | A revisão por pares não foi registrada no material fornecido. | - |

---

## 12. Checklist de Qualidade

| Pergunta | Sim | Não | Observação |
|---|:---:|:---:|---|
| O requisito está completo? | ☑ | ☐ | Os requisitos foram descritos com a capacidade ou característica esperada. |
| Está correto em relação à necessidade do stakeholder? | ☑ | ☐ | Os requisitos foram relacionados às necessidades e aos stakeholders. |
| Descreve apenas uma capacidade ou característica? | ☑ | ☐ | Cada requisito descreve uma capacidade ou característica principal. |
| É necessário? | ☑ | ☐ | Os requisitos tratam dos problemas identificados no processo atual. |
| É viável? | ☑ | ☐ | Os requisitos são compatíveis com o contexto apresentado. |
| Possui prioridade? | ☑ | ☐ | Os requisitos funcionais possuem prioridade definida. |
| Está livre de ambiguidades? | ☑ | ☐ | Foram evitados termos vagos nos requisitos mensuráveis. |
| Pode ser verificado ou testado? | ☑ | ☐ | Os requisitos de qualidade possuem forma de verificação. |
| A fonte/stakeholder está identificada? | ☑ | ☐ | A fonte/stakeholder foi indicada. |

---

## 13. Entrega da Etapa - 31/08

Ao final da aula, o grupo deverá ter produzido:

- 8 requisitos funcionais (RF);
- 5 requisitos de qualidade (RQ);
- 3 restrições (RES);
- 3 regras de negócio (RN).

Todos devem estar associados às necessidades e aos stakeholders identificados.

---

## 14. Reflexão Final do Grupo

### Qual requisito gerou mais discussão durante o levantamento e por quê?

Não há registro, no material fornecido, de qual requisito gerou mais discussão. Por isso, não é possível afirmar qual foi sem inventar informação.

### Qual necessidade do usuário inicialmente parecia simples, mas gerou vários requisitos?

A necessidade de organizar o agendamento e a agenda parecia simples, mas envolve:

- Cadastro do paciente;
- Consulta de disponibilidade;
- Agendamento;
- Confirmação;
- Lembretes;
- Cancelamentos;
- Alterações;
- Atualização da agenda.

### O grupo identificou algum requisito implícito que somente apareceu durante a discussão? Qual?

O material identifica a necessidade de proteger dados pessoais e informações de atendimento, mas não registra se esse requisito surgiu somente durante a discussão.

---

## Conclusão

O levantamento permitiu identificar os principais problemas relacionados ao processo atual de atendimento e agendamento da clínica, transformando essas necessidades em requisitos funcionais, requisitos de qualidade, restrições e regras de negócio.

O projeto **Clinica+Saúde** busca organizar e centralizar as informações relacionadas a pacientes, médicos, consultas e atendimentos, contribuindo para a redução de conflitos de agenda, retrabalho, duplicidade de informações e falhas de comunicação.

> **Observação:** nesta etapa, o foco não é projetar telas nem escolher tecnologias. O objetivo é compreender e registrar o que é necessário para resolver o problema, mantendo os requisitos claros, verificáveis e rastreáveis às necessidades dos stakeholders.

---

**Engenharia de Requisitos | Atividade em Grupo | 31/08**

**Projeto:** Clinica+Saúde  
**Turma:** Turma A - Engenharia de Software
