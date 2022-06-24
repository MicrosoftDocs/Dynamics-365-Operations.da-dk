---
title: Målretning af enhed, marked og geografisk placering
description: Denne artikel beskriver, hvordan du kan oprette, redigere og administrere målgrupper og mål i Microsoft Dynamics 365 Commerce Site Builder ved hjælp af oplysninger om enhed, marked og geografisk placering.
author: sushma-rao
ms.date: 02/03/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2021-07-31
ms.dyn365.ops.version: AX 10.0.21
ms.openlocfilehash: 90772fd942db30bbf4f65a87b1dca4b2aaacee1e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881651"
---
# <a name="device-market-and-geolocation-targeting"></a>Målretning af enhed, marked og geografisk placering

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du kan oprette, redigere og administrere målgrupper og mål i Microsoft Dynamics 365 Commerce Site Builder ved hjælp af oplysninger om enhed, marked og geografisk placering.

Dynamics 365 Commerce giver dig mulighed for at tilpasse variationer af dit sideindhold (kaldet *mål*) for bestemte kundegrupper (kaldet *målgrupper*) for at øge brugerengagementet og -tilfredsheden. Du kan enten oprette en målgruppe eller et mål først. En vellykket målretning kræver dog begge disse komponenter.

Du kan oprette og administrere målgrupper i Commerce Site Builder baseret på kundedata, f.eks. geografisk placering, enhedsoplysninger, logonstatus og andre dynamisk afledte oplysninger fra kunders webanmodninger. Du kan også oprette og administrere mål på e-handelsmoduler og fragmenter i Commerce Site Builder.

**Ansvarsfraskrivelse**: Du er ansvarlig for at bruge denne funktion med overholdelse af angivne standarder og alle gældende love og regulativer, herunder dem, der vedrører målretning og profilering. 

## <a name="audiences"></a>Målgrupper

En målgruppe er en gruppe af brugere, og medlemskab af gruppen bestemmes af et sæt dynamiske regler. Disse regler er simple logiktest, der køres i forhold til de oplysninger, der er tilgængelige i kundeanmodninger eller andre tilgængelige segmenter. Du kan kombinere flere regler ved hjælp af OG/ELLER-operatorer.

Commerce har indbygget understøttelse af basissegmenter som f.eks. enhedsoplysninger, status for logon, henvisninger og strengparametre for forespørgsler. Det understøtter også udvidelige segmenter via forbindelser til tredjepartsleverandører.

### <a name="basic-segments"></a>Basissegmenter

Følgende segmenter er som standard tilgængelige og kan medtages i definitioner af målgrupper:

- **Status for login** – Test, om en bruger er godkendt.
- **Enhedsplatform** – Test for følgende enhedstyper:

    - Mobil
    - Desktop
    - Tablet
    - Anden

- **Enheds-OS** – Test for følgende operativsystemer:

    - Windows
    - Linux
    - iOS
    - Android, Andet

- **Parametre for forespørgselsstreng** – Test for eksistensen af et nøgleværdipar i en forespørgselsstrengparameter i en URL-adresse til anmodningen. For URL-adressen `www.fabrikam.com/en-us/request?promo=true` kan der f.eks. skrives en regel, som tester, om parameteren **promo** har værdien **sand**.
- **Cookie** – Test for en cookieværdi, der er angivet for domænet i URL-adressen til anmodningen. En anmodning om Fabrikam.com. indeholder f.eks. en cookie, der har navnet **CustomLayout** og værdien **1**. I testen af cookie kontrolleres det, om der findes en cookie, men der oprettes ikke eksplicit en cookie. I det forrige eksempel skal JavaScript i forvejen have indstillet **CustomLayout** som cookie fra et andet modul eller en anden forretningsproces.

    > [!NOTE]
    > Sørg for, at din brug af cookies overholder den gældende lovgivning.

- **Henvisende** – Hvis en bruger følger et link for at anmode om siden, er den henvisende URL-adressen for den side, der er vært for linket.

### <a name="extensible-segments"></a>Segmenter, der kan udvides

Ved hjælp af Commerce kan du udvide listen over tilgængelige segmenter ved at forbinde segmenteringsudbydere fra tredjepart. En segmenteringsudbyder vil beskrive de tilgængelige segmenttyper. Du kan finde flere oplysninger om, hvordan der oprettes forbindelse til en geografisk placering eller en segmenteringsudbyder, under [Konfigurere og aktivere connectorer](e-commerce-extensibility/connectors.md).

> [!NOTE]
> - Hvis en ekstern udbyder er aktiveret, kan den oprette forbindelse til en tjeneste, der har uforudsigelig ydeevne. Hvis en bruger anmoder om en side, der omfatter målretning, og siden refererer til en målgruppe, der kontrollerer en tredjeparts segmentudbyder, kan du sikre en bedre brugeroplevelse. Standardversionen af siden vises.
> - Brugeren skal give tilladelse til cookies. Brugerens browser anmoder derefter alle segmenter fra relevante udbydere, og resultaterne placeres i en cookie, som returneres til brugeren. Efterfølgende anmodninger på siden vil bruge disse oplysninger til at levere målrettet indhold til brugeren. Yderligere oplysninger om overholdelse af angivne standarder for cookies finder du i [Cookieoverholdelse](cookie-compliance.md).

**Ansvarsfraskrivelse:** Hvis du aktiverer denne funktion, deles dine data med de tredjepartssystemer, du vælger. Du styrer, hvilke data du eventuelt giver til tredjepart. Du forstår, at tredjeparts standarder for håndtering af data og overholdelse af angivne standarder kan afvige fra standarderne for Microsoft Dynamics 365 Commerce. Beskyttelse af personlige oplysninger er vigtig for Microsoft. Du kan få mere at vide ved at læse vores [Erklæring om beskyttelse af personlige oplysninger og cookies](https://privacy.microsoft.com/privacystatement).

### <a name="create-an-audience-in-site-builder"></a>Oprette en målgruppe i Site Builder

Udfør følgende trin for at oprette en målgruppe i Commerce-webstedsgenerator.

1. Vælg **Målgrupper** i navigationsruden til venstre.
1. Vælg **Ny**.
1. Angiv et navn til målgruppen. Du kan også vælge at tilføje tags og en beskrivelse.
1. Vælg **Opret** og derefter **Tilføj en ny regelblok**. En regelblok er en samling af regler, der er forbundet med OG-betingelser. Du kan også oprette flere regelbloker, der har ELLER-betingelser mellem dem.
1. Vælg en datakilde til segmenter, og angiv derefter segmentnavn, operator og værdier. Du kan oprette og slette flere regler i en regelblok, eller du kan oprette og slette hele regelblokke. Du kan også flytte regelblokke op eller ned efter behov.

    > [!NOTE]
    > Du kan have op til 100 værdier på en liste, og hvert listepunkt kan indeholde op til 50 tegn.

1. Når du er tilfreds med målgruppekonfigurationen, skal du vælge **Afslut redigering**. Du kan derefter vælge **Publicer** for at gøre målgruppen tilgængelig for brug i et live mål. Du kan også publicere målgruppen sammen med målet. 

Hvis du vil redigere en målgruppe, skal du vælge linket til den under fanen **Målgrupper** og derefter vælge **Rediger** i den målgruppeeditor, der vises. Hvis du vil se listen over mål og sider, der refererer til en målgruppe, skal du vælge målgruppen på listevisningen og derefter vælge **Vis tildelinger**. Hvis du vil slette en målgruppe i målgruppelistevisningen eller målgruppeeditoren, skal du fjerne publiceringen af den, hvis den allerede er publiceret, og derefter vælge **Slet** på kommandolinjen.

> [!NOTE]
> Målgrupper er et begreb på webstedsniveau i Commerce-webstedsgeneratoren. Du kan dele den samme målgruppe på tværs af flere mål.

### <a name="rename-an-audience-in-site-builder"></a>Omdøbe en målgruppe i webstedsgenerator

Udfør følgende trin for at omdøbe en eksisterende målgruppe i Commerce-webstedsgenerator.

1. Vælg **Målgrupper** i navigationsruden til venstre.
1. Vælg navnet på det målgruppesegment, du vil omdøbe.
1. Vælg **Rediger** for at begynde at redigere målgruppen.
1. Vælg blyantssymbolet ud for målgruppenavnet i ruden med egenskaber for målgruppe.
1. Rediger målgruppenavnet efter behov.
1. Markér afkrydsningsfeltet for at bekræfte navneændringen.
1. Vælg **Afslut redigering**.

## <a name="targets"></a>Mål

Et mål er den brugeroplevelse, der vises til medlemmer af en eller flere valgte målgrupper. Det kan omfatte variationer af et eller flere moduler på en side eller i et fragment. 

Du kan definere en tidsplan for målene for at angive, hvor længe de skal være aktive. Bemærk, at denne handling er uafhængig af den handling, der bruges til at planlægge en publiceret gruppe, som bestemmer, hvornår en samling af indhold vil blive publiceret. Du kan se en forhåndsversion af dine mål for at se, hvordan de vil se ud for medlemmer af udvalgte målgrupper. Derudover kan du prioritere målene for at angive, hvilket mål der skal vises i tilfælde af en konflikt.

### <a name="create-a-target"></a>Oprette et mål

Hvis du vil oprette en mål-shell for sidemoduler i Commerce-webstedsgeneratoren, skal du følge disse trin.

1. Vælg **Sider** i navigationsruden til venstre. Vælg derefter hyperlinket til den side, der indeholder de moduler, du vil målrette.
1. Vælg **Rediger** for at tjekke siden ud til redigering.
1. I menuen **Mål** skal du vælge **Nyt mål** for at oprette en ny mål-shell. Du kan oprette flere mål på en side efter behov.
1. Angiv et navn og en beskrivelse for målet, og vælg derefter **Næste**.
1. Vælg **Tilføj** for at inkludere de målgrupper, der kan se det målrettede indhold, eller udelukke målgrupper. Vælg derefter **Næste**.

    > [!NOTE]
    > Tildeling af målgrupper er et valgfrit trin under oprettelse af mål. Før du publicerer målet, skal du dog inkludere mindst én målgruppe for at sikre, at de ønskede brugergrupper kan se det målrettede indhold.

1. Definer tidsvinduet for visningen af målet ved at vælge tidszone samt start- og slutdatoer og -klokkeslæt. Du kan indstille målet, så det altid kan se i vinduet, eller du kan vælge bestemte dage og tidspunkter. Vælg **Næste**, når du er færdig.

    > [!NOTE]
    > De tider og tidszoner, du angiver, er globale. Hvis du vil målrette mod forskellige lokationer på forskellige tidspunkter eller i forskellige tidszoner, skal du oprette forskellige mål og definere den ønskede tidsplan for hver lokation.

1. Gennemse detaljerne, og når alt ser korrekt ud, skal du vælge **Opret målerfaring** og derefter **Gå til mål**. Mål-shell oprettes. Du kan nu føje moduler til den.
1. Vælg det modul, der skal målrettes, vælg ellipsen (**...**), og vælg derefter **Føj til det aktuelle mål**. Når du målretter mod et overordnet modul, bliver alle dets underordnede en del af det pågældende mål. De moduler, der er målet, er markeret med grønt.
1. Foretag de nødvendige indholdsopdateringer af det modul, der er målet, og føj flere moduler til målet efter behov. Vælg **Gem** for at gemme alle ændringerne.
1. Før du publicerer målet, skal du sørge for at vælge **Forhåndsvisning** på kommandolinjen for at gennemse det. Du kan derefter vælge en af følgende indstillinger:

    - **Basisforhåndsversion** – Vælg denne indstilling for kun at få vist den valgte variant på forhånd (standardside eller mål) uden tilknyttede målgrupper.
    - **Avanceret forhåndsvisning** – Vælg denne indstilling, hvis du har flere mål på en side og vil se forhåndsversionen af dem som en bruger, der tilhører et udvalgt sæt målgrupper, eller på bestemt dato/klokkeslæt. Vælg **Næste** for at vælge på en liste over relevante målgrupper. Du kan også fjerne filteret for at vælge mellem alle målgrupper.

1. Når du er tilfreds med målkonfigurationen, skal du publicere siden for at gøre målet live. Vælg **Publicer** for at gøre målet live med det samme. Du kan også bruge en publiceringsgruppe til at planlægge, hvornår siden går live. Du kan finde oplysninger om publiceringsgrupper under [Arbejde med publiceringsgrupper](publish-groups.md).

Du kan også målrette fragmenter. Proceduren er lignende. I trin 1 skal du dog vælge **Fragmenter** i stedet for **Sider** i venstre navigationsrude.

> [!NOTE]
> Du kan undgå negativ påvirkning af målepunkter ved enten at have eksperimenter eller mål på en side eller i et fragment. Der kan ikke både et eksperiment og mål.

### <a name="manage-targets"></a>Administrer mål

Hvis du vil redigere, dublere eller slette mål, skal du gå til standardsiden eller -fragmentet og følge disse trin.

1. Vælg **Mål** i rullemenuen, og vælg derefter **Administrer mål**.
1. Vælg et mål, der skal redigeres, dubleres eller slettes.
1. Hvis du har flere mål i samme modul, eller hvis flere mål har modstridende tidsplaner, skal du vælge **Prioriter mål** for at angive den rækkefølge, de skal vises i. Hvis du tilføjer mere end ét mål på en side eller i et fragment, vises knappen **Prioriter mål** også på beskedlinjen for at minde dig om at prioritere målene. Hvis der ikke er angivet nogen prioritet, vælges det nyeste mål som standard.

### <a name="localize-targets"></a>Lokalisere mål

Mål på sider og i fragmenter medtages automatisk, når XLIFF-filer eksporteres og importeres til lokaliseringsformål. Men hvis det ikke er nødvendigt at bruge landestandarder, kan du slette målene for dem, når de lokaliserede XLIFF-filer er importeret.

> [!NOTE]
> Mål administreres pr. kanal og landestandard. Ændringer, du foretager af mål i én kanal eller landestandard overføres ikke automatisk til andre kanaler eller landestandarder.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
