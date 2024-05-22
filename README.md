# Capitol Letters: Detecting Differential Attitudes in Legislator Communications Using NLP

Repo contains code/figures created for my master's thesis which looked at legislator comunication through one-minute pseeches from the House floor and on Twitter. 

## Description

An in-depth paragraph about your project and overview of use.

### Dependencies

* Describe any prerequisites, libraries, OS version, etc., needed before installing program.
* ex. Windows 10

### Components of repo

* scraping and cleaning code
     * scrape 117th one minute speeches.ipynb, program which uses selenium to scrape the links to all CSPAN house sessions which mention one-minute as well as scraping the transcripts of those          House sessions using  link to the CSPAN video. 
     * clean_transcript_data_115.ipynb, code which isolates just one-minute speeches from House session transcripts for 115th Congress
     * clean_transcript_data_116.ipynb, code which isolates just one-minute speeches from House session transcripts for 116th Congress
     * clean_transcript_data_117.ipynb, code which isolates just one-minute speeches from House session transcripts for 117th Congress
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
   

```
code blocks for commands
```

## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Contributors names and contact info

ex. Cara Nix
ex. [@CaraNix](https://twitter.com/caranix)

## Version History

* 0.2
    * Various bug fixes and optimizations
    * See [commit change]() or See [release history]()
* 0.1
    * Initial Release


## Acknowledgments

Inspiration, code snippets, etc.
* [awesome-readme](https://github.com/matiassingers/awesome-readme)

