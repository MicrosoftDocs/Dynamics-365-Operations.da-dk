---
title: Vedligeholdelsesnedetid
description: Dette emne beskriver vedligeholdelsesnedetid i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918238"
---
# <a name="maintenance-downtime"></a>Vedligeholdelsesnedetid


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Du kan oprette registreringer af vedligeholdelsesnedetid for det aktiv, der er valgt på en arbejdsordre. Dette er nyttigt, hvis du vil registrere vedligeholdelsesnedetid på en eller flere maskiner i produktionsområdet. Først skal du oprette de årsagskoder til vedligeholdelsesnedetid, du vil bruge, f.eks. nedbrud og planlagt stop. Dette gøres i **Årsagskoder til vedligeholdelsesnedetid**. Derefter kan du oprette registreringer af vedligeholdelsesnedetid i **Vedligeholdelsesnedetid** og tilføje de relevante årsagskoder.

## <a name="create-maintenance-downtime-reason-codes"></a>Oprette årsagskoder for vedligeholdelsesnedetid

1. Klik på **Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Årsagskoder til vedligeholdelsesnedetid**.

2. Klik på **Ny**.

3. Indsæt et id i feltet **Årsagskode til vedligeholdelsesnedetid**.

4. Angiv et navn til årsagskoden i feltet **Navn**.

5. Markér afkrydsningsfeltet **Medtag KPI**, hvis årsagskoden skal medtages i KPI-beregninger for aktiv. Generelt bør planlagte produktionsstop ikke medtages i KPI-beregninger, da de ikke påvirker den forventede ydeevne.

6. Klik på **Gem**.

![Figur 1](media/15-work-orders.png)


Når du har oprettet de årsagskoder til vedligeholdelsesnedetid, du vil bruge, kan du oprette registreringer af vedligeholdelsesnedetid for arbejdsordrer og aktiver.


## <a name="create-maintenance-downtime-registrations"></a>Oprette registreringer af vedligeholdelsesnedetid

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg arbejdsordren, og klik på **Vedligeholdelsesnedetid**.

3. Klik på **Ny**.

4. Indsæt dato- og tidsinterval for registrering af vedligeholdelsesnedetid i felterne **Fra** og **Til**.

5. Når du forlader feltet **Til**, indsættes varigheden i timer automatisk i feltet **Varighed**.

6. Vælg en årsagskode i feltet **Årsagskode til vedligeholdelsesnedetid**.

7. Gentag trin 3-6, hvis du vil tilføje flere registreringer.

8. Klik på **Gem**.


![Figur 2](media/16-work-orders.png)


Den kalender, der bruges til beregning af registreret vedligeholdelsesnedetid, afhænger af dit valg i opsætningen af aktiver og parametre. Hvis en ressource er valgt på et aktiv i **Alle aktiver** > **Anlægsaktiv**-oversigtspanelet > feltet **Ressource**, bruges den kalender, der er konfigureret for den tilknyttede ressourcegruppe, som vist i følgende figur.

![Figur 3](media/17-work-orders.png)


Hvis der ikke er valgt en ressource på aktivet, bruges den standardkalender, der er valgt i **Parametre til aktivstyring**, som vist i følgende figur.

![Figur 4](media/18-work-orders.png)


Klik på **Styring af virksomhedsaktiv** > **Forespørgsler** > **Vedligeholdelsesnedetid** for at få vist en oversigt over alle registreringer af vedligeholdelsesnedetid.

>[!NOTE]
>Alle de kalendere, der bruges i modulet **Styring af aktiver**, konfigureres i **Virksomhedsadministration** > **Opsætning** > **Kalendere** > **Kalendere**.

