# Entidades e seus tipos

Entidade é uma representação de um objeto, pessoa, lugar, evento ou conceito do mundo real que sobre o qual queremos guardar informações. Ela pode ser classificada como entidades físicas e lógicas, de acordo com sua existência no mundo real.

. *Entidades físicas*: São aquelas realmente tangíveis, existentes e visíveis no mundo real, como um cliente ou um produto por exemplo.

. *Entidades Lógicas*: São aquelas que existem geralmente em decorrência da interação entre ou com entidades físicas, que fazem sentido dentro de um certo domínio de negócios, mas que no mundo externo/ral não são objetos físicos.

. *Entidades fortes*: São aquelas cuja existência não depende de outras entidades, ou seja, por si só elas já possuem total sentido de existir. Em um sistema de vendas, a entidade produto, por exemplo, não depende de quaisquer para existir.

. *Entidades fracas*: Ao contrário das entidades fortes, as fracas são aquelas que dependem de outras entidades para existirem, pois individualmente elas não fazem sentido.

. *Entidades associativas*: esse tipo de entidade  surge quando há necessidade de associar uma entidade a um relacionamneto existente. Na modelagem Entidade-Relacionamento não é possivel que um relacionamento seja associado a uma entidade, então tornamos esse relacionamneto uma entidade associativa, que a partir daí poderá se relacionar com outras entidades.

# Relacionamentos

Uma vez que as entidades são identifificadas, deve-se então definir come se dá o relacionamento entre elas. De acordo com a quatidade dos objetos envolvidos em cada lado do relacionamento, que podemos classificalos de três formas:

. *Relacionamento 1..1(uma para um)*: cada uma das entidades envolvidas referenciam obrigatoriamente apenas uma unidade da outra. Por exemplo, em um banco de dados de currículos, cada usuário cadastrado pode possuir apenas um currículo na base, ao mesmo tempo em que cada currículo só pertence a um único usuário cadastrado.

. *Relacionamento 1..n ou 1..* (um para muitos)*: uma das entidasd envolvidas pode se resferenciar várias unidades da outra, porém, do outro lado cada uma das várias unidades referenciadas só pode estar ligada uma unidade da outra entidade. Por exemplo, num sistema de planp de saúde, um usuário pode ter vários dependentes, mas cada um só pode estar ligado a um usuário.

. *Relacionamento n..n ou *..* (muitos para muitos)*: nesse relacionamento cada entidade, de ambos os lados, podem referenciar múltiplas unidades da outra. Por exemplo , em um sistema de biblioteca, um título pode ser escrito por vários autores, ao mesmo tempo em que um autor pode escrever vários títulos.

Em geral, os relacionamentossão nomeados com verbos ou expressões que representam a forma como as entidades interagem, ou a ação que uma exerce sobre a outra.

# Atributos 

Atributos são caracterìsticas que descrevem cada entidade dentro do domínio. Durante a ánalise de requisitos, são identificados os atributos relevantes de cada entidade naquele contexto, para manteer o modelo mais simples possível e armazenar apenas informações que serão úteis. 

Os atributos podem ser classificados quanto á sua função da seguinte forma:

. *Descritivos*: representam caractrística intrínsecas de uma entidade, tais como nome ou cor.

. *Nominativos*: além de serem também descritivos, estes tem a função de definir e identificar um objeto. Nome, código, número são exemplos de atributos nominativos.

# Estrutura dos atributos:

. *Simples*: Um único atributo define uma característica da entidade. Exemplo: nome, peso.

. *Compostos*: para definir uma informação da entidade, são usados vários atributos. Por exemplo, o endereço pode ser composto por rua, número, bairro, etc.

Alguns atributos representam valores únicos que identificam a entidade dentro do domínio e não podem se repetir. Em um cadastro de clientes, por exemplo, esse atributo poderia ser o CPF. A estes chamamos de Chave Primária.

Já os atributos referenciais são chamados de Chave Estrangeira e geralmente estão ligados à chave primária da outra entidade. Estes termos são bastante comuns no contexto de bancos de dados. Mantendo o exemplo anterior, a entidade cliente tem como chave primária seu CPF, assim, a venda possui também um campo “CPF do cliente” que se relaciona com o campo CPF da entidade cliente.