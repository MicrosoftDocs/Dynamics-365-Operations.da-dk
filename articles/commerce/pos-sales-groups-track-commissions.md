---
title: Spore provisioner i POS via salgsgrupper
description: Det er almindelig detailpraksis at spore salg efter den salgsmedarbejder, der har arbejdet med kunden – ydet assistance, mersalg, krydssalg og behandlet transaktionen.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: afbf69c072ae205e973203d97a5fbca7504ae04f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022051"
---
# <a name="track-commissions-in-the-point-of-sale-pos-by-using-sales-groups"></a>Spore provisioner i POS via salgsgrupper

[!include [banner](includes/banner.md)]

Det er almindelig detailpraksis at spore salg efter den salgsmedarbejder, der har arbejdet med kunden – ved at yde assistance, mersalg, krydssalg og behandle transaktionen.

Sporing af salg efter sælger er et målepunkt for salgsmedarbejderens salgsevner, mens salg efter kasserer er et målepunkt for hastighed og effektivitet. Salg sporet efter sælger bruges også ofte til at beregne provision eller andre incitamenter.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Konfiguration af en medarbejder til at være sælger i POS

Når en medarbejder er føjet til en salgsgruppe, bliver vedkommende berettiget til provision og kan identificeres som en sælger i systemet. En medarbejder, der ikke er i en salgsgruppe, er ikke berettiget til provision og angives ikke som sælger i POS-programmet. Liste over sælgere i POS er afledt af alle salgsgrupper, der indeholder mindst én medarbejder, der er tildelt til butikken. Listen er vist i POS som en kombination af salgsgruppe-id'et og navnet (Id: navn). En standardsalgsgruppe kan tildeles til medarbejdere til at understøtte scenarier, hvor detailhandleren vælger at angive sælgeren på POS-linjer automatisk. Brugerne kan vælge mellem alle de salgsgrupper, som medarbejderen er medlem af.

## <a name="functionality-profile-settings"></a>Indstillinger for funktionalitetsprofil

Der er en række indstillinger for funktionalitetsprofil for en butik, der bestemmer flowet og processen i POS, der vedrører sælgere.

<table>
<thead>
<tr>
<th>Profil</th>
<th>Betegnelse</th>
</tr>
</thead>
<tbody>
<tr>
<td>Brug kasserer som standard, hvis tilgængelig</td>
<td>Hvis denne indstilling er aktiveret, udfylder POS automatisk posteringslinjer med den aktuelle kasserers standardsalgsgruppe. Hvis en kasserer ikke har en standardsalgsgruppe angivet, angives værdien ikke. En bruger kan stadig angive salgsgruppen manuelt ved hjælp af en POS-knapmatrixknap.</td>
</tr>
<tr>
<td>Spørg efter sælger</td>
<td>Denne indstilling har tre mulige værdier:
<ul>
<li><strong>Nej</strong> – Hvis denne indstilling vælges, bliver brugeren ikke bedt om at vælge en salgsgruppe. Værdien kan stadig angives ved hjælp af en kasserers standardsalgsgruppe ved hjælp af en POS-knapmatrixknap.</li>
<li><strong>Starten af transaktionen</strong> – Hvis denne indstilling er valgt, og enten indstillingen <strong>Brug kasserer som standard</strong> ikke er aktiveret eller den aktuelle kasserer ikke har en standard salgsgruppe, så bliver brugeren bedt om at vælge en salgsgruppe i begyndelsen af hver transaktion. Hvis du vælger en salgsgruppe fra denne prompt, indstilles alle efterfølgende linjer som standard til den valgte salgsgruppe. En bruger kan stadig angive salgsgruppen manuelt ved hjælp af en POS-knapmatrixknap.</li>
<li><strong>For hver linje</strong> – Hvis denne indstilling er valgt, og enten indstillingen <strong>Brug kasserer som standard</strong> ikke er aktiveret eller den aktuelle kasserer ikke har en standard salgsgruppe, så bliver brugeren bedt om at vælge en salgsgruppe efter tilføjelse af hver linje. En bruger kan stadig angive salgsgruppen manuelt ved hjælp af en POS-knapmatrixknap.</li>
</ul>
</td>
</tr>
<tr>
<td>Krævet</td>
<td>Denne indstilling gælder kun, når POS er konfigureret til at bede om en sælger. Hvis den er aktiveret, skal brugeren vælge en salgsgruppe for at kunne fortsætte. Ellers vil brugeren blive bedt om det, men kan annullere og fortsætte uden at foretage et valg. Når linjen er tilføjet, kan en bruger med de nødvendige tilladelser stadig fjerne salgsgruppen fra linjen. "Kræv sælger" gennemtvinges ikke i denne situation.</td>
</tr>
</tbody>
</table>

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Vis oplysninger om sælgeren på POS-transaktionsskærmen

POS-skærmlayoutet for transaktioner og indhold kan konfigureres ved hjælp af skærmlayoutdesigneren og tildelte skærmlayouts til butikker, kasseapparater eller medarbejdere.Feltet **Sælger** feltet kan føjes til fanen Linjer i ruden Kvittering.Dette viser id'et for den angivne salgsgruppe for hver linje på transaktionsskærmbilledet.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Tilføjelse af sælgerhandlinger på POS-knapmatricer

POS gør det muligt for brugerne at konfigurere knapmatricer, som indgår i skærmlayout for at give adgang til POS-handlinger. Følgende POS-handlinger kan tildeles til knapmatricer, der vedrører sælgere.

| Handling                                 | Betegnelse |
|-------------------------------------------|-------------|
| Angiv sælger på linjen          | Denne POS-handling viser en liste over berettigede salgsgrupper (Id: navn) for butikken.Når der vælges en salgsgruppe på denne liste, angives værdien på den aktuelle transaktionslinje. |
| Ryd sælger på linjen        | Denne POS-handling fjerner den aktuelle værdi for salgsgruppe fra den aktuelle transaktionslinje. |
| Angiv sælger for transaktion   | Denne POS-handling viser en liste over berettigede salgsgrupper (Id: navn) for butikken.Når der vælges en salgsgruppe på denne liste, angives standardværdien på den aktuelle transaktion. Alle eksisterende linjer uden en tildelt salgsgruppe får værdien angivet, ligesom alle efterfølgende tilføjede linjer. |
| Ryd sælgeren på transaktionen | Denne POS-handling fjerner den aktuelle standardværdi for salgsgruppe fra den aktuelle transaktion. Det har ingen indflydelse på alle de linjer, der allerede eksisterer i transaktionen. |

## <a name="calculating-commissions"></a>Beregning af provision

Provisionen beregnes for medarbejderne i de angivne salgsgrupper på tidspunktet for bogføring af opgørelsen eller bogføring af salgsordrer.Provisionsbeløbet bestemmes på basis af medarbejderens provisionsandel, som defineret i salgsgruppen og de tilhørende indstillinger for provisionsberegning for kunden og/eller produkter på transaktionen.
