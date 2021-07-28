---
title: Vis ordrebeskeder på POS
description: I dette emne beskrives, hvordan du aktiverer ordrebeskeder på salgsstedet (POS) og i beskedstrukturen.
author: ShalabhjainMSFT
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 57f5d23533c2fd17593648a15745fa770fc01dc4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345202"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Vis ordrebeskeder på POS

[!include [banner](includes/banner.md)]

Butiksmedarbejdere kan tildeles forskellige opgaver i butikken, f.eks. opfyldelse af ordrer eller udførelse af lageropgørelse eller statusoptællinger. POS-klienten leverer ét enkelt program, hvor medarbejderne kan blive gjort opmærksom på disse opgaver. Beskedstrukturen på POS'et er en hjælp, fordi forhandlere kan bruge den til at konfigurere rollebaserede beskeder. Med start i Dynamics 365 Retail med programopdatering 5 kan disse meddelelser konfigureres til POS-handlinger.

Systemet kan vise beskeder om *ordreopfyldningshandlingen*, og der kan også vises beskeder om *tilbagekaldsordrehandlingen* ved at starte i Commerce version 10.0.18. Fordi strukturen er udviklet til at kunne udvides, vil udviklere dog senere kunne [skrive en beskedbehandler](dev-itpro/extend-pos-notification.md) for operationer og få vist beskederne for den pågældende operation i POS.

## <a name="enable-notifications-for-order-fulfillment-or-recall-order-operations"></a>Aktivere beskeder for ordreopfyldningsoperationer eller tilbagekalde handlinger

Hvis du vil aktivere beskeder for ordreopfyldningsoperationer eller tilbagekalde handlinger, skal du se følgende trin.

1. Gå til **Retail og Commerce \> Kanalopsætning \> POS-opsætning \> POS \> Handlinger**.
1. Søg efter ente **Ordreopfyldning**-operationen eller **Tilbagekald**-operationen, og marker afkrydsningsfeltet **Aktiver beskeder** ud for indstillingen for at angive, at beskedstrukturen skal lytte til behandleren for denne operation. Hvis behandleren er implementeret, vises beskeder for denne operation derefter i POS.
1. Gå til **Retail og Commerce \> Medarbejdere \> Arbejdere**.
1. Vælg fanen **Handel**, vælg en arbejderrække, og vælg derefter **POS-tilladelser**. Vælg oversigtspanelet **Beskeder** for at udvide det, og tilføj derefter de handlinger, du har aktiveret beskeder for. Hvis du konfigurerer en enkelt besked til en arbejder, skal du sikre dig, at værdien for **Visningsrækkefølge** er angivet til **1**. Hvis du konfigurerer mere end én handling, skal du angive værdierne for **Visningsrækkefølge** for at angive den rækkefølge, som beskederne skal vises i. 

      Beskeder vises kun for handlinger, der er tilføjet i oversigtspanelet **Beskeder**. Du kan kun tilføje handlinger der, hvis afkrydsningsfelterne **Aktiver beskeder** for disse handlinger er markeret på siden **POS-handlinger**. Derudover vises beskeder for en operation kun for arbejdere, hvis operationen føjes til POS-rettighederne for disse arbejdere.

    > [!NOTE]
    > Beskeder kan tilsidesættes på brugerniveau. Gør dette ved at åbne arbejderens post, vælge **POS-rettigheder**, og rediger derefter brugerens beskedabonnement.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**. I feltet **Beskedinterval** skal du angive, hvor ofte beskeder skal udtrækkes. For nogle beskeder skal POS foretage kald i realtid til back-office-programmet. Disse kald forbruger databehandlingskapaciteten fra back-office-programmet. Når du indstiller beskedintervallet, skal du derfor overveje både virksomhedens behov og virkningen af kald i realtid til back-office-programmet. En værdi på **0** (nul) deaktiverer beskeder.
1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**. Vælg tidsplanen **1060** (**personale**) for at synkronisere indstillinger for beskedabonnementet, og vælg derefter **Kør nu**. Vælg derefter tidsplanen **1070** (**kanalkonfiguration**) for at synkronisere rettighedsintervallet, og vælg derefter **Kør nu**.

## <a name="view-notifications-in-the-pos"></a>Vise beskeder i POS'et

Når du har fuldført de foregående trin, kan arbejderne se beskederne i POS'et. Vælg beskedikonet i øverste højre hjørne i POS'et for at få vist beskederne. Der vises et beskedpanel, som viser beskeder om de handlinger, der er konfigureret for arbejderen. 

Beskedcenteret skal vise følgende grupper i **ordreopfyldningsoperation**:

- **Afhentning i butik** - Denne gruppe viser antallet af individuelle ordrer, der har leveringsmåden Afhentning, og som er planlagt til afhentning fra den aktuelle butik. Du kan vælge nummeret på gruppen for at åbne **ordreopfyldningsoperationen** med et filter, så den kun viser de aktive ordrelinjer, der er konfigureret til afhentning fra den aktuelle butik.
- **Afsendelse fra butik** - Denne gruppe viser optællingen af individuelle ordrelinjer, der er konfigureret til at blive afsendt fra brugerens aktuelle butik. Du kan vælge nummeret på gruppen for at åbne **ordreopfyldningsoperationen** med en filtreret visning, så den kun viser de aktive ordrelinjer, der er konfigureret til afhentning fra den aktuelle butik.

Beskedcenteret skal vise følgende grupper i **ordreopfyldningsoperation**:

- **Ordrer, der skal opfyldes** – Denne gruppe viser optællingen af ordrer, der er konfigureret til enten afhentning eller forsendelsesopfyldning for brugerens aktuelle butik. Du kan vælge nummeret på gruppen for at åbne operationen **Tilbagekald ordre** med en filtreret visning, der kun viser de åbne ordrer, som skal opfyldes af brugerens aktuelle butik for enten afhentning i butiks- eller afsendelse fra butiksscenarier.
- **Afhentning i butik** - Denne gruppe viser antallet af ordrer, der har leveringsmåden Afhentning, og som er planlagt til afhentning fra den aktuelle butik. Du kan vælge nummeret på gruppen for at åbne operationen **Tilbagekald ordre** med en filtreret visning, der kun viser de åbne ordrer, som skal opfyldes med kundens afhentning i kundens aktuelle butik.
- **Ordrer, der skal afsendes** – Denne gruppe viser antallet af ordrer, der skal afsendes fra brugerens aktuelle butik. Du kan vælge nummeret på gruppen for at åbne operationen **Tilbagekald ordre** med en filtreret visning, der kun viser de åbne ordrer, som skal opfyldes med afsendelse fra kundens aktuelle butik.

For både ordreopfyldning og tilbagekaldsmeddelelser kan nye ordrer, der afhentes af processen, ændre beskedikon, så det angiver, at der er nye beskeder, og antallet af de relevante grupper opdateres. Selvom grupperne opdateres med jævne mellemrum, kan POS-brugere manuelt opdatere grupperne til enhver tid ved at vælge knappen **Opdater** ud for gruppen. Endelig, hvis en gruppe har en ny vare, som den aktuelle arbejder ikke har fået vist, viser gruppen et burst-symbol for at angive nyt indhold.

## <a name="enable-live-content-on-pos-buttons"></a>Aktivere dynamisk indhold på POS-knapper

POS-knapper kan nu vise en optælling, så arbejderne nemmere kan bestemme, hvilke opgaver der kræver deres omgående opmærksomhed. For at vise dette nummer på en POS-knap skal du fuldføre opsætningen af beskeder, der er beskrevet tidligere i dette emne, (det vil sige, du skal aktivere beskeder for en operation, oprette et beskedinterval og opdatere POS-rettighedsgruppen for arbejderen). Derudover skal du åbne knapgitterdesigneren, se knappens egenskaber og markere afkrydsningsfeltet **Aktiver dynamisk indhold**. I feltet **Justering af indhold** kan du vælge, om antallet skal vises i øverste højre hjørne af knappen (**Øverst til højre**) eller i midten (**Centreret**).

> [!NOTE]
> Dynamisk indhold kan kun aktiveres for operationer, hvis afkrydsningsfeltet **Aktiver beskeder** er markeret for dem på siden **POS-handlinger** som beskrevet tidligere i dette emne.

I følgende illustration vises indstillingerne for dynamisk indhold i knapgitterdesigneren.

![Indstillinger for dynamisk indhold i knapgitterdesigneren.](./media/ButtonGridDesigner.png "Indstillinger for dynamisk indhold i knapgitterdesigneren")

Hvis du vil have vist antallet af beskeder på en knap, skal du sikre dig, at det korrekte skærmlayout opdateres. Hvis du vil fastlægge, hvilket skærmlayout der bruges af POS, skal du vælge ikonet **Indstillinger** i øverste højre hjørne og notere **Skærmlayout-id** og **Layoutopløsning**. Brug nu Microsoft Edge-browseren, og gå til siden **Skærmlayout**, find det **Skærmlayout-id** og den **Layoutopløsning**, der blev identificeret ovenfor, og markér afkrydsningsfeltet **Aktivér dynamisk indhold**. Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**, og kør jobbet 1090 (Kasseapparater) for at synkronisere ændringer af layoutet.

![Finde det skærmlayout, der bruges af POS.](./media/Choose_screen_layout.png "Finde skærmlayoutet")

I følgende illustration viser effekten af at vælge **Øverst til højre** og **Centreret** i feltet **Justering af indhold** for knapper i forskellige størrelser.

![Dynamisk indhold på POS-knapper.](./media/ButtonsWithLiveContent.png "Dynamisk indhold på POS-knapper")

[!INCLUDE[footer-include](../includes/footer-banner.md)]
