---
title: Oprette forbrugsrapporter
description: Denne artikel forklarer, hvordan du opretter forbrugsrapporter i Styring af aktiver.
author: johanhoffmann
ms.date: 08/21/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 136d6248db8012e5870e0627ddbd3703aa63703b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852894"
---
# <a name="create-consumption-reports"></a>Oprette forbrugsrapporter

[!include [banner](../../includes/banner.md)]

 

Når du har oprettet og bogført forbrugsregistreringer på arbejdsordrer i aktivstyring, er der to rapporter tilgængelige til visning af detaljer om forbrug.


## <a name="asset-consumption-report"></a>Forbrugsrapport over aktiv

Når du har bogført forbrug på arbejdsordrer, kan du udskrive en rapport over aktivforbrug. Rapporten viser timer, timeomkostninger, vareomkostninger og udgifter, der er bogført på aktiver.

1. Klik på **Styring af aktiver** > **Rapporter** > **Aktiver** > **Aktivforbrug**.

2. Vælg i dialogboksen **Aktivforbrug** de parametre og det detaljeringsniveau, du vil have vist, ved at vælge **Ja** på de relevante til/fra-knapper, og indsæt et arbejdssted i afsnittet **Vis**.
    - Du kan bruge feltet **Niveauer** til at angive, hvor detaljerede aktivlinjerne skal være i forbindelse med arbejdssteder. 
    
        Hvis du f.eks. indtaster tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle aktiver for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. 
        
        Hvis du indtaster tallet "0" i feltet **Niveauer**, kan du se et detaljeret resultat, der viser alle aktiver på alle de arbejdsstedsniveauer, de er relateret til. 
        
    - Vælg **Ja** på til/fra-knappen **Sum på alle underaktiver** for at få vist summen for hvert underaktiv i rapporten.

3. Vælg et datointerval i sektionen **Datoer**.

4. I oversigtspanelet **Destination** skal du vælge, om du vil have vist rapporten på skærmen, udskrive den eller gemme den som en fil eller mail.

5. Hvis det er nødvendigt, kan du vælge de specifikke aktiver, der skal vises i rapporten. Klik på **Filter** i oversigtspanelet **Poster, der skal indgå**, og tilføj de aktiver, der skal medtages i rapporten.

6. Klik på **OK** for at oprette rapporten.


## <a name="work-order-consumption-report"></a>Forbrugsrapport for arbejdsordre

Når du har bogført forbrug på arbejdsordrer, kan du udskrive en forbrugsrapport for arbejdsordrer. Rapporten viser timer, timeomkostninger, vareomkostninger og udgifter, der er bogført på arbejdsordrer.

1. Klik på **Styring af aktiver** > **Rapporter** > **Arbejdsordrer** > **Forbrug af arbejdsordre**.

2. Vælg i dialogboksen **Forbrug af arbejdsordre** de parametre, du vil medtage i rapporten, ved at vælge **Ja** i de relevante til/fra-knapper i sektionen **Vis**.

3. Vælg et datointerval i sektionen **Datoer**.

4. I oversigtspanelet **Destination** skal du vælge, om du vil have vist rapporten på skærmen, udskrive den eller gemme den som en fil eller mail.

5. Hvis det er nødvendigt, kan du vælge de specifikke arbejdsordrer, der skal vises i rapporten. Klik på **Filter** i oversigtspanelet **Poster, der skal indgå**, og tilføj de arbejdsordrer, der skal medtages i rapporten.

6. Klik på **OK** for at oprette rapporten.


>[!NOTE]
>Du kan også oprette en [arbejdsordrerapport](../work-orders/work-order-report.md), der indeholder flere oplysninger om arbejdsordrer.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]