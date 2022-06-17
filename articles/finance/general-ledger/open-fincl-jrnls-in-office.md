---
title: Åbne økonomikladdeskabeloner i Office
description: I denne artikel beskrives de problemer, der kan opstå, når du opretter brugerdefinerede økonomikladder ved hjælp af en Microsoft Excel-skabelon.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a29ab1cb2980ebfed6c6fa6409538bc802849156
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896341"
---
# <a name="open-financial-journal-templates-in-office"></a>Åbne økonomikladdeskabeloner i Office

[!include [banner](../includes/banner.md)]

I denne artikel beskrives de problemer, der kan opstå, når du opretter brugerdefinerede økonomikladder ved hjælp af en Microsoft Excel-skabelon.

## <a name="symptom"></a>Symptom

Du har oprettet en brugerdefineret Excel-skabelon til økonomikladder, men den vises ikke i menuen **Åbn linjer i Excel**. Den kan vises i menuen, men der åbnes en anden skabelon, når du vælger den.

## <a name="resolution"></a>Løsning

Standardfunktionen Åbn i Excel bruger roddatakilden (tabellen) på den aktuelle side til at bestemme, hvilke Office-skabeloner eller dataenheder der vises som indstillinger i menuen **Åbn i Excel**. Denne funktionsmåde er ikke en ideel oplevelse for økonomikladder, fordi økonomikladder bruger de samme tabeller (LedgerJournalTable og LedgerJournalTrans) som roddatakilde for mange andre typer kladder.

I forbindelse med økonomikladder er funktionen Åbn linjer i Excel beregnet til at vise skabeloner, der er udviklet til den kladde, du aktuelt arbejder i forbindelse med, f.eks. økonomikladden eller en betalingskladde. En skabelon, der er beregnet til at blive brugt sammen med en kreditorbetalingskladde, vil f.eks. være designet til at gennemtvinge din primære konto som en kreditorkonto.

Hvis du vil hæve en skabelon, så den er tilgængelig på menuerne **Åbn linjer i Excel** og **Åbn i Excel**, er en nem udvikleroplevelse at implementere **LedgerIJournalExcelTemplate**-grænsefladen og udvide **DocuTemplateRegistrationBase**-klassen. Mange eksempler på denne fremgangsmåde er implementeret i systemet. Et eksempel, der kan bruges til reference, er **LedgerDailyJournalExcelTemplate**-grænsefladen, der blev oprettet til økonomikladden (eller kassekladden).

Når **LedgerIJournalExcelTemplate**-grænsefladen er implementeret for skabelonen, filtrerer menuen **Åbn linjer i Excel** kladder efter kladdetypen og viser kun de skabeloner, der er tilgængelige for den pågældende kladde. Grænsefladen indeholder også en valideringsmetode, der sikrer, at en skabelon ikke kan åbnes for en kladde, hvis den ikke opfylder kravene til kontotypen. Du kan f.eks. angive, at kontotypen skal være af typen **Kreditor** eller **Finans**.

Du kan finde flere oplysninger om denne funktion i [Føje skabeloner til menuen Åbn i Excel](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).
