---
title: Konfigurere fremtidige livshændelser
description: Du kan planlægge fremtidige livshændelser i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 655070e52e3d1f43ca6904ce3218582868f193fe
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008501"
---
# <a name="configure-future-life-events"></a>Konfigurere fremtidige livshændelser

[!include [banner](includes/preview-feature.md)]

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
