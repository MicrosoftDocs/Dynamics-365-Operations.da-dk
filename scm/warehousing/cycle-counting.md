---
title: "Cyklusoptælling"
description: "I denne artikel beskrives, hvordan du kan bruge cyklusoptælling med den lagerstedsløsning, der er tilgængelig i Lagerstedsstyring. Denne artikel gælder ikke for lagerstedsløsninger, der findes i Lagerstyring."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4446dfec1fa8eabb45e14b3f2ff685b3b1d68e2c
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="cycle-counting"></a>Cyklusoptælling

[!include[banner](../includes/banner.md)]


I denne artikel beskrives, hvordan du kan bruge cyklusoptælling med den lagerstedsløsning, der er tilgængelig i Lagerstedsstyring. Denne artikel gælder ikke for lagerstedsløsninger, der findes i Lagerstyring.

Cyklusoptælling er en lagerproces, du kan bruge til at overvåge disponible varer i lagerbeholdningen. Cyklusoptællingsprocessen kan beskrives i tre trin:

1.  **Oprette cyklusoptællingsarbejde** – cyklusoptællingsarbejde kan oprettes automatisk baseret på tærskelparametre for varer eller ved hjælp af en plan til cyklusoptælling. Du kan også oprette cyklusoptællingsarbejde manuelt ved hjælp af parametrene for vare eller lagersted på siden **Cyklusoptællingsarbejde efter vare** eller siden **Cyklusoptællingsarbejde efter lokalitet**.
2.  **Udfør behandling af cyklusoptællingen** – Når cyklusoptællingsarbejdet er oprettet, udfører du cyklusoptællingsarbejde ved optælling af varer på et lagersted og derefter bruge en mobilenhed til at angive resultatet i Microsoft Dynamics 365 for Operations. Du kan også tælle varer på et lagersted uden at oprette cyklusoptællingsarbejde. Denne proces kaldes *spotcyklusoptælling*.
3.  **Løs forskelle i værdien for cyklusoptællingen** – efter en cyklusoptælling vil varer, der har forskelle i den optalte værdi, have arbejdsstatussen **Afventer gennemsyn** på siden **Alt arbejde**. Du kan løse disse forskelle på siden **Ventende gennemsyn af cyklusoptællingsarbejde**.

Følgende illustration viser cyklusoptællingsprocessen. ![Procesforløb for cyklusoptælling](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a>Forudsætninger for cyklusoptælling
Følgende tabel viser de forudsætninger, der skal være på plads, før du kan begynde at bruge cyklusoptælling.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Forudsætning</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vare</td>
<td>Varen skal være aktiveret for lagerprocesser for lagersted.</td>
</tr>
<tr class="even">
<td>Lagersted</td>
<td>Lagerstedet skal være aktiveret for lagerprocesser for lagersted. Hvis du vil aktivere lagerstedet for lagerstedsstyringsprocesser, skal du på siden <strong>Lagersteder</strong> vælge lagerstedet og derefter vælge indstillingen <strong>Brug lagerstedsstyringsprocesser</strong>. Hvis du vil gøre det muligt for arbejdere at flytte paller under en cyklusoptælling, skal du vælge indstillingen <strong>Tillad palleflytninger under cyklusoptælling</strong> i oversigtspanelet <strong>Lagerstedsstyring</strong>.</td>
</tr>
<tr class="odd">
<td>Arbejdspuljer</td>
<td>Valgfrit: Opret en arbejdspulje for at udskille lagerstedsarbejdet baseret på typen af arbejde (i dette tilfælde cyklusoptællingsarbejde).</td>
</tr>
<tr class="even">
<td>Lokationer</td>
<td>Aktivér cyklusoptælling for lokationer. Hvis du vil tillade cyklusoptælling for en lagerstedslokalitet, skal du vælge indstillingen <strong>Tillad cyklusoptælling</strong> på siden <strong>Lokalitetsprofiler</strong>.</td>
</tr>
<tr class="odd">
<td>Parametre til lokationsstyring</td>
<td>Konfigurer parametre for cyklusoptælling. På siden <strong>Parametre til lagerstedsstyring</strong> skal du angive koden for standardreguleringstype, arbejdsklasse-id og arbejdsprioritet for cyklusoptælling.</td>
</tr>
<tr class="even">
<td>Mobilenhed</td>
<td><ul>
<li>Opret et menupunkt for en af følgende metoder på siden <strong>Menupunkter i mobilenhed</strong>:
<ul>
<li>Brugerstyret cyklusoptælling</li>
<li>Brugerstyret cyklusoptælling</li>
<li>Gruppering af cyklusoptælling</li>
<li>Spotcyklusoptælling</li>
</ul>
</li>
<li>Konfigurer en menu til mobilenheden.</li>
<li>Opret en brugerkonto til arbejde, og tildel en mobilenhedsmenu til arbejdsbruger-id'et.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Relateret opsætningsopgave</td>
<td>Opret en cyklusoptællingsplan for en lagerlokation.</td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a>Opret automatisk cyklusoptællingsarbejde
Der er to måder at planlægge tilbagevendende oprettelse af cyklusoptællingsarbejde: Konfigurer cyklusoptællingstærskler eller cyklusoptællingsplaner.

-   En grænse for cyklusoptælling angiver mængden eller den procentvise grænse for lagervarer. Cyklusoptællingsarbejde oprettes automatisk, når grænsen er nået.
-   En cyklusoptællingsplan opretter cyklusoptællingsarbejde straks eller med jævne mellemrum. Når der oprettes cyklusoptællingsarbejde, indeholder optællingsarbejdslinjen oplysninger om, hvilken lokalitet der skal optælles. Den disponible lagerbeholdning, der er knyttet til denne lokalitet, er ikke blokeret og er derfor tilgængelig for reservation og udgående behandling, selvom der findes åbent optællingsarbejde.

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a>Oprette cyklusoptællingsarbejde baseret på tærskelparametre for varer

Cyklusoptællingsarbejde kan oprettes, når antallet af varer falder under en bestemt tærskelværdi på en lokalitet. For eksempel er der 60 varer på en lokalitet, der har en grænse på 40 for cyklusoptælling. Under en salgsordrepostering plukkes 25 varer fra lokaliteten og lægges på en midlertidig lokalitet. Da antallet af nye elementer på 35 er mindre end tærskelantallet, oprettes cyklusoptællingsarbejdet automatisk for lokationen.

### <a name="schedule-cycle-counting-work"></a>Planlægge cyklusoptællingsarbejde

Du kan lægge cyklusoptællingsplaner for at oprette cyklusoptællingsarbejde straks eller med jævne mellemrum. Når du konfigurerer cyklusoptællingsplaner, kan du styre den arbejdspulje, som cyklusoptællingsarbejdet er oprettet for, det maksimale antal cyklusoptællinger, der er oprettet for varer på forskellige lokaliteter, og antallet af dage, før en lagerlokation tælles igen. Eksempel: En vare er tilgængelige på tre lokaliteter på lageret, og det maksimale antal cyklusoptællinger er indstillet til **2**. I dette tilfælde oprettes to cyklusoptællinger for de to lokationer, hvor varen er, når du kører cyklusoptællingsplanen. Et andet eksempel: Du indstiller antallet af dage mellem cyklusoptællinger til **5**. I dette tilfælde oprettes cyklusoptællingsarbejdet hver femte dag. Men cyklusoptællingsarbejdet imidlertid behandles på dag 3, oprettes det næste cyklusoptællingsarbejde, fem dage efter at den seneste cyklusoptælling blev behandling, nemlig på dag 8.

## <a name="create-cycle-counting-work-manually"></a>Oprette cyklusoptællingsarbejde manuelt
For at oprette en cyklusoptællingsarbejde manuelt kan du bruge siden **Cyklusoptællingsarbejde efter vare** eller **Cyklusoptællingsarbejde efter lokation**. Du kan angive det maks. antal cyklusoptællinger, der skal oprettes. For eksempel hvis lagerchefen angiver en værdi på **5**, oprettes der cyklusoptællingsarbejde for fem steder, selvom varen findes på 10 lokaliteter. Du kan også vælge et arbejdsgruppe-id, som de oprettede id'er for cyklusoptællingsarbejdet skal tildeles til. Når et arbejdspulje-id er behandlet for cyklusoptælling, behandles id'er for cyklusoptællingsarbejde, der er tildelt til arbejdspuljen, som en gruppe.

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a>Udføre en cyklusoptælling ved hjælp af en mobilenhed
Der er flere metoder til behandling af cyklusoptællingsarbejde ved hjælp af Dynamics 365 for Operations på en mobilenhed:

-   **Brugerbaseret** – Arbejderen kan angive et id for cyklusoptællingsarbejde, der har statussen **Åben**.
-   **Systembaseret** – Dynamics 365 for Operations tildeler et id for cyklusoptællingsarbejde til arbejderen.
-   **Gruppering af cyklusoptælling** – Arbejderen kan gruppere id'er for cyklusoptællingsarbejde, der er specifikke for en bestemt lokation, zone eller arbejdspulje.
-   **Spotcyklusoptælling** – Valgfrit: Arbejderen kan tælle elementerne på en lagerlokation til enhver tid uden at oprette cyklusoptællingsarbejde. For at udføre spotcyklusoptælling på en lokation angiver arbejderen lokalitets-id'et.

Følgende er et eksempel på, hvordan du kan udføre spotcyklusoptælling ved hjælp af en mobilenhed: Vejledningen, som arbejderen kan se på enheden, afhænger af opsætningen af menupunktet for spotcyklusoptælling.

1.  Vælg det menupunkt, der skal bruges til at behandle cyklusoptællingsarbejdet, på mobilenheden.
2.  Registrer lokaliteten, der skal udføres spotcyklusoptælling for.
3.  Register og bekræft varenummeret og antallet af optalte varer. **Bemærk!** Statussen for cyklusoptællingsarbejdet opdateres til **Afventer gennemsyn** eller **Lukket** på siden **Alt arbejde**, afhængigt af de parametre, der er angivet på siden **Arbejder**.
4.  Valgfrit: Gentag trin 3 for de resterende varer på placeringen, og bekræft, at der ingen yderligere elementer er til optælling.

## <a name="resolve-cycle-counting-differences"></a>Løse cyklusoptællingsforskelle
En cyklusoptællingsforskel opstår i følgende situationer, hvis indstillingen **Er en cyklusoptællingssupervisor** er **Nej** for et arbejdsbruger-id:

-   Værdien for optællingen er ikke inden for de afvigelsesgrænser, der er angivet i feltet **Grænse for maks. procent** eller feltet **Grænse for maks. antal** på siden **Arbejdsbrugere**. For eksempel er det disponible lagerantal på en lokalitet 50, og afvigelsesgrænsen for arbejdsbrugeren er 10. Hvis arbejdsbrugeren indtaster en værdi, der ikke er mellem 40 og 60, opstår der en forskel.
-   Værdien for optællingen adskiller sig fra det disponible lagerantal, og der er ingen angivne afvigelsesgrænser.

Du kan justere forskelle i den optalte værdi og derefter acceptere den optællingsværdien på siden **Ventende gennemsyn af cyklusoptælling**. Du kan kontrollere det ændrede vareantal på siden **Disponibel efter lokalitet**. Værdien for optællingen afvises, hvis forskellen ikke kan godkendes.

# <a name="see-also"></a>Se også
[Konfigurer mobilenheder til lagerstedsarbejde](configure-mobile-devices-warehouse.md)




