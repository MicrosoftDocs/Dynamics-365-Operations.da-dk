---
title: Skærmlayouts til demodata i Modern POS (MPOS) og Cloud POS
description: Dette emne indeholder oplysninger om de skærmlayout, der følger med demodatasæt til POS-oplevelserne i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 5e75210e77d1187f482d716f795ec0155553cb3f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213619"
---
# <a name="demo-data-screen-layouts-in-modern-pos-mpos-and-cloud-pos"></a>Skærmlayouts til demodata i Modern POS (MPOS) og Cloud POS

[!include [banner](includes/banner.md)]

Dette emne indeholder oplysninger om de skærmlayout, der følger med demodatasæt til POS-oplevelserne i Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

De eksempelskærmlayouts, der følger med Commerce-demodata, leverer indhold, der er optimeret til forskellige detailsegmenter, butiksmedarbejderroller og enheder. Et enkelt layout kan indeholde flere layoutstørrelser og kombinationer af knapmatricer for at sikre dækning, når butiksmedarbejderne flytter mellem enheder og stationer. I dette emne beskrives forskellene mellem disse layouts, de operationer, de indeholder, og den samlede oplevelse, de leverer.

![Layouts til demodata på tværs af enheder](../commerce/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>Anatomi af et skærmlayout-id

For at finde skærmlayouts skal du gå til **Retail og Commerce** \> **Konfiguration af kanal** \> **POS-opsætning** \> **POS** \> **Skærmlayout**.

![Side til skærmlayouts](../commerce/media/demo-screen-layouts-fig-2-1.png)

Skærmlayout-id'er må være på op til 10 tegn. Id'et er en streng, der består af tre dele af oplysninger i følgende rækkefølge:

1. Regnskab
2. Layoutversion
3. Karakter

### <a name="company"></a>Regnskab

| Bogstav | Regnskab         |
|--------|-----------------|
| T      | Adventure Works |
| F      | Fabrikam        |
| A      | Contoso         |

### <a name="layout-version"></a>Layoutversion

| Versionsnummer | Betegnelse                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | Den grundlæggende version, der understøtter flere skærmstørrelser til forskellige enheder og størrelsesforhold |
| 3.1            | Den grundlæggende version, der har yderligere understøttelse af panelet **Anbefalede produkter**        |
| 4              | Den udvidede version til det opdaterede layout for det udvidede Fabrikam                                  |

### <a name="persona"></a>Karakter

| Forkortelse | Karakter       | Indhold |
|--------------|---------------|----------|
| CSH          | Kasseassistent       | Kasserer-layouts omfatter alle transaktionsrelaterede handlinger, f.eks. kundeordrer, returneringer, rabatter, annulleringer og gavekort. Disse layout omfatter også de daglige opgaver til lagerstyring, f.eks. pristjek, lageropslag og lageroptællinger. Der er også grundlæggende styring af skift med startbeløb, afbrydelse af skift og tidsregistrering. |
| MGR          | Butikschef | Layouts til butikschef omfatter alle posteringsrelaterede operationer, der findes i kassererens layout, men omfatte også tilsidesættelser af moms. Disse layout omfatter også de daglige opgaver til lagerstyring, f.eks. pristjek, lageropslag og lageroptællinger. Styring af skift er medtaget for at starte, afbryde og lukke skift. Desuden omfatter layouts kasseskuffeoperationer for posteringer, fjernelse, kasseoptællinger og aflevering i pengeskab og bank. Endelig omfatter disse layouts adgangen til ydeevnerapporter og mulighed for at udskrive X- og / Z-rapporter. |
| STK          | Lagermedarbejder   | Layouts til lagermedarbejder er optimeret til lagerstyring. De omfatter adgangen til de daglige opgaver til pristjek, lageropslag, pluk og tilgang, statusoptællinger og adskillelse af sæt. Disse layouts indeholder også grundlæggende operationer for skift, f.eks. tidsregistrering og afbrydelse af skift. Selvom disse layouts primært er beregnet til back-office-opgaver, har lagermedarbejdere de samme operationer som kasserere med hensyn til transaktionsskærmbilleder. |

### <a name="example-layout"></a>Eksempellayout

Her er et eksempel på et skærmlayout-id for Fabrikam-virksomheden, layout version 4 og karakteren butikschef:

F4MGR

I følgende illustration vises et eksempel på velkomstskærmbilledet for en butikschef hos Fabrikam.

![Velkomstskærmbillede for Fabrikam-butikschefen](../commerce/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a>Layoutstørrelser

### <a name="full-vs-compact-layouts"></a>Fuldstændige vs. kompakte layouts

Et skærmlayout kan indeholde konfigurationer for både fuldstændige og kompakte enheder. Derfor kan en bruger blive knyttet til et enkelt skærmlayout, der fungerer på tværs af forskellige størrelser og formfaktorer i butikken.

- **Moderne POS – Fuld** – Fulde layouts er typisk bedst til større skærme som pc-skærme eller tablets. Brugere kan vælge de elementer på brugergrænsefladen, som layoutet omfatter, angive størrelsen på og placeringen af disse elementer og konfigurere deres detaljerede egenskaber. Fulde layouts understøtter både stående og liggende konfigurationer.
- **Moderne POS - Kompakt** – Kompakte layouts er typisk bedst til telefoner eller små tablets. Designmulighederne er begrænsede på kompakte enheder. Brugerne kan konfigurere kolonnerne og felterne til kvitteringsruden og ruden med totaler.

### <a name="screen-resolutions-that-are-provided"></a>Skærmopløsninger, der følger

Følgende tabel viser de layoutstørrelser, som findes til typiske skærmopløsninger.

| Layouttype | Løsning | Størrelsesforhold | Måldisplay          |
|-------------|------------|--------------|-------------------------|
| Komprimer\*   | 480 × 853  | 16:9         | Telefoner                  |
| Fuld        | 1024 × 768 | 4:3          | Tablets                 |
| Fuld\*      | 1280 × 720 | 16:9         | Tablets                 |
| Fuld        | 1366 × 768 | 16:9         | Tablets, større skærme |
| Fuld        | 1440 × 960 | 3:2          | Tablets, større skærme |
| Fuld\*      | 1536 × 864 | 16:9         | Tablets, større skærme |

\* Disse yderligere layoutstørrelser er kun tilgængelige i Adventure Works- og Fabrikam-layouts.

> [!TIP]
> POS vælger automatisk layoutstørrelser, baseret på den nærmeste størrelse, der er tilgængelig for skærmopløsningen i det aktuelle appvindue. Hvis du vil finde det skærmlayout-id og den layoutopløsning, der aktuelt bruges i Modern POS (MPOS) eller Retail Cloud POS (CPOS), skal du åbne siden **Indstillinger** siden, og se i afsnittet **Sessionsoplysninger**. Du kan også se den faktiske vinduesopløsning for dit aktuelle program eller browserramme. Når du har disse oplysninger, du kan finde kilden til indholdet i layoutet i Retail ved at gå til **Konfiguration af kanal** \> **POS-opsætning** \> **POS** \> **Skærmlayout**.

![Skærmlayouts og layoutopløsninger/-størrelser i Commerce og POS](../commerce/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>Firmaer og brands

Hvert fiktivt firma henvender sig til en andet detailsegment og omfatter produktkataloger, som er tilpasset til virksomhedens marked. Hver virksomhed har et entydigt visuelt brand, der følger med dets produkter. Brandingelementerne omfatter fremhævelsesfarve, mørkt eller lyst tema og ledsagende billeder, der giver realistiske oplevelser.

### <a name="company-segment-and-visual-characteristics"></a>Firmasegment og visuelle egenskaber

| Regnskab         | Adresse | Segment        | Markering | Tema |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | Seattle  | Sportsudstyr | Blå   | Mørk  |
| Fabrikam        | San Francisco  | Mode        | Grøn  | Lys |
| Contoso         | Boston   | Elektronik    | Rød    | Mørk  |

> [!NOTE]
> Adventure Works og Fabrikam er de to største brands. Contoso er tilgængelig, men ikke alle layouts medfølger.

Nedenstående illustrationer viser eksempler på velkomstsiden og transaktionssiden for de tre fiktive firmaer.

### <a name="adventure-works"></a>Adventure Works

![Velkomstside i demodata til Adventure Works](../commerce/media/demo-screen-layouts-fig-4-1a.png)

![Transaktionsside i demodata til Adventure Works](../commerce/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![Velkomstside i demodata til Fabrikam](../commerce/media/demo-screen-layouts-fig-4-2a.png)

![Transaktionsside i demodata til Fabrikam](../commerce/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>Contoso

![Layout af demodata til Contoso](../commerce/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>Matrix for brugerlogon

Der er angivet brugere til de forskellige skærmlayouts. Ved hjælp af tabellen nedenfor, skal du være i stand til at få adgang til alle skærmbillederne. Du skal blot logge på ved brug af et passende operatør-id.

| Regnskab         | Skærmlayout-id | Karakter       | Operatør-id'er           |
|-----------------|------------------|---------------|------------------------|
| Adventure Works | A3MGR            | Butikschef | 000154, 000137, 000073 |
| Adventure Works | A3CSH            | Kasseassistent       | 000150, 000175, 000165 |
| Adventure Works | A3STK            | Lagermedarbejder   | 000155, 000181, 000152 |
| Fabrikam        | F4MGR            | Butikschef | 000160, 000713         |
| Fabrikam        | F3CSH            | Kasseassistent       | 000161, 000113, 000114 |
| Fabrikam        | F3STK            | Lagermedarbejder   | 000164, 000112, 000123 |
| Contoso         | C3MGR            | Butikschef | 000100, 000111         |
| Contoso         | C3CSH            | Kasseassistent       | 000110, 000120         |
| Contoso         | Ikke tilgængelig   | Lagermedarbejder   | Ikke tilgængelig         |

> [!TIP]
> For at få de bedste resultater skal du aktivere et register i den tilsvarende butikslokalitet og angive firmaet til firmaet for den karakter, som du vil bruge, når du logger på. På denne måde kan du hjælpe med til at garantere, at den visuelle profil og brandingbillederne justeres på tværs af oplevelsen. Hvis du f.eks. er interesseret i at se et layout til Fabrikam for en kasserer, skal du aktivere et register i butikken i Houston.

<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail and Commerce \> Channel setup \> POS setup \> POS \> Images**. -->

<!-- ![Images in Dynamics 365 Commerce](../commerce/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../commerce/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->


[!INCLUDE[footer-include](../includes/footer-banner.md)]