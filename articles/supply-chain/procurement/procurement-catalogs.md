---
title: "Indkøbskataloger"
description: "I denne artikel beskrives på et højt niveau, hvor indkøbsmedarbejderne kan konfigurere og vedligeholde indkøbskataloger. Indkøbskataloger definerer de varer og tjenesteydelser, som virksomhedens medarbejdere kan bestille til intern brug."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b94ecf3e173a2a7ce649170b6eff1e16f2626074
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---

# <a name="procurement-catalogs"></a>Indkøbskataloger

[!include[banner](../includes/banner.md)]


I denne artikel beskrives på et højt niveau, hvor indkøbsmedarbejderne kan konfigurere og vedligeholde indkøbskataloger. Indkøbskataloger definerer de varer og tjenesteydelser, som virksomhedens medarbejdere kan bestille til intern brug.

I Køb kan indkøbsmedarbejderne oprette og vedligeholde kataloger over varer og tjenesteydelser, der kan købes, til intern brug i en organisation. Når der er oprettet kataloger, kan virksomhedens medarbejdere oprette indkøbsrekvisitioner, der kan bestilles fra dem. Katalogerne kan bruges til at gennemtvinge indkøbspolitikker, så medarbejderne kun kan bestille de varer og tjenester, der er tilladt for deres juridiske indkøbsenhed. Når du opretter et indkøbskatalog, skal du overveje følgende opgaver:

-   Konfigurer dit indkøbskategorihierarki, før du opretter kataloget.
-   Bestem, hvilke produkter dine medarbejdere skal kunne bestille. Du kan vise eller skjule bestemte produkter i en katalognode, eller du kan vise eller skjule alle produkter i en node.
-   Bestem, hvor mange indkøbskataloger der er brug for. Den katalogpolitikregel, som du konfigurerer for den juridiske enhed og den driftsenhed, som medarbejderen er tilknyttet, bestemmer, om medarbejderen kan få adgang til et indkøbskatalog eller ej.

Flere faktorer bestemmer, hvilke produkter medarbejdere kan bestille, og hvilke indkøbskategorier de kan bruge, når de opretter indkøbsrekvisitioner:

-   Kategoriadgangspolitikreglen i indkøbspolitikken bestemmer, hvilke indkøbskategorier der er tilgængelige i indkøbsrekvisitionen. Hvis der ikke er defineret nogen regler, er alle indkøbskategorier tilgængelige.
-   Medarbejdere kan kun bestille et produkt, hvis det er i det aktive indkøbskatalog for din organisation, og hvis det er i en aktiveret node og ikke skjult. Produktet skal også være i en kategori, som en bestemt medarbejder har adgang til i henhold til kategoriadgangspolitikreglen.
-   Katalogpolitikreglen angiver det katalog, der bruges. Hvis der ikke er defineret en katalogpolitikregel, bestemmer kategoriadgangsreglen alene, hvilke produkter en medarbejder kan bestille på rekvisitionen.

## <a name="prerequisites"></a>Forudsætninger
Tabellen nedenfor beskriver de opgaver, der skal fuldføres, før en indkøbsmedarbejder kan oprette et indkøbskatalog:

| Opgave                                                | Rolle               | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfigurer et indkøbskategorihierarki.            | Indkøbschef | Indkøbskategorihierarkier klassificerer varer eller transaktioner til rapporterings- og analyseformål. Ved at bruge et indkøbskategorihierarki kan virksomheder strategisk styre kategorier, produkter, leverandører og andre indkøbsfaktorer fra ét centralt sted. Der defineres ét indkøbskategorihierarki for en hel organisation. Kataloget er baseret på indkøbskategorihierarkiet: Kategorier i hierarkiet bliver noder i kataloget. Leverandører og produkter, der er medtaget i kataloget. |
| Føj leverandører og produkter til indkøbskategorier. | Indkøbschef | Når indkøbskategorihierarkiet oprettes for organisationen, kan hver enkelt indkøbskategori knyttes til bestemte leverandører, produkter osv. Disse tilknytninger kopieres automatisk til kataloget.                                                                                                                                                                                                                                                                                           |

## <a name="setting-up-a-catalog"></a>Oprette et katalog
Når forudsætningerne er opfyldt, kan du oprette kataloger. Du kan enten oprette et enkelt katalog, der bruges i hele organisationen, eller flere kataloger, som de forskellige afdelinger i organisationen bruger. Hvis du opretter et enkelt katalog til hele organisationen, styres adgang til kataloget af dine indkøbspolitikregler.  

Kataloget definerer, hvilke produkter der er tilgængelige, når der oprettes indkøbsrekvisitionslinjer, men du kan bruge kategoriadgangspolitikregler til at anvende yderligere begrænsninger. Da noderne i et katalog er indkøbskategorier, kan de tilsidesættes af en kategoriadgangspolitikregel I dette tilfælde er produkterne i denne kategori ikke tilgængelige for medarbejdere til brug i rekvisitioner. Du kan definere adgangspolitikregler på siden **Indkøbspolitikker**. Følgende tabel beskriver de opgaver, der skal udføres, før du kan oprette et katalog.

| Opgave                                                   | Rolle             | Beskrivelse                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Opret et nyt katalog.                                  | Indkøbsassistent | Når du opretter et katalog, skal du angive katalogets navn og en beskrivelse af kataloget. Du kan også angive, om kataloget skal opdateres manuelt eller automatisk, og du kan angive katalogets ejer.                                                                                                                                      |
| Kontrollér, om produkterne findes i kataloget. | Indkøbsassistent | Da produkterne er nedarvet fra indkøbskategorierne, vises de alle i de relevante katalognoder. Du kan kontrollere, om alle produkter i en node, er skjult eller vises, når kataloget bruges i en indkøbsrekvisition. Du kan også kontrollere, om individuelle produkter i en node er skjult eller vises. |
| Udgiv kataloget.                                   | Indkøbsassistent | Inden et katalog bliver tilgængeligt for medarbejderne, så de kan bruges i en indkøbsrekvisition, skal du angive en politikregel for kataloget, angive katalogets status som **Aktiv** og derefter udgive kataloget. Du kan deaktivere kataloger, som ikke længere skal kunne benyttes af dine brugere.                                              |

Opdateringer publiceres enten automatisk eller manuelt, afhængigt af de indstillinger du vælge for kataloget i feltet **Standardopdateringstype** på siden **Kataloger**. Der findes følgende standardopdateringstyper for kataloger:

-   **Dynamisk** – Katalogerne opdateres automatisk, når der foretages ændringer.
-   **Statisk** – Katalogerne skal opdateres manuelt.
-   **Begge** – Hvis kataloget indeholder produktkategorier, som har standardopdateringstypen **Statisk**, skal det opdateres, når disse kategorier opdateres. Hvis kataloget indeholder produktkategorier, der har standardopdateringstypen **Dynamisk**, opdateres det automatisk, når det ændres.


<a name="see-also"></a>Se også
--------

[Konfigurer et indkøbskategorihierarki (opgaveguide)](/dynamics365/unified-operations/supply-chain/procurement/tasks/set-up-procurement-category-hierarchy)



