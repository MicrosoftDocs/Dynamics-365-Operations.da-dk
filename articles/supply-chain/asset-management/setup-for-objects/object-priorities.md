---
title: Aktivers tjenesteniveauer
description: I dette emne beskrives aktivtjenesteniveauer i Styring af aktiver.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e4f7daa10931ce406a5d2bdbbc1dced067e3de5065cdb61cce369d617709d67
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723593"
---
# <a name="asset-service-levels"></a>Aktivers tjenesteniveauer

[!include [banner](../../includes/banner.md)]

 

I dette emne beskrives aktivtjenesteniveauer i Styring af aktiver. Aktivers tjenesteniveauer er relateret til aktiver og overføres til vedligeholdelsesanmodninger og arbejdsordrer. De bruges til at beregne prioriteringen af arbejdsordrer i forbindelse med arbejdsordreplanlægning. Aktivers tjenesteniveauer kan ændres, hvis der er behov for ændringer.

Du finder flere oplysninger om den opsætning, der er relateret til beregningen af rangeringsresultater for planlægning af arbejdsordre under [Parametre for Styring af aktiver](../setup-for-objects/enterprise-asset-management-parameters.md). Du skal oprette mindst én standardpost for tjenesteniveauet for aktivet. Denne standardpost bruges, hvis der ikke findes andre match under planlægning af arbejdsordren.

**Eksempel 1:** det tjenesteniveau, der som standard bruges, hvis der ikke findes andre match. I denne post skal du kun vælge et tjenesteniveau.

**Eksempel 2:** et højt tjenesteniveau, der bruges til at planlægge job til en Volvo-lastbilmotor. I denne post vælger du en relevant aktivtype (f.eks **Lastbilmotor**), en producent (**Volvo**) og et tjenesteniveau.

## <a name="set-up-asset-service-levels"></a>Konfigurer aktivers tjenesteniveauer

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Tjenesteniveau for aktiv**.
2. Vælg **Ny** for at oprette en post.
3. Afhængigt af det detaljeringsniveau, der kræves for aktiv tjenesteniveauet, skal du foretage relevante valg i felterne **Arbejdssted**, **Aktivtype**, **Producent**, **Model**, **Aktiv**, **Arbejdsordretype** og **Tjenesteniveau**.

    > [!NOTE]
    > Når tjenesteniveauet for et aktiv bruges til vedligeholdelsesanmodninger og arbejdsordrer, gennemgår Styring af aktiver alle poster på et aktivs tjenesteniveau for at kontrollere, om der er et muligt match. Den kontrollerer altid den mest specifikke kombination først. Med andre ord kontrollerer Styring af aktiver først, om der er et match for feltet **Arbejdsordretype**. Hvis der ikke findes et match, kontrolleres det, om der er et match for feltet **Aktiv** osv. Som du kan se i layoutet for siden **Tjenesteniveauer for aktiver**, betyder denne adfærd, at Styring af aktiver kontrollerer hver enkelt post fra højre mod venstre for et match for at finde den mest specifikke kombination. Hvis der ikke findes et match, bruges standardposten, som ikke har nogen markeringer i de pågældende felter.

4. I feltet **Tjenesteniveau** skal du vælge et nummer, der angiver tjenesteniveauet (prioritet).


> [!NOTE]
> Hvis du ændrer en registrering af tjenesteniveauet for aktivet på siden **Tjenesteniveauer for aktiv**, efter at du allerede har brugt den på en arbejdsordre, opdateres tjenesteniveauet på vedligeholdelsesanmodninger og arbejdsordrer ikke i overensstemmelse hermed.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]