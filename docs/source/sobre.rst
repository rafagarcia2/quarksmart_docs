Sobre
===========

O quarksmart é uma biblioteca Python que permite a integração entre ferramentas de Data Science (como o Jupyter Notebooks) com os dados armazenados no sistema `QuarkSmart <https://quarkbi.esig.com.br>`_.

Instalação
-----------

A instalação da biblioteca é bem simples e pode ser realizada facilmente por meio do gerenciador de pacotes do python (pip).

Para instalar, abrir o terminal e rodar o comando abaixo do ``pip`` ::

    $ pip install quarksmart

Para verificar se a instalação aconteceu corretamente, basta importar o pacote e verificar a versão.

.. code-block:: python

   >>> import quarksmart
   >>> quarksmart.__version__
   ... 1.0.0

Equipe
-----------
.. code-block:: python

   >>> import pyexcel as pe
   >>> records = pe.iget_records(file_name="your_file.xls")
   >>> for record in records:
   ...     print("%s is aged at %d" % (record['Name'], record['Age']))
   Adam is aged at 28
   Beatrice is aged at 29
   Ceri is aged at 30
   Dean is aged at 26
   >>> pe.free_resources()