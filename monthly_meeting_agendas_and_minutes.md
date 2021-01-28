## Minutes from INIDUN monthly meetings

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
