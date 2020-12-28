---
title: Styre lagerarbejde ved at bruge arbejdsskabeloner og lokalitetsdirektiver
description: I dette emne beskrives, hvordan du bruger arbejdsskabeloner og lokationsvejledninger til at bestemme, hvordan og hvor der udføres arbejde på lageret.
author: perlynne
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 21f6240b247433c7448a9aa5543996f19b3a25dd
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517422"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Styre lagerarbejde ved at bruge arbejdsskabeloner og lokalitetsdirektiver

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du bruger arbejdsskabeloner og lokationsvejledninger til at bestemme, hvordan og hvor der udføres arbejde på lageret.

De instruktioner, som lagermedarbejderne modtager på en mobilenhed, bestemmes af de arbejdsskabeloner, du konfigurerer i Dynamics 365 Supply Chain Management for at definere de forskellige lagerprocesser og -opgaver. Arbejdsskabeloner afgør, hvordan arbejdet udføres for hver proces på lagerstedet. Når du sammenkæder et lokalitetsdirektiv med arbejdsskabeloner, kan du sikre, at arbejdet forekommer i bestemte fysiske områder på lagerstederne.

## <a name="work-templates"></a>Arbejdsskabeloner

Siden **Arbejdsskabeloner** gør det muligt at definere arbejdshandlinger, der skal udføres på lagerstedet. Arbejdshandlinger på lagersted består typisk af parvise handlinger: en lagerarbejder plukker disponibel lagerbeholdning på ét sted og sætter derefter det plukkede lager ned på en anden placering. 

Arbejdsskabeloner består af et hoved og tilhørende linjer. Hver arbejdsskabelon gælder en bestemt *arbejdsordretype*. Mange arbejdsordretyper er knyttet til kildedokumenter som f.eks. købs- eller salgsordrer. Andre arbejdsordretyper repræsenterer separate lagerstedsprocesser, f.eks cyklusoptælling. *Arbejdspulje-id'et* gør det muligt at organisere arbejdet i grupper. 

Brug indstillingerne i arbejdshoveddefinitionen til at bestemme, hvornår der skal oprettes et nyt arbejdsemne. Du kan for eksempel angive et maksimalt antal pluklinjer og en maksimal forventet plukketid. Hvis arbejdet for en salgsordreplukkeprocessen derefter overstiger en af disse værdier, bliver det arbejde opdelt i to stykker arbejde.

Brug knappen **Opgaveoverskriften skifter** til at definere, hvornår systemet skal oprette nye arbejdshoveder. Hvis du f.eks. vil oprette et arbejdshoved for hvert _ordrenummer_, skal du vælge **Rediger forespørgsel** i handlingsruden og derefter føje feltet **Ordrenummer** til fanen **Sortering** i forespørgselseditoren. Felter, der føjes til fanen **Sortering**, kan vælges som *grupperingsfelter*. Hvis du vil angive grupperingsfelterne, skal du vælge **Opgaveoverskriften skifter** i handlingsruden og derefter markere afkrydsningsfeltet i kolonnen **Gruppér efter dette felt** for hvert af de felter, du vil bruge som grupperingsfelt.

Arbejdslinjerne repræsenterer de fysiske opgaver, der kræves for at behandle arbejdet. For en udgående lagerproces kan der for eksempel være én arbejdslinje til plukning af varer i lagerstedet og en anden linje til placering af varerne i et midlertidigt lagerområde. Der kan derefter være en ekstra linje til plukning af varer fra det midlertidige lagerområde og en anden linje til placering af varerne på en lastbil som en del af læsseprocessen. Du kan angive en *direktivkode* på arbejdsskabelonlinjerne. Et direktivkode er knyttet til et placeringsdirektiv og sikrer derfor, at lagerstedsarbejdet behandles på den korrekte placering på lagerstedet.

Du kan oprette en forespørgsel til at styre, hvornår en bestemt arbejdsskabelon bruges. Du kan for eksempel angive en begrænsning, så en bestemt skabelon kun kan bruges til arbejde på et bestemt lagersted. Du kan også have flere skabeloner, der opretter arbejde til behandling af udgående salgsordrer, afhængigt af salgsoprindelsen. Systemet bruger feltet **Løbenummer** til at bestemme den rækkefølge, som de tilgængelige arbejdsskabeloner vurderes i. Derfor, hvis du har en meget specifik forespørgsel til en bestemt arbejdsskabelon, skal du give den et lavt løbenummer. Denne forespørgsel vil derefter blive evalueret før de andre, mere generelle forespørgsler.

> [!NOTE]
> Hvis du vil forhindre, at systemet automatisk overskriver arbejdsskabelonen *sekvensnumre*, efter at en skabelon er blevet slettet, skal du aktivere funktionen *Bevar arbejdsskabeloners sekvensnumre ved sletning* i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

For at stoppe eller afbryde en arbejdsproces kan du bruge indstillingen **Stop arbejde** på arbejdslinjen. I så fald bliver den arbejder, der udfører arbejdet, ikke bedt om at udføre det næste arbejdslinjetrin. For at gå videre til næste trin skal den arbejder eller en anden arbejder vælge arbejdet igen. Du kan også adskille opgaverne i et stykke arbejde ved hjælp af et andet *arbejdsklasse-id* på arbejdsskabelonlinjerne.

## <a name="location-directives"></a>Lokationsvejledninger

Lokationsvejledninger er regler, der hjælper med at identificere pluk og læg-lokationer for lagerbevægelser. I f.eks. en salgsordretransaktion bestemmer en lokationsvejledning, hvor varerne plukkes, og hvor de plukkede varer skal lægges på lager. Lokationsvejledninger består af et hoved og tilhørende linjer, og du opretter dem på siden **Lokationsvejledninger**.

I hovedet skal hver lokationsvejledning være knyttet til en *arbejdsordretype*, der angiver den type lagertransaktion som direktivet anvendes til, f.eks. salgsordrer, genopfyldning eller plukning af råvarer. *Arbejdstype* angiver, om lokationsvejledningen bruges til at plukke eller placere arbejde eller til en anden lagerstedproces som f.eks. optælling eller ændringer i lagerstatus. Du skal også angive et *sted* og et *lager*. En *lokationskode*, som du angiver i hovedet, kan bruges til at kæde lokationsvejledningen sammen med en eller flere arbejdsskabeloner. 

Når det gælder arbejdsskabeloner, kan du konfigurere en forespørgsel for at finde ud af, om der bruges en bestemt lokationsvejledning. Du kan for eksempel angive, at når e-handel er udgangspunktet for en salgsordre, skal lageret være afhentet fra et bestemt område på lagerstedet. Systemet bruger feltet **Løbenummer** til at bestemme den rækkefølge, som de tilgængelige lokationsvejledninger vurderes i.

Linjerne i lokationsvejledninger angiver yderligere restriktioner for anvendelsen af søgeregler for lokationer. Du kan angive et minimumantal og et maksimumantal, som vejledningen skal gælde for, og du kan angive, at vejledningen skal gælde for en bestemt lagerenhed. Hvis måleenheden f.eks. er paller, kan elementerne i paller lægges på en bestemt lokalitet. Du kan også angive, om antallet kan opdeles på tværs af flere lokationer. Ligesom lokationsvejledningens overskrift har hver lokationsvejledningslinje et løbenummer, der bestemmer den rækkefølge, linjerne vurderes i.

Lokationsvejledninger har et ekstra niveau af detaljer: *lokationsvejledningshandlinger*. Du kan definere flere handlinger i lokationsvejledning for hver linje. Igen, et løbenummer bruges til at bestemme den rækkefølge, handlingerne vurderes i. På dette niveau kan du oprette en forespørgsel for at definere, hvordan du finder det bedste sted på lageret. Du kan også bruge foruddefinerede indstillinger for **Strategi** for at finde en optimal placering.

Yderligere oplysninger om, hvordan du opretter og konfigurerer lokationsvejledninger, finder du i afsnittet [Opret en lokationsvejledning](create-location-directive.md).

### <a name="how-location-directives-work"></a>Sådan fungerer lokationsvejledninger

Lokationsvejledninger bestemmer *, hvor* varer skal plukkes, og *hvor* de skal placeres. Systemet evaluerer en lokationsvejledning i forhold til hver enkelt arbejdslinje og vælger derefter en lokation baseret på oplysningerne i arbejdslinjen. Systemet finder først alle lokationsvejledninger, der svarer til en bestemt arbejdslinje (f.eks. er de til det korrekte lagersted og matcher forespørgslen). Derefter evalueres de vejledninger, den har fundet, i sekvens.

> [!NOTE]
> Der er særlige tilfælde, hvor pluklokationen eller læg på lager-lokationen allerede er valgt. Under _indkøbsregistrering_ er det første pluk f.eks. altid fra den lokation, hvor registreringen finder sted. Et andet eksempel er *lagerbevægelse efter skabelon*, hvor lagermedarbejderen vælger pluklokationen, og det kun er læg på lager-lokationer, der findes via lokationsvejledninger.

## <a name="additional-resources"></a>Yderligere ressourcer

- Video: [Detaljeret konfiguration af lokationsstyring](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Hjælp-emne: [Oprette lokationsvejledninger](create-location-directive.md)
