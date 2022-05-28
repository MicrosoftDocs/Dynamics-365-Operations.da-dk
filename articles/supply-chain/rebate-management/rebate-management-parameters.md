---
title: Parametre til rabatstyring
description: I dette emne beskrives siden Parametre for rabatstyring. Denne side indeholder indstillinger, der påvirker bogføring, statusopdateringer, nummerserier og anden funktionalitet.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8f5c9734b2480329eed246bcbbfe3bd6e9991e0b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688985"
---
# <a name="rebate-management-parameters"></a>Parametre til rabatstyring

[!include [banner](../includes/banner.md)]

Siden **Parametre for rabatstyring** bruges til at definere de indstillinger, der gælder for hele modulet **Rabatstyring**. Disse indstillinger påvirker bogføring, statusopdateringer, nummerserier og anden funktionalitet. Opsætningen på denne side deles på tværs af juridiske enheder og kan redigeres af brugere, der har de relevante sikkerhedsrettigheder.

Du kan åbne siden **Parametre for rabatstyring** ved at gå til **Rabatstyring \> Konfiguration \> Parametre til rabatstyring**. Derefter skal du angive felterne som beskrevet i følgende underafsnit.

## <a name="rebate-management-tab"></a>Fanen Rabatstyring

I følgende tabel beskrives de felter, der er tilgængelige under fanen **Rabatstyring** på siden **Parametre for rabatstyring**.

| Felt | Betegnelse |
|---|---|
| Standardstatus | Vælg standardstatus for alle nye aftaler. Brug siden [**Rabatstatusser**](rebate-statuses.md) til at definere sættet med statusværdier, der kan vælges. |
| Proces efter dimension | Vælg, om hensættelses-, rabat- og afskrivningstransaktioner skal behandles efter økonomisk dimension. Når denne indstilling er aktiveret, bruger systemet økonomiske dimensioner fra kildetransaktionerne i måltransaktionerne. |
| Kontrollér, om tidligere bogført | <p>Vælg systemfunktionsmåden, hvis ikke-bogførte rabattransaktioner skal behandles mere end én gang for samme periode:</p><ul><li>**Advarsel** – Systemet giver brugerne mulighed for at tilsidesætte de oprindelige transaktionslinjer, men der vises en advarsel.</li><li>**Fejl** – Systemet forhindrer brugere i at tilsidesætte de oprindelige transaktionslinjer, og der vises en fejlmeddelelse. |
| Bogfør kladder automatisk | Vælg, om systemet automatisk skal bogføre foreslåede kladder. Disse kladder omfatter daglige kladder, der bruges til hensættelser og kundefradrag, samt kreditormomsfakturakladder. |
| Bogføre fritekstfakturaer automatisk | Vælg, om systemet automatisk skal bogføre fritekstfakturaer. Denne indstilling gælder kun for fritekstfakturaer, hvor betalingstypen er angivet til *Debitorfradrag på momsfaktura*. |
| Reference til rabatvareordre | Vælg den rabatreference, der skal bruges i salgsordrer og indkøbsordrer, som genereres af rabatprocessen (*Ingen*, *Rabatstyringshandel*, *Rabatstyringsnummer*, *Rabattransaktionsnummer* eller *Dokumentnoter*). |
| Brug kravsproces | <p>Angiv denne indstilling til *Ja*, hvis du vil bruge en kravsproces. På denne måde kan du markere de transaktioner, som Rabatstyring opretter som enten indkasserede eller ikke indkasserede, og derefter kun bogføre de indkasserede transaktioner.</p><p>Du beregner f.eks. rabatter for en måneds transaktioner, men kunden har ikke indkasseret to dage. I dette tilfælde oprettes de ikke-indkasserede transaktioner igen, næste gang du kører funktionen *Proces* for næste periode.</p><p>Hvis du angiver denne indstilling til *Nej*, bogføres alle kravtransaktioner.</p> |
| Medtag ordretypekladde | I forbindelse med aftaler eller aftalelinjer, hvor transaktionstypen er angivet til *Ordre*, styrer denne indstilling, om en salgsordre af typen *Kladde* skal inkluderes. Den giver fleksibilitet, hvis disse ordretyper bruges i scenarier, hvor en rabat endnu ikke skal anvendes. |

## <a name="number-sequences-tab"></a>Fanen Nummerserier

Brug fanen **Nummerserier** på siden **Parametre for rabatstyring** til at tildele nummerseriekoder til de forskellige nummerserier, som Rabatstyring bruger. I følgende tabel beskrives formålet med hver af disse nummerserier. Yderligere oplysninger om nummerserier finder du i [Oversigt over nummerserier](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) og relaterede emner.

| Reference | Betegnelse |
|---|---|
| Rabatstyringshandel | Nummerserien tildeler en entydig nøgleværdi til hver rabataftale. Denne nøgle bruges, når der oprettes aftaler. |
| Rabatstyringsnummer | Nummerserien tildeler en entydig nøgleværdi til hver rabat. Denne nøgle bruges til at identificere rabatrelationer. |
| Rabattransaktionsnummer | Nummerserien tildeler en entydig nøgleværdi til hver rabattransaktion. Denne nøgle bruges til at identificere rabattransaktioner. |
| Momsfaktura | Nummerserien tildeler en entydig nøgleværdi til hver rabatfaktura. Denne nøgle bruges, når rabatkladder bogføres automatisk. |

## <a name="feature-visibility-tab"></a>Fanen Funktionssynlighed

Rabatstyring føjer funktioner (felter og funktioner) til flere sider, der ofte bruges i Microsoft Dynamics 365 Supply Chain Management. Disse sider omfatter sider, der er relateret til salgsordrer og salgsaftaler. Hvis du bruger Rabatstyring, skal du gøre disse funktioner synlige overalt, før du kan udnytte dem. Hvis du ikke bruger Rabatstyring, kan du skjule funktionerne for at holde dem ude af vejen.

Under fanen **Funktionssynlighed** på siden **Parametre for rabatstyring** skal du angive indstillingen **Aktivér** til *Ja* for at gøre funktioner for Rabatstyring synlige alle de steder, hvor de er tilgængelige. Angiv den til *Nej* for at skjule funktionerne på fælles sider uden for modulet **Rabatstyring**. Men selv når indstillingen er angivet til *Nej*, vil selve modulet, herunder siden **Parametre for rabatstyring**, stadig være tilgængeligt for brugere, der har de korrekte adgangstilladelser til den.
