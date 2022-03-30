---
title: Journalisere bogførte kladdeposter
description: Denne procedure viser, hvordan du journaliserer bogførte kladdeposter.
author: aprilolson
ms.date: 03/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d8fca167563b14c825ebe29874c6488ddfb4d9a
ms.sourcegitcommit: 06acdfbccd7bd213a2397ea7b85d104f01914437
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/10/2022
ms.locfileid: "8400869"
---
# <a name="journalize-posted-journal-entries"></a>Journalisere bogførte kladdeposter

[!include [banner](../../includes/banner.md)]

Journaliseringsprocessen i finansmodulet giver dig mulighed for at gruppere og rapportere om bogførte bilagsposter i finansmodulet. Ud fra de kriterier, du angiver, genererer behandlingen en liste over bilag, der bruger en entydig nummerserie, og som har værdien af **Kladdenummer** for finans som reference.

Følg disse trin for at journalisere bogførte kladdeposter. Denne procedure bruger demodatafirmaet **USMF**.

1. Gå til **Finans** \> **Opsætning Finans** \> **Finansparametre**.
2. Vælg en værdi i feltet **Udvidet finanskladde**. Hvis du vælger **Ja**, vil rapportens output være anderledes.
3. Vælg, om perioden kan lukkes, hvis journaliseringsprocessen endnu ikke er blevet kørt. Hvis du vælger **Ja**, kan perioden ikke lukkes, før journaliseringsprocessen er fuldført for den pågældende periode.
4. Luk siden.
5. Gå til **Finans** \> **Periodiske opgaver** \> **Journalisering**, og vælg **Filter**.
6. Vælg rækken for de filtreringskriterier, som du vil definere.
7. Indtast eller vælg filtreringskriterierne i feltet **Kriterier**.
8. Vælg **OK** for at lukke siden.
9. Vælg **OK** for at starte journaliseringsprocessen. Der genereres en rapport, når processen er fuldført.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
