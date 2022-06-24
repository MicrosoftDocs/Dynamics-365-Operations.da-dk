---
title: Konfigurere parametre administration af frynsegoder pr. firma
description: Denne artikel beskriver, hvordan du konfigurerer parametre for Frynsegodeadministration pr. firma i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 8/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e9516977002280e17ee82bf7581d8d7c5060de2a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904211"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Konfigurere parametre for administration af frynsegoder pr. firma


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

For hver organisation, der tilbyder frynsegoder, skal du konfigurere indstillinger for emails med bekræftelse af frynsegoder.

## <a name="configure-confirmation-email-settings"></a>Konfigurere indstillinger for emails om frynsegoder

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for personale** under **Konfiguration**.

2. Angiv værdier for følgende felter under fanen **Frynsegodeadministration**: 

   | Felt | Beskrivelse |
   | --- | --- |
   | **Send bekræftelsesmail** | Når denne funktion er aktiveret, sendes der en bekræftelsesmail til medarbejdere, når de logger af frynsegodetilmeldingen i **Medarbejderselvbetjening**. |
   | **Skabelon for bekræftelsesmail** | Vælg den skabelon til organisationsmail, der skal bruges, når tilmeldingsbekræftelsen sendes. Hvis du ikke vælger en skabelon, sendes der følgende generiske email:<br><br>%EmployeeFirstName%,<br><br>Tillykke! Du har fuldført tilmeldingen til frynsegoder.<br><br>Tak<br><Firma/Organisationsnavn> Frynsegoder. |
   | **Afsenderadresse for standardmail** | Den emailadresse, der skal bruges ved afsendelse af bekræftelsesmailen. |

3. Vælg **Gem**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
