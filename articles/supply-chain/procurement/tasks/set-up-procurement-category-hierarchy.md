--- 
title: "Konfigurer et indkøbskategorihierarki"
description: "Denne fremgangsmåde viser, hvordan du opretter nye noder i et indkøbskategorihierarki, og hvordan du konfigurerer en indkøbskategori, der skal bruges i en indkøbsproces."
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6ad5c8552a6989e9093d0b1325754bc0f6d19372
ms.openlocfilehash: 4541d029c9c3be3ee42332e5d8ff183dd503f13e
ms.contentlocale: da-dk
ms.lasthandoff: 11/06/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a>Konfigurer et indkøbskategorihierarki

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du opretter nye noder i et indkøbskategorihierarki, og hvordan du konfigurerer en indkøbskategori, der skal bruges i en indkøbsproces. Disse opgaver udføres normalt af en indkøbschef. Før du starter denne procedure, skal der være en kategorihierarki af typen Indkøb. Hvis du bruger et demodatafirma, kan du køre denne procedure i USMF-firmaet.


## <a name="add-a-new-procurement-category"></a>Tilføj en ny indkøbskategori
1. Gå til Indkøb og forsyning > Indkøbskategorier.
2. Klik på Rediger kategorihierarkityper.
    * Det aktuelle indkøbskategorihierarki vises i venstre side af siden. Du er ved at ændre hierarkiet.  
3. Klik på Ny kategorinode.
    * Systemet vælger øverste node som standard. Hvis du kører denne procedure som en opgaveguide, kan du klikke på knappen Lås op og vælge en anden overordnet node for at indsætte en ny node. Når det er gjort, skal du låse opgaveguiden igen og derefter klikke på Ny kategorinode.  
4. Skriv en værdi i feltet Navn.
5. Skriv en værdi i feltet Beskrivelse.
6. Indtast en værdi i feltet Brugervenligt navn.
    * Det fulde navn er valgfrit. Det vises i kategoriopslag sammen med navnet på kategorien.  
7. Klik på Gem.

## <a name="add-products-to-your-new-procurement-category"></a>Føj produkter til den nye indkøbskategori
1. Gå til Indkøb og forsyning > Indkøbskategorier.
    * Vælg den node, du lige har tilføjet. Hvis du kører denne procedure som en opgaveguide, skal du eventuelt låse opgaveguiden op for at vælge noden.  
2. Slå udvidelsen af sektionen Produkter til/fra.
3. Klik på Tilføj for at knytte produkter til indkøbskategorien.
4. Vælg det produkt, der skal føjes til indkøbskategorien.
5. Klik på pilen for at vælge produktet.
6. Vælg et andet produkt, der skal føjes til indkøbskategorien.
7. Klik på pilen for at vælge produktet.
8. Klik på OK.

## <a name="add-approved-and-preferred-vendors"></a>Tilføj godkendte og foretrukne kreditorer
1. Slå udvidelsen af sektionen Kreditorer til/fra.
2. Klik på Tilføj.
    * Du kan føje en kreditor til en indkøbskategori og angive, om en kreditor foretrækkes eller blot er godkendt for kategorien. Når du sletter en leverandør i en kategori, slettes de historiske posteringer for leverandøren i kategorien ikke.   
3. Vælg den kreditor, der skal føjes til kategorien.
4. Klik på pilen for at vælge kreditoren.
5. Klik på OK.
6. Vælg den kreditorrække, du vil redigere.
7. Vælg en indstilling i feltet Kreditorstatus.
    * Indstillingen til valg af kreditor i Politikregel for kategori bestemmer, om foretrukne, godkendte eller alle kreditorer er tilgængelige på indkøbsrekvisitioner.   

## <a name="add-additional-information-to-the-category"></a>Føj yderligere oplysninger til kategorien
1. Slå udvidelsen af sektionen Kriteriegrupper for kreditorevaluering til/fra.
    * Denne fane giver dig mulighed for at definere, hvilke kriterier kreditorerne i indkøbskategorien skal bedømmes ud fra. Det kan du gøre ved at klikke på Tilføj og derefter vælge en kreditorevalueringsgruppe, der indeholder de ønskede kriterier.  
2. Slå udvidelsen af sektionen Spørgeskemaer til/fra.
    * Denne fane giver dig mulighed for at tilføje spørgeskemaer, der vises på rekvisitionen, så længe du angiver aktivitetstypen til "Rekvisition". Anmoderen skal derefter udfylde et spørgeskema, før de kan sende en rekvisition for det eller de specifikke produkter i indkøbskategorien.  
3. Slå udvidelsen af sektionen Varemomsgrupper til/fra.
4. Klik på rullelisten i feltet Varemomsgruppe: for at åbne opslaget.
5. Vælg en momsgruppe.
6. Slå udvidelsen af afsnittet Kategoriside til/fra.
    * Kategorisider oprettes på siden Kategorihierarki. De indeholder oplysninger om indkøbskategorien, f.eks. oplysninger om typen af produkter i en kategori, billeder af produkter i en kategori eller meddelelser, f.eks. rabatter i en kategori. Oplysningerne på en kategoriside vises på indkøbsrekvisitioner.  
7. Luk siden.


