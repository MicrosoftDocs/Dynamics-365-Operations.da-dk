---
title: "Få vist ordrebeskeder i POS"
description: "I dette emne beskrives, hvordan du aktiverer ordrebeskeder på salgsstedet (POS) og beskedstrukturen, som kan udvides til andre operationer."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ec6cb212766dd90fa9db7719a2119419ecb935c7
ms.openlocfilehash: aea36591a81f727059e37a958efa62a9ebde9d9d
ms.contentlocale: da-dk
ms.lasthandoff: 12/20/2017

---

# <a name="display-notifications-in-point-of-sale"></a>Få vist beskeder i POS

I dagens moderne detailmiljø, tildeles medarbejderne i butikken forskellige opgaver, f.eks. at hjælpe kunder, indtaste transaktioner, udføre optællinger af lagerbeholdninger og modtage ordrer i butikken. POS-klienten gør det muligt for medarbejderne at udføre disse opgaver og meget mere, det hele i ét enkelt program. Med forskellige opgaver, der skal udføres i løbet af en dag, skal medarbejderne evt. have besked, når noget kræver deres opmærksomhed. Beskedstrukturen på POS'et løser dette problem ved at tillade forhandlere at konfigurere rollebaseret beskeder. Med Dynamics 365 for Retail med programopdatering 5, kan disse beskeder kun konfigureres for POS-operationer.

I øjeblikket giver systemet dig mulighed for at få vist beskeder for ordreopfyldningsoperationer, men strukturen er designet, så den kan udvides, så i fremtiden kan udviklere skrive en beskedbehandler til enhver operation, så beskeder kan vises i POS.  

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Aktivere beskeder for ordreopfyldningsoperationer

Hvis du vil aktivere beskeder for ordreopfyldningsoperationer, skal du se følgende trin:

 - Gå til siden **Operationer** (**Detail** > **Konfiguration af kanal** > **POS-opsætning** > **POS** > **Operationer**).
 - Søg efter ordreopfyldningsoperationen, og markér afkrydsningsfeltet **Aktivér beskeder** ud for denne operation. Dette giver beskedstrukturen besked om at lytte til behandleren for ordreopfyldningsoperationen. Hvis behandleren er implementeret, vises beskeder på POS, ellers bliver der ikke vist beskeder for denne operation.
- Gå til de POS-rettigheder, der er knyttet til medarbejderne, og tilføj ordreopfyldningsoperationen i oversigtspanelet **Beskeder** med "visningsrækkefølge" 1. Når der er mere end én konfigureret besked, bruges visningsrækkefølgen til at arrangere beskeden fra top til bund med 1 øverst. Kun de operationer, hvor afkrydsningsfeltet **Aktiver beskeder** er markeret, kan tilføjes. Desuden vises beskederne kun for de operationer, der er tilføjet her, og kun for de medarbejdere, for hvem operationerne er føjet til de tilsvarende POS-rettigheder. 

> [!NOTE]
> Du kan tilsidesætte beskeder på brugerniveau ved at navigere til posten for medarbejderen og vælge **POS-rettigheder** og derefter redigere denne brugers beskedabonnement.

 - Gå til siden **Funktionalitetsprofil** (**Detail** > **Konfiguration af kanal** > **POS-opsætning** > **POS-profiler** > **Funktionalitetsprofiler**). Opdater **Beskedinterval**-egenskaben til at angive det interval i minutter, som beskederne skal hentes med. Vi anbefaler at indstille værdien til 10 minutter for at undgå unødvendig kommunikation til hovedkontoret. Hvis du indstiller beskedintervallet til "0", deaktiveres beskeder.  

 - Gå til **Detail** > **Detail-it** > **Distributionsplan**. Vælg tidsplan "1060-personale" for at synkronisere indstillinger for beskedabonnementet, og klik derefter på **Kør nu**. Synkroniser derefter rettighedsintervallet ved at vælge "1070-kanalkonfiguration", og klik derefter på **Kør nu**. 

## <a name="view-notifications-in-pos"></a>Vise beskeder i POS

Når ovenstående trin er fuldført, kan de medarbejdere, for hvem beskederne er oprettet, få vist beskederne i POS. Klik på beskedikonet på titellinjen i POS for at få vist beskederne. Der vises et beskedcenter med beskederne for ordreopfyldningsoperationen. Beskedcenteret skal vise følgende grupper i ordreopfyldningsoperationen: 

- **Ventende ordrer** - Denne gruppe viser antallet af ordrer, der er i tilstanden Afventer, som f.eks. ordrer der skal godkendes af en POS-medarbejder, der har de nødvendige rettigheder til butiksopfyldning. Når du klikker på nummeret på gruppen, åbnes siden **Ordreopfyldning** filtreret, så kun de ventende ordrer, der er tildelt butikken for at blive opfyldt, vises. Hvis ordrerne automatisk accepteres for butikken, er antallet for denne gruppe nul.

- **Afhentning i butik** - Denne gruppe viser antallet af ordrer, der har leveringsmåden **Afhentning**, og afhentningen planlægges fra den aktuelle butik. Når du klikker på nummeret på gruppen, åbnes siden **Ordreopfyldning** filtreret, så de aktive ordrer, der er konfigureret til at blive plukket fra den aktuelle butik, vises.

- **Afsend fra butik** - Denne gruppe viser antallet af ordrer, der har leveringsmåden **Levering**, og leveringen planlægges fra den aktuelle butik. Når du klikker på nummeret på gruppen, åbnes siden **Ordreopfyldning** filtreret, så de aktive ordrer, der er konfigureret til at blive leveret fra den aktuelle butik, vises.

Hvis der er nye ordrer, der er tildelt butikken for at blive opfyldt, ændres beskedikonet, så det angiver de nye beskeder, og antallet af de tilsvarende grupper bliver opdateret. Brugeren kan også klikke på opdateringsikonet ud for navnet på operationen for straks at opdatere antallet af grupper. Antallet opdateres også med det interval, der er foruddefineret. En gruppe, der har en ny vare, der ikke kan ses af den aktuelle medarbejder, vises med et burst-ikon, der angiver, at denne gruppe har en ny vare. Klik på felterne i beskeder åbner den operation, som beskeden er konfigureret for. Hvis du i ovenstående situationer klikker på beskederne, åbnes siden **Ordreopfyldning**, og de relevante parametre overføres: ventende ordrer, afhentning i butik og afsend fra butik. 

> [!NOTE]
> Beskeder om ventende ordrer aktiveres i en kommende opdatering til Dynamics 365 for Retail. 


