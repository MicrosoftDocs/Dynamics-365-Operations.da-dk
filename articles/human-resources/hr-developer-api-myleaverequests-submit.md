---
title: Sende en orlovsanmodning til arbejdsgang
description: I Microsoft Dynamics 365 Human Resources kan du bruge MyLeaveRequests submit()-API'en (Application Programming Interface) til at sende en orlovsanmodning til arbejdsgangen.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 7552a4c921dc4a88034b5d2c87d5a9b47d699ae3
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092008"
---
# <a name="submit-a-leave-request-to-workflow"></a>Sende en orlovsanmodning til arbejdsgang

I Microsoft Dynamics 365 Human Resources kan du bruge MyLeaveRequests submit()-API'en (Application Programming Interface) til at sende en orlovsanmodning til arbejdsgangen. Denne API vises som en handling i MyLeaveRequests OData-enheden.

## <a name="prerequisites"></a>Forudsætninger

Orlovsanmodningen skal gemmes i databasen og skal kunne hentes via MyLeaveRequests-enheden.

## <a name="permissions"></a>Tilladelser

En af følgende tilladelser kræves for at kalde denne API. Du kan finde flere oplysninger om tilladelser, og hvordan du vælger dem, i [Godkendelse](hr-developer-api-authentication.md).

| Tilladelsestype                    | Tilladelser (fra færrest til flest rettigheder) |
|------------------------------------|--------------------------------------------------------|
| Delegeret (arbejds- eller skolekonto) | bruger-\_repræsentation                                    |

## <a name="https-request"></a>HTTPS-anmodning

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

Anmodningen er i overensstemmelse med OData-standarder. Parametrene {requestId}, {leaveType}, {leaveDate} og {dataArea} refererer til de felter, der udgør den sammensatte naturlige nøgle for MyLeaveRequests-enheden.

> [!NOTE]
> Mens felterne for MyLeaveRequests-enheden refererer til en enkelt linje i orlovsanmodningen, vil kald af submit-API'en sende hele orlovsanmodningen (alle linjer) til arbejdsgangen.

### <a name="request-headers"></a>Overskrifter til anmodning

| Header         | Value                     |
|----------------|---------------------------|
| Godkendelse  | Bærer {token} (obligatorisk) |
| Indholdstype   | program/json          |

### <a name="request-body"></a>Anmodningstekst

Du skal ikke angive en anmodningstekst for denne metode.

### <a name="response"></a>Svar

Et vellykket svar er altid svaret **204 intet indhold**.

Uautoriserede opkaldere modtager svaret **401 ikke-godkendt** eller **403 forbudt**.

Hvis afsendelse ikke lykkes (f.eks. pga. validering), vil svaret være **500 serverfejl**, og svarets brødtekst indeholder et JSON-objekt med yderligere oplysninger.

## <a name="example"></a>Eksempel

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a>Validering og fejlmeddelelser

Som led i kaldet til submit-API'en udfører Personale validering af forretningslogik før afsendelse, hvilket sikrer, at orlovsanmodningen er i en gyldig tilstand for afsendelse. De mulige fejlmeddelelser, du kan modtage i svaret, hvis valideringer ikke lykkes, er:

 - Anmodningen ville bringe saldoen '{LeaveTypeId}' ned under den tilladte minimumsaldo på {date}.
 - Anmodning om fridage i afsluttet tilstand kan ikke sendes.
 - Anmodningen kan ikke sendes eller gemmes, da der ikke er foretaget ændringer. Tilføj eller opdater beløbet eller orlovstypen, og prøv igen.
 - Den angivne anmodning om fridage indeholder en eller flere dage med samme dato og orlovstype som en eksisterende ventende anmodning. Tilbagekald den eksisterende anmodning for at foretage ændringer.
 - Årsagskoden '{ReasonCodeId}' kan ikke anvendes til nogen af orlovstyperne i anmodningen.
 - Orlovstypen '{LeaveTypeId}' kræver en årsagskode. Vælg den relevante type og årsagskode.
 - Fritidsanmodningen blev ikke sendt. Anmodningen om fridage er gemt som en kladdeanmodning.

## <a name="see-also"></a>Se også

- [Oversigt over MyLeaveRequests](hr-developer-api-myleaverequests-overview.md)
- [Godkendelse](hr-developer-api-authentication.md)