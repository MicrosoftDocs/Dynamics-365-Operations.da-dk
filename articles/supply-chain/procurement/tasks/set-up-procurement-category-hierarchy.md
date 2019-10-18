---
title: Konfigurer et indkøbskategorihierarki
description: Denne fremgangsmåde viser, hvordan du opretter nye noder i et indkøbskategorihierarki, og hvordan du konfigurerer en indkøbskategori, der skal bruges i en indkøbsproces.
author: mkirknel
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7010a1c612b9b3884c675f578657d951da06c38
ms.sourcegitcommit: 25fe679b73663fda6b5b3c32646026d0993a9f00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/12/2019
ms.locfileid: "1995276"
---
# <a name="set-up-a-procurement-category-hierarchy"></a>Konfigurer et indkøbskategorihierarki

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
