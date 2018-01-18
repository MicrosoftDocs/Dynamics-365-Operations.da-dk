--- 
title: Oprette foruddefinerede produktvarianter
description: "Denne procedure fører dig gennem oprettelsen af produktvarianter for en produktmaster ved hjælp af kombinationer af produktdimensioner."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c49d25004b19084276404cf887188e89200afa32
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-predefined-product-variants"></a>Oprette foruddefinerede produktvarianter

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure fører dig gennem oprettelsen af produktvarianter for en produktmaster ved hjælp af kombinationer af produktdimensioner. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-a-product-master"></a>Oprette en produktmaster
1. Gå til Administration af produktoplysninger > Produkter > Produktmastere.
2. Klik på Ny.
3. Skriv en værdi i feltet Produktnummer.
    * Manuel indtastning af et produktnummer kræves kun, hvis der ingen nummerserie er indstillet for produktnummerfeltet. Med andre ord kan du springe dette trin over, hvis nummerserien er indstillet for feltet.  
4. Angiv en værdi i feltet Produktnavn.
5. Indtast eller vælg en værdi i feltet Produktdimensionsgruppe.
    * Vælg produktdimensionsgruppen SizeCol (størrelse og farve).  
6. Klik på OK.

## <a name="add-product-dimensions"></a>Tilføje produktdimensioner
1. Klik på Produktdimensioner.
    * Dette eksempel viser, hvordan du manuelt angiver produktdimensioner. Du kan også vælge en størrelses-, farve- eller typografigruppe, der indeholder de produktdimensionsværdier, du vil bruge.  
2. Klik på Ny.
3. Markér den valgte række på listen.
4. Indtast eller vælg en værdi i feltet Størrelse.
5. Skriv en værdi i feltet Navn.
6. Klik på Ny.
7. Markér den valgte række på listen.
8. Indtast eller vælg en værdi i feltet Størrelse.
9. Skriv en værdi i feltet Navn.
10. Klik på fanen Farver.
11. Klik på Ny.
12. Markér den valgte række på listen.
13. Indtast eller vælg en værdi i feltet Farve.
14. Skriv en værdi i feltet Navn.
15. Klik på Ny.
16. Markér den valgte række på listen.
17. Indtast eller vælg en værdi i feltet Farve.
18. Skriv en værdi i feltet Navn.
19. Klik på Gem.
20. Luk siden.

## <a name="generate-product-variants"></a>Generere produktvarianter
1. Klik på Produktvarianter.
2. Klik på Forslag til varianter.
3. Klik på Vælg alle.
    * I dette eksempel vælges alle mulige varianter. Hvis kun en delmængde af de mulige produktdimensionskombinationer skal bruges til at oprette varianter, kan du vælge de enkelte poster.  
4. Klik på Opret.
    * Du kan generere beskrivelser for alle de varianter, der er baseret på en kombination af dimensionsværdier for produktet. Beskrivelserne er valgfrie.  
5. Klik på Gem.


