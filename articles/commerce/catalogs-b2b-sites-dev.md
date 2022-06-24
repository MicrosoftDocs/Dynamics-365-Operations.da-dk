---
title: Udvidet virkning af Commerce-kataloger til B2B-tilpasninger
description: Denne artikel beskriver udvidelsespåvirkning af funktionen Commerce-kataloger til B2B-funktion i Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: f21d3375db69dd412325d00261bfc18e26d0c257
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849009"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>Udvidet virkning af Commerce-kataloger til B2B-tilpasninger

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikel beskriver udvidelsespåvirkning af funktionen **Commerce-kataloger til B2B**-funktion i Microsoft Dynamics 365 Commerce.

Hvis du er interesseret i at udvide katalogkonteksten til tilpassede scenarier, skal tilpasningerne måske opdateres. Denne opdatering følger den standardproces, som kunder skal følge, da tilpasningerne muligvis ikke automatisk understøtter de seneste funktioner, efter opgraderingerne er udført. Hvis tilpasningerne inkluderer nye funktioner eller rettelser i deres erfaringer, anbefales det, at du opdaterer tilpasningskoden tilsvarende. Denne opdatering svarer til de ændringer, Microsoft kan have foretaget for kernekoden.

Gennemse de tilpasningssager, der følger for at finde ud af, om tilpasningerne skal opdateres.

> [!NOTE]
> - Alle markedsførings-API'er (Application Programming Interfaces) skal være katalogbaserede. Det er derfor vigtigt, at du sender parameteren **CatalogID**.
> - Standardkataloget (**CatalogID**=**0**) er ikke et gyldigt katalog for signerede B2B-brugere (business-to-business). Derfor vil alle API-kald, der sender "0", eller som bruger en standardværdi, mislykkes, fordi webstedsbrugeren ikke har adgang til katalog 0. For at få den korrekte erfaring skal kunde-API-kald opdateres, så de sender det katalog-id, der blev valgt i katalogplukkeren. Hvis du bruger en standardværdi, og brugeren ændrer kataloger, skal webstedet indeholde dataene til det valgte katalog. Så tilpassede API'er skal bestå det valgte katalog, så de svarer til de API'er, der køres fra kernehandelskoden.

Følgende tilpasningssager kræver udviklingsopdateringer:

- **Eksempel 1:** En kunde introducerer sin egen [datahandling,](e-commerce-extensibility/data-actions.md), der kalder en produktrelateret API eller datahandling. De følgende opdateringstrin er obligatoriske:

    1. Hvis datahandlingen bruger et direkte API-kald, skal du opdatere datahandlingen, så den sender katalog-id'et, som vist i følgende illustration af eksemplet nedenfor.

        ![Den opdaterede datahandling, der sender katalog-id'et.](./media/customization1_a.png)

    1. Hvis datahandlingen kalder en anden produktrelateret datahandling inde i tilpasningen, skal koden opdateres, så den sender nogle nye parametre, f.eks. **requestContext**. Parameteren **requestContext** bruges til at hente det aktuelle katalog-id, som vist i følgende illustration af eksemplet.

        ![Den opdaterede datahandling, der sender den nye parameter.](./media/customization1_b.png)

- **Eksempel 2:** En kunde har en [overskrevet datahandling](e-commerce-extensibility/data-action-overrides.md). De følgende opdateringstrin er obligatorisk:

    - Opdater datahandlingen som for Eksempel 1.

- **Eksempel 3:** En kunde har en visningsudvidelse, script-injektormodul eller [klonet modul](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module), der indeholder opkald til API'er eller datahandlinger. De følgende opdateringstrin er obligatorisk:

    - Opdater koden for Eksempel 1, som vist i følgende eksempelillustration.

       ![Den opdaterede kode, der sender den nye parameter.](./media/customization3.png)

- **Eksempel 4:** En kunde bruger et **getById** API-kald. De følgende opdateringstrin er obligatorisk:

    - Skift til **getByIds** API-opkaldet i stedet, fordi **getById** APT-opkaldet har visse begrænsninger og ikke understøtter katalog bevågenhed.

- **Eksempel 5:** En kunde har en datahandling, der henter oplysninger om flere produkter, der kan være fra forskellige kataloger. De følgende opdateringstrin er obligatorisk:

    - Opdel API-opkaldene efter katalog-id. I forbindelse med API'er til indkøbsvogn kan indkøbsvognen f.eks. indeholde produkter fra forskellige kataloger. Produktlinjerne skal grupperes efter katalog-id, og de skal kalde API'en for hvert katalog separat som vist i følgende illustration af eksemplet.

        ![Opdateret datahandling, der grupperer produktlinjer efter katalog-id.](./media/customization5.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette handelskataloger til B2B-websteder](catalogs-b2b-sites.md)

[Handelskataloger for B2B Ofte stillede spørgsmål](catalogs-b2b-sites-FAQ.md)
