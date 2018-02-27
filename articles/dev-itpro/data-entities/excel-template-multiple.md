---
title: Importere data fra Excel-dataenhedsskabeloner med flere regneark
description: "I dette emne beskrives, hvordan du kan importere data ved hjælp af Excel-dataenhedsskabeloner i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 84b9e9128d7ea6cdf9949549f4ab7a1c6c01691b
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---

# <a name="excel-templates-with-multiple-worksheets"></a>Excel-skabeloner med flere regneark

[!include[banner](../includes/banner.md)]

Administration af data i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition understøtter Microsoft Excel-baserede skabeloner til dataenheder. Disse skabeloner kan indeholde et eller flere regneark. Skabeloner med flere regneark bruges ofte, når det passer til at administrere data i en enkelt fil og importere den til flere dataenheder. Et eksempel er lokationer og lagersteder.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Overføre en fil én gang og knytte den til alle enheder
Lad os tage et eksempel, hvor der er én Excel-fil med regnearkene **Lokationer** og **Lagersteder**. For at konfigurere dataimportprojektet skal du tilføje den første dataenhed **Lokationer** og derefter overføre filen. Du kan vælge **Lokationer** som det regneark, der skal bruges til denne enhed.

Hvis du tilføjer den anden enhed, **Lagersteder**, uden at forlade formularen **Tilføj fil**, gør regnearksopslaget det muligt for dig at vælge regnearket **Lagersteder** uden at skulle overføre filen igen. Den eneste grund til at overføre en ny fil er, hvis **Lagersteder**-dataene er i en anden fil.

![Flere regneark](./media/AddFileMultipleWorkSheets.png) 

## <a name="fix-worksheet-to-entity-mapping"></a>Rette regneark til enhedstilknytning

Tilknytningen af regnearket til en dataenhed i importjobbet kan rettes i gitteret. Kolonnen **Regneark** i gitteret viser de regneark fra den fil, der blev tilknyttet. Du kan vælge et andet regneark i rullemenuen. Hvis det valgte regneark allerede er knyttet til en enhed i dataprojektet, beder systemet dig om at bekræfte ændringen. Det anbefales, at du retter alle tilknytninger i gitteret.

![Opdatere tilknytning af regneark](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Tilknytte igen til en ny fil

I tilfælde, hvor der skal overføres en ny version af den samme fil eller en helt ny fil til eksisterende objekter i et dataprojekt, skal du bruge **Tilføj fil**-oplevelsen og tilføje enhederne igen, som om de blev tilføjet for første gang. Systemet bekræfter, at du vil overskrive de eksisterende enheder i dataprojektet, før du fortsætter. Enheder, der ikke tilføjes igen (eller overskrives) fortsætter med at have de tidligere tilknytninger fra den tidligere fil.

## <a name="upload-a-file-using-run-project"></a>Overføre en fil ved hjælp af Kør projekt

Du kan overføre en Excel-fil, mens du bruger indstillingen **Kør projekt** til at udføre et importprojekt. Du skal være omhyggelig med kun at overføre de filer, der har de samme regneark som de eksisterende tilknytninger på dataenhederne i dataprojektet. Hvis der ikke findes et regneark i den fil, der netop er overført, vises der en fejlmeddelelse i systemet, og importen stopper. Hvis tilknytningen til regnearket skal ændres for et objekt, skal tilknytningerne i dataprojektet først opdateres fra dataprojektet, før du kan bruge filen i **Kør projekt**-oplevelsen.


