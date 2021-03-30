---
title: Funktioner og egenskaber til øget tilgængelighed
description: Dette emne indeholder oplysninger om funktionerne og egenskaberne til øget tilgængelighed i Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 094ad8d34e13051ce7596be462070ead4cbc4f14
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206649"
---
# <a name="accessibility-features-and-capabilities"></a>Tilgængelighedsfunktioner og -egenskaber


[!include [banner](includes/banner.md)]

Dette emne indeholder oplysninger om funktionerne og egenskaberne til øget tilgængelighed i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Funktioner og egenskaber til øget tilgængelighed giver alle brugere de funktionelle midler til at kunne tilgå og udføre handlinger, så de kan nå deres mål. Denne brede vifte af brugere kan få brug for hjælpemidler til hørelse, syn, mobilitet eller neurodiversitet.

De forskellige funktioner i Dynamics 365 Commerce gør det muligt for dig at bygge dit websted, så det omfatter hjælpefunktioner. Når du designer dit websted, bør du overveje de områder af tilgængelighedsfunktioner, der er omtalt i [Microsoft Accessibility Center](https://www.microsoft.com/accessibility). 

I dette emne beskrives endvidere nogle andre områder af tilgængelighedsfunktioner, som du bør tage i betragtning, når du bruger Dynamics 365 Commerce.

## <a name="image-alt-text"></a>Billede-alternativ tekst

Dynamics 365 Commerce har et indbygget digitalt system til styring af aktiver, som kan spore de billede- og videoaktiver, der bruges på dit websted. Billedtekster, -beskrivelser og -alternativ tekst kan tilføjes i egenskabsruden for et billede, når det vælges eller overføres.

## <a name="video-accessibility"></a>Videotilgængelighed

Dynamics 365 Commerce's digitale system til styring af aktiver understøtter flere tilgængelighedsfunktioner for videoindhold. Der gives nogle eksempler herpå i følgende tabel.

| Videofunktion               | Beskrivelse |
|-----------------------------|-------------|
| Undertekster for hørehæmmede (CC)      | Tekst, der kan vises for lydelementer og lydbeskrivende elementer i en video, for at hjælpe brugere, der er døve eller hørehæmmede |
| Undertitler                   | Undertekstfiler, der viser teksten til kontekstspor eller -dialog på skærmen |
| Lydtransskription           | En tekstmæssige transkription af talte ord, der genereres fra lyden af et videoaktiv |
| Beskrivende lyd           | En ikke-primær lydkanal, der beskriver det indhold eller den kontekst, der forekommer på skærmen |
| Port for minimumsalder            | En attribut, der kan gemme den minimumsalder, som en seer skal have for at få vist en video (kun metadata) |

### <a name="configure-video-accessibility-elements"></a>Konfiguration af tilgængelighedselementer til video

I Commerce-afsnittet **Mediebibliotek** for dit websted kan du overføre videoaktiver, der har separate filer til undertekster, almindelig lyd og beskrivende lyd. Undertekster kan også genereres automatisk, når et videoaktiv overføres.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Generer eller overfør filer med undertekster i forbindelse med overførslen af videoaktiver

Følg dette trin for at generere en undertekstfil automatisk, når du overfører en video.

- I dialogboksen **Aktivoverførsel** skal du vælge **Generer undertekster automatisk**. Hvis du genererer en fil med en undertekstfil, er filvælgeren for undertekstfiler ikke tilgængelig i dialogboksen.

Følg dette trin for manuelt at overføre en undertekstfil, når du overfører en video.

- I dialogboksen **Aktivoverførsel** skal du fravælge **Generer undertekster automatisk**.

Hvis du vil overføre almindelige lydfiler eller beskrivende lydfiler for videoen, skal du bruge filvælgeren i dialogboksen **Aktivoverførsel**.

> [!NOTE]
> Aktiver relateret til undertekster, almindelig lyd og beskrivende lyd kan også tilføjes efter, at et videoaktiv er blevet overført. Gå til **Mediebibliotek**, vælg videoaktivet, og vælg **Rediger**. Overfør derefter de andre aktiver i egenskabsruden for videoaktivet.

#### <a name="edit-cc-and-audio-transcript-files"></a>Redigering af CC- og audiotransskriptionsfiler

CC- og audiotransskriptionsfiler kan redigeres direkte i oprettelsesværktøjet. Videoafspilning er tilgængelig under redigering.

For at redigerer CC- og audiotransskriptionsfiler skal du følge disse trin.

1. Gå til **Mediebibliotek**, og vælg filnavnet på videoaktivet. Editoren til undertekster og transskriptionen vises.
1. Vælg **Rediger**.
1. Rediger underteksten eller transskriptionen.
1. Når du er færdig, skal du vælge **Gem** og derefter vælge **Afslut redigering**.
1. Når du er klar til at udgive, skal du vælge **Udgiv**.

#### <a name="set-the-minimum-age-attribute"></a>Angiv attributten minimumsalder

Der kan tilknyttes en metadata-attribut for **Minimumsalder** til videoaktiver.

Følg disse trin for at angive en attribut for **Minimumsalder** for et videoaktiv.

1. Gå til **Mediebibliotek**, og vælg videoaktivet.
1. Vælg **Rediger**.
1. Angiv attributten **Minimumsalder** i egenskabsruden for videoaktivet.

> [!NOTE]
> Egenskabsruden bruges kun til at angive og gemme metadataattributværdien. Der skal oprettes tilpassede moduler for at denne attribut kan bruges til afspilningsgating.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilgængelighed i formularer, produkter og kontrolelementer](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Microsoft Accessibility Center](https://www.microsoft.com/accessibility)

[Dynamics 365 Accessibility Center](https://docs.microsoft.com/dynamics365/get-started/accessibility/index)

[Oversigt over overholdelse](compliance-overview.md)

[Cookie-compliance](cookie-compliance.md)

[Tilføje en side med politik om beskyttelse af personlige oplysninger](add-privacy-page.md)

[Erstatte bruger-id'er, der er tilknyttet sporede indholdsændringer](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]