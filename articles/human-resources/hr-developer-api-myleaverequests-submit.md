---
title: Sende en orlovsanmodning til arbejdsgang
description: ''
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
ms.openlocfilehash: 008ee231ca9f0459e332b17cea9f2a3f3e3cc2a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008534"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="e3285-102">Sende en orlovsanmodning til arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="e3285-102">Submit a leave request to workflow</span></span>

<span data-ttu-id="e3285-103">I Microsoft Dynamics 365 Human Resources kan du bruge MyLeaveRequests submit()-API'en (Application Programming Interface) til at sende en orlovsanmodning til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="e3285-103">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="e3285-104">Denne API vises som en handling i MyLeaveRequests OData-enheden.</span><span class="sxs-lookup"><span data-stu-id="e3285-104">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e3285-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="e3285-105">Prerequisites</span></span>

<span data-ttu-id="e3285-106">Orlovsanmodningen skal gemmes i databasen og skal kunne hentes via MyLeaveRequests-enheden.</span><span class="sxs-lookup"><span data-stu-id="e3285-106">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="e3285-107">Tilladelser</span><span class="sxs-lookup"><span data-stu-id="e3285-107">Permissions</span></span>

<span data-ttu-id="e3285-108">En af følgende tilladelser kræves for at kalde denne API.</span><span class="sxs-lookup"><span data-stu-id="e3285-108">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="e3285-109">Du kan finde flere oplysninger om tilladelser, og hvordan du vælger dem, i [Godkendelse](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="e3285-109">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="e3285-110">Tilladelsestype</span><span class="sxs-lookup"><span data-stu-id="e3285-110">Permission type</span></span>                    | <span data-ttu-id="e3285-111">Tilladelser (fra færrest til flest rettigheder)</span><span class="sxs-lookup"><span data-stu-id="e3285-111">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="e3285-112">Delegeret (arbejds- eller skolekonto)</span><span class="sxs-lookup"><span data-stu-id="e3285-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e3285-113">bruger-\_repræsentation</span><span class="sxs-lookup"><span data-stu-id="e3285-113">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="e3285-114">HTTPS-anmodning</span><span class="sxs-lookup"><span data-stu-id="e3285-114">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="e3285-115">Anmodningen er i overensstemmelse med OData-standarder.</span><span class="sxs-lookup"><span data-stu-id="e3285-115">The request conforms to OData standards.</span></span> <span data-ttu-id="e3285-116">Parametrene {requestId}, {leaveType}, {leaveDate} og {dataArea} refererer til de felter, der udgør den sammensatte naturlige nøgle for MyLeaveRequests-enheden.</span><span class="sxs-lookup"><span data-stu-id="e3285-116">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="e3285-117">Mens felterne for MyLeaveRequests-enheden refererer til en enkelt linje i orlovsanmodningen, vil kald af submit-API'en sende hele orlovsanmodningen (alle linjer) til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="e3285-117">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="e3285-118">Overskrifter til anmodning</span><span class="sxs-lookup"><span data-stu-id="e3285-118">Request headers</span></span>

| <span data-ttu-id="e3285-119">Header</span><span class="sxs-lookup"><span data-stu-id="e3285-119">Header</span></span>         | <span data-ttu-id="e3285-120">Value</span><span class="sxs-lookup"><span data-stu-id="e3285-120">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="e3285-121">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="e3285-121">Authorization</span></span>  | <span data-ttu-id="e3285-122">Bærer {token} (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="e3285-122">Bearer {token} (required)</span></span> |
| <span data-ttu-id="e3285-123">Indholdstype</span><span class="sxs-lookup"><span data-stu-id="e3285-123">Content-Type</span></span>   | <span data-ttu-id="e3285-124">program/json</span><span class="sxs-lookup"><span data-stu-id="e3285-124">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="e3285-125">Anmodningstekst</span><span class="sxs-lookup"><span data-stu-id="e3285-125">Request body</span></span>

<span data-ttu-id="e3285-126">Du skal ikke angive en anmodningstekst for denne metode.</span><span class="sxs-lookup"><span data-stu-id="e3285-126">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="e3285-127">Svar</span><span class="sxs-lookup"><span data-stu-id="e3285-127">Response</span></span>

<span data-ttu-id="e3285-128">Et vellykket svar er altid svaret **204 intet indhold**.</span><span class="sxs-lookup"><span data-stu-id="e3285-128">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="e3285-129">Uautoriserede opkaldere modtager svaret **401 ikke-godkendt** eller **403 forbudt**.</span><span class="sxs-lookup"><span data-stu-id="e3285-129">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="e3285-130">Hvis afsendelse ikke lykkes (f.eks. pga. validering), vil svaret være **500 serverfejl**, og svarets brødtekst indeholder et JSON-objekt med yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e3285-130">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="e3285-131">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e3285-131">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="e3285-132">Validering og fejlmeddelelser</span><span class="sxs-lookup"><span data-stu-id="e3285-132">Validation and error messages</span></span>

<span data-ttu-id="e3285-133">Som led i kaldet til submit-API'en udfører Personale validering af forretningslogik før afsendelse, hvilket sikrer, at orlovsanmodningen er i en gyldig tilstand for afsendelse.</span><span class="sxs-lookup"><span data-stu-id="e3285-133">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="e3285-134">De mulige fejlmeddelelser, du kan modtage i svaret, hvis valideringer ikke lykkes, er:</span><span class="sxs-lookup"><span data-stu-id="e3285-134">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="e3285-135">Anmodningen ville bringe saldoen '{LeaveTypeId}' ned under den tilladte minimumsaldo på {date}.</span><span class="sxs-lookup"><span data-stu-id="e3285-135">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="e3285-136">Anmodning om fridage i afsluttet tilstand kan ikke sendes.</span><span class="sxs-lookup"><span data-stu-id="e3285-136">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="e3285-137">Anmodningen kan ikke sendes eller gemmes, da der ikke er foretaget ændringer.</span><span class="sxs-lookup"><span data-stu-id="e3285-137">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="e3285-138">Tilføj eller opdater beløbet eller orlovstypen, og prøv igen.</span><span class="sxs-lookup"><span data-stu-id="e3285-138">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="e3285-139">Den angivne anmodning om fridage indeholder en eller flere dage med samme dato og orlovstype som en eksisterende ventende anmodning.</span><span class="sxs-lookup"><span data-stu-id="e3285-139">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="e3285-140">Tilbagekald den eksisterende anmodning for at foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="e3285-140">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="e3285-141">Årsagskoden '{ReasonCodeId}' kan ikke anvendes til nogen af orlovstyperne i anmodningen.</span><span class="sxs-lookup"><span data-stu-id="e3285-141">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="e3285-142">Orlovstypen '{LeaveTypeId}' kræver en årsagskode.</span><span class="sxs-lookup"><span data-stu-id="e3285-142">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="e3285-143">Vælg den relevante type og årsagskode.</span><span class="sxs-lookup"><span data-stu-id="e3285-143">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="e3285-144">Fritidsanmodningen blev ikke sendt.</span><span class="sxs-lookup"><span data-stu-id="e3285-144">The time off was not submitted successfully.</span></span> <span data-ttu-id="e3285-145">Anmodningen om fridage er gemt som en kladdeanmodning.</span><span class="sxs-lookup"><span data-stu-id="e3285-145">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3285-146">Se også</span><span class="sxs-lookup"><span data-stu-id="e3285-146">See also</span></span>

- [<span data-ttu-id="e3285-147">Oversigt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="e3285-147">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="e3285-148">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="e3285-148">Authentication</span></span>](hr-developer-api-authentication.md)