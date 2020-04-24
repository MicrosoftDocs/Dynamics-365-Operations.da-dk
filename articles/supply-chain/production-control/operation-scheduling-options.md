---
title: Indstillinger for grovplanlægning
description: I dette emne beskrives indstillingerne for grovplanlægning. Du kan bruge grovplanlægning til at få et generelt estimat af produktionsprocessens over tid.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3865bfc3b66c018f836e21bbddf658de0351e57
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211370"
---
# <a name="operations-scheduling-options"></a>Indstillinger for grovplanlægning

[!include [banner](../includes/banner.md)]

I dette emne beskrives indstillingerne for grovplanlægning. Du kan bruge grovplanlægning til at få et generelt estimat af produktionsprocessens over tid.

Grovplanlægning beregner følgende oplysninger for en produktionsordre:

-   Start- og slutdatoer angives for produktionsordren og hver operation.
-   Ressourcer tildeles operationer.

En række indstillinger bestemmer, hvordan produktionsplaner beregnes. Du kan definere disse indstillinger på siden **Grovplanlægning** side. Indstillingerne for planlægningen beskrives i det følgende.

## <a name="operations-scheduling"></a>Grovplanlægning
### <a name="scheduling-direction"></a>Planlægningsvej

Planlægningsvejen er grundlæggende for planlægningsprocessen. Produktionen kan planlægges fremad eller bagud fra en vilkårlig dato, afhængigt af tids- og planlægningsbehov.

-   **Forudplanlægning**– Du kan planlægge, at produktionen skal starte så tidligt som muligt. Den kan startes i dag, i morgen eller fra en given dato i fremtiden. Produktionsstarten planlægges til den først mulige dato og planlægges fremad i tid til den først mulige slutdato.
-   **Bagudplanlægning** – Du kan planlægge, at produktionen skal starte så sent som muligt. Tidsplanen er baseret på den dato, hvor produktionen skal være fuldført, og tæller baglæns til den senest mulige dato, som produktionen kan startes, uden at den ønskede deadline overskrides.

Følgende valgmuligheder er tilgængelige:

-   **Fremad fra i dag** – Planlæg fremad fra dags dato. (Dags dato er lig med systemdatoen).
-   **Fremad fra planlagt start** – Planlæg fremad fra en tidligere startdato. Hvis der ikke eksisterer nogen tidligere planlægning, er planlægningsvejen fremad fra dags dato.
-   **Fremad fra planlægningsdato** – Planlæg fremad fra den dato, der er angivet i feltet **Planlægningsdato**. Hvis du ikke angiver en planlægningsdato, planlægges der fremad fra dags dato.
-   **Bagud fra leveringsdato** – Planlæg bagud fra den leveringsdato, der er angivet i produktionsordren. Hvis du valgte denne mulighed, og der ikke er angivet nogen leveringsdato, er leveringsdatoen dags dato.
-   **Bagud fra planlagt slut** – Planlæg bagud fra en tidligere beregnet slutdato. Hvis der ikke eksisterer nogen tidligere planlægning, er slutdatoen dags dato.
-   **Bagud fra planlægningsdato** – Planlæg bagud fra den dato, der er angivet i feltet **Planlægningsdato**. Hvis du ikke angiver en planlægningsdato, bruges dags dato. Planlægningsdatoen bagud blev beregnet for produktionsordren, sidste gang der blev beregnet et behov. Hvis der ikke er angivet en dato for produktionsordren, bruges dags dato i systemet.
-   **Bagud fra terminsdato** – Planlæg bagud fra den terminsdato, der blev beregnet for produktionsordren sidste gang, der blev beregnet et behov. Hvis der ikke er angivet nogen terminsdato for produktionsordren, bruges dags dato i systemet.
-   **Som ved sidste planlægning** – Den valgte planlægningsvej og -dato gemmes i forbindelse med grov- og finplanlægningen. Derfor kan du vælge denne mulighed for efterfølgende planlægninger. Hvis der ikke tidligere er foretaget planlægning af produktionsordren, sker planlægningen bagud fra dags dato (systemdatoen).
-   **Fremad fra i morgen** – Planlæg fremad fra dags dato plus én dag.
-   **Fremad fra forrige job** – Denne funktion er kun relevant i finplanlægning. Hvis du vælger denne planlægningsvej i forbindelse med grovplanlægning, planlægges produktionsordren fremad fra dags dato. Ved finplanlægning angives planlægningen for ét job, og alle de øvrige job for produktionen planlægges ud fra dette job.
-   **Bagud fra forrige job** – Denne funktion er kun relevant i finplanlægning. Hvis du vælger denne planlægningsvej i forbindelse med grovplanlægning, planlægges ordreforslagene bagud fra dags dato. Ved finplanlægning angives planlægningen for ét job, og alle de øvrige job for produktionen planlægges ud fra dette job.

### <a name="scheduling-date"></a>Planlægningsdato

Denne dato anvendes til planlægningsvejene **Fremad fra planlægningsdato** og **Bagud fra planlægningsdato**. Planlægningen foretages derefter bagud eller fremad fra denne dato. Du kan finde flere oplysninger i ovenstående afsnit "Planlægningsvej".

### <a name="recalculate-bom-levels"></a>Genberegn styklisteniveauer

Når du vælger **Genberegn styklisteniveauer**, genberegnes de valgte styklisteniveauer for at sikre den korrekte rækkefølge i planlægningen.

## <a name="limitations"></a>Begrænsninger
### <a name="finite-capacity"></a>Kapacitetsbegrænsning

Planlægningen afhænger af tilgængeligheden af de ressourcer, der kræves for at gennemføre produktionen. Hvis der ikke er tilstrækkelig kapacitet, kan produktionsordrer forsinkes eller endda stoppes. Hvis kapacitetsbegrænsning anvendes i grovplanlægning, tages der højde for eksisterende reservationer af kapacitetsressourcer, så de regnes for at være utilgængelige. Produktionsordren planlægges ud fra tilgængeligheden af kapacitet på de nødvendige ressourcer. Grovplanlægningen bruger den angivne sekvens af operationer til at bestemme rækkefølgen af operationer i produktionsruten. Grovplanlægningen reserverer kapacitet på ressourcegrupperne på basis af de operationstider, der er defineret for produktionsruten. Ressourcegruppernes kapacitet er summen af tilgængelig kapacitet på alle ressourcerne i ressourcegrupperne.

### <a name="finite-material"></a>Materialebegrænsning

Planlægningen afhænger også af tilgængeligheden af de materialer, der kræves til produktionen. Utilstrækkelig tilgængelighed af komponenter kan også medføre forsinkelser i produktionen. Planlægning kan også baseres på brugen af materialer. Angiv de materialer, der skal være tilgængelige for produktion, i forhold for de materialer, der ikke er vigtige. Denne type planlægning kaldes planlægning med materialebegrænsning. Når du angiver materialebegrænsning, planlægges produktionen ud fra, om materialerne er tilgængelige eller ej. **Bemærk:** Når du optimerer både kapacitet og materialer, beregnes produktionen til at opfylde begge begrænsninger. Der tages højde for tilgængeligheden af kapacitet og materialer, og produktionsordrens operationer kan ikke planlægges til start, før kapacitet og materialer er tilgængelige samtidig i de påkrævede mængder. Marker dette afkrydsningsfelt, hvis materialerne skal anses som værende begrænsede under planlægningen. Hvis materialerne er begrænsede, tages der højde for materialedisponeringen på det pågældende tidspunkt. Varens beregnede terminsdatoer tages med andre ord med i betragtning ved planlægningen. Under planlægningen reserveres råmaterialerne, og der foretages udfoldning for den aktuelle produktion. Hvis planlægningen foretages flere gange, foretages udfoldningen og reservationerne kun i den første planlægning. Hvis der ændres i produktionsstyklisten eller -ruten, foretages der en udfoldning ved næste planlægning. Udfoldningen sker efter den antagelse, at materialerne kræves samme dag. Da produktionen ikke er planlagt på det tidspunkt, hvor der foretages behovsplanlægning, anvendes dags dato som bedste bud på, hvornår varerne bliver disponible. Ved udfoldningen kontrolleres det, om varerne er tilgængelige. Hvis varerne er tilgængelige, kan produktionsbehovet opfyldes. Hvis varerne ikke er tilgængelige pr. dags dato, genereres der et ordreforslag, og der foretages et udligningsvalg for ordreforslaget. Hvis der er valgt automatisk autorisering af ordreforslaget, autoriseres det automatisk til indkøb eller produktion. Produktionen skifter automatisk status til den status, der er angivet i feltet **Ønsket produktionsstatus** i dialogboksen **Disponeringsgrupper**. Hvis markeringen i afkrydsningsfeltet fjernes, betragtes materialerne altid som tilgængelige. Derfor tages det ikke med i planlægningsovervejelserne, om materialerne er tilgængelige på det tidspunkt, der er behov for dem.

### <a name="finite-property"></a>Egenskabsbegrænsning

Markér dette afkrydsningsfelt for at lade finplanlægningen medtage eventuelle egenskabskrav.

### <a name="keep-production-unit"></a>Bevar produktionsenhed

Markér, om planlægningsprogrammet kun skal planlægge ressourcer, der allerede er angivet på produktionsenheden.

### <a name="keep-warehouse-from-resource"></a>Behold lagersted fra ressource

Markér, om planlægningsprogrammet kun skal planlægge ressourcer, der er knyttet til det interne lagersted, der er angivet på ressourcen.

## <a name="references"></a>Referencer
### <a name="schedule-references"></a>Planlæg referencer

Når referencer afhænger af produktionsordrer, er de også kendt som underproduktioner. Underproduktioner kan planlægges som en del af planlægningen af en produktionsordre. Markér dette afkrydsningsfelt, hvis planlægningen af underproduktioner skal baseres på planlægningen af hovedproduktionen. I forhold til hovedproduktionen planlægges de overliggende produktioner fremad, og de underliggende produktioner planlægges bagud. Du kan se produktionsordrereferencer i feltet **Referenceniveau** på siden **Produktionsordrer**.

### <a name="synchronize-references"></a>Synkroniser referencer

Du kan synkronisere referencer med produktionsordren. Hvis denne indstilling vælges, flyttes og justeres datoerne for underproduktionerne, når der foretages ændringer i produktionsordrens tidsplan. Hvis en produktionsordre har en eller flere underproduktioner, kan du vælge at planlægge underproduktionerne sammen med hovedproduktionen. I så fald kan hovedproduktionen ikke startes, før de relaterede underproduktioner er fuldført. Markér derfor dette afkrydsningsfelt, hvis planlægningen af underproduktioner skal baseres på start- og sluttidspunkter for den valgte produktion. Du kan kun markere dette afkrydsningsfelt, hvis afkrydsningsfeltet **Planlæg referencer** også er markeret.

## <a name="cancellation"></a>Annullering
### <a name="cancel-queue-time"></a>Annuller køtid

Markér dette afkrydsningsfelt, hvis du vil udelade køtid i planlægningen.

### <a name="cancel-setup"></a>Annuller opstilling

Markér dette afkrydsningsfelt, hvis du vil udelade opstillingstid i planlægningen.

### <a name="cancel-process"></a>Annuller proces

Markér dette afkrydsningsfelt for at udelukke procestid i planlægningen.

### <a name="cancel-overlap"></a>Annuller overlapning

Markér dette afkrydsningsfelt for at udelade overlapningstid i planlægningen.

### <a name="cancel-transport"></a>Annuller transport

Markér dette afkrydsningsfelt, hvis du vil udelade transittid i planlægningen.

## <a name="set-default"></a>Angiv standard
Du kan gemme de aktuelle værdier som standardværdier. Der er to valgmuligheder:

-   Angiv som min standard
-   Angiv som standard for alle


<a name="additional-resources"></a>Yderligere ressourcer
--------

[Grovplanlægning](operations-scheduling.md)



