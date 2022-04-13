---
title: Definere dækningsregler for varer
description: Denne procedure viser, hvordan du opretter disponeringsregler og tilsidesætter disponeringsindstillinger for et bestemt element. Det viser også, hvordan du angiver standardindstillinger for lager.
author: t-benebo
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bca0e1786adb08a7cd4795b49c974ab95183b1dd
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469305"
---
# <a name="define-coverage-rules-for-items"></a>Definere dækningsregler for varer

[!include [banner](../../includes/banner.md)]

Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure viser, hvordan du opretter disponeringsregler og tilsidesætter disponeringsindstillinger for et bestemt element. Det viser også, hvordan du angiver standardindstillinger for lager.

## <a name="create-a-coverage-group"></a>Oprette en disponeringsgruppe

Opret en disponeringsgruppe ved at gøre følgende:

1. Gå til **Navigationsrude > Moduler > Varedisponering > Opsætning > Disponeringsgrupper**.
1. Vælg **Ny**.
1. Skriv en værdi i feltet **Disponeringsgruppe**.
1. Skriv en værdi i feltet **Navn**.
1. Skriv en værdi i feltet **Kalender**. Vælg den kalender, som varedisponering bruger til at oprette genopfyldningsforslag for varer i denne gruppe.  
1. Vælg en indstilling i feltet **Disponeringskode**. Vælg 'Krav' til denne procedure.  
1. Angiv '90' i feltet **Disponeringstidshorisont (dage)**. For elementer i denne gruppe vil varedisponering oprette genopfyldningsforslag for op til 90 dage ud i fremtiden.  
1. Angiv '1' i feltet **Negative dage**.
1. Angiv '1' i feltet **Positive dage**.
1. Vis eller skjul sektionen **Andet**.
1. Angiv '1' i feltet **Modtagelsesmargen lagt til behovsdato** under sektionen **Sikkerhedsmargen i dage**. Hvis modtagelsesmargenen f.eks. angives til 1 dag, og en indkøbsordrelinje planlægges til tilgang d. 15. maj, beregner varedisponering den justerede modtagelsesdato som d. 16. maj.
1. Angiv '1' i feltet **Afgangsmargen trukket fra behovsdato**. Hvis sikkerhedsmargenen f.eks. angives til 1 dag, og en salgsordrelinje planlægges til levering d. 15. maj, beregner varedisponering den justerede leveringsdato som d. 14. maj.  
1. Angiv '1' i feltet **Bestillingsmargen tilføjet til varens leveringstid**.
1. Vælg **Gem**.

## <a name="create-a-new-product"></a>Opret et nyt produkt

Opret et nyt produkt ved at gøre følgende:

1. Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.
1. Vælg **Ny**.
1. Skriv en værdi i feltet **Produktnummer**.
1. Skriv en værdi i feltet **Produktnavn**.
1. Vælg rullelisten i feltet **Varemodelgruppe** for at åbne opslaget.
1. Find og vælg den ønskede post på listen.
1. Vælg linket i den valgte række på listen.
1. Vælg rullelisten i feltet **Varegruppe** for at åbne opslaget.
1. Find og vælg den ønskede post på listen.
1. Vælg linket i den valgte række på listen.
1. Vælg rullelisten i feltet **Lagringsdimensionsgruppe** for at åbne opslaget.
1. Find og vælg den ønskede post på listen.
1. Vælg linket i den valgte række på listen.
1. Vælg rullelisten i feltet **Sporingsdimensionsgruppe** for at åbne opslaget.
1. Find og vælg den ønskede post på listen.
1. Vælg linket i den valgte række på listen.
1. Vælg **OK**.

## <a name="set-up-default-order-settings"></a>Konfigurer standardindstillinger for ordre

Du kan angive standardindstillinger for ordren på følgende måde:

1. Vælg **Plan** i **handlingsruden**.
1. Vælg **Standardindstillinger for ordre** under **Ordreindstillinger**.
1. Angiv det sted, der bruges som standard, når indkøbsordrer oprettes, i feltet **Standardsted** under **Indkøbsordre**.
1. I feltet **Standardlagersted** skal du angive det sted, hvor varen opbevares.
1. Vis eller skjul sektionen **Lager**.
1. Skriv '10' i feltet **Multiplum**.
1. Skriv '10' i feltet **Min. ordreantal**.
1. Skriv '100' i feltet **Maks. ordreantal**.
1. Skriv '10' i feltet **Standardordreantal**.
1. Angiv et tal i feltet **Leveringstid for indkøb**.
1. Markér eller fjern markeringen i afkrydsningsfeltet **Arbejdsdage**.
1. Vælg **Gem**.
1. I feltet **Standardordretype** skal du vælge 'Indkøbsordre'.
1. Vælg **Gem**.
1. Luk siden. Luk siden Standardindstillinger for ordre.  

## <a name="add-an-item-to-a-coverage-group"></a>Føj en vare til en disponeringsgruppe

Tilføj en vare i en disponeringsgruppe ved at gøre følgende:

1. Vis eller skjul sektionen **Plan**.
1. Vælg på rullelisten i feltet **Disponeringsgruppe** for at åbne opslaget.
1. Find den **Disponeringsgruppe**, du har oprettet, på listen.
1. Vælg linket i den valgte række på listen.

## <a name="create-item-coverage-rules"></a>Opret varedisponeringsregler

Opret varedisponeringsregler ved at gøre følgende:

1. Vælg **Plan** i **handlingsruden**.
1. Vælg **Varedisponering** under **Disponering**.
1. Vælg **Ny**.
1. Vælg fanen **Generelt**.
1. Markér feltet på overskriften **Tilsidesæt indstillinger for disponeringsgruppe**.
1. Angiv '60' i feltet **Disponeringstidshorisont (dage)**. Selvom varerne i disponeringsgruppen Krav er planlagt 90 dage frem, bliver dette element planlagt 60 dage frem.  
1. Angiv '2' i feltet **Negative dage**.
1. Angiv '2' i feltet **Positive dage**.
1. Vælg fanen **Leveringstid**.
1. Markér feltet på overskriften **Indkøb**.
1. Angiv '5' i feltet **Indkøbstid**.
1. Vælg **Gem**.

> [!NOTE]
> For producerede varer bruges **produktionsgennemløbstiden**, hvis der ikke findes en rute for varen. Hvis der er knyttet en aktiv rute til varen, planlægger varedisponering ordren og beregner dens datoer i overensstemmelse med ressourcernes rutetider og kapacitet (hvis det er relevant).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
