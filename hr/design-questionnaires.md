---
title: "Designe et spørgeskema"
description: "I dette emne beskrives fremgangsmåden til oprettelse af et spørgeskema. Det første trin er at designe spørgeskemaet. Når du designer et spørgeskema, skriver du ikke kun spørgsmål og svar, men opretter også den struktur, der gør det muligt at registrere svar og placere dem i tabelform."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0cac68f90f724777cfe8c3b7ac742d94b34ecd6b
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# Designe et spørgeskema
<a id="design-a-questionnaire" class="xliff"></a>

[!include[banner](includes/banner.md)]


I dette emne beskrives fremgangsmåden til oprettelse af et spørgeskema. Det første trin er at designe spørgeskemaet. Når du designer et spørgeskema, skriver du ikke kun spørgsmål og svar, men opretter også den struktur, der gør det muligt at registrere svar og placere dem i tabelform. 

Et omhyggelig udformet spørgeskemaet kan være med til at øge kvaliteten af de oplysninger, du indsamler. Via et omhyggeligt design kan du vælge de relevante indstillinger på det relevante tidspunkt for et spørgeskema. Følgende punkter kan hjælpe dig med at planlægge et effektivt spørgeskema:

-   Definer klart formålet med spørgeskemaet for at sikre, at spørgsmålene understøtter formålet.
-   Bestem den enkeltperson eller den gruppe af personer, der skal udfylde spørgeskemaet.
-   Skriv spørgsmål, der skal fremgå af spørgeskemaet, og medtag svarmuligheder, hvis det er relevant.
-   Sørg for, at spørgeskemaet flyder logisk, så svarpersonernes interesse fastholdes.
-   Opstil spørgsmål og svar i den rækkefølge, de skal præsenteres i for svarpersonerne.
-   Beslutte, hvordan resultaterne skal evalueres, hvis det er relevant.
-   Find ud af, om du har brug for yderligere funktioner. Bestem f.eks. om og hvordan resultater skal kategoriseres, om en tidsfrist er nødvendig, eller om alle spørgsmål skal være obligatoriske.

Designfasen indeholder fire kategorier af opgaver, der skal udføres i denne rækkefølge:

1.  Angiv forudsætninger efter behov.
2.  Angivelse af svargrupper og svar, hvis det er relevant.
3.  Angivelse af spørgsmål og deres tilknytning til svargrupperne.
4.  Opret selve spørgeskemaet, og føj spørgsmål til det.

## Forudsætninger
<a id="prerequisites" class="xliff"></a>
Visse forudsætninger skal være på plads, før du kan oprette spørgeskemaer, svar og spørgsmål. Det er imidlertid ikke alle forudsætninger, der er påkrævet for at få fuld funktionalitet.

### Påkrævet
<a id="required" class="xliff"></a>

| Forudsætning        | Beskrivelse                |
|---------------------|----------------------------|
| Spørgeskematyper | Kategoriser spørgeskemaer. |
| Spørgsmålstyper      | Kategoriser spørgsmål.      |

### Valgfri
<a id="optional" class="xliff"></a>

| Forudsætning             | Beskrivelse                                                    |
|--------------------------|----------------------------------------------------------------|
| Spørgeskemaparametre | Ret grundlæggende kontrolelementer og standardindstillingerne for spørgeskemaer. |

### Spørgeskematyper
<a id="questionnaire-types" class="xliff"></a>

Spørgeskematyper er obligatoriske og skal tildeles, når du opretter et spørgeskema. Spørgeskematyper gør det lettere at administrere og klassificere spørgeskemaer. Brug spørgeskematyper til at klassificere spørgeskemaer og skelne dem fra hinanden. Hvis du f.eks. har flere spørgeskemaer at vælge mellem, kan du filtrere dem for at gøre det nemmere at finde et bestemt spørgeskema. Følgende er eksempler på spørgeskematyper:

-   Personaleudvikling
-   Kundemeningsmålinger
-   Gennemse proces

### Spørgsmålstyper
<a id="question-types" class="xliff"></a>

Spørgsmålstyper er obligatoriske og skal tildeles, når du opretter et spørgsmål. 

Brug spørgsmålstyper til at kategorisere spørgsmål i forbindelse med rapporter. Spørgsmålstyper gør det også nemmere at finde spørgsmål, fordi du kan bruge typer som filtre på siden **Spørgsmål**. Følgende er eksempler på spørgsmålstyper:

-   Personale
-   Forretningsadministration
-   Kursusevaluering

### Spørgeskemaparametre
<a id="questionnaire-parameters" class="xliff"></a>

Parametre for spørgeskemaer er valgfri. Du kan vælge ikke at bruge dem, afhængigt af dit firmas behov. 

Spørgeskemaparametre definerer anonymitet, nummerseriekoder og referencetyper for et spørgeskema. Når en organisation udsender et spørgeskema, kan muligheden for at give svarpersonerne mulighed at være anonyme være noget, der skal tages i betragtning. 

Nummerseriekoderne bruges til at organisere spørgsmål og svar. Baseret på disse nummerseriekoder tildeles værdier automatisk til disse elementer. 

Du bør definere alle parametre, før du begynder at oprette dataene. Du kan til enhver tid ændre parameterindstillinger for spørgeskemaer.

## Spørgeskemakomponenter
<a id="questionnaire-components" class="xliff"></a>
Spørgeskemaer omfatter tre hovedelementer: svarsamlinger, der indeholder svar på spørgsmål med flere svarmuligheder, spørgsmål og selve spørgeskemaet. Du kan eventuelt også gruppere spørgsmål i et spørgeskema i resultatgrupper. Med resultatgrupper kan du kategorisere spørgsmål og få yderligere analyse af spørgeskemaet. 

[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)

### Svarsamlinger og svar
<a id="answer-groups-and-answers" class="xliff"></a>

Svarpersoner kan besvare et spørgsmål på to måder afhængigt af spørgsmålets emne:

-   Åbne spørgsmål kræver ikke svar i et bestemt format. Svarpersonerne kan angive et svar som tekst, et tal, en dato eller et klokkeslæt. Disse spørgsmål kræver typisk, at svarpersonerne angiver subjektive oplysninger i deres svar som en udtalelse, en beskrivelse, en vurdering eller et estimat.
-   Lukkede spørgsmål kræver, at svarpersonen vælger et svar på en liste over mulige korrekte svar.

For at angive en liste over mulige svar til lukkede spørgsmål kan du oprette svar på siden **Svarsamlinger**. 

Svarsamlinger og svar er komponenter, der udgør hovedafsnittet med oplysninger, som spørgsmålene oprettes ud fra. Når du har oprettet en svarsamling, kan du knytte svarsamlingen til et spørgsmål i feltet **Svarsamling** på siden **Spørgsmål**. 

En svarsamling kan bruges til mere end ét spørgsmål i det samme spørgeskema og kan også bruges i mere end ét spørgeskema. 

>**Bemærk!** Hvis du redigerer svartekst i svargrupper, der allerede er brugt i udfyldte spørgeskemaer, kan det blive vanskeligt at evaluere data, og resultaterne af spørgeskemaet er muligvis ikke længere gyldige. Hvis du skal ændre en svarsamling, kan du overveje at oprette en ny svargruppe i stedet for at ændre en eksisterende. Du kan ikke slette svargrupper, der er knyttet til et spørgsmål eller svar, eller som er besvaret.

### Spørgsmål
<a id="questions" class="xliff"></a>

Et spørgeskema skal indeholde spørgsmål. Spørgsmål kan enten være åbne eller lukkede.

-   Svar på spørgsmål med åbne svarmuligheder kontrolleres ikke, og svarpersonerne kan skrive deres svar.
-   Lukkede spørgsmål kræver en liste over foruddefinerede svarindstillinger, og spørgsmålene kan struktureres, så en svarperson kan vælge flere svarmuligheder. Spørgsmål skal være designet til at indhente specifikke oplysninger fra en svarperson og skal være kædet sammen med en svarsamling, der indeholder indstillinger for svar for hvert lukket spørgsmål. 
    >**Bemærk!** Før du kan definere lukkede spørgsmål, skal du oprette svarsamlinger og svar.

Spørgsmål kan arrangeres i et hierarki med betingede spørgsmål, så sekundære spørgsmål afhænger af det svar, som svarpersonen vælger til det forrige spørgsmål. Du kan skrive spørgsmålene først og så arrangere dem i et hierarki senere.

## Oprette spørgeskemaer
<a id="setting-up-questionnaires" class="xliff"></a>
>**Bemærk!**
>  Før du kan oprette et spørgeskema, skal du angive svar, spørgsmål og forudsætninger. 

Til hvert spørgeskema kan du angive følgende oplysninger:

-   Samlet timeantal eller tidsgrænse for besvarelse af obligatoriske spørgsmål.
-   Om alle spørgsmål skal besvares.
-   Om der skal beregnes point på et spørgeskema.
-   Hvordan resultater skal kategoriseres.
-   Om spørgeskemaet skal være tilgængelige for et begrænset antal svarpersoner.
-   Om der skal vises en formskabelon som baggrund til hver side i spørgeskemaet.
-   Om der kræves yderligere bemærkninger til at tydeliggøre formålet med spørgeskemaet for svarpersonerne.
-   Om spørgsmålene skal vises i en fast rækkefølge, eller om de skal vælges i tilfældig rækkefølge fra en pulje.
-   Om spørgsmål kun bliver stillet, hvis der gives bestemte svarmuligheder til foregående svar.

### Oprette et spørgeskema
<a id="set-up-a-questionnaire" class="xliff"></a>

Den primære side, som du kan bruge til at oprette et spørgeskema, er siden **Spørgeskemaer**. Når du vil oprette et spørgeskema, skal du udføre følgende opgaver i rækkefølge:

1.  Opret et spørgeskema.
2.  Benyt en af følgende fremgangsmåder til at knytte spørgsmål til spørgeskemaet:
    -   Hvis du bruger resultatgrupper, kan du føje spørgsmål til et spørgeskema ved hjælp af resultatgrupper. Opret først resultatgrupperne til spørgeskemaet, og føj derefter spørgsmål til resultatgrupperne.
    -   Hvis du ikke bruger resultatgrupper, kan du knytte spørgsmål direkte til spørgeskemaet.

3.  Opret et hierarki for betingede spørgsmål, hvis det er nødvendigt.
4.  Test spørgeskemaet.

Klik på **Valider** på siden **Spørgeskemaer** for at teste, om det er korrekt sat sammen. Vi anbefaler dog også, at du udfylder spørgeskemaet og selv tester skemaet, før du distribuerer det.

### Ændre et spørgeskema
<a id="modify-a-questionnaire" class="xliff"></a>

Du kan udføre følgende opgaver på siden **Spørgeskemaer**:

-   Ret oplysninger i spørgeskemaet, f.eks. resultatgrupper og spørgsmål.
-   Slette og tilføje spørgsmål.
-   Foretage ændringer i resultatgrupperne og sekvensnummeret. 

>**Advarsel!** Vær forsigtig, når du ændrer de spørgeskemaer der allerede er udfyldt. Ændringer kan reducere statistiknøjagtigheden, hvilket kan resultere i et dårligt grundlag for evalueringen. Overvej at oprette et nyt spørgsmål i stedet for at ændre et spørgsmål, som allerede er besvaret.

Du kan ikke slette følgende typer spørgsmål i et spørgeskema:

-   Spørgsmål, der er knyttet til et spørgeskema
-   Spørgsmål, der allerede er besvaret, og som derfor findes i dialogboksen **Svar**.

### Resultatgrupper
<a id="result-groups" class="xliff"></a>

Resultatgrupper er valgfrie, når du føjer spørgsmål til et spørgeskema. 

En resultatgruppe bruges til at beregne point og kategorisere resultaterne af et spørgeskema. Hvis du bruger resultatgrupper, kan du udføre følgende opgaver:

-   Evaluere resultaterne af spørgeskemaet på baggrund af pointstatistik.
-   Evaluere en svarpersons point for hver resultatgruppe, som du opretter.
-   Opret statistik for hver resultatgruppe, som kan hjælpe dig med at analysere resultaterne.
-   Udskrive en rapport, der viser resultaterne for hver resultatgruppe og også valgfri point/tekster, der er baseret på point, som er optjent i hver resultatgruppe.

> **Bemærk!**
>  Inden du kan konfigurere resultatgrupper, skal du fuldføre følgende opgaver:

-   Konfigurere lukkede spørgsmål. Til et lukket spørgsmål skal inputtypen på siden **Spørgsmål** være **Afkrydsningsfelt**, **Alternativknap** eller **Kombinationsboks**.
-   Definer point for svar i svargrupperne, der tildeles hvert spørgsmål.
-   Oprette et spørgeskema.

For at føje spørgsmål til et spørgeskema ved hjælp af resultatgrupper skal du først oprette resultatgrupper for spørgeskemaet og derefter føje spørgsmål til resultatgruppen. Hvis du ikke bruger resultatgrupper, kan du knytte spørgsmål direkte til et spørgeskema. 

Du kan angive flere resultatgrupper for at evaluere point, som en svarperson optjener i hver kategori. Når et spørgeskema er fuldført, kan du få vist de point, der er opnået for hver resultatgruppe. 

> **Tip!**
>  For at evaluere et spørgeskema ved at bruge point men ikke separate kategorier kan du føje alle spørgsmål til en enkelt resultatgruppe. 

For hver resultatgruppe kan du også oprette en eller flere pointbaserede meddelelser, som svarpersoner modtager, efter de har udfyldt et spørgeskema. Den tekst, der vises, kan variere alt efter det resultat, som en svarperson opnår i en resultatgruppe. For at bruge pointbaserede meddelelser skal du definere pointintervaller og en beskrivelse af hvert interval. Når en svarperson opnår et resultat i et bestemt interval, er teksten til det pågældende interval medtaget i resultatrapporten. 

Da en resultatgruppe vedrører points, der er knyttet til et bestemt sæt spørgsmål i et spørgeskema, kan du kun bruge en bestemt resultatgruppe til et spørgeskema.

#### Eksempel: Point/tekster til resultatgruppe 3
<a id="example-pointstexts-for-result-group-3" class="xliff"></a>

Du bruger et spørgeskema til en ledertest med 15 spørgsmål i tre kategorier. Du opretter tre resultatgrupper og knytter fem spørgsmål til hver resultatgruppe. Point opsummeres så i de tre grupper. De tre resultatgrupper er som følger:

-   Kreativitet
-   Lederevner
-   Teknisk kunnen

Hvis du vil bruge pointbaserede meddelelser, kan du angive tekstintervaller for hver resultatgruppe. Hvert spørgsmål tildeles to point. Derfor er det maksimale antal point i hver resultatgruppe 10. 

Følgende tabel viser de pointbaserede meddelelser, som du definerer for resultatgruppen "lederevner".

| Pointinterval | Tekst                                       |
|----------------|--------------------------------------------|
| 1-3         | Du har gennemsnitlige lederevner.     |
| 4-7         | Du har gode lederevner.        |
| 8-10        | Du har fremragende lederevner. |

Du kan angive pointintervaller og tekster til hver resultatgruppe i et spørgeskema. Tekster, der svarer til hver svarpersons score, vises for hver resultatgruppe. 

> **Bemærk!**
>  Du kan ændre intervaller og tekster. Hvis et spørgeskema er udfyldt, kan ændringer dog forårsage uoverensstemmelser mellem gamle og nye resultatrapporter.

### Hierarkier med betingede spørgsmål
<a id="conditional-question-hierarchies" class="xliff"></a>

Hierarkier med betingede spørgsmål er valgfrie, når du konfigurerer et spørgeskema. 

> **Bemærk!**
>  Før du kan konfigurere et hierarki med betingede spørgsmål, skal du knytte spørgsmål, der har tildelte svargrupper, til spørgeskemaet. 

Hvis du vil bruge betingede spørgsmål til at oprette et spørgsmålshierarki i et spørgeskema, kan du lade rækkefølgen, som spørgsmålene vises i, være afhængig af det svar, som en svarperson vælger for hvert spørgsmål. Hvis du baserer spørgsmålenes rækkefølge på en svarpersons svar, kan du ændre spørgeskemaet, efterhånden som efter svarpersonen færdiggør det.

#### Eksempler
<a id="examples" class="xliff"></a>

En juridisk enhed tilbyder både varer og tjenester til kunderne. Som det ofte er tilfældet, køber nogle kunder kun varer, nogle køber kun tjenester, mens nogle køber begge både varer og tjenester. Når den juridiske enhed derfor distribuerer en undersøgelse om kundetilfredshed, anvender den en betinget struktur til spørgeskemaet, så kunder, som kun køber tjenester, ikke behøver at besvare spørgsmål om varer. 

Du kan alternativt oprette et spørgeskema, så hvis en svarpersonen vælger Svar A til spørgsmål 1, er Spørgsmål 2 det næste i rækkefølgen af spørgsmål. Men hvis svarpersonen vælger Svar B til Spørgsmål 1, kan Spørgsmål 5 være det næste.

Se også
<a id="see-also" class="xliff"></a>
--------

[Brug af spørgeskemaer](questionnaires.md)

[Distribution og udfyldning af et spørgeskema](distribute-questionnaires.md)

[Visning og evaluering af resultaterne af spørgeskemaer](evaluate-questionnaire-results.md)



