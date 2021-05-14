---
title: Oprette skabeloner til arbejdstid
description: Arbejdstidsskabeloner definerer arbejdstiderne i hele ugen og bruges til at generere arbejdstider for et bestemt tidsrum.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920922"
---
# <a name="create-working-time-templates"></a>Oprette skabeloner til arbejdstid

[!include [banner](../../includes/banner.md)]

Arbejdstidsskabeloner definerer arbejdstiderne i hele ugen og bruges til at generere arbejdstider for et bestemt tidsrum. Denne procedure viser, hvordan du definerer en arbejdstidsskabelon ved hjælp af planlægningsegenskaber for arbejdstider til kategorisering af arbejdstidsintervaller. Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.

1. Gå til **Arbejdsområder > Styring af ressourcelivscyklus**.
1. Vælg **Arbejdstidsskabeloner**.

## <a name="create-working-time-template"></a>Oprette arbejdstidsskabelon

1. Vælg **Ny**.
1. Indtast en værdi i feltet **Arbejdstidsskabelon**.
1. Skriv en værdi i feltet **Navn**.
1. Udvid sektionen **Mandag**.
1. Vælg **Tilføj**.
1. Angiv et klokkeslæt i feltet **Fra**.
    * Angiv det tidspunkt, hvor arbejdet begynder om morgenen.  
1. Angiv et klokkeslæt i feltet **Til**.
    * Angiv det tidspunkt, hvor arbejdere har frokostpause.  
1. Vælg **Tilføj**.
1. Angiv et klokkeslæt i feltet **Fra**.
    * Angiv det tidspunkt, hvor arbejdet genoptages efter frokost.  
1. Angiv et klokkeslæt i feltet **Til**.
    * Angiv, hvornår arbejdsdagen er slut.  

## <a name="replicate-working-times-to-all-week-days"></a>Replikere arbejdstider til alle ugedage

1. Vælg **Kopiér dag**.
    * Kopier arbejdstidsdefinitionerne fra mandag til tirsdag.  
1. Vælg **OK**.
1. Vælg **Kopiér dag**.
    * Kopier arbejdstidsdefinitionerne fra mandag til onsdag.  
1. Vælg en indstilling i feltet **Til ugedag**.
1. Vælg **OK**.
1. Vælg **Kopiér dag**.
    * Kopier arbejdstidsdefinitionerne fra mandag til torsdag.  
1. Vælg en indstilling i feltet **Til ugedag**.
1. Vælg **OK**.
1. Vælg **Kopiér dag**.
    * Kopier arbejdstidsdefinitionerne fra mandag til fredag.  
1. Vælg en indstilling i feltet **Til ugedag**.
1. Vælg **OK**.

## <a name="define-time-slots-for-special-operations"></a>Definere tidsrubrikker for særlige operationer

1. Udvid sektionen **Fredag**.
1. Find og vælg den ønskede post på listen.
1. Indtast eller vælg en værdi i feltet **Egenskab**.
1. Find og vælg den ønskede post på listen.
1. Indtast eller vælg en værdi i feltet **Egenskab**.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Markér dage i weekend som lukket for afhentning

1. Udvid sektionen **Lørdag**.
1. Vælg *Ja* i feltet **Lukket for afhentning**.
1. Udvid sektionen **Søndag**.
1. Vælg *Ja* i feltet **Lukket for afhentning**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]