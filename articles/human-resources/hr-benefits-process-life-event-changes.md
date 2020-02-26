---
title: Behandle ændringer af livshændelse
description: Behandl ændringer af livshændelser i Microsoft Dynamics 365 Human Resources for ændringer af livshændelser.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f9bce9394a361bbecfcc0531c5d7ebe9302c8f11
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008499"
---
# <a name="process-life-event-changes"></a>Behandle ændringer af livshændelse

[!include [banner](includes/preview-feature.md)]

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
