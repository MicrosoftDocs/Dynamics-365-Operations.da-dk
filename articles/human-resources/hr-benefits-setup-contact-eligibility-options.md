---
title: Konfigurere indstillinger for personlig kontaktberettigelse
description: Denne artikel forklarer, hvordan du angiver indstillinger for berettigelsesindstillinger for personlige kontakter i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 251a12b0da364744f1d8c84324099708a2f816a1
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749276"
---
# <a name="configure-personal-contact-eligibility-options"></a>Konfigurere indstillinger for personlig kontaktberettigelse


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver, hvordan du kan konfigurere typerne af personlige kontakter, som kan bruges i frynsegoder i Microsoft Dynamics 365 Human Resources. Personlige kontakter er de personer, som er omfattet af dine planer (afhængige), eller som vil få glæde af dine planer (modtagere). Afhængige er typisk ægtefæller eller børn. Modtagere kan være ægtefæller, børn, betroede personer eller forældre.

1. Vælg **Indstillinger for berettigelse for personlige kontakter** under **Konfiguration** i arbejdsområdet **Frynsegodeadministration**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Berettigelsesindstilling** | Et entydigt navn eller en entydig kode, der identificerer indstillingen for berettigelse. |
   | **Beskrivelse** | En kort beskrivelse af indstillingen for berettigelse. |
   | **Kode for kontaktberettigelse** | Den systemkode, der bedst beskriver indstillingen for personlig berettigelse. Du kan vælge mellem følgende: <ul><li>Relation</li><li>Studerende</li><li>Afhængigt af overskydende beløb</li><li>For gammel deaktiveret afhængig</li></ul> |
   | **Status** | Statussen for berettigelsesindstillingen. Hvis status for en berettigelsesindstilling er angivet til inaktiv, kan du ikke vælge denne berettigelsesindstilling for personlige kontakter. |
   | **Relation** | Angiver forholdet mellem den personlige kontaktperson og medarbejderen. Dette felt er kun aktivt, hvis koden for kontaktberettigelse er angivet til Relation. |
   | **Alder** | Den mindste alder for en berettiget personlig kontaktperson for frynsegodeplanen. Dette felt er kun aktivt, hvis du vælger en relation. Denne alder sammenlignes med den beregnede alder for den personlige kontakt. Beregnet alder er: (dækningsdato – personlig kontakts fødselsdato/365). Dette tal er altid et heltal. |

4. Vælg **Gem**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
