---
title: Behandle ændringer af livshændelser
description: Dette emne forklarer, hvordan du kan behandle ændringer af livshændelser i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 30834b685c535d464dbe016d92579752fac4b7fa
ms.sourcegitcommit: 4f9c889e5cf72f34dd9746a322f8c0d6b983037b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/25/2021
ms.locfileid: "7417451"
---
# <a name="process-life-event-changes"></a>Behandle ændringer af livshændelser

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Behandl ændringer af livshændelser i Microsoft Dynamics 365 Human Resources for to ændringer af livshændelser:

- Fødselsdagsændringer
- Berettigelsesregel tilsidesætte udløbsændringer 

1. Vælg **Behandling af ændringer af livshændelse** under **Behandling** i arbejdsområdet **Frynsegodeadministration**.

2. Angiv værdier for følgende felter i dialogboksen **Kør behandling af ændringer af livshændelse**:

   | Felt | Beskrivelse |
   | --- | --- |
   | Tilmeldingsperiode | Den tilmeldingsperiode, der skal behandles ændringer af livshændelse for. |
   | Juridisk enhed | Den juridiske enhed, der skal behandles ændringer af livshændelse for. |

3. Hvis du vil køre processen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:

   1. Angiv oplysninger om processen.

   2. Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.

   3. Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.

   4. Vælg **OK**. Processen køres med de parametre, du angiver.

4. Vælg **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
