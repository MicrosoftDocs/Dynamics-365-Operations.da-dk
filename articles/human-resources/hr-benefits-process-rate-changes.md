---
title: Behandle satsændringer
description: Behandle ændringer i frynsegodesatsen i Microsoft Dynamics 365 Human Resources, når en ny eller eksisterende frynsegodeplan har en ændring i indstillingerne for berettigelsesregler.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c87d98a16431805ad652e28e5ca100a4152ad0c6
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466224"
---
# <a name="process-rate-changes"></a>Behandle satsændringer

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Behandle ændringer i frynsegodesatsen i Microsoft Dynamics 365 Human Resources, når en ny eller eksisterende frynsegodeplan har en ændring i indstillingerne for berettigelsesregler. Hvis der oprettes en ny berettigelsesregel, som tildeles til planen, bliver systemet bedt om at køre medarbejderberettigelse igen for at kontrollere, om arbejdere nu er berettiget til planen baseret på nye indstillinger for berettigelse. 

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