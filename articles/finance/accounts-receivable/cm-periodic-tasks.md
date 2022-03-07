---
title: Periodiske opgaver for kreditstyring
description: I dette emne beskrives de periodiske opgaver, der er en del af processen til administration af kreditmaksimum for kunder.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 398fcd9d45ce0ddfb1f7189e0712f9dac2db012f
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753501"
---
# <a name="periodic-credit-management-tasks"></a>Periodiske kreditsstyringsopgaver

[!include [banner](../includes/banner.md)]

I dette emne beskrives de periodiske opgaver, der er en del af processen til administration af kreditmaksimum for kunder.

## <a name="update-risk-scores"></a>Opdater risikoscorer

Efterhånden som virksomheder udvikler sig og deres omstændigheder ændres, kan det også betyde, at kunders kreditrisici ændres. For at sikre opretholdelse af relevante kreditlofter for kunderne skal du regelmæssigt gennemgå kriterierne for hver risikovurdering og opdatere vurderingerne for hver kunde. Du kan opdatere følgende vurderinger på siden **Opdater risikovurderinger** (**Kredit \> Periodiske opgaver \> Kreditstyring \> Opdater risikovurderinger**). Alle brugerdefinerede beregninger behandles også.

- **Betalingsdage i gennemsnit**– Denne vurdering er det gennemsnitlige antal dage, inden en kunde betaler fakturaer.
- **Kunde siden** – Denne vurdering er det antal år, som en kunde har været kunde i din organisation.
- **Har drevet forretning siden** – Denne vurdering er det antal år, som en kunde har drevet forretning på området. Værdien i feltet **Virksomhedsstart** på siden **Kunder** bruges.
- **Udestående dages salg** – Denne vurdering er baseret på debitorsaldoen, salgsindtægterne og antallet af dage for den foregående 12-måneders periode.
- **Gennemsnitlig saldo** – Denne vurdering er baseret på debitorsaldoen for den forrige 12-måneders periode.
- **Kreditstyringsgruppe**, **Kontostatus** og **Land** – Disse vurderinger bruger oplysninger fra kunden.

## <a name="update-customer-balance-statistics"></a>Opdatere statistik for debitorsaldo

Du kan køre processen **Opdatere statistik for debitorsaldo** for at opdatere beregningen af saldostatistik, der vises på siden med **Forespørgsler om saldostatistik**. Disse oplysninger bruges til at beregne risikovurderinger og de værdier, der vises i faktaboksene med kreditstatistik på siden **Kunde**.

Når du kører processen, opdateres debitorsaldostatistik for en enkelt debitor. Hvis du vil definere et batchjob, der skal køre processen for flere debitorer, kan du bruge siden **Beregn saldostatistik** (**Kreditstyring \> Periodiske opgaver \> Beregn saldostatistik**).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
