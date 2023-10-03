# GenAI Learning Day demo/exercise material

## Setup

Create a python (3.8+) virtualenv and install the `requirements.txt`

Copy `cp .env.template .env` and get a DBA Token, a (vector) database ID,
an OpenAI key and optionally a keyspace name. Finally `source .env`.

Spin a notebook with `jupyter notebook` in the shell where you sourced the `.env`.

## Demo 1: Without Frameworks

**Prerequisite**:
populate the "philosopher" non-partitioned quote vector store
by running [this Colab](https://colab.research.google.com/github/openai/openai-cookbook/blob/main/examples/vector_databases/cassandra_astradb/Philosophical_Quotes_cassIO.ipynb) up to and including the
"Insert quotes into vector store" cell.

Then you can run the present `demo1` notebook.

## Demo 2: LangChain, QA

This is the simplest QA ever to show the mechanism.
