---
title: Oprette et produktnummernomenklatur for foruddefinerede produktvarianter
description: Dette emne viser, hvordan du konfigurerer en nomenklatur for produktnumre til foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fada426b03aa8a908c3351932a288c911cb8c60fa13ccbfbfd0ceed232759a88
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736034"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Oprette et produktnummernomenklatur for foruddefinerede produktvarianter

[!include [banner](../../includes/banner.md)]

Dette emne viser, hvordan du konfigurerer en nomenklatur for produktnumre til foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Den nye nomenklatur for produktnummer tildeles til produktdimensionsgruppen Farve og størrelse. Denne opgave udføres normalt af en produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Opret en nomenklatur for produktnummer

1. Gå til **Administration af produktoplysninger \> Opsætning \> Produktnomenklatur**.
1. Vælg **Ny**.
1. Angiv i feltet **Navn** et navn til nomenklaturen, der hjælper med at identificere målproduktdimensionsgruppen, for eksempel `ColorSize`.
1. Indtast en værdi i feltet **Beskrivelse**.
1. Vælg **Tilføj**.
1. Vælg **Produktmasternummer**.
1. Vælg **Tilføj**.
1. Vælg **Tekstkonstant**.
1. I feltet **Tekst** skal du indtaste en værdi.
1. Vælg **Tilføj**.
1. Vælg **Farve**.
1. Vælg **Tilføj**.
1. Vælg **Tekstkonstant**.
1. I feltet **Tekst** skal du indtaste en værdi.
1. Vælg **Tilføj**.
1. Vælg **Størrelse**.
1. Luk siden.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Tildel nomenklaturen til en produktmaster

1. Vælg **Produktdimensionsgrupper**.
2. Vælg **SizeCol-produktdimensionsgruppen**.
3. Vælg **Rediger**.
4. Vælg **Ja** i feltet **Brug nomenklatur**.
5. Indtast eller vælg en værdi i feltet **Nomenklatur for produktvariantnummer**.
6. Luk siden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]