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
ms.openlocfilehash: 9b3151cb042012a167854a1e69b55b36981dab19
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054566"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="01ebf-103">Sende en orlovsanmodning til arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="01ebf-103">Submit a leave request to workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="01ebf-104">I Microsoft Dynamics 365 Human Resources kan du bruge MyLeaveRequests submit()-API'en (Application Programming Interface) til at sende en orlovsanmodning til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="01ebf-104">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="01ebf-105">Denne API vises som en handling i MyLeaveRequests OData-enheden.</span><span class="sxs-lookup"><span data-stu-id="01ebf-105">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="01ebf-106">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="01ebf-106">Prerequisites</span></span>

<span data-ttu-id="01ebf-107">Orlovsanmodningen skal gemmes i databasen og skal kunne hentes via MyLeaveRequests-enheden.</span><span class="sxs-lookup"><span data-stu-id="01ebf-107">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="01ebf-108">Tilladelser</span><span class="sxs-lookup"><span data-stu-id="01ebf-108">Permissions</span></span>

<span data-ttu-id="01ebf-109">En af følgende tilladelser kræves for at kalde denne API.</span><span class="sxs-lookup"><span data-stu-id="01ebf-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="01ebf-110">Du kan finde flere oplysninger om tilladelser, og hvordan du vælger dem, i [Godkendelse](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="01ebf-110">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="01ebf-111">Tilladelsestype</span><span class="sxs-lookup"><span data-stu-id="01ebf-111">Permission type</span></span>                    | <span data-ttu-id="01ebf-112">Tilladelser (fra færrest til flest rettigheder)</span><span class="sxs-lookup"><span data-stu-id="01ebf-112">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="01ebf-113">Delegeret (arbejds- eller skolekonto)</span><span class="sxs-lookup"><span data-stu-id="01ebf-113">Delegated (work or school account)</span></span> | <span data-ttu-id="01ebf-114">bruger-\_repræsentation</span><span class="sxs-lookup"><span data-stu-id="01ebf-114">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="01ebf-115">HTTPS-anmodning</span><span class="sxs-lookup"><span data-stu-id="01ebf-115">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="01ebf-116">Anmodningen er i overensstemmelse med OData-standarder.</span><span class="sxs-lookup"><span data-stu-id="01ebf-116">The request conforms to OData standards.</span></span> <span data-ttu-id="01ebf-117">Parametrene {requestId}, {leaveType}, {leaveDate} og {dataArea} refererer til de felter, der udgør den sammensatte naturlige nøgle for MyLeaveRequests-enheden.</span><span class="sxs-lookup"><span data-stu-id="01ebf-117">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="01ebf-118">Mens felterne for MyLeaveRequests-enheden refererer til en enkelt linje i orlovsanmodningen, vil kald af submit-API'en sende hele orlovsanmodningen (alle linjer) til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="01ebf-118">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="01ebf-119">Overskrifter til anmodning</span><span class="sxs-lookup"><span data-stu-id="01ebf-119">Request headers</span></span>

| <span data-ttu-id="01ebf-120">Header</span><span class="sxs-lookup"><span data-stu-id="01ebf-120">Header</span></span>         | <span data-ttu-id="01ebf-121">Value</span><span class="sxs-lookup"><span data-stu-id="01ebf-121">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="01ebf-122">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="01ebf-122">Authorization</span></span>  | <span data-ttu-id="01ebf-123">Bærer {token} (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="01ebf-123">Bearer {token} (required)</span></span> |
| <span data-ttu-id="01ebf-124">Indholdstype</span><span class="sxs-lookup"><span data-stu-id="01ebf-124">Content-Type</span></span>   | <span data-ttu-id="01ebf-125">program/json</span><span class="sxs-lookup"><span data-stu-id="01ebf-125">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="01ebf-126">Anmodningstekst</span><span class="sxs-lookup"><span data-stu-id="01ebf-126">Request body</span></span>

<span data-ttu-id="01ebf-127">Du skal ikke angive en anmodningstekst for denne metode.</span><span class="sxs-lookup"><span data-stu-id="01ebf-127">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="01ebf-128">Svar</span><span class="sxs-lookup"><span data-stu-id="01ebf-128">Response</span></span>

<span data-ttu-id="01ebf-129">Et vellykket svar er altid svaret **204 intet indhold**.</span><span class="sxs-lookup"><span data-stu-id="01ebf-129">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="01ebf-130">Uautoriserede opkaldere modtager svaret **401 ikke-godkendt** eller **403 forbudt**.</span><span class="sxs-lookup"><span data-stu-id="01ebf-130">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="01ebf-131">Hvis afsendelse ikke lykkes (f.eks. pga. validering), vil svaret være **500 serverfejl**, og svarets brødtekst indeholder et JSON-objekt med yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="01ebf-131">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="01ebf-132">Eksempel</span><span class="sxs-lookup"><span data-stu-id="01ebf-132">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="01ebf-133">Validering og fejlmeddelelser</span><span class="sxs-lookup"><span data-stu-id="01ebf-133">Validation and error messages</span></span>

<span data-ttu-id="01ebf-134">Som led i kaldet til submit-API'en udfører Human Resources validering af forretningslogik før afsendelse, hvilket sikrer, at orlovsanmodningen er i en gyldig tilstand for afsendelse.</span><span class="sxs-lookup"><span data-stu-id="01ebf-134">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="01ebf-135">De mulige fejlmeddelelser, du kan modtage i svaret, hvis valideringer ikke lykkes, er:</span><span class="sxs-lookup"><span data-stu-id="01ebf-135">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="01ebf-136">Anmodningen ville bringe saldoen '{LeaveTypeId}' ned under den tilladte minimumsaldo på {date}.</span><span class="sxs-lookup"><span data-stu-id="01ebf-136">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="01ebf-137">Anmodning om fridage i afsluttet tilstand kan ikke sendes.</span><span class="sxs-lookup"><span data-stu-id="01ebf-137">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="01ebf-138">Anmodningen kan ikke sendes eller gemmes, da der ikke er foretaget ændringer.</span><span class="sxs-lookup"><span data-stu-id="01ebf-138">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="01ebf-139">Tilføj eller opdater beløbet eller orlovstypen, og prøv igen.</span><span class="sxs-lookup"><span data-stu-id="01ebf-139">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="01ebf-140">Den angivne anmodning om fridage indeholder en eller flere dage med samme dato og orlovstype som en eksisterende ventende anmodning.</span><span class="sxs-lookup"><span data-stu-id="01ebf-140">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="01ebf-141">Tilbagekald den eksisterende anmodning for at foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="01ebf-141">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="01ebf-142">Årsagskoden '{ReasonCodeId}' kan ikke anvendes til nogen af orlovstyperne i anmodningen.</span><span class="sxs-lookup"><span data-stu-id="01ebf-142">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="01ebf-143">Orlovstypen '{LeaveTypeId}' kræver en årsagskode.</span><span class="sxs-lookup"><span data-stu-id="01ebf-143">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="01ebf-144">Vælg den relevante type og årsagskode.</span><span class="sxs-lookup"><span data-stu-id="01ebf-144">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="01ebf-145">Fritidsanmodningen blev ikke sendt.</span><span class="sxs-lookup"><span data-stu-id="01ebf-145">The time off was not submitted successfully.</span></span> <span data-ttu-id="01ebf-146">Anmodningen om fridage er gemt som en kladdeanmodning.</span><span class="sxs-lookup"><span data-stu-id="01ebf-146">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="01ebf-147">Se også</span><span class="sxs-lookup"><span data-stu-id="01ebf-147">See also</span></span>

- [<span data-ttu-id="01ebf-148">Oversigt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="01ebf-148">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="01ebf-149">Godkendelse</span><span class="sxs-lookup"><span data-stu-id="01ebf-149">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]