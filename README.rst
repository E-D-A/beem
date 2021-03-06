beem - Unofficial Python Library for Steem
===============================================

beem is an unofficial python library for steem, which is created new from scratch from `python-bitshares`_
The library name is derived from a beam maschine, similar to the analogy between steem and steam. beem includes `python-graphenelib`_.

.. image:: https://img.shields.io/pypi/v/beem.svg
    :target: https://pypi.python.org/pypi/beem/
    :alt: Latest Version

.. image:: https://img.shields.io/pypi/pyversions/beem.svg
    :target: https://pypi.python.org/pypi/beem/
    :alt: Python Versions
    

.. image:: https://anaconda.org/conda-forge/beem/badges/version.svg   
    :target: https://anaconda.org/conda-forge/beem
  
.. image:: https://anaconda.org/conda-forge/beem/badges/downloads.svg   
    :target: https://anaconda.org/conda-forge/beem


Current build status
--------------------

.. image:: https://travis-ci.org/holgern/beem.svg?branch=master
    :target: https://travis-ci.org/holgern/beem

.. image:: https://ci.appveyor.com/api/projects/status/ig8oqp8bt2fmr09a?svg=true
    :target: https://ci.appveyor.com/project/holger80/beem

.. image:: https://circleci.com/gh/holgern/beem.svg?style=svg
    :target: https://circleci.com/gh/holgern/beem

.. image:: https://readthedocs.org/projects/beem/badge/?version=latest
  :target: http://beem.readthedocs.org/en/latest/?badge=latest

.. image:: https://api.codacy.com/project/badge/Grade/e5476faf97df4c658697b8e7a7efebd7    
    :target: https://www.codacy.com/app/holgern/beem?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=holgern/beem&amp;utm_campaign=Badge_Grade

.. image:: https://api.codeclimate.com/v1/badges/e7bdb5b4aa7ab160a780/test_coverage
   :target: https://codeclimate.com/github/holgern/beem/test_coverage
   :alt: Test Coverage

Support
=======
You may find help at https://discord.gg/4HM592V. The discord channel can also be used to discuss things about beem.

Installation
============
The minimal working python version is 2.7.x. or 3.4.x

beem can be installed parallel to python-steem.

For Debian and Ubuntu, please ensure that the following packages are installed:
        
.. code:: bash

    sudo apt-get install build-essential libssl-dev python-dev

For Fedora and RHEL-derivatives, please ensure that the following packages are installed:

.. code:: bash

    sudo yum install gcc openssl-devel python-devel

For OSX, please do the following::

    brew install openssl
    export CFLAGS="-I$(brew --prefix openssl)/include $CFLAGS"
    export LDFLAGS="-L$(brew --prefix openssl)/lib $LDFLAGS"

For Termux on Android, please install the following packages:

.. code:: bash

    pkg install clang openssl-dev python-dev

Signing and Verify can be fasten (200 %) by installing cryptography:

.. code:: bash

    pip install -U cryptography
    
Install beem by pip::

    pip install -U beem
    
You can install beem from this repository if you want the latest
but possibly non-compiling version::

    git clone https://github.com/holgern/beem.git
    cd beem
    python setup.py build
    
    python setup.py install --user

Run tests after install::

    pytest
    
    
Installing beem with conda-forge
--------------------------------

Installing beem from the conda-forge channel can be achieved by adding conda-forge to your channels with::

    conda config --add channels conda-forge
    
Once the conda-forge channel has been enabled, beem can be installed with::

    conda install beem

Signing and Verify can be fasten (200 %) by installing cryptography::

    conda install cryptography
    

CLI tool bundled
----------------
I started to work on a CLI tool::

    beempy

Documentation
=============
Documentation is available at http://beem.readthedocs.io/en/latest/

Changelog
=========
0.19.23
-------
* new function for beempy added: power, follower, following, muter, muting, mute, nextnode, pingnode, currentnode 
* support for read-only systems added
* more unit tests
* Several improvements and bug fixes

0.19.22
-------
* beempy (command line tool) improved and all missing functions which are available in steempy are added
* new functions to beempy added: witnesses, walletinfo, openorders, orderbook and claimreward
* unit tests for cli added

0.19.21
-------
* Transactionbuilder and Wallet improved
* Accounts with more than one authority can be used for signing
* Examples added
* reconstruct_tx added to sign and addSigningInformation
* proposer from Transactionbuilder removed, as it had no function
* rshares_to_vote_pct added

0.19.20
-------
* serveral bug fixes and improvements
* coverage improved
* rpc improvements
* Native appbase support for broadcasting transactions added
* Native appbase support for Transfer added

0.19.19
-------
* serveral bug fixes and improvements
* coverage improved
* steem.get_blockchain_version added
* post and comment_options moved from beem.commment to beem.steem
* wait_for_and_get_block improved
* num_retries handling improved
* block_numbers can be set as start and stop in account.history and account.history_reverse, when use_block_num=True (default)

0.19.18
-------
* bug fix release

0.19.17
-------
* GOLOS chain added
* Huge speed improvements for all sign/verify operations (around 200%) when secp256k1 can not be installed and cryptography is installed
* benchmark added
* Example for speed comparison with steem-python added
* Several bug fixes and improvements

0.19.16
-------
* rename wallet.purge() and wallet.purgeWallet() to wallet.wipe()
* Handle internal node errors
* Account class improved
* Several improvements

0.19.15
-------
* bugfixes for testnet operations
* refactoring

0.19.14
-------
* batched api calls possible
* Threading added for websockets
* bug fixes

0.19.13
-------
* beem is now in the beta state, as now 270 unit tests exists
* unit tests added for appbase
* bug fixes for appbase-api calls

0.19.12
-------
* bug fix release for condenser_api

0.19.11
-------
* beem is appbase ready
* more examples added
* print_appbase_calls added
* https nodes can be used

0.19.10
-------
* Memo encryption/decryption fixed

0.19.9
------
* CLI tool improved
* bug fixes
* more unittests

0.19.8
------
* bug fixes
* CLI tool added
* beem added to conda-forge
* more unittests

0.19.7
------
* works on python 2.7
* can be installed besides steem-python
* graphenelib included
* unit tests added
* comment and account improved
* timezone added
* Delete_comment added

0.19.6
------
* Small bug-fix

0.19.5
------
* Market fixed
* Account, Comment, Discussion and Witness class improved
* Bug fixes

0.19.4
------
* New library name is now beem
* Upstream fixes from https://github.com/xeroc/python-bitshares
* Improved Docu

0.19.3
------
* Add Comment/Post
* Add Witness
* Several bugfixes
* Added all transactions that are supported from steem-python
* New library name planned: beem

0.19.2
------
* Notify and websocket fixed
* Several fixes

0.19.1
------
* Imported from https://github.com/xeroc/python-bitshares 
* Replaced all BitShares by Steem
* Flake8 fixed
* Unit tests are working
* renamed to beem
* Docs fixed
* Signing fixed
* pysteem: Account, Amount, Asset, Block, Blockchain, Instance, Memo, Message, Notify, Price, Steem, Transactionbuilder, Vote, Witness are working


License
=======
This library is licensed under the MIT License.

Acknowledgements
================
`python-bitshares`_ and `python-graphenelib`_ were created by Fabian Schuh (xeroc).


.. _python-graphenelib: https://github.com/xeroc/python-graphenelib
.. _python-bitshares: https://github.com/xeroc/python-bitshares
.. _Python: http://python.org
.. _Anaconda: https://www.continuum.io
