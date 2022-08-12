---
title: Oversigt over genopfyldning
description: Denne artikel beskriver de genopfyldningsstrategier, der er tilgængelige for lagersteder, der bruger den funktionalitet, der findes i Lagerstedsstyring.
author: Mirzaab
ms.date: 02/19/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSReplenishmentTemplates, WHSInventFixedLocation, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "90043"
- intro-internal
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 075e74845eb8e0363cdb706f1f3af0dc9cfddfaa
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069176"
---
# <a name="replenishment-overview"></a>Oversigt over genopfyldning

[!include [banner](../includes/banner.md)]

Denne artikel beskriver de genopfyldningsstrategier, der er tilgængelige for lagersteder, der bruger den funktionalitet, der findes i Lagerstedsstyring. Oplysningerne i denne artikel gælder ikke for lagerstedsløsninger, der findes i Lagerstyring.

Der findes følgende genopfyldningsstrategier:

- **Genopfyldning baseret på bølgebehov** – Denne strategi opretter genopfyldningsarbejde for udgående ordrer eller laster, hvis lageret ikke er tilgængeligt, når bølgen opretter arbejde. Genopfyldningsarbejde kan f.eks. oprettes, hvis det antal, der er nødvendigt for en salgsordre, ikke er tilgængeligt, når en bølge behandles.
- **Min./maks. genopfyldning** – Genopfyldning baseret på minimale og maksimale mængder – denne strategi bruger minimum og maksimum for grænser for lagring for at afgøre, hvornår lokationerne skal genopfyldes. Kriterierne for vare og lokalitet definerer det lager, der evalueres for genopfyldning. Min/Max er genopfyldningsskabeloner den primære mekanisme til opretholdelse af optimale niveauer i plukpladser. Du kan bruge genopfyldning af behov som supplement mellem Min/Maks genopfyldning cyklusser for at sikre, at der er tilstrækkelig direkte pluklagerbeholdning tilgængelig til at opfylde bølgebehovet.
- **Genopfyldning for lastbehov** – Denne strategi opsummerer behovet for flere laster og opretter det genopfyldningsarbejde, der er nødvendigt for lagerbeholdningen på de relevante plukpladser. Denne strategi hjælper med at sikre, at de laster, der oprettes, kan plukkes på lageret, når de er frigivet.
- **Øjeblikkelig genopfyldning** – Denne strategi genopfylder lageret, før der køres en bølge, hvis allokeringen mislykkes for en lokalitetsvejledningslinje, der har en genopfyldningsskabelon. 

Alle fire strategier opretter genopfyldningsarbejde baseret på en genopfyldningsskabelon.

## <a name="wave-demand-replenishment"></a>Genopfyldning baseret på bølgebehov
Genopfyldning baseret på bølgebehov opretter genopfyldningsarbejde baseret på behov, hvis den mængde, der kræves til produktionsordrer, kanbans, udgående ordrer eller laster, ikke er tilgængelig, når en bølge opretter arbejdet. Genopfyldningsskabelonen indeholder oplysninger om varekriterier, måleenhed, behovsforøgelse og lokation. 

Lokationsvejledninger bruges til at bestemme, hvilken lokation der skal genopfyldes. Du sammenkæder disse lokationsvejledninger med genopfyldningsskabelonen ved hjælp af feltet **Vejledningskode**. Hvis feltet **Vejledningskode** ikke er indstillet, bruges forespørgsler til at bestemme, hvilken lokationsvejledning der skal bruges. Bemærk, at hvis en vejledningskode ikke er angivet i genopfyldningsskabelonen, og lokationsvejledningen har en vejledningskode, bliver lokationsvejledningen ignoreret, selvom forespørgslen i lokationsvejledningen er korrekt. Pluklokationsvejledninger bruges til at bestemme, hvor du kan få lagervarer til genopfyldningen. 

Ud over at oprette en skabelon skal du angive nogle genopfyldningsindstillinger i bølgeskabelonen. Bølgeskabelonen skal indeholde et bølgetrin for genopfyldning, der kun køres, hvis en vare ikke er korrekt fordelt. Genopfyldningsbølgetrinnet bruger en bølgetrinskode til at bestemme, hvilken genopfyldningsskabelon der skal bruges. Ud over at have et bølgetrin for genopfyldning du skal kontrollere, at **Genopfyld** er valgt i sektionen **Metoder** i bølgeskabelonen. 

Siden **Genopfyldningsskabelon** indeholder afkrydsningsfeltet **Tillad bølgebehov at bruge ikke-reserverede antal**. Markér dette afkrydsningsfelt, hvis genopfyldningsbehov skal være i stand til at trække ikke-reserverede mængder fra arbejde, der er oprettet ud fra den valgte genopfyldningsskabelon. For at gøre det muligt for genopfyldningsskabeloner at bruge denne logik skal du markere dette afkrydsningsfelt for hver eksisterende genopfyldningsskabelon. Når der udløses genopfyldningsbehov på lagerstedet, trækkes behovet fra eksisterende genopfyldningsarbejde, der har ikkereserverede mængder, hvis arbejdet stammer fra genopfyldningsskabeloner, hvor afkrydsningsfeltet **Tillad bølgebehov at bruge ikke-reserverede antal** er markeret.

**Genopfyldningsenhed** er den mindste enhed, der skal genopfyldes. Det skal være et helt tal, der er et multiplum af enheden. Systemet vil runde op til den højest mulige enhed, når der oprettes arbejde.

Genopfyldning ved behov understøttes for salgsordrer, flytteordrer, produktionsordrer og kanbans. 

## <a name="minmax-replenishment"></a>Min./maks. genopfyldning
I Min/Maks genopfyldning genopfyldes lagerbeholdningen, så det ligger mellem den angivne minimum- og maksimumgrænse. Processen udføres typisk én gang hver dag for at sikre, at alle plukpladser er fyldt til det maksimale niveau, før plukningen starter. 

Minimum- og maksimummængderne indstilles i en genopfyldningsskabelon. Mange af de andre indstillinger i skabelonen minder om indstillingerne i skabeloner, der bruges i Genopfyldning baseret på bølgebehov. Skabelonen skal indeholde én linje for hver vare og lokation. Når du kører genopfyldning ved hjælp af batchjobbet, vurderer systemet, om der kræves genopfyldning ved hjælp af den rækkefølge, som linjerne er organiseret i. 

Bemærk, at Min./maks genopfyldningsstrategien ikke kan genopfylde en tom lokation, medmindre lokationen er angivet som fast lokation for varen. Hvis den lokation, der skal genopfyldes, ikke er en fast lokation, kan systemet ikke fastslå, hvilken vare der skal genopfyldes. En vis minimumbeholdning er derfor påkrævet, før der foretages genopfyldning.

## <a name="load-demand-replenishment"></a>Genopfyldning for lastbehov
Genopfyldning for lastbehov opsummerer behovet for flere laster og opretter det genopfyldningsarbejde, der er nødvendigt for lagerbeholdningen på de relevante plukpladser. Genopfyldning for lastbehov ligner på mange måder Genopfyldning baseret på bølgebehov. Den væsentligste forskel er, hvordan og hvornår Genopfyldning for lastbehov og Genopfyldning baseret på bølgebehov kører. Ligesom Min./maks. genopfyldning køres Genopfyldning for lastbehov ved hjælp af et batchjob. Når du vil konfigurere batchjobbet skal du på siden **Genopfyldning for lastbehov** vælge den genopfyldningsskabelonen, der skal bruges, og indstille en filterforespørgsel til at angive, hvilke laster der bruges til at bestemme behovet. Forespørgslen om lokation angiver de lokationer, som enhver tilgængelig mængde trækkes fra for at opfylde det samlede lastebehov.

## <a name="immediate-replenishment"></a>Øjeblikkelig genopfyldning
I stedet for at opsummere behov i slutningen af en fordelingsproces og foretage genopfyldning på basis af sammentalte antal, kan du anvende strategien øjeblikkelig genopfyldning. Når du bruger denne strategi, kan lageret genopfyldes, umiddelbart efter at en lokalitetsvejledningslinje mislykkes. Du kan derfor konfigurere genopfyldningen, så den er begrænset af bestemte enheder, og så den bruger antal, der er angivet for bestemte lokationer.

## <a name="replenishment-prerequisites"></a>Forudsætninger for genopfyldning

|      Forudsætning       |                                                                                                                                Beskrivelse                                                                                                                                 |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|          Vare           |                                                                                                        Varen skal være aktiveret for lokationsstyringsprocesser (WMS).                                                                                                        |
|        Lagersted        | Lagerstedet skal være aktiveret for lokationsstyringsprocesser (WMS). Hvis du vil aktivere et lagersted for WMS, skal du på siden <strong>Lagersteder</strong> vælge lagerstedet og derefter vælge indstillingen <strong>Brug lagerstedsstyringsprocesser</strong>. |
| Genopfyldningsskabeloner |                                                                   Mindst én genopfyldningsskabelon skal sættes op til Min/Maks genopfyldning, Genopfyldning baseret på bølgebehov eller Genopfyldning for lastbehov.                                                                   |
|        Lokationer        |                                                                                                       Lokationer skal oprettes og forbindes til en lokationsprofil.                                                                                                       |
|    Lokationsprofiler    |                                                                                                        Lokationsprofiler er nødvendige for at oprette lokationer.                                                                                                        |
|   Lokationsvejledninger   |                                                       Lokationsvejledninger er nødvendige for at lede arbejdet til de lokationer, hvor genopfyldning er nødvendig, og til de lokationer, som lageret leveres fra.                                                        |
|     Arbejdsskabeloner      |                                                   Arbejdsskabeloner af typen <strong>Genopfyldning</strong> kræves for at oprette genopfyldningsarbejde, så lageret kan flyttes til de ønskede lokationer.                                                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]