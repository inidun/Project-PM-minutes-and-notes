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


