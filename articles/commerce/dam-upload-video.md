---
title: Uploade videoer
description: I dette emne beskrives, hvordan du overfører videoer i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: psimolin
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f481e5d3f323b0c86d637b67c119d13b956d5714dc0d990004834e2be05b370e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735624"
---
# <a name="upload-videos"></a>Uploade videoer

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du overfører videoer i Microsoft Dynamics 365 Commerce-webstedsgenerator.

Mediebiblioteket i Commerce-webstedsgenerator giver dig mulighed for at uploade videoer. Du bør altid uploade versionen af videoen med den højeste bithastighed og opløsning, da videoen automatisk vil blive konverteret til at være passende for forskellige billeder og deres pausepunkter.

### <a name="video-information-specified-during-upload"></a>Videooplysninger, der er angivet under upload

Når du uploader en video, kan du angive følgende oplysninger.

- **Titel, Beskrivelse, Nøgleord**: Videoens metadata.
- **Generér undertekster automatisk**: Angiver, om der automatisk skal genereres undertekster til videoen (kun engelsk understøttes). 
- **Undertekster**: Angiver, om undertekster skal bruges.
- **Almindeligt lydsignal**: Angiver det almindelige lydspor, der skal bruges.
- **Miniaturebillede**: Angiver miniaturebilledet for videoen. Hvis miniaturebilledet ikke angives, genereres det automatisk.
- **Beskrivende lyd**: Angiver det beskrivende lydspor, der skal bruges.

## <a name="upload-a-video"></a>Uploade en video

Følg disse trin for at uploade en video i webstedsgenerator.

1. Vælg **Mediebibliotek** i navigationsruden til venstre.
1. Vælg **Upload \> Upload medieelementer** på kommandolinjen.
1. Naviger til og vælg en eller flere videofiler, der skal uploades, i Stifinder, og vælg derefter **Åbn**.
1. Angiv den påkrævede titel og alternative tekst i dialogboksen **Overfør medieelement**.
1. Angiv en valgfri beskrivelse og nøgleord, og vælg evt. en evt. kategori. 
1. Hvis du vil udgive en eller flere billeder umiddelbart efter upload, skal du markere afkrydsningsfeltet **Publicer medieelementer efter upload**
1. Vælg **OK**.

Hvis du uploader flere typer aktiver på én gang (f.eks. billeder og videoer), kan du kun angive nøgleord i dialogboksen **Upload medieelement**, uanset om filerne skal udgives umiddelbart efter upload, og om der automatisk skal genereres undertekster til videofiler. Alle aktiverne vil dele de samme nøgleord.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over digital aktivstyring](dam-overview.md)

[Overføre billeder](dam-upload-images.md)

[Uploade filer](dam-upload-files.md)

[Beskære billeder](dam-crop-images.md)

[Tilpasse billedets fokuspunkter](dam-custom-focal-point.md)

[Overføre og håndtere statiske filer](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
