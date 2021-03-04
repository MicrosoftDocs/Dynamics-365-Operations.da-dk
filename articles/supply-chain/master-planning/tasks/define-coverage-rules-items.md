---
title: Definere dækningsregler for varer
description: Det demodatafirma, der bruges til at oprette denne procedure, er USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11d92185bdbcf7aa1a668b6d2aa311805e42293c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424645"
---
# <a name="define-coverage-rules-for-items"></a>Definere dækningsregler for varer

[!include [banner](../../includes/banner.md)]

Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure viser, hvordan du opretter disponeringsregler og tilsidesætter disponeringsindstillinger for et bestemt element. Det viser også, hvordan du angiver standardindstillinger for lager.


## <a name="create-a-coverage-group"></a>Oprette en disponeringsgruppe
1. Gå til **Navigationsrude > Moduler > Varedisponering > Opsætning > Disponeringsgrupper**.
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Disponeringsgruppe**.
4. Skriv en værdi i feltet **Navn**.
5. Skriv en værdi i feltet **Kalender**. Vælg den kalender, som varedisponering bruger til at oprette genopfyldningsforslag for varer i denne gruppe.  
6. Vælg en indstilling i feltet **Disponeringskode**. Vælg 'Krav' til denne procedure.  
7. Angiv '90' i feltet **Disponeringstidshorisont (dage)**. For elementer i denne gruppe vil varedisponering oprette genopfyldningsforslag for op til 90 dage ud i fremtiden.  
8. Angiv '1' i feltet **Negative dage**.
9. Angiv '1' i feltet **Positive dage**.
10. Vis eller skjul sektionen **Andet**.
11. Angiv '1' i feltet **Modtagelsesmargen lagt til behovsdato** under sektionen **Sikkerhedsmargen i dage**. Hvis modtagelsesmargenen f.eks. angives til 1 dag, og en indkøbsordrelinje planlægges til tilgang d. 15. maj, beregner varedisponering den justerede modtagelsesdato som d. 16. maj.  
12. Angiv '1' i feltet **Afgangsmargen trukket fra behovsdato**. Hvis sikkerhedsmargenen f.eks. angives til 1 dag, og en salgsordrelinje planlægges til levering d. 15. maj, beregner varedisponering den justerede leveringsdato som d. 14. maj.  
13. Angiv '1' i feltet **Bestillingsmargen tilføjet til varens leveringstid**.
14. Klik på **Gem**.

## <a name="create-a-new-product"></a>Oprette et nyt produkt
1. Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Produktnummer**.
4. Skriv en værdi i feltet **Produktnavn**.
5. Klik på rullelisten i feltet **Varemodelgruppe** for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Klik på rullelisten i feltet **Varegruppe** for at åbne opslaget.
9. Find og vælg den ønskede post på listen.
10. Klik op linket i den valgte række på listen.
11. Klik på rullelisten i feltet **Lagringsdimensionsgruppe** for at åbne opslaget.
12. Find og vælg den ønskede post på listen.
13. Klik op linket i den valgte række på listen.
14. Klik på rullelisten i feltet **Sporingsdimensionsgruppe** for at åbne opslaget.
15. Find og vælg den ønskede post på listen.
16. Klik op linket i den valgte række på listen.
17. Klik på **OK**.

## <a name="setup-default-order-settings"></a>Konfigurer standardindstillinger for ordre
1. Klik på **Plan** i **handlingsruden**.
2. Klik på **Standardindstillinger for ordre** under **Ordreindstillinger**.
3. Angiv det sted, der bruges som standard, når indkøbsordrer oprettes, i feltet **Standardsted** under **Indkøbsordre**.
4. I feltet **Standardlagersted** skal du angive det sted, hvor varen opbevares.
5. Vis eller skjul sektionen **Lager**.
6. Skriv '10' i feltet **Multiplum**.
7. Skriv '10' i feltet **Min. ordreantal**.
8. Skriv '100' i feltet **Maks. ordreantal**.
9. Skriv '10' i feltet **Standardordreantal**.
10. Angiv et tal i feltet **Leveringstid for indkøb**.
11. Markér eller fjern markeringen i afkrydsningsfeltet **Arbejdsdage**.
12. Klik på **Gem**.
13. I feltet **Standardordretype** skal du vælge 'Indkøbsordre'.
14. Klik på **Gem**.
15. Luk siden. Luk siden Standardindstillinger for ordre.  

## <a name="add-an-item-to-a-coverage-group"></a>Føj en vare til en disponeringsgruppe
1. Vis eller skjul sektionen **Plan**.
2. Klik på rullelisten i feltet **Disponeringsgruppe** for at åbne opslaget.
3. Find den **Disponeringsgruppe**, du har oprettet, på listen.
4. Klik op linket i den valgte række på listen.

## <a name="create-item-coverage-rules"></a>Opret varedisponeringsregler
1. Klik på **Plan** i **handlingsruden**.
2. Klik på **Varedisponering** under **Disponering**.
3. Klik på **Ny**.
4. Klik på fanen **Generelt**.
5. Markér feltet på overskriften **Tilsidesæt indstillinger for disponeringsgruppe**.
6. Angiv '60' i feltet **Disponeringstidshorisont (dage)**. Selvom varerne i disponeringsgruppen Krav er planlagt 90 dage frem, bliver dette element planlagt 60 dage frem.  
7. Angiv '2' i feltet **Negative dage**.
8. Angiv '2' i feltet **Positive dage**.
9. Klik på fanen **Leveringstid**.
10. Markér feltet på overskriften **Indkøb**.
11. Angiv '5' i feltet **Indkøbstid**.
12. Klik på **Gem**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]