## PROJETO ESTUDAFÁCIL

## Etapa 1 — Leitura e Identificação dos Requisitos

### 1. Qual é o objetivo principal do sistema?

O objetivo principal do EstudaFácil é **auxiliar estudantes da área de Tecnologia da Informação (TI) em sua rotina acadêmica e no aprendizado das disciplinas do curso**, reunindo em um único ambiente conteúdos, materiais de estudo, atividades, exercícios e recursos para organização e acompanhamento do desempenho. A plataforma busca facilitar o acesso ao conhecimento e ajudar os estudantes a organizar seus estudos.

### 2. Quem interage diretamente com o sistema?

O sistema possui três atores principais:

- **Aluno:** utiliza a plataforma para estudar conteúdos de TI, consultar materiais, realizar atividades e acompanhar seu progresso.
- **Professor:** possui acesso próprio para registrar, organizar e administrar conteúdos e atividades disponibilizados aos alunos.
- **Administrador:** gerencia a plataforma, os usuários, as permissões e o funcionamento geral do aplicativo.

Cada ator possui permissões específicas. O aluno não pode executar funções exclusivas dos professores ou do administrador.

### 3. Quais funcionalidades são oferecidas ao aluno?

O sistema disponibiliza ao aluno:

- Cadastro e acesso à conta;
- Acesso a conteúdos de diferentes disciplinas de TI;
- Seleção de temas de estudo;
- Consulta de materiais, conceitos e exemplos;
- Realização de exercícios e atividades;
- Visualização dos resultados;
- Acompanhamento do progresso acadêmico;
- Acesso ao modo de treino;
- Configuração das opções de acessibilidade;
- Controle de áudio e narração dos conteúdos.

### 4. Quais funcionalidades são oferecidas aos professores?

Os professores possuem acesso específico para:

- Realizar login na plataforma;
- Registrar conteúdos e materiais de estudo;
- Organizar conteúdos por disciplina ou tema;
- Criar e cadastrar exercícios e atividades;
- Editar ou atualizar materiais e atividades cadastrados;
- Consultar informações sobre o desempenho dos alunos, conforme as permissões do sistema.

### 5. Quais funcionalidades são oferecidas ao administrador?

O administrador é responsável pelo gerenciamento geral da plataforma e pode:

- Realizar login administrativo;
- Gerenciar contas de usuários;
- Cadastrar, editar ou desativar perfis de professores;
- Gerenciar permissões de acesso;
- Administrar conteúdos e atividades;
- Acompanhar o funcionamento geral do aplicativo.

### 6. Quais regras condicionam o acesso às funcionalidades?

O sistema possui regras específicas, como:

- Cada usuário deve acessar as funcionalidades correspondentes ao seu perfil;
- O aluno precisa selecionar um tema ou conteúdo antes de iniciar determinadas atividades;
- O aluno deve responder às questões antes de avançar, quando a atividade exigir;
- O resultado é apresentado após a conclusão da atividade;
- O progresso do aluno é atualizado após a realização dos exercícios;
- Somente professores autorizados podem registrar ou editar conteúdos e atividades;
- Somente o administrador pode executar funções administrativas e alterar permissões de usuários.

### 7. Quais funcionalidades contribuem para a acessibilidade?

O sistema possui recursos como:

- **Narração de conteúdo textual:** leitura dos textos e questões por voz;
- **Navegação por teclado:** permite utilizar o sistema sem depender do mouse;
- **Controle de áudio:** permite ativar ou desativar sons e narração;
- **Contraste visual:** facilita a visualização dos elementos da interface;
- **Ausência de limite de tempo:** permite que o aluno responda às atividades no seu próprio ritmo.

---

# Elementos Identificados

| Elemento Identificado | Evidência / Descrição | Classificação |
|---|---|---|
| Aluno | Usuário que utiliza a plataforma para estudar conteúdos de TI | Ator |
| Professor | Usuário autorizado a registrar e gerenciar conteúdos e atividades | Ator |
| Administrador | Usuário responsável pelo gerenciamento da plataforma e das permissões | Ator |
| Cadastrar-se | Permite ao aluno criar uma conta | Requisito Funcional |
| Realizar Login | Permite acessar a conta conforme o perfil | Requisito Funcional |
| Consultar Conteúdo | Permite acessar materiais de diferentes disciplinas de TI | Requisito Funcional |
| Selecionar Tema | Permite escolher o assunto que deseja estudar | Requisito Funcional |
| Visualizar Exemplos | Permite consultar exemplos relacionados ao conteúdo | Requisito Funcional |
| Realizar Exercício | Permite responder questões e atividades | Requisito Funcional |
| Visualizar Resultado | Apresenta o desempenho após a atividade | Requisito Funcional |
| Acompanhar Progresso | Permite visualizar o progresso nos estudos | Requisito Funcional |
| Acessar Modo Treino | Permite praticar os conteúdos | Requisito Funcional |
| Registrar Conteúdo | Permite ao professor cadastrar materiais de estudo | Requisito Funcional |
| Gerenciar Conteúdo | Permite ao professor editar ou atualizar materiais | Requisito Funcional |
| Cadastrar Atividade | Permite ao professor criar exercícios e atividades | Requisito Funcional |
| Gerenciar Usuários | Permite ao administrador administrar contas | Requisito Funcional |
| Gerenciar Professores | Permite ao administrador cadastrar ou desativar professores | Requisito Funcional |
| Gerenciar Permissões | Permite ao administrador controlar os acessos | Requisito Funcional |
| Configurar Acessibilidade | Permite configurar recursos de acessibilidade | Requisito de Acessibilidade |
| Ativar/Desativar Narração | Permite controlar a leitura por voz | Requisito de Acessibilidade |
| Ativar/Desativar Áudio | Permite controlar sons do sistema | Requisito de Acessibilidade |
| Navegar por Teclado | Permite utilizar as funcionalidades sem mouse | Requisito de Acessibilidade |
| Sem Limite de Tempo | Não exige tempo máximo para responder exercícios | Requisito de Acessibilidade |

---

# Etapa 2 — Construção do Diagrama de Casos de Uso

## Estrutura do Diagrama

### Fronteira do Sistema

A fronteira representa o **EstudaFácil — Plataforma de Apoio ao Aprendizado de Estudantes de TI**.

### Atores

Os três atores ficam localizados fora da fronteira do sistema:

- **Aluno:** acessa conteúdos, realiza exercícios e acompanha seu aprendizado.
- **Professor:** registra e gerencia conteúdos e atividades.
- **Administrador:** gerencia usuários, professores, permissões e aspectos gerais da plataforma.

---

# Casos de Uso e Relacionamentos

## Funcionalidades do Aluno

### 1. Cadastrar-se
- Associação direta com o Aluno.
- Permite criar uma conta para utilizar a plataforma.

### 2. Realizar Login
- Associação com Aluno, Professor e Administrador, cada um acessando seu perfil autorizado.
- Permite acessar as funcionalidades correspondentes ao papel do usuário.

### 3. Selecionar Tema
- Associação direta com o Aluno.
- Permite escolher o assunto ou disciplina de TI que deseja estudar.

### 4. Consultar Conteúdo
- Associação direta com o Aluno.
- Permite acessar materiais e explicações relacionados ao tema escolhido.

### 5. Visualizar Exemplos
- Associação direta com o Aluno.
- Permite consultar exemplos que auxiliam na compreensão do conteúdo.

### 6. Realizar Exercício
- Associação direta com o Aluno.
- Permite responder questões e atividades disponibilizadas na plataforma.

### 7. Visualizar Resultado
- Associação direta com o Aluno.
- Apresenta o desempenho após a conclusão dos exercícios.

### 8. Acompanhar Progresso
- Associação direta com o Aluno.
- Permite consultar seu histórico e evolução nos estudos.

### 9. Acessar Modo Treino
- Associação direta com o Aluno.
- Permite praticar conteúdos e exercícios.

### 10. Configurar Acessibilidade
- Associação direta com o Aluno.
- Permite configurar os recursos de acessibilidade disponíveis.

## Funcionalidades do Professor

### 11. Registrar Conteúdo
- Associação direta com o Professor.
- Permite cadastrar materiais de estudo relacionados às disciplinas de TI.

### 12. Gerenciar Conteúdo
- Associação direta com o Professor.
- Permite editar, atualizar ou organizar conteúdos cadastrados.

### 13. Cadastrar Atividade
- Associação direta com o Professor.
- Permite criar e disponibilizar exercícios e atividades para os alunos.

### 14. Gerenciar Atividades
- Associação direta com o Professor.
- Permite editar ou atualizar atividades que cadastrou.

### 15. Consultar Desempenho dos Alunos
- Associação direta com o Professor, respeitando as permissões estabelecidas.
- Permite acompanhar informações de desempenho relacionadas às atividades.

## Funcionalidades do Administrador

### 16. Gerenciar Usuários
- Associação direta com o Administrador.
- Permite administrar as contas cadastradas na plataforma.

### 17. Gerenciar Professores
- Associação direta com o Administrador.
- Permite cadastrar, editar ou desativar perfis de professores.

### 18. Gerenciar Permissões
- Associação direta com o Administrador.
- Permite definir quais funcionalidades cada perfil pode acessar.

### 19. Administrar Plataforma
- Associação direta com o Administrador.
- Permite gerenciar aspectos gerais do funcionamento do aplicativo.

## Recursos de Acessibilidade

### 20. Ativar/Desativar Narração
- Pode ser representado como uma extensão de Configurar Acessibilidade.
- Permite ativar ou desativar a leitura dos conteúdos por voz.

### 21. Ativar/Desativar Áudio
- Pode ser representado como uma extensão de Configurar Acessibilidade.
- Permite controlar os sons do sistema.

---

# Relacionamentos UML

A estrutura abaixo é uma representação textual simplificada dos atores e de suas funcionalidades. No diagrama UML real, os atores ficam fora do retângulo do sistema e os casos de uso são representados por elipses.

```text
                 ESTUDAFÁCIL — PLATAFORMA DE APOIO AO APRENDIZADO EM TI

ALUNO  ── Cadastrar-se
       ── Realizar Login
       ── Selecionar Tema
       ── Consultar Conteúdo
       ── Visualizar Exemplos
       ── Realizar Exercício
       ── Visualizar Resultado
       ── Acompanhar Progresso
       ── Acessar Modo Treino
       ── Configurar Acessibilidade

PROFESSOR ── Realizar Login
          ── Registrar Conteúdo
          ── Gerenciar Conteúdo
          ── Cadastrar Atividade
          ── Gerenciar Atividades
          ── Consultar Desempenho dos Alunos

ADMINISTRADOR ── Realizar Login
              ── Gerenciar Usuários
              ── Gerenciar Professores
              ── Gerenciar Permissões
              ── Administrar Plataforma
```

---

# Etapa 3 — Matriz de Rastreabilidade

| ID | Requisito Funcional | Caso de Uso | No Diagrama? |
|---|---|---|---|
| RF01 | Permitir ao aluno criar uma conta | Cadastrar-se | Sim |
| RF02 | Permitir que os usuários acessem suas contas conforme o perfil | Realizar Login | Sim |
| RF03 | Permitir ao aluno escolher um tema de estudo | Selecionar Tema | Sim |
| RF04 | Permitir consultar conteúdos de diferentes disciplinas de TI | Consultar Conteúdo | Sim |
| RF05 | Permitir visualizar exemplos dos conteúdos | Visualizar Exemplos | Sim |
| RF06 | Permitir realizar exercícios e atividades | Realizar Exercício | Sim |
| RF07 | Apresentar o resultado dos exercícios | Visualizar Resultado | Sim |
| RF08 | Permitir acompanhar o progresso acadêmico | Acompanhar Progresso | Sim |
| RF09 | Permitir acessar o modo de treino | Acessar Modo Treino | Sim |
| RF10 | Permitir configurar recursos de acessibilidade | Configurar Acessibilidade | Sim |
| RF11 | Permitir ao professor registrar conteúdos | Registrar Conteúdo | Sim |
| RF12 | Permitir ao professor editar e organizar conteúdos | Gerenciar Conteúdo | Sim |
| RF13 | Permitir ao professor criar atividades | Cadastrar Atividade | Sim |
| RF14 | Permitir ao professor gerenciar atividades cadastradas | Gerenciar Atividades | Sim |
| RF15 | Permitir ao professor consultar o desempenho dos alunos | Consultar Desempenho dos Alunos | Sim |
| RF16 | Permitir ao administrador gerenciar usuários | Gerenciar Usuários | Sim |
| RF17 | Permitir ao administrador gerenciar professores | Gerenciar Professores | Sim |
| RF18 | Permitir ao administrador controlar permissões | Gerenciar Permissões | Sim |
| RF19 | Permitir ao administrador administrar a plataforma | Administrar Plataforma | Sim |

---

# Checklist de Validação

- [x] Os três atores estão identificados: Aluno, Professor e Administrador.
- [x] Cada ator possui funcionalidades específicas.
- [x] O aluno não possui acesso às funções exclusivas de professor ou administrador.
- [x] Os casos de uso foram escritos com verbo no infinitivo.
- [x] A fronteira do sistema está identificada.
- [x] Cada associação representa uma interação entre ator e sistema.
- [x] Os casos de uso representam funcionalidades da plataforma.
- [x] Os recursos de acessibilidade foram considerados.
- [x] Os requisitos funcionais possuem correspondência com casos de uso.
- [x] O sistema contempla aprendizado, exercícios, conteúdos e acompanhamento.
- [x] O diagrama pode ser construído a partir dos requisitos identificados.

---

# Justificativa das Decisões de Modelagem

O caso de uso **Consultar Conteúdo** representa uma das principais funcionalidades do EstudaFácil, pois permite que o aluno acesse materiais de diferentes disciplinas da área de TI. Dessa forma, a plataforma não fica limitada a um único assunto, podendo apoiar o aprendizado em conteúdos como programação, banco de dados, engenharia de software, redes e outras áreas relacionadas.

O caso de uso **Realizar Exercício** permite que o aluno pratique os conteúdos estudados, enquanto **Visualizar Resultado** apresenta seu desempenho após a conclusão das atividades. O caso de uso **Acompanhar Progresso** foi incluído para que o estudante consiga observar sua evolução ao longo dos estudos.

O ator **Professor** foi incluído porque possui acesso próprio à plataforma e pode registrar, organizar e atualizar conteúdos e atividades. Essa separação permite que os materiais educacionais sejam disponibilizados aos alunos por usuários autorizados.

O ator **Administrador** representa o responsável pelo gerenciamento geral do aplicativo. Suas funcionalidades incluem administrar usuários, gerenciar professores e controlar permissões. Assim, o sistema mantém uma divisão de responsabilidades e evita que todos os usuários tenham acesso irrestrito às funcionalidades.

As funcionalidades de acessibilidade foram consideradas para permitir que diferentes estudantes utilizem a plataforma de acordo com suas necessidades.

---

# Questão de Encerramento

## Que problemas podem surgir quando um requisito funcional não possui correspondência clara no modelo UML?

Quando um requisito funcional não possui correspondência clara no modelo UML, podem ocorrer problemas durante o desenvolvimento do sistema. Uma funcionalidade pode ser esquecida ou implementada de forma diferente do que foi especificado.

Também podem surgir dificuldades para identificar as interações entre os diferentes atores e o sistema. No EstudaFácil, por exemplo, a ausência de uma separação clara entre as permissões do aluno, do professor e do administrador poderia permitir acessos indevidos ou dificultar a identificação das responsabilidades de cada perfil.

Por isso, a rastreabilidade entre os requisitos e os casos de uso é importante para garantir que as funcionalidades identificadas sejam representadas no modelo e consideradas durante o desenvolvimento e os testes.
