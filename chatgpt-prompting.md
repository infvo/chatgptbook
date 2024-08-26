# ChatGPT prompting

* [presentatie](https://docs.google.com/presentation/d/1IOA1N8DRYeyUONZHTiVhqAdEIfJHPmXPmkNeQYRCnns/edit?usp=sharing)

Dit is een samenvatting van de belangrijkste regels voor ChatGPT prompting.
Prompting is geen exacte wetenschap: je moet voor je eigen situatie proberen wat het beste werkt.
Door experimenteren bouw je daarvoor een intuïtie op: volgens Ethan Mollick krijg je dit na ca. 10 uur experimenteren in de vingers.
(Maar, dat kan van geval tot geval verschillen.) Geef dus niet te snel op, maar probeer het eens op een andere manier.

:::{admonition} ChatGPT is geen zoekmachine!
:class: warning
Als je naar een bepaald feit zoekt, gebruik dan een zoekmachine zoals Google, Bing, of DuckDuckGo; of de AI-zoekmachine [Perplexity[(https://perplexity.ai). Ga na welk van de gevonden antwoorden het best bij je vraag past. En controleer de betrouwbaarheid van je bronnen.

Je kunt ChatGPT wel vragen om voor bepaalde zaken het web te raadplegen. Vraag in dat geval ChatGPT ook om een oordeel te geven over de betrouwbaarheid van de bronnen.
:::

* Gebruik voor een nieuwe vraag een nieuwe chat, zonder voorgeschiedenis.
* Zorg dat je *profiel* past bij de vraag(en) die je nu stelt.d

## Onderdelen van een gestructureerde prompt

Hoewel de AI (ChatGPT) geen persoon is, helpt het om te denken en te formuleren alsof je met een persoon te maken hebt: een assistent die je graag terwille wil zijn, maar die niet aan een half woord genoeg heeft.

Je kunt een prompt vergelijken met een opdracht voor een leerling: als je duidelijk en specifiek bent, en voldoende informatie (details) geeft, krijg je een beter resultaat.

- **Persona (Rol)**
    - welke rol heeft de AI? welke rol heeft de gebruiker?
- **Context**
    - wat is het *doel* van de gebruiker? in welke *context*? voor welke *doelgroep*?
- **Taak**
    - wat moet de AI voor jou doen in deze context?
- **Formaat (van het resultaat)**
    - hoe moet het resultaat eruit zien? voorbeelden? taalgebruik?

### Voorbeeld:

**Maken van een lesplan:**

```markdown
**Persona**: ik ben docent informatica aan een VO school. 
Jij (AI) bent expert in de didactiek van programmeren in Python.

**Context**: ik geef les in informatica aan 4 HAVO; 
ze moeten leren programmeren in Python. 
Het volgende onderwerp is *variabelen*. 
De leerlingen kennen de basis-syntax van Python.  

**Taak**: maak voor mij een lesplan voor een les van 45 minuten, 
waarin leerlingen het concept "variabele" in Python leren.

**Format**: geef dit plan puntsgewijs weer, 
met een planning voor de tijd van de verschillende onderdelen.
```

Mogelijke vervolgvragen (in dezelfde chat):

- geef een uitleg van het begrip "variabele" die ik bij de inleiding kan gebruiken, met 5 voorbeelden. Denk hierbij aan de doelgroep: 4 HAVO.
- geef 5 toetsvragen om te controleren of de leerlingen het begrepen hebben
- wat zijn mogelijke misconcepties betreffende het begrip "variabele"
- geef 5 toetsvragen om deze misconcepties te detecteren.


**Opmerking.** Je hoeft die verschillende onderdelen niet altijd zo expliciet te benoemen, maar het helpt jezelf om je eigen prompts goed te structureren en te begrijpen.

**Voorbeeld 2**

```markdown
**Persona**: ik ben een docent aan de VO-lerarenopleiding van de UvA; jij (AI) bent een expert in AI en de didactiek daarvan.

**Context**: ik moet docenten uitleggen wat AI is en waarom dit belangrijk is voor VO-docenten

**Taak**: geef een inleiding voor de eerste les over AI in het onderwijs

**Formaat**: geef deze inleiding als punten voor powerpoint slides, met per slide uitgebreide spreker-aantekeningen.
```

Mogelijke vervolgvragen:
- maak een powerpoint-presentatie voor deze slides;
- maak een illustratie voor een bepaalde slide
- pas dit aan met als doelgroep leerlingen in 4-HAVO (of 2-VMBO).

**Voorbeeld 3**

```markdown
**Persona**: ik ben docent in het VO; ik geef het vak [MIJN VAK]

**Context**: ik moet het concept [CONCEPT] uitleggen aan [MIJN KLAS] leerlingen

**Taak**: geef een uitleg van dit concept die ik in de les kan gebruiken,

**Formaat**: gebruik maximaal 200 woorden voor de uitleg van het concept.

```

Mogelijke vervolgvraag:

- pas deze uitleg aan zoals deze in Sesamstraat gegeven zou worden
- geef 5 voorbeelden van dit concept; wees daarbij zo creatief mogelijk; gebruik enthousiaste taal.
- geef 5 multiple-choice toetsvragen waarmee leerlingen hun begrip van het concept kunnen testen

### Context

De context (prompt) kan in een aantal gevallen heel uitgebreid zijn: je kunt daarin ook documenten opnemen, zoals een hoofdstuk uit een lesbooek, plaatjes, of zelfs video's.
Eén van de recente ontwikkelingen van LLMs zoals ChatGPT is dat deze een veel grotere context kunnen verwerken zonder het spoor bijster te raken. De maximale context-lengte van Gemini 1.5 Pro momenteel is 1 miljoen tokens (ca. 750.000 woorden, 1500 pagina's).

*Opmerking.* Hier wordt gesproken over "context length" wordt eigenlijk de hele prompt bedoeld; maar omdat het context-gedeelte meestal veruit het grootst is, heet dit *context length*.

## Extra informatie

Je kunt nog de volgende informatie toevoegen:

* **Stappen** (Chain of Thought, CoT)
    - als je de AI vraagt om de taak in stappen uit te voeren, krijg je soms een (veel) beter resultaat. Dit gelt bijvoorbeeld bij het uitwerken van wiskundige vraagstukken.
    - je kunt vragen om deze stappen in de uitwerking op te nemen;
    - soms is het handig om zelf de stappen aan te geven, maar dat is meestal niet nodig.
    - (dit is als bij een leerling: "geef niet zomaar een antwoord, maar denk eerst na welke stappen je nodig hebt")
* **Zelfkritiek**
    - vraag de AI om het resultaat kritisch te bekijken, en daarna te verbeteren.
    - (een aanpak die soms bij leerlingen ook werkt)
* **Laten vragen (of zoeken) naar extra informatie**
    - zeg tegen de AI dat deze als het nodig is de gebruiker om extra informatie vraagt
    - variant: zoek feiten op via het web, en geef een oordeel over de betrouwbaarheid van de bron(nen)
* **Aansporen**
    - soms zegt de AI dat deze een taak niet kan uitvoeren, terwijl je wel verwacht dat dit kan: het kan dan helpen om de AI aan te moedigen ("je kunt het!" - alweer, net als bij een leerling)
* **Creatief of feitelijk**
    - wil je een creatief resultaat, of juist erg feitelijk/waarschijnlijk: geef dat aan. ("temperatuur": 0 is feitelijk, 1 (of 2) is creatief.
 
### Voorbeelden

* Chain of Thought

```markdown
De kantine had 23 appels. Ze gebruikten 20 voor het maken van de lunch, 
en kochten er nog 6 appels bij. 
Hoeveel appels heeft de kantine nu? 
Los dit stapsgewijs op.
```

## Chat: bijsturen van het resultaat

Het resultaat na de prompt is niet altijd precies wat je bedoelt. In de vervolgvragen van de chat kun je dat dan bijsturen, bijvoorbeeld door te vragen om een andere taal-stijl in het resultaat. ("Pas het resultaat aan voor leerlingen van de tweede klas VMBO").

Een aantal tips voor het bijsturen (naar Mollick & Mollick):

| AI-fout | Mogelijke bijsturing |
| :---       | :---                             |
| Reageert met hardnekkige misvattingen  | Vraag de AI om een zoekopdracht uit te voeren; geef aanvullende context, bijvoorbeeld: in plaats van de AI te vragen om een analogie over een onderwerp, geef eerst informatie over het onderwerp en vraag dan om de analogie en vraag de AI uit te leggen hoe de analogie verband houdt met het concept. |
| Fout in redenering | Stapsgewijze instructies; few-shot prompting; keten van gedachte-redenering waarbij de AI een proces opsplitst in stappen en zo zijn eigen context creëert. |
| Oppervlakkige beheersing van onderwerpen resulterend in foutieve uitleg of uitvoer | Voeg details toe; leg in detail uit wat je wilt alsof je het aan een persoon uitlegt. | 
| Inconsistente uitvoer/weigering om te reageren of een actie uit te voeren | Vraag opnieuw; zeg de AI dat hij het kan; herformuleer de prompt. |
| Vastlopen in een eindeloze lus | Herinner de AI aan je doel; herstart het gesprek. |
| Argumentatief (twistziek)| Herstart of herleid het gesprek. |


## Profiel ("custom instructions")

Via je persoonlijke menu (rechtsboven) kun je via "ChatGPT aanpassen" je profiel aanpassen. De "custom instructions" bestaat uit twee delen:

* Wat moet ChatGPT over jou weten om betere reacties te geven?
* Hoe wil je dat ChatGPT reageert?

Deze elementen uit je profiel worden gecombineerd met je prompt: deze gegevens hoef je dan niet steeds in je prompts te herhalen.

Voor bepaalde vragen kun je dit profiel uitschakelen, bijvoorbeeld als je profiel werk-georiëntieerd is, en je een privé-vraag stelt. Als je wisselende profielen nodig hebt, kun je ook een verzameling van profielen bijhouden in een (Word) document, en steeds het relevantie profiel naar de instellingen kopiëren.

Meer informatie: https://help.openai.com/en/articles/8096356-custom-instructions-for-chatgpt