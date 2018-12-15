---
layout: page
title: Data
permalink: /datastory2/
---
# Hide and seek: the money edition

## Introduction
The Panama Papers scandal erupted in 2015 after an anonymous whistle-blower nicknamed "John Doe" leaked over 11.5 million documents from a law firm in Panama called Mossack Fonseca. The documents, published by the International Consortium of Investigative Journalists, revealed a huge web of over 214'488 shell companies, that were partially used for the purpose of fraud, tax evasion and escaping international sanctions.

The documents also implicated several high profile personalities in the affair, such as sportspeople, actors and even the Queen of England. They also showed that several people and companies blacklisted by the U.S. government, for crimes such as collaborating with drug lords, terrorists or "rogue nations" such as Iran and North Korea, used these shell companies to escape sanctions. More importantly, they revealed that a large number of politicians, many of whom were campaigning on anti-corruption platforms, were also involved. Some notable mentions were the prime minister of Iceland, the king of Saudi Arabia, former British Prime Minister David Cameron, and Chinese President Xi Jinping.

The whistle-blower claimed his reasons for leaking the documents was the growing income inequality and an understanding of the injustices and corruption that were taking place. But this begs the question, can we explain the involvement in this affair using socioeconomic factors? Is it simply high taxes that led these poor rich people to hide their money away? Are people in richer countries more likely to be involved? What about more corrupt countries? How are the people implicated in this affair linked? These are a few of the questions we'll try to answer in this DATA STORY. (TODO)

## What was in the data?
We had a total of five Panama Papers datasets at our disposal. These datasets represent a graph, with three datasets containing three distinct types of nodes, as well as a dataset containing edges linking the nodes. The nodes are people and organizations involved in the Panama Papers. The fifth dataset contains the addresses of these people and organizations. Here's a breakdown on the three types of nodes we have:

- **Entities:** offshore entities are companies, trusts or funds created by agents in low-tax jurisdictions that typically attract non-resident clients through preferential tax treatment. Agents are firms in offshore jurisdictions that manage offshore entities at their clients' request.
- **Officers:** officers are people or companies that play some role in an offshore entity. These are typically shareholders and beneficiaries of the offshore companies.
- **Intermediaries:** intermediaries are the lawyers and service providers who helped set up offshore entities.

TODO: add diagram

## Which countries were involved?
The very first question we asked ourselves was which countries were involved in the scandal and to what extent. Was it the usual suspects? Was it mostly rich countries? There are many ways of trying to compute their involvement, but our first attempt was to simply count the number of people and organizations involved and group them by country.  (TODO: bar chart) This yields the following table:

{% raw %}
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="100%" height="500" src="../ressources/bar_occurrences.html"></iframe>
{% endraw %}

Or when plotted in a world map:

{% raw %}
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="100%" height="500" src="../ressources/map_occurrences.html"></iframe>
{% endraw %}

By looking at these results, it seems that the most involved countries are a combination of the most populous countries in the world and tax havens.

(TODO: read text from here onwards)

We see little Switzerland almost in the lead, which seems to reinforce many of the clichés about the country. It seems cheese and watches are not the only thing Swiss people are good at. Similarly, Monaco, Luxembourg and British Virgin Islands are also present. And very near the top, we see Panama, which makes sense given the name.

We also see that there are quite a large number of very large countries, such as China, United States and Brazil. This however, is to be expected, as very large countries will naturally have more occurrences. Interestingly, this is not always the case, as we see India didn't even manage to crack the Top 20 list, even though it's the second most populated country in the world. This suggests that population alone doesn't tell the whole story, but we will look at this later. For now, let us look at the same data but normalized by population:

{% raw %}
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="100%" height="500" src="../ressources/bar_occurrences_per_hab.html"></iframe>
{% endraw %}

{% raw %}
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="100%" height="500" src="../ressources/map_occurences_per_hab.html"></iframe>
{% endraw %}

This data is much easier to interpret. We see that almost all of the countries on the top 20 list are countries that are typically known as "tax-havens", such as Seychelles, Cayman and Bermuda. We see however that all of them are dwarfed by the British Virgin Islands. For such a small island, being on both Top 20 lists shows that it was surely heavily involved in this affair.

This data indeed is corroborated by many news [reports](http://www.independent.com.mt/articles/2016-04-18/world-news/Panama-Papers-Tiny-British-Virgin-Islands-has-big-role-in-leaked-documents-6736156470) (FIND BETTER SOURCE), which seem to suggest that Panama, Switzerland, United Kingdom and many Commonwealth islands, particularly British Virgin Islands, were the countries most heavily involved in setting up this whole scheme.

So if population alone is not enough to explain the number of occurrences, can other socio-economic factors explain this? Let's have a look.

## Socioeconomic factors
Now we will try to find a correlation between the amount of involvement in Panama Papers of the three different types of node and different socioeconomic factors. We considered several different socioeconomic factors, but ultimately we decided to focus on:
- Human Development Index
- GDP per capita
- Gini coefficient (measures inequality)
- Income share of the 20% richest

To analyse the correlation, we will use the Pearson and Spearman coefficients between the number of occurrences normalized by populations size and the different factors. We will also look at the p-values to determine the degree of confidence in our analysis. We decided to use the number of occurrence in the Panama Papers normalized by the population size to avoid the bias brought by country that have a large population. Additionally, we also plotted these different results to see if they were similar to our "intuition".

### GDP per capita
The GDP per capita is the value of all the goods and services produced by a country in one year. It therefore represents approximately how rich a country is. We chose to use this indicator because we thought that richer people might have more incentive to try to evade the tax system. We will go deeper in the analyze later. 

Now we'll have a look at the scatter plot of GDP vs number of occurrences normalized in the Panama Papers.
{% raw %}

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="100%" height="500" src="../ressources/scatter_gdp_count_normalized.html"></iframe>
{% endraw %}


There is no evident correlation even if the spearman coefficient suggests it.
Most of the points have a very low number of occurrence in the Panama Papers and there are a few outliers. Those outliers are again mainly either the fiscal paradise or the country that were involved in setting up this scheme (British Virgin Islands, Luxembourg, Bermuda, etc.). As we're plotting the number of occurrences normalized, we would expect such countries to stand out. Since we are interested in finding general patterns, we'll remove the outliers to study the correlations for the majority of the countries.

{% raw %}
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="100%" height="500" src="../ressources/scatter_gdp_count_outlier.html"></iframe>
{% endraw %}

	Total references
	pearson :  0.12165059315598446 ; p-val:  0.23033496857175298
	spearman :  0.5385112508104001 ; p-val:  8.959416567754556e-09

Even if on this graph the correlation are smaller, it is can better see the pattern that the number are suggesting. We observe that countries where the GDP is higher appear more often in the Panama Papers. Again, this is what we would intuitively predict.
Richer countries have usually better infrastructure and therefore have a system to ensure that the taxes are actually collected.
This provides a much larger incentive for people to try to evade this systems by any means they can, which leads to scandals such as this one.


### Impact of inequality
In this section will analyze if there is a correlation between the number of occurrence in the Panama papers and between two different indicators that try to determine the inequality in a country.
#### Gini
The Gini coefficient measures the inequality in the distribution of wealth in a country (lower coefficient means lower inequality). The most equal equal society is when every person get the same income (When gini = 0). Our initial assumption was that countries in which there is high levels of income inequality would be more heavily involved in this affair, as this is generally heavily linked with corruption and tax evasion.

This time we directly show the scatter plot without the outliers by using the techniques we described above.

{% raw %}
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="100%" height="500" src="../ressources/scatter_gini_count_outlier.html"></iframe>
{% endraw %}


	Total references
	pearson :  -0.027051310386034675 ; p-val:  0.8177976273022307
	spearman :  -0.09558222096389055 ; p-val:  0.41465273285911763


As we can see in the table above, the correlation between the number of occurrence and the Gini coefficient is not really relevant as the high p-value suggests. 

We can then reject our initial hypothesis. It seems like there is no link between the inequality in a country and the number of references in the Panama Papers.

This is surprising because intuitively we would imagine 
This could be because:

// TODO: say why gini doesn't work

#### Income held by top 20%
This index also measures inequality but it quantifies it differently by expressing the share of wealth held to the top 20% richest. We would expect similar results as for the Gini coefficient since  both indices are measuring inequality.

{% raw %}
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="100%" height="500" src="../ressources/scatter_20_count_outliers.html"></iframe>
{% endraw %}

As we can observe, there is almost no correlation which is coherent with what we said before.

#### Human Development Index (HDI)

The HDI index try to represent how well a country is developed by using the lifespan, the education level and the GDP per capita of an average citizen. \
Let's see if there is a correlation between the HDI and the number of occurrence in this affair.

{% raw %}
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="100%" height="500" src="../ressources/scatter_hdi_count_outlier.html"></iframe>
{% endraw %}

	Total references
	pearson :  0.23480729070912107 ; p-val:  0.021995627233654214
	spearman :  0.48046530551766936 ; p-val:  8.324509404392334e-07

There seems to be a correlation as the plot and the Spearman coefficient suggest.
One of the reasons could be that a country with higher HDI have generally a better infrastructures to ensure that the tax are paid. Additionally, a country with higher HDI is home to richer people since the GDP per capita is also taken into account in the calculation of the HDI.

TODO: socioeconomic factors conclusion

We've studied the involvement of each country in Panama Papers, but we know that a significant part of the information about countries involved resides in how they interact with other countries involved in the affair. Let's have a look at how the countries interact, shall we?

## International links

One of the most representative measures of displaying international links is to do so on a world map. Below, we display a world map with undirected edges representing the number of connections between any two countries, with the width indicating the number of connections:

{% raw %}

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="100%" height="500" src="../ressources/international_links_map.html"></iframe>

{% endraw %}

There is a clear transatlantic bridge being built between Central America and Central Europe. This isn't surprising, considering that a large number of tax havens are situated in Central America and the Channel Islands (todo: is this true), as well as Mossack Fonseca being based in Panama, and Switzerland's global tax haven reputation.

There's also a noticeable edge between China and Hong Kong. Having studied the data, this is majorly due to over 20000 edges originating in China and going to Hong Kong, justifying the magnitude of the edge. Interestingly, China appears to significantly rely on Hong Kong for all business stuff (todo: find a word).

Interestingly, we also see some "international link hubs", such as UAE, Seychelles and Samoa. (todo: what can we say about these countries)

Although this representation of international edges gives us an idea of who interacts with whom in a geographic sense, it would be interesting to see which country is the most important one in terms of international transactions. We refer on a network representation of international links to answer this question.

#### Who's at the center of it all?



{% raw %}

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width="100%" height="500" src="../ressources/international_links_network.html"></iframe>

{% endraw %}