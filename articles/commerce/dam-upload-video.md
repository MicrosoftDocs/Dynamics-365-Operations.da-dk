---
title: Uploade videoer
description: I dette emne beskrives, hvordan du overfører videoer i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: d74e7116d68074bfc917784a8f51f85d5682c5d6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213836"
---
# <a name="upload-videos"></a>Uploade videoer

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du overfører videoer i Microsoft Dynamics 365 Commerce-webstedsgenerator.

## <a name="overview"></a>Overblik

Mediebiblioteket i Commerce-webstedsgenerator giver dig mulighed for at uploade videoer. Du bør altid uploade versionen af videoen med den højeste bithastighed og opløsning, da videoen automatisk vil blive konverteret til at være passende for forskellige billeder og deres pausepunkter.

### <a name="video-information-specified-during-upload"></a>Videooplysninger, der er angivet under upload

Når du uploader en video, kan du angive følgende oplysninger.

- **Titel, Beskrivelse, Nøgleord**: Videoens metadata.
- **Generer undertekster automatisk**: Angiver, om der automatisk skal genereres undertekster til videoen.
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