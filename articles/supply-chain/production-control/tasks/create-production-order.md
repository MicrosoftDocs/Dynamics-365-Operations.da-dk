--- 
title: Oprette en produktionsordre
description: Denne procedure viser, hvordan du opretter en produktionsordre.
author: johanhoffmann
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 4db56f76c7f8ce0cccf85ab04024d9a1e88a8822
ms.contentlocale: da-dk
ms.lasthandoff: 02/06/2018

---
# <a name="create-a-production-order"></a>Oprette en produktionsordre

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en produktionsordre. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Dette er den første procedure ud af syv, der beskriver produktionsordrens livscyklus.


## <a name="create-a-production-order"></a>Oprette en produktionsordre
1. Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.
2. Klik på Ny produktionsordre.
3. Skriv 'D0001' i feltet Varenummer.
4. Angiv en dato i feltet Levering.
    * Leveringsdatoen angiver, hvornår produktionsordren skal slutte med henblik på at levere til tiden. Denne dato kan bruges i planlægningsprocessen. Du kan f.eks. planlægge ordren bagud i forhold til leveringsdatoen.  
5. Angiv antallet til '20'.
    * Bemærk! Feltet Styklistenummer viser automatisk antallet i en aktiv stykliste for den aktuelle vare, men du kan ændre styklisten for produktionsordren ved at vælge en aktiv stykliste på listen over godkendte styklisteversioner.    Feltet Rutenummer viser automatisk antallet i en aktiv rute for den aktuelle vare, men du kan ændre ruten for produktionsordren ved at vælge en aktiv rute på listen over godkendte ruteversioner.  
6. Klik på Opret.

## <a name="validate-the-production-order"></a>Valider produktionsordren
1. Klik op linket i den valgte række på listen.
    * Klik på linket til det produktionsordrenummer, du lige har oprettet. Derved åbnes detaljesiden for ordren.  
2. Klik på Rediger.
3. Angiv en dato i feltet Levering.
    * Du kan f.eks. ændre leveringsdatoen for produktionsordren.  
4. Klik på Gem.
5. Luk siden.

## <a name="update-the-bom"></a>Opdater styklisten
1. Klik på Produktionsordre i handlingsruden.
2. Klik på Stykliste.
    * Åbn styklistesiden for at validere de styklistedata, der er kopieret fra standarddataene, da produktionsordren blev oprettet. I denne procedure skal du opdatere antallet for en stykliste.  
3. Klik på Rediger.
4. Angiv et tal i feltet Antal.
    * Ændring af antallet på styklistelinjen påvirker forkalkulationen af materialeforbruget for produktionsordren.  
5. Klik på Gem.
6. Luk siden.

## <a name="update-the-production-route"></a>Opdater produktionsruten
1. Klik på Produktionsordre i handlingsruden.
2. Klik på Rute.
    * Åbn rutesiden for at validere dataene i den produktionsrute, der er kopieret fra standarddataene, da ordren blev oprettet. I denne procedure skal du opdatere antallet for en af operationerne i produktionsruten.  
3. Find og vælg den ønskede post på listen.
4. Klik på Rediger.
5. I feltet Procesantal skal du angive et tal.
    * Ændring af procestiden påvirker det beregnede ruteforbrug og omkostninger for produktionsordren.  
6. Klik på Gem.
7. Luk siden.


