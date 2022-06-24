---
title: Bølgefordeling
description: Denne artikel indeholder en beskrivelse af, hvordan du kan konfigurere trinnet til bølgefordeling, herunder hvordan du kan aktivere parallel behandling af den.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c6b89364afd57b9c4b4413d0319b86e725433594
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906945"
---
# <a name="wave-allocation"></a>Bølgefordeling

[!include [banner](../includes/banner.md)]

Bølgebehandling kan være tidskrævende, og den meste af behandlingstiden bruges på fordelingstrinnet og i trin til oprettelse af arbejde.

Nu er det muligt at køre hvert af disse trin parallelt, hvilket kan forbedre ydeevnen af bølgebehandling og give mulighed for større gennemløb af bølger på samme lagersted. Denne artikel forklarer, hvordan du kan konfigurere metode til tildeling af bølger, så den kører parallelt. Du kan finde flere oplysninger om, hvordan du konfigurerer arbejdsoprettelse til at køre parallelt, under [Planlægge oprettelse af arbejde under bølgen](configure-wave-schedule-work-creation.md).

Tidligere var det kun muligt at tildele én bølge ad gangen på et lagersted. Denne begrænsning er blevet fjernet og erstattet af en ny begrænsning, der kun låser den vare og de dimensioner, der ligger over lokationen i reservationshierarkiet. Dimensioner over lokationen omfatter altid produktdimensioner. Hvis en vare f.eks. er konfigureret med *Farve*, kan varianterne *Rød*, *Blå* og *Gul* hver behandles parallelt.

Dette betyder, at hvis den samme vare med samme dimensioner over lokationen tildeles af én bølge, vil andre bølger blive nødt til at vente med at få en lås på samme vare og dimensioner. Hvis låsen ikke kan anskaffes i rette tid, opstår der en fejl, og behandling af bølgen mislykkes.

Hvis du vil bruge parallel behandling, skal der køres en bølge i batch.

## <a name="performance-improvements"></a>Forbedringer af ydeevne

Ydeevnefordelene ved parallel behandling falder i to kategorier:

- **Forbedret gennemløb** – Gennemløbet af bølger forbedres typisk, selvom parallel behandling ikke er konfigureret, især for scenarier, hvor der ikke er overlapning af varer i bølgen.
- **Forbedring af fordelingen af en enkelt bølge** – Test af kundedata har vist en næsten 50 % ydeevneforbedring efter skift til parallel fordeling. Den parallelle behandling udføres for de varer og dimensioner, der ligger over lokationen, og derfor afhænger forbedringerne af, hvor mange forskellige varer en bølge indeholder, den tilgængelige infrastruktur og varigheden af fordelingen i forhold til varigheden af oprettelsen af arbejdet.

## <a name="configure-parallel-allocation"></a>Konfigurere parallel fordeling

### <a name="warehouse-management-parameters"></a>Parametre til lokationsstyring

Hvis du vil bruge parallel fordelingsbehandling, skal du gå til **Lokationsstyring > Opsætning > Parametre for lokationsstyring**, åbne fanen **Bølgebehandling** og angive følgende indstillinger:

- **Batchgruppe til behandling af bølger** – Vælg den batchgruppe, som den første behandling af bølgerne skal bruge. Den efterfølgende behandling af fordelingen kan ske ved hjælp af forskellige batchgrupper.
- **Udfør behandling af bølger i batch** – Angiv dette til *Ja*, så der bruges parallel behandling.
- **Vent på lås (ms)** – Angiv tid i millisekunder, som et fordelingstrin venter på en systemressource, der er låst af et andet fordelingstrin. Når denne tid overskrides, behandles bølgen ikke, og der vises en fejlmeddelelse. Det anbefales, at du tillader mindst et par sekunder, før fordelingen af én logisk enhed slutter.

Du kan finde oplysninger om disse og andre indstillinger for behandling af bølger på siden **Parametre for lokationsstyring** under [Lagerstedsparametre til bølgebehandling](wave-warehouse-parameters.md).

## <a name="wave-process-methods"></a>Metoder til bølgeproces

Sådan konfigurerer du parallel behandling:

1. Gå til **Lokationsstyring > Konfiguration > Bølger > Bølgeprocesmetoder**.
1. Vælg metoden `allocateWave` i gitteret.
1. Vælg **Opgavekonfiguration** i handlingsruden.
1. Siden **Konfiguration af opgave til bølgebogføringsmetode** åbnes. Dette gitter viser de enkelte lagersteder, hvor du har konfigureret `allocateWave`-metoden. Parallel behandling bruges kun til lagerstederne på listen. Brug knapperne i handlingsruden til at tilføje eller fjerne lagersteder fra gitteret efter behov. 
1. For hvert lagersted skal du foretage følgende indstillinger:
    - **Maksimalt antal batchopgaver** – Angiv det antal batchopgaver, der skal bruges til fordelingen for det valgte lagersted. Det optimale antal batchopgaver afhænger af den tilgængelige infrastruktur, og hvilke andre batchjob der behandles på serveren. Test udført på et firekernemiljø, der var dedikeret til behandling af bølger, har vist, at brug af otte opgaver giver gode resultater.
    - **Batchgruppe til bølgebehandling** – Bestemte batchgrupper kan bruges til forskellige lagersteder for at tillade, at fordelingsbehandlingen skaleres ud pr. lagersted.

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a>Aktivere eller deaktivere parallelisering på tværs af alle juridiske enheder

Det anbefales, at du angiver metoden `allocateWave` til at køre parallelt på tværs af alle juridiske enheder, da det er med til at forbedre ydeevnen af bølgebehandling. Fra og med Supply Chain Management version 10.0.17 aktiveres funktionen *Bølgeparallelisering af Tildel bølge-metode* som standard for alle nye og opdaterede installationer, og den kan ikke deaktiveres igen. Når du har aktiveret denne funktion, sker følgende:

- Metoden `allocateWave` opdateres, så den indeholder en indstilling for opgavekonfiguration, som giver dig mulighed for at bruge siden **Bølgeprocesmetoder** til at definere antallet af opgaver, der skal køres samtidigt, hvilket svarer til antallet af parallelle processer. Som følge heraf reduceres den tid, der bruges på trinnet Tildel bølge (som typisk er 30 % til 60 % af den samlede behandlingstid) med en faktor, der stort set svarer til antallet af opgaver. Det er også muligt at vælge, hvilket batch der skal tildeles for at behandle disse opgaver. Det er vigtigt at bemærke, at alle de juridiske enheder konfigureres til at behandle bølger i batch. For de lagersteder, der allerede er konfigureret til at behandle bølger i batch, og for de lagersteder, der allerede er konfigureret til at bruge metoden `allocateWave` parallelt, bevares den eksisterende konfiguration.
- Som standard er alle de nye juridiske enheder konfigureret til at behandle bølger i batch. Alle nye lagersteder, hvor indstillingen **Lokationsstyringsprocesser** er aktiveret, vil have metoden `allocateWave` konfigureret til at køre parallelt som standard.
- På siden **Parametre for lokationsstyring** angives **Udfør behandling af bølger i batch** til *Ja* og **Vent på lås (ms)** er angivet til standarden 15 sekunder. Det betyder, at alle bølger udføres i batch. Når en bølge kører, får den en lås på varen og dimensionerne over lokationen under fordelingstrinnet. Når en anden bølgebehandlingsopgave forsøger at få den samme lås for den samme post, blokeres den, indtil den aktuelle proces er færdig. Indstillingerne **Vent på lås (ms)** fastsætter den maksimale tid, systemet vil vente, før låsen frigives.

Parallel fordelingsbehandling kræver, at der køres bølgebehandling i batch. Du vil derfor reducere den ydeevne, du bruger til behandling af bølger, hvis du deaktiverer indstillingen **Udfør behandling af bølger i batch**, specielt hvis behandling af bølger bruger en parallel proces som defineret af opgavekonfigurationen for de relevante bølgemetoder.

Hvis det er nødvendigt, kan du fortryde hver af de indstillinger, der er foretaget som standard, når funktionen *Bølgeparallelisering af Tilde bølge-metode* automatisk aktiveres for din forekomst. Sådan gør du dette:

- Gå til **Warehouse Management \> Opsætning \> Parametre til lagerstedsstyring**. Anvend dine foretrukne værdier for **Udfør behandling af bølger i batch** og **Vent på lås (ms)** under fanen **Bølgebehandling**.
- Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**. Vælg metoden `allocateWave`. Vælg **Opgavekonfiguration** i handlingsruden for at åbne en side med en oversigt over hvert lagersted, hvor metoden er indstillet til at køre parallelt. Rediger eller slet antallet af batchopgaver og den tildelte bølgegruppe for hvert af de viste lagersteder efter behov.

## <a name="troubleshooting"></a>Fejlfinding

### <a name="troubleshoot-using-the-infolog"></a>Foretage fejlfinding af infologgen

Da batchstrukturen bruges, registreres fejl, der opstår under behandling af bølger, som en del af infologgen til batchjobbene. Sådan aflæser du de batchjob, der er relateret til en bølge:

1. Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Vælg den bølge, der skal inspiceres.
1. Åbn fanen **Bølge** i handlingsruden, og vælg **Batchjob** i gruppen **Bølge**.

Bølgebehandling er selvkorrigerende, så alle fejl, der registreres under behandlingen, skulle blive rapporteret i infologgen.

En typisk fejl, der er relateret til parallel behandling, kan være, at to bølger forsøger at tildele den samme vare samtidig, og at den ene ikke fuldføres, så den anden bølge ikke kan få en lås inden for den angivne tid. Hvis denne situation opstår, indeholder batchjobloggen oplysninger om, at låsen for varen ikke kunne anskaffes. I så fald skal den bølge, der mislykkedes, behandles igen.

Da behandlingen sker parallelt, skal data vedligeholdes i forskellige tabeller for at spore behandlingstilstanden. Det betyder, at logfilerne for batchjobbene kan indeholde fejl, f.eks. fejl med om identiske nøgler.

Fejlene fra batchopgaverne er også en del af batchjobloggen. De vigtigste oplysninger vises typisk i bunden.

I sjældne tilfælde, hvis SQL-forbindelsen f.eks. afbrydes, kan bølgebehandlingen afsluttes i en uoverensstemmende tilstand, hvor batchjobbet ser ud til at køre, men behandlingen stoppes. Bølgen kan ikke håndtere fejl som denne, så der udføres et forsøg på at rydde op i mislykkede bølger, når næste bølge køres. Hvis den aktuelle bølge har uoverensstemmende tilstand, kan du også udføre følgende trin:

1. Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Vælg den bølge, der skal ryddes op i.
1. Åbn fanen **Bølge** i handlingsruden, og vælg **Oprydning af bølgedata** i gruppen **Bølge**.

### <a name="troubleshoot-using-the-wave-progress-log"></a>Foretage fejlfinding ved hjælp af log over bølgestatus

Hvis indstillingen **Opret log over bølgestatus** er aktiveret på siden **Parametre for lokationsstyring**, oprettes der en logpost, hver gang fordelingen for en vare og dens dimensioner starter og slutter. Du skal kun aktivere denne log, når du har brug for den, f.eks. under den indledende test eller ved fejlfinding. Når denne indstilling er aktiveret, kan du få vist loggen ved at følge nedenstående trin:

1. Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Vælg den bølge, der skal inspiceres.
1. I handlingsruden under fanen **Bølge** i gruppen **Bølge** skal du vælge **Status**.
