---
title: Operations-ressourcer
description: "Operationsressourcer udfører aktiviteterne i et projekt eller en produktionsproces. De kan være af forskellige typer og kan have forskellige egenskaber."
author: sorenva
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OpResLifecycleManagementWorkspace, WrkCtrCapability
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c4018632e5e20470948ee59e4bb2a1cab905d829
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="operations-resources"></a>Operations-ressourcer

[!include [banner](../includes/banner.md)]

Operationsressourcer udfører aktiviteterne i et projekt eller en produktionsproces. De kan være af forskellige typer og kan have forskellige egenskaber. 

<a name="operations-resources"></a>Operations-ressourcer
--------------------

Ved operationsressourcer forstås maskiner, værktøjer, arbejdere, faciliteter, fysiske områder eller leverandører, der udfører aktiviteterne i et projekt eller en produktionsproces. De kan være af forskellige typer og kan have forskellige egenskaber.

-   **Leverandør** – En ekstern ressource, der udfører projektaktiviteter eller produktionsoperationer. Et eksempel er en underleverandør. Ved at knytte leverandørressourcer til en leverandørkonto kan du generere køb for underleverandører på baggrund af styklistelinjerne eller produktionslinjerne.
-   **Personale** – En projekt- eller produktionsarbejder, der udfører en aktivitet, enten alene eller ved at betjene et værktøj eller en maskine. Hvis du bruger funktionen Personale, kan du knytte personale til en arbejder. Planlægningsprogrammet kan derefter tildele ressourcerne baseret på de kompetencer, der er defineret for den tilsvarende arbejder.
-   **Maskine** – En maskine eller andet produktionsudstyr, der skal bruges i produktionen.
-   **Værktøj** – Et instrument eller en enhed, der normalt bruges sammen med en anden ressource til at udføre en aktivitet i et projekt eller i produktionen.
-   **Lokalitet** – En fysisk lokalitet af en bestemt størrelse, der kræves for at udføre en aktivitet. Et eksempel er et samlingsområde.
-   **Facilitet** – En bygning eller fast struktur, der er nødvendig for at udføre en aktivitet.

## <a name="calendars"></a>Kalendere
Der kan tildeles en kalender til en operationsressource, som beskriver kapacitet (i timer) for den pågældende ressource. Arbejdstider for operationsressourcen bestemmes af den kalender, der er tildelt til den ressourcegruppe, som operationsressourcen er en del af. Du kan også angive en ikrafttrædelsesdato og en udløbsdato for den tildelte kalender. Du kan derefter tildele mere end én kalender til en operationsressource. Men datoerne for de tildelte kalendere må ikke overlappe, og operationsressourcen kan kun tildeles én kalender ad gangen. **Bemærk!** Hvis der ikke findes gældende arbejdskalendere til en ressourcegruppe (f.eks. hvis den sidst tildelte kalender eller den eneste tildelte kalender er udløbet), har du ikke længere adgang til de operationsressourcer, der er knyttet til ressourcegruppen til produktionsplanlægning og grovplanlægning. Du kan også tildele en kalender til en ressourcegruppe for at angive arbejdstider for både ressourcegruppen og alle de operationsressourcer, der er knyttet til ressourcegruppen. Kapaciteten i ressourcegruppen beregnes som summen af kapacitet for de enkelte operationsressourcer, der er tildelt denne ressourcegruppe. Den kalender, der er tildelt til en ressourcegruppe, kan ændres med tiden.

## <a name="resource-capabilities"></a>Ressourceegenskaber
En funktion er en operationsressource evne til at udføre en bestemt aktivitet. Du kan tildele en eller flere egenskaber til en operationsressource. Planlægningsprogrammet allokerer derefter ressourcer ved at sammenligne ressourcekravene for hver enkelt aktivitet med funktionerne i de tilgængelige operationsressourcer. Egenskaber kan tildeles til alle typer operationsressourcer (**værktøj**, **leverandør**, **maskine**, **personale**, **lokalitet** eller **facilitet**). Hvis du vil tildele egenskaber til operationsressourcer i en begrænset periode, skal du definere en startdato og en udløbsdato for egenskabstildelingen. Du kan finde flere oplysninger under [Ressourceegenskaber](resource-capabilities.md).

## <a name="resource-groups"></a>Ressourcegrupper
En ressourcegruppe er et sæt operationsressourcer, der repræsenterer den granularitet, som du vil planlægge ressourcer med, når du bruger grovplanlægningsmetoden. Derfor svarer ressourcegrupper normalt til den fysiske organisation af arbejdsceller, som markeres af gule streger på produktionen. Ressourcegruppen definerer rammerne for stedet, produktionsenheden og lagerstedet for de operationsressourcer, der er tildelt gruppen. Når du tildeler en operationsressource til en ressourcegruppe, kan ressourcen planlægges på det sted, hvor ressourcegruppen er placeret. Du behøver ikke at tildele de operationsressourcer, som du opretter for en ressourcegruppe. Men en operationsressource skal tildeles til en ressourcegruppe, før ressourcen kan planlægges til at udføre arbejde. En operationsressource kan tildeles til en ressourcegruppe i en begrænset periode. Du kan også tildele en operationsressource til flere ressourcegrupper, så du derefter kan dele ressourcen på tværs af steder. Men ikrafttrædelsesdatoerne og udløbsdatoerne må ikke overlappe. Du kan med andre ord ikke tildele en operationsressource til to ressourcegrupper samtidigt. Ændringer i tildelinger af ressourcegrupper gælder kun for nye ressourceallokeringer. Kapacitetsreservationer for job, operationer og timebudgetter for projekter, der er allerede planlagt, påvirkes ikke. **Bemærk!** Når du tildeler operationsressourcer af typen **Leverandør** til en ressourcegruppe, skal alle de operationsressourcer, der er tildelt til denne ressourcegruppe, være af typen **Leverandør** og være knyttet til samme leverandørkonto.

## <a name="production-units"></a>Produktionsenheder
En produktionsenhed er en administrativ enhed, der består af en samling ressourcegrupper. En produktionsenhed kan indeholde flere ressourcegrupper, men der kan kun tildeles en ressourcegruppe til én produktionsenhed. En produktionsenhed afspejler den fysiske opbygning af produktionsressourcer og har ingen indflydelse på posteringer, eller hvordan de behandles. Du skal knytte den valgte produktionsenhed til en bestemt lokation. Du kan også knytte et pluklagersted og et opbevaringslagersted til en produktionsenhed. Du kan bruge en produktionsenhed til at konsolidere og filtrere produktionsrelaterede oplysninger. En shop floor manager kan f.eks. få vist en praktisk oversigt over den udestående arbejdsbyrde og den tilgængelige kapacitet for en bestemt produktionsenhed. Du kan ændre den produktionsenhed, der er knyttet til en ressourcegruppe. Du kan også slette en produktionsenhed. Men disse ændringer i produktionsenheden træder først i kraft for nye ordrer, der oprettes, efter at der er udført en behovsplanlægning. Hvis du vil anvende ændringen i produktionsenheden på eksisterende ordrer, skal du foretage denne ændring manuelt.

## <a name="resource-scheduling"></a>Ressourceplanlægning
Operationsressourcer tildeles til aktiviteter, når et projekt eller en produktionen planlægges. Der findes to metoder til planlægning: grovplanlægning og finplanlægning. Når du bruger grovplanlægning, planlægges hver operation eller projektaktivitet for den ressourcegruppe, der indeholder operationsressourcer, som opfylder de ressourcekrav, der er angivet for operationen. Hvis der skal bruges en bestemt operationsressource for handlingen, reserverer grovplanlægningen kun kapacitet for en bestemt operationsressource i gruppen. Finplanlægning er en mere detaljeret form for planlægning end grovplanlægning. I finplanlægning opbrydes hver enkelt operation i individuelle opgaver eller job. Disse job tildeles derefter til de operationsressourcer, der skal udføre dem. Planlægningen reserverer kapacitet på ressourcegrupperne på basis af de operationstider, der er defineret for produktionsruten eller projektaktiviteter. Hvis du arbejder med kapacitetsbegrænsning, afhænger tidsplanen af tilgængeligheden af de operationsressourcer, der skal bruges til at fuldføre aktiviteten. I forbindelse med grovplanlægning er kapaciteten i ressourcegruppen summen af den tilgængelige kapacitet for de operationsressourcer, der er medlem af den pågældende gruppe. Kapacitetsreservationer, der allerede findes for operationsressourcerne, betragtes som ikke-tilgængelig kapacitet. Hvis der ikke er nok tilgængelig kapacitet til produktion, kan produktionsordrer udskydes eller endda stoppes. På siden **Ressourcer** kan du definere flere egenskaber, der styrer, hvordan kapacitetsreservationer foretages:

-   **Kapacitet** – Angiv operationsressourcens kapacitet pr. time i måleenheden for kapaciteten.
-   **Batchkapacitet** – Angiv det maksimale antal styk, operationsressourcen kan behandle pr. kørsel.
-   **Effektivitetsprocent** – Angiv den effektivitet, du forventer af operationsressourcen. Effektivitetsprocenten justerer operationsressourcens gennemløb og påvirker den tid, der er afsat til ressourcen. Leveringstider for de operationer, der bruger operationsressourcen, justeres også i overensstemmelse med dette. Her er formlen, der bruges til beregningen: Planlægningstid = tid × 100 ÷ effektivitetsprocent. I formlen omfatter *Tid* både procestid og opstillingstid.
-   **Grovplanlægningsprocent** – Angiv den maksimale procent af kapaciteten af den operationsressource, som du vil bruge til grovplanlægning. For at give kapacitetsfleksibilitet ved finplanlægningen skal du angive denne procentdel til mindre end 100 procent.
-   **Kapacitetsbegrænsning** – Angiv denne indstilling til **Ja**, hvis operationsressourcen skal planlægges ud fra den faktiske kapacitet, der er tilgængelig, og om der skal tages hensyn til eksisterende kapacitetsreservationer. Hvis denne indstilling er angivet til **Nej**, antages operationsressourcen at have ubegrænset kapacitet, og ressourcen kan derfor være overbooket.
-   **Egenskabsbegrænsning** – Angiv denne indstilling til **Ja**, hvis du ønsker, at operationsressourcen skal planlægges ud fra den faktiske kapacitet, der er tilgængelig i forbindelse med de nødvendige planlægningsegenskaber for arbejdstider.
-   **Eksklusiv** – Angiv denne indstilling til **Ja**, hvis operationsressourcen ikke skal være tilgængelig til et andet job eller en anden operation, før den aktuelle produktion er fuldført. I dette tilfælde kan operationsressourcen ikke bruges, selvom der er huller i ressourcens procestid.
-   **Flaskehalsressource** – Definer operationsressourcen som en flaskehalsressource. En flaskehalsressource planlægges ved hjælp af kapacitetsbegrænsning, når indstillingerne **Kapacitetsbegrænsning** og **Planlægning for flaskehals** på siden **Behovsplaner** er markeret.

Hvis du vil planlægge flere operationsressourcer på samme, der f.eks. skal udføre en handling i produktionen, skal du angive kravene til de forskellige ressourcer ved hjælp af primære og sekundære operationer. Derefter kan du også reservere flere operationsressourcer, der har forskellig kapacitet. Den operationsressource, der er planlagt til den primære operation, bestemmer varighed af aktiviteten.

## <a name="lean-work-cells"></a>Lean arbejdsceller
Du kan angive, at en ressourcegruppe er en lean arbejdscelle. Derefter kan ressourcegruppen blive en del af et produktionsflow. Ved at angive en ressourcegruppe som en lean arbejdscelle kan du også forhindre, at ressourcegruppen og tilknyttede operationsressourcer knyttes til operationerne i en produktionsordre eller et timebudget for projektet. For hver ressourcegruppe, der fungerer som en lean arbejdscelle, skal du angive følgende oplysninger:

-   **Kalender** – Arbejdskalenderen for den arbejdscelle, som skal have egenskaben for en standardarbejdsdag.
-   **Indlagringssted og lokalitet** – Den standardlokalitet, der bruges til at plukke materiale til en aktivitet.
-   **Udlagringssted og lokalitet** – Den standardplacering, hvor alt output fra arbejdscellen placeres.
-   **Kørselsomkostningsart** – Denne kategori skal være defineret for arbejdscellen, hvis direkte arbejdsløn spores i efterkalkulationer.

Når en ressourcegruppe bruges som en lean arbejdscelle, er kapaciteten for arbejdscellen angivet direkte på ressourcegruppen. Du behøver derfor ikke at tildele operationsressourcerne til ressourcegruppen. Kun når arbejdscellen styres af en underleverandør, skal der tildeles en operationsressource af typen **Leverandør** til arbejdscellen. Hvis du tildeler en operationsressource til en ressourcegruppe, der er markeret som en arbejdscelle, påvirkes kapaciteten for arbejdscellen ikke.

## <a name="costing-resources"></a>Efterkalkulerede ressourcer
Når du definerer en aktivitet som en ruteoperation eller timebudget for et projekt, kan du angive kravene til en bestemt operationsressource eller ressourcegruppe. Men du kan også angive krav til en operationsressource af en bestemt type eller en operationsressource, der har en bestemt funktion eller kompetence. Derfor sker den faktiske ressourcetildeling først, når aktiviteten planlægges, og kapaciteten reserveres. På en ruteoperation kan du derfor angive, at forkalkulation og styklisteberegning skal baseres på en bestemt operationsressource. Denne operationsressource omtales som efterkalkuleret ressource. Du kan også overføre omkostningsarter og operationstider fra den efterkalkulerede ressource til aktiviteten. Når operationen planlægges, bruges forkalkulation og styklisteberegning ved hjælp af den operationsressource, der faktisk er blevet planlagt.




