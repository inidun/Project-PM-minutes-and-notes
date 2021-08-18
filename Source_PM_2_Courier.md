## Tematiska fel som identifierat i samband med identifieringen av artiklars början och slut i Courier (augusti 2021)

Så här såg min process ut:

* Jag tog ett slumpmässigt nummer vart femte år (totalt 14 nummer) och gick igenom samtliga artiklar som extraherats för respektive numer, totalt 140 artiklar. Jag exkluderade dock april-numret från 2003 (id: 130036) då den extraherad texten var helt oläsbar.
* Jag jämförde endast om texten i en extraherad artikel motsvarade pdf-versionen vad gäller när en artikel börjar och slutar. (OCR-brister och oordning i extraherad text har ibland noterats men inte markerats som fel. Överlag ser detta ok ut, även om det ibland finns problem med att texten på sidor med flera kolumner kastas om.
* **Träffsäkerheten för när artiklar börjar/slutar ligger på ca 70 %.** Jag tror det vore bra om vi kan komma upp till iaf 90 % träffsäkerhet om vi ska gör något med materialet.
  * Om man räknade bort mindre brister (som att det bara var en bildtext eller någon enstaka textrad på slutet av en artikel som hade klippts bort) så blev det 75 % träffsäkerhet.
  * Om man räknade bort numret från 1948 (som innehöll 14 extraherade artiklar varav 13 hade fel i hur texten hade extraherats) så hade siffran blivit 83 % träffsäkerhet. Förmodligen är träffsäkerheten låg för de första 2–4 åren pga att flera artiklar ryms på samma sida. Här finns det anledning att fundera på om det krävs någon form av manuell kurering


**Typiska fel:**

Två artiklar på samma sida där det helt saknas extraherad text från en av artikelsidorna.
* 070144_70148_a_world_wide_watch_on_the_atmosphere
* 062404_62420_unesco_art_pocket_books_a_new_venture_inart_publishing
* 062404_62421_unesco_in_retrospect_and_perspective
* 070144_70149_ceylon_s_dry_zone_pioneers_restore_prosperity_to_an_ancient_
* 073867_73875_educational_scientific_and_cultural_reconstruction
* 073867_73876_natural_sciences
* 073867_73878_achievements_in_the_social_sciences
* 073867_73879_mass_communications
* 073867_73880_echanges_culturels_arts_lettres_philosophie
* 073867_73881_u_s_commission_studies_unesco_in_a_divided_world_
* 073867_73882_the_place_of_women_in_unesco_an_indian_view
* 158378_158396_preaching_in_the_wilderness_or_banking_on_the_future_


En artikel som börjar på en sida och fortsätter längre fram i numret, men där det bara finns extraherad text från någon av dessa sidor (eller ingen text alls)
* 073867_73868_dr_huxley_s_suggestions_for_the_advance_of_world_civilizatio
* 073867_73870_macarthur_accepts_unesco_programme_in_japan
* 073867_73872_spotlight_on_arab_thought_taha_hussein_calls_unesco_common_m
* 073867_73873_a_philosopher_looks_at_arab_literature_among_world_classics
* 073867_73877_emphasis_on_education_clearing_house_function
* 074880_50644_africa_in_the_stress_of_technology
* 078234_58762_only_the_educated_are_free_
* 078438_45102_learning_to_share_the_same_globe


Minst två artiklar finns med på samma sida och där text från någon av artiklarna har extraherats och blandats ihop med den andra artikeln (vissa av exemplen nedan hänger ihop med varandra, eftersom det t ex kan vara fel ett i slutet av en artikel påverkar det den extraherade texten i följande artikel)
* 073867_73871_middle_east_cultural_liaison_office_proposed
* 074686_52496_education_training_and_society
* 074686_52513_the_sciences_and_their_applications_to_development
* 074686_52553_the_human_environment_and_terrestrial_and_marine_resources
* 074686_52554_culture_and_the_future
* 074686_52575_prejudices_intolerance_racism_apartheid
* 077050_77046_as_american_as_apple_pie_the_art_of_the_circus_spectacular
* 077050_77048_the_rubber_man
* 078438_45102_learning_to_share_the_same_globe
* 078438_45105_the_colourful_world_of_third_theatre_testing_new_forms_of_co
* 158378_158407_strange_language_let_s_say_it_s_a_whale_
* 192261_192324_conquering_the_job_market
* 192261_192326_gender_equality_a_global_public_good
* 192261_192332_mother_teresa_the_most_powerful_woman_in_the_world
* 192261_192335_manuela_sáenz_liberator_of_the_liberator


Andra fel
* 074686_52516_information_systems_and_access_to_knowledge
  * FEL: Denna artikel anges börja på sida 18 men den börjar på sida 19 (där en annan artikeln sedan börjar). Ingen text har extraherats.
* 077050_77049_a_topsy_turvy_world + 095106_187175_books_of_the_world
  * FEL: Detta är den sista artikeln i numret, och på an andra halvan av sidan ryms sådant som inte här till artikeln.
* 095106_95075_culture_first_and_last_commentary
  * FEL: Artikeln börjar i högra kanten av sidan, första halvan är text som inte har med denna artikel att göra
* 158378_158416_the_doctor_prince
  * FEL: Artikeln börjar mitt på sidan och algoritmen har inte lyckats identifiera denna första halvsida.


**Därtill: Kolla issue 130036 (2003, April) vars layout inte funkade med PDFbox, och kanske andra issues som har liknande problem**




 


## Översiktliga anteckningar från genomgång av segmenterings- och ocr-kvalitén för PDFBox, Tesseract, Ms Word Pdfplumber och Pdfminer (februari 2021)

Testet gick ut på att jämföra outputen (txt-filerna) från de olika programmen. Ingen exakt uppräkning av fel gjordes, istället identifierades mönster för när kvalitébrister kunde uppstå.

Nedan följer en höftad rangordning

**1a plats: PDFBox**
* Bra: ocr-kvaliteten är bra (kan dock inte bedöma utifrån detta test om PDFBox är bättre än Tesseract)
* Bra: kan t ex hantera ordföljd vid inledningar på artiklar där den första bokstaven är oproportionerligt större än resten av brödtexten ¬(detta misslyckas Tesseract nästan alltid med och blandar då ihop meningsordningen)
* Dåligt: det går inte att avläsa när ett stycke börjar och slutar. PDFBox verkar betrakta varje rad som ett textsegment. 

**2a plats: Tesseract (men väldigt nära delad 1a plats med PDFBox)**
* Bra: ocr-kvalitet (som PDFBox)
* Bra: markerar med ett radavstånd när ett textsegment börjar och slutar 
* Dåligt: fångar ofta ordföljden i styckena, men inte alltid (se undantag i anteckningen om PDFBox), vilket drar ner betyget

**3e plats: Ms Word**
* Bra: identifiera ofta och kan särskilja paragrafer (ord som följs utan radbrytning, dessa avgränsas med indrag  
* Bra: OCR-kvalitén förefaller vara sämre än PDFBox och Tesseract
* Dåligt: blandar ibland samman meningarna från t ex bildtexter som ligger nära varandra, men också i vissa fall meningar från två spalter (då Word läser från första översta spaltraden till andra översta spaltraden osv). Detta är en allvarlig brist

**Sistaplats: Pdfplumber & Pdfminer** – är skräp, blandar t ex ihop om ordföljder och ocr-kvalitén är delvis svajig.


**Slutsats och reflektioner:**

PDFBox och Tesseract presterar bäst segmenterings- och ocr-kvalitet. 

I båda fallen bryter bildtexter in i artiklarnas brödtext. Detta är förmodligen något som är svårt att åtgärda utan manuellt arbete, och därför något som kommer ta väldigt lång tid att åtgärda i alla artiklar i Courier. Förslagsvis gör vi inget år detta, men med konsekvensen att ordföljden i artiklarna inte alltid är korrekta (dvs när en bildtext bryter in i brödtexten). 

**Möjligen kan man tänka sig ett kurreringsprocess så här:**

Steg 1
* Kör Tesseract eller PDFBox på materialet – eller båda – och märk upp varje tidskriftsnummer med år och nummer
* Pos-tagga (Stanford?)
* Detta dataset kan sedan användas i Jupyter för: PoS-statistik, word trends, most descriminating terms… och kanske topic modeling. Co-occurrence-metoden blir lite vanskligt då ordordningen inte är helt säker, däremot skulle det möjligen gå att använda sig den textsegmentering som Tesseract producerar och då betrakta ett textblock som själva ordfönstret

Steg 2
* Utifrån körningen av Tesseract eller PDFBox (och PoS-taggningen?)
  * Tagga upp start och slut för samtliga artiklar som finns angivna i metadata-filen 
  * Taggar upp ev författare till enskilda artiklar




## Anteckningar om ”metadata-file” för Courier (januari 2021)

Jag har gjort en ganska noga genomgång av ”metadata-file” för Courier. Metadatan är överlag koherent och korrekt. Den anomalier som finns går säkerligen att rätta till manuellt. Jag har gjort detaljerade anteckningar som vi kan ha nytta av när vi ska arbeta med att få stycka upp Courier i enskilda artiklar och försedda med relevant metadata.

Efter redogörelsen följer ett kortfattat förslag på en trestegsprocess för att kurera Courier.<br /><br /><br />


**A-kolumnen: ”Record number”-** Anger ett unikt serienummer för respektive text (artikel eller tidskriftsnummer).<br /><br />

**B-kolumnen: ”Catalogue – Title”.** Anger titeln för respektive artikel/tidskriftsnummer. 
* Det språk som anges är det som anges först i E-kolumnen (”Languages”). Om det istället står t ex ”fre|eng spa rus ara por chi cat kor” i E-kolumnen anges franska som titel i B-kolumnen (”Catalogue – Title”). I D-kolumnen (”Titles in other languages”) anges sedan titeln på de översatta språken (i den ordning som anges i E-kolumnen med ”|” som avskiljare), t ex: ”Powerful women|El poder de las mujeres|Mulheres poderosas|Dones poderoses”. I nästan alla artiklar som inte har engelska som huvudspråk anges det alltid som andraspråk (50 artiklar undantagna). **Vi kan med andra ord skapa en regel som säger att när eng inte är huvudspråk ska skriptet ta den första textsträngen som slutar med ”|”**
* Det finns ett 30-tal artiklar som är editorials, vilket nästan aldrig annars listas. För konsekvensens skull skulle vi kunna ta bort dessa ur metadata-filen innan vi skrapar hem artiklar.
* I B-kolumnen anges också titlar på de enskilda tidskriftsnumren (alltså de som står listade som ”periodical issue” i H-kolumnen.<br /><br />

**C-kolumnen: ”Catalogue – Authors”.** Anger om det finns en utskriven författare till respektive artikel. Sorterat på article (7639 st) finns det 6238 artiklar (81,7 %) som har en författare, varav 4343 är unika författare (inkl sådana som anges som ”UNESCO”). 
*	Författare anges först med efternamn sedan förnamn (t ex ”Guerrero, Carolina interviewee”). Om det är flera författare på en artikel avskiljs dessa med | (t ex ”Guerrero, Carolina|Iglesias Kuntz, Lucía”). 
*	Om det är någon som blir intervjuad kan det iaf ibland stå så här: ”Markelova, Katerina **interviewer**|Dvortsevoï, Sergueï **interviewee**|Yeslyamova, Samal interviewee”. 
*	Om någon är med som fotograf kan det ibland också stå så här: ”Ferroukhi, Nadia **photographer**”, men inte alltid, i denna artikel är t ex den ena författare och den andra fotograf: ”Markelova, Katerina|Dormino, Marco”. 
*	Ibland kan det även stå så här: ”Patou-Mathis, Marylène **author**”. 
*	Ibland kan det bli fel då det är en intervjuartikel och det blir intervjupersonen som står som författare tillsammans med organisationen som intervjuade, som här: ”Gargallo, Ligia|UNESCO Office Santiago and Regional Bureau for Education in Latin America and the Caribbean”<br /><br />

**D-kolumnen: ”Titles in other languages”.** Anger de andra språk som artikeln har översatts till. Det totalt rör sig om 83 poster som inte har engelska titlar som första andraspråk.
* Om det första språket som anges i E-kolumnen ”Languages” är engelska (”eng”) är det andra språk som anges i ”Titles in other languages” (t ex franska och spanska). Om det är ett annat huvudspråk som anges i ”Language” (t ex ”fre|eng spa rus ara por chi cat kor”) är det i regel i den språkordningen som artikeltitlarna ges, med ”|” som avskiljare: 
  * "Burkina Faso: addicted to radio|Burkina Faso, un país adicto a la radio|Burkina Faso: viciados em rádio|Burkina Faso, un país addicte a la ràdio”
*	I vissa enstaka fall kommer den engelska titeln före i ordningen, t ex i följande fall ”fre|spa rus ara eng chi epo” gavs först en spansk titel följt av en engelsk titel (och hoppade således över ryska och arabiska, som för övrigt inte fanns med bland titlarna i andra språk).  <br /><br />

**E-kolumnen: ”Languages”.** Ange vilka språk som artiklarna gavs ut på. Huvudspråket anges först och om det finns översatt anges det efter ett ”|”, t ex ”eng|ara chi fre por rus spa epo srd”.
* Nästan alla finns i en engelsk version, men några enstaka gavs också ut bara på andra språk: 
  * Tex det enda numret 2012, och aprilnumret 2007.
  * 2007:3 (ett nummer om museum) som bara finns på franska, spanska och ryska. 
  * En artikel i numret 1956:5 (Le Courrier de l'UNESCO: une fenêtre ouverte sur le monde IX, 5 p. 29 78152 fre) som handlar om skilda saker i den engelska versionen (om London och dialekter) och i den franska (om en skola och dess elever (?)). 
  * Ett sista (?) exempel är från 1956:5 på sida 10 där det finns en liten del av artikeln (en slags faktaruta) som bara finns på franska (möjligen för att det fanns utrymme att fylla ut sidan efter översättningen). 
* Följande poster har felaktigt angivet att artiklarna bara finns på andra språk än engelska:
  * El Correo de la UNESCO I, 7 p. 3 73809 spa
  * El Correo de la UNESCO I, 8 p. 8 73829 spa
  * El Correo de la UNESCO II, 7 p. 9 74029 spa
  * El Correo de la UNESCO III, 4 p. 11, illus. 81370 spa
  * El Correo de la UNESCO III, 6/7 p. 13, illus., port. 81475 spa
  * El Correo de la UNESCO III, 9 p. 2, illus. 81564 spa
  * El Correo de la UNESCO: una ventana abierta sobre el mundo IX, 5 p. 29 78152 spa <br /><br />

**F-kolumnen: ”Series”.** Anger de olika Courier-numren (volym och nummer), alltså inte enskilda artiklar, angivet i olika språk avgränsade med ”|”, t ex: 
* ”The UNESCO Courier: a window open on the world VIII, 10|Le Courrier de l'UNESCO: une fenêtre ouverte sur le monde VIII, 10|El Correo de la UNESCO: una ventana abierta sobre el mundo VIII, 10)”. Dock anges detta på lite olika sätt, för mer info se I-Kolumnen. 
* Här anges inte id-numret för publikationen, vilket det dock gör i I-kolumnen. <br /><br />

**G-kolumnen: ”Catalogue – Subjects”.** Unesco:s/Couriers keywords för vad varje artikel och nummer handlar om, enligt följande system: 
* ”Transport engineering|Railway transport|International trade|Mexico|Development projects|Financial aid|World Bank” <br /><br />

 **H-kolumnen: ”Document type”.** Anger om det är en 1) enskild artikel (article) eller 2) ett tidskriftsnummer (periodical issue) – **vi kan därför ignorera alla ”periodical issue”** <br /><br /> 

**I-kolumnen: ”Host item”.** Anger bl a information om varje artikels volym, tidskriftsnummer, sidnummer och id-numret för respektive tidskriftsnummer. Detta görs upprepande för respektive språk som artikeln är översatt till (separerat med ”|”). Nedan är ett exempel från Courier 1983 no 3: 
*	”The UNESCO Courier: a window open on the world **XXXVI, 3 p. 4-7**, illus. **74689** eng|(UNESCO courier (Arabic)) XXXVI, 3 p. 4-7, illus. 74689 ara|(The UNESCO Courier (Chinese)) XXXVI, 3 p. 4-7, illus. 74689 chi|Le Courrier de l'UNESCO: une fenêtre ouverte sur le monde XXXVI, 3 p. 4-7, illus. 74689 fre|Kur'er Yunesko XXXVI, 3 p. 4-7, illus. 74689 rus|El Correo de la UNESCO: una ventana abierta sobre el mundo XXXVI, 3 p. 4-7, illus. 74689 spa”. **Här utgör XXXVI = volymnummer. 3 = tidskriftsnummer. p. 4-7 = sidnummer. 74689 = id-numret för tidskriftsnumret.**
* **Angående volym- och tidskriftsnummer** (liksom namnet på tidskriften) finns det finns variation för hur detta skrivs ut:
  * The UNESCO Courier **1948–1954** enligt principen: “The UNESCO courier **VII, 3** p. 14-15, illus. 69904 eng”. Här anges volymnumret med romerska siffror och tidskriftsnumret med vanliga siffror.
  * The UNESCO Courier: a window open on the world **1955¬–1995** anges enligt principen: “The UNESCO Courier: a window open on the world **VIII, 1** p. 5-7, illus. 68948 eng”. Här anges volymnumret med romerska siffror och tidskriftsnumret med vanliga siffror. 
  * The UNESCO courier: a window open on the world **1996–1998** (fram till 1998:9) enligt principen: “The UNESCO courier: a window open on the world **49, 10** p. 50 104412 eng”. Här anges både volym- och tidskriftsnumret med vanliga siffror.
  * The UNESCO courier **1998–2001** (från och med skrivs volymnumret med vanliga siffror (dvs nr 51–54) enligt principen: ”The UNESCO courier **52, 2** p. 33-36, illus. 114969 eng”. Här anges både volym- och tidskriftsnumret med vanliga siffror.
  * The New Courier **2002–2003** ger bara ut 2 nummer per år. I metadata-filen anges dessa nummer som 0–3, dvs inte som 1–2 för varje år/volym. T ex: ”The New courier **2** p. 22-23, illus. 130036 eng”. Volymnumret anges inte i Kolumn-I.
  * The New Courier **2004** ger ut 4 nummer och här anges nummer ibland med månad (”Dec.” och ”October”), en gång inte alls (april-numret) och fjärde gången som ”Special issue”. T ex: ”The New courier **Dec. 2004** p. 10-12, illus. 138446 eng”. Volymnumret anges inte i Kolumn-I.
  * The New Courier **2005** ger ut 2 nummer som inte numreras i Kolumn-I (april och november enligt Kolumn-J). T ex: ”The New courier p. 10 142021 eng”. Volymnumret anges inte heller i Kolumn-I. 
The UNESCO courier **2006** har 7 nummer som anges enligt principen ”July-Aug. 2006” eller ”June 2006” i Kolumn-I. T ex: ”The UNESCO courier **Dec. 2006** p. 10-11, illus. 191575 eng”. Volymnumret anges inte i Kolumn-I. 
  * The UNESCO courier **2007–2009** har mellan 9–13 nummer per år och ange ofta så här: ”The UNESCO courier 8 p. 17-19, illus. 185864 eng”, men ibland så här: “The UNESCO courier **Special edition** p. 11-12, illus. 185818 eng” eller ”The UNESCO courier **Special issue** p. 14, 16-18, illus. 185958 eng”. Volymnumret anges inte i Kolumn-I.
The UNESCO courier **2010** har 1 nummer som anges så här: “The UNESCO courier **Sept. 2010** p. 11-12, illus. 189496 eng”. Volymnumret anges inte i Kolumn-I.
  * The UNESCO courier **2011** har 5 nummer varav 3 anges enligt principen: “The UNESCO courier **64, 4** p. 25-26, illus. 213061 eng”. Ett annat nummer anges istället enligt denna princip: ”The UNESCO courier **Jan.-Mar. 2011** p. 11-16, illus. 190645 eng”. Ett tredje nummer (som är ett specialnummer) anges enligt denna princip: ”The UNESCO courier **Special issue, Mar. 2011** p. 10-12, illus. 191443 eng”. Här anges volymnumret också i Kolumn-I.
  * **2012**-numret gavs bara ut på franska och då enligt principen: ”Le Courrier de l'UNESCO Numéro spécial, avril 2012 p. 10-11, illus. 216066 fre”.
 	* Uppehåll för Courier **2013–2016**.
  * The UNESCO courier **2017–2019** ger ut 4 nummer per år enligt principen: “The UNESCO courier **1** p. 16-17, illustration 366654 eng”. Volymnumret anges inte i Kolumn-I.
* **Angående sidnummer** står det oftast ”p.”, men ibland också ”pages”, ”page”. Ibland är det ”,” efter angivet sidnummer, om det är en artikel på olika spridda sidor kan det stå ”p. 16, p. 17” eller ”p. 7, 8”, om det finns med en illustration kan det stå ”p. 8, illus.”, vid någon enstaka gång kan det se ut så här: ”p.23-24, 33, maps” (alltså inget mellanslag mellan p. och sidnumret). 
* **Angående id-numret** för tidskriftsnumret anges detta alltid efter sidnumret. Id-numret är alltså samma för varje artikel som ingår i respektive tidskriftsnummer. **Id-numret är viktigt då det är det numret som varje nummer av Courier döps till vid nerladdning!**
* **OBS! UNESCO Monitor** gavs ut i 3 nummer under 1947 innan Courier lanseras och tar över. I Kolumn-I finns bara en artikel registrerad för Monitor. De tre tidskriftsnumren finns istället registrerade i Kolumn-B som ”UNESCO monitor, vol. 1, no. 1”, ”UNESCO monitor, vol. 1, no. 2” och ”UNESCO monitor, vol. 1, no. 3”. **Antingen exkluderas dessa två nummer från analysen eller så kurerar vi dem själva för hand (de saknar nämligen metadata för artikeltitlar, sidnummer, författare etc).** <br /><br />

**J-kolumnen: ”Catalogue - Publication date”.** År finns för alla angivna artiklar. Hur detta skrivs skiftar lite, men det börjar alltid med året med fyra siffertecken (t ex 1965). Olika exempel: ”1983|May 1983”, ” 2018|Jan. - Mar. 2018”, ”1950”. **Det är med andra ord lätt att extrahera ut årtalet för respektive artikel och kan användas istället för volymnummer!** <br /><br />

**K-kolumnen: ”Notes”.** Diverse anteckningar till artiklar och tidskriftsnummer. Omkring 2200 poster är försedda med anteckningar. <br /><br /><br />



**Förslag på process för att extrahera enskilda artiklar med metadata**
1.	Ladda ner varje nummer av Courier och förse dem med metadata för volym/år, tidskriftsnummer och id-nummer (se Kolumn-I och Kolumn-J). Från omkring år 2000 kommer det finnas större behov av manuell påläggning. Detta steg bör vara förhållandevis enkelt att utföra.
2.	Stycka upp varje nummer av Courier efter artiklar baserat på sidhänvisning (se Kolumn-I). Detta kommer kräva en hel del manuell påläggning för att kontrollera att rätt text hör till rätt artikel. Detta arbete bör därför göras stegvis (kanske för varje femårsperiod) för att lära sig av misstag och förbättra processen.
3.	Förse varje artikel/textfil med ytterligare metadata för artikeltitel (Kolumn-B alt. Kolumn-D), författare (Kolumn-C) och möjligen även keywords (Kolumn-G). När väl steg 2 är utfört är bör det vara relativt enkelt att förse varje enskild artikel med metadata från respektive kolumn. <br /><br /><br />





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
