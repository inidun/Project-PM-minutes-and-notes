## Minutes from INIDUN monthly meetings

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
