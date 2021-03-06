Creating a new DApp
===================

If you want to create a blank new app.

.. code:: bash

    $ embark new AppName
    $ cd AppName

To run Embark then in one console run:

.. code:: bash

    $ embark blockchain

And in another console run:

.. code:: bash

    $ embark run

DApp Structure
==============

.. code:: bash

      app/ # dapp code
      contracts/ #smart contracts
      config/
        |___ blockchain.json #rpc and blockchain configuration
        |___ contracts.json  #ethereum contracts configuration
        |___ storage.json  #ipfs configuration
        |___ communication.json  #whisper/orbit configuration
        |___ webserver.json  #dev webserver configuration
      test/
        |___ #contracts tests
      dist/
        |___ # build folder
      chains.json #keeps track of deployments in each chain

Solidity files in the contracts directory will automatically be deployed with ``embark run``. Changes in any files will automatically be reflected in app, changes to contracts will result in a redeployment and update of their JS Bindings

