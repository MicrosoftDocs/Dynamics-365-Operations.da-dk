---
title: Test af dataagnostik ved hjælp af Regression Suite Automation Tool
description: Denne artikel diskuterer anbefalingerne til test af dataagnostik ved hjælp af Regression Suite Automation Tool.
author: FrankDahl
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.custom: 21761
ms.openlocfilehash: f4322cb76d1d83c02ec9d4dcb997a1cd4730d090
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269585"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>Test af dataagnostik ved hjælp af Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

Selvom den funktionelle validering af et ERP-program ikke kan være fuldstændig dataagnostik, er der flere faser og måder for test. Disse testfaser omfatter:  

- SysTest-struktur
- ATL-struktur
- Regression Suite Automation Tool (RSAT)

[![Testklassifikationspyramide.](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>Overblik
-   **SysTest-struktur** – SysTest-strukturen er pålidelig til skrivning af enhedstest. Da enhedstest generelt tester en metode eller funktion, bør de altid være dataagnostik og kun afhænge af de inputdata, der leveres som en del af testen.
-   **ATL-struktur** – Microsoft har en ATL-struktur, der er en abstraktion i SysTest-strukturen og gør skrivning af funktionel test meget mere simpel og pålidelig. Denne struktur skal bruges til at skrive komponenttest eller simple integrationstest.
-   **RSAT** – RSAT bruges til integrationstest og test af forretningsprocesser. Forretningscyklustestene, som også kaldes regressionsvalideringstest, afhænger af eksisterende data. Disse test kan dog blive dataagnostik, hvis du overvejer yderligere faktorer. 

    - o Mens enhedstest og komponenttest er på lavt niveau og kan være fuldt dataagnostiske (ikke afhængige af eksisterende datasæt), afhænger forretningscyklussen eller regressionsvalideringstestene af nogle eksisterende data. Disse data omfatter opsætning, konfigurationsindstillinger (parametre) og masterdata (debitor, kreditorer, varer osv.), men aldrig transaktionsdata. Sørg for, at hvis en af disse ændres under testen, tilbageføres de som en del af den endelige test.
    - Vælg masterdata ud fra bestemte kriterier i stedet for at vælge en bestemt post. Hvis du f.eks. vil vælge en vare, der er baseret på dens dimensionsværdier og lagerbeholdning, skal du filtrere produktlisten med disse værdier, vælge den første vare og kopiere det nummer, der skal bruges til fremtidige test. Hvis det er en simpel masterdatalinje, f.eks. debitor, kreditor eller vare, kan den oprettes som en del af automatiseringen og bruges i fremtidige test via sammenkædning. 
    - o Angiv de entydige identifikatorer, f.eks. fakturanumre, via nummerserien eller ved at bruge Microsoft Excel-funktioner som =TEKST(NU(),"ååååmmddttmm"). Denne funktion angiver et entydigt tal hvert minut, hvilket giver dig mulighed for at spore, hvornår handlingen fandt sted. Dette kan bruges til variabler som produktkvitteringsnumre og kreditorfakturanumre. Disse test fortsætter med at arbejde på samme database igen og igen uden at kræve nogen gendannelse.
    - Indstil altid miljøets **redigeringstilstand** til **Læs** eller **Rediger** som første test, fordi standardindstillingen er **Automatisk**. **Automatisk**-indstillinger bruger altid den tidligere indstilling og kan forårsage upålidelige test. 
 
    [![Siden Indstillinger, fanen Ydeevne.](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - Valider kun, når du har filtreret på en bestemt transaktion i stedet for generisk validering. Hvis det f.eks. er antallet af poster, skal du filtrere efter transaktionsnummeret eller transaktionsdatoen, så valideringen udelukker alle andre transaktioner. 
    - Hvis du kontrollerer en debitorsaldo eller budgetkontrol, skal du gemme værdien først og derefter tilføje din transaktionsværdi for at validere det forventede resultat i stedet for at validere en fast forventet værdi. 
 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
