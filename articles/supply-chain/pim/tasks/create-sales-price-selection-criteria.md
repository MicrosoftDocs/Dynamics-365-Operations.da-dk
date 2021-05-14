---
title: Oprette kriterier for valg af salgspris
description: Denne procedure viser, hvordan du opretter et valgkriterium for salgspris til attributbaserede salgsprismodeller.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920525"
---
# <a name="create-sales-price-selection-criteria"></a>Oprette kriterier for valg af salgspris

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du opretter et valgkriterium for salgspris til attributbaserede salgsprismodeller. Denne procedure kræver, at der er mindst én tilgængelig salgspris. I dette eksempel bruges prismodellen for salgsprismodellen for højttalerløsningen i demodatafirmaet USMF. Normalt bruger en produktchef denne procedure.

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Tilføj et nyt kriterium for en eksisterende salgsprismodel

1. Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.
1. På listen skal du vælge rækken for produktmodellen for højttalerløsning, men ikke vælge linket for modelnavnet.
1. Vælg **Model** i handlingsruden.
1. Vælg **Prismodelkriterier**.
1. Vælg **Ny**.
1. Skriv 'Kundegruppe 10' i feltet **Navn**.
    * Navnet på prismodelkriteriet bruges til at identificere de underliggende udvælgelseskriterier.  
1. Indtast eller vælg en værdi i feltet **Prismodel**.
1. I feltet **Ordretype** skal du vælge *Salgsordre*.
    * Ordretypen bestemmer de databasefelter, der er tilgængelige for valgforespørgslen.  
1. Indtast en dato i feltet **Gyldig fra**.
1. Angiv en dato i feltet **Udløber senest**.
1. Vælg **Gem**.

## <a name="create-the-query-for-the-selection-criteria"></a>Opret forespørgslen for udvælgelseskriterierne

1. Vælg **Rediger**.
2. Vælg *Kunder* i feltet **Tabel**.
3. Vælg *Kundegruppe* i feltet **Felt**.
    * I dette eksempel bruger vi en specifik kundegruppe til udvælgelseskriterierne.  
4. Vælg *Kundegruppe 10* i feltet **Kriterier**.
5. Vælg **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]