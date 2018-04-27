--- 
title: Oprette et produktnummer for foruddefinerede produktvarianter
description: Denne vejledning viser, hvordan du konfigurerer en nomenklatur for produktnumre for foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe.
author: BibiSp
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3a1bfd4bd5f396c05277159ac112eaa8197d5818
ms.openlocfilehash: c423aab341ddad9383c4c95b9dbb63c9875c99ef
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a>Oprette et produktnummer for foruddefinerede produktvarianter

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne vejledning viser, hvordan du konfigurerer en nomenklatur for produktnumre for foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Den nye nomenklatur for produktnummer tildeles til produktdimensionsgruppen Farve og størrelse. Denne opgave udføres normalt af en produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Opret en nomenklatur for produktnummer
1. Klik på Definition af produktvariantmodel.
2. Klik på Produktnomenklatur.
3. Klik på Ny.
4. Angiv i feltet Navn et navn til nomenklaturen, der hjælper med at identificere målproduktdimensionsgruppen, for eksempel ColorSize.
5. Skriv en værdi i feltet Beskrivelse.
6. Klik på Tilføj.
7. Klik på Produktmasternummer.
8. Klik på Tilføj.
9. Klik på Tekstkonstant.
10. Skriv en værdi i feltet Tekst.
11. Klik på Tilføj.
12. Klik på Farve.
13. Klik på Tilføj.
14. Klik på Tekstkonstant.
15. Skriv en værdi i feltet Tekst.
16. Klik på Tilføj.
17. Klik på Størrelse.
18. Luk siden.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Tildel nomenklaturen til en produktmaster
1. Klik på Produktdimensionsgrupper.
2. Vælg produktdimensionsgruppen SizeCol.
3. Klik på Rediger.
4. Vælg Ja i feltet Brug nomenklatur.
5. Indtast eller vælg en værdi i feltet Nomenklatur for produktvariantnummer.
6. Luk siden.


