---
title: Oversigt over MyLeaveRequests
description: MyLeaveRequests-enheden i Microsoft Dynamics 365 Human Resources indeholder listen over orlovsanmodninger i systemet, beregnet (begrænset) til de anmodninger, der er tilgængelige for den aktuelle bruger, der forespørger om enheden.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803627"
---
# <a name="myleaverequests-overview"></a>Oversigt over MyLeaveRequests

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

MyLeaveRequests-enheden i Microsoft Dynamics 365 Human Resources indeholder listen over orlovsanmodninger i systemet, beregnet (begrænset) til de anmodninger, der er tilgængelige for den aktuelle bruger, der forespørger om enheden.

## <a name="key"></a>Nøgle

  | Egenskabsnavn | Datatype |
  |---------------|-----------|
  | dataAreaId    | Streng    |
  | RequestId     | Streng    |
  | LeaveType     | Streng    |
  | LeaveDate     | Dato      |
  
## <a name="properties"></a>Egenskaber

  | Egenskabsnavn     | Datatype | Obligatorisk |
  |-------------------|-----------|----------|
  | dataAreaId        | Streng    | X        |
  | RequestId         | Streng    | X        |
  | LeaveType         | Streng    | X        |
  | LeaveDate         | Dato      | X        |
  | ReasonCodeId      | Streng    |          |
  | PersonnelNumber   | Streng    | X        |
  | RequestDate       | Dato      | X        |
  | Kommentar           | Streng    |          |
  | Status            | Fasttekst      | X        |
  | Beløb            | Kommatal      |          |
  | HalfDayDefinition | Fasttekst      |          |

## <a name="actions"></a>Handlinger

 | Handlingsnavn                               | Beskrivelse                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [indsend](hr-developer-api-myleaverequests-submit.md)   | Send den anmodning, der skal behandles af arbejdsgangen. |

## <a name="see-also"></a>Se også

- [Sende en orlovsanmodning til arbejdsgang](hr-developer-api-myleaverequests-submit.md)
- [Godkendelse](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]