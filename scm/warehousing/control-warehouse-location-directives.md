---
title: "Styre lager arbejde ved hjælp af skabeloner til arbejde og placering direktiver"
description: "I denne artikel beskrives, hvordan du bruger arbejdsskabeloner og lokationsvejledninger til at bestemme, hvordan og hvor der udføres arbejde på lageret."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 64bcea1f305d67c01967184596a58a48a002cf48
ms.lasthandoff: 03/31/2017


---

# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Styre lager arbejde ved hjælp af skabeloner til arbejde og placering direktiver

I denne artikel beskrives, hvordan du bruger arbejdsskabeloner og lokationsvejledninger til at bestemme, hvordan og hvor der udføres arbejde på lageret.

De instruktioner, som lagermedarbejderne modtager på en mobilenhed, bestemmes af de arbejdsskabeloner, du konfigurerer i Microsoft Dynamics 365 for Operations for at definere de forskellige lagerprocesser og -opgaver. Arbejdsskabeloner afgør, hvordan arbejdet udføres for hver proces på lagerstedet. Når du sammenkæder et lokalitetsdirektiv med arbejdsskabeloner, kan du sikre, at arbejdet forekommer i bestemte fysiske områder på lagerstederne.

## <a name="work-templates"></a>Arbejdsskabeloner
Siden **Arbejdsskabeloner** gør det muligt at definere arbejdshandlinger, der skal udføres på lagerstedet. Arbejdshandlinger på lagersted består typisk af parvise handlinger: en lagerarbejder plukker disponibel lagerbeholdning på ét sted og sætter derefter det plukkede lager ned på en anden placering. 

Arbejdsskabeloner består af et hoved og tilhørende linjer. Hver arbejdsskabelon gælder en bestemt *arbejdsordretype*. Mange arbejdsordretyper er knyttet til kildedokumenter som f.eks. købs- eller salgsordrer. Andre arbejdsordretyper repræsenterer separate lagerstedsprocesser, f.eks cyklusoptælling. *Arbejdspulje-id'et* gør det muligt at organisere arbejdet i grupper. 

Indstillingerne i arbejdshoveddefinitionen kan bruges til at bestemme, hvornår der skal oprettes et nyt arbejdsemne. Du kan for eksempel angive et maksimalt antal pluklinjer og en maksimal forventet plukketid. Hvis arbejdet for en salgsordreplukkeprocessen derefter overstiger en af disse værdier, bliver det arbejde opdelt i to stykker arbejde. 

Arbejdslinjerne repræsenterer de fysiske opgaver, der kræves for at behandle arbejdet. For en udgående lagerproces kan der for eksempel være en arbejdslinje til plukning af varer inden for lagerstedet og en anden linje til placering af varerne i et stadieinddelt område. Der kan derefter være en ekstra linje til plukning af varer fra det stadieinddelte område og en anden linje til placering af varerne på en lastbil som en del af læsseprocessen. Du kan angive en *direktivkode *på arbejdsskabelonlinjerne. Et direktivkode er knyttet til et placeringsdirektiv og sikrer derfor, at lagerstedsarbejdet behandles på den korrekte placering på lagerstedet. 

Du kan oprette en forespørgsel til at styre, hvornår en bestemt arbejdsskabelon bruges. Du kan for eksempel angive en begrænsning, så en bestemt skabelon kun kan bruges til arbejde på et bestemt lagersted. Du kan også have flere skabeloner, der bruges til at oprette arbejde til behandling af udgående salgsordrer, afhængigt af den salgsoprindelsen. Systemet bruger den **sekvensnummer** til at bestemme den rækkefølge, som vurderes tilgængeligt arbejde-skabeloner i. Derfor, hvis du har en meget specifik forespørgsel efter en bestemt arbejde-skabelon, du skal give det en lave sekvensnummer. Denne forespørgsel vil derefter blive evalueret før andre, mere generelle forespørgsler. 

For at stoppe eller afbryde en arbejdsproces kan du bruge indstillingen **Stop arbejde** på arbejdslinjen. I så fald bliver den arbejder, der udfører arbejdet, ikke bedt om at udføre det næste arbejdslinjetrin. For at gå videre til næste trin skal den arbejder eller en anden arbejder vælge arbejdet igen. Du kan også adskille opgaverne i et stykke arbejde ved hjælp af et andet *arbejdsklasse-id* på arbejdsskabelonlinjerne.

## <a name="location-directives"></a>Lokationsvejledninger
Lokalitetsvejledninger er regler, der hjælper med at identificere pluk og læg-lokationer for lagerbevægelser. I f.eks. en salgsordretransaktion bestemmer en lokalitetsvejledning, hvor varerne plukkes, og hvor de plukkede varer skal lægges på lager. Lokationsvejledninger består af et hoved og tilhørende linjer, og du opretter dem på siden **Lokationsvejledninger**. 

I hovedet skal hver lokationsvejledning være knyttet til en *arbejdsordretype *, der angiver den type lagertransaktion som direktivet anvendes til, f.eks. salgsordrer, genopfyldning eller plukning af råvarer. *Arbejdstype *angiver, om lokationsvejledningen bruges til at plukke eller placere arbejde eller til en anden lagerstedproces som f.eks. optælling eller ændringer i lagerstatus. Du skal også angive et *sted *og et *lager*. En *lokationskode*, som du angiver i hovedet, kan bruges til at kæde lokationsvejledningen sammen med en eller flere arbejdsskabeloner. 

Når det gælder arbejdsskabeloner, kan du konfigurere en forespørgsel for at finde ud af, om der bruges en bestemt lokationsvejledning. Du kan for eksempel angive, at når e-handel er udgangspunktet for en salgsordre, skal lageret være afhentet fra et bestemt område på lagerstedet. Systemet bruger feltet **Løbenummer** til at bestemme den rækkefølge, som de tilgængelige lokationsvejledninger vurderes i. 

Linjerne i lokationsvejledninger angiver yderligere restriktioner for anvendelsen af søgeregler for lokationer. Du kan angive et minimumantal og et maksimumantal, som vejledningen skal gælde for, og du kan angive, at vejledningen skal gælde for en bestemt lagerenhed. Hvis måleenheden f.eks. er paller, kan elementerne i paller lægges på en bestemt lokalitet. Du kan også angive, om antallet kan opdeles på tværs af flere lokationer. Ligesom lokationsvejledningens overskrift har hver lokationsvejledningslinje et løbenummer, der bestemmer den rækkefølge, linjerne vurderes i. 

Lokationsvejledninger har et ekstra niveau af detaljer: *lokationsvejledningshandlinger*. Du kan definere flere handlinger i lokationsvejledning for hver linje. Igen, et sekvensnummer, der bruges til at bestemme den rækkefølge, handlingerne, der vurderes i. På dette niveau, kan du oprette en forespørgsel til at definere, hvordan du finder den bedste placering på lageret. Du kan også bruge foruddefinerede indstillinger for **Strategi **for at finde en optimal placering.

### <a name="example-of-the-use-of-location-directives"></a>Eksempel på brug af lokationsvejledninger

I dette eksempel ser vi på en indkøbsordreproces, hvor lokationsvejledningen skal finde ledig kapacitet inden for et lagersted for lagervarer, der netop er registreret på i modtagelsesområdet. Vi vil først prøve at finde ledige kapacitet inden for lageret ved at konsolidere med eksisterende disponibel lagerbeholdning. Hvis konsolideringen ikke er muligt, skal vi finde en tom lokation. 

I dette scenarie skal vi definere to handlinger i lokationsvejledningen. Den første handling i rækken skal bruge strategien **Konsolider**, og den anden skal bruge strategien **Tom lokation uden indgående arbejde**. Medmindre vi definerer en tredje handling for at håndtere et overløbsscenarie, er der to mulige udfald, når der ikke er mere kapacitet på lagerstedet. Arbejde kan oprettes, selvom ingen lokationer er defineret, eller processen til oprettelse af arbejde kan mislykkes. Resultatet bestemmes af opsætningen på siden **Fejl i lokationsvejledning**, hvor du kan beslutte, om du vil vælge indstillingen **Stop arbejdet ved fejl i lokationsvejledning** for hver arbejdsordretype.

