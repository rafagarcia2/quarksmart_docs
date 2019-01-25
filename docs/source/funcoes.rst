carregar_dados
===========

Paramêtros
-----------
.. note::

   As informações que seram passadas nos paremêtros da função devem ser consultadas direto no sistema do QuarkSmart.

Carregando os dados com o quarksmart é muito fácil, bastar utilizar a funções *carregar_dados* e passar alguns paramêtros:

* ``token`` - é a chave de acesso que autentica o usuário no sistema. Esse Token pode ser encontrado no próprio sistema do QuarkSmart na página da `API REST`_.
* ``entidade`` - Identificador da Entidade, é um atalho para a entidade que permite encontra-la de forma mais fácil. Para encontra-lo, basta acessar a página de `listagem das entidades`_.
* ``data`` - quando se deseja consultar os dados da entidade em determinada data, é possível informa-la por meio desse parâmetro e o sistema retornará o conjunto de dados da entidade naquele momento. Quando esse parâmetro não é informado o sistema pega estado atual. Ex: ``data='01/01/2019'``.

O retorno da função é um **Dataframe** do *pandas*.

.. code-block:: python

    >>> import quarksmart as qs
    >>> entidade = qs.carregar_dados("colaboradores", \
    ...                token="b40734876aeea537ec0dce2e371da4a1")
    >>> type(entidade)
    pandas.core.frame.DataFrame

Exemplo informando uma data:

.. code-block:: python

    >>> import quarksmart as qs
    >>> entidade = qs.carregar_dados(entidade="movimentacoes-financeiro", \
    ...                token="b40734876aeea537ec0dce2e371da4a1", data="01/12/2018")
    >>> type(entidade)
    pandas.core.frame.DataFrame

Erros
-----------
Quando o sistema não consegue carregar os dados, ele retorna uma mensagem no lugar dos dados, as mensagens podem ser:

* ``Falha de Autenticação.`` - quando o sistema não consegue autenticar o usuário com o Token informado.
* ``Falha ao carregar os dados`` - quando a entidade não é encontrada ou existe algum problema com os dados.

.. code-block:: python

    >>> entidade = qs.carregar_dados("colaboradores", \
    ...                token="token_invalido")
    >>> entidade
    Falha de Autenticação.

.. _`API REST`: https://quarkbi.esig.com.br/app/extrator/entidade/api_rest.jsf
.. _`listagem das entidades`: https://quarkbi.esig.com.br/app/extrator/entidade/list.jsf