---
title: Konfigurere arbejdsgange for leasinggodkendelse
description: I emnet forklares det, hvordan du opretter en godkendelsesarbejdsgang, der skal køres, når der oprettes en ny leasingaftale.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 58c0fd781710b7ab8efeaa7a6874f412279a5924
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441748"
---
# <a name="set-up-lease-approval-workflows"></a>Konfigurere arbejdsgange for leasinggodkendelse

[!include [banner](../includes/banner.md)]

I emnet forklares det, hvordan du opretter en godkendelsesarbejdsgang, der skal køres, når der oprettes en ny leasingaftale. Du kan finde flere oplysninger om, hvordan du bruger arbejdsgangen, i [Bruge arbejdsgange for leasinggodkendelse](use-create-lease-wrkflw.md). 

1. Gå til **Aktivleasing \> Konfiguration \> Leasingarbejdsproces**.
2. På siden **Leasingarbejdsproces** skal du vælge **Ny**.
3. I den dialogboks, der vises, skal du under **Arbejdsprocestype** vælge linket **Leasingarbejdsproces**.

    Ansøgningen åbnes. Når den er kørt, skal du logge på Azure Active Directory (Azure AD) for at blive omdirigeret til arbejdsprocesprogrammet.

4. Træk **Godkendelse af leasingarbejdsproces** til arbejdsprocessen.
5. Forbind en node fra **Start** til **Godkendelse af leasingarbejdsproces**. Forbind derefter **Godkendelse af leasingarbejdsproces** til **Slut**.
6. Dobbeltklik på **Godkendelse af leasingarbejdsproces**.
7. Vælg **Egenskaber** og angiv derefter under **Grundlæggende indstillinger** et navn til arbejdsgangen.

    På denne side kan du også angive flere parametre for arbejdsgangen. Hvis du har aktiveret **Automatiske aktioner**, vil systemet automatisk udføre en bestemt handling. Notifikationer kan sendes, hvis de er angivet under fanen **Notifikationer**. Under fanen **Avancerede indstillinger** kan du angive en endelig godkender, angive en tidsgrænse og angive bestemte handlinger, der skal være fuldført.

8. Vælg **Luk**, når du er færdig med at angive arbejdsprocesparametrene.
9. Vælg **Trin 1** og derefter **Egenskaber**.
10. Angiv et navn til trinnet under **Grundlæggende indstillinger**, opret en emnelinje til godkendelsen, og angiv instruktioner til godkendelsen.
11. Vælg tildelingstypen på siden **Tildeling**.
12. Hvis du vil tildele specifikke brugere til godkendelsen, skal du vælge **Bruger**, vælge de brugere, der godkender leasingaftaler og derefter vælge **Luk**.
13. Vælg **Gem og luk** for at oprette arbejdsprocessen. Vælg derefter **OK**, når du bliver bedt om det.
14. På siden **Opret arbejdsproces** skal du vælge **luk**.
14. Vælg den nye arbejdsproces, og vælg derefter **Versioner**. Vælg derefter **Gør aktiv** for at sikre, at arbejdsgangen er aktiv.
15. Vælg **Luk**. Den nye aktive version vises.
