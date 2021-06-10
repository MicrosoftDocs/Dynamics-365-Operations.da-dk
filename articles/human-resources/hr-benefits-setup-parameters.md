---
title: Angive parametre for frynsegodeadministration og Employee Self-Service for alle firmaer
description: Konfigurere parametre for frynsegodeadministration og Employee Self-Service i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d668238378e41287c7a9f845ae3e67078fc7776a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058962"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a>Angive parametre for frynsegodeadministration og Employee Self-Service for alle firmaer

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Før du kan oprette frynsegodeplaner i Microsoft Dynamics 365 Human Resources, skal du konfigurere parametre for administration af frynsegoder. Disse parametre angiver standardværdier, årsagskoder og andre indstillinger. 

## <a name="configure-general-parameters"></a>Konfigurere generelle parametre

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Delte Human Resources-parametre** under **Konfiguration**.

2. Angiv værdier for følgende felter under fanen **Frynsegodeadministration**:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Land/område** | Feltet **Land/område** bestemmer, hvilken visningsrækkefølgen for postnumre/stater. Det valgte land vises først på rullelisten. |
   | **Årsagskode for tilmelding** | Vælg en standardårsagskode, der skal bruges, når der oprettes medarbejderplaner under behandling af en åben tilmelding. |
   | **Årsagskode for annullering** | Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan annulleres. Den vises i en dialogboks under annulleringsprocessen. Brugerne kan eventuelt ændre den i **Årsagskode til annullering**. |
   | **Årsagskode for genåbning** | Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan genåbnes. Den vises i en dialogboks under annulleringsprocessen. Brugerne kan eventuelt ændre den i **Åbn årsagskode igen**. | 
   | **Årsagskode for livshændelse** | Den årsagskode, der skal bruges, når der indtræffer en livshændelse. |
   | **Årsagskode for satsændring** | Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan annulleres og genåbnes under behandlingen af opdateret satsændring. Den angiver, hvilke poster der er ændret af opdateringsprocessen for satsændringen. |
   | **Årlig løn som personalegoder** | Giver dig mulighed for at angive et beløb for **Årlig frynsegodeløn** for en medarbejder. Human Resources skal bruge beløbet for **Årlig frynsegodeløn** til bestemmelse af dækningsbeløb i stedet for det årlige beløb for fast løn. |
   | **Ny ansættelse berettiget** | Angiver, om nyansatte er berettigede. |
   | **Periode for tilmelding af nyansat** | Den tidsperiode, hvor tilmelding for den nyansatte er tilladt.</br></br>**Bemærk** Denne indstilling tilsidesætter en eventuel tilmeldingsperiode for nyansatte, som du angiver for berettigelsesreglen for planen. |
   | **Standardlønfrekvens** | Den standardlønsats, der skal bruges, når der tilføjes nye arbejdere. |
   | **Livshændelser er aktiveret** | Aktiverer levetidshændelser. |
   | **Skjul formularer for ældre personalegoder** | Giver dig mulighed for at skjule ældre frynsegodeformularer. |
   | **Frynsegodebekræftelse** | Den kontroltekst, der skal bruges under betaling af selvbetjeningsfrynsegoder. |
   | **Vælg automatisk udpegede modtagere** | Angiver, om der automatisk skal vælges afhængige og modtagere baseret på deres berettigelse til planindstillinger. |

3. Vælg **Gem**.

## <a name="configure-employee-self-service-parameters"></a>Konfigurere parametre for Employee Self-Service

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for personale** under **Konfiguration**.

2. Angiv værdier for følgende felter under fanen **Frynsegodeadministration**:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Frynsegodebekræftelse** | Den kontroltekst, der skal bruges under betaling af selvbetjeningsfrynsegoder. |
   | **Vælg automatisk udpegede modtagere** | Angiver, om der automatisk skal vælges afhængige og modtagere baseret på deres berettigelse til planindstillinger. |

3. Vælg **Gem**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]