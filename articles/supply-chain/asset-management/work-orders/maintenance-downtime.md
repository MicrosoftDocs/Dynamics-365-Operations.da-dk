---
title: Vedligeholdelsesnedetid for arbejdsordrer
description: Dette emne beskriver, hvordan du kan oprette registreringer af vedligeholdelsesnedetid for det aktiv, der er valgt på en arbejdsordre.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5c0c584ed53dc4ec8a761065838127dc67cbc41e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813719"
---
# <a name="maintenance-downtime-for-work-orders"></a>Vedligeholdelsesnedetid for arbejdsordrer

[!include [banner](../../includes/banner.md)]


Du kan oprette registreringer af vedligeholdelsesnedetid for det aktiv, der er valgt på en arbejdsordre. Dette er nyttigt, hvis du vil registrere vedligeholdelsesnedetid på en eller flere maskiner i produktionsområdet. Først skal du oprette de årsagskoder til vedligeholdelsesnedetid, du vil bruge, f.eks. **Nedbrud** og **Planlagt stop**. Dette gøres på siden **Årsagskoder til vedligeholdelsesnedetid**. Derefter kan du oprette registreringer af vedligeholdelsesnedetid på siden **Vedligeholdelsesnedetid** og tilføje de relevante årsagskoder for vedligeholdelsesnedetid.

## <a name="create-maintenance-downtime-reason-codes"></a>Oprette årsagskoder for vedligeholdelsesnedetid

1. Vælg **Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Årsagskoder til vedligeholdelsesnedetid**.

2. Vælg **Ny**.

3. Angiv et id for årsags koden til vedligeholdelsesnedetid i feltet **Årsagskode til vedligeholdelsesnedetid**.

4. Indtast et navn i feltet **Navn**.

5. Markér afkrydsningsfeltet **Medtag KPI**, hvis årsagskoden skal medtages i beregningerne af KPI'er for aktivet. Generelt bør planlagte produktionsstop ikke medtages i KPI-beregninger, da de ikke påvirker den forventede ydeevne.

6. Vælg **Gem**.

I følgende illustration vises et eksempel på siden **Årsagskoder til vedligeholdelsesnedetid**.

![Figur 1](media/15-work-orders.png)

Når du har oprettet de årsagskoder til vedligeholdelsesnedetid, du vil bruge, kan du oprette registreringer af vedligeholdelsesnedetid for arbejdsordrer og aktiver.


## <a name="create-maintenance-downtime-registrations"></a>Oprette registreringer af vedligeholdelsesnedetid

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg arbejdsordren, og vælg derefter **Vedligeholdelsesnedetid** i gruppen **Aktiv** under fanen **Arbejdsordre**.

3. Vælg **Ny**.

4. Indsæt dato- og tidsinterval for registrering af vedligeholdelsesnedetid i felterne **Fra** og **Til**.

>[!NOTE]
>Når du forlader feltet **Til**, indsættes varigheden i timer automatisk i feltet **Varighed**.

5. Vælg en årsagskode i feltet **Årsagskode til vedligeholdelsesnedetid**.

6. Gentag trin 3 til 5 for at tilføje flere registreringer.

7. Vælg **Gem**.

Følgende illustration viser et eksempel på en registrering af vedligeholdelsesnedetid.

![Figur 2](media/16-work-orders.png)

Den kalender, der bruges til beregning af registreret vedligeholdelsesnedetid, afhænger af dit valg i opsætningen af aktiver og parametre. Hvis en ressource er valgt på et aktiv i feltet **Ressource** i oversigtspanelet **Anlægsaktiv** på siden **Alle aktiver**, bruges den kalender, der er konfigureret for den tilknyttede ressourcegruppe, som vist i følgende illustration.

![Figur 3](media/17-work-orders.png)

Hvis der ikke er valgt en ressource på aktivet, bruges den standardkalender, der er valgt på siden **Parametre til aktivstyring**, som vist i følgende illustration.

![Figur 4](media/18-work-orders.png)

Klik på **Styring af aktiver** > **Forespørgsler** > **Vedligeholdelsesnedetid** for at se en oversigt over alle registreringer af vedligeholdelsesnedetid.

>[!NOTE]
>Alle de kalendere, der bruges i modulet **Styring af aktiver**, konfigureres i **Virksomhedsadministration** > **Opsætning** > **Kalendere** > **Kalendere**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]