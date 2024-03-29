---
title: Konfigurere delte parametre
description: I denne artikel beskrives det, hvordan du kan bruge personaleparametre på tværs af juridiske enheder.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c0d8dbca302d90cc402feb4715a6fcc2b935d8b1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906176"
---
# <a name="configure-shared-parameters"></a>Konfigurere delte parametre

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du skal konfigurere delte parametre for poster, der deles på tværs af virksomheder, herunder **Stilling**-poster. I denne artikel beskrives det, hvordan du kan bruge personaleparametre på tværs af juridiske enheder.

Visse typer poster, f.eks. **Stilling**-poster, deles på tværs af firmaer. Du skal konfigurere delte parametre for disse poster. Du kan f.eks. bruge siden **Delte parametre for personale** for at konfigurere personaleparametre på tværs af juridiske enheder. 

På siden **Delte parametre for personale** er parametrene grupperet i områder, baseret på deres funktionalitet. 

### <a name="settings"></a>Indstillinger
På fanen **Identifikation** skal du vælge de identifikationstyper, der repræsenterer de identifikationsnumre, der er angivet på siden. Før du kan angive identifikationsoplysninger om arbejderne, skal du konfigurere identifikationstyper. Oplysninger om CPR-nummer, nationalt id-nummer, ID for udlænding og personlige id-kode vedligeholdes på siden **Identifikationstype**. Hvis du vil definere en ny identifikationstype eller gennemse listen over eksisterende typer, skal du gå til **Personalestyring** &gt; **Links** &gt; **Konfiguration** &gt; **Identifikationstyper**. Du kan indtaste en simpel kode og beskrivelse. 

Under fanen **Nummerserier** kan du vælge den nummerserie, der bruges til følgende poster: **Personalenummer**, **Stilling**, **Id for brugeranmodning**, **I-9-dokument**, **Ansøger**, **Diskussion**, **Frynsegode-id** og **Personalehandling** (hvis denne posttype er aktiveret). Brug listesiden **Nummerserier**, hvis du vil vedligeholde nummerseriereferencer og -koder. Brug sidesøgefunktionen for at finde denne side. 

På fanen **Stillinger** skal du angive, om nye stillinger er tilgængelige for tildeling som standard:

- **Altid** – Du kan tildele arbejdere til nye stillinger, når stillingerne oprettes. Når der oprettes stillinger, angives dato og klokkeslæt for **Tilgængelig for tildeling** under fanen **Generelt** på siden **Stilling** automatisk til oprettelsesdatoen og -klokkeslættet.
- **Aldrig** – Du kan ikke tildele arbejdere til nye stillinger, når stillingerne oprettes. Hvis du vælger denne indstilling, skal du åbne siden **Stilling** for hver ny stilling, efterhånden som den bliver tilgængelig. Derefter skal du gå til fanen **Generelt** og angive datoen **Tilgængelig for tildeling** for at aktivere arbejdertildeling.

Du kan begrænse adgangen til visse oplysninger eller links under fanen **Avanceret adgang**:

- **Begræns adgang til arbejderoplysninger** – Vælg denne funktion, hvis brugere kun skal kunne se medarbejderoplysninger for de juridiske enheder, som de har adgang til, og for medarbejdere, der er ansat i disse juridiske enheder.

    Når denne funktion er valgt, skal du benytte følgende fremgangsmåde for at angive de rette rettigheder for hver af de brugere, hvis visning skal begrænses:

    1. Vælg en bruger på siden **Brugere**.
    1. Vælg en rolle for brugeren. Indstillingen **Tildel organisationer** bliver tilgængelig.
    1. Vælg **Tildel organisationer**.
    1. Vælg **Giv adgang til bestemte organisationer enkeltvis** på den nye side, og vælg derefter de organisationer, som brugeren skal have adgang til.
    1. Gentag trin 2 til 4 for alle andre roller, brugeren har, herunder systembrugerrollen.

    > [!NOTE]
    > De regnskaber, som en bruger har adgang til, skal matche på tværs af alle brugerens roller.

- **Aktiver Visning af kompensation på tværs af firmaer** – Kompensation for medarbejdere tildeles pr. juridisk ansættelsesenhed. Nogle gange kan en medarbejder være ansat i flere juridiske enheder på samme tid. Når denne funktion er valgt, vises kompensationen for hver juridisk enhed i **Selvbetjening for medarbejder** og **Selvbetjening for leder**, uden at du behøver at skifte juridiske enheder. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
