---
title: Oprette forbrugsrapporter
description: Dette emne forklarer, hvordan du opretter forbrugsrapporter i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
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
ms.openlocfilehash: 3d978f8b991211e477dd8f766fe67432d9d493d0
ms.sourcegitcommit: c0b581e4c647b6c47bc14d1d7bfe267832afecba
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/21/2019
ms.locfileid: "1913078"
---
# <a name="create-consumption-reports"></a>Oprette forbrugsrapporter

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Når du har oprettet og bogført forbrugsregistreringer på arbejdsordrer i aktivstyring, er der to rapporter tilgængelige til visning af detaljer om forbrug.


## <a name="asset-consumption-report"></a>Forbrugsrapport over aktiv

Når du har bogført forbrug på arbejdsordrer, kan du udskrive en rapport over aktivforbrug. Rapporten viser timer, timeomkostninger, vareomkostninger og udgifter, der er bogført på aktiver.

1. Klik på **Styring af aktiver** > **Rapporter** > **Aktiver** > **Aktivforbrug**.

2. Vælg i dialogboksen **Aktivforbrug** de parametre og det detaljeringsniveau, du vil have vist, ved at vælge "Ja" på de relevante til/fra-knapper, og Indsæt et arbejdssted i afsnittet **Vis**.
    - Du kan bruge feltet **Niveauer** til at angive, hvor detaljerede aktivlinjerne skal være i forbindelse med arbejdssteder. Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle aktiver for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. Hvis du indsætter tallet "0" i feltet **Niveauer**, kan du se et detaljeret resultat, der viser alle aktiver på alle de arbejdsstedsniveauer, de er relateret til. 
    - Vælg "ja" på til/fra-knappen **Sum på alle underaktiver** for at få vist summen for hvert underaktiv i rapporten.

3. Vælg et datointerval i sektionen **Datoer**.

4. I oversigtspanelet **Destination** skal du vælge, om du vil have vist rapporten på skærmen, udskrive den eller gemme den som en fil eller mail.

5. Hvis det er nødvendigt, kan du vælge de specifikke aktiver, der skal vises i rapporten. Klik på **Filter** i oversigtspanelet **Poster, der skal indgå**, og tilføj de aktiver, der skal medtages i rapporten.

6. Klik på **OK** for at oprette rapporten.


## <a name="work-order-consumption-report"></a>Forbrugsrapport for arbejdsordre

Når du har bogført forbrug på arbejdsordrer, kan du udskrive en forbrugsrapport for arbejdsordrer. Rapporten viser timer, timeomkostninger, vareomkostninger og udgifter, der er bogført på arbejdsordrer.

1. Klik på **Styring af aktiver** > **Rapporter** > **Arbejdsordrer** > **Forbrug af arbejdsordre**.

2. Vælg i dialogboksen **Forbrug af arbejdsordre** de parametre, du vil medtage i rapporten, ved at vælge "Ja" i de relevante til/fra-knapper i sektionen **Vis**.

3. Vælg et datointerval i sektionen **Datoer**.

4. I oversigtspanelet **Destination** skal du vælge, om du vil have vist rapporten på skærmen, udskrive den eller gemme den som en fil eller mail.

5. Hvis det er nødvendigt, kan du vælge de specifikke arbejdsordrer, der skal vises i rapporten. Klik på **Filter** i oversigtspanelet **Poster, der skal indgå**, og tilføj de arbejdsordrer, der skal medtages i rapporten.

6. Klik på **OK** for at oprette rapporten.


>[!NOTE]
>Du kan også oprette en [arbejdsordrerapport](../work-orders/work-order-report.md), der indeholder flere oplysninger om arbejdsordrer.

