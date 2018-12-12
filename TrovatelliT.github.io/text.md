---
layout: page
title: Data
permalink: /datastory2/
---
# Who's the biggest tax evader?
## Introduction
The Panama Papers scandal erupted in 2015 after an anonymous whistleblower  nicknamed "John Doe" leaked over 11.5 million documents from a law firm in Panama called Mossack Fonseca.
The documents, published by the International Consortium of Investigative Journalists, revealed a huge web of over 214'488 shell companies, that were partially used for the purpose of fraud, tax evasion and escaping international sanctions.

The documents also implicated several high profile personalities in the affair, such as sportspeople, actors and even the Queen of England. They also showed that several people and companies blacklisted by the U.S. government, for crimes such as collaborating with Drug lords, terrorists or "rogue nations" such as Iran and North Korea, used this shell companies to escape sanctions. More importantly, they  revealed that a large number of politicians, many of whom were campaigning on anti-corruption platforms, were also involved. Some notable mentions were Prime Minister of Iceland, the king of Saudi Arabia, previous British Prime minister David Cameron, and the Chinese leader Xi Jinping.

The whistleblower claimed his reasons for leaking the documents was the growing income inequality and an understanding of the injustices and corruption that were taking place. But this begs the question, can we explain the involvement in this affair using socio-economic factors? Is it simply high taxes that led these poor rich people to hide their money away? Are people in richer countries more likely to be involved? What about more corrupt countries? How are the people implicated in this affair linked? This are a few of the questions we'll try to answer in this DATA STORY.

## What was in the data?
We had a total of five Panama Papers datasets at our disposal. These datasets represent a graph, with three datasets containing three distinct types of nodes, as well as a dataset containing edges linking the nodes. The nodes are people and organizations involved in the Panama Papers. The fifth dataset contains the addresses of these people and organizations. Here's a breakdown on the three types of nodes we have:

- **Entities:** offshore entities are companies, trusts or funds created by agents in low-tax jurisdictions that typically attract non-resident clients through preferential tax treatment. Agents are firms in offshore jurisdictions that manage offshore entities at their clients' request.
- **Officers:** officers are people or companies that play some role in an offshore entity. These are typically shareholders and beneficiaries of the offshore companies.
- **Intermediaries:** intermediaries are the lawyers and service providers who helped set up offshore entities.

## Which countries were involved?
The very first question we asked ourselves which countries were involved in the scandal and to which extend. Was it the usual suspects? Was it mostly rich countries?
There are many ways of trying to compute their involvement, but our first attempt was to simply count the number of nodes in the 3 datasets by country. This yields the following table:

|Country Code |Name | Number of occurences |
| --- | --- | --- |
|HKG| Hong Kong | 53475|
|CHE| Switzerland | 43397|
|CHN| China | 28101|
|PAN| Panama | 21432|
|GBR |United Kingdom| 15900|
|LUX|  Luxembourg |12983|
|VGB | British Virgin Islands| 12368|
|ARE | United Arab Emirates| 10392|
|RUS |Russia | 8389|
|USA|United States | 7281|
|URY|     Uruguay | 7205|
|IMN| Isle of Man |7087|
|BHS|     Bahamas| 6532|
|TWN|      Taiwan|6466|
|SGP|   Singapore|6411|
|CYP|      Cyprus|6405|
|MCO|      Monaco|4670|
|BRA|      Brazil|3806|
|COL|    Colombia|3310|
|LIE|Liechtenstein|3266|

Or when plotted in a world map:

(INSERT WORLD MAP YO)

By looking at this results, it seems to be a weird combination of large countries and tax havens.

We see little Switzerland almost in the lead, which seems to reinforce many of the cliches about the country. It seems cheese and watches are not the only thing Swiss people are good at. Similarly, Monaco, Luxembourg and  British Virgin Islands are also present.

We also see that there are quite a large number of very large countries, such as China, United States and Brazil. This however, is to be expected, as very large countries will naturally have more occurrences. Interestingly, this is not always the case, as we see India didn't even manage to crack the Top 20 list, even though it's the second most populated country in the world. This suggests that population alone doesn't tell the whole story, but we will look at this later. For now, let us look at the same data but normalized by population:

(INSERT NORMALIZED TABLE HERE)

(INSERT WORLD MAP YO)

This data is much easier to interpret. We see that almost all of the countries on the top 20 list are countries that are typically known as "tax-havens", such as Seychelles, Cayman  and Bermuda. We see however that all of them are dwarfed by the British Virgin Islands. For such a small island, being on both Top 20 lists shows that it was surely heavily involved in this affair.

This data indeed is corroborated by many news [reports](http://www.independent.com.mt/articles/2016-04-18/world-news/Panama-Papers-Tiny-British-Virgin-Islands-has-big-role-in-leaked-documents-6736156470) (FIND BETTER SOURCE), which seem to suggest that Panama, Switzerland, United Kingdom and many Commonwealth islands, particularly British Virgin Islands, were the countries most heavily involved in setting up this whole scheme.

So if population alone is not enough to explain the number of occurences, can other socio-economic factors explain this? Let's have a look.
