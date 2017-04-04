---
title: Opfyldning
description: "I denne artikel beskrives de genopfyldningsstrategier, der er tilgængelige for lagersteder, der bruger den funktionalitet, der findes i Lagerstedsstyring"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSReplenishmentTemplates
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 77b895e7f7edd6f22ee960ba2ec4bdd2931c29f8
ms.lasthandoff: 03/31/2017


---

# <a name="replenishment"></a>Opfyldning

I denne artikel beskrives de genopfyldningsstrategier, der er tilgængelige for lagersteder, der bruger den funktionalitet, der findes i Lagerstedsstyring

I denne artikel beskrives de genopfyldningsstrategier, der er tilgængelige for lagersteder, der bruger den funktionalitet, der findes i Lagerstedsstyring Oplysningerne gælder ikke for lagerstedsløsninger, der findes i Lagerstyring. Der findes tre genopfyldningsstrategier:

-   **Genopfyldning baseret på bølgebehov** – Denne strategi opretter genopfyldningsarbejde for udgående ordrer eller laster, hvis lageret ikke er tilgængeligt, når bølgen opretter arbejde. Genopfyldningsarbejde kan f.eks. oprettes, hvis det antal, der er nødvendigt for en salgsordre, ikke er tilgængeligt, når en bølge behandles.
-   **Min./maks. genopfyldning** – Genopfyldning baseret på minimale og maksimale mængder – denne strategi bruger minimum og maksimum for grænser for lagring for at afgøre, hvornår lokationerne skal genopfyldes. Kriterierne for vare og lokalitet definerer det lager, der evalueres for genopfyldning. Min/Max er genopfyldningsskabeloner den primære mekanisme til opretholdelse af optimale niveauer i plukpladser. Du kan bruge genopfyldning af behov som supplement mellem Min/Maks genopfyldning cyklusser for at sikre, at der er tilstrækkelig direkte pluklagerbeholdning tilgængelig til at opfylde bølgebehovet.
-   **Genopfyldning for lastbehov** – Denne strategi opsummerer behovet for flere laster og opretter det genopfyldningsarbejde, der er nødvendigt for lagerbeholdningen på de relevante plukpladser. Denne strategi hjælper med at sikre, at de laster, der oprettes, kan plukkes på lageret, når de er frigivet.

Alle tre strategier opretter genopfyldningsarbejde baseret på en genopfyldningsskabelon.

## <a name="wave-demand-replenishment"></a>Genopfyldning baseret på bølgebehov
Genopfyldning baseret på bølgebehov opretter genopfyldningsarbejde baseret på behov, hvis den mængde, der kræves til udgående ordrer eller laster, ikke er tilgængelig, når en bølge opretter arbejdet. Genopfyldningsskabelonen indeholder oplysninger om varekriterier, måleenhed, behovsforøgelse og lokation. 

Lokationsvejledninger bruges til at bestemme, hvilken lokation der skal genopfyldes. Du sammenkæder disse lokationsvejledninger med genopfyldningsskabelonen ved hjælp af feltet **Vejledningskode**. Hvis feltet **Vejledningskode** ikke er indstillet, bruges forespørgsler til at bestemme, hvilken lokationsvejledning der skal bruges. Bemærk, at hvis en vejledningskode ikke er angivet i genopfyldningsskabelonen, og lokationsvejledningen har en vejledningskode, bliver lokationsvejledningen ignoreret, selvom forespørgslen i lokationsvejledningen er korrekt. Pluklokationsvejledninger bruges til at bestemme, hvor du kan få lagervarer til genopfyldningen. 

Ud over at oprette en skabelon skal du angive nogle genopfyldningsindstillinger i bølgeskabelonen. Bølgeskabelonen skal indeholde et bølgetrin for genopfyldning, der kun køres, hvis fordelingen af en vare mislykkes. Genopfyldningsbølgetrinnet bruger en bølgetrinskode til at bestemme, hvilken genopfyldningsskabelon der skal bruges. Ud over at have et bølgetrin for genopfyldning du skal kontrollere, at **genbestille** er valgt i sektionen **Metoder** i bølgeskabelonen. 

Siden **Genopfyldningsskabelon** indeholder afkrydsningsfeltet **Tillad bølgebehov at bruge ikke-reserverede antal**. Du skal markere dette afkrydsningsfelt, hvis du vil tillade, at genopfyldningsbehov kan trække ikkereserverede mængder fra arbejde, der er oprettet ud fra den valgte genopfyldningsskabelon. For at gøre det muligt for genopfyldningsskabeloner at bruge denne logik skal du markere dette afkrydsningsfelt for hver eksisterende genopfyldningsskabelon. Når der udløses genopfyldningsbehov på lagerstedet, trækkes behovet fra eksisterende genopfyldningsarbejde, der har ikkereserverede mængder, hvis arbejdet stammer fra genopfyldningsskabeloner, hvor afkrydsningsfeltet **Tillad bølgebehov at bruge ikke-reserverede antal** er markeret.

## <a name="minmax-replenishment"></a>Min./maks. genopfyldning
I Min/Maks genopfyldning genopfyldes lagerbeholdningen, så det ligger mellem den angivne minimum- og maksimumgrænse. Processen udføres typisk én gang hver dag for at sikre, at alle plukpladser er fyldt til det maksimale niveau, før plukningen starter. 

Minimum- og maksimummængderne indstilles i en genopfyldningsskabelon. Mange af de andre indstillinger i skabelonen minder om indstillingerne i skabeloner, der bruges i Genopfyldning baseret på bølgebehov. Skabelonen skal indeholde én linje for hver vare og lokation. Når du kører genopfyldning ved hjælp af batchjobbet, vurderer Microsoft Dynamics 365 for Operations, om der kræves genopfyldning i den rækkefølge, som linjerne er organiseret i. 

Bemærk, at Min./maks genopfyldningsstrategien ikke kan genopfylde en tom lokation, medmindre lokationen er angivet som fast lokation for varen. Hvis den lokation, der skal genopfyldes, ikke er en fast lokation, kan Dynamics 365 for Operations ikke fastslå, hvilken vare der skal genopfyldes. En vis minimumbeholdning er derfor påkrævet, før der foretages genopfyldning.

## <a name="load-demand-replenishment"></a>Genopfyldning for lastbehov
Genopfyldning for lastbehov opsummerer behovet for flere laster og opretter det genopfyldningsarbejde, der er nødvendigt for lagerbeholdningen på de relevante plukpladser. Genopfyldning for lastbehov ligner på mange måder Genopfyldning baseret på bølgebehov. Den væsentligste forskel er, hvordan og hvornår Genopfyldning for lastbehov og Genopfyldning baseret på bølgebehov kører. Ligesom Min./maks. genopfyldning køres Genopfyldning for lastbehov ved hjælp af et batchjob. Når du vil konfigurere batchjobbet skal du på siden **Genopfyldning for lastbehov** vælge den genopfyldningsskabelonen, der skal bruges, og indstille en filterforespørgsel til at angive, hvilke laster der bruges til at bestemme behovet. Forespørgslen om lokation angiver de lokationer, som enhver tilgængelig mængde trækkes fra for at opfylde det samlede lastebehov.

## <a name="replenishment-prerequisites"></a>Forudsætninger for genopfyldning
| Forudsætning            | Beskrivelse                                                                                                                                                                                                                                        |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vare                    | Varen skal være aktiveret for lagerprocesser for lagersted.                                                                                                                                                                                       |
| Lagersted               | Lagerstedet skal være aktiveret for lagerprocesser for lagersted. Hvis du vil aktivere lagerstedet for lagerstedsstyringsprocesser, skal du på siden **Lagersteder** vælge lagerstedet og derefter vælge indstillingen **Brug lagerstedsstyringsprocesser**. |
| Genopfyldningsskabeloner | Mindst én genopfyldningsskabelon skal sættes op til Min/Maks genopfyldning, Genopfyldning baseret på bølgebehov eller Genopfyldning for lastbehov.                                                                                                             |
| Lokationer               | Lokationer skal oprettes og forbindes til en lokationsprofil.                                                                                                                                                                                     |
| Lokationsprofiler       | Lokationsprofiler er nødvendige for at oprette lokationer.                                                                                                                                                                                       |
| Lokationsvejledninger     | Lokationsvejledninger er nødvendige for at lede arbejdet til de lokationer, hvor genopfyldning er nødvendig, og til de lokationer, som lageret leveres fra.                                                                                     |
| Arbejdsskabeloner          | Arbejdsskabeloner af typen **Genopfyldning** kræves for at oprette genopfyldningsarbejde, så lageret kan flyttes til de ønskede lokationer.                                                                                           |




