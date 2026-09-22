# Do requisito ao Diagrama de Casos de Uso

## Etapa 1 — Leitura e Identificação dos Requisitos

### 1. Qual é o objetivo principal do U.C. Battle?

O objetivo principal da aplicação é auxiliar o processo de ensino e aprendizagem da linguagem UML, com foco nos Diagramas e Especificações de Casos de Uso, por meio de uma abordagem lúdica, interativa e acessível a alunos da área de Computação com deficiência visual.

### 2. Quem interage diretamente com o sistema?

O ator principal é o **Jogador**, representado pelo estudante de Ciência da Computação, Engenharia de Software ou Sistemas de Informação.

### 3. Quais funcionalidades são oferecidas ao jogador?

O sistema disponibiliza:

- Seleção de fases/vilões;
- Combate através da resolução de charadas;
- Utilização da habilidade especial de dica;
- Rendição na batalha;
- Acesso ao modo de treino com o mestre;
- Consulta da teoria de casos de uso na seção **Book**;
- Seleção do tema de estudo;
- Configuração das opções de acessibilidade e áudio.

### 4. Quais regras condicionam o uso da habilidade de receber uma dica?

A habilidade especial:

- Pode ser utilizada **apenas uma vez por batalha**;
- Só pode ser utilizada quando o jogador possuir **2 pontos de vida ou menos**.

### 5. Quais funcionalidades contribuem para a acessibilidade?

- **Narração de conteúdo textual:** sintetização de voz para perguntas, alternativas, dicas e diálogos do Book;
- **Ausência de limite de tempo:** não exige respostas rápidas durante os combates;
- **Controle de áudio independente:** permite ajustar ou desativar efeitos sonoros e músicas;
- **Navegação por teclado:** permite utilizar a interface sem mouse;
- **Modo tutorial/treino:** permite praticar sem penalizações;
- **Design adaptativo:** utiliza contraste visual e padronização dos botões.

---

# Elementos Identificados

| Elemento Identificado | Evidência no Artigo | Classificação ABNT |
|---|---|---|
| Jogador | "Nele o jogador é um herói..." | Ator |
| Selecionar uma Fase | "O software deverá permitir ao usuário selecionar uma fase" | Requisito Funcional |
| Enfrentar Vilão | "O combate consiste em responder charadas do oponente..." | Requisito Funcional |
| Responder Charada | "O software deverá trocar de charada após o usuário escolher uma resposta" | Requisito Funcional |
| Utilizar Habilidade (Receber Dica) | "O software deverá permitir ao usuário usar a habilidade somente quando tiver 2 ou menos pontos de vida" | Requisito Funcional |
| Regra dos 2 Pontos de Vida | "Se tiver 2 pontos de vida ou menos você poderá usar seu poder e receber uma dica..." (máx. 1x) | Regra de Negócio |
| Render-se | "O software deverá indicar derrota caso o usuário escolha se render" | Requisito Funcional |
| Aceder Modo Treino | "O software deverá permitir ao usuário selecionar a opção de tutorial" | Requisito Funcional |
| Estudar Conceitos (Book) | "O software deverá permitir ao usuário selecionar a opção de estudar conceitos" | Requisito Funcional |
| Selecionar Tema de Estudo | "O software deverá permitir ao usuário escolher uma opção de tema para poder estudá-lo" | Requisito Funcional |
| Configurar Acessibilidade | "Opções para ligar e desligar efeitos sonoros, músicas e narrações" | Requisito de Acessibilidade |
| Narração de Texto por Voz | "Opção de ligar e desligar narração sobre perguntas, imagens, alternativas e quadrinhos..." | Requisito de Acessibilidade |
| Sem Limite de Tempo | "Não exigir um tempo limite para responder as questões dentro do jogo..." | Requisito de Acessibilidade |

---

# Etapa 2 — Construção do Diagrama de Casos de Uso

## Estrutura do Diagrama UML

- **Fronteira do Sistema:** retângulo que representa a aplicação U.C. Battle.
- **Ator Principal:** Jogador, localizado fora do limite do sistema.

## Casos de Uso e Relacionamentos

### 1. Selecionar Fase

- Associação direta com o Jogador.

### 2. Enfrentar Vilão

- Associação direta com o Jogador.
- Inclui obrigatoriamente **Responder Charada**.

### 3. Responder Charada

- Pode ser estendido por **Utilizar Habilidade (Receber Dica)**.
- Condição da extensão:
  - Pontos de vida do jogador `<= 2`;
  - Habilidade ainda não utilizada na batalha atual.

### 4. Render-se

- Associação direta com o Jogador.
- Inclui **Voltar ao Menu Principal**.

### 5. Aceder Modo Treino

- Associação direta com o Jogador.

### 6. Estudar Conceitos

- Associação direta com o Jogador.
- Inclui **Selecionar Tema de Estudo**.

### 7. Configurar Acessibilidade

- Associação direta com o Jogador.

### 8. Voltar ao Menu Principal

- Caso de uso reutilizado por inclusão.

## Notas UML

### Regra de Negócio

A habilidade de receber dica só pode ser ativada **1 vez por batalha** e exige que os pontos de vida do Jogador sejam **menores ou iguais a 2**.

### Acessibilidade

Não existe limite de tempo para a escolha das respostas.

---

# Etapa 3 — Matriz de Rastreabilidade

| ID | Requisito Funcional | Caso de Uso | No Diagrama? |
|---|---|---|---|
| RF01 | Permitir ao usuário selecionar uma fase. | Selecionar Fase | Sim |
| RF02 | Trocar a charada após o usuário responder. | Responder Charada | Sim |
| RF03 | Permitir usar a habilidade com 2 ou menos pontos de vida. | Utilizar Habilidade (Receber Dica) | Sim |
| RF04 | Indicar derrota quando o usuário se render. | Render-se | Sim |
| RF05 | Permitir escolher um tema para estudar. | Selecionar Tema de Estudo | Sim |

### Resumo

Todos os **5 requisitos funcionais** apresentados na matriz possuem correspondência com casos de uso no diagrama.

---

# Checklist de Validação

- [x] Os atores representam papéis externos ao sistema.
- [x] Os casos de uso foram escritos com verbo no infinitivo.
- [x] A fronteira do sistema está identificada.
- [x] Cada associação representa uma interação real.
- [x] O `<<include>>` representa um comportamento obrigatório e reutilizado.
- [x] O `<<extend>>` representa um comportamento opcional ou condicionado.
- [x] As regras de negócio não foram representadas como atores.
- [x] Os requisitos selecionados estão rastreados no diagrama.
- [x] Foi considerada uma necessidade de acessibilidade.
- [x] O diagrama está legível e sem elementos desconectados.

---

# Justificativa das Decisões de Modelagem

Modelou-se **Enfrentar Vilão** com relacionamento `<<include>>` para **Responder Charada**, pois a resolução de charadas é uma parte obrigatória do combate.

A funcionalidade **Utilizar Habilidade** foi definida como `<<extend>>` de **Responder Charada**, pois é opcional e depende da regra de possuir 2 ou menos pontos de vida.

O **Book** e as opções de acessibilidade foram representados como casos de uso independentes por atenderem a requisitos funcionais e de acessibilidade específicos.

---

# Questão de Encerramento

## Que problemas podem surgir quando um requisito funcional não possui correspondência clara no modelo UML?

Quando um requisito funcional não possui correspondência no modelo UML, podem ocorrer:

1. **Omissão de funcionalidades:** a equipe pode deixar de implementar uma funcionalidade.
2. **Falhas de arquitetura e design:** podem surgir problemas na identificação de dependências e relacionamentos.
3. **Dificuldade na estimação e nos testes:** a equipe de QA pode ter dificuldades para criar casos de teste adequados e os gestores podem ter estimativas imprecisas sobre o desenvolvimento.

### Conclusão

A rastreabilidade entre requisitos e casos de uso ajuda a garantir que as funcionalidades identificadas sejam representadas no modelo UML e consideradas durante o desenvolvimento e os testes.
