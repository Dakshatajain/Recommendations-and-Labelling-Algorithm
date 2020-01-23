
### Recommendations for writing good job descriptions

__Objective:__

This project analyzes job postings for City of LA to suggest for improvements in the job postings that will fill in all the open positions. The analysis is explores various text mining and NLP techniques like readability and similarity to gather insights and suggest recommendations

__Data Overview:__

1. The data comes from an old competition posted by City of Los Angeles on Kaggle. The data consists of 684 plain text files. Each file represents a job posting. 
2. The key identifier of the job postings is the title of the posting along with the code which is included in the name of the file.
3. Each posting consists some or all of sections such as Open date, annual salary, requirements and/or duties, application process, selection procedure, qualification review and additional information.

__Data Source__: https://www.kaggle.com/c/data-science-for-good-city-of-los-angeles/data 

__Methodology:__
1. Plain Text Files to Dataframe 
2. Data Cleaning
3. Feature Engineering and insights: Features are extracted to conduct the analysis in following three areas:
    * a. Content - Readability, Similarity
    * b. Format - Completeness, Word count, spell check, complexity of selection process
    * c. Tone - Parts of Speech Tagging, Sentiment Analysis
4. Scoring and labelling postings  - a cumulative score for each job posting has been computed based on the above three criteria. This cumulative score can be used to rate the postings as good or bad (need improvement).
5. Recommendations and Conclusion 
6. Future Scope

__Analysis and Observations__:

Content : 
   1. Readability analysis using Flesch Kincaid and and Dale Chall scores indicate that approximately 92% of the entire postings, 26% of Requirement & 48% of Selection Process Sections are difficult to understand. Interaction effect also suggests that readability is not congruent with the level of education required for the job.
   2. Cosine Similarity score indicates that approximately 73% of the sections are very similar. Hence duplicated information is present in these descriptions.This is considering anything above 0.25 as overly replicated descriptions.

Tone: 
   1. It is observed that ~84% documents do not use direct pronouns
   2. The sentiment analysis indicates that the overall sentiment of job descriptions is neutral

Format:
   1. 14%, 2 % and 90% of the postings do not have number of experience years, annual salary and Full/Part Time information respectively. This is indicative of incompleteness for a job posting
   2. The word count of job descriptions ranged from 800 – 4000 words which is far away from ideal number of words (~600-700) for better readability. Also, the average proportion of word count for most important sections of requirements and duties was only 18%.  

__Conclusion and recommendation__:

Based on the preliminary analysis, following recommendations can be provided to the city of LA which can be the first steps to improve the job postings:

1. Increase the readability based on the target applicants (Job-type, Education level)
2. Avoid duplication of information
3. Speak directly to candidates
4. Increase the availability of a job posting (in terms of duration)
5. Avoid spelling errors
6. Increase the proportion of highly relevant sections (Requirements, Selection Process)
7. Reduce the length of job description (< than 600-700)
8. Separate sections for important information/requirement (education)

__Future Scope Suggestion:__

Few ways in which the preliminary analysis can be extended:
1. To check using pronouns if there is gender bias in the postings which is discouraging candidates to apply 
2. Look for most frequent words (probable methods: Word 2 Vec and TSNE) used in the postings, specifically     in the requirements/duties section and compare it with ones used by some other companies
3. Modelling to find most dominant/ commmon topic if any using LDA 
4. Building an algorithm to score the job descriptions so that whenever a new posting is posted, it can   first be validated, scored and improved if required.

