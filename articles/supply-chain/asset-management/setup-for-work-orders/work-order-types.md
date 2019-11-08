---
title: Arbejdsordretyper
description: I dette emne beskrives typer af arbejdsordrer i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3e813bd4f2d47b928b6184bb063d9afa45695727
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569725"
---
# <a name="work-order-types"></a>Arbejdsordretyper

[!include [banner](../../includes/banner.md)]

 

Arbejdsordretyper bruges til kategorisering af arbejdsordrer. Du kan for eksempel have arbejdsordrer, der er relateret til forebyggende vedligeholdelse eller korrigerende vedligeholdelse.

En arbejdsordretype definerer et tilhørsforhold til en arbejdsordres livscyklusmodel. En arbejdsordres livscyklusmodel definerer de levetidstilstande for arbejdsordren, som kan angives på en arbejdsordre. (Eksempler på livscyklustilstande for arbejdsordrer omfatter **Oprettet**, **I gang** og **Afsluttet**).

Du kan finde flere oplysninger om arbejdsordrers livscyklustilstande og projektstadier i [Livscyklustilstande for arbejdsordre](work-order-lifecycle-states.md).

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Arbejdsordretyper**.
2. Vælg **Ny** for at oprette en arbejdsordretype.
3. Angiv et id for arbejdsordretypen i feltet **Arbejdsordretype**.
4. Indtast et navn i feltet **Navn**.
5. Vælg en livscyklusmodel i feltet **Livscyklusmodel for arbejdsordre**.
5. Vælg **Ja** i indstillingen **Én vedligeholdelsesarbejder**, hvis alle arbejdsordrejob, der er knyttet til en arbejdsordre af denne type, skal planlægges til samme vedligeholdelsesarbejder.
6. I feltet **Omkostningstype** skal du vælge **Korrigerende**, **Forebyggende** eller **Investering** efter behov. Alle arbejdsordrejob i en arbejdsordre skal have samme omkostningstype.
7. Vælg **Ja** i de relevante indstillinger i sektionen **Obligatorisk** for at angive, hvilke fejlrelaterede oplysninger eller oplysninger relateret til vedligeholdelsesnedetid, der skal føjes til en arbejdsordre af denne type.

    > [!NOTE]
    > Indstillingerne i sektionen **Obligatorisk** er relateret til indstillingerne i oversigtspanelet **Valider** på siden **Livscyklustilstande for arbejdsordre** (**Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Livscyklustilstande**).

8. Vælg **Gem**.

![Arbejdsordretyper](media/16-setup-for-work-orders.png)