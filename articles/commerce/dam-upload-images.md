---
title: Overføre billeder
description: Denne artikel beskriver, hvordan du overfører billeder i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d937e8c0e00ce28b0e4a4c2feab3ac1c8f075916
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283373"
---
# <a name="upload-images"></a>Overføre billeder

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du overfører billeder i Microsoft Dynamics 365 Commerce-webstedsgenerator.

I Commerce-webstedsgeneratorens mediebibliotek kan du uploade billeder enkeltvist eller masseupload ved hjælp af mapper. Du bør altid uploade billedet med den højeste opløsning og kvalitet, da funktionen til tilpasning af billedstørrelsen optimerer automatisk billedet for forskellige billeder og pausepunkterne.

### <a name="image-information-specified-during-upload"></a>Billedoplysninger, der er angivet under upload

Når du uploader et billede, kan du angive følgende oplysninger.

- **Titel, Alternativ tekst, Beskrivelse, Nøgleord**: Metadata for billedet eller billederne. Titel og alternativ tekst er obligatoriske værdier.
- **Vælg kategori**:
    - **Ingen**: Bruges til en e-handelsbilledhistorie eller -billeder.
    - **Produkt, Kategori, Kunde, Medarbejder, Katalog**: Bruges til Dynamics 365 Commerce-omni-kanalbillede eller -billeder.
- **Publicer aktiver efter upload**: Når dette afkrydsningsfelt er markeret, udgives billedet eller billederne straks efter upload.

> [!NOTE]
> - Billedaktiver med en tildelt kategori mærkes også automatisk med kategorien som et nøgleord for at hjælpe med at søge efter aktiver af en bestemt kategori.
> - På sider med produktdetaljer genereres **Alt-tekst** dynamisk ved hjælp af produktnavnet, så ændring af **Alt-tekst** til et produktbillede har ingen indflydelse på det gengivne billede.

### <a name="naming-conventions-for-omni-channel-images"></a>Navngivningskonventioner for omni-kanalbilleder 

Hvis du har konfigureret mediebiblioteket som back-end for omni-kanalbilledet, kan du bruge billedkategorier til at angive, hvilken kategori det uploadede billede tilhører. Der findes også en navngivningsregel, der skal følges for at sikre, at billeder hentes korrekt af andre kanaler, f.eks. POS (Point Of Sale).

Standardnavngivningskonventionen varierer, afhængigt af kategorien:
- Katalogbilleder skal navngives "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"
- Kategoribilleder skal navngives "**/Categories/\{CategoryName\}.png**"
- Kundebilleder skal navngives "**/Customers/\{CustomerNumber\}.jpg**"
- Medarbejderbilleder skal navngives "**/Workers/\{WorkerNumber\}.jpg**"
- Produktbilleder skal navngives "**/Produkter/\{Produktnummer\}\_000_001.png**"
    - 001 er rækkefølgen af billedet, og det kan være 001, 002, 003, 004 eller 005
- Produktvariantbilleder skal navngives "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"
    - For eksempel: 93039 \^ &nbsp;\^ 2 \^ Sort \^\_000_001.png
- Produktvariantbilleder med konfigurationsdimension skal navngives "**/Produkter/\{Produktnummer\} \^ \{Konfiguration\}\_000_001.png**"
    - For eksempel: 93039 \^ LB8017_000_001.png

> [!NOTE]
> Hvis dimensionsværdien er tom for produktvariantbilleder, skal der være to blanktegn mellem cirkumflekserne i filnavnet.

I eksemplerne ovenfor bruges standardkonfigurationen. Separatortegnet og dimensionerne kan konfigureres, og det nøjagtige navn, der skal bruges, kan variere mellem installationer. En metode til at identificere den nøjagtige navngivningskonvention er at bruge udviklerkonsollen i browseren til at kontrollere anmodninger om produktvariantbilleder, mens produktdimensionerne ændres på butikkens produktdetaljeside (PDP).

## <a name="upload-an-image"></a>Upload et billede

Følg disse trin for at uploade et billede i webstedsgenerator.

1. Vælg **Mediebibliotek** i navigationsruden til venstre.
1. Vælg **Upload \> Upload medieelementer** på kommandolinjen.
1. Naviger til og vælg en eller flere billedfiler, der skal uploades, i Stifinder, og vælg derefter **Åbn**.
1. Angiv den påkrævede titel og alternative tekst i dialogboksen **Overfør medieelement**.
1. Angiv en valgfri beskrivelse og nøgleord, og vælg evt. en evt. kategori. 
1. Hvis du vil udgive en eller flere billeder umiddelbart efter upload, skal du markere afkrydsningsfeltet **Publicer medieelementer efter upload** .
1. Vælg **OK**.

## <a name="upload-a-folder-of-images"></a>Uploade en mappe med billeder

Følg disse trin for at masseuploade en mappe med billeder i webstedsgenerator.

1. Vælg **Mediebibliotek** i navigationsruden til venstre.
1. Vælg **Upload \> Uploadmappe** på kommandolinjen.
1. Naviger til, og vælg en mappe, der skal uploades, i Stifinder, og vælg derefter **Åbn**.
1. Angiv valgfrie nøgleord, og vælg en kategori efter behov i dialogboksen **Upload medieelementer**. 
1. Hvis du vil udgive billederne i en mappe umiddelbart efter upload, skal du markere afkrydsningsfeltet **Publicer medieelementer efter upload** .
1. Vælg **OK**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over digital aktivstyring](dam-overview.md)

[Overføre video](dam-upload-video.md)

[Uploade filer](dam-upload-files.md)

[Beskære billeder](dam-crop-images.md)

[Tilpasse billedets fokuspunkter](dam-custom-focal-point.md)

[Overføre og håndtere statiske filer](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
