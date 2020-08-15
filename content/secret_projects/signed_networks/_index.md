---
title: "Signed networks - or how can you understand sentiment in a network"
date: 2019-03-23T13:25:26Z
draft: false
---


Research in the **complex network** domain seems to converge on the idea that, unlike other types of networks (e.g., technological and biological), **social networks** (e.g., online social networks and scientific collaboration networks) share a distinctive empirical regularity: that the number of neighbouring nodes tend to be correlated. Nodes with many friends are connected with nodes that have many friends, while nodes with few friends are connected with nodes with few friends. It is possible to quantitatively evaluate this through the correlation of the number of connections of a node with the number of the average connections of its neighbours.

Let me give you a simple example. Node i posses five friends, and its five friends have on average five friends as well (someone can have 6 and another 4, but the average number of friends would still be 5). We say that node i’s “degree” is correlated with its neighbors. The opposite situation sees node i with five friends who have just node i as a friend. We say that node i‘s degree is anticorrelated with its neighbours. The tendency of nodes with (dis)similar degrees to connect with each other is often referred to as ”(dis)assortative mixing by degree”.

Signed social networks are not new in sociological and psychological literature. There are many works on this subject. Among them,  is the theory of cognitive dissonance: an individual who experiences inconsistency (dissonance) tends to become psychologically uncomfortable, and is motivated to try to reduce this dissonance. This means that in triadic relationships we will find an abundance of balanced triads, i.e. situations where we have only positive relations between three connected people or only two negative links, which reflect, respectively, the fact that “the friend of my friend is my friend” and “the enemy of my enemy is my friend“. When a network has only positive balanced triads, it is said to be structurally balanced.

Relatively little attention has been devoted to the emergence of degree correlations in signed social networks, i.e. networks where we have a mixture of positive and negative ties between individuals. In particular, we have difficulty finding negative networks, where individuals are connected through links with a negative connotation (e.g., distrust, enmity, and competition). Do individuals who like (dislike) many others tend to like (dislike) each other, or do they like (dislike) those who like (dislike) only very few others? 

We start by analysing the two whole social networks, treating them as unsigned network. We find that both networks have the usual social networks characteristics: both are assortative. Our aim is to test whether the sign of the link affects the structure of the network: do we create ties with each other in a different way based on the nature of the connection? In order to test that, we split the whole network into two sub-networks with only positive and only negative links (see Fig.1).

<figure>
  <img src="/img_l/signed_networks/figure_1.png#floatright"/>
</figure>


On the right hand side figure (Fig.1) we can observe the division of the whole signed network (a) into two sub-networks with only positive (b) and only negative (c) links.

We then ran the network measure over these two datasets (two for each analysed social network). Results are quite interesting: the positive sub-network is assortative while the negative one is disassortative. This reflects the fact that individuals that have many negative ties are negatively connected with individuals that have few negative relations, while individuals that have many, or few, positive ties are positively connected with individuals that have respectively, many or few positive ties.

<figure>
  <img src="/img_l/signed_networks/figure_2.png#floatleft"/>
</figure>


The left hand side figure (Fig.2) shows a subset of Slashdot’s network. Red links represent negative relationships between nodes, green links positive ones. From this picture it is clear that the way with which nodes connected is influenced by the nature of the relationships: people that make many enemies are connected with people that make few enemies, while the opposite happens for friend relationships.


We were curious to understand why this happens. Is it possible to find the mechanisms that reproduce these two distinctive patterns for the positive and the negative sub-networks? We propose a model to analyse the interplay between network topology and sign of links, and uncover the conditions that underpin the emergence of the degree correlations observed in the data.

The model is simple: we first create a network which is assortative; we label every node with two possible label, A or B, with different probability: a node belongs to the group A with probability _m_, while with probability 1-m to group B (see Fig.3). Once everything is ready, we must find a 
<figure>
  <img src="/img_l/signed_networks/figure_3.png#floatright"/>
</figure>
rule to assign a sign over each link: links within a group are positive while links across groups are negative.



In order to reproduce the empirical finding we found three fundamental mechanisms: 

- an assortative unsigned network;
- the groups of nodes are of different size;
- the signed global network is structurally balanced.


If I have made you curious, you can find more about this work [here](https://www.sciencedirect.com/science/article/pii/S0378437114010334).

V. Ciotti, G. Bianconi, A. Capocci, F. Colaiori, and P. Panzarasa (2015). Degree correlations in signed social networks. Physica A: Statistical Mechanics and its Applications 422: 25-39
