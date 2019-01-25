QuarkSmart
===========

O **quarksmart** é uma biblioteca Python que permite a integração entre ferramentas de Data Science (como o Jupyter Notebooks) 
com os dados armazenados no sistema `QuarkSmart <https://quarkbi.esig.com.br>`_.

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

Contributing
============

Please read `QuarkSmart <https://quarkbi.esig.com.br>`_ for details on our code of conduct, and the process for submitting pull requests to us.

Versioning
============

We use `QuarkSmart <https://quarkbi.esig.com.br>`_ for versioning. For the versions available, see the `QuarkSmart <https://quarkbi.esig.com.br>`_. 

Authors
============

* **Billie Thompson** - *Initial work* - `QuarkSmart <https://quarkbi.esig.com.br>`_

See also the list of `QuarkSmart <https://quarkbi.esig.com.br>`_ who participated in this project.

License
============

This project is licensed under the MIT License - see the `QuarkSmart <https://quarkbi.esig.com.br>`_ file for details

Design
--------------------

.. toctree::
   index
   sobre
