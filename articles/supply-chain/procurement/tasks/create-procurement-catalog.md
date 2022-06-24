---
title: Oprette et indkøbskatalog
description: Denne artikel beskriver, hvordan du opretter et indkøbskatalog.
author: GalynaFedorova
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e35e8c5b5c93fa9aac914f04e7ea658748cb052
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869540"
---
# <a name="create-a-procurement-catalog"></a>Oprette et indkøbskatalog

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du opretter et indkøbskatalog. Denne opgave vil normalt udføres af en professionel indkøber. Du lærer også, hvordan medarbejdere kan bruge kataloget, når de opretter en indkøbsrekvisition. Før du kan oprette et katalog, skal der være et indkøbskategorihierarki i systemet. Hierarkiet arves af det nye katalog sammen med alle de produkter, der er i hierarkiet. Du kan bruge denne vejledning i demodatafirmaet USMF, hvor indkøbskategorihierarkiet er tilgængeligt, såvel som de eksempler, der bruges i trinnene i proceduren.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Kontroller, at der findes et indkøbskategorihierarki
1. Gå til **Navigationsrude > Moduler > Indkøb og forsyning > Kreditorer > Indkøbskategorier**. Et indkøbskategorihierarki er tilgængeligt i USMF-demodatafirmaet, og produkter er føjet til kategorien **Kontormaskiner/computere**. Hvis du kører denne procedure som en opgaveguide, skal du låse opgaveguiden op, hvis du vil søge i kategorien. Hvis et hierarki ikke var tilgængeligt, skal du oprette det ved at klikke på **Nyt**. Det kan du kun gøre én gang.  
2. Luk siden.

## <a name="create-a-catalog"></a>Oprette et katalog
1. Gå til **Navigationsrude > Moduler > Indkøb og forsyning > Kataloger > Indkøbskataloger**.
2. Vælg **Nyt indkøbskatalog** for at åbne dialogboksen.
3. Skriv en værdi i feltet **Navn**.
4. Vælg **OK**.
5. Udvid **FIRMAS INDKØBSKATEGORIER** i træet.
6. Udvid **KONTORMASKINER** i træet.
7. Vælg **Computere** i træet.

  - Produkterne fra indkøbskategorien vises på listen. Hvis du vil føje et produkt til kategorien, skal du gøre det på siden **Indkøbskategorihierarki** eller på siden **Vareoplysninger**.  
  - Opdateringstypen **Standard** bestemmer, om nye produkter, der er føjet til indkøbskategorihierarkiet, er synlige i kataloget med det samme. Hvis opdateringstypen er indstillet til **Dynamisk**, kan ændringer ses øjeblikkeligt. Hvis opdateringstypen er **Statisk**, er nye produkter kun synlige for brugere af kataloget, når kataloget er blevet udgivet igen. Handlingen **Publicer** er tilgængelig i handlingsruden øverst på siden. Hvis produkter fjernes fra indkøbskategorihierarkiet, er ændringen straks synlig, uanset hvilken værdi der er i feltet **Standard** for opdateringstype.  

8. I handlingsruden skal du vælge **Kategorinavigation** og sikre, at **Aktivér** er valgt.
9. Vælg **Aktivér katalog**.
10. Luk siden.

## <a name="make-the-catalog-visible"></a>Gør kataloget synligt
1. Gå til **Navigationsrude > Moduler > Indkøb og forsyning > Opsætning > Politikker > Indkøbspolitikker**.
2. Vælg **Indkøbspolitikken USMF**. Du skal vælge indkøbspolitik, så den juridiske enhed, som arbejderen har knyttet til din brugerprofil, kan bestille produkter. I USMF-demodataene er administratorbrugeren knyttet til den arbejder, der hedder **Julia Funderburk**, og hun bestiller som standard produkter i USMF.  
3. Vælg det katalog, du netop har oprettet.
4. Vælg **OK**.

## <a name="use-the-catalog"></a>Brug kataloget
1. Gå til **Navigationsrude > Moduler > Indkøb og forsyning > Indkøbsrekvisitioner > Alle indkøbsrekvisitioner**.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Navn**.
4. Vælg **OK**.
5. Vælg **Tilføj produkter**.
6. Find og vælg den ønskede post på listen. Du kan bruge kategorihierarkiet til venstre eller filteret øverst på listen til at filtrere produkterne.  
7. Vælg **Tilføj til linjer**.
8. Vælg **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]