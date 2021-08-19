---
title: Oprette en stykliste for en dimensionsbaseret produktmaster
description: Til denne procedure skal du har fuldført de foregående 4 vejledninger i denne sekvens på otte optagelser.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 696cb96c6e934eaa44bfe6f51347df4541e5648f75f1ce07139787a1b235d69d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715765"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Oprette en stykliste for en dimensionsbaseret produktmaster

[!include [banner](../../includes/banner.md)]

Til denne procedure skal du har fuldført de foregående 4 vejledninger i denne sekvens på otte optagelser. De første fire optagelser opsætter de data, der kræves for at fuldføre denne procedure. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne opgave håndteres normalt af produktdesigneren.

## <a name="select-the-product"></a>Vælge produktet

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Markér den valgte række på listen.
    * Find den frigivne produktmasteren med teknologien til dimensionsbaseret konfiguration, som du oprettede i den første opgavevejledning i denne sekvens.  
1. Vælg **Tekniker** i handlingsruden.
1. Vælg **Styklisteversioner**.

## <a name="create-new-bom-and-bom-version"></a>Oprette en ny stykliste og en ny styklisteversion

1. Vælg **Ny**.
1. Vælg **Stykliste og styklisteversion**.
1. Skriv en værdi i feltet **Navn**.
    * Indstilling af en lokation  
    * Vi angiver ikke en specifik lokation for styklisten i denne procedure.  
1. Vælg **OK**.
1. Vælg **Ny**.
    * I denne procedure vil vi tilføje fire linjer til styklisten. To linjer repræsenterer kabelindstillinger, og to linjer repræsenterer kabinetindstillinger.  
1. Markér den valgte række på listen.
1. Indtast eller vælg en værdi i feltet **Varenummer**.
    * Vælg varenummeret A0001, HDMI 6'-kabler.  
1. Indtast eller vælg en værdi i feltet **Konfigurationsgruppe**.
    * Vælg den kabelkonfigurationsgruppe, der blev oprettet i vejledning 4 i denne sekvens.  
1. Vælg **Ny**.
    * Vælg varenummeret A0002, HDMI 12'-kabler.  
1. Markér den valgte række på listen.
1. Indtast eller vælg en værdi i feltet **Varenummer**.
1. Indtast eller vælg en værdi i feltet **Konfigurationsgruppe**.
    * Vælg kabelkonfigurationsgruppen igen.  
1. Vælg **Ny**.
1. Markér den valgte række på listen.
1. Indtast eller vælg en værdi i feltet **Varenummer**.
    * Vælg varenummeret D0002 Kabinet.  
1. Indtast eller vælg en værdi i feltet **Konfigurationsgruppe**.
    * Vælg kabinetkonfigurationsgruppen for denne styklistelinje.  
1. Vælg **Ny**.
1. Markér den valgte række på listen.
1. Indtast eller vælg en værdi i feltet **Varenummer**.
    * Vælg varenummeret M0007 Standardkabinet som den sidste styklistelinje.  
1. Indtast eller vælg en værdi i feltet **Konfigurationsgruppe**.
    * Vælg kabinetkonfigurationsgruppen for den sidste styklistelinje.  

## <a name="approve-and-activate"></a>Godkend og aktivér

1. Luk siden.
1. Vælg **Godkend**.
1. Indtast eller vælg en værdi i feltet **Godkendt af**.
1. Vælg *Ja* i feltet **Vil du også godkende styklisten?**.
1. Vælg **OK**.
1. Vælg **Aktivér**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]