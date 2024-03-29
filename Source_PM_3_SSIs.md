# Memo regarding UNESCO standard-setting instruments (SSIs)

UNESCOs SSIs consist of three groups:
* Conventions
* Resolutions
* Declarations

We have already downloaded all of these. See the [excel file with list of these](https://github.com/inidun/unesco_data_collection/blob/master/data/legal_instrument_index.xlsx).

Additional note: in one case, UNESCO also published background documentation related to a particular SSI:
* Declaration on Mass Media (28 Nov 1978): see ["Historical Background of the Mass Media Declaration" (1982)](https://unesdoc.unesco.org/ark:/48223/pf0000047669).

Are there more like this? Searching for "historical background" in UNESDOC does not reveal any others.

Some of the Conventions are Regional in character. Especially a set of regional agreements "on the Recognition of Studies, Diplomas and Degrees in Higher Education" in Latin America, Africa, Europe, Asia-Pacific, etc, 1974-1983, and again one in 2019.

It would be worthwhile to think about measuring how many countries (absolute number and % of total number of member states) signed/adopted which of the resolutions and declarations. These are adopted by UNESCO's General Conference "by a simple majority, while a two-thirds majority is required for the adoption of conventions" (See [UNESCO's page of general info on SSIs](http://portal.unesco.org/en/ev.php-URL_ID=23772&URL_DO=DO_TOPIC&URL_SECTION=201.html#).)



*Update, 4 August 2020*

I added the texts to three SSIs (in the data file legal_instrument_corpus.txt) where the files were empty (2003, 2017, 2019). 


*Quality control of the texts (27 August 2020)* 

The SSI texts we have downloaded do not include the title at the top of the file (with the exception of the Constitution of UNESCO). That might be good, since those words are not, in fact, part of the treaty text, I suppose. It does make it hard to see which one you're looking at, but we are unlikely to read the texts in this form ourselves, and anyway the titles are visible in the excel list of all the SSIs. So I think that not having the titles in the text files is as it should be. Leaving as is for now.

_(2 October 2020)_
Ben completed manual quality control, and some spelling corrections, of all SSIs. Corrections made in the "dates first" version.

_(3 November 2021)_
Discovered an SSI that was not included in our list: the 1976 Recommendation on the Development of Adult Education (13096). On UNESCO's SSI webpages this is listed on the page "Theme: Education", but not on the main list! 
- Ben created new txt file, added it to INIDUN Drive, folder "legal_instrument_corpus (dates first)".
- Ben added this SSI to metadata, "legal_instrument_index Ben copy".

Checking for others we missed, I find another one: 
1978 International Charter of Physical Education and Sport. The original number of this one was 13150; but that number is taken by the revised recommendation of 2015 ("International Charter of Physical Education, Physical Activity and Sport"). There are interesting differences between this one and the current one! And OBS, this was amended in 2001, adding one paragraph (a new article 7: "Protection of  the  ethical  and  moral  values  of  physical  education  and
sport must be a constant concern for all") but otherwise leaving the text unchanged. See the 2001 version [here](https://en.unesco.org/sites/default/files/sport_e.pdf). UNESCO's collection, _Standard-Setting in UNESCO_ (2007), does not include the 2001 revision as a new, separate recommendation; so we won't either. But be aware of such modifications in other cases, too! For now:
- Ben created new txt file (called "13150_1978"), added it to INIDUN Drive, folder "legal_instrument_corpus (dates first)". 
  * NOTE: This document now appears in the metadata list "legal instrument corpus" as 90000. Should we make a renamed version of the 1978 one as 90000, too?
- Ben added this SSI to metadata, "legal_instrument_index Ben copy".

- (12 November 2021) Ben added both 13096 and 13150_1978 to INIDUN drive folder "legal_instrument_corpus_nonregional" AND to the INIDUN (master) collection "legal_instrument_corpus".

Removing one from our corpus? 
The Convention on Wetlands (Ramsar, 1971) is not included in UNESCO's own book _Standard-Setting in UNESCO_ (2007). It was, after not adopted by the General Conference, but at a special one-time international conference; UNESCO was the "depositary" for this convention, but it's not really a UNESCO SSI. On the other hand, it _is_ included in the list of Conventions on UNESCO's SSI website; and both that list and the 2007 book include other conventions adopted at special conferences, like the 1954 Protection of Cultural Property Convention (signed at the Hague) and the 1961 Phonogram Convention (signed at Rome). So for now we can leave it in the corpus. 

_(12 November 2021)_
Some SSIs have an annex, with quotations of relevant passages from other earlier international legal instruments. Note for example the 1980 Recommendation on the status of the artist (13138). Several other SSIs have an annex or appendix in which they define terms or list relevant existing instruments. But no other SSI seems to include an annex or appendix with long quotations from earlier instruments. You could argue that it seems reasonable to remove that part of the text from the corpus, since the presence of these phrases in the later document just throws off our results. On the other hand, they did in fact choose to repeat that language in this document, and that's part of what it did as an SSI. So, am leaving the 1980 document alone for now, but at least we have to be aware of it!   

_(25 February 2022)_
Trying to do word trend analysis of SSIs with jupyter I find that we are missing some documents: The problem is that the set of nonregional SSIs we’re using in jupyter is only 72 documents. The list I am using in Antconc and VSC has 74 documents. And it seems clear that the two missing are the ones I added in the fall: 
- 13096 (1976 Recommendation on the Development of Adult Education) and
- 13150_1978 (which appears in the master metadata file as 90000). (1978 International Charter of Physical Education and Sport, which appears under the number 13150 in its revised 2015 form.)  
Note: these two DO already appear in the master legal_instrument_index in our INIDUN file.

Now: we need to add these two to the metadata file that jupyter is using to create the nonreg SSI corpus. AND we need to rename 13150_1978 to 90000, I think, so that the system can find this file.

So, can I just go ahead and delete the existing metadata files in INIDUN/text_analytics/data and replace them with the updated ones? (Asked on 25/2 2022)
Update: these files were correctly included in the metadata files uploaded for use in jupyter. The problem was rather that 13150_1978 needed to be renamed to 90000 for it match the way it was listed in the metadata file. So I did this, and created new zipfiles, and installed them in text_analytics/data.

Did this, and created a new DTM (called SSI_NONREG_ALLPOS_NOLEMMA3_FEB2022), and it still does not give numbers that match what I found in VSC or Antconc. Sigh. 
