---
title: Oprette et produktnummernomenklatur for foruddefinerede produktvarianter
description: Denne vejledning viser, hvordan du konfigurerer en nomenklatur for produktnumre for foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a2e61fd99cb80a1a9cc3d8e985fb0f14e3c2fc2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844675"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Oprette et produktnummernomenklatur for foruddefinerede produktvarianter

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

