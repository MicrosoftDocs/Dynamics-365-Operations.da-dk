---
title: Lagerkladder
description: "I denne artikel beskrives det, hvordan du kan bruge lagerkladder til at bogføre forskellige typer fysiske lagertransaktioner."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: c64ba9e081ab4224556af86ec855ebf508853454
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-journals"></a>Lagerkladder

I denne artikel beskrives det, hvordan du kan bruge lagerkladder til at bogføre forskellige typer fysiske lagertransaktioner. 

Lagerkladder i Microsoft Dynamics 365 for Operations bruges til at bogføre fysiske lagertransaktioner af forskellige typer, som bogføring af afgange og tilgange, lagerbevægelser, oprettelse af styklister og afstemning af det fysiske lager. Alle disse lagerkladder bruges på samme måde, men de er opdelt i forskellige typer.

## <a name="types-of-inventory-journals"></a>Typer af lagerkladder
Du kan vælge mellem følgende lagerkladdetyper:

-   Flytning
-   Lagerregulering
-   Flytning
-   Stykliste
-   Varemodtagelse
-   Produktionsindlagring
-   Optælling
-   Mærkatoptælling

### <a name="movement"></a>Flytning

Når du bruger en lagerbevægelseskladde, kan du føje omkostninger til et element, når du tilføjer lager, men du skal manuelt tildele de ekstra omkostninger til en bestemt finanskonto ved at angive en modkonto i Finans, når du opretter en kladde. Denne lagerkladdetype er nyttig, hvis du vil bogføre en udgift for en vare mod en anden afdeling, eller hvis du vil fjerne varer fra lageret til udgiftsformål.

### <a name="inventory-adjustment"></a>Lagerregulering

Når du bruger en lagerreguleringskladde, kan du føje omkostninger til en vare, når du tilføjer lager. De ekstra omkostninger bogføres automatisk på en bestemt finanskonto, baseret på opsætningen af posteringsprofilen for varegruppen. Du kan bruge denne lagerkladdetype til at opdatere gevinst og tab til lagerantal, når varen bør holde sin standardmodkonto til finansmodulet. Når du bogfører en lagerjusteringskladde, bogføres en lagertilgang eller -afgang, lagerniveauet og -værdierne ændres, og der oprettes finansposteringer.

### <a name="transfer"></a>Flytning

Du kan bruge overførselskladder for at overflytte varer mellem lokationer til oplagring, partier eller produktvarianter uden at tilknytte eventuelle omkostninger. Du kan f.eks. overføre varer fra et lagersted til et andet lagersted i samme firma. Når du bruger en overførselskladde, skal du angive lagerdimensionerne "fra" og "til" (for eksempel for lokation og lagersted). Den disponible lagerbeholdning af de definerede lagerdimensioner ændres herefter. Lageroverførsler afspejler omgående flytning af materialer. Lagersporing i transit spores ikke. Hvis lageret i transit skal spores, skal du i stedet bruge en overflytningsordre. Når du bogfører en overførselskladde, oprettes der to lagerposteringer for hver kladdelinje:

-   En lagerafgang på lokationen "fra"
-   En lagertilgang på lokationen "til"

### <a name="bom"></a>Stykliste

Når du færdigmelder en stykliste, kan du oprette en styklistekladde. Du kan bogføre styklistekladden direkte ved hjælp af en styklistekladde. Denne bogføring opretter en lagertilgang for produktet sammen med en tilhørende stykliste og en lagerafgang for de produkter, der indgår i styklisten. Denne lagerkladdetype er nyttig i simple eller store produktionsscenarier, hvor ruter ikke er nødvendige.

### <a name="item-arrival"></a>Varemodtagelse

Du kan bruge varemodtagelseskladden til at registrere modtagelsen af varer (f.eks, fra indkøbsordrer). En varemodtagelseskladde kan oprettes som en del af modtagelsesstyring fra siden **Modtagelsesoversigt**, eller du kan manuelt oprette en kladdepostering fra siden **Varemodtagelse**. Hvis du aktiverer kladdenavnet for varemodtagelse for at kontrollere for plukpladser, søger Dynamics 365 for Operations efter et sted til modtagede varer, og hvis der er plads, genereres der automatisk lokationsdestinationer til indgående varer.

### <a name="production-input"></a>Produktionsindlagring

Produktionsindlagringskladder fungerer som varemodtagelseskladder, men bruges til produktionsordrer.

### <a name="counting"></a>Optælling

Med optællingskladder kan du rette den aktuelle disponible lagerbeholdning, der er registreret for varer eller for grupper af varer, og derefter bogføre det faktiske fysiske antal, så du kan foretage justeringer, der er nødvendige for at afstemme forskelle. Du kan knytte optællingspolitikker til optælling af grupper for at hjælpe gruppevarer, der har forskellige karakteristika, så disse elementer kan være inkluderet i en optællingskladde. Du kan f.eks. oprette optællingsgrupper for at tælle varer, der har en bestemt frekvens, eller for at tælle varer, når materiel falder til et bestemt niveau. Finde oplysninger om, hvordan du definerer optælling af grupper, i [Definer lageroptælling processer (opgave guide)](http://ax.help.dynamics.com/en/wiki/define-inventory-counting-processes/).

### <a name="tag-counting"></a>Mærkatoptælling

Mærkatoptællingskladder bruges til at tildele et nummereret mærkat til et antal parti. Mærkatet skal indeholde et mærkatnummer, varenummer og antal varer. For at sikre, at et mærkat kun bruges én gang, og at alle mærkater anvendes, skal hvert varenummer have et unikt sæt af mærkater, der har sin egen nummerserie. Tre statusværdier kan indstilles for hvert mærkat:

-   **Anvendt** – Varenummeret er optalt for dette mærkat.
-   **Afvist** – Varenummeret er afvist for dette mærkat.
-   **Mangler** – Varenummeret mangler for dette mærkat.

Når du bogfører en mærkatoptællingskladde, oprettes en ny optællingskladde på basis af mærkatoptællingskladdelinjerne. Du kan få flere oplysninger om mærkatoptælling i [Lagermærkatoptælling](inventory-tag-counting.md).

## <a name="working-with-journals"></a>Arbejde med kladder
Der er kun adgang til en kladde for en bruger ad gangen. Hvis flere brugere skal have adgang til kladderne på samme tid for at oprette kladdelinjerne, skal disse brugere vælge kladder, der ikke bruges i øjeblikket, for at undgå overskrivning af oplysninger. I situationer, hvor flere afdelinger anvender den samme kladdetype, er det nyttigt at oprette flere kladdenavne (for eksempel en pr. afdeling). Det kan også være nyttigt at opdele kladder, så hver posteringsrutine angives i sin egen entydige lagerkladde. Til posteringsrutiner, der er tilknyttet lagertransaktioner, skal du oprette en kladde til periodiske lagerreguleringer og en anden til lageroptællinger.

## <a name="posting-journal-lines"></a>Bogføre kladdelinjer
Du kan bogføre kladdelinjer, du opretter til enhver tid, indtil du har låst en vare fra flere transaktioner. De data, du indtaster i en kladde, forbliver i den pågældende kladde, selv hvis du lukker kladden uden at bogføre linjerne.


