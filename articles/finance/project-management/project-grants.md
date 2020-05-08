---
title: Projekttilskud
description: Dette emner beskriver, hvordan du opretter eller redigerer et tilskud.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f4f7d347dab9f02fc474656e2f4cfba8e374480d
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282818"
---
# <a name="project-grants"></a>Projekttilskud

[!include [banner](../includes/banner.md)]

Et tilskud er en pengegave til et bestemt formål eller projekt. Normalt er der begrænsninger på, hvordan et tilskud må bruges. I Projektstyring og regnskab kan du angive og spore tilskud samt definere deres relationer til projekter og projektkontrakter. Du kan f.eks. udføre følgende opgaver:

- Knyt tilskud til projekter og finansieringskilder via links til siderne **Projekt** og **Projektkontraktdetaljer**.
- Angiv og spor ændringer af et tilskud ved overgangen fra én status til en anden.
- Angiv og spor omkostninger, anmodede beløb og tildelte beløb.
- Opret mastertilskud, og tilknyt undertilskud.

Du kan oprette et tilskud ved at angive alle oplysninger i en ny post, eller du kan kopiere og redigere oplysningerne for et eksisterende tilskud og derefter opdatere dem.

## <a name="create-a-new-grant"></a>Opret et nyt tilskud

1. Gå til **Projektstyring og regnskab** \> **Tilskud** \> **Tilskud**.
2. Vælg **Nyt** \> **Tilskud**.
3. Angiv en alfanumerisk identifikator for tilskuddet i feltet **Tilskuds-id** på oversigtspanelet **Generelt** på siden med tilskudsdetaljer.
4. Angiv et navn til tilskuddet i feltet **Tilskudsnavn**.
5. Tilføj oplysninger om det nye tilskud i feltet **Beskrivelse**.

    De fleste felter på siden er valgfrie, og du kan angive så få eller så mange oplysninger, du har lyst til.

    På følgende liste beskrives de oplysninger, der er angivet i hvert oversigtspanel på siden med tilskudsdetaljer:

    - **Generelt** – Angiv tilskuddets navn, status, beskrivelse, formål og beløb.
    - **Kontaktoplysninger** – Angiv oplysninger om de medarbejdere og den afdeling, der skal administrere tilskuddet, og om den tilskudskunde eller organisation, der er tilskudskilden. Du kan også angive, om organisationen er en gennemgangsenhed, der modtager tilskuddet og derefter sender det videre til en anden modtager. Vælg **Tilføj** for at tilføje kontaktoplysninger som f.eks. telefonnummer og mailadresse for den organisation, der tildeler tilskuddet.
    - **Datoer og deadlines** – Angiv datoer relateret til tilskuddet og tilskudsansøgningen. Det kan være datoen for ansøgningsfristen, afsendelsesdatoen og den dato, hvor tilskuddet godkendes eller afvises.
    - **Tilknyttede projekter og projektkontrakter** – Du kan kun angive oplysninger i dette oversigtspanel, hvis feltet **Tilskudsstatus** i oversigtspanelet **Generelt** er angivet til **Aktiv** eller **Tildelt**. Vælg mellem følgende indstillinger for at fuldføre den relaterede opgave:

        - **Tilføj finansieringskilde** – Tilføj en ny finansieringskilde for tilskuddet. Du kan indtaste alle detaljerne nu, eller du kan bruge standardoplysningerne og opdatere dem senere.
        - **Tilføj projektkontrakt** – Tilføj eller opdater projektkontraktoplysninger.
        - **Tilføj projekt** – Tilføj eller opdater projektdetaljer.

    - **Opsætning** – Angiv detaljer om tilsvarende midler, hvis disse oplysninger kræves. Mange organisationer, som bevilger tilskud, kræver, at modtagerne bruger et vist beløb af deres egne penge eller ressourcer, som modsvarer det bevilgede beløb. I feltet **Lokalt projekt- eller sporings-id** kan du angive en identifikator, der er forskellig fra projektidentifikatoren.

        > [!NOTE]
        > Hvis en del af tilskuddet skal tildeles en anden organisation, skal du angive indstillingen **Underordnet udsteder** til **Ja**. I forbindelse med tilskud, der tildeles i USA, kan du angive, om et tilskud tildeles under statslig eller føderal bemyndigelse.

    - **Lånudbetalingsdetaljer** – Tilføj eller opdater oplysninger om, hvor ofte tilskudsmidler kan hæves, faktureres eller bruges.

## <a name="create-a-new-grant-from-a-copy"></a>Oprette et nyt tilskud ud fra en kopi

1. Gå til **Projektstyring og regnskab** \> **Tilskud** \> **Tilskud**.
2. Vælg **Nyt** \> **Kopier fra tilskud**.
3. Angiv en alfanumerisk identifikator og et navn til det nye tilskud, og vælg derefter **OK**.
4. Gennemse oplysningerne om det kopierede tilskud på siden med tilskudsdetaljer, og foretag eventuelle nødvendige ændringer. De fleste af felterne på siden er valgfrie.

## <a name="view-or-modify-grant-details"></a>Se eller redigere tilskudsoplysninger

1. Gå til **Projektstyring og regnskab** \> **Tilskud** \> **Tilskud**.
2. Vælg det tilskud, der skal redigeres.
3. Vælg **Rediger** i gruppen **Vedligehold** under fanen **Tilskud** i handlingsruden.
4. Gennemgå tilskudsoplysningerne, og foretag eventuelle nødvendige ændringer.
