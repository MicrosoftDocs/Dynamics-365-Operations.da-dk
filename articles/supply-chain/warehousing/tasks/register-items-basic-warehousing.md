---
title: Registrer varer til en grundlæggende lagerstedsaktiveret vare ved hjælp af en varemodtagelseskladde
description: Denne fremgangsmåde viser, hvordan du registrerer varer ved hjælp af varemodtagelseskladden, når du bruger "grundlæggende lagerstedsfunktioner" i Lagerstyringsmodulet.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c53a38eb6afdf8d3cc1a316c8da5e84549ab60d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "361423"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a>Registrer varer til en grundlæggende lagerstedsaktiveret vare ved hjælp af en varemodtagelseskladde

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du registrerer varer ved hjælp af varemodtagelseskladden, når du bruger "grundlæggende lagerstedsfunktioner" i Lagerstyringsmodulet. Dette vil normalt blive udført af en modtagende medarbejder. Du kan køre denne procedure i USMF-demodatafirmaet ved hjælp af eksempelværdierne, der vises.  Hvis du ikke bruger USMF, skal du have en bekræftet indkøbsordre med en åben indkøbsordrelinje, før du starter denne guide. Varen på linjen skal på lager, og den skal ikke bruge produktvarianter og ikke have sporingsdimensioner. Og varen skal tilknyttes en lagringsdimensionsgruppe, hvor sted og lagersted er aktive.


## <a name="create-item-arrival-journal-header"></a>Opret en overskrift til varemodtagelseskladden
1. Gå til Lagerstyring > Kladdeposteringer > Varemodtagelse > Varemodtagelse.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
    * Hvis du bruger USMF, kan du skrive WHS. Hvis du bruger andre data, skal kladden, hvis navn du vælger, have følgende egenskaber: Undersøg plukplads skal angives til Nej, og Karantænestyring skal angives til Nej.  
4. Skriv en værdi i feltet Følgeseddel.
    * Dette er følgeseddel-id'et fra følgesedlen, der er udstedt af kreditoren. Tilføj et entydigt tal.  
5. Vælg indkøbsordren i feltet Tal.
6. Klik på OK.

## <a name="add-lines-to-item-arrival-journal"></a>Føj linjer til varemodtagelseskladden
1. Klik på Funktioner.
2. Klik på Opret linjer.
    * Linjerne kan indtastes manuelt i denne kladde eller oprettes automatisk. Dette viser, hvordan du oprette dette automatisk.  
3. Markér eller fjern markeringen af afkrydsningsfeltet Initialiser antal.
    * Dette initialiserer mængden på kladdelinjerne med den mængde, der ikke er registreret fra indkøbsordrelinjen.  
4. Klik på OK.

## <a name="post-the-journal"></a>Bogfør kladden
1. Klik på Bogfør.
2. Klik på OK.

## <a name="generate-the-product-receipt"></a>Generer produktkvitteringen
1. Klik på Funktioner.
2. Klik på Produktkvittering.
3. Klik på OK.

