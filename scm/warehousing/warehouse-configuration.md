---
title: Konfiguration af lagersted
description: I denne artikel beskrives det, hvordan du konfigurerer et lagersted. Det indeholder oplysninger om, hvordan du aktiverer en lageropbygning og lagerprocesser.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-10-30 12 - 52 - 43
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11554
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 437f2348603db432df6d7589e4043d8145c52a1e
ms.lasthandoff: 03/30/2017


---

# <a name="warehouse-configuration"></a>Konfiguration af lagersted

I denne artikel beskrives det, hvordan du konfigurerer et lagersted. Det indeholder oplysninger om, hvordan du aktiverer en lageropbygning og lagerprocesser.

**Bemærk!** Denne artikel gælder for funktioner i modulet** Lagerstedsstyring** (avanceret logistik). Det gælder ikke for lagerstedsfunktioner i modulet** Lagerstyring**.

## <a name="warehouse-layout"></a>Lageropbygning
Lokationsstyringssystemet i Microsoft Dynamics 365 for Operations giver dig fleksible muligheder for at definere din lageropbygnings skiftende behov, så du kan opnå en optimal lagereffektivitet.

-   Du kan oprette opbevaringssteder med høj prioritet og lav prioritet til optimal placering af varer.
-   Du kan opdele lageret i områder, der passer til forskellige opbevaringsbehov, som temperaturkrav eller forskellige omsætningssatser for varer.
-   Du kan angive lagerlokationer på et hvilket som helst niveau (for eksempel websted, lagersted, gang, reol, hylde og placeringsposition).
-   Du kan gruppere lokationer ved hjælp af indstillingerne for begrænsning af fysisk kapacitet.
-   Du kan styre, hvordan varer opbevares og plukkes, baseret på regler, der er defineret af forespørgslen.

Hvis du vil bruge lokationsstyring i Microsoft Dynamics 365 for Operations, skal du oprette et lagersted og aktivere det til styring af mere avancerede eller specialiserede lageraktiviteter. På siden **Lagersteder** skal du vælge indstillingen **Brug lagerstedsstyringsprocesser**.

### <a name="zone-groups-zones-location-types-and-locations"></a>Zonegrupper, zoner, lokationstyper og lokationer

Du skal definere lagerets zonegrupper og zoner, lokationsprofiler, lokationstyper og placeringer som en del af processen til aktivering af en lageropbygning.

-   **Zonegrupper** – en fysisk eller logisk inddeling af zoner inden for et lagersted.
-   **Zoner** – en fysisk eller logisk inddeling af lokaliteter inden for et lagersted.
-   **Lokalitetsprofiler** – en logisk eller fysisk gruppering af lokaliteter, der har samme behandlingspolitikker for lagerlokaliteter (en blanding af forskellige varenumre kan f.eks. lagres der, og de samme fysiske kapacitetsbegrænsninger gælder).
-   **Lokalitetstyper** – en fysisk eller logisk inddeling af lagerstedets lokaliteter. Du kan for eksempel oprette en lokationstype for alle midlertidige lokationer. Faste indstillinger på siden **Parametre til lagerstedsstyring** driver processen med at definere midlertidige lokalitetstyper og den endelige afsendelseslokalitetstype.
-   **Lokaliteter** – det laveste niveau af lokalitetsoplysninger. Lokaliteter bruges til at spore, hvor den disponible lagerbeholdning er gemt og plukket på et lagersted.

De enheder, du opretter for at definere din lageropbygning, bruges i forespørgsler, der er angivet i arbejdsskabeloner til at drive arbejdsordrer på lageret. Når du definerer zonerne, lokalitetstyperne osv., skal du overveje, hvordan forskellige områder på lagerstedet bruges til forskellige processer. Derudover skal du overveje faktorer som de fysiske karakteristika for et bestemt område. Der kan eksempelvis være områder, hvor du kan bruge kun en bestemt type truck, der. Eller hvis din virksomhed har både produktion og færdige varer inden for den samme facilitet, kan du oprette et enkelt lagersted i Dynamics 365 for operationer, men derefter adskiller de to operationer ved at oprette to grupper i zonen. Giv dine enheder beskrivende navne, så det er nemt at identificere dem, når du bruger dem i skabelonen forespørgsler.

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a>Grænser for lokalitetslagring, lokalitetsprofiler og faste plukpladser

Du skal overveje den fysiske udformning af lagerstedet, både til at bestemme lagerkapacitet (grænser for lokalitetslagring og lokalitetsprofiler) og som en del af dit forsøg på at opnå optimale lagerprocesser. 

Placering belægningsgraden grænser hjælper med at sikre, at arbejdet ikke er oprettet for at anmode om, at lageret sættes på en placering, der ikke har den fysiske kapacitet til at have på lager. Eksempelvis hvis nogle steder inden for et lagersted kan holde en palle pr. lokation, kan placering, lagerføre grænser være aktiveret. Den ** antal ** værdi kan indstilles til **1**, og den ** enhed ** værdi kan indstilles til **PL** inden for en bestemt lokation profil gruppering. 

Hvis der kræves mere avancerede beregninger til at styre kapacitetsbegrænsninger for lokaliteter, kan lokalitetsprofilindstillingerne bruges. I dette tilfælde betragtes vægt og volumen, når kapacitetsberegninger er færdige. 

For at opnå optimal udgående processer skal du evaluere, om du vil bruge faste plukpladser og/eller pakkelokaliteter. Ofte bruges minimum/maksimum genopfyldning til genopfyldningsprocesser fra et bulk-område til de faste plukpladser, og flere faste plukpladser kan aktiveres inden for samme lager- og produktvarianter. Overvej den fleksibilitet, du kan opnå ved at aktivere dedikeret behov for genopfyldning ved overløb af lokaliteter, der kun bruges til behandling af bølge/belastning ved genopfyldning.

### <a name="location-setup-wizard"></a>Guiden Konfiguration af lokation

Du kan bruge for hurtigt at oprette placeringer på et lagersted, den ** lokationsopsætning ** guide. Du kan sagtens bevare formatet af lokationsnavne som en del af denne proces.

## <a name="warehouse-processes"></a>Lagerstedsprocesser
Som en del af konfigurationen af lagerstedet er det vigtigt, at du aktiverer lagerstedsprocesser efter virksomhedens behov. De vigtigste komponenter, du skal konfigurere, er bølgeskabeloner, arbejdsskabeloner, arbejdspuljer og lokalitetsvejledninger.

### <a name="wave-templates"></a>Bølgeskabeloner

Bølgeskabeloner hjælper med at sikre den udgående proces "Frigiv til lagersted". Så snart ordrelinjer udgives (enten direkte fra kildedokumenter, via kørselsprocesserne eller via belastninger, der allerede er oprettet), bruges funktionen med bølgeskabelon. 

Du kan oprette tre typer af wave-skabeloner: **levering**, **produktion**, og **Kanban**. Parametre, der bruges til at definere, hvor langt systemet automatisk skal gå i behandling af udgående arbejde. En bølgeskabelon er valgt ud fra bølgeskabelonens rækkefølge og kriterier, der er angivet i skabelonen. Hvis en skabelon er angivet øverst i rækkefølgen, kontrolleres først kriterier i den pågældende skabelon. Hvis kriterierne kan opfyldes, behandles bølgeskabelonen. I modsat fald kontrolleres kriterierne i den næste skabelon osv. Det er derfor en god ide at placere den skabelon, som har de mest specifikke kriterier, i toppen af listen over rækkefølgen af bølgeskabeloner, så den behandles først. Du vil f.eks. behandle alt arbejde for et bestemt luftfartsselskab i dag og midlertidigt udskyde behandlingen af arbejdet for andre luftfartsselskaber. I dette tilfælde skal den bølgeskabelon, der vælger arbejde for luftfartsselskabet, i så fald anføres højere i rækkefølgen end andre skabeloner. Ellers kan arbejde for andre luftfartsselskaber blive behandlet, før arbejdet for luftfartsselskabet er fuldført. 

Du skal angive metoder for bølgeprocessen i de enkelte bølgeskabeloner. De tilgængelige metoder afhænger af typen af bølgeskabelon.

### <a name="work-templates"></a>Arbejdsskabeloner

Skabelondefinitioner for arbejde spiller en vigtig rolle i definitionen af arbejdsprocesser for lagerstyring. De definerer, hvilket arbejde der udføres, og hvordan arbejdet udføres. Skabeloner kan også indeholde en vejledningskode, der indeholder hyperlinks til en lokalitetsvejledning, der bestemmer, hvor arbejdet udføres. Arbejdsskabeloner omfatter en forespørgsel, der angiver kriterier for arbejdet. Hver skabelon skal indeholde mindst én handling af pluk og læg for at drive det grundlæggende arbejde med at overføre disponibel lagerbeholdning fra én lokalitet til en anden. 

Hvis flere arbejdere skal kunne behandle arbejde for nogle af dine aktiviteter på lagerstedet, kan du bruge begrebet *midlertidig* for lageret og adskille arbejdsudførelse i forskellige arbejdsklasser.

### <a name="work-pools"></a>Arbejdspuljer

Arbejdspuljer bruges til at organisere arbejde i grupper. Du kan f.eks. oprette en arbejdsgruppe til at klassificere arbejde, der opstår på et bestemt lagersted. Med undtagelse af optælling kan du for arbejdstyper tildele en arbejdsgruppe til en arbejdsskabelon. Når det gælder cyklusoptælling, kan du tildele en arbejdspulje til følgende sider:

-   Cyklusoptællingsplaner
-   Cyklusoptællingsgrænser
-   Cyklusoptællingsarbejde efter lokation
-   Cyklusoptællingsarbejde efter vare

Når du bruger arbejdsskabeloner til at oprette arbejde, tildeles arbejdspuljen automatisk til arbejdet. 

Arbejdspulje-id'er kan også bruges til at begrænse typen af arbejde, der sendes til en bestemt lagermedarbejder, forudsat at denne funktionalitet er konfigureret på menupunktet på den relevante mobilenhed.

### <a name="location-directives"></a>Lokationsvejledninger

Som navnet antyder, bruges lokalitetsvejledninger til at dirigere arbejdstransaktioner til de relevante lokaliteter på lagerstedet. Med andre ord definerer de, hvor der skal plukkes og lægges. 

For at gøre det nemmere og hurtigere at definere de handlinger, der er tilknyttet hver enkelt linje for lokalitetsvejledning, skal du bruge en af de foruddefinerede strategier. Du kan f.eks. bruge strategien **Tom lokation uden indgående arbejde** til at søge efter ledige lokaliteter på et lagersted, eller du kan bruge strategien **FEFO-batchreservation** for udgående salgspluk.

<a name="see-also"></a>Se også
--------

[Konfigurere lokationer i et oplag af WMS-aktiveret (opgave guide)](https://ax.help.dynamics.com/en/wiki/configure-locations-in-a-wms-enabled-warehousing/)


