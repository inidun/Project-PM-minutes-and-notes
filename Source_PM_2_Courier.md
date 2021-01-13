## Anteckningar om ”metadata-file” för Courier (januari 2021)

Jag har gjort en ganska noga genomgång av ”metadata-file” för Courier. Metadatan är överlag koherent och korrekt. Den anomalier som finns går säkerligen att rätta till manuellt. Jag har gjort detaljerade anteckningar som vi kan ha nytta av när vi ska arbeta med att få stycka upp Courier i enskilda artiklar och försedda med relevant metadata.

Efter redogörelsen följer ett kortfattat förslag på en trestegsprocess för att kurera Courier. 


## Anteckningar om ”metadata-file” för Courier

**A-kolumnen: ”Record number”-** Anger ett unikt serienummer för respektive text (artikel eller tidskriftsnummer).
<br/>
<br/>
**B-kolumnen: ”Catalogue – Title”.** Anger titeln för respektive artikel/tidskriftsnummer. 
* Det språk som anges är det som anges först i E-kolumnen (”Languages”). Om det istället står t ex ”fre|eng spa rus ara por chi cat kor” i E-kolumnen anges franska som titel i B-kolumnen (”Catalogue – Title”). I D-kolumnen (”Titles in other languages”) anges sedan titeln på de översatta språken (i den ordning som anges i E-kolumnen med ”|” som avskiljare), t ex: ”Powerful women|El poder de las mujeres|Mulheres poderosas|Dones poderoses”. I nästan alla artiklar som inte har engelska som huvudspråk anges det alltid som andraspråk (50 artiklar undantagna). Vi kan med andra ord skapa en regel som säger att när eng inte är huvudspråk ska skriptet ta den första textsträngen som slutar med ”|”
* Det finns ett 30-tal artiklar som är editorials, vilket nästan aldrig annars listas. För konsekvensens skull skulle vi kunna ta bort dessa ur metadata-filen innan vi skrapar hem artiklar.
* I B-kolumnen anges också titlar på de enskilda tidskriftsnumren (alltså de som står listade som ”periodical issue” i H-kolumnen.
<br/>
<br/>
**C-kolumnen: ”Catalogue – Authors”.** Anger om det finns en utskriven författare till respektive artikel. Sorterat på article (7639 st) finns det 6238 artiklar (81,7 %) som har en författare, varav 4343 är unika författare (inkl sådana som anges som ”UNESCO”). 
*	Författare anges först med efternamn sedan förnamn (t ex ”Guerrero, Carolina interviewee”). Om det är flera författare på en artikel avskiljs dessa med | (t ex ”Guerrero, Carolina|Iglesias Kuntz, Lucía”). 
*	Om det är någon som blir intervjuad kan det iaf ibland stå så här: ”Markelova, Katerina interviewer|Dvortsevoï, Sergueï interviewee|Yeslyamova, Samal interviewee”. 
*	Om någon är med som fotograf kan det ibland också stå så här: ”Ferroukhi, Nadia photographer”, men inte alltid, i denna artikel är t ex den ena författare och den andra fotograf: ”Markelova, Katerina|Dormino, Marco”. 
*	Ibland kan det även stå så här: ”Patou-Mathis, Marylène author”. 
*	Ibland kan det bli fel då det är en intervjuartikel och det blir intervjupersonen som står som författare tillsammans med organisationen som intervjuade, som här: ”Gargallo, Ligia|UNESCO Office Santiago and Regional Bureau for Education in Latin America and the Caribbean”

**D-kolumnen: ”Titles in other languages”.** Anger de andra språk som artikeln har översatts till. Det totalt rör sig om 83 poster som inte har engelska titlar som första andraspråk.
* Om det första språket som anges i E-kolumnen ”Languages” är engelska (”eng”) är det andra språk som anges i ”Titles in other languages” (t ex franska och spanska). Om det är ett annat huvudspråk som anges i ”Language” (t ex ”fre|eng spa rus ara por chi cat kor”) är det i regel i den språkordningen som artikeltitlarna ges, med ”|” som avskiljare: 
  * "Burkina Faso: addicted to radio|Burkina Faso, un país adicto a la radio|Burkina Faso: viciados em rádio|Burkina Faso, un país addicte a la ràdio”
*	I vissa enstaka fall kommer den engelska titeln före i ordningen, t ex i följande fall ”fre|spa rus ara eng chi epo” gavs först en spansk titel följt av en engelsk titel (och hoppade således över ryska och arabiska, som för övrigt inte fanns med bland titlarna i andra språk).  
<br/>
<br/>
**E-kolumnen: ”Languages”.** Ange vilka språk som artiklarna gavs ut på. Huvudspråket anges först och om det finns översatt anges det efter ett ”|”, t ex ”eng|ara chi fre por rus spa epo srd”.
*	Item 1 Nästan alla finns i en engelsk version, men några enstaka gavs också ut bara på andra språk: 
  * Item 1a Tex det enda numret 2012, och aprilnumret 2007. 
  * Item 1b 2007:3 (ett nummer om museum) som bara finns på franska, spanska och ryska. 
  * Item 1c En artikel i numret 1956:5 (Le Courrier de l'UNESCO: une fenêtre ouverte sur le monde IX, 5 p. 29 78152 fre) som handlar om skilda saker i den engelska versionen (om London och dialekter) och i den franska (om en skola och dess elever (?)). 
  *	Item 1d Ett sista (?) exempel är från 1956:5 på sida 10 där det finns en liten del av artikeln (en slags faktaruta) som bara finns på franska (möjligen för att det fanns utrymme att fylla ut sidan efter översättningen). 
o	Följande poster har felaktigt angivet att artiklarna bara finns på andra språk än engelska:
	El Correo de la UNESCO I, 7 p. 3 73809 spa
	El Correo de la UNESCO I, 8 p. 8 73829 spa
	El Correo de la UNESCO II, 7 p. 9 74029 spa
	El Correo de la UNESCO III, 4 p. 11, illus. 81370 spa
	El Correo de la UNESCO III, 6/7 p. 13, illus., port. 81475 spa
	El Correo de la UNESCO III, 9 p. 2, illus. 81564 spa
	El Correo de la UNESCO: una ventana abierta sobre el mundo IX, 5 p. 29 78152 spa
<br/>
<br/>
**F-kolumnen: ”Series”.** Anger de olika Courier-numren (volym och nummer), alltså inte enskilda artiklar, angivet i olika språk avgränsade med ”|”, t ex: 
o	”The UNESCO Courier: a window open on the world VIII, 10|Le Courrier de l'UNESCO: une fenêtre ouverte sur le monde VIII, 10|El Correo de la UNESCO: una ventana abierta sobre el mundo VIII, 10)”. Dock anges detta på lite olika sätt, för mer info se I-Kolumnen. 
o	Här anges inte id-numret för publikationen, vilket det dock gör i I-kolumnen. 
<br/>
<br/>
**G-kolumnen: ”Catalogue – Subjects”.** Unesco:s/Couriers keywords för vad varje artikel och nummer handlar om, enligt följande system: 
* ”Transport engineering|Railway transport|International trade|Mexico|Development projects|Financial aid|World Bank”
 <br/>
 <br/>
 **H-kolumnen: ”Document type”.** Anger om det är en 1) enskild artikel (article) eller 2) ett tidskriftsnummer (periodical issue) – vi kan därför ignorera alla ”periodical issue”
<br/>
<br/>
**I-kolumnen: ”Host item”.** Anger bl a information om varje artikels volym, tidskriftsnummer, sidnummer och id-numret för respektive tidskriftsnummer. Detta görs upprepande för respektive språk som artikeln är översatt till (separerat med ”|”). Nedan är ett exempel från Courier 1983 no 3: 
*	”The UNESCO Courier: a window open on the world XXXVI, 3 p. 4-7, illus. 74689 eng|(UNESCO courier (Arabic)) XXXVI, 3 p. 4-7, illus. 74689 ara|(The UNESCO Courier (Chinese)) XXXVI, 3 p. 4-7, illus. 74689 chi|Le Courrier de l'UNESCO: une fenêtre ouverte sur le monde XXXVI, 3 p. 4-7, illus. 74689 fre|Kur'er Yunesko XXXVI, 3 p. 4-7, illus. 74689 rus|El Correo de la UNESCO: una ventana abierta sobre el mundo XXXVI, 3 p. 4-7, illus. 74689 spa”. Här utgör XXXVI = volymnummer. 3 = tidskriftsnummer. p. 4-7 = sidnummer. 74689 = id-numret för tidskriftsnumret.
* Item 1	Angående volym- och tidskriftsnummer (liksom namnet på tidskriften) finns det finns variation för hur detta skrivs ut:
  * The UNESCO Courier 1948–1954 enligt principen: “The UNESCO courier VII, 3 p. 14-15, illus. 69904 eng”. Här anges volymnumret med romerska siffror och tidskriftsnumret med vanliga siffror.
  * The UNESCO Courier: a window open on the world 1955¬–1995 anges enligt principen: “The UNESCO Courier: a window open on the world VIII, 1 p. 5-7, illus. 68948 eng”. Här anges volymnumret med romerska siffror och tidskriftsnumret med vanliga siffror. 
  * The UNESCO courier: a window open on the world 1996–1998 (fram till 1998:9) enligt principen: “The UNESCO courier: a window open on the world 49, 10 p. 50 104412 eng”. Här anges både volym- och tidskriftsnumret med vanliga siffror.
  * The UNESCO courier 1998–2001 (från och med skrivs volymnumret med vanliga siffror (dvs nr 51–54) enligt principen: ”The UNESCO courier 52, 2 p. 33-36, illus. 114969 eng”. Här anges både volym- och tidskriftsnumret med vanliga siffror.
  * The New Courier 2002–2003 ger bara ut 2 nummer per år. I metadata-filen anges dessa nummer som 0–3, dvs inte som 1–2 för varje år/volym. T ex: ”The New courier 2 p. 22-23, illus. 130036 eng”. Volymnumret anges inte i Kolumn-I.
  * The New Courier 2004 ger ut 4 nummer och här anges nummer ibland med månad (”Dec.” och ”October”), en gång inte alls (april-numret) och fjärde gången som ”Special issue”. T ex: ”The New courier Dec. 2004 p. 10-12, illus. 138446 eng”. Volymnumret anges inte i Kolumn-I.
  * The New Courier 2005 ger ut 2 nummer som inte numreras i Kolumn-I (april och november enligt Kolumn-J). T ex: ”The New courier p. 10 142021 eng”. Volymnumret anges inte heller i Kolumn-I. 
The UNESCO courier 2006 har 7 nummer som anges enligt principen ”July-Aug. 2006” eller ”June 2006” i Kolumn-I. T ex: ”The UNESCO courier Dec. 2006 p. 10-11, illus. 191575 eng”. Volymnumret anges inte i Kolumn-I. 
  * The UNESCO courier 2007–2009 har mellan 9–13 nummer per år och ange ofta så här: ”The UNESCO courier 8 p. 17-19, illus. 185864 eng”, men ibland så här: “The UNESCO courier Special edition p. 11-12, illus. 185818 eng” eller ”The UNESCO courier Special issue p. 14, 16-18, illus. 185958 eng”. Volymnumret anges inte i Kolumn-I.
The UNESCO courier 2010 har 1 nummer som anges så här: “The UNESCO courier Sept. 2010 p. 11-12, illus. 189496 eng”. Volymnumret anges inte i Kolumn-I.
  * The UNESCO courier 2011 har 5 nummer varav 3 anges enligt principen: “The UNESCO courier 64, 4 p. 25-26, illus. 213061 eng”. Ett annat nummer anges istället enligt denna princip: ”The UNESCO courier Jan.-Mar. 2011 p. 11-16, illus. 190645 eng”. Ett tredje nummer (som är ett specialnummer) anges enligt denna princip: ”The UNESCO courier Special issue, Mar. 2011 p. 10-12, illus. 191443 eng”. Här anges volymnumret också i Kolumn-I.
  * 2012-numret gavs bara ut på franska och då enligt principen: ”Le Courrier de l'UNESCO Numéro spécial, avril 2012 p. 10-11, illus. 216066 fre”.
 	* Uppehåll för Courier 2013–2016.
  * The UNESCO courier 2017–2019 ger ut 4 nummer per år enligt principen: “The UNESCO courier 1 p. 16-17, illustration 366654 eng”. Volymnumret anges inte i Kolumn-I.
o	Angående sidnummer står det oftast ”p.”, men ibland också ”pages”, ”page”. Ibland är det ”,” efter angivet sidnummer, om det är en artikel på olika spridda sidor kan det stå ”p. 16, p. 17” eller ”p. 7, 8”, om det finns med en illustration kan det stå ”p. 8, illus.”, vid någon enstaka gång kan det se ut så här: ”p.23-24, 33, maps” (alltså inget mellanslag mellan p. och sidnumret). 
o	Angående id-numret för tidskriftsnumret anges detta alltid efter sidnumret. Id-numret är alltså samma för varje artikel som ingår i respektive tidskriftsnummer. Id-numret är viktigt då det är det numret som varje nummer av Courier döps till vid nerladdning!
o	OBS! UNESCO Monitor gavs ut i 3 nummer under 1947 innan Courier lanseras och tar över. I Kolumn-I finns bara en artikel registrerad för Monitor. De tre tidskriftsnumren finns istället registrerade i Kolumn-B som ”UNESCO monitor, vol. 1, no. 1”, ”UNESCO monitor, vol. 1, no. 2” och ”UNESCO monitor, vol. 1, no. 3”. Antingen exkluderas dessa två nummer från analysen eller så kurerar vi dem själva för hand (de saknar nämligen metadata för artikeltitlar, sidnummer, författare etc).
<br/>
<br/>
**J-kolumnen: ”Catalogue - Publication date”.** År finns för alla angivna artiklar. Hur detta skrivs skiftar lite, men det börjar alltid med året med fyra siffertecken (t ex 1965). Olika exempel: ”1983|May 1983”, ” 2018|Jan. - Mar. 2018”, ”1950”. Det är med andra ord lätt att extrahera ut årtalet för respektive artikel och kan användas istället för volymnummer!
<br/>
<br/>
**K-kolumnen: ”Notes”.** Diverse anteckningar till artiklar och tidskriftsnummer. Omkring 2200 poster är försedda med anteckningar.
<br/>
<br/>
<br/>
Förslag på process för att extrahera enskilda artiklar med metadata
1.	Ladda ner varje nummer av Courier och förse dem med metadata för volym/år, tidskriftsnummer och id-nummer (se Kolumn-I och Kolumn-J). Från omkring år 2000 kommer det finnas större behov av manuell påläggning. Detta steg bör vara förhållandevis enkelt att utföra.
2.	Stycka upp varje nummer av Courier efter artiklar baserat på sidhänvisning (se Kolumn-I). Detta kommer kräva en hel del manuell påläggning för att kontrollera att rätt text hör till rätt artikel. Detta arbete bör därför göras stegvis (kanske för varje femårsperiod) för att lära sig av misstag och förbättra processen.
3.	Förse varje artikel/textfil med ytterligare metadata för artikeltitel (Kolumn-B alt. Kolumn-D), författare (Kolumn-C) och möjligen även keywords (Kolumn-G). När väl steg 2 är utfört är bör det vara relativt enkelt att förse varje enskild artikel med metadata från respektive kolumn.





## Anteckningar om Courier (augusti 2020) 


__Kortfattad översikt__

Jag har gjort en översiktlig genomgång av Courier utifrån följande två sidor:
- https://unesdoc.unesco.org/ark:/48223/pf0000108360
- https://en.unesco.org/courier/archives

Nästan alla nummer av tidskriften finns digitalt på hemsidan (december-numret 2001 förefaller inte finnas digitalt).

För projektets undersökningsperiod löper tidskriften på engelska mellan 1948 och 2011 (sen gör den ett uppehåll till 2017). Det enda numret från 2012 gavs bara ut på franska (om jazz).

Antalet nummer ligger under perioden 1948–2001 relativt stabilt på 10–12 nummer/år, mellan 2002–2006 sjunker utgivningen till 2–7 nummer/år.

Antalet sidor ökar successivt över perioden, från omkring 15 till 50–80 (även om åren 2006–2011 innebär en viss minskning i omfång). 


__Frågor att diskutera__

Hur är Courier digitaliserad?
* Jag har inte gjort någon systematisk undersökning av ocr-kvalité, men den förefaller vara god. Men: bör vi göra en sådan systematisk undersökning och i så fall hur? Detta är en fråga även gäller de andra två materialkategorierna.
* Fråga till Roger och Andreas: Finns det en underliggande digital struktur som märkt upp hela artiklar eller textblock?


Hur ska vi extraheras texten i Courier?
* Fråga till Roger och Andreas: på vilka olika sätt kan vi få ut den underliggande texten? 
* Vilken metod är sedan bäst för att kurera materialet på det sätt vi vill? Ska det ske genom en delvis automatiserad process med manuell påläggning? Eller är det resursmässigt rimligt att göra det helt manuellt (på ca 656 nummer)


Hur ska vi dela upp Courier?
* Idealet vore att extrahera hela artiklar. Men med möjlighet att välja bort icke-redaktionellt material (t ex sidhuvud, innehållsförteckningar, referenslistor, tabeller, förteckningar, kalendrar/listor, annonser, redaktionsinformation, hur man prenumererar etc). Detta medför dock vissa potentiella problem:
* En artikel börja på sida 1 och sedan fortsätta på sida 6 (gäller främst i början av tidsperioden).
* Det finns en hel del bildtexter – hur hanteras dessa i relation till artiklar/textblock?
* Alternativt att dela in tidskriften efter ev textblock som skapats under digitaliseringen. 
* Oavsett: extraherade textenheter ska förses med år, nummer, samt ett nummer-id för vilket textblock/artikel som det rör sig om


Att göra:
* Identifiera hur den underliggande textstrukturen är uppbyggd i pdf:erna –  gör nedslag i olika delar av perioden 1948–2011
* Identifiera olika alternativ för art extrahera text ur pdf:erna
* Förse alla nerladdade Courier-nummer med år och serienummer (en siffra efter numret alternativ ”oi” som kan stå för special issue eller dylikt (därav oi, other issue). T ex 1948_10, 1948_oi
* Ocr-test? 
