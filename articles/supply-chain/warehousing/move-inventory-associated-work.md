---
title: Flytning af lager med tilknyttet arbejde i Lokationsstyring
description: "I dette emne beskrives, hvordan du kan konfigurere og anvende bekræftelse af stykplukning fra en mobilenhed."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 463e438418c4bc1b38fd1bde8251d1383cb44a13
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>Flytning af lager med tilknyttet arbejde i Lokationsstyring

[!include[banner](../includes/banner.md)]

Ved hjælp af lagerbevægelse kan du bestemme, hvilke lagermedarbejdere der skal have tilladelse til at flytte reserveret lager. Dette giver en fleksibilitet på regulerede lagersteder, hvor du kan vælge, at en arbejder ikke skal kunne vælge en ny pluklokation for plukarbejde, der allerede er oprettet. Det gør det også muligt for lagerstedets chef at styre, hvilke funktioner mindre erfarne arbejdere skal have adgang til.

Muligheden for fleksibel administration af lagermedarbejdernes daglige operationer kan være nyttig i situationer som disse:

## <a name="scenario-1"></a>Scenario 1
Et firma har et relativt lille modtagelsesområde, og det er overfyldt med paller og kasser, der venter på at blive lagt på lager. Der ventes en stor forsendelse på den aktuelle dag, så medarbejderen i modtagelsen beslutter at rydde op i modtagelsesområdet ved at flytte nogle af pallerne til et sekundært, midlertidigt indgående område.

## <a name="scenario-2"></a>Scenario 2
En erfaren lagermedarbejderen ser en mulighed for på et lagersted at konsolidere varer på ét sted i stedet for at få dem spredt på 3 steder i nærheden med et lavt antal på hvert sted. Arbejderen ønsker at konsolidere antallet ved at flytte varer fra hvert af disse steder til det samme sted og på det samme id.

## <a name="scenario-3"></a>Scenario 3
En palle afventer forsendelse på et midlertidig sted, f.eks. STAGE01, som er i nærheden af BAYDOOR01. På grund af en ændring af planerne ventes lastbilen imidlertid at ankomme til BAYDOOR04. Kontorassistenten er opmærksom på dette og skal sikre, at lastbilen ikke behøver at vente på at blive lastet fra STAGE01. Kontorassistenten beslutter sig for at flytte varerne i forsendelsen fra STAGE01 til STAGE04, som er tættere på den nye destination.

### <a name="current-limitations"></a>Aktuelle begrænsninger

De arbejdsreservationer, du kan flytte, er begrænset til salgsordre, flytteordreafgang, Flytteordretilgang, indkøbsordre og genopfyldningsarbejde.

Flytning af varer er begrænset for at forhindre opdeling af arbejdslinjer. Det betyder, at hvis du har en arbejdslinje for 100 stk. af vare A fra stedet Loc1, du ikke kan nøjes med at flytte 30 stk. af vare A derfra til et andet sted. Det ville medføre en opdeling af den eksisterende arbejdslinje i 30 og 70, fordi stederne nu er forskellige.

For midlertidige scenarier, hvor det id, du flytter varerne fra, eller det id, du flytter varerne til, er konfigureret som en mål-LP for en arbejdsordre, er det kun tilladt at flytte hele LP'en for ikke at opdele mål-LP'en.
Kun ad hoc-flytningen understøttes i øjeblikket. Det betyder, at du ikke kan flytte reserveret lager via den flytning, der udføres ved hjælp af menupunkter på mobilenheden i skabelonen.

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a>Konfigurere rettighed til at flytte reserveret lager for individuelle arbejdere

For den medarbejder, der skal have rettighed til at flytte reserveret lager, skal du markere afkrydsningsfeltet **Tillad flytning af lager med tilknyttet arbejde** under **Lokationsstyring** > **Opsætning** > **Arbejder**.  

### <a name="backported"></a>Overførsel

Denne funktion er også blevet overført til Microsoft Dynamics AX 2012 R3 og kan bruges som en del af CU12.
Den kan også hentes særskilt via KB-nummer 3192548. 


