---
title: Behandle satsændringer
description: Denne artikel forklarer, hvordan du behandler ændringer af frynsegodesatser i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 09714c70cb00b1a1b5dbd4613bbd70ff11d35cb2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882947"
---
# <a name="process-rate-changes"></a>Behandle satsændringer


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel forklarer, hvordan du behandlinger ændringer af frynsegodesatser i Microsoft Dynamics 365 Human Resources, når en ny eller eksisterende frynsegodeplan indeholder ændrede indstillinger for berettigelsesregler. Hvis der oprettes en ny berettigelsesregel, som tildeles til planen, bliver systemet bedt om at køre medarbejderberettigelse igen for at kontrollere, om arbejdere nu er berettiget til planen baseret på nye indstillinger for berettigelse. 

1. Vælg **Behandling af opdateret satsændring** under **Behandling** i arbejdsområdet **Frynsegodeadministration**.

2. Angiv værdier for følgende felter i dialogboksen **Kør behandling af opdateret frynsegodesats**:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Tilmeldingsperiode** | Den tilmeldingsperiode, som satsændringer skal behandles for. |

3. Hvis du vil køre processen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:

   1. Angiv oplysninger om processen.

   2. Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.

   3. Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.

   4. Vælg **OK**. Processen køres med de parametre, du angiver.

4. Vælg **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
