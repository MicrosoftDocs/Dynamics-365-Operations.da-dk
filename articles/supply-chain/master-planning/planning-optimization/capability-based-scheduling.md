---
title: Planlægning med ressourcevalg baseret på egenskab
description: Denne artikel beskriver ressourcevalg under planlægning af ubegrænset kapacitet, når du angiver egenskaber som ressourcekrav til en operation.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd, WrkCtrTable, WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 176f40ad8cd1aa1831bbe50c0ebd91ec0cc3bc89
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739892"
---
# <a name="scheduling-with-resource-selection-based-on-capability"></a>Planlægning med ressourcevalg baseret på egenskab

[!include [banner](../../includes/banner.md)]

Ved at angive ressourcekrav til en operation i en produktionsrute definerer du, hvad der kræves for at udføre operationen. En operation kan f.eks. kræve en bestemt ressource eller en ressourcegruppe eller en kombination af færdigheder eller egenskaber. Denne artikel beskriver ressourcevalg under planlægning af ubegrænset kapacitet, når du angiver egenskaber som ressourcekrav til en operation.

## <a name="turn-the-capability-based-scheduling-feature-on-or-off"></a>Aktivere eller deaktivere funktionen til egenskabsbaseret planlægning

Før du kan bruge denne funktion, skal den være aktiveret i dit system. Fra og med Supply Chain Management version 10.0.29 er funktionen som standard aktiveret. Administratorer kan aktivere eller deaktivere denne funktion ved at søge efter funktionen *Uendelig kapacitetsplanlægning til planlægningsoptimering* i arbejdsområdet [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Yderligere oplysninger finder du under [Planlægning med ubegrænset kapacitet](infinite-capacity-planning.md).

## <a name="capability-based-scheduling"></a>Egenskabsbaseret planlægning

En funktion er en operationsressources evne til at udføre en bestemt aktivitet. En enkelt operationsressource kan have tilknyttet mere end en egenskab, og en enkelt egenskab kan have tilknyttet mere end en ressource. Egenskaber kan tildeles til alle typer ressourcer som f.eks. værktøjer, leverandører, maskiner, personale, lokalitet eller facilitet.

Når du angiver egenskaber som ressourcekrav, kan du vente med at fordele ressourcer, indtil ordrerne planlægges. I stedet for at tildele bestemte ressourcer eller ressourcegrupper til en ruteoperation, kan du definere de egenskaber, der kræves til hver ruteoperation. Under planlægningen matcher systemet de påkrævede egenskaber med de egenskaber, der er defineret for ressourcerne. Systemet vælger kun ressourcer, der opfylder kravene.

Hvis du vil tildele egenskaber til en operationsressource, skal du bruge oversigtspanelet **Egenskaber** på siden **Ressourcer**. Hvis du vil tildele ressourcer til en egenskab, skal du bruge oversigtspanelet **Ressourcer** på siden **Ressourceegenskaber**. Begge sider er tilgængelige under **Produktionsstyring \> Konfiguration \> Ressourcer** i navigationsruden. Begge oversigtspaneler indeholder et gitter, der viser de ressourcer, der er tilknyttet en valgt ressource eller egenskab. Begge oversigtspaneler indeholder også en værktøjslinje, som du kan bruge til at tilføje, fjerne og redigere rækker i gitteret. Gitteret indeholder følgende kolonner:

- **Ressource** eller **Egenskab** – Vælg den ressource eller egenskab, der tildeles af rækken.
- **Beskrivelse** – Angiv en kort beskrivelse af ressourcen eller egenskaben.
- **Gyldig fra** – Angiv den første dato, hvor ressourcen eller egenskabstildelingen gælder. Under planlægning vil systemet ikke bruge en ressource eller egenskab, der har en udløbet egenskabstildeling, heller ikke hvis ressourcen ellers opfylder kravene.
- **Udløb** – Angiv den sidste dato, hvor ressourcen eller egenskabstildelingen gælder. Under planlægning vil systemet ikke bruge en ressource eller egenskab, der har en udløbet egenskabstildeling, heller ikke hvis ressourcen ellers opfylder kravene.
- **Niveau** – Angiv det færdighedsniveau, ressourcen skal have for egenskaben. Hvis du derefter angiver en værdi af **Minimumsniveau, der kræves** for ressourcen eller egenskabskravet, tager planlægningsprogrammet højde for færdighedsniveauet ved valg af ressource. Systemet vælger derefter kun ressourcer, der har den nødvendige egenskab på et niveau, der er lig med eller overstiger minimumsniveauet, der er angivet i kildeforudsætningen.
- **Prioritet** – Dette felt er endnu ikke understøttet af Planlægningsoptimering. Hvis du bruger det udfasede varedisponeringsprogram, kan du dog bruge feltet **Prioritet** i ressource- eller egenskabstildelingen til at definere ressourceprioriteten. Hvis *Prioritet* er valgt i feltet **Valg af primær ressource** på siden **Planlægningsparametre** side, så vælger systemet først den ressource, der har den højeste prioritet (dvs. den laveste numeriske værdi i feltet **Prioritet**) under planlægning.

## <a name="example"></a>Eksempel

Dette eksempel viser, hvordan planlægningsprogrammet vælger ressourcer baseret på egenskab.

En produktionsrute har fem operationer: *10*, *20*, *30*, *40* og *50*. Hver ruteoperation kræver en ressource, der har forskellige egenskaber. Ruteoperation *10* kræver f.eks. en ressource, der har mulighed for at samle en højttaler (*0050 Højttalersamling*) og egenskaberne for træarbejde (*1010 Træegenskaber*). Ruteoperation *50* kræver en ressource, der har en egenskab til at pakke et produkt (*0070 Pakkeegenskab*).

![Egenskabsbaseret planlægning.](media/capability-based-scheduling.png "Egenskabsbaseret planlægning.")

Under planlægning søget programmet efter ressourcer, der opfylder operationskravene. Planlægningsprogrammet vælger f.eks. ressourcen *00101* til at udføre operation *10*, da denne ressource er den første fundne ressource med begge de påkrævede egenskaber. Planlægningsprogrammet vælger f.eks. ressourcen *00301* til at udføre operation *50*, da denne ressource er den eneste ressource med pakkeegenskaben.

Overvej derefter, hvordan dette eksempel påvirkes, når der bruges færdighedsniveauer:

- Operation *10* kræver et minimalt færdighedsniveau på *7* for egenskaben *0059 Samling*.
- Ressource *00101* har et færdighedsniveau på *5* for egenskaben *0059 Samling*.
- Ressource *00102* har et færdighedsniveau på *10* for egenskaben *0059 Samling*.

I dette tilfælde vælger planlægningsprogrammet ressource *00102* under planlægning af ubegrænset kapacitet for at udføre operation *10*, da denne ressource, i modsætning til ressource *00101*, har det nødvendige færdighedsniveau for egenskaben.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
