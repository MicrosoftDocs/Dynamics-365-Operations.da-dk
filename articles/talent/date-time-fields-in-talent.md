---
title: Arbejde med dato og klokkeslæt i Microsoft Dynamics 365 for Talent
description: Forstå, hvad du kan forvente, når du bruger dato- og klokkeslætsfelter i Microsoft Dynamics 365 for Talent. Bliv klar over, hvad du kan forvente, når der interageres med dato- og klokkeslætsdata i en form i Dynamics 365 for Talent, en ekstern kilde eller Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b4c652992272ed1a5aecbb4c78f0d11f077149d1
ms.sourcegitcommit: 46bded82aa072adfedcf443629c2adc69f512c09
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/26/2019
ms.locfileid: "1791200"
---
# <a name="date-and-time-fields-in-talent"></a><span data-ttu-id="eda7e-104">Dato-og tidsfelter i Talent</span><span class="sxs-lookup"><span data-stu-id="eda7e-104">Date and Time fields in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eda7e-105">**Dato- og klokkeslætsfelter** er et grundkoncept i Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="eda7e-105">**Date and Time** fields are a fundamental concept in Dynamics 365 for Talent.</span></span> <span data-ttu-id="eda7e-106">Det er vigtigt at forstå, hvordan du kan arbejde med **Dato- og klokkeslætsdata** i en Dynamics 365-form, Common Data Service og eksterne kilder.</span><span class="sxs-lookup"><span data-stu-id="eda7e-106">It's important to understand how to work with **Date and Time** data in a Dynamics 365 form, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="eda7e-107">Forstå forskellen mellem feltdatatyper for dato og dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="eda7e-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="eda7e-108">**Dato og klokkeslæt**-felter indeholder oplysninger om tidszoner, mens **Dato**-felter ikke gør det.</span><span class="sxs-lookup"><span data-stu-id="eda7e-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="eda7e-109">**Dato**-felter viser de samme oplysninger et hvilket som helst sted.</span><span class="sxs-lookup"><span data-stu-id="eda7e-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="eda7e-110">Når du angiver en dato i et **Dato**-felt, skriver Talent den samme dato i databasen.</span><span class="sxs-lookup"><span data-stu-id="eda7e-110">When you enter a date into a **Date** field, Talent writes that same date to the database.</span></span>

<span data-ttu-id="eda7e-111">Når Talent viser data i er **Dato og klokkeslæt**-felt, justeres dato og klokkeslæt ud fra den tidszone, der er angivet i formen **Brugerindstillinger** (**Generelt > Opsætning > Brugerindstillinger**).</span><span class="sxs-lookup"><span data-stu-id="eda7e-111">When displaying data in a **Date and Time** field, Talent adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="eda7e-112">De dato- og klokkeslætsoplysninger, du angiver i feltet, er muligvis ikke de samme som de oplysninger, der skrives til databasen.</span><span class="sxs-lookup"><span data-stu-id="eda7e-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="eda7e-113">[![Formen Brugerindstillinger](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="eda7e-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="eda7e-114">Forstå Dato og klokkeslæt-felter i forme</span><span class="sxs-lookup"><span data-stu-id="eda7e-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="eda7e-115">Når der indtastes data i et **Dato og klokkeslæt**-felt, er de data, der vises på skærmen, ikke de samme som de data, der gemmes i databasen, hvis brugerens tidszone ikke er indstillet til UTC-tid (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="eda7e-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="eda7e-116">Data i **Dato og klokkeslæt**-felter gemmes altid som UTC.</span><span class="sxs-lookup"><span data-stu-id="eda7e-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="eda7e-117">[![Arbejderform](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="eda7e-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="eda7e-118">Forstå Dato og klokkeslæt-felter i databasen</span><span class="sxs-lookup"><span data-stu-id="eda7e-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="eda7e-119">Når Talent skriver en **Dato og klokkeslæt**-værdi i databasen, gemmes dataene i UTC-tid.</span><span class="sxs-lookup"><span data-stu-id="eda7e-119">When Talent writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="eda7e-120">Det giver brugerne mulighed for at se alle **Dato og klokkeslæt**-data i forhold til den tidszone, der er defineret i deres brugerindstillinger.</span><span class="sxs-lookup"><span data-stu-id="eda7e-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="eda7e-121">I det foregående eksempel er starttidspunktet et tidspunkt, ikke en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="eda7e-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="eda7e-122">Ved at ændre tidszonen for den bruger, der er logget på, fra GMT + 12:00 til GMT UTC, viser den samme post, der netop er oprettet, 30-4-2019 12:00:00 i stedet for 1-5-2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="eda7e-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="eda7e-123">I nedenstående eksempel bliver medarbejder 000724 aktiv på samme tidspunkt uanset tidszone.</span><span class="sxs-lookup"><span data-stu-id="eda7e-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="eda7e-124">Medarbejderen vil blive aktiv 30-4-2019 i GMT-tidszonen, hvilket er det samme som 1-5-2019 i GMT + 12:00 tidszonen.</span><span class="sxs-lookup"><span data-stu-id="eda7e-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="eda7e-125">De refererer begge til samme tidspunkt og ikke en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="eda7e-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="eda7e-126">[![Arbejderform](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="eda7e-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="eda7e-127">Dato og klokkeslæt-data i Data Management Framework, Excel, Common Data Service og Power BI</span><span class="sxs-lookup"><span data-stu-id="eda7e-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="eda7e-128">Data Management Framework, Excel-tilføjelsesprogrammet, Common Data Service og Power BI-rapportering er alle designet til at interagere med data direkte på databaseniveau.</span><span class="sxs-lookup"><span data-stu-id="eda7e-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="eda7e-129">Da der ikke er nogen klient, der kan justere **Dato og klokkeslæt**-data til brugerens tidszone, er alle **Dato og klokkeslæt**-værdier i UTC-tid, hvilket kan medføre ukorrekte antagelser ved indtastning eller visning af data.</span><span class="sxs-lookup"><span data-stu-id="eda7e-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="eda7e-130">**Dato og klokkeslæt**-data, der sendes via DMF, Excel eller Common Data Service, antages af databasen at være i UTC-format.</span><span class="sxs-lookup"><span data-stu-id="eda7e-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="eda7e-131">Dette kan forårsage forvirring, når sendte værdi for **Dato og klokkeslæt** ikke vises som forventet, fordi den bruger, der ser dataene, ikke har brugerens tidszone angivet til UTC.</span><span class="sxs-lookup"><span data-stu-id="eda7e-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="eda7e-132">Det samme kan ske ved tilbageførsel, når dataene eksporteres.</span><span class="sxs-lookup"><span data-stu-id="eda7e-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="eda7e-133">**Dato og klokkeslæt**-dataene i den eksporterede DMF-enhed kan være forskellige fra, hvad der vises i Dynamics-klienten.</span><span class="sxs-lookup"><span data-stu-id="eda7e-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="eda7e-134">Når der bruges eksterne kilder, f.eks. DMF, til at vise eller oprette data, er det vigtigt at huske på, at **Dato og klokkeslæt**-værdierne anses som standard for at være i UTC, uanset tidszonen på brugerens computer eller brugerens aktuelle tidszoneindstillinger.</span><span class="sxs-lookup"><span data-stu-id="eda7e-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="eda7e-135">Eksempler på den samme post, der vises i forskellige produktområder</span><span class="sxs-lookup"><span data-stu-id="eda7e-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="eda7e-136">**Talent med brugerens tidszone indstillet til UTC**</span><span class="sxs-lookup"><span data-stu-id="eda7e-136">**Talent with user time zone set to UTC**</span></span>

<span data-ttu-id="eda7e-137">[![Arbejderform](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="eda7e-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="eda7e-138">**Talent med brugerens tidszone indstillet til GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="eda7e-138">**Talent with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="eda7e-139">[![Arbejderform](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="eda7e-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="eda7e-140">**Excel via OData**</span><span class="sxs-lookup"><span data-stu-id="eda7e-140">**Excel Via OData**</span></span>

<span data-ttu-id="eda7e-141">[![Excel via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="eda7e-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="eda7e-142">**Midlertidig DMF**</span><span class="sxs-lookup"><span data-stu-id="eda7e-142">**DMF Staging**</span></span>

<span data-ttu-id="eda7e-143">[![Midlertidig DMF](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="eda7e-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="eda7e-144">**DMF-eksport**</span><span class="sxs-lookup"><span data-stu-id="eda7e-144">**DMF Export**</span></span>

<span data-ttu-id="eda7e-145">[![Midlertidig DMF](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="eda7e-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="eda7e-146">**Excel via Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="eda7e-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="eda7e-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="eda7e-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

### <a name="see-also"></a><span data-ttu-id="eda7e-148">Se også</span><span class="sxs-lookup"><span data-stu-id="eda7e-148">See also</span></span>

[<span data-ttu-id="eda7e-149">Dato- og klokkeslætsdata</span><span class="sxs-lookup"><span data-stu-id="eda7e-149">Date and time data</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="eda7e-150">Brugerindstillede tidszoner</span><span class="sxs-lookup"><span data-stu-id="eda7e-150">User preferred time zones</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
