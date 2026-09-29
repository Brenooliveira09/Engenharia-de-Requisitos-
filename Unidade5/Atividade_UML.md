# Do requisito ao Diagrama de Casos de Uso

## Etapa 1 — Leitura e Identificação dos Requisitos

### 1. Qual é o objetivo principal do sistema?

O objetivo principal do sistema é **auxiliar estudantes da área de Computação no aprendizado de UML, com foco em Diagramas e Especificações de Casos de Uso**, disponibilizando conteúdos teóricos, atividades práticas e recursos de acessibilidade em um único ambiente.

### 2. Quem interage diretamente com o sistema?

O ator principal é o **Aluno**, representado por estudantes de Ciência da Computação, Engenharia de Software ou Sistemas de Informação.

### 3. Quais funcionalidades são oferecidas ao aluno?

O sistema disponibiliza:

* Cadastro e acesso à conta;
* Acesso aos conteúdos de UML;
* Seleção de temas de estudo;
* Consulta de conceitos e exemplos;
* Realização de exercícios;
* Visualização do resultado dos exercícios;
* Acompanhamento do progresso;
* Acesso ao modo de treino;
* Configuração das opções de acessibilidade;
* Controle de áudio e narração dos conteúdos.

### 4. Quais regras condicionam o acesso aos exercícios?

Os exercícios podem possuir regras específicas, como:

* O aluno precisa selecionar um tema antes de iniciar uma atividade;
* Cada exercício deve ser respondido antes de avançar para o próximo;
* O resultado é apresentado após a conclusão da atividade;
* O progresso do aluno é atualizado após a realização dos exercícios.

### 5. Quais funcionalidades contribuem para a acessibilidade?

O sistema possui recursos como:

* **Narração de conteúdo textual:** leitura dos textos e questões por voz;
* **Navegação por teclado:** permite utilizar o sistema sem depender do mouse;
* **Controle de áudio:** permite ativar ou desativar sons e narração;
* **Contraste visual:** facilita a visualização dos elementos da interface;
* **Ausência de limite de tempo:** permite que o aluno responda às atividades no seu próprio ritmo.

---

# Elementos Identificados

| Elemento Identificado     | Evidência / Descrição                                | Classificação ABNT          |
| ------------------------- | ---------------------------------------------------- | --------------------------- |
| Aluno                     | Usuário que utiliza o sistema para estudar UML       | Ator                        |
| Cadastrar-se              | Permite ao aluno criar uma conta no sistema          | Requisito Funcional         |
| Realizar Login            | Permite acessar a conta cadastrada                   | Requisito Funcional         |
| Selecionar Tema           | Permite escolher o conteúdo que deseja estudar       | Requisito Funcional         |
| Consultar Conteúdo        | Permite acessar conceitos e explicações de UML       | Requisito Funcional         |
| Visualizar Exemplos       | Permite consultar exemplos relacionados ao conteúdo  | Requisito Funcional         |
| Realizar Exercício        | Permite responder questões sobre o conteúdo estudado | Requisito Funcional         |
| Visualizar Resultado      | Apresenta o desempenho após a atividade              | Requisito Funcional         |
| Acompanhar Progresso      | Permite visualizar o progresso nos estudos           | Requisito Funcional         |
| Acessar Modo Treino       | Permite praticar os conteúdos sem avaliação          | Requisito Funcional         |
| Configurar Acessibilidade | Permite configurar recursos de acessibilidade        | Requisito de Acessibilidade |
| Ativar/Desativar Narração | Permite controlar a leitura dos conteúdos por voz    | Requisito de Acessibilidade |
| Ativar/Desativar Áudio    | Permite controlar sons do sistema                    | Requisito de Acessibilidade |
| Navegar por Teclado       | Permite utilizar as funcionalidades sem mouse        | Requisito de Acessibilidade |
| Sem Limite de Tempo       | Não exige tempo máximo para responder exercícios     | Requisito de Acessibilidade |

---

# Etapa 2 — Construção do Diagrama de Casos de Uso

## Estrutura do Diagrama UML

### Fronteira do Sistema

A fronteira representa o **Sistema de Aprendizagem de UML**.

### Ator Principal

O ator principal é o **Aluno**, localizado fora da fronteira do sistema.

---

# Casos de Uso e Relacionamentos

### 1. Cadastrar-se

* Associação direta com o Aluno.
* Permite criar uma conta para utilizar o sistema.

### 2. Realizar Login

* Associação direta com o Aluno.
* Permite acessar as funcionalidades da plataforma.

### 3. Selecionar Tema

* Associação direta com o Aluno.
* Permite escolher o assunto de UML que deseja estudar.

### 4. Consultar Conteúdo

* Associação direta com o Aluno.
* Permite acessar conceitos e explicações relacionados ao tema estudado.

### 5. Visualizar Exemplos

* Associação direta com o Aluno.
* Permite visualizar exemplos relacionados ao conteúdo.

### 6. Realizar Exercício

* Associação direta com o Aluno.
* Permite responder questões relacionadas ao conteúdo estudado.

### 7. Visualizar Resultado

* É executado após a conclusão dos exercícios.
* Apresenta o desempenho obtido pelo aluno.

### 8. Acompanhar Progresso

* Associação direta com o Aluno.
* Permite consultar o histórico e o progresso dos estudos.

### 9. Acessar Modo Treino

* Associação direta com o Aluno.
* Permite praticar os conteúdos sem necessidade de avaliação.

### 10. Configurar Acessibilidade

* Associação direta com o Aluno.
* Permite configurar os recursos de acessibilidade disponíveis.

### 11. Ativar/Desativar Narração

* Pode ser representado como uma extensão de **Configurar Acessibilidade**.
* Permite ativar ou desativar a leitura dos conteúdos por voz.

### 12. Ativar/Desativar Áudio

* Pode ser representado como uma extensão de **Configurar Acessibilidade**.
* Permite controlar os sons do sistema.

---

# Relacionamentos UML

Uma estrutura simplificada do sistema pode ser representada da seguinte forma:

```text
                    ┌─────────────────────────────────────┐
                    │   SISTEMA DE APRENDIZAGEM DE UML   │
                    │                                     │
                    │  (Cadastrar-se)                     │
                    │  (Realizar Login)                   │
                    │                                     │
                    │  (Selecionar Tema)                  │
                    │         │                           │
                    │         ▼                           │
                    │  (Consultar Conteúdo)               │
                    │         │                           │
                    │         ▼                           │
                    │  (Visualizar Exemplos)              │
                    │                                     │
                    │  (Realizar Exercício)               │
                    │         │                           │
                    │         ▼                           │
                    │  (Visualizar Resultado)             │
                    │                                     │
                    │  (Acompanhar Progresso)             │
                    │                                     │
                    │  (Acessar Modo Treino)              │
                    │                                     │
                    │  (Configurar Acessibilidade)        │
                    │         ├── (Ativar/Desativar       │
                    │         │       Narração)            │
                    │         └── (Ativar/Desativar Áudio)│
                    │                                     │
                    └─────────────────────────────────────┘
                              ▲
                              │
                            Aluno
```

> **Observação:** No diagrama UML real, o ator ficará fora do retângulo e os casos de uso serão representados por elipses.

---

# Etapa 3 — Matriz de Rastreabilidade

| ID   | Requisito Funcional                             | Caso de Uso               | No Diagrama? |
| ---- | ----------------------------------------------- | ------------------------- | ------------ |
| RF01 | Permitir ao aluno criar uma conta.              | Cadastrar-se              | Sim          |
| RF02 | Permitir ao aluno acessar sua conta.            | Realizar Login            | Sim          |
| RF03 | Permitir escolher um tema de estudo.            | Selecionar Tema           | Sim          |
| RF04 | Permitir consultar conteúdos de UML.            | Consultar Conteúdo        | Sim          |
| RF05 | Permitir visualizar exemplos dos conteúdos.     | Visualizar Exemplos       | Sim          |
| RF06 | Permitir realizar exercícios.                   | Realizar Exercício        | Sim          |
| RF07 | Apresentar o resultado dos exercícios.          | Visualizar Resultado      | Sim          |
| RF08 | Permitir acompanhar o progresso.                | Acompanhar Progresso      | Sim          |
| RF09 | Permitir acessar o modo de treino.              | Acessar Modo Treino       | Sim          |
| RF10 | Permitir configurar recursos de acessibilidade. | Configurar Acessibilidade | Sim          |

---

# Checklist de Validação

* [x] O ator representa um papel externo ao sistema.
* [x] Os casos de uso foram escritos com verbo no infinitivo.
* [x] A fronteira do sistema está identificada.
* [x] Cada associação representa uma interação real entre o aluno e o sistema.
* [x] Os casos de uso representam funcionalidades do sistema.
* [x] Os recursos de acessibilidade foram considerados.
* [x] Os requisitos funcionais possuem correspondência com casos de uso.
* [x] Não foram utilizados elementos relacionados a jogos, como vilões, batalha ou pontos de vida.
* [x] O sistema possui funcionalidades de estudo, exercícios e acompanhamento.
* [x] O diagrama pode ser construído a partir dos requisitos identificados.

---

# Justificativa das Decisões de Modelagem

O caso de uso **Realizar Exercício** representa uma das principais funcionalidades do sistema, pois permite que o aluno pratique os conteúdos de UML estudados.

O caso de uso **Visualizar Resultado** está relacionado à realização dos exercícios, pois o sistema apresenta o desempenho do aluno após a conclusão da atividade.

O caso de uso **Selecionar Tema** permite que o aluno escolha o assunto que deseja estudar, enquanto **Consultar Conteúdo** disponibiliza as informações relacionadas ao tema selecionado.

O caso de uso **Acompanhar Progresso** foi incluído para permitir que o aluno acompanhe sua evolução dentro do sistema.

As funcionalidades de **Configurar Acessibilidade**, **Ativar/Desativar Narração** e **Ativar/Desativar Áudio** foram incluídas para garantir que o sistema possa ser utilizado por diferentes perfis de alunos.

---

# Questão de Encerramento

## Que problemas podem surgir quando um requisito funcional não possui correspondência clara no modelo UML?

Quando um requisito funcional não possui correspondência clara no modelo UML, podem ocorrer problemas durante o desenvolvimento do sistema. Uma funcionalidade pode ser esquecida ou implementada de forma diferente do que foi especificado.

Também podem surgir dificuldades para identificar as interações entre o usuário e o sistema, além de problemas durante a criação dos testes.

Por isso, a rastreabilidade entre os requisitos e os casos de uso é importante para garantir que as funcionalidades identificadas sejam representadas no modelo e consideradas durante o desenvolvimento e os testes.

## Conclusão

O modelo de casos de uso permite representar de forma clara as principais funcionalidades do **Sistema de Aprendizagem de UML**, mostrando como o aluno interage com a plataforma.

A utilização dos requisitos como base para a construção do diagrama também facilita a organização, implementação e validação do sistema.


Link do Canva de Produto : https://www.canva.com/design/DAHWmo9spgU/e4WGOG5ip33es2vlxAwBwQ/edit
