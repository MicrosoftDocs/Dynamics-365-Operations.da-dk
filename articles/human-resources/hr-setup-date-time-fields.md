---
title: Forstå dato- og klokkeslætsfelter
description: Forstå, hvad du kan forvente, når du bruger dato- og klokkeslætsfelter i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 924d7369129d4115d45f23864e7b851d318c52a4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467355"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="c7abe-103">Forstå dato- og tidsfelter</span><span class="sxs-lookup"><span data-stu-id="c7abe-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c7abe-104">**Dato- og klokkeslætsfelter** er et grundkoncept i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c7abe-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c7abe-105">Det er vigtigt at forstå, hvordan du kan arbejde med **Dato- og klokkeslætsdata** i -formularer, Dataverse og eksterne kilder.</span><span class="sxs-lookup"><span data-stu-id="c7abe-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="c7abe-106">Forstå forskellen mellem feltdatatyper for dato og dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="c7abe-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="c7abe-107">**Dato og klokkeslæt**-felter indeholder oplysninger om tidszoner, mens **Dato**-felter ikke gør det.</span><span class="sxs-lookup"><span data-stu-id="c7abe-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="c7abe-108">**Dato**-felter viser de samme oplysninger et hvilket som helst sted.</span><span class="sxs-lookup"><span data-stu-id="c7abe-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="c7abe-109">Når du angiver en dato i et **Dato**-felt, skriver Human Resources den samme dato i databasen.</span><span class="sxs-lookup"><span data-stu-id="c7abe-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="c7abe-110">Når Human Resources viser data i et **Dato og klokkeslæt**-felt, justeres dato og klokkeslæt ud fra den tidszone, der er angivet i formen **Brugerindstillinger** (**Generelt > Opsætning > Brugerindstillinger**).</span><span class="sxs-lookup"><span data-stu-id="c7abe-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="c7abe-111">De dato- og klokkeslætsoplysninger, du angiver i feltet, er muligvis ikke de samme som de oplysninger, der skrives til databasen.</span><span class="sxs-lookup"><span data-stu-id="c7abe-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="c7abe-112">[![Formen Brugerindstillinger](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="c7abe-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="c7abe-113">Forstå Dato og klokkeslæt-felter i forme</span><span class="sxs-lookup"><span data-stu-id="c7abe-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="c7abe-114">Når der indtastes data i et **Dato og klokkeslæt**-felt, er de data, der vises på skærmen, ikke de samme som de data, der gemmes i databasen, hvis brugerens tidszone ikke er indstillet til UTC-tid (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="c7abe-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="c7abe-115">Data i **Dato og klokkeslæt**-felter gemmes altid som UTC.</span><span class="sxs-lookup"><span data-stu-id="c7abe-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="c7abe-116">[![Arbejderformular UTC](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="c7abe-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="c7abe-117">Forstå Dato og klokkeslæt-felter i databasen</span><span class="sxs-lookup"><span data-stu-id="c7abe-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="c7abe-118">Når Human Resources skriver en **Dato og klokkeslæt**-værdi i databasen, gemmes dataene i UTC-tid.</span><span class="sxs-lookup"><span data-stu-id="c7abe-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="c7abe-119">Det giver brugerne mulighed for at se alle **Dato og klokkeslæt**-data i forhold til den tidszone, der er defineret i deres brugerindstillinger.</span><span class="sxs-lookup"><span data-stu-id="c7abe-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="c7abe-120">I det foregående eksempel er starttidspunktet et tidspunkt, ikke en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="c7abe-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="c7abe-121">Ved at ændre tidszonen for den bruger, der er logget på, fra GMT + 12:00 til GMT UTC, viser den samme post, der netop er oprettet, 30-4-2019 12:00:00 i stedet for 1-5-2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="c7abe-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="c7abe-122">I nedenstående eksempel bliver medarbejder 000724 aktiv på samme tidspunkt uanset tidszone.</span><span class="sxs-lookup"><span data-stu-id="c7abe-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="c7abe-123">Medarbejderen vil blive aktiv 30-4-2019 i GMT-tidszonen, hvilket er det samme som 1-5-2019 i GMT + 12:00 tidszonen.</span><span class="sxs-lookup"><span data-stu-id="c7abe-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="c7abe-124">De refererer begge til samme tidspunkt og ikke en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="c7abe-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="c7abe-125">[![Arbejderformular GMT](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="c7abe-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="c7abe-126">Dato og klokkeslæt-data i Data Management Framework, Excel, Dataverse og Power BI</span><span class="sxs-lookup"><span data-stu-id="c7abe-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="c7abe-127">Data Management Framework, Excel-tilføjelsesprogrammet, Dataverse og Power BI-rapportering er alle designet til at interagere med data direkte på databaseniveau.</span><span class="sxs-lookup"><span data-stu-id="c7abe-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="c7abe-128">Da der ikke er nogen klient, der kan justere **Dato og klokkeslæt**-data til brugerens tidszone, er alle **Dato og klokkeslæt**-værdier i UTC-tid, hvilket kan medføre ukorrekte antagelser ved indtastning eller visning af data.</span><span class="sxs-lookup"><span data-stu-id="c7abe-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="c7abe-129">**Dato og klokkeslæt**-data, der sendes via DMF, Excel eller Dataverse, antages af databasen at være i UTC-format.</span><span class="sxs-lookup"><span data-stu-id="c7abe-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="c7abe-130">Dette kan forårsage forvirring, når sendte værdi for **Dato og klokkeslæt** ikke vises som forventet, fordi den bruger, der ser dataene, ikke har brugerens tidszone angivet til UTC.</span><span class="sxs-lookup"><span data-stu-id="c7abe-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="c7abe-131">Det samme kan ske ved tilbageførsel, når dataene eksporteres.</span><span class="sxs-lookup"><span data-stu-id="c7abe-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="c7abe-132">**Dato og klokkeslæt**-dataene i den eksporterede DMF-enhed kan være forskellige fra, hvad der vises i Dynamics-klienten.</span><span class="sxs-lookup"><span data-stu-id="c7abe-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="c7abe-133">Når der bruges eksterne kilder, f.eks. DMF, til at vise eller oprette data, er det vigtigt at huske på, at **Dato og klokkeslæt**-værdierne anses som standard for at være i UTC, uanset tidszonen på brugerens computer eller brugerens aktuelle tidszoneindstillinger.</span><span class="sxs-lookup"><span data-stu-id="c7abe-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="c7abe-134">Eksempler på den samme post, der vises i forskellige produktområder</span><span class="sxs-lookup"><span data-stu-id="c7abe-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="c7abe-135">**Human Resources med brugerens tidszone indstillet til UTC**</span><span class="sxs-lookup"><span data-stu-id="c7abe-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="c7abe-136">[![Arbejderformular angivet til UTC](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="c7abe-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="c7abe-137">**Human Resources med brugerens tidszone indstillet til GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="c7abe-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="c7abe-138">[![Arbejderformular angivet til GMT](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="c7abe-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="c7abe-139">**Excel via OData**</span><span class="sxs-lookup"><span data-stu-id="c7abe-139">**Excel Via OData**</span></span>

<span data-ttu-id="c7abe-140">[![Excel via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="c7abe-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="c7abe-141">**Midlertidig DMF**</span><span class="sxs-lookup"><span data-stu-id="c7abe-141">**DMF Staging**</span></span>

<span data-ttu-id="c7abe-142">[![Midlertidig DMF](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="c7abe-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="c7abe-143">**DMF-eksport**</span><span class="sxs-lookup"><span data-stu-id="c7abe-143">**DMF Export**</span></span>

<span data-ttu-id="c7abe-144">[![DMF Eksport](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="c7abe-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="c7abe-145">**Excel via Dataverse**</span><span class="sxs-lookup"><span data-stu-id="c7abe-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="c7abe-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="c7abe-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="c7abe-147">Se også</span><span class="sxs-lookup"><span data-stu-id="c7abe-147">See also</span></span>

[<span data-ttu-id="c7abe-148">Dato- og klokkeslætsdata</span><span class="sxs-lookup"><span data-stu-id="c7abe-148">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="c7abe-149">Brugerindstillede tidszoner</span><span class="sxs-lookup"><span data-stu-id="c7abe-149">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]