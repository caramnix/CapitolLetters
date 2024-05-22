# Capitol Letters: Detecting Differential Attitudes in Legislator Communications Using NLP

Repo contains code/figures created for my master's thesis which looked at legislator comunication through one-minute pseeches from the House floor and on Twitter. 

## Description

This repo contains code necessary for end-to-end workflow for scraping and analyzing one-minute speech data using gpt-3.5-turbo. 

First, I provide code to collect all links to C-SPAN videos which mention a given phrase, in this analysis that phrase is "one-minute" (scrape 117th one minute speeches.ipynb). I also provide the code I used to isolate just the one-minute speeches from the transcript data, since the transcripts contains other House session communication (clean_transcript_data_11*.ipynb). The result fo this cleaning can be found in the folder, One Minute Congresional Speech Data. After cleaning the transcript data the goal is to then  score these speeches for valece, arousal, confidence, empathy and smypathy. This is done using open ai's gpt-3.5-turbo (openapi_getVACES_115.ipynb). Similar scoring is done for 116th and 117th congresses. The resulting scores are availible in the VACES output directory, which has each spceech, the speaker, the party identification of the speaker as well as it's score for each VACES measure. 

The goal of this project was to explore differntial emotion by Members of Congress, so KS-testing is done on the distributions by party to determine if the distrubtions differ (ks-testing VAC_11*.ipynb). Figures of the dsitributions are also created and combined in 'make kde-figure-115-116-117.ipynb.' 


One could use this code to expand the work done here to analyze House Session transcripts on any topic. 


### Dependencies

* Describe any prerequisites, libraries, OS version, etc., needed before installing program.
* ex. Windows 10

### Components of repo

* scraping and cleaning code
     * scrape 117th one minute speeches.ipynb, program which uses selenium to scrape the links to all CSPAN house sessions which mention one-minute as well as scraping the transcripts of those House sessions using  link to the CSPAN video. Similar collection was done for 115th and 116th Congresses. 
     * clean_transcript_data_115.ipynb, code which isolates just one-minute speeches from House session transcripts for 115th Congress
     * clean_transcript_data_116.ipynb, code which isolates just one-minute speeches from House session transcripts for 116th Congress
     * clean_transcript_data_117.ipynb, code which isolates just one-minute speeches from House session transcripts for 117th Congress
* One Minute Congresional Speech Data
      * cleaned_transcript_data_115th.csv, cleaned_transcript_data_116th.csv, cleaned_transcript_data_117th.csv resulting output from cleaning pipeline above. 
* open ai code
     * openapi_getVACES_115.ipynb, code which scores one-minute speeches using 
* VACES output
     * Contains collected one-minute speeches for 115th, 116th and 117th Congresses as well as their Valence, Arousal, Confidence, Empathy and Sympathy which was scored using OpenAI                      gpt-3.5-turbo in openapi_getVACES_115.ipynb
* figure and ks code
    * kde figures and ks testing
         * ks-testing VAC_115.ipynb, ks testing for 115th Congress and figure generation
         * ks-testing VAC_116.ipynb, ks testing for 116th Congress and figure generation
         * ks-testing VAC_117.ipynb, ks testing for 117th Congress and figure generation
         * make kde-figure-115-116-117.ipynb, combine figures into one.
     * sentiment figures
          * cleaning_and_sentiment_scoring_116.ipynb, cleans Tweets and scores sentiment for 116th Congress
          * cleaning_and_sentiment_scoring_117.ipynb, cleans Tweets and scores sentiment for 117th Congress 

## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Contributors names and contact info

ex. Cara Nix, nix.39@osu.edu 

## Version History

* 0.2
    * Various bug fixes and optimizations
    * See [commit change]() or See [release history]()
* 0.1
    * Initial Release


## Acknowledgments

Inspiration, code snippets, etc.
* [awesome-readme](https://github.com/matiassingers/awesome-readme)

