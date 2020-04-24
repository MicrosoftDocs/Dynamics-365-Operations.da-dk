---
title: Konfigurer et indkøbskategorihierarki
description: Denne fremgangsmåde viser, hvordan du opretter nye noder i et indkøbskategorihierarki, og hvordan du konfigurerer en indkøbskategori, der skal bruges i en indkøbsproces.
author: mkirknel
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eaab2093eb2531b63f27717d828f7064a8f9ed1d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207502"
---
# <a name="set-up-a-procurement-category-hierarchy"></a>Konfigurer et indkøbskategorihierarki

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du opretter nye noder i et indkøbskategorihierarki, og hvordan du konfigurerer en indkøbskategori, der skal bruges i en indkøbsproces. Disse opgaver udføres normalt af en indkøbschef. Før du starter denne procedure, skal der være en kategorihierarki af typen Indkøb. Hvis du bruger et demodatafirma, kan du køre denne procedure i USMF-firmaet.


## <a name="add-a-new-procurement-category"></a>Tilføj en ny indkøbskategori
1. Gå til **Navigationsrude > Moduler > Indkøb og forsyning > Konsignation > Indkøbskategorier**.
2. Vælg **Rediger kategorihierarki** i handlingsruden. Det aktuelle indkøbskategorihierarki vises i venstre side af siden. Du er ved at ændre hierarkiet.  
3. Vælg **Ny kategorinode** i handlingsruden. Systemet vælger øverste node som standard. Hvis du kører denne procedure som en opgaveguide, kan du klikke på knappen Lås op og vælge en anden overordnet node for at indsætte en ny node. Når det er gjort, skal du låse opgaveguiden igen og derefter klikke på Ny kategorinode.  
4. Skriv en værdi i feltet **Navn**.
5. Indtast en værdi i feltet **Beskrivelse**.
6. Indtast en værdi i feltet **Brugervenligt navn**. Det fulde navn er valgfrit. Det vises i kategoriopslag sammen med navnet på kategorien.  
7. Vælg **Gem**.

## <a name="add-products-to-your-new-procurement-category"></a>Føj produkter til den nye indkøbskategori
1. Gå til **Indkøb og forsyning > Konsignation > Indkøbskategorier**. Vælg den node, du lige har tilføjet. Hvis du kører denne procedure som en opgaveguide, skal du eventuelt låse opgaveguiden op for at vælge noden.  
2. Slå udvidelsen af sektionen **Produkter** til/fra.
3. Vælg **Tilføj** for at knytte produkter til indkøbskategorien.
4. Vælg de produkter, der skal føjes til indkøbskategorien.
5. Vælg pilen for at tilføje produkter i tabellen **Valgte**.
6. Vælg **OK**.
