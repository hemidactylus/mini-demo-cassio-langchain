# GenAI Learning Day demo/exercise material

## Setup

Create a python (3.8+) virtualenv and install the `requirements.txt`

Copy `cp .env.template .env` and get a DBA Token, a (vector) database ID,
an OpenAI key and optionally a keyspace name. Finally `source .env`.

Spin a notebook with `jupyter notebook` in the shell where you sourced the `.env`.

## Demo 1: Without Frameworks

> _Note_: if you want to use a keyspace other than the default one for the DB, make sure you tweak running the prerequisites to point to that one as well (i.e. pass `keyspace='...'` explicitly in the `cassio.init(...)` call there as well). Check with the CQL console that the tables are created in the right keyspace.

**Prerequisite**:
populate the "philosopher" non-partitioned quote vector store
by running [this Colab](https://colab.research.google.com/github/openai/openai-cookbook/blob/main/examples/vector_databases/cassandra_astradb/Philosophical_Quotes_cassIO.ipynb) up to and including the
"Insert quotes into vector store" cell.

Then you can run the present `demo1` notebook.

## Demo 2: LangChain, QA

This is the simplest QA ever to show the mechanism.

Open the `demo2` notebook and run all cells.

## Demo 3: LangChain, agents

This shows something more convoluted
(and less trivial to do without a framework):
an agent repeatedly taking actions after observations
in a ReACT pattern.

Open the `demo3` notebook and run all cells.

## Demo 4: LangChain, vectors

A little more usages of vector stores in LangChain
(metadata filtering and MMR retrieval).

The pre-requisite is to have done `demo2`, so the store is not empty.

Open the `demo4` notebook and run the cells.

## Demo 5: LlamaIndex, vectors

This is the LlamaIndex equivalent of Demo 4: inserting documents into a vector store and querying it in various ways.

No pre-requisites, just open the notebook and run it end-to-end.
