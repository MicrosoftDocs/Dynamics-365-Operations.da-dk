---
title: Oprette et produktnummernomenklatur for konfigurerede produktvarianter
description: Denne procedure viser, hvordan du konfigurerer en nomenklatur for produktnumre for konfigurerede produktvarianter, og hvordan den kan knyttes til en produktmaster, der kan konfigureres.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921005"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Oprette et produktnummernomenklatur for konfigurerede produktvarianter

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du konfigurerer en nomenklatur for produktnumre for konfigurerede produktvarianter, og hvordan den kan knyttes til en produktmaster, der kan konfigureres. Denne fremgangsmåde viser også, hvordan du kan opbygge en konfigurationsnomenklatur en produktkonfigurations modelkomponent. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Den nye nomenklatur for produktnumre er knyttet til produktmasteren D0004. Denne opgave udføres normalt af en produktdesigner.

## <a name="create-a-product-number-nomenclature"></a>Opret en nomenklatur for produktnummer

1. Gå til **Administration af produktoplysninger \> Opsætning \> Produktnomenklatur**.
1. Vælg **Ny**.
1. Skriv en værdi i feltet **Navn**.
1. Indtast en værdi i feltet **Beskrivelse**.
1. Vælg **Tilføj**.
1. Vælg **Produktmasternummer**.
1. Vælg **Tilføj**.
1. Vælg **Tekstkonstant**.
1. Markér den valgte række på listen.
1. I feltet **Tekst** skal du indtaste en værdi.
1. Vælg **Tilføj**.
1. Vælg **Konfiguration**.
1. Luk siden.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Tildel nomenklaturen for produktnummer til en produktmaster

1. Gå til **Administration af produktoplysninger \> Produkter \> Produktmastere**.
1. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet **Produktnummer** med værdien "D".
1. Vælg linket i den valgte række på listen.
1. Vælg **Rediger**.
1. Vælg *Ja* i feltet **Brug nomenklatur**.
1. Indtast eller vælg en værdi i feltet **Nomenklatur for produktvariantnummer**.
1. Luk siden.
1. Luk siden.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Opret nomenklatur for en komponent i en produktkonfigurationsmodel

1. Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.
1. Find og vælg den ønskede post på listen.
1. Vælg linket i den valgte række på listen.
1. Vælg **Rediger**.
1. Vælg *Ja* i feltet **Brug konfigurationsnomenklatur**.
1. Vælg **Tilføj**.
1. Vælg **Attributværdi**.
1. Markér den valgte række på listen.
1. Indtast eller vælg en værdi i feltet **Attribut**.
1. Vælg **Tilføj**.
1. Vælg **Tekstkonstant**.
1. Markér den valgte række på listen.
1. I feltet **Tekst** skal du indtaste en værdi.
1. Vælg **Tilføj**.
1. Vælg **Attributværdi**.
1. Markér den valgte række på listen.
1. Indtast eller vælg en værdi i feltet **Attribut**.
1. Vælg **Tilføj**.
1. Vælg **Tekstkonstant**.
1. Markér den valgte række på listen.
1. I feltet **Tekst** skal du indtaste en værdi.
1. Vælg **Tilføj**.
1. Vælg **Attributværdi**.
1. Markér den valgte række på listen.
1. Indtast eller vælg en værdi i feltet **Attribut**.
1. Vælg **Tilføj**.
1. Vælg **Tekstkonstant**.
1. Markér den valgte række på listen.
1. I feltet **Tekst** skal du indtaste en værdi.
1. Vælg **Tilføj**.
1. Vælg **Attributværdi**.
1. Markér den valgte række på listen.
1. Indtast eller vælg en værdi i feltet **Attribut**.
1. Vælg **Tilføj**.
1. Vælg **Tekstkonstant**.
1. Markér den valgte række på listen.
1. I feltet **Tekst** skal du indtaste en værdi.
1. Vælg **Tilføj**.
1. Vælge **Nummerserieværdi**.
1. Markér den valgte række på listen.
1. Indtast eller vælg en værdi i feltet **Nummerserie**.
1. Luk siden.
1. Luk siden.
1. Luk siden.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]