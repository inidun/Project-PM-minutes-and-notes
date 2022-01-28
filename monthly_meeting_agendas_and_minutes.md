## Minutes from INIDUN monthly meetings

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
