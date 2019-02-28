# How To: Getting started in Hyperledger Composer and Fabric

The purpose of this repository is to get you started working on Hyperledger Fabric framework which is an all- purpose permissinoes blockchain where you can desing a business logic, code smart contracts, build and deploy a network that will follow the business logic. Composer is a tool for rapid prototyping that allows you tom build proof of concept ob the business network and that can be deployed and tested on an online playground, locally or on a server. Composer is ment to be a tool for testing and addoption but it is recomended tha in development to work directly on Fabric.

This How To will guide you to the documentation and tutorials of both Fabric and Composer and propose some exercises to get you started. It is based on the work we have been doing on [Blockchain for Open Science](http://blockchain4openscience.com/) and the [git repo](https://github.com/Blockchain4openscience) and a number of side projects that we have worked on over the last two years.

## Material

In this repo you can find three presentations that I prepared for a tutorial I gave on Blockchain at the [Biohackaton in Paris in November 2018](https://github.com/elixir-europe/BioHackathon/tree/master/interoperability/Using%20blockchain%20in%20biomedical%20provenance%20the%20identifiers%20use%20case)
This is a good stating point for our main project which is the scholarly wallet, the other presentations are a summary of the Fabric framework and the Composer tool.

## Composer

The best place to get started is to look at the [oficial documentation](https://hyperledger.github.io/composer/latest/) 

1. First use the online tutorial, the [Composer-Playground](https://composer-playground.mybluemix.net/) and follow a couple of examples: my-basic-sample or deploy some of the other samples like the marble or bond network.
The playground will give you the understanding og the elements that make up a business model, for example the participants, the assets and the transactions. Understand the business model and the business logic of the transactions that are coded using JS. 
2. You can complement your undertanding of the examples with the presentation [Introduction to Composer](https://github.com/ccastroiragorri/ComposerFabric101/blob/master/Introduction%20to%20Composer.pdf) or go directly to the [Playground Tutorial](https://hyperledger.github.io/composer/latest/tutorials/playground-tutorial)
3. You can export any business network archive (*.bna) that can be deployed onto a running fabric network.

## Fabric

After you play around with the on-line tutorial you might want to perform a local installation of the development enviorment. Currently you have the official documentation that is supporting [version 1.2](https://hyperledger.github.io/composer/latest/installing/development-tools.html) and [version 1.4](https://hyperledger-fabric.readthedocs.io/en/release-1.4/getting_started.html) (latest and first long term support release). 

1. Follow the installation instructions, this includes the [pre-requisites](https://hyperledger.github.io/composer/latest/installing/installing-prereqs)
2. Once installation is complete you can start a basic network locally for [version 1.2](https://hyperledger.github.io/composer/latest/tutorials/deploy-to-fabric-single-org) and [version 1.4](https://hyperledger-fabric.readthedocs.io/en/release-1.4/build_network.html) and deploy a *.bna file that contains the business logic of your network. This *.bna was previously build using composer language.

## Working with Fabric and Composer

The blockchain for open science project is currently focused on building a scholarly wallet that can track the provenance of different types of research objects that are intermediate inputs in the research process. So far we ahved designed the business logic using composer and then deploy this logic onto the most [basic network in Fabric](https://hyperledger.github.io/composer/latest/tutorials/deploy-to-fabric-single-org) using Fabric version 1.2.

1. The business logic behind the first version of the scholarly wallet is denoted as [bforos](https://github.com/Blockchain4openscience/hyperledger/tree/master/bforos3). You can upload the file  	'bforos@0.0.1.bna' to composer playground and follow the readme file.

2. [Instructions to deploy this business network onto Fabric](https://github.com/Blockchain4openscience/hyperledger)

3. [Instructions to deploy the business network onto Fabric and start a frontend application using Angular](https://github.com/Blockchain4openscience/B4OS-frontend)

## Working only with native Fabric

We are currently looking into the design the business logic directly using native Fabric, this is an important step to go beyond a proof of concept. The most recent version of Fabric (version 1.4) has an excellent example to do this base on the [PaperNet: Comercial Paper Tutorial](https://hyperledger-fabric.readthedocs.io/en/release-1.4/tutorial/commercial_paper.html)

1. [I wrote my own summary of this tutorial](https://github.com/ccastroiragorri/papernet/blob/master/README_Fabric_PaperNet.md)

2. It would be an interesting exercise to build a Composer example that follows the Comercial Paper Tutorial. Although there are already somo examples that consider a bond network or letters of credit (see Playgroud examples), however the idea is to build an example that shows the transition from Composer to native Fabric. I already [started to do this](https://github.com/ccastroiragorri/papernet). The model file is done (*.cto) still need to do the business logic.

