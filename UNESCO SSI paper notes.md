## NOTES toward a paper applying digital text analysis to UNESCO corpus A (standard-setting instruments, or SSIs)

**_Fredrik N., 29 June 2020:_**

Något jag har funderat på är om vi skulle kunna närma oss detta material på ett liknande sätt som Moretti och Pestre gör i sin ”Bankspeak”-studie, t ex för att studera huruvida språket har blivit mer abstrakt allteftersom fler länder som anslutit sig till UNESCO
 
* Legal docs (conventions, recommendations, declarations):
* Ca 80 dokument
* Totalt 268 884 ord
* 8 043 unika ordformer/tokens
* Topp 20 vanligaste ord: shall (2114), cultural (1840), article (1698), states (1555), convention (1553), education (1513), international (1118), state (1115), general (988), contracting (798), nations (754), educational (751), member (706), united (703), higher (695), scientific (657), national (652), heritage (630), organization (626), parties (624)
 
 
_Förslag på metoder_

* PoS-taggning – studera grammatiska förändringar
* Hur förändras antalet substantiv, verb och adjektiv?
* Använda liknande metoder som Moretti & Pestre i deras ”Bankspeak”-studie: Nominalizations (-tion, -ment, -sion) för mäta abstrakt språkbruk. Min grova undersökning visade att det relativa antalet ökade från 0,055 till 0,065 (i en jämförelse mellan perioden 1945–1955 och 2000–2019). Jag kollad även användningen av ”and” som fördubblas från 0,030 till 0,066 mellan samma period – möjligen kan vi alltså hitta liknande tendenser som i Bankspeak
* Most discriminating terms – mäta distinkta skillnader mellan olika tidsperioder/dokumentkategorier
* Tf-idf – mäta distinkta ord i alla enskilda dokument (i relation till hela korpus) för att studera ev förändringar och kontinuiteter över tid
* Samförekomstanalys – t ex av ”culture”/”cultural” – dela in korpuset i t ex 20-årsperioder för att studera förändring/kontinuitet vad gäller hur kultur omtalas i Unesco
 

**_Ben's notes, 30 June 2020_**:

_General thoughts on this article, how it might work:_

There are, I guess, two main ways to approach a first article using these sources: 

1. Do a Moretti-like exploration of the texts to look for stylistic and structural changes; find a historical argument in these.
1. Develop a hypothesis in relation to the existing literature, and use digital methods to test it against these sources; for example: 
   1. Changing meanings of ‘culture’: Scovazzi says X, Wouters and Vidal say Y. Does that seem to check out in the sources?  
   1. Continuity or change? : Many scholars present UNESCO’s goals as having been the same over time; they look back to the founding documents and find evidence that those goals have been pursued. (W and V do this, for example, by seeing diversity as a core value; Scovazzi does this by looking for “fundamental messages” of the organization’s treaties, even if he does acknowledge changes in UNESCO’s definition of culture.) By contrast, we use DH to look for continuity and change in these texts. 

For example: 
* Using co-occurrences, plotted as a network (in gephi) we let the computer identify concepts that were pivotal/central/nodal; and then look to see if these are/are not the same as the ones scholars have focused on.
* Or: Using some version of the tool used in Rule et al., "Lexical shifts, substantive changes, and continuity in State of the Union discourse, 1790–2014" (PNAS 2015), we identify lexical continuities and shifts in each of the three classes of documents (conventions, recommendations, declarations) and in the SSIs as a whole. 


**_Notes from meeting, 30 June 2020:_**

We agreed that the hypothesis-testing route was the best way to go; although I at least would still like to run some of the tests of the kind Fredrik suggested, inspired by "Bankspeak".

Next step is to identify our hypotheses, framed (ideally) against some statements by other scholars. Start with:

* Scovazzi, "Culture", in _The Oxford Handbook of United Nations Treaties_ (2019)
* Wouters and Vidal, "UNESCO and the Promotion of Cultural Exchange and Cultural Diversity", in Yusuf, ed., _Standard-setting in UNESCO._ Vol. I (2007)
* Francioni, "A Dynamic Evolution of Concept and Scope: From Cultural Property to Cultural Heritage", in Yusuf, ed., _Standard-setting in UNESCO._ Vol. I (2007) 

On that basis, identify several text-analytical methods we want to use to test these. Prepare a list of these methods (with reference to tools created for earlier projects) to present to Roger and Andreas by end of August 2020.

**_Identifying text-analytical methods to use on UNESCO's SSIs_**

I have started a file (in my own notes) called "Claims to Test". There I list claims historians have made that seem to be suitable for testing with digital methods. I divide these claims up by the corpus in which they would make sense to test, although of course some of these could be tested in all three.

The point _here_ is to make the link from (1) the claim, to (2) how (through which methods) we could test/explore it, to (3) which text-analytical tools would be most appropriate for these tasks? So, here are notes on claims from three relevant scholarly texts, and ideas about how to test (or follow up on) them.  

...

**Scovazzi, "Culture", in _The Oxford Handbook of United Nations Treaties_ (2019)**

Argues that meaning of culture in the SSIs changed:
 
* he notes changing meaning of culture concept at official UNESCO meetings, especially UNESCO's World Conference on Cultural Policies (Mexico City, 1982). 
	
PROBLEM: So, this raises a problem: this seems to be an important document, but was NOT an SSI. What category was it? Can we get (all of) those texts?     
	
* Basically, quite lame claims: argues that "two fundamental messages" can be drawn "from the mandates and activities of the United Nations and UNESCO in the field of culture, as reflected in the treaties of global scope adopted within the framework of UNESCO. First, culture contributes to the maintenance of peace. Second, the protection and promotion of culture is a general interest of the international community as a whole." (320). Can’t we do better than this? How? By asking: a) what did “culture” refer to in the SSIs; b) what role(s) did it play, or what work did it do, in the SSIs? 

So, how do we formulate those questions in a way that is amenable to digital testing? 

_Method group A:_ Translate questions into terms we can explore with text-corpus analysis tools.

1. What did “culture” refer to in the SSIs? —> collocates —> What words was it most closely linked to? How did those change over time? 
1. With which verbs is it most strongly linked? (Scovazzi suggests “protection and promotion” were key activities. Were they? And was the culture being protected and that being promoted the same thing?
1. Did “culture” become broader, or narrower? —> what was range of ideas to which culture was linked? Did this grow broader/narrower over time?
1. What is the nature of the linkage between “culture” and “peace” in the corpus? 
1. Can we locate turning points/moments of change. 

QUESTION: besides collocates, what else could we do here?

_Method group B:_

Can we formulate a hypothesis, determine what one would expect to find if that were the case, and then look to see if you in fact find that? For example: 

1. If Scovazzi is right, we should expect to find a strong cooccurrence of “culture” and “peace”. Do we?
1. Scovazzi suggests that the “protection and promotion” of culture were the core activities of UNESCO treaties. If so, we’d expect to see those verbs/nouns cooccur to a high degree with culture. So, with which verbs is culture in fact most strongly linked? 
1. Also, was the “culture” being protected and that being promoted the same thing? When “culture” cooccurs with “protect”, it also does so with …[?].; when “culture” cooccurs with “promote”, it also does so with …[?]


**Wouters and Vidal, "UNESCO and the Promotion of Cultural Exchange and Cultural Diversity", in Yusuf, ed., Standard-setting in UNESCO. Vol. I (2007)**
	
Key point here is to chart “the transformation of cultural diversity from a mere concept of soft law into a matter for binding legal agreement” (168). They see “cultural diversity” as having been a key theme the whole time. Was it?
1. Measure frequency of “cultural diversity” and “diversity” over time in the corpus.
1. When did “cultural diversity” grow in use? What else (in the corpus or externally) does that appear to correlate with? 
1. This article has the best, most sophisticated discussion of UNESCO’s idea of culture; argues that it is a double definition, focusing at the same time on both the “exchange of cultural creations [objects] and the protection of cultural creators [persons]” (149). Can we see/measure this doubleness in the corpus? How?
   1. Focus on “exchange” and “protection” (via collocates; or in another way?)
   1. Compare the two, and how they collocate with “culture”. 
   1. Find where culture links to objects as opposed to when it links to persons.  


**Francioni, "A Dynamic Evolution of Concept and Scope: From Cultural Property to Cultural Heritage", in Yusuf, ed., Standard-setting in UNESCO. Vol. I (2007)**

Argues that there was important shift from emphasis on Cultural Property to one on Cultural Heritage. Can we quantify/confirm/probe that claim? 

1. Measure frequency over time of phrases “Cultural Property”, “Cultural Heritage”
1. collocates of the words “Property” and “Heritage”
1. The shift from property to heritage is marked by the 1972 World Heritage Convention. So take measurements on the corpus before and after that date? 
On the other hand, F. finds “remarkable continuity in UNESCO’s attitude toward identification of what is to be considered cultural patrimony in need of safeguarding. This continuity is provided by constant reference to the idea that parts of the cultural patrimony of any nation also belong to the common heritage of humanity.” How can we track this purported continuity? 
1. trace/compare key terms: “humanity” vs “nation/national”…?



