---
title: Konfigurere roller for skabeloner til arbejdsopgavehierarki
description: Dette emne giver oplysninger om opsætning af rolleoplysninger for skabeloner til arbejdsopgavehierarkier.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dfb429eae933ba4d687ec4cbd417d2f78308e47
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760506"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Konfigurere roller for skabeloner til arbejdsopgavehierarki

[!include [banner](../includes/banner.md)]

Projektledere kan konfigurere skabeloner for arbejdsopgavehierarki, som de kan anvende, når de opretter et arbejdsopgavehierarki (WBS) til nye projekter. Projektledere kan tilføje roller, når de opretter en skabelon. Benyt følgende fremgangsmåde til at tildele en rolle til en WBS-skabelon. 

1. Vælg **Projektstyring og regnskab** > **Konfiguration** > **Projekter** > **Skabeloner til arbejdsopgavehierarki**.
2. Vælg **Detaljer** for en valgt WBS-skabelon.
3. Markér en opgave på listen, og vælg derefter en rolle, der skal tildeles opgaven, i feltet **Rolle**.

## <a name="work-with-a-wbs"></a>Arbejde med et WBS

Du kan oprette et nyt WBS, eller du kan kopiere et WBS fra en eksisterende WBS-skabelon. En projektleder kan nemt administrere ressourcerne ved at tildele roller til nye opgaver i WBS'et. Roller kan erstattes, enten når der er skaffet en ressource, eller når der er identificeret en bekræftet ressource til at arbejde på opgaven. Denne fleksibilitet gør det muligt for projektledere at udføre følgende opgaver:

- Identificere det antal ressourcer, der kræves til WBS-arbejdspakker.
- Forkalkulere projektomkostninger.
- Bestemme et foreløbigt budget.
- Anslå varighed af aktivitet, baseret på roller og ressourcer.
- Udvikle nogle projektstyringsplaner, baseret på de tilgængelige projektoplysninger.

Yderligere indstillinger er tilføjet i WBS for at forbedre brugen af ressourcefunktionaliteten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Indstilling</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressourcetildelinger</td>
<td>Se de tildelte ressourcer, datoer, antallet af timer og reservationstypen for opgaver i WBS'et.</td>
</tr>
<tr class="even">
<td>Generér team automatisk</td>
<td>Tilføj automatisk planlagte ressourcer ved hjælp af roller, der er knyttet til en opgave. Finance foreslår automatisk planlagte ressourcer ved hjælp af beslutningsanalyse med flere kriterier, som er baseret på roller. Når roller og tidsforbrug (timer) er angivet for opgaverne i et WBS, og efter strukturen er blevet frigivet, skal du vælge <strong>Generér team automatisk</strong>. Det nødvendige antal planlagte ressourcer føjes til WBS og fanen <strong>Projekt og teamplanlægning</strong>.</td>
</tr>
<tr class="odd">
<td>Ressource (rulleliste)</td>
<td>På siden <strong>Start ressourcetildeling</strong> kan du vælge ressourcer, som skal reserveres definitivt eller foreløbigt, baseret på den angivne varighed. Du kan justere visningsindstillingerne og angive varigheden af ressourceaktiviteter. Du kan vælge og tildele ressourcer på arbejdspakkeniveau ved hjælp af følgende indstillinger:
<ul>
<li><strong>Accepter</strong> – Bekræft ændringer af den ressource, der er tildelt en opgave.</li>
<li><strong>Annuller</strong> – Annuller ændringer af den ressource, der er tildelt en opgave.</li>
<li><strong>Tildel automatisk</strong> – En tilgængelig bemandingsressource, der har en matchende rolle, vælges automatisk og tildeles til den markerede opgave.</li>
</ul></td>
</tr>
</tbody>
</table>

1. På siden **Alle projekter** skal du vælge projektet **XYZ-opgradering fase 2**.
2. Vælg **Plan** > **Aktiviteter** > **Arbejdsopgavehierarki**.
3. Vælg **Ny** for at føje følgende aktiviteter på niveau et til WBS:

    - Initiering
    - Planlægning
    - Udfører
    - Overvågning og kontrol
    - Afslut

4. Angiv datoerne og tidsforbruget (timer), som vist i følgende illustration.

    [![Angivelse af datoer og indsats](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Vælg opgavelinjen **Initiering**, og vælg derefter **Seniorprojektleder** i feltet **Rolle**.
6. Vælg **Publicer**.
7. På samme linje i feltet **Ressource** skal du vælge **Daniel Goldschmidt**, og derefter vælge **Godkend**.
8. Vælg opgavelinjen **Planlægning**, og vælg derefter **Forretningsanalytiker** i feltet **Rolle**.
9. Vælg **Publicer**, og vælg derefter **Generér team automatisk**.
10. Vælg **Ja** i den dialogboks, der vises.
11. I feltet **Ressource** skal du kontrollere, at værdien er **Forretningsanalytiker 1**.
12. For ressourcen **Forretningsanalytiker 1** skal du åbne opslaget og vælge **Start ressourcetildeling**. Vælg derefter en arbejder til opgaven.
13. Vælg **Tildel foreløbigt** &gt; **Fuld kapacitet**.

    > [!NOTE] 
    > Du modtager ikke en advarsel om, at den angivne ressource nu er 2, fordi antallet af ressourcer forbliver på 1.

14. På siden **Arbejdsopdelingsstruktur** skal du validere ressourcetildelingen på WBS'et og derefter vælge **Gem**.
