## Minutes from INIDUN monthly meetings

### Meeting, 29 August, 13:15 on zoom

_NOTES_

- Ben, Roger, and Andreas present
  
1. Courier
   * R and A showed Ben the status (and location) of all the files related to our Curated Courier datasets.
   * B reported that UNESCO has given us permission to publish the original article metadata file (email from Eng Sengsavang, 28 August 2023).
   * R and A explained that the metadata file is already included in the article corpus (in the zip-file, as "document_index.csv").
   * We will post the corpora to Zenodo, but also have them up on GitHub.
   * The relevant material on GitHub is in three places:
     - Curated_Courier is the repository with the "products", including the final corpora and supplementary materials.
     - Tagged_Courier is the repository in which the work took place; this may also be of interest for those eager to really see how we did things.
     - Finally, [Courier-lab](https://github.com/inidun/courier-lab/tree/main/content/notebooks) is the repository where we have created code and materials for an online interface with the Courier corpora, in the form of a "Jupyter Lite" webpage.
   
   * B will have a meeting (today, 16:00) with UNESCO archivist Eng S. and with Ian Denison, "Chief, UNESCO Publishing and Branding". 

1. Coming tasks
   * Barring any surprises, B will proceed with the uploads to Zenodo.
   * B will complete intro texts for the Zenodo uploads, adding a reference to UNESCO's open access publishing license, with link.
   * B will add a short version of the same presentation text to the Read Me files of the following three GitHub repositories:
     i. Curated_Courier 
     i. Tagged_Courier
     i. Courier-lab
   * B will add a short introductory text to the beginning of the JupyterLite page.
     - Do this by making edits and saving them in the online form. Then, download the notebook, then send it to R and A (alternately I could push it up to the server, but maybe easier and safer to do it this way!).
   * This short text that will appear in all the above mentioned places should include:
     - A line about Courier as source
     - A reference to Courier's open access CC publishing license (with link)
     - A reference to VR project support  

Next meeting: 12 September, 13:15 (zoom).

### MEETING SCHEDULE for FALL 2023

Tuesdays, 13:15-15:00 (at the latest), on zoom.

29/8
12/9
26/9 
10/10 
7/11 
21/11
5/12 


### Meeting, 20 June, 13:15 on zoom

_NOTES_

1. Courier updates
   * Roger has created several new topic models based on the Courier article corpus. These are available in the drop-down menu in the INIDUN jupyter topic modeling page.

1. The Curated Courier: corpora and article     
   * We discussed the article text, but mostly focused on the issue of what exactly we will make available, and how. Here are my notes on what we concluded:
   * We will produce three (sets of) items:
     1. Corpora made available to the public through zenodo.
     2. A repository on GitHub
     3. An article, to submit to Journal of Open Humanities Data  

__Item set 1:__ corpora to publish on Zenodo
  * Primary output: a digital text corpus called “Curated Courier 1.0”
    - This consists of the texts of all (indexed) articles published in The UNESCO Courier 1948-2020, (extracted from the complete text and compiled).
  * Secondary output: Complete curated issue corpus.
    - This consists of the complete text found in all Courier issues 1948-2020, extracted from the PDFs and rendered as simple text, by issue.
    - Goal: a researcher should be able to download this and open it in, for example, Voyant.
    - OBS: Roger and Andreas will recreate this from the original files that Oriane annotated.
  * In the intro texts on zenodo, we will link to the complete repository on GitHub, where all process-related files will live.

__Item set 2:__ things to include in our GitHub repository
  * (QUESTION) Will the two corpora mentioned above live here, as well? I guess they have to, in order to be functional within our jupyter pages, right? 
  * Additional items (not published on Zenodo):
    - Complete curated and annotated issue corpus (all pages, complete text, but annotated with labels showing when indexed articles begin, etc.): by issue. 
    - OBS: We must remove links to the Courier page PDFs that are currently hosted on our server.
    - Goal: this serves mostly as evidence of the process; published for transparency/traceability.
    - Additional files:
      - The Courier metadata file (which the compiling algorithm uses as its “document index”)
	- OBS: Must confirm with UNESCO archive that this is OK to publish.
      - Quality control file (re: OCR)
      - Quality control file (re: accuracy of segmentation/compiling) 
      - Curation process instructions 
      - “Read me” file(s)
        
__Item 3:__ our article, to submit to Journal of Open Humanities Data


1. ORDER of EVENTS:
   * Roger and Andreas prepare final versions of:
     - The Curated Courier 1.0 (article corpus)
     - The complete curated issue corpus (“A” above)

   * Andreas creates zipfiles in GitHub, sends links to Ben
   * Ben writes drafts of introductory texts (for zenodo pages), shares with all for comments.
   * Ben uploads these to zenodo.
   * In the meantime: Roger and Andreas “clean up” in the relevant GitHub pages.
   * Finalize our article text (including references to zenodo pages and GitHub repository)
     - Fredrik and Roger will discuss parts of article text on Thursday, 29/6
     - Fredrik and Ben will discuss article text on Monday, 26/6
    * Submit to journal


### Meeting, 24 May, 13:15 on zoom 

1. Courier: Corpus curation
   * Oriane has completed the [Courier segmentation QC.](https://docs.google.com/spreadsheets/d/1Z40M5FqTLceO8tttw6L87P6fEMvUmQSfeJ4xczDDUto/edit#gid=0)
   * Results: 
     - The articles texts are complete with an error rate of 8%
     - Only 5.8% of the sample of articles contain extraneous text (usually just a page number)
     - About 15% of the sampled articles contain some text that is out of order. This is generally at the level of paragraph (i.e., whole paragraphs are in the wrong order, but are correct internally). 15 out of 20 cases are from the year 2000 or later. (This means that if we are using the 1947 to 2002 corpus there are only two such articles.)     
   * Now that the Courier curating and QC is done: 
     - R and A will create topic models based on the article-corpus : 50, 100, and 200. Non-lemmatize. Exclude numerals, words that appear less than 5 times in the whole corpus, and delimiters (punctuation, etc)
     - Use the article-corpus which is [already up](https://github.com/inidun/courier_article_corpus)
     - See the article-corpus in the ["release" form](https://github.com/inidun/courier_article_corpus/releases/tag/0.2)

1. Writing: Courier Corpus data article (for _Journal of Open Humanities Data_)
   * We have [a working document in the INIDUN google drive](https://docs.google.com/document/d/1Qcx4s8rsMGWkBJ8SnbK0fwf2qG65V1fKt3dTNjThBjY/edit). 
   * Andreas and Roger will look at this, add their sections.
   * All of us should be prepared to discuss the article text in detail at our next meeting on 20/6.
   * Before then, look into the step-by-step plan:
     - When do we upload the datat sets? (Before submitting the article ms? Check journal guidelines.)
     - To which repository? Zenodo, Swedish one?
     - Which datasets, exactly?
       - the Courier article-corpus
       - the whole (bag of words) Courier corpus? Yes (it's already on GitHub).
       - the Courier articles metadata file (assuming UNESCO archive gives permission)
       - Code/scripts used to create Jupyter pages with tools to explore the data
       - The two QC spreadsheets (Courier OCR QC, and Courier segmentation QC). Copy these into GitHub. 
     - Confirm the precise CC license that UNESCO publishes Courier under, so that we can cite it correctly.  
     - Confirm with UNESCO archive that we can publish the Courier metadata file. 

1. Other Writing:
   * For the article on "Information" and "Communication" in Courier, maybe publish the topic models; at least refer to the GitHub page where the corpus is, from which we made the topic models.
       
1. _Proceedings_: Corpus curation
   * Now that Oriane is done with [the meeting index](https://docs.google.com/spreadsheets/d/1ERPQtWja0qSTLzfUiFvNE31Bv5XHA64oTngIKIajEIY/edit#gid=0), we can use the page numbers to extract text from the current corpus with the "meeting" as the smallest unit. 
   * OBS: make sure to get only the actual verbatim meetings, not the others. The three relevant titles (in column H) are: 
     - Verbatim records of plenary meetings
     - PLENARY MEETINGS
     - Proceedings
     - PLENARY MEETINGS OF THE GENERAL CONFERENCE
   * Andreas has created a rough corpus from the relevant pages of the "Verbatim proceedings". Needs now to extract the English and French text (and remove the other languages). At this stage we will keep both English and French text on the same pages, in the same files.
   * For the rest of this term, the work with Proceedings is second priority compared to the work with Courier! In the autumn Ben, Roger and Andreas will make some decisions about how best to finalize a Proceedings corpus, what to make public, whether or not to seek additional funding, etc.  

### Meeting, 26 April, 13:15 on zoom 

_Notes_

1. Proceedings: Corpus curation

   * MEETING INDEX
     - Oriane has completed work on [a meeting index](https://docs.google.com/spreadsheets/d/1ERPQtWja0qSTLzfUiFvNE31Bv5XHA64oTngIKIajEIY/edit#gid=0). This list all the "meetings" of each "session" (that is, the year), and include the meeting president's name. 
     - The names of the meeting presidents do not always appear in the same way in the Proceedings; some are missing first names, etc. Oriane has entered them as they appear in the source, and that's how we'll leave it for now. In the future it might be helpful to standardize these, but not just now.

    * Creating a rough corpus now
      - R and A are working on creating a rough corpus, extracting the English and French text from the relevant pages of the "Verbatim proceedings". 
      - Also, now that Oriane is done with the meeting index, we can use the page numbers to extract text from the current corpus with the "meeting" as the smallest unit. This is important for use in topic modeling, for example.
      - Question: so these are two corpora? One based on session (whole year) and one based on meetings? Or just one, with meeting as a smallest unit?
     
    * Automated segmentation
      - R and A are working on automated forms of segmentation of speeches; also with help from Rebecca (Humlab).
      - The plan is to use Prodigy (a program in the same suite as SpaCy) to conduct a machine learning approach to tag up the Proceedings, marking the line when new speeches begin, identifying the speaker name, speaker nationality, and so on.
      - Next step will be for R and A to prepare a text sample (drawn from multiple different years of Proceedings?), that Oriane (and all of us) can tag manually. This will then serve as a training corpus.  
          
1. Courier: Corpus curation

   * Courier segmentation QC
     - Oriane showed us her work on creating a spreadsheet in which to enter data for a quality control of the Courier article segmentation and compiling processes. 
     - We discussed how this should work. After the columns listing the name, year, and number of the randomly selected articles (two per year), the following columns should be as follows (or something similar):
       - Complete? (That is, does the entire article text appear?) yes/no
       - Excess/incorrect text? (That is, does any additional text appear, that is not from the article?) yes/no
       - Text out of order? yes/no
       - Comments (a space for textual comments on anything else of note)

1. Writing: Courier Corpus article
   
   * B and F presented the idea of writing an article together in which we present our Curated Courier corpus.
   * Intended journal is [Journal of Open Humanities Data](https://openhumanitiesdata.metajnl.com) (JOHD). 
   * We have started [a working document in the INIDUN google drive](https://docs.google.com/document/d/1Qcx4s8rsMGWkBJ8SnbK0fwf2qG65V1fKt3dTNjThBjY/edit). 
   * Goal and timeframe: we aim to have a draft of the complete article by end of June/early July (before summer vacation). Then in late August or September we will upload the Courier files to a digital repository and submit the article to the journal. 
   * TASKS for writing the draft
     - Andreas: write short text explaining our OCR process; and a short text explaining the compiler algorithm that allowed us to create the article corpus. 
     - Oriane: write short texts re:
       a. the tagging work you did (for article segmentation)
       b. the OCR quality control 
       c. the segmentation and compilation quality control (that you're doing now)
     - Fredrik: continue work on section 2, re: Courier as curated corpus (general features of the content, and creating sections in which Andreas and Oriane can enter their texts)
     - Ben: continue work on section 1, re: Courier as source for humanities research (not just history!)   
     - Ben and Fredrik: editing and coordinating all the parts 
     - Ben: contact UNESCO archive to inform them of our plan, ask for permission to publish the Courier article metadata, and see if they have an opinion about where (which repository) the corpus and metadata should be uploaded to. 



### Meeting, 28 March, 13:15 on zoom 

_Notes_

1. Courier: Corpus curation
   * Status: 
     - A corpus consisting (only) of articles from Courier is now ready. R and A have created a DTM of this that can be used in the Word Trends tool in jupyter. OBS: to use this, change the setting in the first cell so that corpus_config="courier_article",
     - There is one article in the corpus that is left over from UNESCO's pre-Courier publication. Andreas will remove this.
     	- [x] __Done__
     - Question: Do we have to create a new DTM to reflect that change?
     	- [x] __A new DTM has been created. Change setting to `corpus_config="courier_article_v0_2"` to use it.__
     - To work with this corpus outside of jupyter, we can download it from the Github repository called "Courier_Article_Corpus".     
   
   * Create a topic model (or two) on article level:
     - R and A will create a topic model (of this corpus, divided up into articles). 
     - Questions (for B and F): should this be 100 topics, 200, or maybe do both? Should the TM be lemmatized or not?
   
   * Courier segmentation: Quality control
     - After Oriane's successful work running a quality control on the OCR quality of our Courier corpus, we agreed that she should now create and run a similar QC process that measures how well the article segmentation has funtioned.
     - O. will select (at random) two articles per year, and for each will simply check if they start and end where they are supposed to. 
     - O. will begin by creating a form in which to enter this data (similar to the one used for OCR quality control) and share it with the rest of us. 

1. Courier: writing
   * B and F submitted an article (to DHNB conference volume)
   * Next steps re: general Courier corpus article:
     - F will ask Johan Jarlbrink about good places to publish an article like this
     - B will create a Google drive document for the draft text of this article 
     - The article will have three main parts:
       1. Courier as historical source (B will write first draft)
       2. Courier as curated corpus, including technical matters (F will write first draft)
       3. Investigating the Courier corpus: examples of methods we have used, or could use (B and F will get this started) 
   * Time frame: aim to complete at least a first draft of this article before June 1 

1. Proceedings: corpus curation
   * Improving OCR quality?
     - Update from Fredrik's contacts at Riksdagsbiblioteket (Addition after meeting). RB cannot help us; they would have to cut up their copies to do the scanning, and they only have one copy of each year. B will check once more if some library has the books and could do a scan. Otherwise we will just proceed with the corpus as we have it.  
     
   * Curating Goals: 
     - The most ambitious goal is a corpus consisting of speeches, each given by an particular speaker on a particular day. This would be linked to an index in which each speech is linked to a date, speaker, plenary meeting, "session" (one every two years, each one of which has a UNESCO-assigned "record number"), and so on. Later, we could add information to the speakers, like nationality, gender, and so on.    
     - An intermediate goal is to create a corpus divided up by "plenary meetings" (of which there are many during each biannual "session" of UNESCO's General Conference). Each plenary meeting has a president, who is listed by that title only in the text. So it is important to identify that meeting president in order to be able to assign a speaker to each speech. 

   * MEETING INDEX
     - To achieve that intermediate goal, we need an index listing all the "meetings", with date, the "session" (year) they belong to, and the meeting president's name. 
     - Oriane has begun work on [this index](https://docs.google.com/spreadsheets/d/1ERPQtWja0qSTLzfUiFvNE31Bv5XHA64oTngIKIajEIY/edit#gid=0).  

   * Automated segmentation
     - In parallel, R and A will continue work on automated forms of segmentation of speeches. 
     - Once Oriane is done with the meeting index, we can use the page numbers to extraxt text from the current corpus with the "meeting" as the smallest unit. This is important for use in topic modeling, for example.     
     
   * Creating a rough corpus now
     - In the meantime, R and A will work on creating a rough corpus, extracting the English and French text from the relevant pages of the "Verbatim proceedings". These are identified by the page numbers that are listed in [Proceedings_metadata_edited](https://docs.google.com/spreadsheets/d/1z_QzDF2cYwaxP5ZdJ9t5h612g3nNRDZI/edit#gid=1893730714), in column K. The number in parentheses are the PDF page numbers.
      - We can then create topic model of this corpus. One of 100 topics, one of 200 topics, to begin with (OK?).
      - QUESTION: should these topic models be lemmatized? In general, that's probably best. It is often interesting for me to see both "culture" and "cultures" (plural), but maybe that's not so important in a topic model...?
         


_Agenda_

1. Courier: Corpus curation
   * Status?
   * Plans for B and F to work with this?
   * Create a topic model (or two) on article level?
   
1. Courier: writing
   * B and F submitted article (to DHNB conference volume)
   * Next steps re: general Courier corpus article?

1. Proceedings: corpus curation
   * Status?
   * Update from Fredrik's contacts at Riksdagsbiblioteket?
   * Tasks for Oriane?
  
1. Prioritization for remainder of 2023
   * Collect possible priorities, sort them and decide!
   * Possible categories: 
     * corpus preparation and publication (where?)
     * article publication
     * writing final report for funder
     * Ideas for follow-up projects, applications, etc? 

### Meeting, 28 February, 13:15 on zoom 

_Notes_

1. Courier: Corpus curation
   * Oriane has finished putting in corrections to problems that Andreas found.
   * Andreas found 100+ additional errors in testing the compiler algorithm, especially discrepancies between the article page numbers in the metadata index and in the markdown files. Oriane will now work on fixing those.
   * Oriane has begun work on Courier OCR quality control; anticipates being done with that in 2 weeks or so. She will let us all know when that is done.
   * At that point, R and A will prepare the Curated Courier 1.0. Roger will prepare a DTM of this so that it we can open it in jupyter, for word trends, etc. Also, R will create a 200-topic topic model that we can explore with the existing TM page.
      
1. Courier: writing
   * Fredrik and Ben present their idea to write an article presenting Courier as historical source and machine-readable corpus. We may, in conjunction with this, want to ask Roger for other ways to interface with the corpus, based on the metadata index. One idea would be to add gender to the Courier article authors, so that one could divide up the corpus to two subcorpora, one by female authors and the other by male authors. We could have all 5 of us as co-authors on this. F and B will turn their attention to this after March 15; at that point we can also consider the best places to publish such an article.

1. Proceedings: corpus curation
   * B reported on difficulties in getting new scans of selected Proceedings volumes (because they are not, in fact, at KB, but are at Riksdagsbiblioteket). Ben will write up which issues and pages we need and email this to Fredrik, who will ask his contacts at Riksdagsbiblioteket if they could help us scan two issues.

1. Business updates
   * B reported that we were granted an extension of the project period (dispositionstid), so we now have until Dec 31, 2024 to use all project-related funds. Also, it seems that there is enough money in the amount already agreed upon between Uppsala and Humlab to allow Roger and Andreas to work on the project at 15% (rather than only 10%) for the rest of 2023, and perhaps into 2024. B will check in again about money matters by May or June.

1. Priorities for the rest of the project time
   * This will be the subject of our next meeting, 28 March, 13:15 (via zoom).

### Meeting, 31 January, 15:15 on zoom (plus 1 February work session at Humlab)

_Notes_

1. Courier: Corpus curation
   * We discussed issue of adding in text from those few pages where the OCR quality is still very poor. Oriane could for example transcribe these directly into the text files. But that would mean that just a tiny part of the corpus would be hand-curated in a manner that is inconsistent. So, we will let these few pages go, at least for now, for the sake of being consistent in our application of OCR.
   * Courier Quality Control: 
     * Roger suggests that we conduct a quality control (QC) of Courier, in a manner similar to what we did with Proceedings ([see Proceedings QC file here](https://docs.google.com/spreadsheets/d/1fCYz5jZDkf_y36fv8bjaXdrTyR5WT9wlaFnV2i2pBQ4/edit?usp=share_link)). That is, a test that leads to an error percentage number as a measure of OCR quality. It is also a good idea to have a human review of Courier article corpus, to confirm that the article compilation procedures work correctly.   
     * Oriane will conduct this Courier QC 
     * The QC will be conducted by article (rather than by page)
     * There are circa 7600 Courier articles: so 2% of the total is ca. 150 articles.
     * The process thus includes the following steps:
       1. Roger and Andreas compile Curated Courier 1.0 (and tell Oriane when it's ready!)
       1. Oriane develops a way to select 150 articles, distributed over the time period. 
          * Question: go to 2011 only, or all the way through 2019? 
       3. In each article, select a section of 100-200 words, and count the number of errors
          * This is best done in Visual Studio Code, using a simple spellchecker to identify errors.
          * Question: is one text selection per article enough?  
       4. Create a spreadsheet tabulating 
          a. the sample article's info (title, year, issue number, and maybe link to the relevant PDF?) 
	  a. the number of words in the text selection 
	  a. the number of errors in the text selection
	  a. the error percentage for that text selection  

1. Proceedings: Corpus curation
   * Proceedings quality control is complete. Ben will now order re-scanning of those issues with an error rate of 5% or higher. 

1. Courier: research tools
   * We looked again at co-occurrence calculations Roger prepared.
   * Ben sent Roger email (1/2) with questions and requests.

1. Courier: writing
   * Ben and Fredrik started worked on article "Nature and Culture in Courier" for DHNB2023 conference.
   * Ben has created a working text document in INIDUN drive. See [that file](https://docs.google.com/document/d/1KVRb59gAO9CV2xVQq4yQS_lGaYEs_5j4WrzuCHyIzBg/edit) for more on the paper and the division of research and writing tasks.  
   

### Meeting, 31 January - 1 February 2023 (Umeå), including 31/1, 15:15 on zoom.

_Agenda_

1. Courier: Corpus curation
   * Oriane's status?
   * Ready to compile Curated Courier 1.0? 	

1. Proceedings: Corpus curation
   * Status of quality control
   * Oriane's roll?

1. Courier: research tools
   * Look again at co-occurrence calculations Roger prepared
   * Using these for "Nature and Culture" paper ...? 

### Meeting, 17 January 2023 (on zoom)

_Notes_

1. We confirmed the following VT23 meeting schedule:
     - 31/1-1/2 	INIDUN days in Umeå (B comes up Tuesday and all day Wednesday) 
       - 31/1, 15:15    everyone, via zoom 
       - 1/2, 9:00	Meeting: Ben, Fredrik, Roger and Andreas 
     - 15/2, 13:15  	just B and F
     - 28/2, 13:15  	everyone, via zoom
     - 28/3, 13:15  	everyone, via zoom
     - 25/4, 13:15  	everyone, via zoom
     - 23/5, 13:15  	everyone, via zoom
     - 13/6, 13:15  	everyone, via zoom

1. Courier: Corpus curation
   * Oriane updated us on her (impressive!) progress
     - She completed tagging on the Courier articles from the 1940s and 50s
     - Has compiled a list of metadata on articles that did not appear in the index we got from UNESCO (unindexed_articles)
     - Has compiled a list of errrors/missing pages/poor OCR in the Courier pages. 
      
   * With regard to the "Next steps" (see _Notes_ from 13 December meeting, below), the status is as follows:
     1. Oriane will now prepare a detailed overview document (on GitHub), listing (at least) the issues that include pages that need to be OCRed and added to the total collection of Courier pages. DONE
     1. Andreas will OCR and integrate these pages (and tell Oriane when done). DONE 
     1. Oriane will then apply tags to those newly added pages (and tell us all when done). TO DO
     1. Also, regarding missing/faulty pages, Oriane will locate correct text in newly OCR'd files and insert that into the relevant Tagged Courier file. Will tell us when this is complete. TO DO
        * At that point, Roger can run the compiler algorithm and release the Tagged Courier Corpus 1.0 (!).   
     1. Andreas will create a version of the Courier Index (on GitHub) to which we add our additions and corrections. TO DO
        * This will be a new index, based on the file "article_index.csv", to which we will add the new data on the unindexed articles.
     1. Oriane will correct the incorrect page numbers in the index (by comparing with annotations in Tagged Courier progress file). TO DO  
     1. Ben and Fredrik will decide whether or not it is worthwhile to manually add to the index entries (author, title, year, page numbers) for the 86 or more unindexed articles that Oriane identified. DONE, answer is "Yes!"

1. Proceedings: 
   * Status of OCR Quality control:
     * Ben needs to finish his part of Proceedings OCR quality control.
     * Regarding which volumes should be re-scanned, re-OCR'd
       * Step one: for all Proceedings volumes for which the error rate is over 5%, Ben will order a new scan (with OCR, if possible) at KB.
       * Step two: depending on cost and time constraints, Ben will order a new scan also for all Proceedings volumes for which the error rate is over 1%.  
   * Proceedings "next steps":
     - Roger and Andreas will see whether the basis for a more detailed metadata database on Proceedings can be derived automatically from machine reading of the corpus. IN PROGRESS
     - Then (or otherwise), we will create such a database, to which we can add details (speaker names, nationalities, genders, etc) later, as time permits.   
     - LATER: Andreas (or Oriane) will see if the Lists of Participants in each Proceedings volumes can be used to create a "personindex". 

1. Courier: Research tools
   * Look together at the new Courier co-occurrence models that Roger prepared just before Christmas
     * There seems to have been some confusion about what exactly the goal was here. Ben and Fredrik will explore these models and let Roger and Andreas know if they want some other ones in addition.    


_Agenda_

1. Confirm VT23 meeting schedule
   * (see suggested schedule in _Notes_ from 13 December meeting, below)

1. Courier: Corpus curation
   * Oriane updates on situation, her progress
   * Where are we with regard to the "Next steps" (see _Notes_ from 13 December meeting, below)...?
   * What should Oriane do next? 
   * Decide on revised "Next steps" and relevant division of labor 

1. Proceedings: 
   * Status of OCR Quality control:
     * Which volumes should be re-scanned, re-OCR:ed?
   * Review Proceedings "next steps":
     - Roger and Andreas will see whether the basis for a more detailed metadata database on Proceedings can be derived automatically from machine reading of the corpus.
     - Then (or otherwise), we will create such a database, to which we can add details (speaker names, nationalities, genders, etc) later, as time permits.   
     - Andreas will see if the Lists of Participants in each Proceedings volumes can be used to create a "personindex". 

1. Courier: Research tools
   * Look together at the new Courier co-occurrence models that Roger prepared just before Christmas
   * Discuss VT23 research plan  


### Meeting, 13 December 2022 (on zoom)

_Notes_

1. Courier:
   * Oriane has completed review of Courier pages through end of print run; has now begun looking at late 1940s issues. Will report in January on how long it is taking so we can decide whether it is worth the trouble.   
   * Oriane showed an overview of the problems or discrepancies that appeared most often in Courier. For example:
     * Circa 86 issues include at least one unindexed article (that is, a text with an author and title which, for whatever reason, is not listed in the index we received from the UNESCO archive).
     * Circa 65 issues include at least one article where the page numbers listed in the index are incorrect (article in fact begins earlier, or ends later, in the issue).
     * Circa 15 issues contain one or more pages in the PDF originals that were not OCRed. 
     * In the case of circa 4 issues the page numbers are systematically incorrect (adding 2 to the correct page number, for example)  

   * Next steps:
     1. Oriane will now prepare a detailed overview document (on GitHub), listing (at least) the issues that include pages that need to be OCRed and added to the total collection of Courier pages.
     1. Andreas will OCR and integrate these pages (and tell Oriane when done)
     1. Oriane will then apply tags to those newly added pages (and tell us all when done)
     1. Andreas will create a version of the Courier Index (on GitHub) to which we add our additions and corrections.
     1. Andreas and Roger will work on correcting the incorrect page numbers in the index.
     1. Ben and Fredrik will decide whether or not it is worthwhile to manually add to the index entries (author, title, year, page numbers) for the 86 or more unindexed articles that Oriane identified. 
   
   * How to work with the Courier corpus: Fredrik suggests that we think of it as two corpora:
     * Courier (A) is the entire text of all issues.
     * Courier (B) is the corpus composed of the texts of all articles listed in the index. 
       * Courier (B1) includes the texts of all articles listed in the index, as well as all articles tagged as "unindexed articles". 
       * (Later, perhaps, we can incorporate metadata on these articles into the index, making the "unindexed article" category disappear.) 

1. Project planning and budget for 2023
   * According to Ben's calculations, we can keep Humlab on the project at 10% for all of 2023. Ben will send detailed information on this to Roger and to Humlab's ekonom (and director). 

1. Meeting dates for 2023
   * Ben suggests the following meeting dates for (the first part of) Spring term 2023:
     - 13/1, 13:15      just B and F
     - 17/1, 13:15  	everyone, [via zoom](https://uu-se.zoom.us/j/6261245082)
     - 31/1-1/2 	INIDUN days in Umeå (B comes up for all day Tuesday and half of Wednesday) 
       - 31/1, 13:15    everyone, via zoom 
     - 15/2, 13:15  	just B and F
     - 28/2, 13:15  	everyone, via zoom
     - 28/3, 13:15  	everyone, via zoom
     - 25/4, 13:15  	everyone, via zoom
     - 23/5, 13:15  	everyone, via zoom
     - 13/6, 13:15  	everyone, via zoom
   

_Agenda_

1. Courier:
   * status updates
   * Oriane takes us through her comments and notes
   * next steps?

1. Proceedings:
   * status updates

1. Project planning and budget for 2023
   * Ben presents tentative 2023 plan
   * Meeting dates for 2023 

### Meeting, 30 November 2022 (on zoom)

_Notes_

1. Courier:
   * Oriane is almost done with her work on Courier.
   * We decided that she should then begin doing the same kind of tagging work on the issues 1948-1952, which we had thusfar skipped.
   * We will discuss her annotations (as written in the Progress file) on December 13.
   * A next step is for F and B to run some quality-control tests of the Courier corpus, in January. 

1. Project planning and budget for 2023
   * Discussed general 2023 outline; B will collect information, report back on Dec 13.


_Agenda_

1. Courier:
   * status updates
   * Next steps?
   * Go through ways to work with this in jupyter

1. Proceedings:
   * status updates
   * Next steps
   * Tasks for Oriane?
   * Go through ways to work with this in jupyter

1. Project planning and budget for 2023
   * Fredrik's move to Malmö Univ., plans till 1 March 2023 
   * Overall budget situation
   * Humlab involvement in 2023: how much, 


### Meeting, 1 November 2022 (at Humlab)

_Notes_

1. Courier: 
   * Status of "compiler" algorithm is ready, has been tested; must be run and tested again once Oriane is done with tagging all Courier pages.
   * Courier curating
     - Oriane emailed questions regarding how to mark the "Greenwatch" supplemental sections of Courier in the 1990s, as well as how to deal with editorials that are catalogued as articles. The answer was that she should just mark small articles in the Greenwatch section (and other similar supplements or sub-sections) with “ignore”, as she had been doing in earlier cases. The logic is that the tagging she is doing primarily serves just to link the metadata file (about articles) to the text of those articles. So, the fact that these small text blocks are in the Greenwatch section is not actually a relevant question for that process. Similarly, any editorials that UNESCO decided to enter into their index as articles we need to tag in the text as articles, so that the compiling algorithm can find them and include them in relevant compiled corpora.
   * Courier Metadata improvement
     * we decided which is the master file for Courier metadata: it is on GitHub, INIDUN_data, Courier. (We are keeping an unedited copy of the version UNESCO sent us under "original") 
     * Edits and additions to this file can be made by opening it, from GitHub, in VSC, and using the plug-in called Edit CSV. (That way we avoid problems associated with opening and editing it in Excel.)  
     * We will likely want to add new columns to the metadata (e.g., author gender, nationality, UNESCO official or not, etc). Will discuss this together once Oriane is done.
   * Next steps: 
     * Once Oriane is done with Courier tagging: hold meeting where we go through all her (and Marita's) annotations.
     * R and A will run the compiler and create a corpus of just article texts. 
       - OBS: It might be a good idea to save compiled corpora in Zenodo, which allows for easy versioning of large files like this. (Ben and Andreas looked at the options for this on [zenodo's homepage.](https://about.zenodo.org/)
     * Ben, Fredrik and maybe Oriane will devise and impliment some simple quality control tests on this corpus. 

1. Proceedings:
   * Roger and company showed their progress on a systematic identification of the textual patterns in Proceedings that mark when a new speaker begins speaking. We can apply this and test it, once F and B are done with OCR quality control check.  
   * Next steps: 
     - Roger and Andreas will see whether the basis for a more detailed metadata database on Proceedings can be derived automatically from machine reading of the corpus.
     - Then (or otherwise), we will create such a database, to which we can add details (speaker names, nationalities, genders, etc) later, as time permits.   
     - Andreas will see if the Lists of Participants in each Proceedings volumes can be used to create a "personindex". 
     - Ben and Fredrik will complete results of OCR quality control work on Proceedings. 

1. Wrapping up, moving forward
   * timeframe for rest of project
     - Ben will apply for förlangd dispositionstid in January. Otherwise, project concludes at end of 2023.
   * Ben, Fredrik, Roger and Johan Jarlbrink discussed what a good project conclusion would look like:
     - The minimum is that we publish all our corpora and relevant metadata indexes on GitHub (and/or zenodo), and publish examples of how we worked with the data, based on articles we publish, as code on GitHub and/or as "frozen" Jupyter notebooks.  
   * Relationship of this to UNESCO:
     - We confirmed that all UNESCO texts are under a special creative commmons license for Intergovernmental organizations (IGOs), according to which we can re-use and change and publish as long as we cite the source. So, we do not need to ask for permission to publish our corpora. But we will tell UNESCO that we doing this so that they can link to it, or perhaps so that we can discuss more ambitious options with them.       


### Meeting, 1 November 2022 (at Humlab)

_Agenda_

1. Review agenda; agree on plan for these sessions

1. Courier: 
   * curating issues
   * status of "compiler" algorithm?
   * Courier Metadata improvement
     * decide which is the master file for Courier metadata
     * create a workflow for updating, cleaning, correcting, and adding to this file
     * decide if we want to add new columns to the metadata (e.g., author gender, nationality, UNESCO official or not, etc).
   * Status of Courier articles
     - Re: Courier TM for nature/culture issues (see [Ben's abstract](https://docs.google.com/document/d/1u2LwWv06BASS9Z4Jd4tNVSSqvCfkn8F8l07HBxg_UL4/edit), submitted to DHNB23)
     - Re: Courier TM for "information" and "communication" (see [Fredrik's draft](https://docs.google.com/document/d/1F8JHupOE6DAbYkhk3bjyL7XX2YE7rkJt/edit))

1. Proceedings:
   * Roger and company have been working on a systematic identification of the textual patterns in Proceedings that mark when a new speaker begins speaking, or when a section of text is a translation of the text immediately above, and so on. Status?
   * Ben and Fredrik present (preliminary) results of OCR quality control work on Proceedings. 
   * Ben and Fredrik present other questions and/or desiderata re: Proceedings
   * Establish next steps
   
1. SSI:
   * status of article
   * Issues/problems
     - Ben shows his manually made concordance worksheet; how to make this into a claim?

1. Future plans
   * Our own conference or workshop?
   * Ben and Fredrik will discuss ideas on this with Jani Marjanen in Uppsala, March 2023.

1. Cooperation with Westac
   * Opportunities?

1. Wrapping up, moving forward
   * timeframe for rest of project
     - Ben will apply for förlangd dispositionstid in January. Otherwise, project concludes at end of 2023.
   * discuss what a good project conclusion would look like
   * Where/how to publish curated corpora?
   * Relationship of this to UNESCO?

***Special side session, Tuesday afternoon***
1. Closing up Culture of International Society (Ben, Roger and Andreas)
   * Where/how to publish curated corpora?
     - Zenodo and/or GitHub?
   * Where/how to archive (and make available) jupyter pages, other project-related data?
   * How to keep jupyter pages alive for future use?


### Meeting, 28 September 2022 (via zoom)

_Notes_

1. Courier: curating issues
   * Oriane notes that mid-1970s Courier sometimes includes a supplemental bulletin called "News from UNESCO"; how to tag this? We decided that these should be tagged with a new category, "unindexed supplement". Short, untitled mini-statements from the editors (for example, presenting the topic of a special issue) should be tagged as "editorials".
   
1. Courier: next steps 
   * R and A will create and run a "compiler" algorithm that will pull together the pieces of an article text (spread across multiple pages) into one article text, that corresponds to a title and number from the metadata index. 
   * R and A will create jupyter pages (modeled on ones from Westac) as our interface with these Courier articles, with links to (a) the PDFs and (b) the relevant txt files.
   * Once Oriane is done with Courier tagging, we will conduct a quality control process by running tests on the articles (are they complete, do they match the index, etc?) via the jupyter page(s). 

1. Courier: Metadata improvement
   * At next meeting (1 Nov), we will:
     * decide which is the master file for Courier metadata
     * create a workflow for updating, cleaning, correcting, and adding to this file
     * decide if we want to add new columns to the metadata (e.g., author gender, nationality, UNESCO official or not, etc).

1. Proceedings: identifying patterns
   * Roger, with help from Marita and Andreas, will conduct a systematic identification of the textual patterns in Proceedings that mark when a new speaker begins speaking, or when a section of text is a translation of the text immediately above, and so on. 
   * They will present the results of this at our next meeting (1 Nov, or maybe even 19 Oct?) 
   * Ben and Fredrik will also review Proceedings by then, and prepare relevant questions and desiderata.
   
3. Proceedings: OCR quality control
   * Ben and Fredrik will conduct systematic review of the quality of OCR in all our Proceedings documents. Results of this are recorded in [this spreadsheet](https://docs.google.com/spreadsheets/d/1fCYz5jZDkf_y36fv8bjaXdrTyR5WT9wlaFnV2i2pBQ4/edit?usp=sharing)
   * Where possible, they will use the files listed in this ~~[Index of Proceedings PDFs](https://demo.humlab.umu.se/inidun/proceedings/reocr/) (each of these has OCR text embedded in the PDF)~~ . :exclamation: __Note__: Updated link with all PDFs: [Proceedings PDFs](https://demo.humlab.umu.se/inidun/proceedings/pdfs/)
   * Where there is no file in that index, they will use the [2019 Scrape files](https://drive.google.com/drive/folders/1YoeRe21aCgFmThDwkJJ9Ni38iJGIpbRp) (now on google drive). To know what file number corresponds to which year, consult ["Proceedings Metadata Edited"](https://docs.google.com/spreadsheets/d/1z_QzDF2cYwaxP5ZdJ9t5h612g3nNRDZI/edit#gid=1893730714)
   * Ben and Fredrik will present results at next meeting (1 Nov)
   


### Meeting, 30 August 2022 (via zoom)

_Notes_

1. Updates
   * Ben: Hiring a student assistent (again) is on track. Much work recently on reading about UNESCO's history; aim to soon complete new draft of SSI article. 
   * Fredrik: at work on new article on concept of information in Courier, focusing on topic modeling. 
   * New work levels (percentages): hur ser det ut? 

1. Status of Courier work
   * Once assistant is hired we can move quickly to get a complete corpus that links up to the database of article titles.
   * Fredrik asks Roger and Andreas to figure out how to see how a particular word changes its relative position over time _within_ a given topic. Westac group is working on something similar, so the same tool could serve both projects.
   *   

1. Status of Proceedings work
   * Basic preparation of text corpus (OCR work, etc) is moving forward. Coming tasks:
     * Draft instructions for research assistant who will do tagging and quality control of Proceedings
     * Have usable corpus for at least preliminary reserach by the end of 2022. 

1. Set goals for HT22 
   * Submit SSI article and Courier article for publication by end of year.
   * Conference presentation(s): Ben will submit a proposal re: the project to DHiS Lund (November 2022). Fredrik will present other work there, but nothing from this project. Focus instead on DHNB 2023 (online in March 2023). Ben will present on the project at AHA Conference in Philadelphia, January 2023.  
   * Hosting an event: we discussed idea of a smaller workshop, on international/global and/or digital conceptual history, to take place in Spring 2023. Next step: Ben will discuss possible ideas with Jani Marjanen, among others.
   * Preparing RJ infrastructure application: we should do this, and begin preparing a rough draft by no later than October.

1. New meeting day is Wednesdays, 13:15 until (at latest) 15:00, according to attached schedule:

1. MEETING SCHEDULE HT2022
   * 14/9  (just B and F), OBS kl 11:00
   * 28/9
   * 12/10 (just B and F)
   * 19/10
   * INIDUN-dagarna i Umeå: 
     - tisdag 1/11, kl 9-12 
     - eventuellt ett em-pass med Ben, Roger och Andreas
     - onsdag 2/11, kl 10-12.
   * 8/11  OBS tidsag, kl 13:15 (just B and F)
   * 30/11
   * 13/12, OBS tisdag, kl 15:00



_Agenda_

1. Updates
   * Hiring a student assistent (again) is on track
   * New work levels (percentages): hur ser det ut? 

1. Status of Courier work

1. Status of Proceedings work

1. Status of writing tasks
   * SSI article
   * (first) Courier article 

1. Set goals for HT22 
   * With Courier
   * With Proceedings
   * Publications
   * Conference presentation(s)
   * Hosting an event?
   * Preparing RJ infrastructure application

1. Prioritize among these goals, set in time-line




### Meeting, 5 April 2022 (via zoom)

_Notes_

1. Updates?
   * Fredriks RJ infrastructure application made it to second round, so he will need to prioritize that for a while.
    
1. Hiring a student assistent
   * forskningsassistent, not amanuens!
   * B showed draft text of position advertisement; will proceed with this via UU official "lediga jobb" system.
  
1. Re: SSI work in jupyter 
   * Status now is up and good, but:
   * R and A will doulbe-check that the wordcounts in jupyter match those in VSC. B will run a similar test.

1. Re: Courier
   * R and A have prepared [instructions](https://github.com/inidun/tagged_courier) (for an assistant) for manually curating Courier.
     * Focus at this stage is ONLY on correctly marking the start of each article (segmentering). 
     * Editing the texts themselves (correcting spelling, etc) can be done later, if at all.
     * Some texts will be OCR'ed again: R and A decide which ones.
     * The technical difficulties of curating the first years (1948 through 1951) are so great that we might just limit the corpus to the years in which Courier had a magazine format, that is from 1952 to 2011. We will in any case start the manual "segmentering" work with the 1952 issues. Later B and/or F can evaluate how important it is to include 1948 to 1951, and how long it would take to tag the articles in those issues.  
     * We will use a new label to mark when UNESCO's own editorial texts start (since these are not listed as articles in the Courier metadata. Probably something like #starteditorial. Other material that is neither an editorial nor an article can be tagged with #nonarticle_text or maybe #ignore 
   * A and F will meet with Marita at Humlab on 6/4 to do a test of the instructions and invite her feedback.
   
   
_Agenda_

1. Updates?

1. Hiring a student assistent
   * forskningsassistent, not amanuens!
   * Draft text of position advertisement: comments?
  
1. Re: SSI work in jupyter 
   * status now?

1. Re: Courier
   * curating status?
   * Working with student assistant at Umeå?
   * Courier TM article: 
   	- update
   	- next steps


### Meeting, 1 March 2022 (via zoom)

_Notes_

1. Discussed problems with SSIs in jupyter

1. Discussed idea of hiring a student assistent (amanuens)
   * R and A will prepare instructions for student's work
   * B and F will try to follow these instructions on one or more documents, as test.

### Meeting, 1 February 2022 (via zoom)

_Agenda_

1. Updates

1. Discuss and agree on [2022 goals](https://github.com/inidun/Project-PM-minutes-and-notes/blob/master/2022_planning_doc.md)

1. Discuss pitch to UNESCO re: "The Curated Courier"
   - Look over [draft presentation](https://docs.google.com/presentation/d/1mw-xmL3j9dHxd29EnIkKJvewCiyJnqoHzhybvtMA94A/edit?usp=sharing)
   - Discuss the actual project idea: what can/should we promise? What's our ideal outcome?
   - Re: presentation, decide on timeframe, division of labor.
 
1. _Courier_
   * Status update
   * Make concrete plan to hire amanuensis for manual curating!

_Notes_

1. Discussed idea of collaborating with UNESCO on "The Curated Courier", all seem positive.
   The general plan is to proceed with our own curating and research, while we wait to see how UNESCO responds to our proposal.   

1. 2022 goals approved.

1. Next steps: 
     - B will finish draft "Curated Courier" presentation; share with others for feedback; then send to UNESCO archive.
     - B will hire amanuensis to assist with manual curating of Courier.
     - B and F will take first steps toward convening a workshop on Courier, November 2022 
   

### Meeting, 9 November 2021 (via zoom) 

_Agenda_

1. Courier 
   * curating status
   * Working with topic models: update, questions?
   * B questions re: TM jupyter page: 
     * Does it always generate a new topic model? How do you see/download the current one? [No; they are stable.]
     * In Find topics by token: What "topic weight" is significant? (Default threshold is 0.20) [This means that topic accounts for roughly 20% of page content.]
     * What is best way to identify changes in topic weights before and after a particular date? [We have no one tool for this; but we can check the Topic Trends over Time for selected important topics, for example.]
     * What does it mean, really, if we find a particular topic spiking at a particular time? [Shows that the words in that topic appear with greater proportial frequency in pages from that year.]
     * How to read heatmap results? [Many of the dark green squares are garbage topics. But not all; look at this again, more carefully.]
   * Courier conference paper (DHiS 2021): Draft introduction is now up in [INIDUN drive](https://docs.google.com/document/d/1NU_RjrV84_yR-0wGJI1P4s-6spZlOrDiCJhvrzfUybE/edit).

1. SSI paper
   * Status
   * Some ideas: 
     * How to identify/measure a word's use as a category of practice? Some thoughts: 
     * identify the verbs that are linked to 'culture' and 'cultural'?
     * identify what things (categories of people, objects, practices) are gathered most frequently under the headings culture and cultural. 
     * Make a ranked list of these things, and see how that list changed over time. 
     * (How to do these things?)
   * Go through how to use jupyter page (one more time!) (Or maybe later)
     * Is Ben's INIDUN page up to date?
     * Start with "compute DTM"...  

1. Coming meetings:
   * Move 7 Dec meeting to Wednesday 8 Dec (in Umeå) - possible?



### Meeting, 2 November 2021, just Ben and Fredrik (via zoom) 

_Agenda_

1. SSI paper
   * Discuss B's new draft idea
      
   * B's questions for FN:
     - OBS: bigram frequency numbers in figures 5-13 do not match those in table 1.
     - Table 1: things that appear only once; should we even count these? 
     
   * Questions re: new approaches 
     - the notion of popular participation in culture and talk of the state and "policy" seem to have been linked (in 1976 Rec on Participation, for example) CHECK: Can we confirm that link statistically?
     - There seems to be a line of development, where a few key ideas were expressed in the 1970s that then emerge in the 2001 Diversity Declaration, and in the 2005 Diversity Convention. Can we measure and maybe visualize this: show that you can really see the terms, or a particular semantic field, moving along and re-appearing in those two instruments, but _not_ in other UNESCO SSIs?
     -   
   * Working with the noun 'culture' in the SSI corpus
     - Create list of adjectives that modify culture
     - I did this in antconc, but how can we sort by date? 

   * Other ideas:
     - Compare language of recommendations/declarations as a group to that of the conventions. (Do certain ideas make it through the majority, but not up to 2/3 level?)

   * Working with Jupyter:
     - Walk through (again) how to get this going (Compute DTM, etc)
     - If I find errors in the texts, where should I fix them (so that it's fixed once and for all)?

   * Practical question: When exactly does DHiS end?

### Meeting, 19 October 2021, just Ben and Fredrik (via zoom) 

_Agenda_

1. SSI paper
   * Go over critique from recent seminars
   * B's questions for FN:
     - How much of the grown of AND can be tied specifically to the word cultural? (p. 16)
     - How did average length (token count) of SSIs change over time?  
     - Problem with hyphens in the way the algorithm identifies words: 
       - co-operation appears as "co-"
       - The network visualizations show several single letters
     - Idea: a graph showing relative frequency of selected bigrams across the whole period (see Per W's comment) 

1. SSI paper: Plan going forward
   * B. will: 
     - read/review lit on global/international history of culture concept
     - read/review lit re: debate on "culture" at UNESCO
     - develop sharper questions
     - draft new intro (by 2/11)
   * F. will: 
     - Improve text tool (hyphen problem, etc)
     - Leave this for now and move on to _Courier_...?  

### Meeting, 12 October 2021 (via zoom) 

_Notes_
1. SSIs
   * Time to design a jupyter page related to the SSI article? 
     - B and F will decide about this; but in any case the page need not be ready before article is about to be published.
   * B's specific questions for FN: (for next meeting)
     - How much of the grown of AND can be tied specifically to the word cultural? (p. 16)
     - How did average length (token count) of SSIs change over time?  

1. Courier
   * Looked together at topic modeling jupyter page
   * Look together at topic modeling results (google drive)
     * What's going on in 50 topics, t 6? (Probably a few issues with poor OCR)
     * B asks: How can we use these to see change over time? Can we do TM to the texts in time blocs? Or identify topics in the whole, and then measure their relative frequency over time? Answer: Best to isolate a topic, then measure the frequency of its appearance over time; there is already a tool for this on the jupyter page!
     * F and B will make edits (above all, labeling the various topics) in the google docs versions of the files.
   * Curating tasks: update and plans: R and A will go back to the problem of isolating issues after fixing a few more TM-related tasks.

1. Proceedings
   * B wants to scan in 700 pages of text (1976 Proceedings): do we do that KB lab, specially? Or just put in the order at KB as usual?
     - B will wait with this: start by asking UNESCO (again) if they have done this, or are going to do this. If necessary, start by asking a contact at KB Lab, rather than just giving this to the library's normal copy service.  
   * What ARE we going to do about the two-language issue? What is the next step in deciding how to handle this?
     - A big issue, to return to later!

1. NEXT MEETING, 19 Oct (just B and F)
   * Go over comments we've gotten on the SSI article; make plan for cutting it in length and finishing and submitting it!
   * Discuss _Courier_ work plan: 
     - what are the historical/analytical questions we want to ask of this material?
     - division of labor?
     

_Agenda_

1. SSIs
   * Time to design a jupyter page related to the SSI article?
   * B's specific questions for FN: 
     - How much of the grown of AND can be tied specifically to the word cultural? (p. 16)
     - How did average length (token count) of SSIs change over time?  

1. Courier
   * Look together at topic modeling jupyter page
   * Look together at topic modeling results (google drive)
     * What's going on in 50 topics, t 6?
     * How can we use these to see change over time? ("Dynamic tm"...?) 
     * Can we do TM to the texts in time blocs? Or identify topics in the whole, and then measure their relative frequency over time?
     * Should F and B make edits in the google docs versions of the files, or in excel?
   * Curating tasks: update and plans

1. Proceedings
   * B wants to scan in 700 pages of text (1976 Proceedings): do we do that KB lab, specially? Or just put in the order at KB as usual?
   * What ARE we going to do about the two-language issue? What is the next step in deciding how to handle this?
     

### Meeting, 23 August 2021 (via zoom) 

_Notes_

1. No big changes in people’s schedule

1. Re: SSI work: 
   * B and F will keep working on article.
   * Re: a jupyter page for the SSI article:
	  - Next step: B and F decide on the narrative of the jupyter page  
	  - Then: put up everything we use in the article (data, etc) on GitHub
	* So, basically, we should just finish the article. Then, when it’s at a good draft stage, we design the jupyter page. Once that’s in place, B and F contact R and A

1. Courier 
   * Curating is going well; should be ready before 15 Dec.
   * 	Status: the OCR text extraction, via PDF Box, has been v good, but not perfect. Sometimes the word order is a mess because the columns got pushed around. But that may not be such a huge problem for certain kinds of analysis. This is an issue that the developers at PDF box and Tesseract and other such places are best on, so R does not really want to get into this too deeply. But we can make small changes, since PDF Box is open source. But in any case, topic modeling is not affected by word-order problems.
	* F suggests two parallel processes: 
	   1. Start working already now with word trends, cooccurrence, NER. (Use the existing jupyter pages for this.)
	   1. F and B begin already now thinking about an article (or two) based on this material. We could divide up the material by issue (or maybe page); while we’re waiting for Andreas to improve the division of the total corpus into articles.
	* Next step: R and A will make it possible to select and work with the Courier corpus in the same pages where we’ve been working with the SSI corpus.

1. Proceedings
   * B presented state of affairs with curating Proceedings.
   * Next tasks: 
      - Task group A:
        -	Rename the PDFs that Eng sent me, put them in the main file
        -	Create one or more new txt files from selected Proceedings issues (starting from the first ones), using Adobe's OCR function. 
        -	Send the resulting text to Andreas; he will compare its accuracy with what he gets from doing the same thing in Tesseract.

     - Task group B
      -	I should do a test, timed, of how long it takes to clean up and mark up a volume. With these tasks:
         - Go through each vol and see what the rules are for marking a new speaker.
         - Find out: do all volumes use numbers, like 3.1 (and (3.1) for translations) to mark new speakers?
         - Tag each new speaker with (underscore)"start" and (underscore)"end". 
         - Leave all text and mess in place 

1. Outreach
   * We should blog and tweet! Ben agrees to try...

End of meeting

_Agenda_

1. General updates

1. Approve 2021 meeting schedule

1. Look over, approve revised [2021 goals](https://github.com/inidun/Project-PM-minutes-and-notes/blob/master/2021_planning_doc.md) 

1. Review how we use kanbans; other aspects of project communication

1. SSI article
   - status
   - When/how to create associated jupyter page, and/or published version of data?

1. _Courier_ curating
   - status, plans

1. _Proceedings_ curating
   - status
   - How to save updates to metadata file?
   - Make plan of next steps 
   - See [updated PM](https://github.com/inidun/Project-PM-minutes-and-notes/blob/master/Source_PM_1_Proceedings.md)


### Meeting, 1 June 2021 (via zoom) 

_Notes_

1. SSI article: did status update 

1. Courier curating
   - Status: moving forward; using PDF-Box; using font size to identify article titles, and thereby insert breaks in the text. Then, test against the article index to see if this method works well.

1. Summer schedule
   - meet again ca middle of August.


### Meeting, 4 May 2021 (via zoom) 

_Notes_

1. Courier curating
   - status:
     - R and A are working on recognizing breaks between articles.
     - There may need to be some manual editing of article texts (to identify where they end); R and A will try to identify how long that might take.
     - The former problem with missing issues is resolved.
   - next tasks? 
     - R and A will continue with this, trying to shorten list of overlap articles; 
     - By next meeting: R and A identify some samples for B and F to check (comparing PDF images to the article txt files for accuracy)  

1. Goals update
   - Before midsommar:
     - Aim to have complete, usable Courier corpus
     - B and F aim to have complete article re: SSIs
     - B will have taken some decision re: Proceedings 
   - HT2021:
     - Main curating task: _Proceedings_ (or maybe another UNESCO text source)
     - Main analysis/writing task: analysis of _Courier_ 

1. INIDUN jupyter pages
   - R will update the INIDUN pages to match latest developments (done for Westac). 
   - New meeting with run-through of how to use these pages on Wednesday, 12 May, 13:00.


_Agenda_

1. INIDUN Jupyter pages
   - B. questions re: making it work
     - creating a DTM
     - POS statistics page (error messages)
   - 

1. Courier curating
   - status
   - next tasks? 


### Meeting, 30 March 2021 (via zoom) 

_Notes_

1. Updates: there will be a new boss at Humlab

1. SSI article:
   - R and A will make the edited corpus ("nonregional") into the one used in jupyter. 
   - B already made edits to (his, google drive version of the) SSI metadata index, adding a column for regional?=yes/no. Andreas will copy this into the official metadata index.
   - B and F will continue working on text analysis and writing; deadline by end of VT21. 

1. Curating _Courier_: 
   - Pagination issue: R and A report on their way to make page numbers match between metadata index and text files; not done but going well. 
   - There are 1100 pages on which more than one article appears. As it works now we would duplicate (some of) the text on these pages. So we need to check these; A. will continue working on a (partly?) machine-driven solution to this issue.

   - Several whole issues are missing (we don't have any text or PDF at all). These are:
      - 059709eng no match
      - 124785eng no match
      - 367693eng no match
      - 370032eng no match
      - 370977eng no match
      - 372603eng no match
      - 373788eng no match
     F. will check these: they seem (mostly) to be modern. Are they (not) online in UNESDOC? We could ask Eng (at UNESCO archive). Or we could exclude them, since they are so recent (and outside of the project's 1945-2015 time period). 
     
   - One PDF couldn't be handled by PDFBox: 132107engb. We need to either remove it from the sample, or OCR it ourselves (with Tesseract or other tool); but then remember to note that this one was NOT extracted using PDFBox. 
   
   - The corpus is based on Courier articles, working from the metadata index which lists these; that means it does not include all of the text in the issues. What kind of content do we lose by assembling the corpus in this way ? 
      - Editorials
      - Welcome note
      - Letters to editor
    We could extract the text of the editorials as its own separate corpus, and do analysis on that. To come back to later.

1. Proceedings: 
   - B. sets end of VT21 as deadline for deciding whether or not to proceed on curating Proceedings. 

End of meeting.


_Agenda_

1. Checking in, updates

1. Questions, updates re: SSI text analysis

1. Curating _Courier_: 
   - Pagination issue: R and A report on their way to make page numbers match between metadata index and scanned files.
   - Title coordination issue: how much of a problem is this? (Not much)
   - In courier/articles, a problem?: "Sorry, we had to truncate this directory to 1,000 files. 5,938 entries were omitted from the list." (Not a problem!)
   

### Meeting, 9 March 2021 (via zoom) 

_Notes_

1. Fredrik updated us on on-going text analysis work with UNESCO SSIs. He is doing this in AntConc, and has already noted some trends of interest. FN and Ben will meet in two weeks to proceed on this. Goal is to bring our observations into dialogue with arguments made in the existing (legal-historical) literature on the SSIs.

1. Curating _Courier_
   * Fredrik reported on his tests of different OCR options; found that PDFBox was best here. 
   * Roger and Andreas have already run PDFBox on Courier, divided up page by page (see in Inidun_data)
   * Next steps are to link the pages to particular articles, link the article's uinque numbers to the metadata file, and to identify problems, for example pages on which one article ends and another starts.
   * Goal: to have a corpus before the summer.  
   
1. Next meeting (just B and F), 23/3. Next meeting with all of us, 30/3.   

_Agenda_

1. Checking in, updates

1. Quick look at Fredrik's text analysis work on UNESCO SSIs, in this [document](https://docs.google.com/document/d/143A2OjFJPlJAstZ23I1s2Y9lJD27zLV1Rc_rnYnRoIY/edit?usp=sharing)

1. Curating _Courier_: status?


### Meeting, 2 February 2021 (via zoom) 

_Notes_

1. We discussed the data storage question list as item three in agenda (below). Decided to move scraped files out of "UNESCO_data_collection" and into INIDUN_data. Ben made copies of his own, edited versions of the SSI corpus (divided into blocs, with year first) and saved these on google drive.

1. B showed the _Proceedings_ metadata file we recently received from UNESCO. 
   * Ben will edit this excel file by adding various columns to it, with which to keep track of things like: do we have it? Has the OCR been quality controlled? Is the sourse the UNESCO digital archive or UNESDOC, is the text in English or English+French, and (importantly) which are the relevant pages we want for inclusion in the corpus? 
   * R explained that if we want GitHub to "version" each small change we make in the document I will need to save it as a CSV file, at least sometimes, in addition to keeping it in Excel.

1. R and A showed us preliminary results of using tesseract to do a new OCR of a sample of Courier PDFs. R, A, and F agreed on various tests to move forward toward a curated digital txt corpus of Courier.

1. We looked through the jupyter pages related to the UNESCO SSIs (legal instruments).
   * We found a bug in the POS_statistics page: the relative frequency of all parts of speech seemed to go up, following the curve of the total number of tokens, even when the "normalize" button was clicked. R and A will look into this. 
   * Also, the tokens counter included delimiters (punctuation). (Should it?)

1. __Next steps:__ 
   * R, A and F will continue work on _Courier_
   * B and F will meet on 16/2 to discuss ideas for an article re: UNESCO SSIs. Will assemble questions for R and A re: jupyter, and/or create "issues" in GitHub. 
   

_Agenda_

1. Discuss Jupyter pages: questions, problems?

1. Curating _Courier_: status?

1. Data storage
   * Potential problem: I see that the GitHub repro UNESCO_data_collection (designed for code related to actually scraping/collecting the data), in a subfolder called "data", we are keeping the Proceedings files that we scraped in 2019, and the SSI files that we scraped, as well as later, edited versions of these, like the one I made with the dates first (for easier use in Voyant). Isn't this creating confusion? That is, the actual corpora should not live there, but in "INIDUN_data", no? 
   

### Meeting, 19 January 2021 (via zoom) 

_Notes_

1. Updates
   * During 2021 Fredrik will be on the project at 15%, but with some flexibility. 
   * Ben may choose to reduce his active percentage during 2022, so as to keep the project active longer.
   
1. Meeting schedule is OK.

1. Project goals (as outlined in [2021 Planning Document](https://github.com/inidun/Project-PM-minutes-and-notes/blob/master/2021_planning_doc.md)) are OK.

1. Data storage
   * Roger reports that GitHub can host much larger files than we thought. The guiding principle is that items about which we want detailed, careful information on changes and versioning should be kept in GitHub. Everything else can be on google drive.
   So, here is the new, revised version of our data storage plan:
   * GitHub: 
     - All UNESCO text corpora (in the versions we scrape or receive from UNESCO, and in curated versions)
     - Metadata files (for example, indexes that we receive from UNESCO or create ourselves)
     - Code written for the project
     - Project website and blog
   * Google Drive: in folder called [INIDUN (drive)](https://drive.google.com/drive/folders/15bjGlGLLWcyxoZbcUSBu2FkNtI-8kRXH):
     - Outputs (for example, data outputs that R and A produced in response to requests from B or F, or that that B or F create themselves)
       - OBS: These should be saved with carefully marked (and dated) titles, in a clear system of folders 
     - Drafts of texts we write for publication
   * TASK: Ben will move some things from Drive to GitHub  

1. Jupyter
   * Roger showed us the new jupyter pages for the project.
   * TASK: B and F will look at these and prepare questions for next meeting, 2 February. 

1. Work flow
   * Since these jupyter pages are already up, Ben will revise work flow section of 2021 planning document.
   * A general principle: start cheap! This means, 
     - B and F should ask R and A for simple things first, for exploratory research.
     - As research questions stabilize, we ask for bespoke tools.

1. Topics for next meeting (2 Feb):
   * Jupyter pages: discuss B and F questions
   * Curating _Courier_: decide on approach, next steps.

_Agenda_

1. Updates
   * Hur ser VT21 ut för oss?
   * Status of communication with UNESCO
   
1. Review notes from December meeting
   * VT21 meeting schedule OK?
   * Take (final) decision on issue of where to store data
   
1. Discuss [2021 planning document](https://github.com/inidun/Project-PM-minutes-and-notes/blob/master/2021_planning_doc.md)
   * Goals OK?
   * Work flow OK?
   * Tasks OK?
   
1. Take decisions re: VT21 goals and working methods

1. Close meeting

### Notes on meeting, 8 December 2020

1. Roger gave us a tour of pNLoP ("Penelope"). Important to note that this represents an artefact and achievement of the project; to be mentioned when reporting back to funding agencies!

1. We looked at one example of a text-analytical document prepared through Penelope: co-occurrence data (in Excel) for nouns, verbs, and adjectives in the UNESCO SSI text corpus. Roger will make this document available on google drive (see below)

1. R suggests that, although getting bespoke tools up on project-specific jupyter pages is the goal, Fredrik and Ben can and should ask for data outputs in the meantime. We can work with these ourselves (through Excel) and in that way determine what sort of text curating we want, and what sort of text analytical tools we want.    

1. Re: data storage and sharing: 
   Ben suggests the following:
   - GitHub: Small data files can continue to be kept in GitHub (in the folder called INIDUN_data)
   - Google Drive: The following kinds of data will be kept in folder called [INIDUN (drive)](https://drive.google.com/drive/folders/15bjGlGLLWcyxoZbcUSBu2FkNtI-8kRXH):
     - Larger data files (for example, text files that we scrape or receive from UNESCO)
     - Metadata files (for example, indexes that we receive from UNESCO or create ourselves)
     - Outputs (for example, data outputs like the SSI co-occurrence data file mentioned above, or ones that B or F create themselves)
     - Drafts of texts we write for publication
   - Comments on this plan are welcome!

1. B will ask Ulf S. if B can have an UmU email address, which might facilitate other forms of data-sharing and communication.

1. Meeting schedule for VT21: 
   - B suggested a schedule with meetings every 2 weeks. On consideration, a new suggestion: that B and F meet every two weeks, and all four meet once a month (Tuesdays at 13:15), as follows. (This includes two short meetings with all of us, to get the year started.)
      - 19/1 
      - 2/2 
      - 16/2 (just B and F) 
      - 9/3 
      - 23/3 (just B and F)
      - 30/3 
      - 13/4 (just B and F)
      - 4/5
      - 18/5 (just B and F)
      - 1/6
      - 15/6 (just B and F)

1. _Before_ our January 19 meeting:
   - Ben will circulate a document including:
     - Suggested goals for VT21
     - Suggested (specific, delimited) tasks
     - An outline of a work flow, specifically related to the tasks in question.

1. Do to _at_ January 19 meeting (a partial list):
   - Discuss work planning document 
   - Take decisions re: VT21 goals and working methods
   - Revisit issue of where to store data; take (final) decision on this.


### Meeting, 8 December 2020 (via zoom) 

_Agenda_

1. Updates 
   1. Uppdateringsrunda
      - B. question re: GitHub security warning
      - B. quick update re: CultIntSoc status
   1. Approve meeting agenda

1. Penelope: 
   1. Roger shows us the new system

1. inidun.humlab.umu.se: 
   1. Quick presentation
   1. Plans for how to use this

1. Reviewing our work methods: 
   1. Roger's suggestions
   1. Decide on concrete changes
   1. Prepare a work-flow document (as guideline for 2021)?

1. New work methods in practice: UNESCO's SSIs
   1. Outline next steps for this sub-project
   
1. Data management (reviewing where we keep what):
      - What goes on GitHub?
      - What goes on inidun.humlab.umu.se?
      - Where to store Ben or Fredrik's provisional text analysis outputs? 
      - Google docs (or other shared writing platform)?
      - See (and edit?) task in main project kanban re: "Move all relevant data...". 

1. Source material questions

   1. re: _Courier_: Where things stand (Fredrik)

   1. re: _Proceedings_ on UNESCO dig archive: 
      - Status: B. will go through this, determine which pages we want, etc. 
      - Eng's technical question: "They were digitized as one file per page, so all the files belonging to a single document need to be integrated. Would your team be able to find a way to do this? (all the files belonging to the same document share the same file name, with then a sequential number appended – e.g. 223336_ENG_0001, 223336_ENG_0002 etc)." Can we manage this problem?
      
   1. re: Proceedings texts on UNESDOC: 
      - Discuss a Plan B (if UNESCO cannot arrange batch download)
      - Scraping Proceedings: How much was already done? OCR/text quality? Can this be done again with better quality?
      - Schedule this as task for (relatively) early in 2021. 

1. Setting (revised) goals for 2021
   - How to do this? 
   - Suggestion: B. prepares and circulates draft; we decide on it at first 2021 meeting. OK?

1. Meeting schedule for VT21:
   1. B suggests: 
      - 19/1
      - 2/2
      - 16/2
      - 9/3
      - 23/3
      - 13/4
      - 27/4
      - 11/5
      - 25/5
      - 8/6
      - 22/6 

1. Close meeting



### Meeting, 3 November 2020 (via zoom) 

_Agenda_

1. Updates: 
   1. Partnership agreement (almost) done
   
1. Working with UNESCO SSIs:
   1. Status of jupyter page(s) for working with this corpus?
   1. Discuss process for working on an article using (only) this corpus:
      - order of work
      - division of labor
      - time-frame

1. _Courier_:
   1. _Courier_ metadata excel file: all ok? 
      - Plan for storing, updating, versioning
   1. Downloading _Courier_ texts. Eng (at UNESCO) says a batch download "might take a while" and encourages us to think of a plan B. What could that be?
   1. Scraping _Courier_: possible? Already done? Problems?

1. Proceedings:
   1. Note: General Conference sessions 1-7 (1946-1952) are in UNESCO digital archive. The rest (1953-2015) are in UNESDOC.
   1. Discuss Eng's offer to get us the Proceedings texts from [UNESCO digital archive](https://digital.archives.unesco.org/en/):
      - "They were digitized as one file per page, so all the files belonging to a single document need to be integrated. Would your team be able to find a way to do this? (all the files belonging to the same document share the same file name, with then a sequential number appended – e.g. 223336_ENG_0001, 223336_ENG_0002 etc). Our developer has been working on a script to automatically integrate all pages into single documents, but has not had time to implement this yet."
      - Can we manage this problem?
      - Review how much of the total this includes.
      - B. could identify specific page numbers and get those to Eng.

   1. Re: Proceedings texts on UNESDOC: 
      - Discuss a Plan B (if UNESCO cannot arrange batch download)
      - Scraping Proceedings: How much was already done? OCR/text quality? Can this be done again with better quality?
   
1. Review our mode of working
   1. Using the kanban. Useful? How to make more dynamic?
   1. Consolidate all project-related data in GitHub. (How?)
   1. Other changes needed? Should we meet more often (next year), or in a different way? 
   
_Notes_

1. Roger and Andreas will let us know when jupyter page for SSIs is up.
1. Andreas created a new repository in GitHub for actual data from corpora, including the new Courier metadata file.
   - Ben downloaded a copy of this folder (in the INDUN folder) from GitHub to hard drive. Can look at this with a “edit csv” plug-in (from VSC marketplace).
   - We should gradually move data that’s now elsewhere in GitHub, Google drive, or on Open Science to this repository. Right? 
      Answer: Not necessarily. GitHub is for code; data (and outputs, etc) should be stored elsewhere. 

1. Courier: 
   - Fredrik will quality control the _Courier_ metadata file by checking (in particular) if the article titles and page numbers are correct on a random sample of issues. 
   - We will need to extract the _Courier_ text (into simple text, from the PDFs) again, article by article.
   - Ben should ask Eng if UNESCO has txt files of the Courier PDFs (or another format?). What we want is the text in textual/reading order (not as it appears on the page). 
   
1. Other issues: 
   - Ben will discuss Eng's technical questions (re: Proceedings) with R and A via email. 
   - We did not get to other points re: Proceedings, nor to the issue of reviewing our work methods. To return to in December, or at a mellan-möte (Tuesday, Nov 17?).



### Meeting, 6 October 2020 (in Umeå)

_Agenda_

1. Updates, status
1. Work with UNESCO SSIs
   1. Look together at current set of text analysis tools.
   1. Using index (for example: ways to measure how many countries, absolute number and % of total number of member states, signed/adopted which of the resolutions and declarations?) 
   1. Compare to work B and F did with SSIs for Lund talk (in Voyant)
   1. Discussion of _meaning_ of co-occurrences plotted as graph...!
   1. Tools for Moretti-style analysis of SSIs?
   1. Discuss an article using (only) this corpus; order of work, division of labor?
   1. Set time-frame for work on such an article
1. _Courier_: 
   1. Status (F and B report) 
   1. Next steps?
1. Proceedings
1. Other matters
   1. Reading group re: relevant DH methods (incl re: digital conceptual history)?


_Notes_

- The new text analysis tools should be opened and used in jupyter at inidun.humlab.umu.se. The code is stored in GitHub.
- We added several issues regarding new features to add to new Word trends tool (word_trends.ipynb at inidun.humlab.umu.se), in part inspired by Moretti and Pestre, "Bankspeak."
- Decision: we will focus, for the SSIs, on a small group of tools: 
  - word trends
  - most discriminating words
  - collocates
  
Roger will try to re-use tools from CultIntSoc and Westac (common things are kept in area called penelope). Timeline? 
He will let us know when the new versions (in jupyter) are ready to use. 

In the meantime, B and F will focus on: 
- identifying arguments (in the scholarly literature) to test in the corpus
- developing argument about what exactly the SSI corpus is and can show. What is its value as an object of study?
- developing argument about value of digital approaches at all, given small size of corpus
- Timeframe: try to complete and submit an artile on SSIs early in 2021.   


Re: curating UNESCO _Proceedings_

B will continue discussing w UNESCO how to get whole downloads of text files.
Then, B will work on tagging/marking up these texts with # markers, designed to facilitate cutting up the text into usable pieces and creating metadata. These can be inserted into the text file before the text in question, to mark:
1. when a particular session of the General Conference begins: #SESSION_START
1. when a new speaker begins speaking, including UNESCO title (where relevant), country, and language (only EN or FR): #SPEECH_INDIA_EN

B can start doing this with one or two years of _Proceedings_; eventually we might get help from a paid student or other support. 

In the meantime:
- B and F can read up on UNESCO (especially, for F, _Courier_). In each case, they will think about what the corpus _is_, and what sorts of things it can allow us to say. That is, once we are able to do text-analytical work with these corpora, we want to be ready to make an argument about what claims about these corpora show about history and the world (!).   



###  Meeting, 1 September 2020 (via zoom)

_Agenda_ 

1. Updates, status
1. Status of UNESCO SSIs
   1. Quality-controlled?
   1. Desired text analysis tools
   1. Time-frame for work on an article using (only) this corpus
1. _Courier_: Status, next steps?
1. Proceedings: time frame for working on this?
1. Other matters?

_Meeting notes_

Three main results from today's discussion:

1. Roger and Andreas will focus during September on putting together a jupyter page with a few text-analysis tools for use on the SSI corpus. These will include:
   * PoS-tagging
   * a word trends tool, to measure word frequencies, etc.
   * a collocate measuring tool, with: 
     * adjustable window size
     * ability to export results for visualization in Gephi
   * a tool to identify most discriminating terms of each document (probably through Tf-idf)
     * ideal if this can be used also to identify the most discriminating terms of all documents in one time period as compared to other time periods (see division of corpus into three groups in INIDUN/unesco_data_collection/data/legal_instrument_corpus (dates first) in 3 groups.txt 

1. Ben will continue working on SSI, focusing on:
   * Learn more about how they work, which countries sign them, which are universal and which regional, etc. Will enter results into: https://github.com/inidun/Project-PM-minutes-and-notes/blob/master/Source_PM_3_SSIs.md
   * Quality control: Clean up the English in the text files
   * Continue work on developing historical arguments about the SSIs that can be tested/illustrated through digital text analysis. Writing on this will be in: https://github.com/inidun/Project-PM-minutes-and-notes/blob/master/UNESCO%20SSI%20paper%20notes.md
   
   
1. Ben and Fredrik will move forward with _Courier_:
   * Ben will contact UNESCO re: 
     * Can we have meta-data on all Courier articles?
     * Can we have Courier files in an XML format, rather than as PDFs?
   * Fredrik will:
     * Test extracting text from several issues, in different decades, to see how long it would take to do this manually.
     * Contact people (like maybe the author of this [page on Document Layout Analysis](https://github.com/BobLd/DocumentLayoutAnalysis)) to ask for advice on state-of-the-art methods for solving problems of the kind _Courier_ presents.
     * Continue reading in (and about) Courier, to familiarize us with the material.
       * Tip: Maria Simonsen, "Routes of Knowledge: The Transformation and Circulation of Knowledge in the UNESCO Courier, 1947-1955", in J. Östling et al., _Forms of Knowledge: Developing the History of Knowledge_ (Lund, 2020).
