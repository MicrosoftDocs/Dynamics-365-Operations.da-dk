---
title: Forstå dato- og tidsfelter
description: Denne artikel forklarer, hvad du kan forvente, når du bruger dato- og klokkeslætsfelter i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e314efa5ac08288bc7d00c197be59ba9decac203
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856303"
---
# <a name="understand-date-and-time-fields"></a>Forstå dato- og tidsfelter

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



**Dato- og klokkeslætsfelter** er et grundkoncept i Microsoft Dynamics 365 Human Resources. Det er vigtigt at forstå, hvordan du kan arbejde med **Dato- og klokkeslætsdata** på sider i Dataverse og eksterne kilder.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Forstå forskellen mellem feltdatatyper for dato og dato og klokkeslæt

**Dato og klokkeslæt**-felter indeholder oplysninger om tidszoner, mens **Dato**-felter ikke gør det. **Dato**-felter viser de samme oplysninger et hvilket som helst sted. Når du angiver en dato i et **Dato**-felt, skrives den samme dato i databasen.

Når data vises i et **Dato og klokkeslæt**-felt, justeres dato og klokkeslæt ud fra brugerens tidszone, der er angivet på siden **Brugerindstillinger** (**Generelt \> Opsætning \> Brugerindstillinger**). De dato- og klokkeslætsoplysninger, du angiver i feltet, er muligvis ikke de samme som de oplysninger, der skrives til databasen.

[![Siden Brugerindstillinger.](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>Forståelse af Dato og klokkeslæt-felter på sider 

Når der indtastes data i et **Dato og klokkeslæt**-felt, er de data, der vises på skærmen, ikke de samme som de data, der gemmes i databasen, hvis brugerens tidszone ikke er indstillet til UTC-tid (Coordinated Universal Time). Data i **Dato og klokkeslæt**-felter gemmes altid som UTC.

[![Arbejdersides UTC.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Forstå Dato og klokkeslæt-felter i databasen 

Når en **Dato og klokkeslæt**-værdi skrives i databasen, gemmes dataene i UTC-tid. Det giver brugerne mulighed for at se alle **Dato og klokkeslæt**-data i forhold til den tidszone, der er defineret i deres brugerindstillinger.
 
I det foregående eksempel er starttidspunktet et tidspunkt, ikke en bestemt dato. Ved at ændre tidszonen for den bruger, der er logget på, fra GMT + 12:00 til GMT UTC, viser den samme post, der netop er oprettet, 30-4-2019 12:00:00 i stedet for 1-5-2019 12:00:00.

I nedenstående eksempel bliver medarbejder 000724 aktiv på samme tidspunkt uanset tidszone. Medarbejderen vil blive aktiv 30-4-2019 i GMT-tidszonen, hvilket er det samme som 1-5-2019 i GMT + 12:00 tidszonen. De refererer begge til samme tidspunkt og ikke en bestemt dato. 

[![Arbejdersides GMT.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Dato og klokkeslæt-data i Data Management Framework, Excel, Dataverse og Power BI 

Data Management Framework (DMF), Excel-tilføjelsesprogram, Dataverse og Power BI-rapportering er alle designet til at interagere med data direkte på databaseniveau. Da der ikke er nogen klient, der kan justere **Dato og klokkeslæt**-data til brugerens tidszone, er alle **Dato og klokkeslæt**-værdier i UTC-tid, hvilket kan medføre ukorrekte antagelser ved indtastning eller visning af data.
 
Når **Dato og klokkeslæt**-data sendes via DMF, Excel eller Dataverse, antager databasen, at de er i UTC-format. Men hvis brugere, der får vist dataene, ikke har deres brugertidszone angivet til UTC, vises værdien for sendt **Dato og klokkeslæt** ikke som forventet, og brugerne kan blive forvirret. 
 
Det samme kan ske ved tilbageførsel, når dataene eksporteres. **Dato og klokkeslæt**-dataene i den eksporterede DMF-enhed kan være forskellige fra, hvad der vises i Dynamics-klienten. 
 
Når der bruges eksterne kilder, f.eks. DMF, til at vise eller oprette data, er det vigtigt at huske på, at **Dato og klokkeslæt**-værdierne anses som standard for at være i UTC, uanset tidszonen på brugerens computer eller brugerens aktuelle tidszoneindstillinger. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Eksempler på den samme post, der vises i forskellige produktområder 

**Human Resources med brugerens tidszone indstillet til UTC**

[![Arbejdersider angivet til UTC.](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources med brugerens tidszone indstillet til GMT +12:00** 

[![Arbejdersider angivet til GMT.](./media/worker-form4.png)](./media/worker-form4.png)

**Excel via OData**

[![Excel via OData.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**Midlertidig DMF**

[![Midlertidig DMF.](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF-eksport**

[![DMF-eksport.](./media/DMFExport.png)](./media/DMFExport.png)

**Excel via Dataverse**

[![Excel via Dataverse.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Se også

[Dato- og klokkeslætsdata](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Brugerindstillede tidszoner](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
