# CeneoScrapper
## Stage 1 - extraction of all components for a single opinion
1. extraction of single web page content
2. analysis of single a opinions' structure

|  Component   |                                   CSS selector                                  |   Var name   |Data type|
|--------------|---------------------------------------------------------------------------------|--------------|---------|
|Opinion       |div.user-post__card                                                              |opinion       |dict     |
|Opinion ID    |["data-entry-id"]                                                                |opinion_id    |str      |
|Author        |span.user-post__author-name                                                      |author        |str      |
|Recommendation|span.user-post__author-recomendation > em                                        |recommendation|bool     |
|Rating        |span.user-post__score-count                                                      |stars         |float    |
|Content       |div.user-post__text                                                              |content       |str      |
|Advantages    |div.review-feature__col:has(> div[class&="positives"]) > div.review-feature__item|pros          |list(str)|
|Disadvatages  |div.review-feature__col:has(> div[class&="negatives"]) > div.review-feature__item|cons          |list(str)|
|Verification  |div.review-pz                                                                    |verified      |bool     |
|Post Date     |span.user-post__published > time:nth-child(1)["datetime"]                        |post_date     |date     |
|Purchase Date |span.user-post__published > time:nth-child(2)["datetime"]                        |purchase_date |date     |
|Usefulness    |span[id^="votes-yes"]                                                            |usefulness    |int      |
|Uselessness   |span[id^="votes-no"]                                                             |uselessness   |int      |

3. extraction of single opinion components
4. transformation of extracted data to given data types

## Stage 2 - extraction of all opinions from a single page
1. Definition of a dictionary to store all components of a single opinion.
2. Definition of a list for storing the dictionaries.
3. Implementation of loop traversing through all opinions from a single page.

## Stage 3 - extraction of all opinions for a single product
1. Implementation of loop traversing through consecutive pages with opinions.
2. Loading extracted opinions to .json file.
3. Parameterization of product ID and reading product ID from standard input.

## Stage 4 - code refactoring
1. Implementation of a component extraction function.
2. Using dictionary with components selectors and comprehension for the representation of a single opinion.

## Stage 5 - statistical analysis of the extracted opinions
1. Displaying a list of products for each opinion that has been extracted.
2. 

## Stage 6 - drawing charts based on the given data