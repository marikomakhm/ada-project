# Who's the biggest tax evader?

# Abstract

The Panama Papers are a collection of leaked documents revealing that a large number of offshore entities had been used for fraud, evading international sanctions and large-scale tax evasion. A majority of these entities are linked to well-known public figures, from politicians to footballers. Many of these politicians were even directly involved in fighting tax evasion in their own country, showing a level of hypocrisy and corruption never seen before. But how far does this scandal go, and which countries have been most affected by it?

In this project, we will study which countries the people implicated in the Panama Papers come from and investigate the correlation with development indicators of these countries, using UN and World Bank datasets. We will be using indicators such as the Gini coefficient or the GDP per capita at PPP to attempt to explain the distribution of the number of entities involved in Panama Papers in each country. By studying the patterns of the countries involved in Panama Papers, we hope to better understand how to construct a healthier, more honest society.

# Research questions
We would like to address the following research questions:

- which countries have the most and least tax evasion?
- what does the distribution of the entities involved in Panama Papers look like?
- to what extent are we able to link the proportion of entities involved in Panama Papers with:
  - the political structure of a country?
  - the internal inequality within a country?
  - the development (HDI, Gini coefficient) of a country?

# Dataset

For this project, we will be using the Panama Papers dataset. We are going to study links between the distribution of the country of origin of the entities involved and various socioeconomic factors related to the country. To study this connection, we will also use datasets from the UN and the World Bank.

### Panama Papers dataset
We are using the standard dataset that is already on the server. In this section, we'll explain how the dataset is formatted and how we can exploit it.
The data are spread over 5 files:

#### panama_papers.nodes.entity.csv
Contains the list of all the offshore entites that were discovered. It contains dozens of fields but the followings are really usefull to us:
- node ID: unique identification of the entity
- juridiction: information about which juridiction is applied to the offshore company.
- severals dates: incorporation dates, inactivation dates, etc.

#### panama_papers.nodes.intermediary.csv
This file contains the lawyers and service providers who helped setting up offshore companies. 
- node ID: unique identification of the intermediary
- country: country of the intermediary
- status: indicates whether the company is still active

#### panama_papers.nodes.officer.csv
The file contains the shareholders and the beneficiaries of the offshore companies.
- node ID: unique identification of the officer
- name: name of the officer

#### panama_papers.nodes.address.csv
Contains the address of the entities, officiers and intermediary.
- node ID: unique identification of the address
- address: full address. If we want to use it, we'll have to parse this field.
- country code: country code of the address (string)

#### panama_papers.edges.csv
This is the most important file. It links all the above datasets together and allows us to understand the connections between them.

- start ID: contains the start ID of an edge
- end ID: contanis the end ID of an edge
- type of edge: describe the edges (intermediary of, registered address, etc.)

### Other datasets

We intend to use the following datasets provided by the UN and the World Bank:

UN datasets:
- GDP per capita, PPP: http://data.un.org/Data.aspx?d=WDI&f=Indicator_Code%3aNY.GDP.PCAP.PP.CD
- GDP per capita: http://data.un.org/Data.aspx?q=gdp&d=SNAAMA&f=grID%3A101%3BcurrID%3AUSD%3BpcFlag%3A1
- HDI and its components: http://data.un.org/DocumentData.aspx?q=hdi&id=377
- HDI trends, 1990–2014: http://data.un.org/DocumentData.aspx?q=hdi&id=378

World Bank datasets:
- Gini coefficients: https://data.worldbank.org/indicator/SI.POV.GINI
- Income share held by highest 10%: https://data.worldbank.org/indicator/SI.DST.10TH.10

Each of these datasets contains relevant data, dating from at least 2011 onwards. The datasets chosen are as complete as possible, each of them containing information for at least 120 countries.

We intend to clean these datasets, extracting the information that interests us. Something that is going to be crucial in our data processing is choosing consistent country names, as countries can be recorded differently, for instance "Iran" can be recorded as "Islamic Republic of Iran". We will base this on the country provided in the `panama_papers.nodes.address.csv` file.

# A list of internal milestones up until project milestone 2

Here is the plan for the next project milestone:
- Merge the datasets taken from the UN and World Bank on the country of interest
- Visualize the country of origin of the people involved in Panama Papers
- Visualize the development indicators taken from UN/WB datasets for each country
- Analyze links between the data from the UN/WB and Panama Papers countries using visual and numerical tools

# Questions for TA

No questions just yet! :smile: 