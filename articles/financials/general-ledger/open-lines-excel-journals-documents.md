---
title: Publicere kladdelinjer og dokumenter fra Excel
description: "I dette emne beskrives, hvordan du skriver og publicerer linjer til finanskladder fra Microsoft Excel. Emnet indeholder oplysninger om de forskellige skabeloner, som du kan bruge, afhængigt af den type postering, du angiver."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: a2da864254efda2621e1b157413a16d251020786
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Publicere kladdelinjer og dokumenter fra Excel

[!INCLUDE [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du skriver og publicerer linjer til finanskladder fra Microsoft Excel. Emnet indeholder oplysninger om de forskellige skabeloner, som du kan bruge, afhængigt af den type postering, du angiver.

Brugere kan skrive og publicere linjer for økonomikladder fra Microsoft Excel. Når en bruger opretter en kladde, viser knappen **Åbn linjer i Excel** de skabeloner, der er tilgængelige. Skabeloner er udviklet til at understøtte specifikke scenarier, men ikke enhver kombination af kontotyper understøttes i kladden. Følgende tabel viser de skabeloner, der er tilgængelige, og de kontotyper, som de understøtter.

|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Skabelon**             | **Understøttede kontotyper**                                                                                             | **Sådan får du adgang til skabelonen**                                                          |
| Finansjournallinjer     | Konto: Finans, debitor, kreditor, bankmodkonto: Finans, debitor, kreditor, Bank intern understøttes.       | Finanskladde                                                                         |
| Indgangsbog         | Konto: Kreditormodkonto: Finans intern understøttes ikke.                                                    | Kreditorfakturaregister                                                                     |
| Fakturajournal          | Konti: Kreditormodkonto: Finans intern understøttes.                                                      | Kreditorfakturakladde                                                                      |
| Kreditorfaktura           |                                                                                                                         | Kreditorfaktura                                                                          |
| Debitorfakturajournal | Konto: Debitormodkonto: Finans intern understøttes.                                                     | Finanskladde                                                                         |
| Fritekstfaktura        |                                                                                                                         | På siden **Fritekstfaktura** skal du klikke på **Åbn i Excel** (Microsoft Office-ikonet). |
| Anlægsaktivkladde     | Anlægsaktiv til finans, bank, debitor eller kreditor. Intern understøttes ikke.                                               | Anlægsaktivkladde                                                                     |
| Kreditorbetalingskladde   | Konto: Kreditormodkonto: Finans, Bank intern understøttes.                                                 | Kreditorbetalingskladde                                                                  |
| Debitorbetalingskladde | Konto: Debitormodkonto: Finans, Bank intern understøttes.                                               | Debitorbetalingskladde                                                                |
| Projektudgiftskladde  | Konto: Projekt, Finans, debitor, kreditormodkonto: Projekt, Finans, debitor, kreditor, Bank intern understøttes. | Finanskladde Udgift (i Projektstyring og regnskab)                       |

Når linjerne publiceres, valideres de for at sikre, at de overholder de regler, der er angivet i de økonomikladderne. Når linjerne er publiceret, kan brugere redigere eller bogføre bilagene fra Microsoft Dynamics 365 for Finance and Operations. 

Hvis du vil føje økonomiske dimensioner til en skabelon, kræver det yderligere ændringer. Du kan finde flere oplysninger i [Føje dimensioner til Microsoft Excel-skabelonen](../../dev-itpro/financial/add-dimensions-excel-templates.md). Når der er føjet dimensioner til enheden, er de tilgængelige i Excel-designeren og kan føjes til skabelonen.






