Material de orientações para desenvolvimento da missão
prática do 1º nível de conhecimento.

RPG0014  - Iniciando o caminho pelo Java


1º Procedimento | Criação das Entidades e Sistema de Persistência

1. Criar um projeto do tipo Ant..Java Application no NetBeans, utilizando o nome
CadastroPOO para o projeto.

2. Criar um pacote com o nome "model", para as entidades e gerenciadores.

3. No pacote model criar as entidades, com as seguintes características:

Classe Pessoa, com os campos id (inteiro) e nome (texto), método exibir, para
impressão dos dados, construtor padrão e completo, além de getters e setters
para todos os campos.
Classe PessoaFisica, herdando de Pessoa, com o acréscimo dos campos cpf
(texto) e idade (inteiro), método exibir polimórfico, construtores, getters e
setters.
Classe PessoaJuridica, herdando de Pessoa, com o acréscimo do campo cnpj
(texto), método exibir polimórfico, construtores, getters e setters.
Adicionar interface Serializable em todas as classes
4. No pacote model criar os gerenciadores, com as seguintes características:

Classe PessoaFisicaRepo, contendo um ArrayList de PessoaFisica, nível de
acesso privado, e métodos públicos inserir, alterar, excluir, obter e obterTodos,
para gerenciamento das entidades contidas no ArrayList.
Classe PessoaJuridicaRepo, com um ArrayList de PessoaJuridica, nível de
acesso privado, e métodos públicos inserir, alterar, excluir, obter e obterTodos,
para gerenciamento das entidades contidas no ArrayList .
Em ambos os gerenciadores adicionar o método público persistir, com a recepção
do nome do arquivo, para armazenagem dos dados no disco.
Em ambos os gerenciadores adicionar o método público recuperar, com a
recepção do nome do arquivo, para recuperação dos dados do disco
Os métodos persistir e recuperar devem ecoar (throws) exceções
O método obter deve retornar uma entidade a partir do id
Os métodos inserir e alterar devem ter entidades como parâmetros
O método excluir deve receber o id da entidade para exclusão
O método obterTodos deve retornar o conjunto completo de entidades.
5. Alterar o método main da classe principal para testar os repositórios:

Instanciar um repositório de pessoas físicas (repo1).
Adicionar duas pessoas físicas, utilizando o construtor completo.
Invocar o método de persistência em repo1, fornecendo um nome de arquivo fixo,
através do código.
Instanciar outro repositório de pessoas físicas (repo2).
Invocar o método de recuperação em repo2, fornecendo o mesmo nome de
arquivo utilizado anteriormente.
Exibir os dados de todas as pessoas físicas recuperadas.
Instanciar um repositório de pessoas jurídicas (repo3).
Adicionar duas pessoas jurídicas, utilizando o construtor completo.
Invocar o método de persistência em repo3, fornecendo um nome de arquivo fixo,
através do código.
Instanciar outro repositório de pessoas jurídicas (repo4).
Invocar o método de recuperação em repo4, fornecendo o mesmo nome de
arquivo utilizado anteriormente.
Exibir os dados de todas as pessoas jurídicas recuperadas.
6. Ajustar as características para obter uma execução como a seguinte:

M1 - 2.png
 (Moderado)
7. Verificar as funcionalidades solicitadas e os arquivos gerados

✅ Resultados esperados

1. É importante que o código seja organizado.

2. Outro ponto importante é explorar as funcionalidades oferecidas pelo NetBeans para
melhoria da produtividade.

3. Nesse exercício, é esperado que o estudante demonstre as habilidades básicas para
a programação Java com persistência em arquivo.

📝 Relatório discente de acompanhamento

Os Relatórios de Práticas deverão ser confeccionados em arquivo no formato PDF, com
a Logo da Universidade, nome do Campus, nome do Curso, nome da Disciplina, número
da Turma, semestre letivo, nome dos integrantes da Prática. Além disso, o projeto deve
ser armazenado em um repositório no GIT e o respectivo endereço deve constar na
documentação. A documentação do projeto deve conter:

Título da Prática;
Objetivo da Prática;
Todos os códigos solicitados neste roteiro de aula;
Os resultados da execução dos códigos também devem ser apresentados;
Análise e Conclusão:
Quais as vantagens e desvantagens do uso de herança?
Por que a interface Serializable é necessária ao efetuar persistência em arquivos
binários?
Como o paradigma funcional é utilizado pela API stream no Java?
Quando trabalhamos com Java, qual padrão de desenvolvimento é adotado na
persistência de dados em arquivos?
