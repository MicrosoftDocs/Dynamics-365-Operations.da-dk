---
title: Ofte stillede spørgsmål vedrørende Økonomirapportering
description: Dette emne indeholder svar på nogle ofte stillede spørgsmål om Økonomirapportering.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266627"
---
# <a name="financial-reporting-faq"></a>Ofte stillede spørgsmål vedrørende Økonomirapportering

Dette emne indeholder svar på ofte stillede spørgsmål om Økonomirapportering.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Hvordan begrænser jeg adgangen til en rapport ved hjælp af sikkerhedstræet?

I følgende eksempel vises, hvordan du kan begrænse adgangen til en rapport ved hjælp af sikkerhedstræet.

USMF-demofirmaet indeholder rapporten **Finansbalance**, som ikke alle brugere af Økonomirapportering bør have adgang til. Du kan bruge sikkerhedstræet til at begrænse adgangen til en enkelt rapport, så kun specifikke brugere kan få adgang til rapporten.

1. Log på Financial Reporter Report Designer.
2. Vælg **Fil \> Ny \> Trædiagramdefinition** for at oprette en ny trædiagramdefinition.
3. Tryk to gange (eller dobbeltklik) på linjen **Oversigt** i kolonnen **Enhedssikkerhed**.
4. Vælg **Brugere og Grupper**.
5. Vælg de brugere eller grupper, der kræver adgang til rapporten.
6. Vælg **Gem**.
7. Tilføj den nye trædefinition i rapportdefinitionen.
8. Vælg **Indstilling** i trædefinitionen. Vælg derefter **Medtag alle enheder** under **Valg af rapporteringsenhed**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Hvordan identificerer jeg, hvilke konti der ikke svarer til mine saldi?

Når du har en rapport, der ikke har tilsvarende saldi, kan du bruge følgende procedurer til at identificere hver konto og afvigelse.

### <a name="in-financial-reporter-report-designer"></a>I Financial Reporter Report Designer

1. Opret en ny rækkedefinition.
2. Vælg **Rediger \> Indsæt rækker fra dimensioner**.
3. Vælg **MainAccount**.
4. Vælg **OK**.
5. Gem rækkedefinitionen.
6. Opret en ny kolonnedefinition.
7. Opret en ny rapportdefinition.
8. Vælg **Indstillinger**, og fjern markering af denne indstilling.
9. Opret rapporten. 
10. Eksporter rapporten til Microsoft Excel.

### <a name="in-dynamics-365-finance"></a>I Dynamics 365 Finance

1. Gå til **Finans \> Forespørgsler og rapporter \> Råbalance**.
2. Angiv følgende felter:

    - **Fra dato** – Angiv startdatoen for regnskabsåret.
    - **Til dato** – Angiv den dato, rapporten skal genereres for.
    - **Økonomisk dimension** – Angiv dette felt til **Hovedkontosæt**.

3. Vælg **Beregn**.
4. Eksporter rapporten til Excel.

Du skal nu kunne kopiere data fra Excel-rapporten i Financial Reporter til rapporten **Råbalance**, så du kan sammenligne kolonnerne **Ultimosaldo**.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Når jeg designer en rapport i Report Designer, eller når jeg opretter en økonomisk rapport, får jeg følgende meddelelse: "Operationen kunne ikke fuldføres pga. problemer i dataproviderstrukturen." Hvordan skal jeg svare?

Meddelelsen angiver, at der opstod et problem, da systemet forsøgte at hente økonomiske metadata fra datacentret, mens du brugte Økonomirapportering. Du kan løse dette problem på to måder:

- Gennemse dataintegrationsstatus ved at gå til **Værktøjer \> Integrationsstatus** i Report Designer. Hvis integrationen ikke er fuldført, skal du vente, indtil den er fuldført. Derefter skal du prøve at gentage det, du var i gang med, da du modtog meddelelsen.
- Kontakt Support for at identificere og arbejde dig gennem problemet. Der kan være uoverensstemmende data i systemet. Supportteknikere kan hjælpe dig med at identificere dette problem på serveren og finde de specifikke data, der muligvis skal opdateres.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
