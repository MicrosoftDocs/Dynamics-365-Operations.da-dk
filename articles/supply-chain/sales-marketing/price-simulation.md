---
title: Prissimulering
description: Denne artikel indeholder oplysninger om prissimuleringen for tilbud. Prissimuleringen hjælper dig med at vurdere effekten af fradrag på den fremtidige salgspris under tilbudsprocessen, før du giver tilsagn om en bestemt pris.
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationPriceSimulation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe8c4bc8f2efb06de4cb6fd727df93ba1a5d14bf
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251333"
---
# <a name="price-simulation"></a>Prissimulering

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om prissimuleringen for tilbud. Prissimuleringen hjælper dig med at vurdere effekten af fradrag på den fremtidige salgspris under tilbudsprocessen, før du giver tilsagn om en bestemt pris.

En prissimulering til et tilbud viser et nyt samlet beløb på basis af en foreslået ny pris. En prissimulering kan også vise et nyt beløb for en bestemt linje, der er oprettet i et eksisterende tilbud. Du kan angive en prissimulering og anvende den senere. Du kan også bruge det oprindelige tilbud – uden en prissimulering – og ændre mere, efterhånden som du arbejder dig gennem salgsprocessen med kunden.  

En prissimulering ændrer ikke prisen i tilbuddet. Hvis prissimuleringen anvendes på et helt tilbud, behandles den som en specialrabat i tilbudshovedet. Hvis prissimuleringen anvendes på bestemte varer, behandles den som en specialrabat på tilbudslinjerne. Enhedssalgsprisen på en tilbudslinje, der oprettes, ændres ikke, når prissimuleringen anvendes. I stedet anvendes en rabatprocent, der svarer til prisreduktionen på tilbudslinjen. Når en prissimulering anvendes, overføres enhedssalgsprisen og rabatprocenten til tilbudslinjen eller tilbudshovedet.  

>[Bemærk!] Når du kører en prissimulering, er det kun den aktuelle salgsvaluta, der bruges til oprettelse af simuleringen. Men når du får vist de samlede tilbudsbeløb, er det med en blanding af regnskabsvalutaen og salgsvalutaen.  

Ekstra varer, der føjes til tilbudslinjer, kan udløse linjerabatter eller samkøbsrabatter. De kan også udløse samlede rabatter, der ændrer dækningsbidrag og dækningsgrader for tilbudslinjerne og den samlede rabat.  

Du kan køre flere prissimuleringer for at spore effekten af prisjusteringer på målene for et tilbud. Hvis du kører disse simuleringer, kan du justere den samlede tilbudspris eller prisen på en eller flere specifikke linjer i tilbuddet og derefter anvende den prissimulering, der med størst sandsynlighed vil få handelen i hus.  

Du kan oprette en påmindelse, når du opretter et tilbud. Her er nogle af de måder, hvorpå påmindelser anvendes:

-   De kan holde dig informeret om status på tilbud i firmaet.
-   De kan udløse en gennemgang af et bestemt tilbud eller give dig besked, hvis rabatgrænserne overskrides.

## <a name="price-simulation-and-discounts"></a>Prissimulering og rabatter
Det er vigtigt at være omhyggelig, når du kører prissimuleringer på tilbud med rabatter, så du er sikker på, at rabatter og priser beregnes korrekt. Eftersom alle prissimuleringer behandles som specielle rabatter på den aktive tilbudslinje eller i hele tilbuddet, skal du spore afvigelserne i rabatterne.

### <a name="types-of-discounts-in-trade-agreements"></a>Typer af rabatter i samhandelsaftaler

Samhandelsaftaler i Supply Chain Management kan have fire typer af prisrabatter. Disse rabatter kan oprettes til forskellige varer, kunder eller prisgrupper, og de kan begrænses med angivelse af en dato. Du skal tage højde for samhandelsaftaler ved kørsel af prissimuleringer for at undgå forkerte beregninger. Her er fire rabattyper, der kan anvendes i samhandelsaftaler:

-   **Salgspris** – Der kan angives separate varesalgspriser. Når tilbudslinjerne oprettes, søger programmet efter den rigtige salgspris for en vare og overføre den til tilbudslinjerne. En samhandelsaftale, der har denne slags rabat, påvirker derfor ikke prissimuleringen. Den salgspris, der bruges i tilbudslinjen, afspejler samhandelsaftalen.
-   **Linjerabat** – Der angives særlige rabatter for varer, afhængigt af ordreantallet. Linjebeløb reduceres typisk med linjerabatten, før der køres en prissimulering. En samhandelsaftale, der har denne slags rabat, påvirker derfor prissimuleringen.
-   **Samkøbsrabat** – Hvis de kombinerede mængder overskrider den angivne grænse, udløser foruddefinerede varekombinationer i ordren en rabat på den samlede ordre. Linjebeløb reduceres typisk med linjerabatten, før der køres en prissimulering. En samhandelsaftale, der har denne slags rabat, påvirker derfor prissimuleringen.
-   **Slutrabat** – Hvis de kombinerede beløb overskrider den angivne grænse, udløser foruddefinerede bestilte varer en rabat på den samlede ordre. Slutrabatten genereres af tilbudslinjerne. Da slutrabatten dog anvendes på det samlede tilbud som en rabat, reduceres det samlede tilbudsbeløb. En samhandelsaftale, der har denne slags rabat, påvirker derfor prissimuleringen.

### <a name="quotation-lines-and-trade-agreements"></a>Tilbudslinjer og samhandelsaftaler

Når du opretter eller regulerer en tilbudslinje, beregnes der automatisk linjerabatter. Den relevante salgspris for varen findes i overensstemmelse med samhandelsaftalen.

## <a name="price-simulation-examples"></a>Eksempler på prissimulering
I eksemplerne nedenfor bruges der prissimulering til tilbudshoveder og enkelte linjeelementer.

### <a name="price-simulation-for-quotation-headers"></a>Prissimulering for tilbudshoveder

Du kan oprette et tilbud med følgende linjer:

-   10 stk. BR-12 (kostpris pr. stk.: USD 9,52, salgspris pr. stk.: USD 15,32)
-   12 stk. BR-14 (kostpris pr. stk.: USD 7,48, salgspris pr. stk.: USD 13,75)

I følgende tabel vises tilbudslinjerne.

|                            | Kalkulation                          | Resultat   |
|----------------------------|--------------------------------------|----------|
| Salgsantal             | 10 stk. + 12 stk.                  | 22 stk. |
| Salgsværdi i USD         | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Kostværdi i USD          | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Dækningsbidrag i USD | 318,20 – 184,96                      | 133,24   |
| Dækningsgrad         | (\[318,20 – 184,96\] ÷ 318,20) × 100 | 41,87 %   |

Du kører en prissimulering og yder en samlet rabat på 15 procent på hele tilbuddet eller tilbudshovedet. I følgende tabel vises de nye samlede beløb for tilbuddet efter kørsel af prissimuleringen.

|                                                      | Kalkulation                               | Resultat   |
|------------------------------------------------------|-------------------------------------------|----------|
| Salgsantal                                       | 10 stk. + 12 stk.                       | 22 stk. |
| Oprindelig salgsværdi i USD                               | (10 × 15,32) + (12 × 13,75)               | 318,20   |
| Oprindelig kostværdi i USD                                | (10 × 9,52) + (12 × 7,48)                 | 184,96   |
| Oprindeligt dækningsbidrag i USD                       | 318,20 – 184,96                           | 133,24   |
| Oprindelig dækningsgrad                               | (\[318,20 – (10 × 9,52)\] ÷ 318,20) × 100 | 41,87 %   |
| Prissimulering med 15 % samlet rabat i USD | (15 × 318,2) ÷ 100                        | 47,73    |
| Ny salgsværdi i USD                               | 318,20 – 47,73                            | 270,47   |
| Nyt dækningsbidrag i USD                       | 270,47 – 184,96                           | 85,51    |
| Ny dækningsgrad                               | \[(270,47 – 184,96) ÷ 270,47\] × 100      | 31,61 %   |

### <a name="price-simulation-for-single-line-items"></a>Prissimulering for enkelte linjeelementer

Du kan oprette et tilbud med følgende linjer:

-   10 stk. BR-12 (kostpris pr. stk.: USD 9,52, salgspris pr. stk.: USD 15,32)
-   12 stk. BR-14 (kostpris pr. stk.: USD 7,48, salgspris pr. stk.: USD 13,75)

I følgende tabel vises tilbudslinjerne.

|                                      | Kalkulation                          | Resultat   |
|--------------------------------------|--------------------------------------|----------|
| Salgsantal                       | 10 stk. + 12 stk.                  | 22 stk. |
| Salgsværdi i USD for BR-12         | 10 × 15,32                           | 153,20   |
| Salgsværdi i USD for BR-14         | 12 × 13,75                           | 165,00   |
| Kostværdi i USD for BR-12          | 10 × 9,52                            | 95,20    |
| Kostværdi i USD for BR-14          | 12 × 7,48                            | 89,76    |
| Dækningsbidrag i USD for BR-12 | 153,20 – 95,20                       | 58,00    |
| Dækningsbidrag i USD for BR-14 | 165,00 – 89,76                       | 75,24    |
| Dækningsgrad i USD for BR-12  | \[(153,20 – 95,20) ÷ 153,20\] × 100  | 37,86    |
| Dækningsgrad i USD for BR-14  | \[(165,00 – 89,76) ÷ 165,00\] × 100  | 45,60    |
| Samlet salgsværdi i USD             | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Samlet kostværdi i USD              | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Samlet dækningsbidrag i USD     | 318,20 – 184,96                      | 133,24   |
| Samlet dækningsgrad             | \[(318,20 – 184,96) ÷ 318,20\] × 100 | 41,87 %   |

Du kører en prissimulering og yder en samlet rabat på 10 procent på BR-12-enheder. I følgende tabel vises de nye samlede beløb for tilbuddet efter kørsel af prissimuleringen for det enkelte linjeelement.

|                                                   | Kalkulation                             | Resultat   |
|---------------------------------------------------|-----------------------------------------|----------|
| Salgsantal                                    | 10 stk. + 12 stk.                     | 22 stk. |
| Oprindelig salgsværdi i USD for BR-12                  | 10 × 15,32                              | 153,20   |
| Prissimulering med 10 % rabat på BR-12 | (10 × 153,2) ÷ 100                      | 15,32    |
| Ny salgsværdi i USD for BR-12                  | (10 × 15,32) – 15,32                    | 137,88   |
| Salgsværdi i USD for BR-14                      | 12 × 13,75                              | 165,00   |
| Kostværdi i USD for BR-12                       | 10 × 9,52                               | 95,20    |
| Kostværdi i USD for BR-14                       | 12 × 7,48                               | 89,76    |
| Nyt dækningsbidrag i USD for BR-12          | 137,88 – 95,20                          | 42,68    |
| Dækningsbidrag i USD for BR-14              | 165,00 – 89,76                          | 75,24    |
| Ny dækningsgrad i USD for BR-12           | \[(137,88 – 95,20) ÷ 137,88\] × 100     | 30,95    |
| Dækningsgrad i USD for BR-14               | \[(165,00 – 89,76) ÷ 165,00\] × 100     | 45,60    |
| Ny samlet salgsværdi i USD                      | \[(10 × 15,32) – 15,32\] + (12 × 13,75) | 302,88   |
| Samlet kostværdi i USD                           | (10 × 9,52) + (12 × 7,48)               | 184,96   |
| Nyt samlet dækningsbidrag i USD              | 302,88 – 184,96                         | 117,92   |
| Ny samlet dækningsgrad                      | \[(302,88 – 184,96) ÷ 302,88\] × 100    | 38,93 %   |

Prissimuleringen påvirker kun den linje, den anvendes på, og reducerer det samlede beløb for den linje.



