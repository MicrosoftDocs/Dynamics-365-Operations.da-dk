---
title: Sende en orlovsanmodning til arbejdsgang
description: I Microsoft Dynamics 365 Human Resources kan du bruge MyLeaveRequests submit()-API'en (Application Programming Interface) til at sende en orlovsanmodning til arbejdsgangen.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9a4c472868002c6cae061507bfe2f75d7f3eb86935d69acaac8cb7f2d970bfd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732051"
---
# <a name="submit-a-leave-request-to-workflow"></a>Sende en orlovsanmodning til arbejdsgang

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

Som led i kaldet til submit-API'en udfører Human Resources validering af forretningslogik før afsendelse, hvilket sikrer, at orlovsanmodningen er i en gyldig tilstand for afsendelse. De mulige fejlmeddelelser, du kan modtage i svaret, hvis valideringer ikke lykkes, er:

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]