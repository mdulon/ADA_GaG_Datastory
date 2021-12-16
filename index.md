# Politics in sport

## Introduction

Sport and politics have always been and will always be very closely related due to the high media coverage and the emotions involved. From the power demonstrations of nations such as as the Olympic games of Berlin 1936, going through movements such as the "black power" salute on the podium of 1968 Olympics games, to unification symbols such as the 1995 world cup organized and won by South Africa just after the end of apartheid. More recently, movements such as Black Lives Matters have been strongly supported by athletes while the US, Australia, UK and Canada announced a diplomatic boycott of Beijing 2022 Olympic games. 

All of these movements are well known political actions and show how strong the bond between sport and politics is. But what if they were just the tip of the iceberg ? Having a big dataset of quotes, the idea of this data story is to investigate the link between sports media and politics. How much a the quotes in sport article are related to politicians ? Are politicans trying to use sport and the related media coverage to influence the votes ? Are all the medias the same or certain are more politicized ? 

A lot of questions can be raised and the analysis can quickly become complexe. This datastory aims to bring an answer supported by data to certain of these questions.

## Data preprocessing

Only selecting sport quotes of years from 2015 to 2020 from Quotebank

(Add proportion of sport quotes among all other quotes ?)





## Exploring data
### All sport quotes speakers : occupation distribution

Among all sport quotes, we are looking at the distribution of the speakers' occupations. 

![sport_quotes_occupation_distribution](image/occupation/all_speakers.png)
Footballer first (# %) and second politician (# %).
We see that the second most present occupation in theses sport quotes is politician which may be surprising at first sight. And that's why it may be interesting to further analyse this phenomenon. 

Second plot with only politicians ?




### Politicians : occupation distribution

For the rest of the analysis, we consider as "politician" a person with a politicial party. We realize that for our analysis this would make a lot more sense. 

Our analysis of speaker occupancy has been broken down into 3 parts according to the number of different occupations for each speaker. 

(Add plot of proportion of 3 parts ?)


#### Speakers with a single occupation

The distribution of occupancies for speakers with a single occupation is shown below. 

![politicians_occupation_distribution_1_occupation](image/occupation/politicians_1_occupation.png)


#### Speakers with multiple occupations including politics

The distribution of occupancies for speakers with multiple occupations including politics is shown below. 

![politicians_occupation_distribution_politics](image/occupation/politicians_politics.png)

-> bcp de politicians font autre chose (lawyer...), résultat attendu

#### Speakers with multiple occupations excluding politics

The distribution of occupancies for speakers with multiple occupations excluding politics is shown below. 

![politicians_occupation_distribution_1_non_politics](image/occupation/politicians_no_politics.png)

Thanks to this pie chart, we see that the most represented occupation is actor. 
This can be interpreted as following, famous people often having a political party take advantage of their popularity to convey poltical opinions.

This is interesting to consider these people as "politician" for us because we are interested in the political messages conveyed, not only by politicians but more broadly by individuals involved in politics.


-> les gens qui ont un parti sont souvent des politicians 




### Which political parties & politicians are most present in the sports quotes

#### Parties

![most_present_political_parties](image/most_present/parties.png)

We can observe that Democrats and Republicans are mostly represented but we can also notice the presence of many smaller parties.

These 2 parties stand out the most because the quotes are English speaking, so it seems quite logical that the main parties of English speaking countries are most represented. 

#### Politicians : 

![most_present_politicians](image/most_present/politicians.png)

à voir avec la nouvelle fonction de Nicolas

-> personnes qui ressortent le plus ?

## How much of the sport quotes among each media is politics related?

So far it appears that quotes among sports media are actually linked to politics. However, we still wonder if all medias are the same regarding this bias. To do so, we can have a look to the proportion of political speakers among the different sports media. However, we have more than 2 000 different media sources, so we first need to pick a selection of them. Let's have look to the 30 biggest sports media in terms of number of sport quotes between 2015 and 2020 :

![](image/media_time_evolution/ranking.png 'Political speaker according to TOP 30 medias')

We can see that the 30 biggest medias have at least 300 000 quotes whereas only two medias really stand out : Yahoo and MSN with more than 2 million sport quotes.
Now, that we have this selection of sports media, let's see what the proportion of political speakers in sport quotes there is for each media : 

![](image/media_time_evolution/Political_speakers_by_media.png 'Political speaker according to TOP 30 medias')

As one can observe on this image, the proportion of political speakers among the different media ranges from 1.5% for Skysports to 71% for krmg. This seems to indicate that certain media are definitely more politicized than others and uses their sports section also for political reasons.

## How does this phenomenon evolve over time? For instance, does it increase before elections?

Another interesting question to ask is : how does the phenonenon of having politicized quotes in sports article evolves through time. For instance, does it increases during the during the campaigns of the US presedential elections ? 

To try to bring an answer, we wanted to have a look at the policized sports quotes each month over the years and here is what we obtained : 

![](image/media_time_evolution/mounth_frequency.png 'Mounth frequency of sport related quotes')

Unfortunately, as one can observe, it is not possible to identify any trends due to the huge variations of sports quotes through the years, itself related to the variation of all the quotes availble in the database at first. Indeed, we relate the drops in 2016 to the one mentionned in the [article about quotebank](https://dlab.epfl.ch/people/west/pub/Vaucher-Spitz-Catasta-West_WSDM-21.pdf).

However, another approach is to have a look at the media themselves and how their tendancies have evolved through time : 

![](image/media_time_evolution/STD.png 'Variation through the years')

This first graph shows the standard deviation of the percentage of politicised sports quotes over the 6 years of data. We can observe that certain media are very stable with a standard deviation inferior to 1% over 6 years, whereas other are highly unstable, reaching more than 26% for KRMG. This could be related to a change of internal policy or direction. 

To visualize better what is going on through the years for the most unstable medias, i.e. with a standard deviation superior to 10 :

![](image/media_time_evolution/variation.png 'Variation through the years')

We can observe that for instance that for MSN there is a downward trend with a sharp drop after 2015, but it stayed relatively stable afterwards. JDSupra shows no clear trends whereas the rest of the medias show relatively upward trends.


## What are the more represented topics in sport quotes?

We are now interested in figuring out if the sport quotes said by politicians are actually related to politics. 

In order to answer this question, we perform a topic analysis on all theses sport quotes said by politicians. 

Using LDA, we find the more likely topic for each quote, the graph below shows the evolution of the proportion of theses 4 topics over years.  

![topics](image/topics/topics.png 'Varation of topics in sport quotes said by politicians through years')


This graph shows that the politics-oriented sport quotes said by politician represents between 25% and 30%. Another topic very present topic encompasses daily life themes (30%-38%). Finally, the two last topics are obviously sport-related (30%-35%). 

We can also add that the percentage of politics-related sport quotes seems stable over years.

However, the conclusions of this topic analysis must be nuanced by the fact that it is sometimes even difficult for a human to correctly identify the topic of a quotation. This is due to the sometimes very short length of the content of the quote. It seems that the task is even more difficult for a machine. So it seems prudent not to get too attached to very precise results from this study.
