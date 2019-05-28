---
title: Oversigt over standardomkostningskonvertering
description: Denne artikel giver et overblik over processer, som kan hjælpe dig med at konfigurere og køre en standardomkostningskonvertering. Trinnene skal udføres, når du har udført forberedelserne til en standardomkostningskonvertering.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 78212
ms.assetid: d601d9d5-1de3-4868-aff4-534dca01d624
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5818bcf55cd7efc2d62f7b382a85653eb8bcbad6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564640"
---
# <a name="standard-cost-conversion-overview"></a>Oversigt over standardomkostningskonvertering

[!include [banner](../includes/banner.md)]

Denne artikel giver et overblik over processer, som kan hjælpe dig med at konfigurere og køre en standardomkostningskonvertering. Trinnene skal udføres, når du har udført forberedelserne til en standardomkostningskonvertering. 

Du kan bruge siden **Standardomkostningskonverteringer** til at konvertere lagermodellen for en serie af udvalgte varer fra faktiske omkostninger til standardomkostninger. Konverteringsprocessen omfatter en forudgående lagerlukning, udførelse af flere trin i en overgangsperiode, som defineres af en startdato og en planlagt konverteringsdato, og derefter udførelse af konverteringen og en tilknyttet lagerlukning.

-   Lagerlukning før overgangsperiode – En lagerlukning repræsenterer et forudgående trin, fordi den udligner en vares åbne transaktioner ved hjælp af den gamle vurderingsmetode. I overgangsperioden kan du indtaste og bogføre baguddaterede transaktioner som f.eks. fakturaer, så du kan lukke den tidligere periode. Datoen for lagerlukning skal være én dag før overgangsperiodens startdato for at sikre en ren afslutning fra den gamle vurderingsmetode.
-   Konverteringstrin i overgangsperioden – Brug siden **Standardomkostningskonverteringer** til at oprette en konverteringspost, der også indeholder det brugerdefinerede id for en ny efterkalkulationsversion. Du skal identificere de varer, son kræver konvertering, og derefter indtaste varernes ventende standardomkostninger i den nye efterkalkulationsversion. Du skal kontrollere de valgte varer for at identificere problemer, som kan forhindre konvertering, løse problemerne og derefter foretage en ny kontrol. Når varerne har bestået kontrollerne, skal du ændre status for konverteringsposten til **Færdig**. På den planlagte konverteringsdato skal du foretage konverteringen og evt. medtage en lagerlukning. Lagerbevægelserne for en vare i overgangsperioden bogføres og værdifastsættes i henhold til den gamle lagermodel. Når konverteringsprocessen er fuldført korrekt, bliver lagerbevægelserne omvurderet til standardomkostninger.
-   Lagerlukning før konverteringen − Lagerlukningen kan medtages som en del af konverteringen på den planlagte konverteringsdato, eller den kan udføres som et separat trin inden konverteringen.

Efter vellykket udførelse af konverteringen vil hver vare have en lagermodel, der er baseret på standardomkostninger, og varens standardomkostninger vil være aktiveret. Efterfølgende lagertransaktioner værdifastsættes til varens standardomkostning. Systemet konverterer desuden varens fysiske lagertransaktioner for tilgange og afgange til standardomkostningen på konverteringsdatoen. Systemet konverterer også varens økonomiske disponible lagerbeholdning til standardomkostning og bogfører differencen i værdi som en lagerregulering. Alle transaktioner, der forekommer efter konverteringen, værdifastsættes til varens standardomkostning. Du kan ikke angive tilbagedaterede transaktioner før konverteringsdatoen, fordi en lagerlukning skal være udført én dag før konverteringsdatoen. En konvertering kan kun udføres, hvis der blev udført en lagerlukning én dag tidligere. Denne lagerlukning kan ikke annulleres.

## <a name="1-define-a-standard-cost-conversion-record-and-the-associated-costing-version"></a>1. Definer en standardomkostningskonverteringspost og den tilknyttede efterkalkulationsversion.
Brug siden **Standardomkostningskonverteringer** til at oprette en konverteringspost. Du kan kun oprette en ny konverteringspost, når de eksisterende konverteringsposter er udført. Varigheden af den planlagte overførselsperiode defineres af startdatoen for overførslen og den planlagte konverteringsdato. En planlagt overførselsperiode kan være så kort som én dag. En planlagt overførselsperiode er med til at sikre, at konverteringen har tid nok til at fuldføre alle trin. En lagerlukning skal udføres på en dato én dag før startdatoen for overførslen som et led i at sikre, at alle udligninger er udført, inden du starter konverteringsprocessen. Du kan sørge for, at ændre startdatoen for overførsel og lagerlukning er korrekt justerede ved at ændre startdatoen for overførslen til én dag efter en eksisterende lagerlukning eller ved at udføre en lagerlukning. Når du angiver en konverteringspost, angiver du også et brugerdefineret id for en ny efterkalkulationsversion, som skal indeholde standardomkostningerne for konverterede varer. Efterkalkulationsversionen oprettes automatisk, når du gemmer konverteringspostoplysningerne.

## <a name="2-review-and-change-the-new-costing-version-for-the-conversion-record"></a>2. Gennemgå og rediger den nye efterkalkulationsversion for konverteringsposten.
Den nye efterkalkulationsversion er knyttet til konverteringsposten, som efterkalkulationstypen **Konvertering** angiver. Den tilknyttede efterkalkulationsversion ligner en efterkalkulationsversion for standardomkostninger og indeholder varekostprisposterne for varer, der er knyttet til konverteringsposten. Den tilknyttede efterkalkulationsversion for en konverteringspost har følgende indstillinger, som du skal gennemse og redigere på under forskellige faner efter behov:

-   **Efterkalkulationstype:** Dette felt skal indstilles til **Standardomkostning**.
-   **Version** Id'et afspejler de oplysninger, der er angivet i konverteringsposten for efterkalkulationsversionens id.
-   **Navn:** Feltet er som standard tomt. Du skal vælge at angive et navn.
-   **Blokering:** I dette felt skal du vælge **Ingen**. Du kan angive omkostningsposter i efterkalkulationsversionen, indtil du ændrer konverteringspostens status til **Færdig**. Statusangivelsen **Færdig** angiver, at de valgte varer er blevet kontrolleret, og at ændringer i omkostningsposterne ikke bør tillades.
-   **Bloker aktivering:** I dette felt skal du vælge **Ja**. Du kan ikke manuelt aktivere en ventende omkostningspost inden for den tilknyttede efterkalkulationsversion. Aktivering forekommer, når konverteringen gennemføres.
-   **Fra dato:** Viser den planlagte konverteringsdato, der er angivet i konverteringsposten.
-   **Sted:** Lad dette felt stå tomt, så omkostningsposter kan angives for alle steder.
-   **Feltgruppen Tillad pristype:** Indstil dette felt til **Ja**, så kun kostprisposter kan angives.
-   **Reserveprincip:** Dette felt er indstillet til **Ingen**. Vælg reserveprincippet **Aktiv**, hvis du kræver omkostningsoplysninger, der er aktiveret i andre efterkalkulationsversioner. Der kræves muligvis omkostningsoplysninger om komponenter, omkostningskategorier og indirekte omkostninger for at beregne omkostningerne for færdigvarer.
-   **Reserveefterkalkulationsversion:** Lad feltet stå tomt.

Kostprisoplysninger i den tilknyttede efterkalkulationsversion kan kun vedligeholdes fra siden **Standardomkostningskonverteringer**. Du kan ikke bruge siden **Opsætning af efterkalkulationsversion** eller siden **Vedligeholdelse af efterkalkulationsversion** til at beregne omkostninger for efterkalkulationsversionen under konverteringen. Du kan dog bruge disse sider til at vedligeholde den tilknyttede efterkalkulationsversion, når du har udført konverteringen.

## <a name="3-identify-the-items-to-convert-to-standard-cost"></a>3. Identificer de varer, der skal konverteres til standardomkostninger
Brug siden **Standardomkostningskonverteringer** til at identificere de enkelte varer, der skal konverteres til standardomkostninger. Du kan tilføje flere varer ved hjælp af siden **Føj varer til standardomkostningskonverteringen**. Generelt skal du medtage alle færdigvarer i en enkelt konverteringspost for bedre at sikre, at omkostningerne beregnes korrekt.

## <a name="4-enter-or-calculate-the-pending-standard-cost-for-each-item-that-is-being-converted"></a>4. Angiv eller beregn den ventende standardomkostning for hver vare, der konverteres
Du kan bruge siden **Varepris** til at angive vendende standardomkostninger i den tilknyttede efterkalkulationsversion for indkøbte varer og overførte farer. Omkostningsposter er lokationsspecifikke, og en vares ventende omkostninger skal angives for hvert sted. Du kan bruge siden **Varepris** til at beregne ventende standardomkostninger for færdigvarer. De ventende omkostninger for en færdigvare skal beregnes for hver produktionslokation, medmindre lokationen repræsenterer en overførselslokation. I så fald skal de ventende omkostninger angives manuelt. Nogle varer kan have produktdimensioner for farve, størrelse eller variant. På siden **Standardomkostningskonverteringer** viser afkrydsningsfeltet **Brug kostpris efter variant** standardomkostningen for hver kombination af produktdimensioner. Hvis afkrydsningsfeltet ikke er markeret, skal du kun angive en ventende omkostning for varen.

## <a name="5-check-and-resolve-any-issues-for-the-items-that-are-being-converted"></a>5. Kontrollér og løs eventuelle problemer med de varer, der konverteres
Brug rapporten **Kontroller af standardomkostningskonvertering** til at identificere problemer med de varer, der konverteres. Hvis der ikke er nogen problemer med en vare, ændres varens status i konverteringsposten til **Kontrolleret**. Hvis der er problemer med en vare, skal du løse dem og derefter køre rapporten igen, indtil varens status er ændret til **Kontrolleret**. Hvis du ikke kan løse problemerne med en vare i rette tid, kan du vælge at slette varen fra konverteringsposten og derefter konvertere varen på et senere tidspunkt.

## <a name="6-change-the-status-of-the-conversion-record-to-ready"></a>6. Indstil statussen for konverteringsposten til Færdig.
Når konverteringspostens status ændres til **Færdig**, udfører systemet en endelig kontrol, inden en standardomkostningskonvertering køres. Status ændres kun til **Færdig**, hvis følgende betingelser er opfyldt:

-   Hver vare i konverteringsposten har status som **Kontrolleret**.
-   Der er blevet udført en lagerlukning på en dato, der ligger en dag før startdatoen for overførslen. Du kan sørge for, at ændre startdatoen for overførsel og lagerlukning er korrekt justerede ved at ændre startdatoen for overførslen til én dag efter en eksisterende lagerlukning eller ved at udføre en lagerlukning.

## <a name="7-back-up-the-database-before-conversion"></a>7. Sikkerhedskopier databasen før konvertering
Med sikkerhedskopien kan du gendanne databasen, hvis der opstår fejl under konverteringen.

## <a name="8-perform-the-conversion-when-the-conversion-record-has-a-ready-status"></a>8. Udfør konverteringen, når konverteringsposten har status som Færdig
Konverteringsprocessen kræver, at der er udført en lagerlukning på en dato, der ligger en dag før den planlagte konverteringsdato. Dette krav er med til at sikre, at tilbagedaterede posteringer ikke kan oprettes i overførselsperioden. Hvis der ikke er udført en lagerlukning, bliver du spurgt, om du vil udføre lukningen i forbindelse med konverteringsprocessen. Konverteringsprocessen håndterer én vare ad gangen. Det starter med de laveste varer i en produktstruktur baseret på varens laveste niveau-kode. Når en vare er konverteret, ændres dens status i konverteringsposten til **Konverteret**. Hvis konverteringsprocessen afbrydes, får varer, der ikke er blevet konverteret, status som **Kontrolleret**. Gennemførelse af konverteringsprocessen medfører følgende:

-   Konverteringspostens status ændres fra **Færdig** til **Fuldført**, og den valgte vares status ændres fra **Kontrolleret** til **Konverteret**.
-   Lagermodelgruppen for konverterede varer ændres, så den viser en ny gruppe, der har en standardomkostningslagermodel.
-   Standardomkostningerne for de konverterede varer er blevet aktiveret i den tilknyttede efterkalkulationsversion.
-   Efterkalkulationstypen for efterkalkulationsversionen ændres fra **Konvertering** til **Standardomkostning**, og efterkalkulationsversionen fungerer nu som andre efterkalkulationsversion for standardomkostninger.

## <a name="9-validate-and-reconcile-the-inventory-values-for-the-converted-items"></a>9. Valider og afstem lagerværdierne for de konverterede varer
Rapporten **Opgørelse af afvigelsesanalyse** kan du analysere revalueringen, og i rapporten **Lagerværdi** kan du se lagerværdien på en bestemt dato.

-   Analyser værdireguleringer. Du kan bruge rapporten **Opgørelse af afvigelsesanalyse** til at få vist lagerværdireguleringer for de konverterede varer. Du kan også bruge siden **Standardomkostningsposter** til at få vist transaktionerne for lagerværdireguleringer for de konverterede varer, der har lagervarer.
-   Analysér lagerværdien før startdatoen for overførslen. Du kan bruge rapporten **Lagerværdi** til at få vist lagerværdier for de konverterede varer. For Til dato for rapporten kan du bruge en dato én dag før startdatoen for overførslen.
-   Analysér lagerværdien før konverteringsdatoen. Du kan bruge rapporten **Lagerværdi** til at få vist lagerværdier for de konverterede varer. For Til dato for rapporten kan du bruge en dato, der afspejler én dag før konverteringsdatoen.
-   Analysér lagerværdien på konverteringsdatoen. Du kan bruge rapporten **Lagerværdi** til at få vist lagerværdierne på konverteringsdatoen. Både Fra dato og Til dato for rapporten skal svare til konverteringsdatoen. Udvælgelseskriterierne i rapporten skal afspejle de konverterede varer.
-   Analysér tilbagedaterede lagerbevægelser. Du kan bruge rapporten **Lagerværdi** til at få vist tilbagedaterede lagerbevægelser, der er indsat efter konverteringen. Fra dato og Til dato for rapporten skal svare til startdatoen for overførslen og konverteringsdatoen minus én dag. Udvælgelseskriterierne i rapporten skal afspejle de konverterede varer. I rapporten vises lagerbevægelser, der er sket til standardomkostningen i overførselsperioden.


<a name="additional-resources"></a>Yderligere ressourcer
--------

[Forudsætninger for en standardomkostningskonvertering](prerequisites-standard-cost-conversion.md)



