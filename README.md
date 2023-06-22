# MoneySaver
App for finances

 Descrição geral

Aplicativo desenvolvido como proposta de projeto de conclusão de disciplina, programação orientada a objetos, disponibilizada na Faculdade CESUSC, ministrada pelo professor Ibsem Dias.


Descrição do aplicativo
MoneySaver é um aplicativo android que destina-se a auxiliar pessoas no controle de gastos. Desenvolvido utilizando como ambiente de desenvolvimento a IDE Android Studio, Java como linguagem de programação. Entre as principais funcionalidades que o aplicativo disponibiliza, o registro dos gastos separados por mês é a principal a ser destacada, a listagem dos dados do mês atual (incluindo todas as movimentações) é a principal forma de entender e perceber o quanto de dinheiro foi gasto no mês e onde o dinheiro foi gasto, a listagem dos dados acontece por meio de gráficos e mensagens. Caso seja de interesse do usuário, os dados das movimentações de meses anteriores também ficam registrados no banco de dados, sendo assim basta que o usuário acesse a tela de registros para selecionar o mês para a listagem dos dados.
Para que o MoneySaver funcione de forma estável é preciso que a versão mínima do android seja a 22 (Android 5.1).




Logo do aplicativo - MoneySaver







Diagrama de classe
São sete as classes nas quais o aplicativo funciona, são elas: Usuario, Movimentacao, Carteira, Categoria, Tag, Configuracao, NaturezaDaAcao.
A relação entre as classes está listada no diagrama abaixo. 


Mapa do aplicativo
O aplicativo possui 10 (dez) atividades, que por sua vez serve para conectar o usuário as funcionalidade do aplicativo e para listar dados do aplicativo ao usuário, como exemplo cadastrar usuario, movimentacao, realizar login e listagem de dados. abaixo será listado o mapa do aplicativo e a descrição de cada atividade.

Login
Serve para que o usuário cadastrado entre no painel de controle particular.


Cadastrar Usuário
Serve para que um usuário possa se cadastrar fornecendo como dados necessários nome, login, senha e a senha repetida. Caso o login digitado já esteja cadastrado ou se as senhas digitadas forem diferentes, o cadastro não acontecerá.

Main
A única funcionalidade da Main é a listagem do menu lateral, e a exibição de Fragments.
Home Fragment
Home é onde os principais dados do usuário será listado, total de receita e despesa no mês, informar onde o dinheiro foi gasto em maior quantidade, informar também se a receita é maior do que a despesa ou vice-versa, por meio de porcentagem ou valores líquidos.


Registro Fragment
Todas as movimentações cadastradas no aplicativo será listada na tela de registros, todas as movimentaçẽos são separadas por mês de cadastro, e fica disponível ao usuário selecionar as movimentações de qual mês.

Configurações Fragment
Tela onde as principais configurações do app serão listadas, onde a sessão pode ser encerrada.

Gerência de Carteiras
Tela para cadastrar e listar carteiras, um gráfico faz parte desta tela para mostrar de forma visual onde o dinheiro está investido.

Gerência de Categoria
Tela para cadastrar e listar categorias.

Gerência de Tags
Tela para cadastrar e listar tags.

Nova Movimentação
A principal fonte de entrada de dados no aplicativo, funciona para receita ou despesa.
Receita

Despesa

Nova Transferência
Transfere dinheiro de uma carteira para outra.

Descrição do desenvolvimento
Camada model
Primeiramente, antes de iniciar a codificação do aplicativo, passei um tempo definindo como seria a camada de modelo. Levando em consideração alguns requisitos solicitados pelo professor, tais como persistência de dados e cadastro de usuário, o início da modelagem aconteceu a partir da classe usuário, para que logo em seguida a classe Movimentação fosse criada, o resultado final da modelagem pode ser encontrada na sessão Diagrama de classe na parte superior desta página.
Camada controller
A princípio o aplicativo seria desenvolvido utilizando o modelo MVVM, porém à medida que o aplicativo aumentava a quantidade de funções aumentava, e para solucionar este problema de forma que o código fonte do aplicativo fosse legível uma nova camada foi adicionada, a camada de controle (controller), para facilitar a leitura do código fonte e futuramente a manutenção. Mais de uma camada de controle foi adicionada ao projeto pois cada controller possui um alvo, como é o caso do controller Carteira, que possui apenas métodos que serão necessaŕios para manipular o objeto carteira.
Camada View
A camada View contém todos os arquivos que são Activity.java e Fragment.java
Camada Adapter
A camada Adapter controla os RecycleViews dispostos no projeto, controlando ainda a interação do usuário com algum determinado item listado.
Camada Dal
A camada Dal controla a persistência dos dados, mais especificamente o ObjectBox e o SharedPreferences.
Camada exceptions
A camada Exceptions, desenvolvida apenas para tornar o código fonte mais legível, através da criação de exceptions personalizados.
Camada Testes
A camada Testes contém um arquivo (Main.java), que é responsável por realizar testes na camada de modelo através do terminal.

