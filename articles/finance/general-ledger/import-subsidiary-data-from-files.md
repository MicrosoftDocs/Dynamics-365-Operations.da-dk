---
title: Importere datterselskabsdata fra filer
description: Denne artikel forklarer, hvordan du forbereder data fra eksterne systemer, så de kan importeres til Microsoft Dynamics 365 Finance.
author: jinniew
ms.date: 10/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 494f6396d5e6fab6fef9404ad473566b02b1b9ab
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780090"
---
# <a name="import-subsidiary-data-from-files"></a>Importere datterselskabsdata fra filer

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du forbereder data fra eksterne systemer, så de kan importeres til Microsoft Dynamics 365 Finance. Du kan bruge siden **Konsolider med import** (**Konsolideringer \> konsolideret med import**) til at forberede overførsel af datterselskabsdata fra eksterne systemer.

1. Oprette en juridisk datterselskabsenhed til brug i konsolideringsprocessen. Du kan finde flere oplysninger om at oprette juridiske enheder i [Oprette juridisk enhed](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Du kan finde flere oplysninger i [Forberede en juridisk enhed til brug i konsolideringsprocessen](prepare-company-for-consolidation.md) og [Konfigurere en juridisk enhed til konsolidering](set-up-subsidiary-company-for-consolidation.md).

2. Forberede en fil, der skal indeholde de data, der importeres. Yderligere oplysninger om importprocesser finder du i [Oversigt over dataimport og eksportjob](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
3. Eksportér data til en fil ved at følge trinnene i proceduren "Dataimport/eksportproces" i [Oversigt over dataimport og -eksport af job](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md). Du kan bruge denne procedure til at konsolidere data fra en anden forekomst af Dynamics 365 Finance eller fra Dynamics 365 Business Central. Hvis du importerer data fra eksterne systemer, skal data være i det format, der er beskrevet i [Eksporter datterselskabsdata til filer](export-subsidiary-data-to-file.md).
4. Gå til **Konsolideringer \> Konsolider med import**. På siden **Konsolider med import** skal du angive detaljerne om rapporten og/eller importen ved at udfylde følgende felter under fanen **Kriterium**.

| Felt                                 | Rapportens værdi | Importens værdi |
|---------------------------------------|----------------------|----------------------|
| **Betegnelse**                      | Ikke anvendelig | Angiv en beskrivelse for at identificere importen. |
| **Hovedkonto**    | Angiv det kontointerval, som rapporten skal indeholde. Hvis du ikke definerer et interval, medtages alle konti. | Angiv det kontointerval, som importen skal indeholde. Hvis du ikke definerer et interval, medtages alle konti. |
    | **Konsolideringsperiode**                  | Definer det datointerval, der skal konsolideres. | Definer det datointerval, der skal konsolideres. |
    | **Medtag faktiske beløb**                | Angiv denne indstilling til **Ja**, hvis du vil medtage faktiske beløb. | Angiv denne indstilling til **Ja**, hvis du vil medtage faktiske beløb. |
| **Medtag budgetbeløb** | Angiv denne indstilling til **Ja**, hvis du vil medtage budgetbeløb i konsolideringer. | Angiv denne indstilling til **Ja**, hvis du vil medtage budgetbeløb i konsolideringer. |
| **Gendanne saldi under konsolidering** | Angiv denne indstilling til **Ja**, hvis gendannelsesprocessen skal rydde saldoen og de nye poster helt og gendanne saldoen fra starten. | Angiv denne indstilling til **Ja**, hvis gendannelsesprocessen skal rydde saldoen og de nye poster helt og gendanne saldoen fra starten. |
| **Budgetmodeller**                         | Ikke anvendelig | Hvis du har valgt at importere budgetbeløb, skal du angive de budgetmodeller, der skal konsolideres. |
    | **Kurstype for budget**                      | Ikke anvendelig | Angiv type af en budgetvalutakurstype. |

6. Hvis du har forskellige regnskabsvalutaer, skal du bruge felterne under fanen **Valutaomregning** til at konfigurere oversættelsen, der udføres under konsolideringen.

    | Felt                      | Betegnelse |
    |----------------------------|-------------|
 | **Juridisk kildeenhed**        | Vælg den juridiske enhed, der importeres fra. |
 | **Kildens regnskabsvaluta** | Denne standardvaluta er den valuta, der er tilknyttet den juridiske kildeenhed, som du har valgt i feltet **Juridisk kildeenhed**. |
 | **Fra** og **Til konti**       | Definer det kontointerval, der skal importeres fra den juridiske kildeenhed. |
    | **Valutakurstype**         | Vælg valutakurstype. Valutakurstyper tildeles, når du opretter en hovedkonto. Du kan finde flere oplysninger i [Oprette en hovedkonto](tasks/create-main-account.md). |
| **Anvend valutakurs fra**   | Angiv en dato for at anvende den valutakurs, som var gældende på den pågældende dato. Alternativt kan du angive den værdi, der skal bruges som valutakurs. |
| **Valutakurs**  | Standardværdien afhænger af typen af valutakurs, du vælger i feltet **Valutakurstype**. Hvis du har angivet en brugerdefineret valutakurs, kan du definere en kurs. |

7. Angiv indstillingen **Kør i baggrund** til **Ja** for at aktivere importprocessen til at køre i baggrunden.
8. Angiv indstillingen **Batchafvikling** til **Ja** for at køre konsolideringen som et batchjob på et bestemt tidspunkt. Hvis konsolideringen skal køres med det samme, skal du vælge **OK**. 

De posteringer og saldi, der er angivet for konsolideringen i datterselskaberne, føjes til de relevante konti i den konsoliderede juridiske enhed.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
