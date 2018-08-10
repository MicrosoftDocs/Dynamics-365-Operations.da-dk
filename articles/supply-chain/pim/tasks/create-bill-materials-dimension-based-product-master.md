--- 
title: Oprette en stykliste for en dimensionsbaseret produktmaster
description: "Til denne procedure skal du har fuldført de foregående 4 vejledninger i denne sekvens på otte optagelser."
author: ShylaThompson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8b5432addd1dd79a64dcbb751a59cf3084a63ab1
ms.openlocfilehash: 05837c2b21957133729074f614a6d3d7b7c08dad
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Oprette en stykliste for en dimensionsbaseret produktmaster

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


