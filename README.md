# Public Annotation Network - PAN 🥘 🍕 🌶

Public Annotation Network (PAN) is a censorship-resistant web annotation service.

Project landing page: https://late-waterfall-9957.on.fleek.co/

## Problems to Solve

The goal of having public annotations is to provide users a transparent overview of information and public opinions available on the internet. Although there are already a few (public) annotation softwares on the market that are open source, the existing services are mainly using centralized storage and hence are prone to censorship. 

## MVP Concept

Our browser extensions, PAN, allow users to annotate on any web pages. Users can sign annotations with their Ethereum address and publish annotations to the network. Annotation data is stored on IPFS. For better compatibility with other services, we adopt [W3C's Web Annotation Data Model](https://www.w3.org/TR/annotation-model/). There are two ways to submit annotations, users can either publish annotations directly to our network or submit via a publisher, who will then publish annotations in batches on behalf of the users. At last, an Ethreum smart contract registry is used to store references to each annotation and its annotator, ensuring that annotation data is immutable.

![PAN](https://github.com/Public-Annotation-Network/management/blob/master/product/2020-07-26%20PAN-Diagram.png)

### 1. Browser Extension >> [Go to Repository](https://github.com/Public-Annotation-Network/extension)

This component contributes the most to PAN user experience. By using the browser expension, users could retrieve published annotations that are already on the netowrk or submit their own annotations in relations to specific webpages.

### 2. Publisher >> [Go to Repository](https://github.com/Public-Annotation-Network/publisher)

[Add short description and how it works]

### 3. Subgraph >> [Go to Repository](https://github.com/Public-Annotation-Network/subgraph)

The PAN subgraph is an optional component of the architecture mainly to reduce query times. For every transaction which stores a batch id on-chain - it indexes all annotations of the batch from IPFS and stores an additional reference (e.g. the tweet id, username) for the annotation. To obtain for example all annotations for a user or a tweet the extension (or the publisher) submits a GraphQL query to the subgraph containing the username or the tweet id.

## Why do we design PAN this way?

### 1. Publishing Cost

[add explaination and how it works]

### 2. 


## Future of PAN

- Mainnet
- Incensitve system


## Potential Use Cases

### 1. Journalism

### 2. Scientific Research

### 3. Content Creation

### 4. Civic Participation




