---
title: Oprette et produktnummernomenklatur for foruddefinerede produktvarianter
description: Dette emne viser, hvordan du konfigurerer en nomenklatur for produktnumre til foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a4ad70a87cd8c6cab2e9853f4f6c52f574d318a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257406"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Oprette et produktnummernomenklatur for foruddefinerede produktvarianter

[!include [banner](../../includes/banner.md)]

Dette emne viser, hvordan du konfigurerer en nomenklatur for produktnumre til foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Den nye nomenklatur for produktnummer tildeles til produktdimensionsgruppen Farve og størrelse. Denne opgave udføres normalt af en produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Opret en nomenklatur for produktnummer
1. Vælg **Definition af produktvariantmodel**.
2. Vælg **Produktnomenklatur**.
3. Vælg **Ny**.
4. Angiv i feltet **Navn** et navn til nomenklaturen, der hjælper med at identificere målproduktdimensionsgruppen, for eksempel `ColorSize`.
5. Indtast en værdi i feltet **Beskrivelse**.
6. Vælg **Tilføj**.
7. Vælg **Produktmasternummer**.
8. Vælg **Tilføj**.
9. Vælg **Tekstkonstant**.
10. I feltet **Tekst** skal du indtaste en værdi.
11. Vælg **Tilføj**.
12. Vælg **Farve**.
13. Vælg **Tilføj**.
14. Vælg **Tekstkonstant**.
15. I feltet **Tekst** skal du indtaste en værdi.
16. Vælg **Tilføj**.
17. Vælg **Størrelse**.
18. Luk siden.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Tildel nomenklaturen til en produktmaster
1. Vælg **Produktdimensionsgrupper**.
2. Vælg **SizeCol-produktdimensionsgruppen**.
3. Vælg **Rediger**.
4. Vælg **Ja** i feltet **Brug nomenklatur**.
5. Indtast eller vælg en værdi i feltet **Nomenklatur for produktvariantnummer**.
6. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]