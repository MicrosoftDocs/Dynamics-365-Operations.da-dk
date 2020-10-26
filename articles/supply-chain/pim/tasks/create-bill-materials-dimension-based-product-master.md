---
title: Oprette en stykliste for en dimensionsbaseret produktmaster
description: Til denne procedure skal du har fuldført de foregående 4 vejledninger i denne sekvens på otte optagelser.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7961cfb4ad0e20c49d327d83f56c08811598ac1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986281"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Oprette en stykliste for en dimensionsbaseret produktmaster

[!include [banner](../../includes/banner.md)]

Til denne procedure skal du har fuldført de foregående 4 vejledninger i denne sekvens på otte optagelser. De første fire optagelser opsætter de data, der kræves for at fuldføre denne procedure. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne opgave håndteres normalt af produktdesigneren.


## <a name="select-the-product"></a>Vælge produktet
1. Klik på Vedligeholdelse af frigivet produkt.
2. Klik på Frigivne produkter.
3. Markér den valgte række på listen.
    * Find den frigivne produktmasteren med teknologien til dimensionsbaseret konfiguration, som du oprettede i den første opgavevejledning i denne sekvens.  
4. Klik på Tekniker i handlingsruden.
5. Klik på Styklisteversioner.

## <a name="create-new-bom-and-bom-version"></a>Oprette en ny stykliste og en ny styklisteversion
1. Klik på Ny.
2. Klik på Stykliste og Styklisteversion.
3. Skriv en værdi i feltet Navn.
    * Indstilling af en lokation  
    * Vi angiver ikke en specifik lokation for styklisten i denne procedure.  
4. Klik på OK.
5. Klik på Ny.
    * I denne procedure vil vi tilføje fire linjer til styklisten. To linjer repræsenterer kabelindstillinger, og to linjer repræsenterer kabinetindstillinger.  
6. Markér den valgte række på listen.
7. Indtast eller vælg en værdi i feltet Varenummer.
    * Vælg varenummeret A0001, HDMI 6'-kabler.  
8. Indtast eller vælg en værdi i feltet Konfiguration.
    * Vælg den kabelvariantgruppe, der blev oprettet i vejledning 4 i denne sekvens.  
9. Klik på Ny.
    * Vælg varenummeret A0002, HDMI 12'-kabler.  
10. Markér den valgte række på listen.
11. Indtast eller vælg en værdi i feltet Varenummer.
12. Indtast eller vælg en værdi i feltet Konfiguration.
    * Vælg igen variantgruppen Kabel.  
13. Klik på Ny.
14. Markér den valgte række på listen.
15. Indtast eller vælg en værdi i feltet Varenummer.
    * Vælg varenummeret D0002 Kabinet.  
16. Indtast eller vælg en værdi i feltet Konfiguration.
    * Vælg variantgruppen Kabinet til denne styklistelinje.  
17. Klik på Ny.
18. Markér den valgte række på listen.
19. Indtast eller vælg en værdi i feltet Varenummer.
    * Vælg varenummeret M0007 Standardkabinet som den sidste styklistelinje.  
20. Indtast eller vælg en værdi i feltet Konfiguration.
    * Vælg variantgruppen Kabinet til den sidste styklistelinje.  

## <a name="approve-and-activate"></a>Godkend og aktivér
1. Luk siden.
2. Klik på Godkend.
3. Indtast eller vælg en værdi i feltet Godkendt af.
4. Vælg Ja til Vil du også godkende styklisten? .
5. Klik på OK.
6. Klik på Aktiver.

