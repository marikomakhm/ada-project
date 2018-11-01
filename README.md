# Title

# Abstract
A 150 word description of the project idea, goals, dataset used. What story you would like to tell and why? What's the motivation behind your project?

To measure the growth of a society there are various metrics that can be used, for instance the happiness of the country (World Happiness Report) or GDP per capita. These metrics are affected by socioeconomic factors such as levels of education, unemployment, fertility rates, etc. In this project, we would like to study how these socioeconomic indicators of development impact the different metrics used to determine the growth of a country, and which indicators best represent the growth of a community. We will be using datasets provided by the UN and the World Bank to study the socioeconomic situations of countries worldwide.

# Research questions
We would like to address the following research questions:

- how do we measure the growth of a country?

- what is the impact of the education (literacy rates, enrolment in primary/secondary/tertiary education) in a country on its growth?
- what is the impact of fertility rates of a country on its growth?
- what is the impact of inflow/outflow of foreign migrants of a country on its growth?

# Dataset

The datasets we intend to use are the following datasets provided by the UN and the World Bank:

UN datasets:

- Gender Development Index: http://data.un.org/DocumentData.aspx?id=380
- Gender Inequality Index: http://data.un.org/DocumentData.aspx?id=381
- Data on refugees: http://data.un.org/Data.aspx?q=refugee&d=UNHCR&f=indID%3AType-Ref
- Total fertility rate: http://data.un.org/Data.aspx?d=SOWC&f=inID%3a127
- Net migration rate: http://data.un.org/Data.aspx?q=migration&d=PopDiv&f=variableID%3A85
- GDP per capita, PPP: http://data.un.org/Data.aspx?d=WDI&f=Indicator_Code%3aNY.GDP.PCAP.PP.CD
- GDP per capita: http://data.un.org/Data.aspx?q=gdp&d=SNAAMA&f=grID%3A101%3BcurrID%3AUSD%3BpcFlag%3A1
- Trade of goods: http://data.un.org/Data.aspx?d=ComTrade&f=_l1Code%3A1
- Population by literacy, age, sex and rural/urban residence: http://data.un.org/Data.aspx?d=POP&f=tableCode%3A31

World Bank datasets:

- [datasets]

Each of these datasets contains relevant data, dating from 2011 onwards. The datasets chosen are as complete as possible, each of them containing information for at least 120 countries.

We intend to clean the datasets, extracting the information that interests us. We will have to deal with countries that are not part of certain datasets, and decide if we want to study all countries worldwide or not. It would make no sense to study a country if we do not have sufficient information about it. However, we will have to evaluate the "sufficient information" threshold when doing data cleaning and merging the data based on each country.

Something that is going to be crucial in our data processing, is choosing consistent country names, as countries can be recorded differently, for instance "Iran" can be recorded as "Islamic Republic of Iran".

One dataset that we are particularly excited to use is about refugees, from the UNHCR statistical database. It has the following format:

| Country or territory of asylum or residence | Country or territory of origin | Year | Refugees | Refugees assisted by UNHCR | Total refugees and people in refugee-like situations | Total refugees and people in refugee-like situations assisted by UNHCR |
| ------------------------------------------- | ------------------------------ | ---- | -------- | -------------------------- | ---------------------------------------------------- | ------------------------------------------------------------ |
| Afghanistan                                 | Iraq                           | 2016 | 1        | 1                          | 1                                                    | 1                                                            |
| Afghanistan                                 | Pakistan                       | 2016 | 59737    | 59737                      | 59737                                                | 59737                                                        |
| Angola                                      | Eritrea                        | 2016 | 34       |                            | 34                                                   |                                                              |
| Oman                                        | Syrian Arab Rep.               | 2016 | 7        | 7                          | 7                                                    | 7                                                            |
| Switzerland                                 | Nigeria                        | 2015 | 179      |                            | 179                                                  |                                                              |

Here, we see that sometimes we obtain empty cells for the number of refugees assisted by UNHCR. In these cases, we would have to map the empty cells to 0 values, rather than simply remove them.

List the dataset(s) you want to use, and some ideas on how do you expect to get, manage, process and enrich it/them. Show us you've read the docs and some examples, and you've a clear idea on what to expect. Discuss data size and format if relevant.

# A list of internal milestones up until project milestone 2
Add here a sketch of your planning for the next project milestone.

# Questions for TA
Add here some questions you have for us, in general or project-specific.
