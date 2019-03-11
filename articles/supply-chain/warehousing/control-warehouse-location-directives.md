---
title: Styre lagerarbejde ved at bruge arbejdsskabeloner og lokalitetsdirektiver
description: I dette emne beskrives, hvordan du bruger arbejdsskabeloner og lokationsvejledninger til at bestemme, hvordan og hvor der udføres arbejde på lageret.
author: perlynne
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74e7c36fb912f35252d6e40d17477ac2962cbc23
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "325405"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Styre lagerarbejde ved at bruge arbejdsskabeloner og lokalitetsdirektiver

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du bruger arbejdsskabeloner og lokationsvejledninger til at bestemme, hvordan og hvor der udføres arbejde på lageret.

De instruktioner, som lagermedarbejderne modtager på en mobilenhed, bestemmes af de arbejdsskabeloner, du konfigurerer i Microsoft Dynamics 365 for Finance and Operations for at definere de forskellige lagerprocesser og -opgaver. Arbejdsskabeloner afgør, hvordan arbejdet udføres for hver proces på lagerstedet. Når du sammenkæder et lokalitetsdirektiv med arbejdsskabeloner, kan du sikre, at arbejdet forekommer i bestemte fysiske områder på lagerstederne.

## <a name="work-templates"></a>Arbejdsskabeloner
Siden **Arbejdsskabeloner** gør det muligt at definere arbejdshandlinger, der skal udføres på lagerstedet. Arbejdshandlinger på lagersted består typisk af parvise handlinger: en lagerarbejder plukker disponibel lagerbeholdning på ét sted og sætter derefter det plukkede lager ned på en anden placering. 

Arbejdsskabeloner består af et hoved og tilhørende linjer. Hver arbejdsskabelon gælder en bestemt *arbejdsordretype*. Mange arbejdsordretyper er knyttet til kildedokumenter som f.eks. købs- eller salgsordrer. Andre arbejdsordretyper repræsenterer separate lagerstedsprocesser, f.eks cyklusoptælling. *Arbejdspulje-id'et* gør det muligt at organisere arbejdet i grupper. 

Indstillingerne i arbejdshoveddefinitionen kan bruges til at bestemme, hvornår der skal oprettes et nyt arbejdsemne. Du kan for eksempel angive et maksimalt antal pluklinjer og en maksimal forventet plukketid. Hvis arbejdet for en salgsordreplukkeprocessen derefter overstiger en af disse værdier, bliver det arbejde opdelt i to stykker arbejde. 

Arbejdslinjerne repræsenterer de fysiske opgaver, der kræves for at behandle arbejdet. For en udgående lagerproces kan der for eksempel være en arbejdslinje til plukning af varer inden for lagerstedet og en anden linje til placering af varerne i et stadieinddelt område. Der kan derefter være en ekstra linje til plukning af varer fra det stadieinddelte område og en anden linje til placering af varerne på en lastbil som en del af læsseprocessen. Du kan angive en *direktivkode* på arbejdsskabelonlinjerne. Et direktivkode er knyttet til et placeringsdirektiv og sikrer derfor, at lagerstedsarbejdet behandles på den korrekte placering på lagerstedet. 

Du kan oprette en forespørgsel til at styre, hvornår en bestemt arbejdsskabelon bruges. Du kan for eksempel angive en begrænsning, så en bestemt skabelon kun kan bruges til arbejde på et bestemt lagersted. Du kan også have flere skabeloner, der bruges til at oprette arbejde til behandling af udgående salgsordrer, afhængigt af den salgsoprindelsen. Systemet bruger feltet **Løbenummer** til at bestemme den rækkefølge, som de tilgængelige arbejdsskabeloner vurderes i. Derfor, hvis du har en meget specifik forespørgsel til en bestemt arbejdsskabelon, skal du give den et lavt løbenummer. Denne forespørgsel vil derefter blive evalueret før andre, mere generelle forespørgsler. 

For at stoppe eller afbryde en arbejdsproces kan du bruge indstillingen **Stop arbejde** på arbejdslinjen. I så fald bliver den arbejder, der udfører arbejdet, ikke bedt om at udføre det næste arbejdslinjetrin. For at gå videre til næste trin skal den arbejder eller en anden arbejder vælge arbejdet igen. Du kan også adskille opgaverne i et stykke arbejde ved hjælp af et andet *arbejdsklasse-id* på arbejdsskabelonlinjerne.

## <a name="location-directives"></a>Lokationsvejledninger
Lokalitetsvejledninger er regler, der hjælper med at identificere pluk og læg-lokationer for lagerbevægelser. I f.eks. en salgsordretransaktion bestemmer en lokalitetsvejledning, hvor varerne plukkes, og hvor de plukkede varer skal lægges på lager. Lokationsvejledninger består af et hoved og tilhørende linjer, og du opretter dem på siden **Lokationsvejledninger**. 

I hovedet skal hver lokationsvejledning være knyttet til en *arbejdsordretype*, der angiver den type lagertransaktion som direktivet anvendes til, f.eks. salgsordrer, genopfyldning eller plukning af råvarer. *Arbejdstype* angiver, om lokationsvejledningen bruges til at plukke eller placere arbejde eller til en anden lagerstedproces som f.eks. optælling eller ændringer i lagerstatus. Du skal også angive et *sted* og et *lager*. En *lokationskode*, som du angiver i hovedet, kan bruges til at kæde lokationsvejledningen sammen med en eller flere arbejdsskabeloner. 

Når det gælder arbejdsskabeloner, kan du konfigurere en forespørgsel for at finde ud af, om der bruges en bestemt lokationsvejledning. Du kan for eksempel angive, at når e-handel er udgangspunktet for en salgsordre, skal lageret være afhentet fra et bestemt område på lagerstedet. Systemet bruger feltet **Løbenummer** til at bestemme den rækkefølge, som de tilgængelige lokationsvejledninger vurderes i. 

Linjerne i lokationsvejledninger angiver yderligere restriktioner for anvendelsen af søgeregler for lokationer. Du kan angive et minimumantal og et maksimumantal, som vejledningen skal gælde for, og du kan angive, at vejledningen skal gælde for en bestemt lagerenhed. Hvis måleenheden f.eks. er paller, kan elementerne i paller lægges på en bestemt lokalitet. Du kan også angive, om antallet kan opdeles på tværs af flere lokationer. Ligesom lokationsvejledningens overskrift har hver lokationsvejledningslinje et løbenummer, der bestemmer den rækkefølge, linjerne vurderes i. 

Lokationsvejledninger har et ekstra niveau af detaljer: *lokationsvejledningshandlinger*. Du kan definere flere handlinger i lokationsvejledning for hver linje. Igen, et løbenummer bruges til at bestemme den rækkefølge, handlingerne vurderes i. På dette niveau kan du oprette en forespørgsel for at definere, hvordan du finder det bedste sted på lageret. Du kan også bruge foruddefinerede indstillinger for **Strategi** for at finde en optimal placering.

## <a name="location-directives-configuration-details"></a>Oplysninger om konfiguration af lokationsvejledninger 

 ### <a name="sequence-number"></a>Løbenummer
 
Dette nummer angiver den rækkefølge, som lokalitetsvejledningen skal behandles i for den valgte ordretype. Det kan ændres ved hjælp af **Flyt op** og **Flyt ned** i menuen.
 
 ### <a name="work-type"></a>Arbejdstype
 
Dette er den type arbejde, der skal udføres. Typen af arbejde, der er tilgængelig, er baseret på typen af lagertransaktion, som du har valgt i feltet **Arbejdsordretype**.
-   **Læg på lager** – Arbejdstypen **Læg på lager** betyder, at lokationsvejledningen vil finde den mest ideelle lokation til at placere eller finde lager, der kommer ind i systemet, enten fra modtagelse, produktion eller lagerreguleringer. Den kan også bruges til at definere en Læg på stadielokation eller en endelig lagerport som afsendelseslokation.
-   **Pluk** – Arbejdstypen **Pluk** betyder, at lagerstedet vil finde den mest ideelle lokation til fysisk reserveration af lager fra (oprette arbejde). Plukket kan fuldføres (plukarbejdslinje kan lukkes), også selvom arbejdet ikke er fuldført. Brugeren kan fuldføre fysisk pluk, som er et pluktrin. Brugeren kan derefter annullere fra en mobilenhed og fuldføre arbejdet senere. Dog lukkes arbejdshovedet, når endelig læg på lager er fuldført. 
-   **Optælling, reguleringer, brugerdefineret, ændring af lagerstatus, id-opbygning, udskrivning, statusændring, pak til indlejrede id'er** - Disse kan ikke bruges i nogen opsætning af lokationsvejledning. Dette er en fasttekst, så der er ingen filtrering knyttet til arbejdsordretypen. 

### <a name="directive-code"></a>Vejledningskode

Vælg den vejledningskode, der skal knyttes til en arbejds- eller genopfyldningsskabelon. På formen **Vejledningskode** kan du oprette nye koder, der kan bruges til forbindelser mellem en arbejdsskabelon, genopfyldningsskabelon og lokationsvejledning. Den kan også bruges til at oprette forbindelse mellem enhver arbejdsskabelonlinje lokationsvejledning (f.eks. lagerport eller stadielokation).

Bemærk, at hvis koden er angivet, når arbejde genereres, søger systemet ikke i lokationsvejledningen i sekvens, men efter vejledningskode. Det betyder, at du kan være mere specifik omkring, hvilken lokationsskabelon der bruges til et bestemt trin i en arbejdsskabelon , f.eks. midlertidige materialer. 

### <a name="site"></a>Sted

Sted er et obligatorisk felt, fordi lokationsvejledningen skal bruge det sted og lagersted, den gælder for. 

### <a name="warehouse"></a>Lagersted

Lagersted er et obligatorisk felt, fordi lokationsvejledningen skal bruge det sted og lagersted, den gælder for.

### <a name="multiple-sku"></a>Flere SKU'er

Dette giver mulighed for flere lagerenheder (SKU) på en lokation, f.eks. lagerport. Hvis du vælger **Flere SKU'er**, angives læg på lager-lokationen i arbejde (hvilket forventes), men den vil kun kunne lægge flere varer på lager (hvis arbejdet omfatter SKU'er, der skal plukkes og placeres, ikke en enkelt SKU-placering). Hvis du ikke vælger **Flere SKU'er**, vil læg på lager-lokationen kun være angivet, hvis placeringen kun har én slags SKU. Hvis du vil bruge begge handlinger, skal du angive to linjer, den ene med flere SKU'er slået til, og den anden med flere SKU'er slået fra. Disse skal have samme struktur og opsætning. I forbindelse med læg på lager skal du have lokationsvejledninger, der er identiske, selvom du ikke skelner mellem enkelte og flere SKU'er på arbejds-id'er. Du skal også konfigurere pluk, hvis du har en ordre med mere end én vare.

### <a name="sequence-number"></a>Løbenummer

Angiv den rækkefølge, som lokalitetsvejledningslinjen skal behandles i for den valgte arbejdstype. Du kan også ændre rækkefølgen, hvis det er nødvendigt, ved hjælp af **Flyt op** og **Flyt ned**.

### <a name="fromto-quantity"></a>Fra/til antal

Det giver mulighed for at angive et antalsinterval for, hvornår den midterste gitterrækkefølge skal være valgt. Du kan angive fra/til-interval i antal i den pågældende enhed.

### <a name="unit"></a>Enhed

Du kan angive et minimumantal og et maksimumantal, som vejledningen skal gælde for, og du kan angive, at vejledningen skal gælde for en bestemt lagerenhed. Feltet enhed på linjen bruges kun til evaluering af antal.

Når det kontrolleres, om lokationsvejledningslinjen er gældende, baseres det på antallet i den tilhørende enhed, der er angivet på lokationsvejledningslinjen. Hver gang en lokationsvejledningslinje nås, forsøger systemet at konvertere efterspørgselsenheden til en enhed, der er angivet på linjen. Hvis måleenhedsomregningen ikke findes, fortsættes til næste linje. 

### <a name="locate-quantity"></a>Angiv lokalitet for antal

Denne indstilling bruges kun til at lægge/finde antal på lagerstedet. Den er kun til arbejdstypen læg på lager. Følgende værdier er gyldige:

-   **Nummerpladeantal** – Ved vurdering af, om antallet er inden for "Fra"- og "Til"-antalsintervallerne, kan du anvende antallet på den nummerplade, der modtages.
-   **Enhedsopdelt antal** – Ved vurdering af, om antallet er inden for "Fra"- og "Til"-antalsintervallerne, kan du anvende det antal, der enhedsopdeleles under den konkrete transaktion.
-   **Resterende antal** – Ved vurdering af, om antallet er inden for "Fra"- og "Til"-antalsintervallerne, kan du bruge det antal, som stadig ikke er modtaget på den indkøbsordrelinje, der i øjeblikket checkes ind.
-   **Forventet antal** – Ved vurdering af, om antallet er inden for "Fra"- og "Til"-antalsintervallerne, kan du bruge det samlede antal på indkøbsordrelinjen, uanset hvad der allerede er modtaget.

### <a name="restrict-by-unit"></a>Begræns efter enhed

Dette gør det muligt at oprette en lokationsvejledningslinje specifikt til en eller flere måleenheder. Når du skal reservere antallet, og hvis du kun vil reservere paller fra et bestemt sæt lokationer, vil den midterste gittersekvens begrænse den pågældende sekvens til "PL", så ethvert antal, der er mindre end en palle, ikke vil vælge sekvensen. Vælg **Begræns efter enhed** for at konfigurere enhederne. Du kan også begrænse linjen til mere end én enhed. Dette fungerer kun med lokationsvejledninger af typen pluk. 

### <a name="round-up-to-unit"></a>Rund op til enhed

Dette felt bruges sammen med feltet **Begræns efter enhed**. Hvis lokationsvejledningslinjen **Begræns efter enhed** er indstillet til "boks", og du vælger **Rund op til enhed**, bliver det arbejde, der er genereret ud fra vejledningen til pluk af råvarer, afrundet til et multiplum af en materialehåndteringsenhed (angivet i **Begræns efter enhed**). Bemærk, at det kun fungerer for pluk af råvarer, og kun med lokationsvejledninger af typen pluk.

### <a name="locate-packing-qty"></a>Find emballagemængde

Hvis en emballagemængde er angivet på en salgsordre, overflytningsordre eller produktionsordre, begrænser det systemet til kun at vælge lokationer med en emballagemængde på lokationen. Dette fungerer kun med lokationsvejledninger af typen pluk.

### <a name="allow-split"></a>Tillad opdeling

Dette angiver, om en lokationsvejledning har tilladelse til at opdele det antal, der modtages eller reserveres på tværs af flere lokationer på lagerstedet, eller om hele antallet skal være placeret på eller reserveret fra en enkelt lokation for at kunne oprette arbejde. 

### <a name="sequence-number"></a>Løbenummer

Dette nummer er den rækkefølge, som lokalitetsvejledningen skal behandles i for den valgte arbejdstype. Du kan om nødvendigt ændre rækkefølgen. Vær dog forsigtig med at bruge sekvensnumre, da behandling altid køres i sekvens. 

### <a name="name"></a>Navn

Angiv et navn til lokalitetsvejledningens handling. Sørg for at være specifik, når du angiver et navn.

### <a name="fixed-location-usage"></a>Anvendelse af fast lokation 

-   **Faste og ikke-faste lokationer** - Lokationsvejledningen medtager alle lokationer.
-   **Kun faste lokationer for produktet** - Lokationsvejledningen medtager kun faste lokationer for produkter.
-   **Kun faste lokationer for produktvarianten** - Lokationsvejledningen medtager kun faste lokationer for produktvarianter.

### <a name="allow-negative-inventory"></a>Tillad negativ lagerbeholdning

Vælg denne indstilling for at tillade negativt lager på den angivne lagerlokation i lokationsvejledninger. 

### <a name="batch-enabled"></a>Batchaktiveret 

Vælg denne for at bruge batchstrategier til de varer, der er batchaktiverede. Hvis en linje er nået, hvor **Batchaktiveret** er angivet med en vare uden batch, fortsætter processen til den næste handlingslinje. 

### <a name="strategy"></a>Strategi

-   **Konsolider** - Denne strategi bruges til at konsolidere varer i en bestemt lokation, når der allerede findes lignende varer. Dette fungerer kun med lokationsvejledninger af typen Læg på lager. Almindelig opsætning af læg på lager er at konsolidere på den første handlingslinje og derefter i andet forsøg at lægge på lager uden konsolidering. Konsolidering af varer gør senere pluk mere effektivt.
-   **Match emballagemængde** - Denne strategi bruges til at kontrollere, om en pluklokation har den angivne emballagemængde. Dette fungerer kun med lokationsvejledninger af typen Pluk. 
-   **FEFO-batchreservation** - Denne strategi bruges, når lageret lokaliseres ved hjælp af en batchudløbsdato og tildeles batchreservation. Du kan kun bruge denne strategi til batchaktiverede varer. Dette fungerer kun med lokationsvejledninger af arbejdstypen Pluk. 
-   **Rund op til fuld LP** - Denne strategi bruges til at afrunde det lagerantal, der skal svare til antallet af id-numre, som er tildelt de varer, der skal plukkes. Du kan kun bruge denne strategi for genopfyldningstypen til lokationsvejledning af typen Pluk. 
-   **Tom lokation uden indgående arbejde** - Denne strategi bruges til at finde tomme lokationer. Lokaliteten anses for at være tom, hvis den ikke har noget fysisk lager og intet forventet indgående arbejde. Denne strategi bruges kun til lokationsvejledninger af typen Læg på lager. 

### <a name="example-of-the-use-of-location-directives"></a>Eksempel på brug af lokationsvejledninger

I dette eksempel ser vi på en indkøbsordreproces, hvor lokationsvejledningen skal finde ledig kapacitet inden for et lagersted for lagervarer, der netop er registreret i modtagelsesområdet. Du skal først prøve at finde ledig kapacitet på lagerstedet ved at konsolidere med eksisterende disponibel lagerbeholdning. Hvis konsolideringen ikke er muligt, skal du finde en tom lokation. 

I dette scenarie skal du definere to handlinger i lokationsvejledningen. Den første handling i rækken skal bruge strategien **Konsolider**, og den anden skal bruge strategien **Tom lokation uden indgående arbejde**. Medmindre du definerer en tredje handling for at håndtere et overløbsscenarie, er der to mulige udfald, når der ikke er mere kapacitet på lagerstedet. Arbejde kan oprettes, selvom ingen lokationer er defineret, eller processen til oprettelse af arbejde kan mislykkes. Resultatet bestemmes af opsætningen på siden **Fejl i lokationsvejledning**, hvor du kan beslutte, om du vil vælge indstillingen **Stop arbejdet ved fejl i lokationsvejledning** for hver arbejdsordretype.
