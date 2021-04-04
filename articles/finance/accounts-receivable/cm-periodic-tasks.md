---
title: Periodiske opgaver for kreditstyring
description: I dette emne beskrives de periodiske opgaver, der er en del af processen til administration af kreditmaksimum for kunder.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a034d563c12c4ba8b99e13b30ea2683555a01276
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254481"
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