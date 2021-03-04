---
title: Konfigurere parametre for administration af frynsegoder pr. firma
description: Konfigurere parametre for administration af frynsegoder pr. firma i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
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
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692739"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Konfigurere parametre for administration af frynsegoder pr. firma

For hver organisation, der tilbyder frynsegoder, skal du konfigurere indstillinger for e-mails med bekræftelse af frynsegoder.

## <a name="configure-confirmation-email-settings"></a>Konfigurere indstillinger for e-mails om frynsegoder

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for personale** under **Konfiguration**.

2. Angiv værdier for følgende felter under fanen **Frynsegodeadministration**: 

   | Felt | Betegnelse |
   | --- | --- |
   | **Send bekræftelsesmail** | Når denne funktion er slået til, sendes der en bekræftelses-e-mail til medarbejdere, når de tjekker ud fra frynsegodetilmeldingsoplevelsen i Employee Self-Service. |
   | **Skabelon for bekræftelsesmail** | Vælg den skabelon til organisationsmail, der skal bruges, når tilmeldingsbekræftelsen sendes. Hvis du ikke vælger en skabelon, sendes der følgende generiske e-mail:<br><br>%EmployeeFirstName%,<br><br>Tillykke! Du har fuldført tilmeldingen til frynsegoder.<br><br>Tak<br><Firma/Organisationsnavn> Frynsegoder. |
   | **Afsenderadresse for standardmail** | Den e-mailadresse, der skal bruges ved afsendelse af bekræftelsesmailen. |

3. Vælg **Gem**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]