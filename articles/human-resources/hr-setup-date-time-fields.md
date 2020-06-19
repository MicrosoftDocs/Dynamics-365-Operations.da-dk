---
title: Forstå dato- og klokkeslætsfelter
description: Forstå, hvad du kan forvente, når du bruger dato- og klokkeslætsfelter i Microsoft Dynamics 365 Human Resources. Bliv klar over, hvad du kan forvente, når der interageres med dato- og klokkeslætsdata i en form i Human Resources, en ekstern kilde eller Common Data Service.
author: Darinkramer
manager: AnnBe
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
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: be1e28d0b842184ce3c4f7bd9748f5e76ac67489
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430089"
---
# <a name="understand-date-and-time-fields"></a>Forstå dato- og klokkeslætsfelter

**Dato- og klokkeslætsfelter** er et grundkoncept i Dynamics 365 Human Resources. Det er vigtigt at forstå, hvordan du kan arbejde med **Dato- og klokkeslætsdata** i Dynamics 365 Human Resources-formularer, Common Data Service og eksterne kilder.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Forstå forskellen mellem feltdatatyper for dato og dato og klokkeslæt

**Dato og klokkeslæt**-felter indeholder oplysninger om tidszoner, mens **Dato**-felter ikke gør det. **Dato**-felter viser de samme oplysninger et hvilket som helst sted. Når du angiver en dato i et **Dato**-felt, skriver Human Resources den samme dato i databasen.

Når Human Resources viser data i et **Dato og klokkeslæt**-felt, justeres dato og klokkeslæt ud fra den tidszone, der er angivet i formen **Brugerindstillinger** (**Generelt > Opsætning > Brugerindstillinger**). De dato- og klokkeslætsoplysninger, du angiver i feltet, er muligvis ikke de samme som de oplysninger, der skrives til databasen.

[![Formen Brugerindstillinger](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Forstå Dato og klokkeslæt-felter i forme 

Når der indtastes data i et **Dato og klokkeslæt**-felt, er de data, der vises på skærmen, ikke de samme som de data, der gemmes i databasen, hvis brugerens tidszone ikke er indstillet til UTC-tid (Coordinated Universal Time). Data i **Dato og klokkeslæt**-felter gemmes altid som UTC.

[![Arbejderform](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Forstå Dato og klokkeslæt-felter i databasen 

Når Human Resources skriver en **Dato og klokkeslæt**-værdi i databasen, gemmes dataene i UTC-tid. Det giver brugerne mulighed for at se alle **Dato og klokkeslæt**-data i forhold til den tidszone, der er defineret i deres brugerindstillinger.
 
I det foregående eksempel er starttidspunktet et tidspunkt, ikke en bestemt dato. Ved at ændre tidszonen for den bruger, der er logget på, fra GMT + 12:00 til GMT UTC, viser den samme post, der netop er oprettet, 30-4-2019 12:00:00 i stedet for 1-5-2019 12:00:00.
  
I nedenstående eksempel bliver medarbejder 000724 aktiv på samme tidspunkt uanset tidszone. Medarbejderen vil blive aktiv 30-4-2019 i GMT-tidszonen, hvilket er det samme som 1-5-2019 i GMT + 12:00 tidszonen. De refererer begge til samme tidspunkt og ikke en bestemt dato. 

[![Arbejderform](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a>Dato og klokkeslæt-data i Data Management Framework, Excel, Common Data Service og Power BI 

Data Management Framework, Excel-tilføjelsesprogrammet, Common Data Service og Power BI-rapportering er alle designet til at interagere med data direkte på databaseniveau. Da der ikke er nogen klient, der kan justere **Dato og klokkeslæt**-data til brugerens tidszone, er alle **Dato og klokkeslæt**-værdier i UTC-tid, hvilket kan medføre ukorrekte antagelser ved indtastning eller visning af data.  
 
**Dato og klokkeslæt**-data, der sendes via DMF, Excel eller Common Data Service, antages af databasen at være i UTC-format. Dette kan forårsage forvirring, når sendte værdi for **Dato og klokkeslæt** ikke vises som forventet, fordi den bruger, der ser dataene, ikke har brugerens tidszone angivet til UTC. 
 
Det samme kan ske ved tilbageførsel, når dataene eksporteres. **Dato og klokkeslæt**-dataene i den eksporterede DMF-enhed kan være forskellige fra, hvad der vises i Dynamics-klienten. 
 
Når der bruges eksterne kilder, f.eks. DMF, til at vise eller oprette data, er det vigtigt at huske på, at **Dato og klokkeslæt**-værdierne anses som standard for at være i UTC, uanset tidszonen på brugerens computer eller brugerens aktuelle tidszoneindstillinger. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Eksempler på den samme post, der vises i forskellige produktområder 

**Human Resources med brugerens tidszone indstillet til UTC**

[![Arbejderform](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources med brugerens tidszone indstillet til GMT +12:00** 

[![Arbejderform](./media/worker-form4.png)](./media/worker-form4.png)

**Excel via OData**

[![Excel via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**Midlertidig DMF**

[![Midlertidig DMF](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF-eksport**

[![Midlertidig DMF](./media/DMFexport.png)](./media/DMFexport.png)

**Excel via Common Data Service**

[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Se også

[Dato- og klokkeslætsdata](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Brugerindstillede tidszoner](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
