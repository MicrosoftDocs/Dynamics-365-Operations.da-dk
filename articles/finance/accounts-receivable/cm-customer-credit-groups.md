---
title: Kundekreditgrupper
description: Dette emne indeholder oplysninger om arbejdsgangen for kundekreditgrupper.
author: mikefalkner
manager: AnnBe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1ddf41d88d085b102a7d69eeeff0ec463d8b4137
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977953"
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
