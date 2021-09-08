# 2PPy (tuProlog in Python)

Experimental porting of [2P-Kt](https://github.com/tuProlog/2p-kt) on Python, via [JPype](https://jpype.readthedocs.io).

> This is a __work in progress__. Py2P is not ready for general availability, yet.

## Introduction

Object-oriented and modular ecosystem for symbolic AI and logic programming, currently featuring:

* a module for logic terms and clauses representation, namely `tuprolog.core`,

* a module for logic unification, namely `tuprolog.unify`,

* a module for in-memory indexing and storing logic theories, as well as other sorts of collections of logic clauses, namely `tuprolog.theory`,

* a module providing generic API for resolution of logic queries, namely `tuprolog.solve`, currently implementing a Prolog solver

* two parsing modules: one aimed at parsing terms, namely `tuprolog.core.parsing`, and the other aimed at parsing theories, namely `tuprolog.theory.parsing`,

* two serialisation-related modules: one aimed at (de)serialising terms and clauses, namely `tuprolog.core.serialize`, and the 
other aimed at  (de)serialising terms theories, namely `tuprolog.theory.serialize`,

* a module for using Prolog via a command-line interface, namely `tuprolog.repl`.

## How to do stuff

### Prerequisites

1. Install Python 3 (look into the `.python-version` to know the exact version)
    * I suggest using [Pyenv](https://github.com/pyenv/pyenv) to easily handle multiple Python versions on the same machine
    * Ensure PIP works fine

2. Install Java (JDK preferred), and **ensure the `JAVA_HOME` variable is correctly set**

3. Ensure Java and Python are both either 64bit or 32bit

### How to develop Py2P

5. Restore Python dependencies via PIP, by running:
    ```bash
    pip install -r requirements.txt
    ```
    On __Mac OS__ this may not work as expected.
    Consider running the following command instead:
    ```bash
    python3 -m pip -r requirements.txt
    ```

6. Restore JVM dependencies via `download-jars.sh`, by running:
    ```bash
    ./download-jars.sh
    ```
    Notice that this command requires `curl` and `wget` to be installed on your system (`wget` may be lacking on __Mac OS__ and Windows)

### How to use Py2P as a library

1. Install Py2P from Pypi by running:
    ```bash
    pip install py2p
    ```
    On __Mac OS__ this may not work as expected.
    Consider running the following command instead:
    ```bash
    python3 -m pip install py2p
    ```
   
2. Import `tuprolog.*` modules in your Python scripts

3. Profit

### How to use Py2P as an executable

1. Install Py2P from Pypi by running:
    ```bash
    pip install py2p
    ```
    On __Mac OS__ this may not work as expected.
    Consider running the following command instead:
    ```bash
    python3 -m pip install py2p
    ```
   
2. Run Py2P via
   ```bash
   python -m py2p
   ```

For the moment, running Py2P means starting an interactive Python shell with pre-loaded Py2P modules.

Eventually `python -m py2p` will launch a command-line logic solver.
