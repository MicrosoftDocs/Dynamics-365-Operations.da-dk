---
title: Installation af aktiver på arbejdssteder
description: Dette emne forklarer, hvordan du installerer aktiver på arbejdssteder i Styring af aktiver
author: josaw1
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c585bce468f87a32204893ea20ce6954e92b0e38
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571800"
---
# <a name="install-assets-on-functional-locations"></a>Installation af aktiver på arbejdssteder

[!include [banner](../../includes/banner.md)]

 

Når du har oprettet strukturerne for arbejdsstederne, er det næste trin at installere aktiverne på de relevante arbejdssteder. Dette emne forklarer, hvordan du installerer aktiver på de pågældende arbejdssteder i Styring af aktiver Du kan finde flere oplysninger om, hvordan du opretter aktiver i [Aktiver](../objects/introduction-to-objects.md).

Hvis du har oprettet en aktivstruktur, skal hele aktivets struktur være installeret på et arbejdssted. Derfor kan kun overordnede aktiver (aktiver på øverste niveau, der ikke har et overordnet aktiv) vælges på et arbejdssted. Alle tilknyttede underordnede aktiver (underaktiver) bliver også installeret på arbejdsstedet. Når du installerer aktiver på et arbejdssted, bliver de økonomiske dimensioner for arbejdsstedet muligvis automatisk overført til dem, afhængigt af opsætningen af typen af det valgte arbejdssted, som er valgt for arbejdsstedet. Du finder flere oplysninger om, hvordan du konfigurerer typer af arbejdssteder i [Typer af arbejdssteder](../setup-for-functional-locations/functional-location-types.md).

> [!NOTE]
> Du kan konfigurere aktivtyper på den type af arbejdssteder, der anvendes for et arbejdssted. Når du installerer aktiver på arbejdsstedet vil der i så fald kun blive vist overordnede aktiver med samme aktivtype på listen over aktiver, der kan installeres på arbejdsstedet.

Når du har installeret aktiverne på et arbejdssted, kan du erstatte et overordnet aktiv eller en aktivstruktur efter behov. Når du installerer aktiver, skal du vælge et overordnet aktiv, der skal udskiftes. Alle tilknyttede underordnede aktiver bliver også erstattet. 


## <a name="install-an-asset-structure-on-a-functional-location"></a>Installer en aktivstruktur på et arbejdssted

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Arbejdssteder** \> **Alle arbejdssteder** eller **Aktive arbejdssteder**.
2. Vælg hvilket arbejdssted, aktivet skal installeres på.
3. Vælg **Installer aktiv**.

    I sektionen **Attributter** vises en liste over de krav til aktivattributter, der er angivet for den arbejdsstedstype, der er valgt for arbejdsstedet. Attributterne er alene til orientering. Systemet validerer ikke attributterne i forhold til de aktivattributter, der er angivet for det aktiv, du installerer. Du skal foretage denne validering, når du har valgt et aktiv i feltet **Aktiv**.

4. I feltet **Aktiv** skal du vælge hvilket overordnet aktiv, du ønsker at installere. Alle tilknyttede underordnede aktiver medtages automatisk i installationen.

    I sektionen **Aktivattributter** til højre for aktivlisten vise de aktivattributter, der er tilknyttet til det valgte aktiv.

5. I feltet **Ikrafttrædelse** skal du vælge datoen og tidspunktet for aktivinstallationens ikrafttrædelse. Efter denne dato og dette tidspunkt vil omkostningerne for aktivet og tilknyttede underaktiver være knyttet til arbejdsstedet.

    > [!NOTE]
    > De aktivattributter, der er konfigureret for aktivet, føjes til sektionen **Attributter**. Eksempelvis er kravet om attributten **Vægt** blevet tilføjet som et krav for både aktivet og arbejdsstedet. Hvis aktivet har attributkrav af samme type som arbejdsstedet, angives værdierne for aktivets attributkrav i feltet **Værdi**. Du kan derfor validere aktivværdierne i forhold til de attributkrav, der er angivet for arbejdsstedet. De attributkrav, der er angivet for arbejdsstedet, markeres.

6. Vælg **OK**.

    > [!NOTE]
    > Hvis du vil ændre installationen af et aktiv ved at installere det på et nyt arbejdssted, skal du følge trin 1 til 6 i denne procedure. Når du installerer et aktiv på at nyt arbejdssted, afinstalleres aktivet automatisk på det forrige arbejdssted. Alle aktive vedligeholdelsesanmodninger eller arbejdsordrer, der blev oprettet for aktivet, før du installerede det på et nyt arbejdssted overføres **ikke** automatisk til det nye arbejdssted. Hvis disse vedligeholdelsesanmodninger og arbejdsordrer stadig er påkrævede for aktivet, skal du manuelt oprette dem igen, når aktivet er blevet installeret på det nye arbejdssted.

7. Hvis du vil have vist en liste over alle de aktiver, herunder underaktiver, der er installeret på arbejdsstedet, skal du vælge arbejdsstedet på siden **Alle arbejdssteder** og dernæst vælge **Aktiver**.
8. Hvis du vil have vist en liste over aktive vedligeholdelsesanmodninger, aktive arbejdsordrer eller fejlregistreringer, der er relateret til de aktiver, der er installeret på et arbejdssted, skal du vælge arbejdsstedet på siden **Alle arbejdssteder** og dernæst vælge **Anmodninger**, **Arbejdsordrer**eller **Fejl**.

> [!NOTE]
> Når data relateret til aktiver ændres, opdateres de automatisk på det arbejdssted, som aktivet er installeret på. Denne automatiske opdatering vedrører ændringer af vedligeholdelsesanmodninger, arbejdsordrer, registreringer af fejl for aktiver, registreringer af vedligeholdelsesnedetid og registreringer af måling af aktiver.

## <a name="automatically-create-one-asset-on-a-functional-location"></a>Opret automatisk ét aktiv på et arbejdssted

Du kan konfigurere arbejdsstedsstadier og arbejdsstedstyper for at håndtere den automatiske oprettelse af *ét* aktiv på et arbejdssted. Aktivet får samme ID og navn som arbejdsstedet. Denne funktion kan være nyttig, hvis du håndterer vedligeholdelse på et stort, statisk aktiv, såsom en bygning.

Før du kan automatisk oprette et aktiv på et arbejdssted, skal følgende opsætningsdata være tilgængelige:

- Opret et arbejdssted for at håndtere den automatiske oprettelse af et aktiv. Vælg en aktivtype i feltet **Aktivtype**. Du kan finde flere oplysninger under [Arbejdsstedstyper](../setup-for-functional-locations/functional-location-types.md).
- Opret et livscyklustilstand for et arbejdssted for at håndtere den automatiske oprettelse af et aktiv. Angiv indstillingen **Opret aktiv** til **Ja**. Du kan finde flere oplysninger under [Livscyklustilstand for arbejdsstedstyper](../setup-for-functional-locations/functional-location-stages.md).

Når opsætningsdataene er tilgængelige, er du klar til at oprette et aktiv.

1. På siden **alle arbejdssteder** skal du sikre dig, at arbejdsstedet, hvor aktivet skal oprettes automatisk, bruger den arbejdsstedstype, som du har oprettet til dette formål.
2. Markér alle arbejdssteder på listen.
3. Vælg **Opdater arbejdsstedstilstand**, og vælg dernæst den livscyklustilstand, du har oprettet til dette formål. Et aktiv installeres nu automatisk på arbejdsstedet. Dette aktiv får samme navn som arbejdsstedet.
