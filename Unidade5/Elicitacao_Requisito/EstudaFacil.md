# ELICITAÇÃO DE REQUISITOS — SISTEMA DE APRENDIZAGEM DE UML

## 1. Stakeholders e Usuários

| Stakeholder | Descrição |
|---|---|
| Aluno | Utiliza o sistema para estudar UML, realizar exercícios e acompanhar seu progresso. |
| Professor | Utiliza os conteúdos da plataforma como apoio ao ensino de UML. |
| Administrador | Responsável pela organização e manutenção dos conteúdos e funcionalidades do sistema. |

## 2. Técnicas de Elicitação

Foram consideradas as seguintes técnicas para identificar as necessidades do sistema:

- **Análise de documentos:** análise das informações e funcionalidades descritas no projeto.
- **Entrevista:** levantamento de perguntas sobre as dificuldades dos alunos no aprendizado de UML.
- **Brainstorming:** identificação de funcionalidades que podem facilitar o aprendizado.

## 3. Requisitos Funcionais

| ID | Requisito |
|---|---|
| RF01 | Permitir que o aluno realize seu cadastro. |
| RF02 | Permitir que o aluno realize login. |
| RF03 | Permitir selecionar um tema de estudo. |
| RF04 | Disponibilizar conteúdos teóricos sobre UML. |
| RF05 | Permitir visualizar exemplos dos conteúdos. |
| RF06 | Permitir realizar exercícios sobre UML. |
| RF07 | Apresentar o resultado dos exercícios após sua conclusão. |
| RF08 | Permitir acompanhar o progresso nos estudos. |
| RF09 | Disponibilizar um modo de treino sem avaliação. |
| RF10 | Permitir configurar os recursos de acessibilidade. |
| RF11 | Permitir ativar ou desativar a narração dos conteúdos. |
| RF12 | Permitir ativar ou desativar os sons do sistema. |

## 4. Requisitos Não Funcionais

| ID | Requisito |
|---|---|
| RNF01 | O sistema deverá possuir uma interface simples e intuitiva. |
| RNF02 | Deverá permitir a navegação por teclado. |
| RNF03 | Deverá disponibilizar opções de contraste visual. |
| RNF04 | Deverá permitir a narração de textos e questões. |
| RNF05 | Não deverá estabelecer limite de tempo para a realização dos exercícios. |
| RNF06 | Deverá proteger as informações pessoais dos usuários. |
| RNF07 | Deverá apresentar os conteúdos de maneira organizada e compreensível. |
| RNF08 | Deverá funcionar adequadamente em navegadores modernos. |

## 5. Regras de Negócio

| ID | Regra |
|---|---|
| RN01 | O aluno deverá selecionar um tema antes de iniciar uma atividade. |
| RN02 | O aluno deverá responder ao exercício atual antes de avançar para o próximo. |
| RN03 | O resultado deverá ser apresentado após a conclusão da atividade. |
| RN04 | O progresso deverá ser atualizado após a realização dos exercícios. |
| RN05 | O modo de treino deverá permitir a prática sem avaliação formal. |
| RN06 | O aluno poderá realizar as atividades no próprio ritmo. |
| RN07 | Os recursos de acessibilidade poderão ser configurados conforme a necessidade do usuário. |

## 6. Requisitos de Acessibilidade

- Narração dos conteúdos textuais e questões por voz.
- Navegação por teclado, sem dependência do mouse.
- Controle para ativar ou desativar sons e narração.
- Opções de contraste visual.
- Ausência de limite de tempo para responder às atividades.

## 7. Priorização dos Requisitos — MoSCoW

| Prioridade | Requisitos |
|---|---|
| Must Have | RF01, RF02, RF03, RF04, RF06, RF07 |
| Should Have | RF05, RF08, RF09, RF10 |
| Could Have | RF11, RF12 |
| Won't Have | Funcionalidades que não fazem parte do escopo atual do projeto. |

## 8. Validação dos Requisitos

- Os requisitos devem ser claros e compreensíveis.
- Cada requisito funcional deverá possuir correspondência com um caso de uso.
- As regras de negócio deverão ser respeitadas durante a utilização do sistema.
- Os resultados dos exercícios deverão ser apresentados corretamente.
- O progresso do aluno deverá ser atualizado após a realização das atividades.
- Os recursos de acessibilidade deverão funcionar conforme especificado.

## 9. Resultado da Elicitação

A elicitação identificou as principais funcionalidades do Sistema de Aprendizagem de UML, incluindo cadastro, login, seleção de temas, consulta de conteúdos, exercícios, acompanhamento do progresso e recursos de acessibilidade.

Os requisitos levantados servirão como base para a construção do Diagrama de Casos de Uso e para o desenvolvimento das funcionalidades do sistema.
