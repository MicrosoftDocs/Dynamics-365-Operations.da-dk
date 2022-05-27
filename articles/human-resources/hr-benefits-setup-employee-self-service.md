---
title: Konfigurere medarbejderselvbetjening
description: I Microsoft Dynamics 365 Human Resources kan du konfigurere felter til navigation på øverste niveau i medarbejderselvbetjening.
author: twheeloc
ms.date: 12/06/2021
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
ms.openlocfilehash: d7ddb1f1ea74a16265dac701151b2c25a4f9d4dc
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687157"
---
# <a name="configure-employee-self-service"></a>Konfigurere medarbejderselvbetjening


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I Microsoft Dynamics 365 Human Resources kan du konfigurere felter til navigation på øverste niveau i **Medarbejderselvbetjening**. Frynsegodeplansfelter sender brugere videre til frynsegodeplaner, som de er berettiget til.

## <a name="set-up-a-benefit-plans-tile"></a>Konfigurere et felt til frynsegodeplaner

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for medarbejdsselvbetjening** under **Konfiguration**.

2. Vælg fanen **Konfigurer felt til frynsegodeplaner**, og vælg derefter **Ny**.

3. Angiv værdier for følgende felter.

   | Felt | Beskrivelse |
   | --- | --- |
   | **Kode for plantype** | Den plantype, der vises, når dette felt er valgt i **Selvbetjening for personalegoder**. |
   | **Felt-id** | Entydigt id for feltet. |
   | **Feltlabeltekst** | Den tekst, der vises for feltet i **Selvbetjening for personalegoder**. |
   | **Beskrivelse** | En beskrivelse af feltet. |
   | **Feltbaggrundsbillede** | URL-adressen for det billede, der skal bruges til feltet (valgfrit). |
   | **Spor åben tilmelding** | Vælg denne indstilling, hvis du vil spore status for åben tilmelding til denne plantype. Der kan for eksempel være oprettet planer, hvor **Plantype = Andet**. Disse planer kan være valgfrie planer, som du ikke ønsker at spore status for tilmeldinger for. Hvis du ikke vælger denne plantype, ignoreres planer af denne type, når der spores status for tilmelding eller fuldførelse af tilmelding under fanen **Åben tilmelding**. Denne indstilling gælder for den plantype, der er valgt for alle perioder og juridiske enheder. |

4. Vælg **Gem**.

## <a name="set-up-a-flex-credit-plan-tile"></a>Konfigurere et felt for flekskreditplan

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for medarbejdsselvbetjening** under **Konfiguration**.

2. Vælg fanen **Konfigurer felt til flekskreditplan**, og vælg derefter **Ny**.

3. Angiv værdier for følgende felter.

   | Felt | Beskrivelse |
   | --- | --- |
   | **Personalegodekredit-id** | De flekskreditprogramplaner, der vises, når dette felt er valgt i **Selvbetjening for personalegoder**. |
   | **Felt-id** | Entydigt id for feltet. |
   | **Feltlabeltekst** | Den tekst, der vises for feltet i **Selvbetjening for personalegoder**. |
   | **Beskrivelse** | En beskrivelse af feltet. |
   | **Feltbaggrundsbillede** | URL-adressen for det billede, der skal bruges til feltet (valgfrit). |
   | **Spor åben tilmelding** | Vælg denne indstilling, hvis du vil spore status for åben tilmelding til denne plantype. Der kan for eksempel være oprettet planer, hvor **Plantype = Andet**. Disse planer kan være valgfrie planer, som du ikke ønsker at spore status for tilmeldinger for. Hvis du ikke vælger denne plantype, ignoreres planer af denne type, når der spores status for tilmelding eller fuldførelse af tilmelding under fanen **Åben tilmelding**. Denne indstilling gælder for den plantype, der er valgt for alle perioder og juridiske enheder. |

4. Vælg **Gem**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
