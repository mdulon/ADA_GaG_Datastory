# Temporary tuto
### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/mdulon/ADA_GaG_Datastory/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.





## Data preprocessing

Only selecting sport quotes of years from 2015 to 2020 from Quotebank

(Add proportion of sport quotes among all other quotes ?)





## Exploring data
### All sport quotes speakers : occupation distribution

Among all sport quotes, we are looking at the distribution of the speakers' occupations. 

![sport_quotes_occupation_distribution](/gh-pages/assets/occupation/all_speakers.png)
Footballer first (# %) and second politician (# %).
We see that the second most present occupation in theses sport quotes is politician which may be surprising at first sight. And that's why it may be interesting to further analyse this phenomenon. 

Second plot with only politicians ?




### Politicians : occupation distribution

For the rest of the analysis, we consider as "politician" a person with a politicial party. We realize that for our analysis this would make a lot more sense. 

Our analysis of speaker occupancy has been broken down into 3 parts according to the number of different occupations for each speaker. 

(Add plot of proportion of 3 parts ?)


#### Speakers with a single occupation

The distribution of occupancies for speakers with a single occupation is shown below. 

![politicians_occupation_distribution_1_occupation](/gh-pages/assets/occupation/politicians_1_occupation.png)


#### Speakers with multiple occupations including politics

The distribution of occupancies for speakers with multiple occupations including politics is shown below. 

![politicians_occupation_distribution_politics](/gh-pages/assets/occupation/politicians_politics.png)

-> bcp de politicians font autre chose (lawyer...), résultat attendu

#### Speakers with multiple occupations excluding politics

The distribution of occupancies for speakers with multiple occupations excluding politics is shown below. 

![politicians_occupation_distribution_1_non_politics](/gh-pages/assets/occupation/politicians_no_politics.png)

Thanks to this pie chart, we see that the most represented occupation is actor. 
This can be interpreted as following, famous people often having a political party take advantage of their popularity to convey poltical opinions.

This is interesting to consider these people as "politician" for us because we are interested in the political messages conveyed, not only by politicians but more broadly by individuals involved in politics.


-> les gens qui ont un parti sont souvent des politicians 




### Which political parties & politicians are most present in the sports quotes

#### Parties

![most_present_political_parties](/gh-pages/assets/most_present/parties.png)

We can observe that Democrats and Republicans are mostly represented but we can also notice the presence of many smaller parties.

These 2 parties stand out the most because the quotes are English speaking, so it seems quite logical that the main parties of English speaking countries are most represented. 

#### Politicians : 

![most_present_politicians](/gh-pages/assets/most_present/politicians.png)

à voir avec la nouvelle fonction de Nicolas

-> personnes qui ressortent le plus ?

## How much of the sport quotes among each media is politics related?



## How does this phenomenon evolve over time? For instance, does it increase before elections?




## What are the more represented topics in sport quotes?

We are now interested in figuring out if the sport quotes said by politicians are actually related to politics. 

In order to answer this question, we perform a topic analysis on all theses sport quotes said by politicians. 

Using LDA, we find the more likely topic for each quote, the graph below shows the evolution of the porportion of theses 4 topics over years.  

![topics](/gh-pages/assets/topics/topics.png)

