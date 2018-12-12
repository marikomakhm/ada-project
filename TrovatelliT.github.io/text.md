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
*To try to answer it, we simply counted the number of nodes by country.*  (Change this)

We get the following table:

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
|RUS| |Russia | 8389|
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

If we plot this on a map, we get the following result:

(INSERT MAP HERE)

This seems to be a mix of different countries and we can't see much of a connection. However, some of this countries are quite large so it's expected they will be much larger. If we normalize it by population, we get the following results:

(INSERT TABLE HERE)
(INSERT MAP HERE)

We clearly see a trend here. All of this countries are the "usual suspects", of countries typically known as tax havens. We see Monaco, Liechtenstein, Seychelles, Luxembourg, 
