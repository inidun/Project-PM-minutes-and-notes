## Memo re: Proceedings of the General Conference


__General information__
The General Conference of UNESCO meets every two years (with some exceptional meetings between these). After each meeting a publication is produced, called Records of the General Conference of UNESCO. This includes several parts:   
* Resolutions
* Reports
* Index (sometimes)
* Proceedings
These are often published in separate volumes, but sometimes together (especially after “extraordinary sessions” like in 1953, 1973).

__Organization, lay-out, language, etc.__

Early _Proceedings_ volumes included the following parts: 
1. “General Information.” This includes the list of delegates, time-table, and list of documents of the session. 
2. “Verbatim Records.” 
	 This normally covers what was said in the Plenary meetings of the GC. This is transcribed text, as spoken by delegates and translated into English (if not delivered in English). This is likely the most interesting part of these texts. After about 1960 the Proceedings volume included only these verbatim records. 
3. “Summary Records.”
	 These are minutes (typ, mötesprotokoll) reporting on what was said in the meetings of UNESCO’s various committees (“The Director-General drew attention to the fact that …. Mr. Bernal Jimenez also agreed with the proposal…”), such as: General committee, Program and Budget commission, administrative commission, Advisory committee on program and budget, etc. 

_Language_: Early volumes seem to be available in just English. Later this changed. At the 15th session (Paris, 1968), the GC resolved that “that the verbatim records of its plenary meetings should be published in a single quadrilingual edition, in which only the speeches in Russian and Spanish should be translated into either English or French, alternately for each meeting” (Proceedings 1968, p. v). 
Today the rule is as follows: “Under Rule [51 and] 53 of the Rules of Procedure of the General Conference, the verbatim records are published in a single edition, in which each intervention is reproduced in the working language in which it was given and interventions given in a working language other than English or French are followed by a translation into either English or French alternately meeting by meeting.” [from Proceedings, Paris 2009]
This means that in many volumes, the main text is in both English and French, shifting between these languages from speaker to speaker (!), and may also include sections in Arabic, Chinese, Russian, and Spanish; these are followed by translation into English (or French).  
	


__Technical information__ 
The texts of the Proceedings are available through UNESDOC from 1953 (second extraordinary session). Some of these are in PDF form. A few are presented on the UNESDOC interface in OCR’ed form. These come with a warning text (repeated on every page): “Optical Character Recognition (OCR) document. WARNING! Spelling errors might subsist. In order to accessto the original document in image form, click on "Original" button on 1st page”. [But the “original” button does not always work!]. See information on how texts appear in UNESDOC in our list (“Proceedings access overview”)
…
NOTES on specific volumes 
* re: 1954 Proceedings: The text of “Verbatim Records” appears in two text columns. Each new paragraph is numbered in parentheses, like so: (1), (2), (3). Where there is a new speaker, the paragraph number is followed by the speaker’s name (with his/her title in parentheses). These titles (except for “The President”) tend to include a country name!
* re: 1960 Proceedings: This includes only “Verbatim Records”. They appear in two columns, numbered in a different way, without parentheses, and with a two digit system to mark when a new speaker begins: 1.1, 1.2, 1.3; then, 2.1, 2.2, etc. Each new speaker has a country name in parentheses. Sometimes the text has title headings, like “Address by the Director General,” but these speeches also open in the same way, with new number and speaker name. Titles (President, Director General) as well as all speakers family names are presented in ALL CAPS.
* re: 1968 Proceedings: This includes “Verbatim records of plenary meetings”, followed at the end by List of delegates and a list of “Officers of the General Conference and of the commissions and committees.” Text is in one column. Paragraph numbering and system for identifying speakers is unchanged from 1960.  [OBS: scan quality is poor…!]
* re: 2009 Proceedings: This includes “Verbatim records of plenary meetings”, followed at the end by List of delegates and List of documents. This also includes an index of “Addresses delivered in the general policy debate” organized by country name, or by organization name. This is printed in one text column. The numbering is as it was in 1960: Each paragraph is numbered with two digits (1.0, 1.1, and so on), with a new first number for each speaker. Each speaker, besides the meeting officials, is named and the name is followed by a country in parentheses. But the language shifts here between English and French! Note also that each section title is given in all six of UNESCO’s “working languages” (English, French, Spanish, Russian, Arabic, Chinese).
* re: 2015 Proceedings: Same as 2009 in layout and language policy.

__Decisions to be made__
* Do we have all the Proceedings texts? Which are missing? 
  * SEE Proceedings_metadata_edited for current overview of which we have, curating status, page numbers, etc.
  
* How to handle English and (at least) French in same document? How big of a problem is that? 
  
 __Wish list of curating tasks__

To be continued…

__NOTES on curating decisions__

3 Feb 2021: The Proceedings documents include a lot of text besides the minutes of the meetings of the General Conference. So these texts may in fact produce two corpora! For example: 
* Proceedings corpus 1: The verbatim minutes of the sessions ("Plenary Meetings") of the General Conference.
* Proceedings corpus 2: Everything else!
  * For example: 
    * the "summary records" of the various commissions
    * verbatim records of various commission meetings (for example in 1947)
    * "Reports" of these commissions submitted to the GC
    * "Resolutions" submitted to and/or adopted by the GC
  * This second corpus should probably include all text, _including_ Corpus 1. But it could be everything else (i.e., the total _minus_ corpus 1). 
  
  Either way, it seems clear that the rest of the texts in the Proceedings volumes, although not as clear as the verbatim records, are not useless! So:
  * Begin by isolating and curating corpus 1.
  * Along the way, determine how hard it would be to also curate the total, as Corpus 2.
    * Perhaps this Corpus 2 could be curated at a lower level of precision, just as a bag of words (per year), without the subtle details of marked-up individual speeches, etc. 

3 Feb 2021:
I will create a new .txt file including only the text from the verbatim minutes of the sessions ("Plenary Meetings") of the General Conference. Each such file will be called number_language_pm_corr.txt. PM for "Plenary Meeting", corr for "corrected" (to show that it is a finished, quality-controlled file). So for example: 114592_eng_pm_corr.txt. These will be saved in a folder called "Proceedings_PM_txt_files". When finished, they will be the content of Proceedings corpus 1.

...
__NOTES re: OCR and other technical matters__

3 Feb 2021: An OCR test: I opened a PDF (of those I received from UNESCO archive, 214793_eng_0029: the first page of the 1947 Plenary Session) in Adobe acrobat pro, and ran "Recognize text" on English UK, Output: editable text and images, Downsample to: 600 dpi. Then copied and pasted the text from the document and put it in a .txt file. This produced a pretty messy text, see "Adobe OCR test...", which I have saved in INIDUN_data, in a folder called "OCR_TESTS_Proceedings".

* How (specifically) did Roger produce the Proceedings .txt files that he scraped in March 2019? 
  * The versions of these documents that you can see in UNESDOC are, in fact, already OCRed texts produced (by UNESCO) from PDFs. There is a button you can press to see the original PDFs, but this does not always work (in the case of the 1953 second extraordinary session Proceedings, 114592).

* Are these text files good enough to use as is, or do we need to do them again? 
  * If not: Can we get access to the original PDFs so that we can do the OCR ourselves?
