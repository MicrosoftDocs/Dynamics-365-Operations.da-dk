---
title: Testgrupper for kvalitetsstyring
description: I dette emne beskrives, hvordan du opretter testgrupper, så der kan bruges flere test sammen med kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 020a610e6a7e4d4b35ceb176d542bae32503a615
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021750"
---
# <a name="quality-management-test-groups"></a>Testgrupper for kvalitetsstyring

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du opretter testgrupper, så der kan bruges flere test sammen med kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.

Du kan bruge siden **Testgrupper** til at konfigurere, redigere og få vist testgrupper og individuelle test, der er tildelt testgrupperne. I den øverste del af siden vises testgrupperne, og i den nederste del vises de test, der er knyttet til en valgt testgruppe.

Du kan tildele flere politikker til en testgruppe, f.eks. en varestikprøveplan, et acceptabelt kvalitetsniveau (AQL) og kravet om destruktiv test. Når du derefter knytter en individuel test til en testgruppe, kan du definere flere oplysninger, f.eks. rækkefølge, dokumenter og gyldighedsdatoer. For kvantitative test skal de oplysninger, du angiver, også omfatte acceptable målingsværdier. For kvalitative test skal oplysningerne også omfatte testvariablen og standardudfaldet.

Den testgruppe, der tildeles til en kvalitetsordre, definerer det testsæt, der skal som standard skal udføres på den angivne vare. Du kan dog tilføje, slette eller ændre test for kvalitetsordren. Testresultaterne rapporteres for hver test i en kvalitetsordre.

Når du definerer en testgruppe, kan du vælge at angive en varestikprøve. Varestikprøver bruges til at definere mængden af det produkt, der skal testes. Du kan finde flere oplysninger under [Varestikprøver for kvalitetsstyring](quality-item-sampling.md). Du kan også angive, om testene i en testgruppe er destruktive. Ved en destruktiv test destrueres varestikprøven, og mængden fjernes fra den disponible lagerbeholdning.

## <a name="example-of-a-test-group"></a>Eksempel på en testgruppe

En produktionsvirksomhed definerer en testgruppe for hver afvigelse fra firmaets retningslinjer for kvalitet. De forskellige testgrupper reflekterer forskelle i prøveplaner, hvilke testsæt der skal udføres sammen, det acceptable kvalitetsniveau og andre faktorer. For kvantitative test er der også forskelle i de acceptable måleværdier. For at håndhæve sine kvalitetsretningslinjer tildeler virksomheden en testgruppe til hver regel, der bruges til automatisk at generere kvalitetsordrer på siden **Kvalitetstilknytninger**. Den tildeler også en testgruppe til kvalitetsordrer, der er oprettet manuelt.

## <a name="create-a-test-group"></a>Oprette en testgruppe

Benyt denne fremgangsmåde for at oprette en testgruppe.

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Testgrupper**.
1. Vælg **Ny** i handlingsruden for at tilføje en række til gitteret i øverste del af siden. Angiv følgende felter til den nye række:

    - **Testgruppe** – Angiv et entydigt id eller navn til testgruppen.
    - **Beskrivelse** – Indtast en detaljeret beskrivelse af testgruppen.
    - **Acceptabelt kvalitetsniveau** – Angiv den samlede procentdel af testresultater, der skal være bestået, for at gruppen af test kan opfattes som bestået.
    - **Varestikprøve** – Vælg en varestikprøve. Du kan finde flere oplysninger under [Varestikprøver for kvalitetsstyring](quality-item-sampling.md).
    - **Destruktiv** – Markér dette afkrydsningsfelt for at angive, at testgruppen vil destruere de varer, der er testet.

1. Mens den nye række stadig er markeret, skal du vælge fanen **Generelt** i den øverste del af siden. Nogle af indstillingerne for den testgruppe, der er valgt under fanen **Oversigt**, gentages her. Derudover kan du angive følgende felter for gruppen:

    - **Opdater lagerbatchattribut** – Når du angiver denne indstilling til *Ja* her, angives den automatisk til *Ja* for hver ny test, der føjes til testgruppen i den nederste del af siden.
    - **Opdater batchdisposition** – Når du angiver denne indstilling til *Ja*, og den vare, der testes, er batchkontrolleret, opdateres batchdispositionen automatisk med den værdi, der er valgt i feltet **Batchdispositionen for mislykket kvalitetsordre** eller **Bestået batchdisposition for kvalitetsordre**.
    - **Mislykket batchdisposition for kvalitetsordre** – Vælg den batchdispositionskode, der skal tildeles, når en kvalitetsordre, der indeholder denne testgruppe, mislykkes, fordi den ikke opfylder AQL'et.
    - **Bestået batchdisposition for kvalitetsordre** – Vælg den batchdispositionskode, der skal tildeles, når en kvalitetsordre, der indeholder denne testgruppe, består, fordi den ikke opfylder AQL'et.
    - **Opdater lagerstatus** – Når du angiver denne indstilling til *Ja*, og **Lagerstatus** er aktiveret på lagringsdimensionsgruppen for den vare, der testes, opdateres status automatisk med den status, der er valgt i feltet **Mislykket kvalitetsordrestatus** eller **Bestået kvalitetsordrestatus**.
    - **Mislykket kvalitetsordrestatus** – Vælg den status for lagerbeholdningen, som skal tildeles varen, når en kvalitetsordre, der inkluderer denne testgruppe, mislykkes, fordi den ikke opfylder AQL'et.
    - **Bestået kvalitetsordrestatus** – Vælg den status for lagerbeholdningen, som skal tildeles varen, når en kvalitetsordre, der inkluderer denne testgruppe, består, fordi den opfylder AQL'et.

## <a name="add-a-qualitative-test-to-a-test-group"></a>Føje en kvalitativ test til en testgruppe

Hvis du vil føje en kvalitativ test til en testgruppe, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Testgrupper**.
1. Vælg den testgruppe, du vil føje en test til, under fanen **Oversigt** i øverste del af siden.
1. Under fanen **Oversigt** nederst på siden skal du vælge **Tilføj** på værktøjslinjen for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Løbenummer** – Angiv et heltal for at angive den rækkefølge, som testene skal udføres i. Test, der har mindre løbenumre, køres før test, der har større løbenumre.

        > [!NOTE]
        > Det anbefales, at der er mellemrum mellem de enkelte løbenumre. Du kan f.eks. angive feltet **Løbenummer** til *10* for den første test og derefter øge numemret med 10 for hver ekstra test. På denne måde kan du tilføje nye test senere uden at skulle slette linjerne og oprette dem igen for at placere dem i den ønskede rækkefølge.

    - **Test** – Vælg den test, du vil udføre. Vælg en test for en kvalitativ test, hvor feltet **Type** er angivet til *Indstilling*.
    - **Gyldig fra** – Vælg den første dato, hvor testen er gyldig. Hvis du lader dette felt være tomt, er der ingen grænse.
    - **Udløb** – Vælg den sidste dato, hvor testen er gyldig. Hvis du ikke udfylder dette felt eller angiver det til *Aldrig*, er der ingen grænse.
    - **Bestemmelse af testværdi** – Vælg, hvordan et AQL skal bestemmes, når der registreres flere resultater for samme test. For en kvalitativ test kan der kun vælges *Manuel*. Hvis du vælger en af de andre værdier (*Gennemsnit*, *Minimum* eller *Maksimum*), vises der en fejlmeddelelse, når du gemmer testgruppen.
    - **Attribut** – Hvis du vil registrere testresultater for en batchattribut, skal du vælge attributten her og markere afkrydsningsfeltet **Opdater lagerbattribut**.
    - **Opdater lagerbatchattribut** – Markér dette afkrydsningsfelt for at registrere testresultater for en batchattribut, der er valgt i feltet **Attribut**.

1. Vælg fanen **Generelt** i den nederste del af siden. Nogle af indstillingerne for den test, der er valgt under fanen **Oversigt**, gentages her. Derudover kan du angive følgende felter for testen:

    - **Analysecertifikatrapport** – Angiv denne indstilling til *Ja* for at angive, at testresultaterne skal udskrives på analysecertifikatet (CoA). Denne rapport kan genereres ud fra kvalitetsordren.
    - **Handling ved fejl** – Vælg enten *Accepter* eller *Mislykket* for at angive, om testen skal bestås eller mislykkes, hvis det angivne AQL ikke er opfyldt.
    - **Acceptabelt kvalitetsniveau** – Angiv den samlede procentdel af testresultater, der skal være bestået, for at testen kan opfattes som bestået.

1. Angiv følgende felter under fanen **Test** i den nederste del af siden:

    - **Variabel** – Vælg den testvariabel, du vil registrere de kvalitative testresultater for.
    - **Standardudfald** – Vælg det standardudfald, der skal registreres for testresultaterne.
    - **Testinstrument** – Vælg den enhed, der skal bruges til testen. Hvis der er defineret et testinstrument, angives det automatisk for testen i testgruppen.

1. Luk siden.

## <a name="add-a-quantitative-test-to-a-test-group"></a>Føje en kvantitativ test til en testgruppe

Hvis du vil føje en kvantitativ test til en testgruppe, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Testgrupper**.
1. Vælg den testgruppe, du vil føje en test til, under fanen **Oversigt** i øverste del af siden.
1. Under fanen **Oversigt** nederst på siden skal du vælge **Tilføj** på værktøjslinjen for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Løbenummer** – Angiv et heltal for at angive den rækkefølge, som testene skal udføres i. Test, der har mindre løbenumre, køres før test, der har større løbenumre.

        > [!NOTE]
        > Det anbefales, at der er mellemrum mellem de enkelte løbenumre. Du kan f.eks. angive feltet **Løbenummer** til *10* for den første test og derefter øge numemret med 10 for hver ekstra test. På denne måde kan du tilføje nye test senere uden at skulle slette linjerne og oprette dem igen for at placere dem i den ønskede rækkefølge.

    - **Test** – Vælg den test, du vil udføre. Vælg en test for en kvantitativ test, hvor feltet **Type** er angivet til *Del* eller *Heltal*.
    - **Gyldig fra** – Vælg den første dato, hvor testen er gyldig. Hvis du lader dette felt være tomt, er der ingen grænse.
    - **Udløb** – Vælg den sidste dato, hvor testen er gyldig. Hvis du ikke udfylder dette felt eller angiver det til *Aldrig*, er der ingen grænse.
    - **Bestemmelse af testværdi** – Vælg, hvordan et AQL skal bestemmes, når der registreres flere resultater for samme test. De tilgængelige indstillinger er *Gennemsnit*, *Minimum*, *Maksimum* og *Manuel*.
    - **Attribut** – Hvis du vil registrere testresultater for en batchattribut, skal du vælge attributten her og markere afkrydsningsfeltet **Opdater lagerbattribut**.
    - **Opdater lagerbatchattribut** – Markér dette afkrydsningsfelt for at registrere testresultater for en batchattribut, der er valgt i feltet **Attribut**.

1. Vælg fanen **Generelt** i den nederste del af siden. Nogle af indstillingerne for den test, der er valgt under fanen **Oversigt**, gentages her. Derudover kan du angive følgende felter for testen:

    - **Analysecertifikatrapport** – Angiv denne indstilling til *Ja* for at angive, at testresultaterne skal udskrives på CoA'et. Denne rapport kan genereres ud fra kvalitetsordren.
    - **Handling ved fejl** – Vælg enten *Accepter* eller *Mislykket* for at angive, om testen skal bestås eller mislykkes, hvis det angivne AQL ikke er opfyldt.
    - **Acceptabelt kvalitetsniveau** – Angiv den samlede procentdel af testresultater, der skal være bestået, for at testen kan opfattes som bestået.

1. Angiv følgende felter under fanen **Test** i den nederste del af siden:

    - **Standard** – Angiv det beløb (heltal eller brøk), der forventes for testresultaterne. Den værdi, du angiver, vil blive angivet som standard i testresultaterne. Den vil desuden automatisk blive angivet som standardværdi i felterne **Min.** og **Maks**.
    - **Min.** – Angiv den mindste tilladte værdi for testresultaterne. Den værdi, du angiver, skal være mindre end det beløb, der er angivet i feltet **Standard**. Når du opdaterer feltet **Min.** opdateres feltet **Min. tolerance** (%) automatisk. Når du opdaterer feltet **Min. tolerance (%)** opdateres ligeledes feltet **Min.** automatisk.
    - **Maks.** – Angiv den største tilladte værdi for testresultaterne. Den værdi, du angiver, skal være større end det beløb, der er angivet i feltet **Standard**. Når du opdaterer feltet **Maks.** opdateres feltet **Maks. tolerance** (%) automatisk. Når du opdaterer feltet **Maks. tolerance (%)** opdateres ligeledes feltet **Maks.** automatisk.
    - **Testinstrument** – Vælg den enhed, der skal bruges til testen. Hvis der er defineret et testinstrument, angives det automatisk for testen i testgruppen.

1. Luk siden.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Testinstrumenter for kvalitetsstyring](quality-management-processes.md)
- [Test for kvalitetsstyring](quality-management-processes.md)
- [Testvariabler for kvalitetsstyring](quality-management-processes.md)
- [Kvalitetstilknytninger](quality-management-processes.md)
- [Batchattributter](/supply-chain/production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
