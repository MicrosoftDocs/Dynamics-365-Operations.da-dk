---
title: Konfigurere fradrag
description: Du kan bruge fradrag i Microsoft Dynamics 365 Human Resources til at afgøre, hvor meget der eventuelt skal trækkes fra en medarbejders løn for hvert enkelt frynsegode.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c59fa09e83ca91e0ad866e5875ff06370b7491d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417723"
---
# <a name="configure-deductions"></a>Konfigurere fradrag

Du kan bruge fradrag i Microsoft Dynamics 365 Human Resources til at afgøre, hvor meget der eventuelt skal trækkes fra en medarbejders løn for hvert enkelt frynsegode. Fradrag gælder for datoer, så du kan bevare en historisk oversigt over oplysninger om fradrag. 

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Fradrag** under **Konfiguration**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Fradrag** | Et entydigt id, der bruges til at identificere frynsegodefradraget. |
   | **Beskrivelse** | En beskrivelse af fradraget. |
   | **Gyldig** | Startdatoen. Standardværdien er den aktuelle systemdato. |
   | **Udløb** | Slutdatoen. Standardværdien er 31-12-2154, som angiver aldrig. |
   | **Overskrift** | Overskriftskoden fra det lønsystem, som dette fradrag vil bruge til medarbejderdelen af fradraget ved behandling af frynsegoder i forbindelse med løn. Den bruges, når du bruger en tredjepartslønudbyder. |
   | **Reference for medarbejders lønfradrag** | Fradragskoden fra det lønsystem, som dette fradrag bruger for medarbejderdelen af fradraget, når der behandles frynsegoder til løn. |
   | **Beløbsoverskrift** | Overskriftskoden fra det lønsystem, som dette fradragsbeløb vil bruge til medarbejderdelen af fradraget ved behandling af frynsegoder i forbindelse med løn. Den bruges normalt, når du bruger en tredjepartslønudbyder. |
   | **Kan slette** | Angiver, om en eksporteret værdi fra Dynamics 365 for Finance and Operations kan forårsage, at værdien slettes i lønsystemet. |
   | **Parrede kolonner** | Angiver, om der skal eksporteres overskrifts- og fradragsbeløb i parrede tilstødende kolonner til lønsystemet. |
   | **Skift ikrafttrædelsesdato** | Den dato, hvor ændringen af frynsegodefradraget træder i kraft. På denne dato ændrer systemet automatisk frynsegodefradraget og opdaterer alle de frynsegodeplaner, der er tilknyttet fradraget, hvis du kører behandling af **Opdatering af ændret fradrag**. |
   | **Ændring af fradrag fuldført** | Afkrydsningsfeltet **Ændret fradrag er fuldført** markeres automatisk, når ændringen af frynsegodefradraget er fuldført af fradrag af behandlingen af opdatering af ændret fradrag. |
   
4. Hvis du vil spore og vedligeholde ændringer af opsætningen af frynsegodesatsen, skal du vælge **Handlinger** og derefter vælge **Vedligehold versioner**.

5. Vælg **Gem**. 
