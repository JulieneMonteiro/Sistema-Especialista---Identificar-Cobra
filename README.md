**Programação de Sistema Especialista - Universidade Veiga de Almeida**

**Professor: Thiago Gabriel**

Grupo Desenvolvedor: **Juliene Cristine de Oliveira Monteiro, Diego Tasso da Cunha Ferreira, Maria Julia Eduarda Maia Silva, Gabriel Torres Machado, Gabriel da Silva Cavalcante.**

### PROJETO ERYLA
### Resenha Detalhada do Código de Identificação de Cobras

Este código foi desenvolvido para criar uma aplicação interativa de identificação de cobras, utilizando a biblioteca Tkinter para a criação de uma interface gráfica simples e funcional. O programa permite que o usuário identifique possíveis espécies de cobras com base nas respostas fornecidas a uma série de perguntas. O código está estruturado de maneira modular, com diferentes seções que cuidam da interface do usuário, do processamento das respostas e da comparação com uma base de dados de cobras. A seguir, vamos detalhar as principais partes do código e explicar como cada uma delas contribui para o funcionamento do sistema.

### 1. **Importações e Definição de Cores:**

No início do código, são importadas as bibliotecas necessárias para a construção da interface gráfica e para o controle da interação com o usuário:
- **`tkinter`**: Biblioteca responsável pela criação da interface gráfica.
- **`tkinter.messagebox`**: Usada para exibir caixas de diálogo com mensagens, como resultados ou alertas.
- **`tkinter.ttk`**: Utilizada para melhorar a aparência dos widgets, com uma versão aprimorada de elementos de interface como botões e caixas de seleção.

Além disso, o código define algumas cores que serão utilizadas para personalizar a aparência da interface, como as cores do fundo da janela e das fontes.

### 2. **Configuração da Janela Principal:**

A janela principal do aplicativo é configurada com o título "Identificação da Cobra", um tamanho fixo de 850x400 pixels e um fundo na cor `#f5f5f5`. O layout da janela é estruturado com o uso de vários elementos gráficos:
- **Título**: Apresenta o nome do sistema de forma destacada no topo da interface.
- **Perguntas e Opções**: Um conjunto de labels e botões para exibir as perguntas e capturar as respostas do usuário.
- **Rodapé**: No rodapé da janela, é fornecida uma informação adicional sobre os desenvolvedores do sistema, oferecendo mais contexto sobre o propósito da aplicação.

### 3. **Estrutura das Perguntas e Respostas:**

Uma parte crucial do código é a definição das perguntas e respostas que o usuário deve responder para ajudar na identificação da cobra. As perguntas são armazenadas em uma lista chamada `perguntas`, onde cada item é um dicionário com as seguintes chaves:
- **`pergunta`**: Texto da pergunta.
- **`respostas`**: Lista de opções de resposta, cada uma associada a uma pontuação que ajudará a comparar com as características das cobras.
  
As perguntas abrangem uma variedade de tópicos:
- Local da mordida (braço, perna, pescoço, etc.).
- Características da cobra (comportamento, coloração, tamanho).
- Sintomas após a mordida.
  
Essas perguntas são essenciais para determinar, com base nas respostas do usuário, quais cobras da base de dados podem ser a responsável pela mordida.

### 4. **Base de Dados das Cobras:**

O sistema contém uma base de dados das cobras, que é definida por meio de uma lista de dicionários. Cada dicionário representa uma cobra, contendo informações detalhadas como:
- **Nome da cobra**.
- **Habitat** (onde a cobra normalmente vive).
- **Tamanho** (tamanho da cobra, como pequeno, médio, grande).
- **Características da mordida** (como dor imediata, inchaço, etc.).
- **Cor e padrão** (detalhes sobre a aparência da cobra).

Essa base de dados é comparada com as respostas fornecidas pelo usuário para determinar quais cobras mais se assemelham ao perfil descrito pelas respostas.

### 5. **Funções de Navegação e Exibição de Perguntas:**

O código inclui funções para navegar pelas perguntas e exibir suas opções de forma dinâmica:
- **`voltar_pergunta()`**: Permite ao usuário voltar para a pergunta anterior e alterar sua resposta.
- **`mostrar_pergunta()`**: Exibe a pergunta atual e as opções de resposta. Essa função também associa cada botão de resposta a uma pontuação, que será registrada quando o usuário clicar na opção.

A navegação é controlada de forma a garantir que o usuário só possa avançar para a próxima pergunta quando uma resposta for selecionada, evitando que o sistema avance sem que todas as questões sejam respondidas.

### 6. **Armazenamento e Análise das Respostas:**

À medida que o usuário avança pelo formulário, as respostas são armazenadas em uma lista chamada `respostas`. Cada resposta possui um valor numérico (pontuação), que é fundamental para a comparação com a base de dados das cobras. Quando todas as perguntas forem respondidas, o código realiza a análise dessas respostas e começa a comparar o perfil obtido com as cobras na base de dados.

### 7. **Função de Identificação e Exibição do Resultado:**

Após o preenchimento completo do formulário, o código usa a função **`exibir_resultado()`** para analisar as respostas do usuário. A função compara os dados inseridos com as características de cada cobra na base de dados. Se houver uma correspondência entre as respostas do usuário e as características de uma cobra específica, o nome dessa cobra será exibido como sugestão.

O resultado é apresentado em uma caixa de diálogo (`messagebox`) que lista as cobras que podem corresponder ao perfil descrito pelas respostas do usuário.

### 8. **Exibição das Cobras Identificadas:**

Com base nas respostas, o sistema exibe um resultado final, indicando quais cobras podem ser a responsável pela mordida. Se várias cobras correspondem às características fornecidas, o sistema as listará todas. Caso não haja correspondências claras, o sistema poderá exibir uma mensagem informando que nenhuma cobra conhecida corresponde exatamente aos dados fornecidos.

### Considerações Finais:

Este código é uma aplicação interativa simples, porém eficaz, para a identificação de cobras com base em informações fornecidas pelo usuário. Ele utiliza uma interface gráfica clara e direta, que facilita a interação com o sistema. Além disso, a estrutura de perguntas e respostas bem definida torna o processo de identificação intuitivo.

**Pontos Positivos:**
- **Interface simples e intuitiva**: A interface gráfica construída com Tkinter é amigável e fácil de usar.
- **Estrutura modular**: O código é bem estruturado, com funções claramente definidas para cada tarefa.
- **Base de dados funcional**: A base de dados das cobras é um ponto forte do sistema, embora possa ser expandida com mais informações sobre diferentes espécies.

**Pontos de Melhoria:**
- **Base de dados limitada**: A base de dados de cobras é relativamente pequena e não cobre uma ampla gama de espécies, o que limita a precisão da identificação.
- **Falta de imagens**: Adicionar imagens das cobras identificadas poderia tornar a aplicação mais interessante e visualmente atraente.
- **Expansão de perguntas**: A inclusão de mais perguntas ou detalhes poderia aumentar a precisão do sistema, além de tornar a experiência do usuário mais completa.

No geral, o código serve como uma boa introdução à criação de aplicativos interativos e ao uso do Tkinter, e pode ser facilmente expandido ou modificado para incluir mais funcionalidades ou uma base de dados mais robusta.
