---
title: Oversigt over MyLeaveRequests
description: MyLeaveRequests-enheden i Microsoft Dynamics 365 Human Resources indeholder listen over orlovsanmodninger i systemet, beregnet (begrænset) til de anmodninger, der er tilgængelige for den aktuelle bruger, der forespørger om enheden.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 90698ddcc8fcf0eb975dffed0bdad11e6b277c90
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984690"
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