---
title: Ansvarlige vedligeholdelsesarbejdere
description: Denne artikel beskriver, hvordan du konfigurerer ansvarlige vedligeholdelsesarbejdere i Styring af aktiver.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9535be3161253e88083b5add7ac55c12364aa383
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875586"
---
# <a name="responsible-maintenance-workers"></a>Ansvarlige vedligeholdelsesarbejdere

[!include [banner](../../includes/banner.md)]

 

Ansvarlige vedligeholdelsesarbejdere kan relateres til aktivtyper, aktiver, arbejdssteder, kategorier af vedligeholdelsesjobtyper, vedligeholdelsesjobtyper, varianter af vedligeholdelsesjobtyper og handler. De kan bruges på arbejdsordrer og vedligeholdelsesanmodninger til at indikere en præference for de vedligeholdelsesarbejdere, der skal være ansvarlige for en arbejdsordre. (Disse vedligeholdelsesarbejdere er dog ikke nødvendigvis de samme arbejdere, der er planlagt til at skulle udføre arbejdsordren.) Du kan frit vælge, om du ønsker at bruge denne funktion. Den kan eksempelvis bruges til at vælge ansvarlige arbejdere eller arbejdergrupper til bestemte arbejdstyper eller arbejdsområder.

I løbet af en arbejdsordres livscyklus eller en vedligeholdelsesanmodnings livscyklus kan ansvarlige vedligeholdelsesarbejdere ændres eller opdateres. Denne ændring eller opdatering kan være relateret til eksempelvis en ændring i tilstanden for vedligeholdelsesanmodnings livscyklus eller tilstanden for arbejdsordrens livscyklus.

Opsætningen på siden **Ansvarlig vedligeholdelsesarbejder** bruges *ikke* under planlægningen af arbejdsordre.

> [!NOTE]
> I Styring af aktiver kan du også konfigurere *foretrukne* vedligeholdelsesarbejdere, der kan allokeres til arbejdsordrer i forbindelse med arbejdsordrens planlægning.

Før du kan konfigurere ansvarlige vedligeholdelsesarbejdere, skal du konfigurere de arbejdere og vedligeholdelsesarbejdergrupper, der skal være tilgængelige for udvælgelse. Du finder oplysninger om, hvordan du konfigurerer arbejdere og vedligeholdelsesarbejdergrupper, i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-responsible-maintenance-workers"></a>Konfigurer ansvarlige vedligeholdelsesarbejdere

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdere** \> **Ansvarlige vedligeholdelsesarbejdere**.
2. Vælg **Ny** for at oprette en post.
3. Opret først en standard ansvarlig vedligeholdelsesarbejder eller konfigurer en ansvarlig vedligeholdelsesarbejdergruppe, hvor du kun konfigurer feltet **Ansvarlig vedligeholdelsesarbejdergruppe** og/eller feltet **Ansvarlig arbejder**. Lad de resterende felter være tomme. Denne standardopsætning bruges i forbindelse med planlægningen af arbejdsordrer, hvis der ikke er angivet en mere specifik kombination, som svarer til indholdet af arbejdsordren.

    > [!NOTE]
    > Ved oprettelse af en vedligeholdelsesanmodning, når en ansvarlig vedligeholdelsesarbejder eller ansvarlig vedligeholdelsesarbejdergruppe stilles til rådighed for udvælgelse på siden **Alle vedligeholdelsesanmodninger**, gennemgår Styring af aktiver alle ansvarlige vedligeholdelsesarbejderposter for at kontrollere, om der er et mulig match. Den kontrollerer altid den mest specifikke kombination først. Med andre ord kontrollerer Styring af aktiver først, om der er et match for feltet **Handel**. Hvis der ikke findes et match, kontrolleres det, om der er et match for feltet **Vedligeholdelsesjobtypevariant**. Hvis der ikke findes et match, kontrolleres det, om der er et match for feltet **Vedligeholdelsesjobtype** osv. Som du kan se på sidens layout, betyder denne adfærd, at Styring af aktiver kontrollerer hver post fra højre mod venstre for et match (i rækkefølgen **Handel**, **Vedligeholdelsesjobtypevariant**, **Vedligeholdelsejobtype**, **Vedligeholdelsejobtypekategori**, **Arbejdssteder**, **Aktiv** og til sidst **Aktivtype**) for at finde den mest specifikke kombination. Hvis der ikke findes et match, bruges standardposten, som ikke har nogen markeringer i de syv felter.

I følgende illustration vises et eksempel på listesiden **Ansvarlige vedligeholdelsesarbejdere**.

![Siden Ansvarlige vedligeholdelsesarbejdere.](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]