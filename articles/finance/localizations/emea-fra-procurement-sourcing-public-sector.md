---
title: Indkøb og forsyning i den offentlige sektor i Frankrig
description: I denne artikel forklares, hvordan de standardfunktioner, der vedrører indkøb og forsyning, suppleres for franske enheder i den offentlige sektor. Disse funktioner bruges til at opfylde kravene i Code des Marchés Publics.
author: brpotter
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: France
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 19891
ms.search.industry: Public sector
ms.search.form: AgreementClassification, PurchAgreement, SysPolicy
ms.openlocfilehash: 2d3f29afd295321af19b4221b2ca65e7c760dd44
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285758"
---
# <a name="procurement-and-sourcing-in-the-public-sector-in-france"></a>Indkøb og forsyning i den offentlige sektor i Frankrig

[!include [banner](../includes/banner.md)]

I denne artikel forklares, hvordan de standardfunktioner, der vedrører indkøb og forsyning, suppleres for franske enheder i den offentlige sektor. Disse funktioner bruges til at opfylde kravene i Code des Marchés Publics. 

## <a name="set-spending-thresholds-by-procurement-category"></a>Angive forbrugsgrænser efter indkøbskategori

Hvis du vil angive forbrugsgrænser for køb i de indkøbskategorier, som er defineret af Clé de Contrôle Marché, skal du bruge indkøbspolitikreglen **Forbrugsgrænser efter kategori**. Når du implementerer denne indkøbspolitikregel til styring af forbrugsgrænser efter kategori, kan du bruge attributter for ikrafttrædelsesdato, estimerede udgiftsbeløb og tærskelbeløb til at understøtte din indkøbspraksis og til at sikre effektiv brug af offentlige midler.

## <a name="create-tranches-and-lots"></a>Oprette trancher og partier
Hvis du vil oprette trancher og partier, skal du oprette et hierarki af overordnede og underordnede købsaftaler. De underordnede købsaftaler fungerer som trancher og parti for den overordnende købsaftale. Købsaftalehierarkiet har nogle specifikke egenskaber:

-   En bruger kan få vist den overordnede købsaftale og kan se den samlede aktivitet i den overordnede aftale og alle relaterede underordnede aftaler. Denne funktion giver en enkel administrationsvisning til gennemgang og styring af aktivitet i købsaftaler.
-   Nogle værdier fra den overordnede købsaftale overføres automatisk til de underordnede aftaler. Politikker, der er relateret til konkurrencedygtige reklame, kan eksempelvis tildeles til den overordnede købsaftale. Disse politikker anvendes derefter på alle underordnede aftaler, der er relateret til den overordnede.
-   Købsaftaler kan have en primær kontrahent, medkontrahenter og underleverandører. Den primære kontrahent kan tildeles til den overordnede købsaftale og en medkontrahent eller underleverandør kan tildeles til specifikke underordnede aftaler.

**Bemærk**! Hvis du har tilføjet linjer i en købsaftale, kan denne købsaftale ikke bruges som en overordnet aftale. Og knappen **Opret underordnet aftale** er ikke længere tilgængelig. Ligeledes, hvis du har oprettet en underordnet købsaftale, kan du ikke tilføje linjer i den overordnede købsaftale. Du kan se relationerne mellem overordnede og underordnede købsaftaler på siden **Købsaftaletræ**.

## <a name="set-up-purchase-agreement-access-and-limits"></a>Konfigurere grænser og adgang for købsaftaler
Du kan konfigurere købsaftaler, så kun godkendte afdelinger har adgang til aftalen. Du kan også begrænse det beløb, som hver afdeling kan bruge forhold til købsaftalen. Brugere, der forsøger at overstige det maksimumbeløb, der er allokeret til en afdeling, modtager en meddelelse, og de forhindres i at bekræfte frigivelsen eller behandle fakturaen. Før du kan bruge denne funktion, skal du angive følgende parametre i afsnittet **Generelt** på siden **Kreditorparametre**:

-   I feltet **Kontostruktur** skal du vælge den kontostruktur, du vil bruge på siden **Afdelingsadgang til købsaftaler**, for at styre adgangen til købsaftaler. Kontostrukturen skal indeholde det økonomiske dimensionssegment, som du bruger til at styre adgangen til købsaftaler.
-   I feltet **Økonomisk dimension** skal du vælge den økonomiske dimension, som du bruger til at styre adgangen til købsaftaler. De fleste organisationer bruger afdelingsdimensionen, men i visse organisationer kan adgangen til købsaftaler være begrænset til forskellige enheder i organisationen.

## <a name="manage-information-about-subcontractors-certifications-and-milestones-on-purchase-agreements"></a>Administrere oplysninger om underleverandører, certificeringer og milepæle i købsaftaler
Du kan oprette købsaftaleklassifikationer, der føjer administrative felter til købsaftaler, der bruger klassifikationen.

-   Hvis du vil føje oplysninger om underleverandører til købsaftaler, skal du vælge indstillingen **Underleverandører** i købsaftaleklassifikationen.  Købsaftaler kan have en primær kontrahent, medkontrahenter og underleverandører. Den primære kontrahent kan tildeles til den overordnede købsaftale og en medkontrahent eller underleverandør kan tildeles til specifikke underordnede aftaler.
-   Hvis du vil føje oplysninger om certificeringer for leverandører til købsaftaler, skal du vælge indstillingen **Certificeringer** i købsaftaleklassifikationen. Certificeringsoplysninger kan bruges til at oprette en rapport, som du kan bruge til at overvåge kreditorens overholdelse af bestemte krav.
-   Hvis du vil føje oplysninger om milepæle og opgaver til købsaftaler, skal du vælge indstillingen **Aktiviteter** i købsaftaleklassifikationen.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
