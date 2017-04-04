---
title: "Indkøb og forsyning i den offentlige sektor i Frankrig"
description: "I denne artikel forklares, hvordan de standardfunktioner, der vedrører indkøb og forsyning er suppleres for franske enheder i den offentlige sektor. Disse funktioner, der bruges til at opfylde kravene i de kode des Marchés publikumsgrupper."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AgreementClassification, PurchAgreement, SysPolicy
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19891
ms.assetid: 3d3c89eb-5d6b-4d79-879b-ad6bf4bade35
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 2265af7696164d68c3bb89569bf44fc2694472da
ms.lasthandoff: 03/31/2017


---

# <a name="procurement-and-sourcing-in-the-public-sector-in-france"></a>Indkøb og forsyning i den offentlige sektor i Frankrig

I denne artikel forklares, hvordan de standardfunktioner, der vedrører indkøb og forsyning er suppleres for franske enheder i den offentlige sektor. Disse funktioner, der bruges til at opfylde kravene i de kode des Marchés publikumsgrupper. 

<a name="set-spending-thresholds-by-procurement-category"></a>Angiv forbrugsgrænser efter indkøbskategori
-----------------------------------------------

Hvis du vil angive forbrugsgrænser til køb i de indkøbskategorier, som er defineret af Clé de Contrôle ordren, kan du bruge den **forbrugsgrænser efter kategori** køb af politikreglen. Ved at implementere denne indkøbspolitik politikregel, der skal styre forbrugsgrænser efter kategori, kan du bruge ikrafttrædelsesdato attributter og estimerede udgifter beløb på tærskelbeløb til at understøtte dine indkøb praksis og til at sikre effektiv og effektiv brug af offentlige midler.

## <a name="create-tranches-and-lots"></a>Oprette trancher og partier
Hvis du vil oprette trancher og partier, kan du oprette et hierarki af overordnede og underordnede købsaftaler. Underordnede købsaftaler, der fungerer som trancher, og masser af overordnet købsaftale. Køb aftale hierarki har nogle specifikke egenskaber:

-   En bruger kan få vist overordnede købsaftalen, og kan se den samlede aktivitet i overordnet og alle relaterede underordnede aftaler er. Denne funktion giver en enkelt visning til at gennemgå og styre aktivitet på købsaftaler.
-   Nogle værdier fra den overordnede købsaftale, overføres automatisk til de underordnede aftaler. Politikker, der er relateret til konkurrencedygtige reklame kan eksempelvis tildeles til den overordnede købsaftale. Disse politikker anvendes derefter til alle underordnede aftaler, der er relateret til overordnet.
-   Købsaftaler kan have en primære kontrahent, medkontrahenter og underleverandører. Den primære kontrahent kan tildeles til den overordnede købsaftale, og kan tildeles en medkontrahent eller underleverandør til specifikke underordnede aftaler.

**Bemærk:** Hvis du har føjet linjer til en købsaftale, købsaftalen kan ikke bruges som en overordnet aftale. Den **oprette underordnede aftale** knap er ikke længere tilgængelig. Ligeledes, hvis du har oprettet en underordnet købsaftale, kan du tilføje linjer til den overordnede købsaftale. For at se relationerne mellem overordnede og underordnede købsaftaler, bruge den **køb aftale træ** side.

## <a name="set-up-purchase-agreement-access-and-limits"></a>Konfigurere grænser og køb aftale adgang
Du kan konfigurere købsaftaler, så kun godkendte afdelinger har adgang til aftalen. Du kan også begrænse det beløb, som hver afdeling kan bruge forhold til købsaftalen. Brugere, der forsøger at overstige det maksimumbeløb, der er allokeret til en afdeling, der modtager meddelelsen, og de er forhindret i at bekræfte frigivelse eller behandling af fakturaen. Før du kan bruge denne funktion, skal du angive følgende parametre den **generelle** del af den **konti Kreditorparametre** side:

-   I den **kontostruktur** skal du vælge den kontostruktur, der skal bruges på den **købe afdelingsadgang til** side til at styre adgangen til købsaftaler. Den valgte kontostruktur skal indeholde den økonomiske dimension målgruppe, som du kan bruge til at styre adgangen til købsaftaler.
-   I den **økonomiske dimension** skal du vælge den økonomiske dimension, som du kan bruge til at styre adgangen til købsaftaler. De fleste organisation bruge Afdelingsdimensionen, men nogle organisationer kan begrænse adgangen til købsaftaler til forskellige enheder i deres organisationer.

## <a name="manage-information-about-subcontractors-certifications-and-milestones-on-purchase-agreements"></a>Administrere oplysninger om underleverandører, certificeringer og milepæle på købsaftaler
Du kan oprette købsaftaleklassifikationer, føjer administrative felter til købsaftaler, der bruger klassifikationen.

-   Hvis du vil tilføje oplysninger om underleverandører til købsaftaler, Vælg den **underleverandører** indstilling på Købsaftaleklassifikation.  Købsaftaler kan have en primære kontrahent, medkontrahenter og underleverandører. Den primære kontrahent kan tildeles til den overordnede købsaftale, og kan tildeles en medkontrahent eller underleverandør til specifikke underordnede aftaler.
-   Hvis du vil tilføje oplysninger om certificeringer for kreditorer til købsaftaler, Vælg den **certificeringer** indstilling på Købsaftaleklassifikation. Certificeringsoplysninger kan bruges til at oprette en rapport, som du kan bruge til at overvåge kreditorens overholdelse af bestemte krav.
-   Hvis du vil tilføje oplysninger om milepæle og opgaver til købsaftaler, Vælg den **aktiviteter** indstilling på Købsaftaleklassifikation.

 


