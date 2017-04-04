---
title: Udgive kladdelinjer og dokumenter fra Excel
description: "Dette emne forklarer, hvordan til at skrive og udgive linjer for finanskladder fra Microsoft Excel. Den indeholder oplysninger om de forskellige skabeloner, som du kan bruge, afhængigt af typen transaktioner, som du indtaster."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 087339cb3002b42bcb985c2ccfc2d97c752a817c
ms.lasthandoff: 03/31/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Udgive kladdelinjer og dokumenter fra Excel

Dette emne forklarer, hvordan til at skrive og udgive linjer for finanskladder fra Microsoft Excel. Den indeholder oplysninger om de forskellige skabeloner, som du kan bruge, afhængigt af typen transaktioner, som du indtaster.

Brugere kan skrive og udgive linjer for økonomikladder fra Microsoft Excel. Når en bruger opretter en kladde, den **åbne linjer i Excel** knap viser de skabeloner, der er tilgængelige. Skabeloner er udviklet til at understøtte specifikke scenarier, men ikke alle kombinationen af kontotype understøttes i kladden. Følgende tabel viser de skabeloner, der er tilgængelige, og de kontotyper, som de understøtter.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Template**             | **Understøttede kontotyper**                                                                                             | **Hvordan du kan få adgang til skabelonen**                                                          |
| Finansjournallinjer     | Konto: Finans, debitor, kreditor, Bank forskydning konto: Finans, debitor, kreditor, Bank interne understøttes.       | Finanskladde                                                                         |
| Indgangsbog         | Konto: Leverandør modkonto: Finans interne understøttes ikke.                                                    | AP fakturere register                                                                     |
| Fakturajournal          | Konti: Leverandør modkonto: Finans interne understøttes.                                                      | Kreditorfakturakladde                                                                      |
| Kreditorfaktura           |                                                                                                                         | Kreditorfaktura                                                                          |
| Debitorfakturajournal | Konto: Kunden modkonto: Finans interne understøttes.                                                     | Finanskladde                                                                         |
| Fritekstfaktura        |                                                                                                                         | På den **fritekstfaktura** skal du klikke på **Åbn i Excel** (Microsoft Office-ikonet). |
| Anlægsaktivkladde     | Anlægsaktiver til Finans, bank, debitor eller kreditor. Interne understøttes ikke.                                               | Anlægsaktivkladde                                                                     |
| Kreditorbetalingskladde   | Konto: Leverandør modkonto: Finans, Bank interne understøttes.                                                 | Kreditorbetalingskladde                                                                  |
| Debitorbetalingskladde | Konto: Kunden modkonto: Finans, Bank interne understøttes.                                               | Debitorbetalingskladde                                                                |
| Projektudgiftskladde  | Konto: Projekt, Finans, debitor, kreditor forskydning konto: projekt, Finans, debitor, kreditor interne understøttes. | Finanskladde Udgift (i Projektstyring og regnskab)                       |

Når linjerne er udgivet valideres de for at sikre, at de overholder de regler, der er angivet i de økonomikladder. Når linjerne er udgivet, kan brugere redigere eller bogføre bilaget fra Microsoft Dynamics 365 for operationer. 

Hvis du vil tilføje en skabelon økonomiske dimensioner, kræves yderligere ændringer. Yderligere oplysninger finder du under [føje dimensioner til Microsoft Excel-skabelonen](\dev-itpro\financial-dimensions\add-dimensions-excel-templates). Når dimensioner er føjet til enheden, de er tilgængelige i Excel designer og kan føjes til skabelonen.




