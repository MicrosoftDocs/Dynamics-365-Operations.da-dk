---
title: Konfigurere fremtidige livshændelser
description: Dette emne beskriver, hvordan du planlægger fremtidige livshændelser i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 441ccc478f78f76b80ac9138dc62592634f005bd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693193"
---
# <a name="configure-future-life-events"></a>Konfigurere fremtidige livshændelser

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan planlægge fremtidige livshændelser i Dynamics 365 Human Resources.

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Fremtidige livshændelser** under **Konfiguration**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | Dato for livshændelse | Systemet behandler alle hændelser under den tilmeldingsperiode, der indtræffer indtil denne dato. |
   | Livshændelse logført | Dato og klokkeslæt, hvor livshændelsen blev logført. |
   | Logtype | Viser, om handlingen er en af følgende:</br></br>- **Opdater** – en ændring af en eksisterende post, der sporer livshændelser</br></br>- **Indsæt** – oprettelse af en ny livshændelsespost |
   | Livshændelsestype-id | Det entydige id for livshændelsestypen. |
   | Livshændelsestype | En katalysator til opdatering af en medarbejders tilmelding til frynsegoder. Du kan finde flere oplysninger i afsnittet om udløsning af livshændelser. |
   | Status | Angiver, om livshændelsen er behandlet eller ej. |
   | Type | Linjenummeret for den fremtidige livshændelse. |

4. Vælg **Gem**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
