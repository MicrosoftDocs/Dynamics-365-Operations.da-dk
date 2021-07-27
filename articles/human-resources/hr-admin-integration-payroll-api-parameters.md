---
title: Parametre for lønintegration
description: Dette emne beskriver parametrene for Dynamics 365 Human Resources-lønintegration.
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f76ce395d7f5a82ab622dd323aee52a39b09847
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314352"
---
# <a name="payroll-integration-parameters"></a>Parametre for lønintegration

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Før du bruger lønintegration i Dynamics 365 Human Resources, skal du konfigurere de parametre, der er beskrevet i dette emne.

## <a name="enable-payroll-address"></a>Aktivere lønadresse

Hvis du vil bruge lønadressen, skal du aktivere den fra [formularen Delte parametre](hr-setup-shared-parameters.md) under fanen Lønintegration.

## <a name="define-the-identification-type"></a>Angive identifikationstypen

Hvis du vil have vist identifikationstype-id i [objektet Lønmedarbejder](hr-admin-integration-payroll-api-payroll-employee.md), skal du [konfigurere Human Resources-parametre](hr-setup-shared-parameters.md) for de enkelte virksomheder.

1. I arbejdsområdet **Kompensationsstyring** skal du vælge **Parametre for Human Resources** under links. 
2. Angiv værdien i følgende felter under fanen **Lønintegration**.

| Felt | Betegnelse |
| --- | --- |
| Brug identifikationstyper i lønbehandling | Når denne indstilling er valgt, vises det valgte type-id i objektet Lønmedarbejder. |
| Identifikationstype | Den identifikationstype, der skal vises i feltet **mshr_payrollemployeeentityid** for [objektet Lønmedarbejder](hr-admin-integration-payroll-api-payroll-employee.md). |

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]