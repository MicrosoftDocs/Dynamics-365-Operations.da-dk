---
title: "Vis ordrebeskeder på POS"
description: "I dette emne beskrives, hvordan du aktiverer ordrebeskeder på salgsstedet (POS) og i beskedstrukturen. Til slut kan udviklere udvide disse beskeder til operationer ud over ordreopfyldningsoperationer."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
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
ms.sourcegitcommit: 0d409b3b7f19ca31d9c720bca191f1ddba81caa3
ms.openlocfilehash: a55af4c26d74cc392d3c53aacb66e0a8bc97abf2
ms.contentlocale: da-dk
ms.lasthandoff: 03/13/2018

---

# <a name="show-order-notifications-in-the-point-of-sale"></a>Vis ordrebeskeder på POS

[!INCLUDE [banner](includes/banner.md)]

I det moderne detailmiljø tildeles medarbejderne i butikken forskellige opgaver, f.eks. at hjælpe kunder, indtaste transaktioner, udføre optællinger af lagerbeholdninger og modtage ordrer i butikken. POS-klienten leverer ét enkelt program, hvor medarbejderne kan udføre alle disse og mange andre opgaver. Da der skal udføres forskellige opgaver i løbet af dagen, skal medarbejderne evt. have besked, når noget kræver deres opmærksomhed. Beskedstrukturen på POS'et er en hjælp, fordi forhandlere kan bruge den til at konfigurere rollebaserede beskeder. I Microsoft Dynamics 365 for Retail med programopdatering 5 kan disse beskeder kun konfigureres for POS-operationer.

På nuværende tidspunkt kan systemet kun vise beskeder for ordreopfyldningsoperationer. Fordi strukturen er udviklet til at kunne udvides, vil udviklere dog senere kunne skrive en beskedbehandler for operationer og få vist beskederne for den pågældende operation i POS'et.

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Aktivere beskeder for ordreopfyldningsoperationer

Hvis du vil aktivere beskeder for ordreopfyldningsoperationer, skal du følge disse trin.

1. Gå til **Retail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Operationer**.
2. Søg efter **Ordreopfyldning**-operationen, og marker afkrydsningsfeltet **Aktiver beskeder** ud for indstillingen for at angive, at beskedstrukturen skal lytte til behandleren for denne operation. Hvis behandleren er implementeret, vises beskeder for denne operation derefter i POS.
3. Gå til **Retail** &gt; **Medarbejdere** &gt; **Arbejdere** &gt;. Under fanen Detail skal du åbne de POS-rettigheder, der er knyttet til arbejderen. Udvid oversigtspanelet **Beskeder**, tilføj operationen **Ordreopfyldning**, og indstil feltet **Visningsrækkefølge** til **1**. Hvis mere end én besked er konfigureret, kan dette felt bruges til at arrangere beskeder. Beskeder, der har en lavere værdi for **Visningsrækkefølge**, vises over beskeder, der har en højere værdi. Beskeder, der har en **Visningsrækkefølge**-værdi på **1**, findes øverst.

    Beskeder vises kun for operationer, der er tilføjet i oversigtspanelet **Beskeder**, og du kan kun tilføje operationer der, hvis afkrydsningsfeltet **Aktiver beskeder** for disse operationer er markeret på siden **POS-operationer**. Derudover vises beskeder for en operation kun for arbejdere, hvis operationen føjes til POS-rettighederne for disse arbejdere.

    > [!NOTE]
    > Beskeder kan tilsidesættes på brugerniveau. Åbn arbejderens post, vælg **POS-rettigheder**, og rediger derefter brugerens beskedabonnement.

4. Gå til **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Funktionalitetsprofiler**. I feltet **Beskedinterval** skal du angive, hvor ofte beskeder skal udtrækkes. For nogle beskeder skal POS foretage kald i realtid til back-office-programmet. Disse kald forbruger databehandlingskapaciteten fra back-office-programmet. Når du indstiller beskedintervallet, skal du derfor overveje både virksomhedens behov og virkningen af kald i realtid til back-office-programmet. En værdi på **0** (nul) deaktiverer beskeder.
5. Gå til **Detail** &gt; **Detail-it** &gt; **Distributionsplan**. Vælg tidsplanen **1060** (**personale**) for at synkronisere indstillinger for beskedabonnementet, og vælg derefter **Kør nu**. Vælg derefter tidsplanen **1070** (**kanalkonfiguration**) for at synkronisere rettighedsintervallet, og vælg derefter **Kør nu**.

## <a name="view-notifications-in-the-pos"></a>Vise beskeder i POS'et

Når du har fuldført de foregående trin, kan arbejderne se beskederne i POS'et. Tryk på beskedikonet i øverste højre hjørne i POS'et for at få vist beskederne. Der vises et beskedcenter med beskederne for ordreopfyldningsoperationen. Beskedcenteret skal vise følgende grupper i ordreopfyldningsoperationen:

- **Afhentning i butik** - Denne gruppe viser antallet af ordrer, der har leveringsmåden **Afhentning**, og som er planlagt til afhentning fra den aktuelle butik. Du kan trykke på nummeret på gruppen for at åbne siden **Ordreopfyldning**. I dette tilfælde filtreres på siden, så den kun viser de aktive ordrer, der er konfigureret til afhentning fra det aktuelle lager.
- **Afsend fra butik** - Denne gruppe viser antallet af ordrer, der har leveringsmåden **Levering**, og som er planlagt til forsendelse fra den aktuelle butik. Du kan trykke på nummeret på gruppen for at åbne siden **Ordreopfyldning**. I dette tilfælde filtreres på siden, så den kun viser de aktive ordrer, der er konfigureret til forsendelse fra det aktuelle lager.

Hvis der tildeles nye ordrer til butikken til opfyldelse, ændres beskedikonet, så det angiver, at der er nye beskeder, og antallet af de relevante grupper opdateres. Selvom grupperne opdateres med jævne mellemrum, kan POS-brugere manuelt opdatere grupperne til enhver tid ved at vælge knappen **Opdater** ud for gruppen. Endelig, hvis en gruppe har en ny vare, som den aktuelle arbejder ikke har fået vist, viser gruppen et burst-symbol for at angive nyt indhold.

## <a name="enable-live-content-on-pos-buttons"></a>Aktivere dynamisk indhold på POS-knapper

POS-knapper kan nu vise en optælling, så arbejderne nemmere kan bestemme, hvilke opgaver der kræver deres omgående opmærksomhed. For at vise dette nummer på en POS-knap skal du fuldføre opsætningen af beskeder, der er beskrevet tidligere i dette emne, (det vil sige, du skal aktivere beskeder for en operation, oprette et beskedinterval og opdatere POS-rettighedsgruppen for arbejderen). Derudover skal du åbne knapgitterdesigneren, se knappens egenskaber og markere afkrydsningsfeltet **Aktiver dynamisk indhold**. I feltet **Justering af indhold** kan du vælge, om antallet skal vises i øverste højre hjørne af knappen (**Øverst til højre**) eller i midten (**Centreret**).

> [!NOTE]
> Dynamisk indhold kan kun aktiveres for operationer, hvis afkrydsningsfeltet **Aktiver beskeder** er markeret for dem på siden **POS-handlinger** som beskrevet tidligere i dette emne.

I følgende illustration vises indstillingerne for dynamisk indhold i knapgitterdesigneren.

![Indstillinger for dynamisk indhold i knapgitterdesigneren](./media/ButtonGridDesigner.png "Indstillinger for dynamisk indhold i knapgitterdesigneren")

I følgende illustration viser effekten af at vælge **Øverst til højre** og **Centreret** i feltet **Justering af indhold** for knapper i forskellige størrelser.

![Dynamisk indhold på POS-knapper](./media/ButtonsWithLiveContent.png "Dynamisk indhold på POS-knapper")

