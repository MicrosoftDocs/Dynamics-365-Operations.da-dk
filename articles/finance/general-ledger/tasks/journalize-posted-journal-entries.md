---
title: Journalisere bogførte kladdeposter
description: Denne procedure viser, hvordan du journaliserer bogførte kladdeposter.
author: aprilolson
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5028db1db2359a54d565fc299c9a3353a4cf8297
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826148"
---
# <a name="journalize-posted-journal-entries"></a>Journalisere bogførte kladdeposter

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du journaliserer bogførte kladdeposter. Proceduren bruger USMF-demodatafirmaet.

1. Gå i **Navigationsrude** til **Moduler > Finans > Opsætning Finans > Finansparametre**.
2. Feltet **Udvidet finanskladde** kan være angivet til Ja eller Nej. Hvis angivet til Ja, vil rapportens output være forskellig.
3. Vælg, om perioden kan lukkes, hvis journaliseringsprocessen endnu ikke er blevet kørt. Hvis denne indstilling er angivet til Ja, kan perioden ikke lukkes, før journaliseringsprocessen er fuldført for den pågældende periode.  
4. Luk siden.
5. Gå i **Navigationsrude** til **Moduler > Finans > Periodiske opgaver > Journalisering**.
6. Klik på **Filtrér**.
7. Fremhæv de rækker med filtreringskriterier, som du vil definere.
8. Indtast eller vælg filtreringskriterierne i feltet **Kriterier**.
9. Klik på **OK** for at lukke filtreringssiden.
10. Klik på **OK** for at starte journaliseringsprocessen. Der genereres en rapport, når processen er fuldført.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]