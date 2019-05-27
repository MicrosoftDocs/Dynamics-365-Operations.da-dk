---
title: Journalisere bogførte kladdeposter
description: Denne procedure viser, hvordan du journaliserer bogførte kladdeposter.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b50809cf9eb59475856f91d9f1ddfe28ecfd8de6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547904"
---
# <a name="journalize-posted-journal-entries"></a>Journalisere bogførte kladdeposter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du journaliserer bogførte kladdeposter. Proceduren bruger USMF-demodatafirmaet.

1. Valider indstillingerne for journalisering under Finans > Opsætning Finans > Finansparametre.
2. Feltet Udvidet finanskladde kan være angivet til Ja eller Nej. Hvis angivet til Ja, vil rapportens output være forskellig.
3. Vælg, om perioden kan lukkes, hvis journaliseringsprocessen endnu ikke er blevet kørt.
    * Hvis denne indstilling er angivet til Ja, kan perioden ikke lukkes, før journaliseringsprocessen er fuldført for den pågældende periode.  
4. Luk siden.
5. Gå til Finans > Periodiske opgaver > Journalisering.
6. Klik på Filtrér.
7. Fremhæv de rækker med filtreringskriterier, som du vil definere.
8. Indtast eller vælg filtreringskriterierne i feltet Kriterier.
9. Klik på OK for at lukke filtreringssiden.
10. Klik på OK for at starte journaliseringsprocessen.
    * Der genereres en rapport, når processen er fuldført.  

