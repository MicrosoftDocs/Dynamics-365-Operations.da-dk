---
title: Oversigt over konfiguration af lagersted
description: I denne artikel beskrives det, hvordan du konfigurerer et lagersted. Det indeholder oplysninger om, hvordan du aktiverer en lageropbygning og lagerprocesser.
author: perlynne
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11554"
- intro-internal
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fb9f8864ec91332c4c66658b94b6d88715120c8
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337827"
---
# <a name="warehouse-configuration-overview"></a>Oversigt over konfiguration af lagersted

[!include [banner](../includes/banner.md)]

I denne artikel beskrives det, hvordan du konfigurerer et lagersted. Det indeholder oplysninger om, hvordan du aktiverer en lageropbygning og lagerprocesser.

> [!NOTE]
> Denne artikel gælder for funktioner i modulet **Lagerstedsstyring** (avanceret logistik). Det gælder ikke for lagerstedsfunktioner i modulet **Lagerstyring**.

## <a name="warehouse-layout"></a>Lageropbygning
Lokationsstyringssystemet i Supply Chain Management giver dig fleksible muligheder for at definere din lageropbygnings skiftende behov, så du kan opnå en optimal lagerstedseffektivitet.

-   Du kan oprette opbevaringssteder med høj prioritet og lav prioritet til optimal placering af varer.
-   Du kan opdele lageret i områder, der passer til forskellige opbevaringsbehov, som temperaturkrav eller forskellige omsætningssatser for varer.
-   Du kan angive lagerlokationer på et hvilket som helst niveau (for eksempel websted, lagersted, gang, reol, hylde og placeringsposition).
-   Du kan gruppere lokationer ved hjælp af indstillingerne for begrænsning af fysisk kapacitet.
-   Du kan styre, hvordan varer opbevares og plukkes, baseret på regler, der er defineret af forespørgslen.

Hvis du vil bruge styring af lagersted i Supply Chain Management, skal du oprette et lagersted og aktivere det til styring af mere avancerede eller specialiserede lageraktiviteter. På siden **Lagersteder** skal du vælge indstillingen **Brug lagerstedsstyringsprocesser**.

### <a name="zone-groups-zones-location-types-and-locations"></a>Zonegrupper, zoner, lokationstyper og lokationer

Du skal definere lagerets zonegrupper og zoner, lokationsprofiler, lokationstyper og placeringer som en del af processen til aktivering af en lageropbygning.

-   **Zonegrupper** – en fysisk eller logisk inddeling af zoner inden for et lagersted.
-   **Zoner** – en fysisk eller logisk inddeling af lokaliteter inden for et lagersted.
-   **Lokalitetsprofiler** – en logisk eller fysisk gruppering af lokaliteter, der har samme behandlingspolitikker for lagerlokaliteter (en blanding af forskellige varenumre kan f.eks. lagres der, og de samme fysiske kapacitetsbegrænsninger gælder).
-   **Lokalitetstyper** – en fysisk eller logisk inddeling af lagerstedets lokaliteter. Du kan for eksempel oprette en lokationstype for alle midlertidige lokationer. Faste indstillinger på siden **Parametre til lagerstedsstyring** driver processen med at definere midlertidige lokalitetstyper og den endelige afsendelseslokalitetstype.
-   **Lokaliteter** – det laveste niveau af lokalitetsoplysninger. Lokaliteter bruges til at spore, hvor den disponible lagerbeholdning er gemt og plukket på et lagersted.

De enheder, du opretter for at definere din lageropbygning, bruges i forespørgsler, der er angivet i arbejdsskabeloner til at drive arbejdsordrer på lageret. Når du definerer zonerne, lokalitetstyperne osv., skal du overveje, hvordan forskellige områder på lagerstedet bruges til forskellige processer. Derudover skal du overveje faktorer som de fysiske karakteristika for et bestemt område. Der kan f.eks. være områder, hvor du kun kan bruge en bestemt type gaffeltruck. Eller hvis din virksomhed har både produktion og færdigvarer inden for den samme facilitet, kan du oprette et enkelt lagersted i Supply Chain Management, men derefter adskille de to operationer ved at oprette to zonegrupper. Giv dine enheder beskrivende navne, så det er nemt at identificere dem, når du bruger dem i skabelonforespørgsler.

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a>Grænser for lokalitetslagring, lokalitetsprofiler og faste plukpladser

Du skal overveje den fysiske udformning af lagerstedet, både til at bestemme lagerkapacitet (grænser for lokalitetslagring og lokalitetsprofiler) og som en del af dit forsøg på at opnå optimale lagerprocesser. 

Grænser for lokationslagring hjælper med til at sikre, at arbejdet ikke oprettes for at anmode om, at lageret skal placeres på en lokalitet, der ikke har den fysiske kapacitet til rumme lageret. Hvis nogle steder inden for et lagersted f.eks. kun kan indeholde én palle pr. lokation, kan grænser for lokationslagring aktiveres. Værdien **Antal** kan indstilles til **1**, og værdien **Enhed** kan indstilles til **PL** inden for en bestemt lokalitetsprofilgruppering. 

Hvis der kræves mere avancerede beregninger til at styre kapacitetsbegrænsninger for lokaliteter, kan lokalitetsprofilindstillingerne bruges. I dette tilfælde betragtes vægt og volumen, når kapacitetsberegninger er færdige. 

For at opnå optimal udgående processer skal du evaluere, om du vil bruge faste plukpladser og/eller pakkelokaliteter. Ofte bruges minimum/maksimum genopfyldning til genopfyldningsprocesser fra et bulk-område til de faste plukpladser, og flere faste plukpladser kan aktiveres inden for samme lager- og produktvarianter. Overvej den fleksibilitet, du kan opnå ved at aktivere dedikeret behov for genopfyldning ved overløb af lokaliteter, der kun bruges til behandling af bølge/belastning ved genopfyldning.

### <a name="location-setup-wizard"></a>Guiden Konfiguration af lokation

Du kan hurtigt at oprette lokaliteter på et lagersted ved at bruge guiden **Konfiguration af lokalitet**. Du kan sagtens bevare formatet af lokationsnavne som en del af denne proces.

## <a name="warehouse-processes"></a>Lagerstedsprocesser
Som en del af konfigurationen af lagerstedet er det vigtigt, at du aktiverer lagerstedsprocesser efter virksomhedens behov. De vigtigste komponenter, du skal konfigurere, er bølgeskabeloner, arbejdsskabeloner, arbejdspuljer og lokalitetsvejledninger.

### <a name="wave-templates"></a>Bølgeskabeloner

Bølgeskabeloner hjælper med at sikre den udgående proces "Frigiv til lagersted". Så snart ordrelinjer udgives (enten direkte fra kildedokumenter, via kørselsprocesserne eller via belastninger, der allerede er oprettet), bruges funktionen med bølgeskabelon. 

Du kan oprette tre typer bølgeskabeloner: 
-   **Forsendelse**
-   **Produktionsordre**
-   **Kanban** 

Parametre, der bruges til at definere, hvor langt systemet automatisk skal gå i behandling af udgående arbejde. En bølgeskabelon er valgt ud fra bølgeskabelonens rækkefølge og kriterier, der er angivet i skabelonen. Hvis en skabelon er angivet øverst i rækkefølgen, kontrolleres først kriterier i den pågældende skabelon. Hvis kriterierne kan opfyldes, behandles bølgeskabelonen. I modsat fald kontrolleres kriterierne i den næste skabelon osv. Det er derfor en god ide at placere den skabelon, som har de mest specifikke kriterier, i toppen af listen over rækkefølgen af bølgeskabeloner, så den behandles først. Du vil f.eks. behandle alt arbejde for et bestemt luftfartsselskab i dag og midlertidigt udskyde behandlingen af arbejdet for andre luftfartsselskaber. I dette tilfælde skal den bølgeskabelon, der vælger arbejde for luftfartsselskabet, i så fald anføres højere i rækkefølgen end andre skabeloner. Ellers kan arbejde for andre luftfartsselskaber blive behandlet, før arbejdet for luftfartsselskabet er fuldført. 

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

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere lokationer på et WMS-aktiveret lagersted](tasks/configure-locations-wms-enabled-warehouse.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]