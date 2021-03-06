---
title: Kundekreditgrupper
description: Dette emne indeholder oplysninger om arbejdsgangen for kundekreditgrupper.
author: mikefalkner
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3cdf4f7e72a55292c64b7a9191974242aab85a90
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835310"
---
# <a name="customer-credit-groups"></a>Kundekreditgrupper

[!include [banner](../includes/banner.md)]

Du kan definere grupper af kunder, der har et delt kreditmaksimum. De enkelte kreditmaksimum, der er defineret på debitorfakturakontoen, tages også i betragtning.

Medlemmer af en kundekreditgruppe kan vælges fra forskellige juridiske enheder. Når du føjer en kunde til listen over kunder i kundekreditgruppen, ændres udløbsdatoen for kreditmaksimum for de enkelte kunder til den udløbsdato, der er tildelt gruppen.

Du kan oprette kundekreditgrupper på siden **Kundekreditgrupper** (**Kreditstyring \> Kundekreditgrupper \> Kundekreditgrupper**).

1. Angiv en identifikator og en beskrivelse af gruppen i felterne **Gruppenummer** og **Beskrivelse**.
2. Angiv det kreditmaksimum og den valuta, der skal bruges, når systemet kontrollerer kreditmaksimum for et medlem af gruppen, i felterne **Kreditgrænse** og **Valuta**.
3. Angiv den dato, hvor kreditgrænsen udløber, i feltet **Kreditmaksimum til dato**. Kundekreditgrupper skal have en udløbsdato.

Når du er færdig med at oprette en kundekreditgruppe, kan du føje debitorer til den ved at angive deres juridiske enhed og kundekonto-id'et. Når du føjer en ny kunde til en kundekreditgruppe, søger systemet efter den samme kundekonto på tværs af alle juridiske enheder, og du bliver bedt om at føje den til kundekreditgruppen.

Brug menuen **Aldersfordelte saldi** til at få vist detaljer om den aldersfordelte saldo for alle fakturakunder i en kundekreditgruppe. På siden **Aldersfordelt saldo** vises en oversigt over aldersfordelte saldi for debitorkontiene på fakturaen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]