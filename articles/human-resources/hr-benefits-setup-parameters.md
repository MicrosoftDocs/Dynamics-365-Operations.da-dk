---
title: Angive parametre for administration af frynsegoder
description: Konfigurere parametre for administration af frynsegoder i Microsoft Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3e001c08751ea9c8bcab0e11a04b6cf639e51d1d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429977"
---
# <a name="set-benefits-management-parameters"></a>Angive parametre til administration af frynsegoder

Før du kan oprette orlovsplaner i Microsoft Dynamics 365 Human Resources, skal du konfigurere parametre for administration af frynsegoder. Disse parametre angiver standardværdier, årsagskoder og andre indstillinger.

## <a name="configure-general-parameters"></a>Konfigurere generelle parametre

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre** under **Konfiguration**.

2. Angiv værdier for følgende felter under fanen **Generelt**:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Land/område** | Feltet **Land/område** bestemmer, hvilken visningsrækkefølgen for postnumre/stater. Det valgte land vises først på rullelisten. |
   | **Årsagskode for tilmelding** | Vælg en standardårsagskode, der skal bruges, når der oprettes medarbejderplaner under behandling af en åben tilmelding. |
   | **Årsagskode for annullering** | Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan annulleres. Den vises i en dialogboks under annulleringsprocessen. Brugerne kan eventuelt ændre den i **Årsagskode til annullering**. |
   | **Årsagskode for genåbning** | Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan genåbnes. Den vises i en dialogboks under annulleringsprocessen. Brugerne kan eventuelt ændre den i **Åbn årsagskode igen**. | 
   | **Årsagskode for livshændelse** | Den årsagskode, der skal bruges, når der indtræffer en livshændelse. |
   | **Årsagskode for satsændring** | Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan annulleres og genåbnes under behandlingen af opdateret satsændring. Den angiver, hvilke poster der er ændret af opdateringsprocessen for satsændringen. |
   | **Ny ansættelse berettiget** | Angiver, om nyansatte er berettigede. |
   | **Periode for tilmelding af nyansat** | Den tidsperiode, hvor tilmelding for den nyansatte er tilladt.</br></br>**Bemærk** Denne indstilling tilsidesætter en eventuel tilmeldingsperiode for nyansatte, som du angiver for berettigelsesreglen for planen. | 
   | **Livshændelser er aktiveret** | Aktiverer levetidshændelser. |
   | **Skjul formularer for ældre frynsegoder** | Giver dig mulighed for at skjule ældre frynsegodeformularer. |

3. Vælg **Gem**.

## <a name="configure-employee-self-service-parameters"></a>Konfigurere parametre for medarbejderselvbetjening

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre** under **Konfiguration**.

2. Angiv værdier for følgende felter under fanen **Medarbejderselvbetjening**:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Frynsegodebekræftelse** | Den kontroltekst, der skal bruges under betaling af selvbetjeningsfrynsegoder. |
   | **Vælg automatisk udpegede modtagere** | Angiver, om der automatisk skal vælges afhængige og modtagere baseret på deres berettigelse til planindstillinger. |

3. Vælg **Gem**.
