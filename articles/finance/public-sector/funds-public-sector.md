---
title: Midler i den offentlige sektor
description: Denne artikel beskriver, hvordan enheder i den offentlige sektor bruger midler til at demonstrere deres økonomiske ansvarlighed. Et middel er et selvafstemmende sæt regnskabsbøger, der bruges til at styre og overvåge den planlagte udnyttelse af ressourcerne, ofte i overensstemmelse med de retlige og administrative krav.
author: v-kiarnd
ms.date: 08/07/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerFund, LedgerFundType
audience: Application User
ms.reviewer: twheeloc
ms.custom: 19571
ms.assetid: c746c09f-dc9e-4381-ae92-e1af484064b6
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4623e751cc4b72937a93b3e11dadd53551a5d432
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897942"
---
# <a name="funds-in-the-public-sector"></a>Midler i den offentlige sektor

[!include [banner](../includes/banner.md)]

Et middel er et selvafstemmende sæt regnskabsbøger, der bruges til at styre og overvåge den planlagte udnyttelse af ressourcerne, ofte i overensstemmelse med de retlige og administrative krav. Organisationer i den offentlige sektor bruger midler til at demonstrere deres økonomiske ansvarlighed.

## <a name="what-general-ledger-parameters-should-be-set-for-funds"></a>Hvilke Finans-parametre skal angives for midler?

Hvis du vil vide mere om de Finans-parametre, der er nødvendige for midler, skal du se under [Finans i den offentlige sektor](general-ledger-public-sector.md).

## <a name="what-fund-classes-and-fund-types-do-i-need-to-set-up"></a>Hvilke middelklasser og -typer skal jeg angive?
GASB (Governmental Accounting Standards Board) anbefaler GAAP (Generally Accepted Accounting Principles) til regnskabsføring for delstater og lokale myndigheder. GAAP identificerer otte middeltyper, der er kategoriseret i de tre middelklasser:

-   Offentlige midler
    -   Generelle midler
    -   Særlige indtægtsmidler
    -   Midler i forbindelse med kapitalprojekter
    -   Midler i forbindelse med servicing af gæld
-   Beskyttede midler eller forretningsrelaterede midler
    -   Virksomhedsmidler
    -   Interne tjenestemidler
-   Fiduciariske midler
    -   Forvaltningsmidler
    -   Agenturmidler

De tre GAAP-finansieringskildeklasser, plus en **Notat**-klasse, er foruddefinerede indstillinger i Dynamics 365 Finance. 

Middeltyper defineres i henhold til organisationens behov. I de fleste tilfælde skal du angive de otte typer af GAAP-midler. Middeltyperne grupperer midler til detaljeret finansiel opfølgning og rapportering. Mange midler kan indgå i en enkelt overordnet rapport, men de enkelte midler forbliver en særskilt finansiel og regnskabsmæssig enhed med sin egen finans, resultatopgørelse og egne balancerapporter. 

Hvert enkelt middel skal have et entydigt middelnummer. Middeltal bruges som dimensionsværdier i økonomiske kontonumre, hvor en dimension er knyttet til et middel. Når et kontonummer er knyttet til et bestemt middel, tilhører det en række finansielle regnskabsbøger, der er omfattet af dette middel.

### <a name="example"></a>Eksempel

Her er en liste over nogle af de midler, der kan bruges af myndighederne i en by:

-   Generelt middel
-   School of Technology
-   Informationsteknologi
-   Farmers Market
-   Utilities Commission
-   Fragttjeneste
-   Worker’s Compensation Fund
-   Omfattende medicinordning
-   Udskudt aflønning
-   Opkrævning af lokal moms
-   Domstolsansatte

Følgende tabel viser disse midler grupperet efter klasse og middeltype.

| Finansieringskildeklasse | Finansieringskildetype          | Finansieringskildenummer | Navn på finansieringskilde                    |
|----------------|------------------------|-----------------|----------------------------------|
| Offentlig   | Generelt middel           | 1103            | Generelt middel                     |
|                | Særlige indtægtsmidler  | 1343            | School of Technology             |
|                |                        | 1372            | Informationsteknologi           |
| Beskyttede    | Virksomhedsmidler       | 2501            | Farmers Market                   |
|                |                        | 2541            | Utilities Commission             |
|                | Interne tjenestemidler | 2723            | Fragttjeneste                  |
|                |                        | 2738            | Worker’s Compensation Fund       |
| Fiduciariske      | Pension Trust Funds    | 3320            | Omfattende medicinordning |
|                |                        | 3324            | Udskudt aflønning            |
|                | Agenturmidler           | 3912            | Opkrævning af lokal moms      |
|                |                        | 3914            | Domstolsansatte                  |

## <a name="how-are-financial-dimensions-used-with-funds"></a>Hvordan bruges økonomiske dimensioner med midler?
Hvert enkelt middel skal have et entydigt middelnummer. Middeltal bruges som dimensionsværdier i økonomiske kontonumre, hvor en dimension er knyttet til et middel. Når et kontonummer er knyttet til et bestemt middel, tilhører det en række finansielle regnskabsbøger, der er omfattet af dette middel. 

Offentlige organisationer kræver normalt afstemte poster for økonomiske dimensioner, der er relateret til midler. Når en økonomisk dimension eller en kombination af dimensioner er markeret til at kræve afstemte poster, vil systemet ikke bogføre en transaktion, hvor debet ikke svarer til kredit for den økonomiske dimension.

## <a name="how-do-i-set-a-fund-balance-to-carry-over-to-the-new-year"></a>Hvordan indstiller jeg en middelsaldo, som skal overføres til det nye år?
Hvis du vil vide mere om årsafslutningen for midler, skal du se under [Årsafslutningen i den offentlige sektor](year-end-processing-public-sector.md).


Du kan finde flere oplysninger under følgende emner:

[Oprettelse af en middeltype](tasks/create-fund-type-public-sector.md)

[Konfigurere et middel](tasks/set-up-fund-public-sector.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
