---
title: "Få vist og eksportere feltbeskrivelser"
description: "I denne artikel beskrives, hvordan du får vist feltbeskrivelser, og hvordan du bruger siden Felt beskrivelser til at eksportere beskrivelser."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: d4fc9cdee0e2160e363f9defcf6bdbc57ed4db74
ms.lasthandoff: 03/31/2017


---

# <a name="view-and-export-field-descriptions"></a>Få vist og eksportere feltbeskrivelser

I denne artikel beskrives, hvordan du får vist feltbeskrivelser, og hvordan du bruger siden Felt beskrivelser til at eksportere beskrivelser.

Microsoft Dynamics 365 for Operations indeholder feltbeskrivelser for nogle af de mere komplekse felter. Disse beskrivelser vises, når du peger på et felt. Du kan også se og eksportere beskrivelser på siden **Feltbeskrivelser**. 

Ikke alle sider har feltbeskrivelser. Vi vil kun levere beskrivelser for de mest komplekse felter og ikke for felter, hvis funktion er indlysende. Derfor har nogle sider ikke nogen feltbeskrivelser, nogle sider har kun få beskrivelser, og nogle af de mere komplekse sider, som f.eks. mange af parametersiderne, har mange beskrivelser. 

Hvis du har adgang til Dynamics 365 for Operations-udviklingsmiljøet, kan du tilføje nye feltbeskrivelser og tilpasse eksisterende beskrivelser. For eksempel kan du føje virksomhedsspecifikke oplysninger til en feltbeskrivelse. Du kan finde flere oplysninger under [Tilpasse hjælp til felter](/dynamics365/operations/dev-itpro/user-interface/customize-field-help).

## <a name="see-field-descriptions-in-the-user-interface"></a>Se feltbeskrivelser i brugergrænsefladen
Du kan se feltbeskrivelser ved at holde musen over et felt. Hvis ingen beskrivelse er tilgængelig, kan du se navnet på feltet, når du peger på feltet. (Bemærk: version 7.0.0 feltbeskrivelser kan vises kun på de **i feltet Beskrivelse** side.) I følgende illustration vises feltet Beskrivelse, der vises, når du peger på den **Lås varer under optælling** felt. 

[![Eksempel på et felt beskrivelse](./media/field-description.png)](./media/field-description.png)

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a>Bruge siden Feltbeskrivelser til at få vist og eksportere hjælp
På siden **Feltbeskrivelser** kan du få vist og eksportere feltbeskrivelser. Du kan se de tilgængelige beskrivelser én side ad gangen.

### <a name="view-the-descriptions-for-a-page"></a>Se en sides beskrivelser

For at se beskrivelserne for en side skal du følge dette trin.

-   I feltet **Vælg en side** skal du skrive navnet på siden. Du kan også klikke på pilen for at åbne en liste over alle siderne og derefter gennemse eller filtrere listen.

Du kan enten bruge navnet på den side, der vises i brugergrænsefladen (f.eks. **Kunder**) eller kodenavnet (AOT-navnet), der bliver tilgængeligt, når du højreklikker på en side (f.eks. **CustTable**). 

Du kan finde oplysninger om de forskellige måder at filtrere listen over sider i afsnittet "Sådan søger du efter en side" senere i denne artikel. 

Hvis du vælger **Ja** i indstillingen **Inkludér felter uden en beskrivelse**, vises alle felter på siden, også selvom de ikke har en feltbeskrivelse.

### <a name="export-the-descriptions-for-a-page"></a>Eksportér en sides beskrivelser

For at eksportere beskrivelserne for en side skal du følge disse trin.

1.  Vælg en side i feltet **Vælg en side**.
2.  Klik på **Åbn i Microsoft Office**-knappen i øverste højre hjørne, og klik derefter på **FieldDescriptionTmp**.

### <a name="searching-for-a-page"></a>Sådan søger du efter en side

Der er flere måder at søge efter en side i feltet **Vælg en side**. Ofte skal du klikke på pilen i feltet **Vælg en side** for at åbne rullelisten og derefter vælge en filtreret liste over sider.

-   Skriv en del af navnet, og åbn derefter rullelisten, så du kan vælge fra en filtreret liste over sider.
-   Åbn rullelisten, og klik derefter på enten overskriften **Sidens navn** øverst på listen, eller på overskriften **Sidens AOT-navn**. Der åbnes en dialogboks, hvor du kan bruge avancerede filtreringsindstillinger som f.eks. **Sidens navn begynder med**.
-   Indtast sidens fulde navn. Når du bruger denne valgmulighed, er det bedst at åbne rullelisten, og se, hvad der ellers er på listen, selvom feltbeskrivelser bliver vist.
    -   Hvis der er et enkelt nøjagtigt match, vises feltbeskrivelserne for den pågældende side.
    -   Hvis der er mere end ét nøjagtigt match, vises der ingen beskrivelser. Du skal åbne rullelisten og vælge den ønskede side.
    -   Hvis det navn, du har skrevet, er en del af navnet på en anden side, kan du se beskrivelserne for din side. Men hvis du åbner rullelisten, ser du flere sider, der indeholder navnet.

For eksempel ingen beskrivelser vises, når du skriver **optælling** i den *** Vælg side *** felt. Du åbner rullelisten og ser, at der både er to sider, der har navnet **Optælling**, og flere andre sider med ordet "Optælling" i navnet. Hvis du vælger den side, der har AOT-navnet **InventJournalCount**, vises feltbeskrivelserne til denne side. Hvis du åbner rullelisten igen, kan du nu se, at listen indeholder alle de sider, der har "InventJournalCount" nu som en del af deres AOT-navn.

## <a name="troubleshooting"></a>Fejlfinding
Dette afsnit indeholder oplysninger, der kan hjælpe dig med at foretage fejlfinding af problemer, der evt. kan opstå, når du bruger feltbeskrivelser.

### <a name="i-cant-find-a-field-description"></a>Jeg kan ikke finde en feltbeskrivelse

Vi er i gang med at tilføje beskrivelser for de mere komplekse felter. Hvis du har brug for hjælp til et bestemt felt, så fortæl os det ved at skrive en kommentar til denne wiki-artikel.

### <a name="the-field-description-isnt-helpful"></a>Feltbeskrivelsen kan ikke hjælpe mig.

Fortæl os det ved at føje en kommentar til denne wiki-artikel. Hvis du kan, bedes du beskrive de yderligere oplysninger, du har brug for.

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a>Jeg kan ikke finde et felt på siden Feltbeskrivelser

Du kan få vist alle felter på en side ved at vælge **Ja** under indstillingen **Inkludér felter uden en beskrivelse**. Klik på feltet **Vælg en side** for at kontrollere, at du har valgt den rigtige side. Hvis det navn, du har skrevet, er en del af et andet feltnavn, har du måske valgt siden med det lange navn.

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a>Jeg kan ikke finde en side på siden Feltbeskrivelser

Du kan finde oplysninger om de forskellige måder, du kan finde sider på, i afsnittet "Sådan søger du efter en side" tidligere i denne artikel. Hvis du har skrevet det nøjagtige navn på siden, vises feltbeskrivelserne vises muligvis ikke, hvis der er mere end én side med det samme navn. Klik på pilen i feltet **Vælg en side** for at åbne en filtreret liste over de sider, der er tilgængelige.

<a name="see-also"></a>Se også
--------

[Tilpasse hjælp til felter](https:/docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/user-interface/customize-field-help.md)

