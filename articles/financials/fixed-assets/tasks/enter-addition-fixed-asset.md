---
title: Angive en tilføjelse til et anlægsaktiv
description: Denne procedure viser, hvordan du føjer en tilføjelse til et eksisterende anlægsaktiv.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c9733f07f995dd37669f3c33fd0f082daa34dd2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566932"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a>Angive en tilføjelse til et anlægsaktiv

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du føjer en tilføjelse til et eksisterende anlægsaktiv. Formålet med tilføjelser til anlægsaktiv er at spore varetilføjelser, vedligeholdelse eller forbedringer for et aktiv og er kun til orientering. Eventuelle ændringer af anlægsaktivværdien eller levetiden skal foretages separat.   



Proceduren bruger rollen Revisor og demodata for den juridiske enhed USMF.

1. Gå til Anlægsaktiver > Anlægsaktiver > Anlægsaktiver.
2. På listen skal du finde og vælge anlægsaktivet for tilføjelsen.
3. Klik op linket i den valgte række på listen.
4. Klik på Anlægsaktiv i handlingsruden.
5. Klik på Tilføjelser til anlægsaktiv.
6. Klik på Ny.
7. Skriv en værdi i feltet Navn.
8. Angiv datoen for køb af tilføjelse eller service.
9. Angiv omkostningen for vare, vedligeholdelse eller anden forbedring for aktivet.
10. Angiv et tal i feltet Antal.
    * De samlede omkostninger har ingen indflydelse på værdien af anlægsaktivet og bruges udelukkende til sporing og orientering. Hvis omkostningerne skal kapitaliseres, skal en opskrivningsregulering bogføres separat.  
11. Klik på fanen Generelt.
    * Indstil Øger levetiden, hvis tilføjelsen øger aktivets levetid.  
    * Feltet er kun til orientering. Hvis du vil forøge levetiden, skal du ændre levetiden i værdimodellerne og/eller afskrivningsmodellerne for aktivet.  

