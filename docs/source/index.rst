QuarkSmart
===========

O **quarksmart** é uma biblioteca Python que permite a integração entre ferramentas de *Data Science*  
com os dados armazenados no sistema `QuarkSmart <https://quarkbi.esig.com.br>`_.

Com apenas um comando é possível carregar seus dados para um formato que permite o tratamento de forma fácil e ágil.
O quarksmart foi pensado para ser utilizado com outras bibliotecas de *Data Science*, como o ``pandas`` e o ``numpy``, mas nada
você pode utiliza-la como preferir.

Instalação
===========

A instalação da biblioteca é bem simples e pode ser realizada facilmente por meio do gerenciador de pacotes do python (pip).

Para instalar, abrir o terminal e rodar o comando abaixo do ``pip``: ::

    $ pip install quarksmart

Para verificar se a instalação aconteceu corretamente, basta importar o pacote e verificar a versão.

.. code-block:: python

   >>> import quarksmart
   >>> quarksmart.__version__
   ... 1.0.0

Utilização
===========
.. note::

   As informações que seram passadas nos paremêtros da função devem ser consultadas direto no sistema do QuarkSmart.

Carregando os dados com o quarksmart é muito fácil, bastar utilizar a funções *carregar_dados* e passar alguns paramêtros:

* ``token`` - é a chave de acesso que autentica o usuário no sistema. Esse Token pode ser encontrado no próprio sistema do QuarkSmart na página da `API REST`_.
* ``entidade`` - Identificador da Entidade, é um atalho para a entidade que permite encontra-la de forma mais fácil. Para encontra-lo, basta acessar a página de `listagem das entidades`_.
* ``data`` - quando se deseja consultar os dados da entidade em determinada data, é possível informa-la por meio desse parâmetro e o sistema retornará o conjunto de dados da entidade naquele momento. Quando esse parâmetro não é informado o sistema pega estado atual. Ex: ``data='01/01/2019'``.

.. code-block:: python

    >>> import quarksmart as qs
    >>> entidade = qs.carregar_dados("pessoa", \
    ...                token="b40734876aeea537ec0dce2e371da4a1")
    >>> type(entidade)
    pandas.core.frame.DataFrame

O retorno da função é um **Dataframe** do *pandas*.

Todas os detalhes das funções da biblioteca podem ser encontrados na página de `funções`_.

.. _`funções`: funcoes.html
.. _`API REST`: https://quarkbi.esig.com.br/app/extrator/entidade/api_rest.jsf
.. _`listagem das entidades`: https://quarkbi.esig.com.br/app/extrator/entidade/list.jsf