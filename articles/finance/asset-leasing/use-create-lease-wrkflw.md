---
title: Bruge arbejdsgange for leasinggodkendelse
description: I dette emne forklares, hvordan du kan bruge arbejdsgange til at godkende aktivleasingaftaler, og hvordan du kan følge op på arbejdsgangernes status og historik.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1086231c65a726df5162d3593419a129d6ae5655
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992752"
---
# <a name="use-lease-approval-workflows"></a>Bruge arbejdsgange for leasinggodkendelse

[!include [banner](../includes/banner.md)]

I dette emne forklares, hvordan du kan bruge arbejdsgange til at godkende aktivleasingaftaler, og hvordan du kan følge op på arbejdsgangernes status og historik. Arbejdsgange medvirker til administration af godkendelser af leasingaftaler ved at levere et standardsæt med godkendelsestrin og tildele bestemte brugere, der godkender hvert trin i processen. En godkender kan godkende en leasingaftale, afvise den, anmode om en ændring på den eller tildele den til en anden bruger til godkendelse. Arbejdsgange kan også give godkendelsesprocessen flere oplysninger ved at lade dig spore deres status og historik. Derudover kan du få vist en centraliseret arbejdsliste, der viser de opgaver og godkendelser, der er tildelt bestemte godkendere.

Før du bruger denne procedure, skal du kontrollere, at der er oprettet mindst en leasinggodkendelse til arbejdsgangen. Hvis der ikke findes en arbejdsgang, skal du oprette en. Du kan finde flere oplysninger om konfiguration af arbejdsgangen i [Konfigurere arbejdsgange for leasinggodkendelse](set-up-lease-wrkflw.md).

1. Sende en leasing til godkendelse. På siden **Kartoteksoplysninger** skal du vælge **Arbejdsgang** og derefter **Send** for leasingaftalen.
2. Du kan tilføje en kommentar i den dialogboks, der vises. Den angivne godkender får vist denne kommentar sammen med leasingaftalen. Når du er færdig med at skrive kommentaren, skal du vælge **Send**. Leasingaftalen sendes til arbejdsgangssystemet, og godkenderen modtager den til godkendelse.
3. Hvis du vil have vist de leasingaftaler, de er udpeget til godkendelse, skal du gå til **Moduler \> Almindelig \> Arbejdsemner \> Arbejdsemner, der er tildelt til mig**.
4. På siden **Arbejdsemner, der er tildelt til mig**, skal du vælge det **Leasing-id**-link for den leasingaftale, du vil have vist. Den side, der vises, afhænger af de leasingkartoteker og de leasingoplysninger, du har adgang til.
5. Når du er færdig med at få vist leasingaftalen, skal du vælge **Arbejdsgang** og beslutte, hvilken handling der skal udføres. Indstillingerne omfatter **Godkend**, **Afvist**, **Anmodning om ændring**, **Deleger** og **Annulleret**. Du kan også vælge **Vis historik** for at få vist godkendelseshistorikken for den valgte leasingaftale.
6. Når du har valgt en handling, skal du angive en kommentar, der beskriver aktionen. Når du er færdig med at angive kommentaren, skal du vælge den **Godkendte** på listen.
7. Hvis du vil have vist godkendelseshandlingerne, skal du gå tilbage til siden **Leasingoplysninger** fra siden **Leasingoversigt** og derefter vælge **Arbejdsproces \> Vis historik**.

    Du kan få vist arbejdsgangsaktiviteterne på siden **Arbejdsgangshistorik**. Denne side viser de arbejdsgangstrin, der er blevet udført på den specifikke leasingaftale. Du kan også bruge feltet **Arbejdsposter** til at få vist status for de tildelte arbejdsprocesopgaver.

8. Hvis du vil standse en arbejdsproces, skal du vælge **Arbejdsproceshistorik** og **Tilbagekald**. I dialogboksen skal du angive en kommentar og derefter vælge **OK**.
9. Hvis du vil deaktivere en arbejdsgang eller aktivere en arbejdsgang, der tidligere er oprettet, skal du gå til **Aktivleasing \> Opsætning \> Leasingarbejdsproces**. Derefter skal du vælge **Leasingarbejdsproces** og **Arbejdsproces \> Versioner**. Hvis du vil gøre en arbejdsproces inaktiv, skal du vælge den aktive leasingaftale i dialogboksen og derefter vælge **Gør inaktiv**. Hvis du vil aktivere en eksisterende arbejdsproces, skal du vælge arbejdsprocessen og derefter vælge **Gør aktiv**.
