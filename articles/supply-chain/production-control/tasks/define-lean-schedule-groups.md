--- 
title: "Definere lean planlægningsgrupper"
description: "Lean planlægningsgrupper defineres for at gruppere og adskille produkter i kanban-planlægning."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3e07fa270b47be3527c572dc53ca30a7bcde5ba6
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---
# <a name="define-lean-schedule-groups"></a>Definere lean planlægningsgrupper

[!include [task guide banner](../../includes/task-guide-banner.md)]

Lean planlægningsgrupper defineres for at gruppere og adskille produkter i kanban-planlægning. Grupperingen kan foretages som standardtilknytning pr. firma eller som specifik for en arbejdscelle. Hver gruppe har en tildelt farvekode for visuel angivelse i kanban-planlægningens listeside. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="define-lean-scheduling-group"></a>Definere lean planlægningsgruppe
1. Gå til Administration af produktoplysninger > Lean produktion > Lean planlægningsgrupper.
2. Klik på Ny.
3. Indtast en værdi i feltet Planlægningsgruppe.
    * En planlægningsgruppe kan defineres som en global gruppe eller specifik for en arbejdscelle. I dette enkle eksempel definerer vi en global gruppe og lader arbejdscellen være tom. Indstillingerne for denne gruppe gælder for arbejdsceller, der ikke har bestemte planlægningsgrupper.  
4. Vælg en farve i farvevalget.
    * Farverne bruges til at fremhæve job på listesiden for kanban-tidsplanen eller kanban-procesområdet.  
5. Markér den valgte række på listen.
6. Klik op linket i den valgte række på listen.

## <a name="associate-product"></a>Tilknytte produkt
1. Tilknytte et bestemt produkt
    * Der er to måder at knytte produkter til lean planlægningsgrupper: enten som et bestemt produkt (varerelationstype = vare) eller som en del af en varefordelingsnøgle (varerelationstype = gruppe).    
2. Vælg Vare i feltet Varerelationstype
3. Indtast en værdi i feltet Varenummer.
4. Angiv et tal i feltet Gennemløbsforhold.
    * Standardgennemløbsforholdet er 1, hvilket betyder, at de relaterede produkter forbruger nøjagtigt den kapacitet, der er angivet i procesaktiviteterne for produktionsflowene. Gennemløbsforhold > 1 definerer et højere ressourceforbrug, Gennemløbsforhold < 1 definerer et lavere ressourceforbrug. Forholdet bruges i omkostningsberegningen og i beregningen af kanban-jobforbruget.  

## <a name="associate-item-allocation-key"></a>Tilknytte varefordelingsnøgle
1. Tilknytte en varefordelingsnøgle
    * Føj en tilknytning til en varefordelingsnøgle ved hjælp af varerelationstypen Gruppe.   Bemærk, at denne proces skal du en budgetvarefordelingsnøgle, der er defineret i dataene.  
2. Vælg Gruppe i feltet Varerelationstype
3. Klik på rullelisten i feltet Varefordelingsnøgle for at åbne opslaget.
4. Klik op linket i den valgte række på listen.


