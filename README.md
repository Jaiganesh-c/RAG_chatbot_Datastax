# RAG_chatbot_Datastax
Retrieval Augmented Generation for AI Chatbots

Overview
Learn how to use Retrieval Augmented Generation (RAG), a key technique for building custom chatbots using your data. RAG performs a vector similarity search to add supplemental context to a Large Language Model (LLM) query.

New to these concepts? See Overview.

open in colab
Prerequisites
An Astra Vector Search database is required. If you already have one, skip to Prepare for using your vector database, or take a couple of minutes to create one with the following instructions.

Create a serverless database with Vector Search
You are required to create a serverless Astra database with Vector Search before using its capacities to work with data. Details to consider precede the procedural steps.

Considerations
As you create a serverless Astra database with Vector Search, fill out the required fields according to these rules:

Database Name: Name your database something meaningful. The database name cannot be altered after the database is created.

Keyspace Name: Name your keyspace to reflect your data model; where all of your tables are stored within the database. You cannot name your keyspace dse or system. Use only alphanumeric characters and no more than 48 total characters. The Vector Search examples use vsearch as the keyspace name.

Provider: Choose a provider from one of the three major cloud providers; Amazon Web Services (AWS), Google Cloud (GCP), or Microsoft Azure.

When using the free plan, only the Google Cloud region is available for a serverless Astra database with Vector Search.

Region: The region associated with the chosen provider automatically populates this field.

Deploy a serverless Astra database with Vector Search
Configure the basic details to create a serverless Astra database with Vector Search.

In your Astra DB dashboard, select Create Database.

Select Serverless (with Vector).

Enter your database details:

Database Name.

Keyspace Name.

Choose a Provider.

Select Create Database.

When this database is active, a green notification appears at the top of your screen. Your Astra database with Vector Search is ready to use for your content.

Prepare for using your vector database
Create a token and download your Secure Connect Bundle (SCB) for your application.

Select your database and then click on the Connect tab.

Get an application token using the Generate token button in the Quick Start section.

Make sure you download the <db-name>-token.json file to use later.

Use the Get Bundle button to generate and download your Secure Connect Bundle (SCB).

Get an OpenAI API key to generate embeddings.

This example requires you to generate text embeddings and to obtain an OpenAI API key. Get the key by visiting platform.openai.com, or by logging into your OpenAI account, selecting your profile in the top right, and selecting API Keys.

Now you are ready to run this example from a Python Jupyter notebook. Launch Retrieval Augmented Generation for AI Chatbots Quickstart Colab.
