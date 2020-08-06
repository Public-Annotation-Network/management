# Public Annotation Network - PAN 🥘 🍕 🌶

Public Annotation Network (PAN) is a censorship-resistant web annotation service.

Project landing page: https://late-waterfall-9957.on.fleek.co/

## Why PAN?

Everyday our society becomes more dependant on centrally controlled platforms, such as social media.
But these social media sites can censor the information by deleting or mutating the content. They could even control what the users can or cannot see. 

Public web annotations provide users a transparent overview of information and opinions available on the internet. Although there are already a few (public) annotation softwares on the market, the existing services are mainly using centralized storage and hence are prone to censorship. 

That is why we are creating PAN. We are using IPFS and Ethereum to reduce the censorship attack vector.


## MVP Concept

Our browser extensions, PAN, allow users to annotate on any web pages. Users can sign annotations with their Ethereum address and publish annotations to the network. Annotation data is stored on IPFS. For better compatibility with other services, we adopt [W3C's Web Annotation Data Model](https://www.w3.org/TR/annotation-model/). There are two ways to submit annotations, users can either publish annotations directly to our network or submit via a publisher, who will then publish annotations in batches on behalf of the users. At last, an Ethreum smart contract registry is used to store references to each annotation and its annotator, ensuring that annotation data is immutable.

![PAN](https://github.com/Public-Annotation-Network/management/blob/master/product/2020-08-06%20PAN-diagram-revision1.png)

### 1. Browser Extension >> [Go to Repository](https://github.com/Public-Annotation-Network/extension)

The PAN browser extension is the primary medium through which users interact with the Public Annotation Network. By using the extension, users can retrieve published annotations that are already on the network or submit their own annotations in relation to specific webpages. 

### 2. Publisher >> [Go to Repository](https://github.com/Public-Annotation-Network/publisher)

The publisher is an optional quality of life component. Its primary objective is to make publishing annotations cheaper by batching multiple operations into a single Ethereum transaction. The more Ethereum transactions are batched together, the cheaper the act of publishing becomes. To provide further utility, the publisher service exposes a REST API that allows for easy querying of existing annotations and optimizing query performance by caching annotations in the registry.

### 3. Subgraph >> [Go to Repository](https://github.com/Public-Annotation-Network/subgraph)

The PAN Subgraph is an optional component of the architecture, mainly used to reduce query times. For every transaction, which stores a batch id on-chain, it indexes all annotations of the batch from IPFS and stores an additional reference (e.g. the tweet id and username) for the annotation. To obtain for example all annotations for a user or a tweet the extension (or the publisher) submits a GraphQL query to the subgraph containing the username or the tweet id.


## Future of PAN

- Mainnet

- Incensitve system for publisher network

- Native interaction with IPFS and Ethereum

- Suitable business model

## Potential Use Cases

- Journalism

- Scientific Research

- Content Creation

- Civic Participation




