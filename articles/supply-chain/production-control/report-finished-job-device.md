---
title: Færdigmelde fra jobkortenheden
description: Dette emne beskriver, hvordan systemet konfigureres, så brugere af en jobkortenhed kan rapportere færdigvarer fra en produktionsordre til lageret.
author: johanhoffmann
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 2fa82c721316fb21442e1cfc00ba00ff8cb2b750
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778225"
---
# <a name="report-as-finished-from-the-job-card-device"></a>Færdigmelde fra jobkortenheden

[!include [banner](../includes/banner.md)]

Arbejderne skal bruge siden **Rapportstatus** på jobkortenheden til at rapportere de mængder, der er færdiggjort for et produktionsjob. Dette emne beskriver, hvordan du konfigurerer forskellige indstillinger, der bestemmer, hvordan arbejdere kan færdigmelde ved hjælp af denne side og vælge det, der sker næste gang. Der findes følgende valgmuligheder:

- Kontrollere, om og hvordan færdigmeldte mængder føjes til lageret.
- Kontrollere, om og hvordan batchnumre genereres og anvendes ved færdigmelding.
- Kontrollere, om og hvordan serienumre genereres og anvendes ved færdigmelding.
- Kontrollere, om og hvordan der færdigmeldes til et id.

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a>Kontrollere, om færdigmeldte mængder føjes til lageret

Udfør følgende trin for at kontrollere, om og hvordan de mængder, der er færdigmeldt i den sidste operation, skal føjes til lageret.

1. Gå til **Produktkontrol \> Opsætning \> Produktionsudførelse \> Produktionsordrestandarder**.
1. På fanen **Færdigmelding** skal du angive feltet **Opdater færdigmelding online** til en af følgende værdier:

    - **Nej** – Der føjes intet antal til lageret, når der rapporteres mængder for den sidste operation. Status for produktionsordren ændres aldrig.
    - **Status + antal** – Statussen for produktionsordren ændres til *Færdigmeldt*, og antallet vil blive færdigmeldt til lageret.
    - **Antal** – Antallet færdigmeldes til lageret, men statussen for produktionsordren ændres aldrig.
    - **Status** – Kun statussen for produktionsordren ændres. Der føjes ingen antal til lageret, når der rapporteres mængder for den sidste operation.

> [!NOTE]
> Antal spores ikke på lageret, hvis de operationer, de er færdigmeldt på, ikke er defineret som den sidste operation. Disse antal kan dog bruges til at få vist status. De kan også inkluderes i regler, der styrer, om arbejderne kan starte den næste operation, før en defineret tærskel for rapporterede antal i den forrige operation nås. Du kan definere disse regler under fanen **Validering af antal** på siden **Produktionsordrestandarder**.

Du kan finde flere oplysninger om, hvordan du arbejder med siden **Produktionsordrestandarder** i [Produktionsparametre i produktionsudførelse](production-parameters-manufacturing-execution.md).

## <a name="report-batch-controlled-items-as-finished"></a>Færdigmelde batchstyrede varer

Jobkortenheden understøtter tre scenarier til rapportering af batchvarer. Disse scenarier gælder både for varer, der er aktiveret til avancerede lagerprocesser, og for varer, der ikke er aktiveret til avancerede lagerprocesser.

- **Manuelt tildelte batchnumre** - Arbejderne angiver et brugerdefineret batchnummer. Dette batchnummer kan komme fra en ekstern kilde, der ikke er kendt af systemet.
- **Foruddefinerede batchnumre** - Arbejderne vælger et batchnummer på en liste over batchnumre, som systemet automatisk genererer, før produktionsordren frigives til jobkortenheden.
- **Faste batchnumre** - Arbejderne angiver og vælger ikke et batchnummer. I stedet tildeler systemet automatisk et batchnummer til produktionsordren, før den frigives.


### <a name="enable-the-feature-on-your-system"></a>Aktivere funktionen på dit system

Hvis du vil sætte dine jobkortenheder i gang med at acceptere et batchnummer under færdigmeldingen, skal du bruge [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere følgende funktioner (i denne rækkefølge):

1. Forbedret brugeroplevelse for dialogboksen Rapport i gang på jobkortenheden.
1. Aktivere for at angive batch- og serienumre, når der færdigmeldes fra jobkortenheden

### <a name="configure-products-that-require-batch-number-reporting"></a>Konfigurere produkter, der kræver batchnummerrapportering

Hvis du vil aktivere et produkt til at understøtte et af de tilgængelige batchstyrede scenarier, skal du følge disse trin:

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg produktet, der skal konfigureres.
1. I oversigtspanelet **Styr lager** i feltet **Batchnummergruppe** skal du vælge den sporingsnummergruppe, der er konfigureret til at understøtte dit scenarie.

> [!NOTE]
> Hvis der ikke er knyttet en batchnummergruppe til et batchstyret produkt, er jobkortenheden som standard angivet til manuel indtastning for batchnummeret under færdigmelding.

I det følgende afsnit beskrives, hvordan du kan konfigurere sporingsnummergrupper, så hvert af de tre scenarier for rapportering om batchvarer understøttes.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>Konfigurere en sporingsnummergruppe, så arbejderne kan tildele et batchnummer manuelt

Du skal følge disse trin for at konfigurere en sporingsnummergruppe og tillade manuelt tildelte batchnumre.

1. Gå til **Lagerstyring \> Opsætning \> Dimensionser \> Sporingsnummergrupper**.
1. Opret eller vælg den sporingsnummergruppe, der skal konfigureres.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Manuel** til **Ja**.

    ![En sporingsnummergruppe for manuelle batchnumre.](media/tracking-number-group-manual.png "En sporingsnummergruppe for manuelle batchnumre")

1. Angiv andre værdier efter behov, og vælg derefter denne sporingsnummergruppe som batchnummergruppe for de frigivne produkter, du vil bruge dette scenarie for.

Når du bruger dette scenarie, er feltet **Batchnummer**, som siden **Rapport i gang** på jobkortenheden indeholder, en tekstboks, hvor arbejderne kan angive en hvilken som helst værdi.

![Siden Rapportstatus med et felt til manuelle batchnumre.](media/job-card-device-batch-manual.png "Siden Rapportstatus med et felt til manuelle batchnumre")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>Konfigurere en sporingsnummergruppe, der viser en liste over foruddefinerede batchnumre

Du skal følge disse trin for at konfigurere en sporingsnummergruppe og lave en liste over foruddefinerede batchnumre.

1. Gå til **Lagerstyring \> Opsætning > Dimensioner \> Sporingsnummergrupper**.
1. Opret eller vælg den sporingsnummergruppe, der skal konfigureres.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Kun på lagertransaktioner** til **Ja**.
1. Brug feltet **Pr. antal** til at opdele batchnumre pr. antal ud fra den værdi, du angiver. Du har f.eks. en produktionsordre på ti stykker, og feltet **Pr. antal** er angivet til *2*. I dette tilfælde tildeles der fem batchnumre til produktionsordren, når den oprettes.

    ![En sporingsnummergruppe for foruddefinerede batchnumre.](media/tracking-number-group-predefined.png "En sporingsnummergruppe for foruddefinerede batchnumre")

1. Angiv andre værdier efter behov, og vælg derefter denne sporingsnummergruppe som batchnummergruppe for de frigivne produkter, du vil bruge dette scenarie for.

Når du bruger dette scenarie, er feltet **Batchnummer**, som siden **Rapport i gang** på jobkortenheden indeholder, en rulleliste, hvor arbejderne skal vælge en foruddefineret værdi.

![Siden Rapportstatus med en liste over foruddefinerede batchnumre.](media/job-card-device-batch-predefined.png "Siden Rapportstatus med en liste over foruddefinerede batchnumre")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>Konfigurere en sporingsnummergruppe, som automatisk tildeler batchnumre

Hvis der automatisk skal tildeles batchnumre uden arbejderinput, skal du følge disse trin for at konfigurere en sporingsnummergruppe.

1. Gå til **Lagerstyring \> Opsætning \> Dimensionser \> Sporingsnummergrupper**.
1. Opret eller vælg den sporingsnummergruppe, der skal konfigureres.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Kun på lagertransaktioner** til **Nej**.
1. Angiv indstillingen **Manuel** til **Nej**.

    ![En sporingsnummergruppe for faste batchnumre.](media/tracking-number-group-fixed.png "En sporingsnummergruppe for faste batchnumre")

1. Angiv andre værdier efter behov, og vælg derefter denne sporingsnummergruppe som batchnummergruppe for de frigivne produkter, du vil bruge dette scenarie for.

Når du bruger dette scenarie, viser feltet **Batchnummer**, som siden **Rapport i gang** på jobkortenheden leverer, en værdi, men arbejderne kan ikke redigere denne værdi.

![Siden Rapportstatus med et fast batchnummer.](media/job-card-device-batch-fixed.png "Siden Rapportstatus med et fast batchnummer")

## <a name="report-serial-controlled-items-as-finished"></a>Færdigmelde seriestyrede varer

Jobkortenheden understøtter tre scenarier til rapportering af seriestyrede varer. Disse scenarier gælder både for varer, der er aktiveret til avancerede lagerprocesser, og for varer, der ikke er aktiveret til avancerede lagerprocesser.

- **Manuelt tildelte serienumre** - Arbejderne angiver et brugerdefineret serienummer. Dette serienummer kan komme fra en ekstern kilde, der ikke er kendt af systemet.
- **Foruddefinerede serienumre** - Arbejderne vælger et serienummer på en liste over serienumre, som systemet automatisk genererer, før produktionsordren frigives til jobkortenheden.
- **Faste serienumre** - Arbejderne angiver og vælger ikke et serienummer. I stedet tildeler systemet automatisk et serienummer til produktionsordren, før den frigives.

### <a name="enable-the-feature-on-your-system"></a>Aktivere funktionen på dit system

Hvis du vil sætte dine jobkortenheder i gang med at acceptere et serienummer under færdigmeldingen, skal du bruge [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere følgende funktioner (i denne rækkefølge):

1. Forbedret brugeroplevelse for dialogboksen Rapport i gang på jobkortenheden.
1. Aktivere for at angive batch- og serienumre, når der færdigmeldes fra jobkortenheden

### <a name="configure-products-that-require-serial-number-reporting"></a>Konfigurere produkter, der kræver serienummerrapportering

Hvis du vil aktivere et produkt til at understøtte et af de tilgængelige seriestyrede scenarier, skal du følge disse trin:

Følg disse trin for at aktivere et scenarie.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg produktet, der skal konfigureres.
1. I oversigtspanelet **Styr lager** i feltet **Serienummergruppe** skal du vælge den sporingsnummergruppe, der er konfigureret til at understøtte dit scenarie.

> [!NOTE]
> Hvis der ikke er knyttet en serienummergruppe til et seriestyret produkt, er jobkortenheden som standard angivet til manuel indtastning for serienummeret under færdigmelding.

I det følgende afsnit beskrives, hvordan du kan konfigurere sporingsnummergrupper, så hvert af de tre scenarier for rapportering om serievarer understøttes.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-serial-number"></a>Konfigurere en sporingsnummergruppe, så arbejderne kan tildele et serienummer manuelt

Du skal følge disse trin for at konfigurere en sporingsnummergruppe og tillade manuelt tildelte serienumre.

1. Gå til **Lagerstyring \> Opsætning \> Dimensionser \> Sporingsnummergrupper**.
1. Opret eller vælg den sporingsnummergruppe, der skal konfigureres.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Manuel** til **Ja**.

    ![Siden Sporingsnummergrupper, serienumre.](media/tracking-number-group-manual-serial.png "Siden Sporingsnummergrupper, serienumre")

1. Angiv andre værdier efter behov, og vælg derefter denne sporingsnummergruppe som serienummergruppe for de frigivne produkter, du vil bruge dette scenarie for.

Når du bruger dette scenarie, er feltet **Serienummer**, som siden **Rapport i gang** på jobkortenheden indeholder, en tekstboks, hvor arbejderne kan angive en hvilken som helst værdi af serienummer. Ved angivelse af en værdi føjes den til listen over serienumre. På listen kan arbejdere gøre følgende:

- Hvis du vil markere et serienummer som kasseret, skal du vælge knappen **Kasseres** for den relevante række. Arbejderen bliver bedt om at angive en **Fejlårsag**.
- Hvis du vil slette et serienummer, skal du vælge knappen **Slet** for den relevante række.

![Siden Rapportstatus med et felt til manuelle serienumre.](media/job-card-device-serial-manual.png "Siden Rapportstatus med et felt til manuelle serienumre")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-serial-numbers"></a>Konfigurere en sporingsnummergruppe, der viser en liste over foruddefinerede serienumre

Du skal følge disse trin for at konfigurere en sporingsnummergruppe og lave en liste over foruddefinerede serienumre.

1. Gå til **Lagerstyring \> Opsætning \> Dimensionser \> Sporingsnummergrupper**.
1. Opret eller vælg den sporingsnummergruppe, der skal konfigureres.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Kun på lagertransaktioner** til **Ja**.
1. Brug feltet **Pr. antal** til at opdele serienumre pr. antal af én.

    ![En sporingsnummergruppe for foruddefinerede serienumre.](media/tracking-number-group-predefined-sn.png "En sporingsnummergruppe for foruddefinerede serienumre")

1. Angiv andre værdier efter behov, og vælg derefter denne sporingsnummergruppe som serienummergruppe for de frigivne produkter, du vil bruge dette scenarie for.

Når du bruger dette scenarie, er feltet **Serienummer**, som siden **Rapport i gang** på jobkortenheden indeholder, en rulleliste, hvor arbejderne skal vælge en foruddefineret værdi.

![Siden Rapportstatus med en liste over foruddefinerede serienumre.](media/job-card-device-serial-predefined.png "Siden Rapportstatus med en liste over foruddefinerede serienumre")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-serial-numbers"></a>Konfigurere en sporingsnummergruppe, som automatisk tildeler serienumre

Hvis der automatisk skal tildeles serienumre uden arbejderinput, skal du følge disse trin for at konfigurere en sporingsnummergruppe.

1. Gå til **Lagerstyring \> Opsætning \> Dimensionser \> Sporingsnummergrupper**.
1. Opret eller vælg den sporingsnummergruppe, der skal konfigureres.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Kun på lagertransaktioner** til **Nej**.
1. Angiv indstillingen **Manuel** til **Nej**.

    ![En sporingsnummergruppe for faste serienumre.](media/tracking-number-group-fixed-sn.png "En sporingsnummergruppe for faste serienumre")

1. Angiv andre værdier efter behov, og vælg derefter denne sporingsnummergruppe som serienummergruppe for de frigivne produkter, du vil bruge dette scenarie for.

Når du bruger dette scenarie, viser feltet **Serienummer**, som siden **Rapport i gang** på jobkortenheden leverer, en værdi, men arbejderne kan ikke redigere denne værdi. Dette scenarie er kun relevant, når der er oprettet en produktionsordre for et antal på ét styk af en serienummerstyret vare.

![Siden Rapportstatus med et fast serienummer.](media/job-card-device-serial-fixed.png "Siden Rapportstatus med et fast serienummer")

## <a name="report-as-finished-to-a-license-plate"></a>Rapportere som færdig til en nummerplade

Avancerede lagerprocesser kan bruge nummerpladedimensionen til at spore lager på lagersteder, der er konfigureret til dette formål. I dette tilfælde er nummeret på nummerpladen nødvendigt, når en arbejder rapporterer antal som færdige.

### <a name="enable-license-plate-reporting-and-label-printing"></a>Aktivere nummerpladerapportering og labeludskrivning

Hvis du vil bruge de funktioner, der er beskrevet i dette afsnit, skal du bruge [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere følgende funktioner (i denne rækkefølge):

1. Nummerplade til færdigmelding er føjet til jobkortenheden (fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret).
1. Aktivér automatisk generering af id-nummer ved færdigmelding i jobkortenheden
1. Udskriv etiket fra jobkortenhed

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a>Konfigurere rapportering som færdig til en nummerplade

Hvis du vil styre, om arbejdere skal genbruge en eksisterende nummerplade eller generere en ny nummerplade, når de færdigmelder antal, skal du følge disse trin.

1. Gå til **Produktionsstyring \> Opsætning \> Produktionsudførelse \> Konfigurere jobkort for enheder**.
2. For hver enhed skal du angive følgende indstillinger:

    - **Generér nummerplade** – Angiv denne indstilling til **Ja** for at generere en ny nummerplade for hver færdigmeldingsrapport. Angiv den til **Nej**, hvis en eksisterende nummerplade skal anvendes til hver færdigmeldingsrapport.
    - **Udskriv label** – Angiv denne indstilling til **Ja**, hvis arbejderen skal udskrive en nummerpladelabel for hver færdigmeldingsrapport. Angiv den til **Nej**, hvis der ikke kræves en label. 

![Siden Konfigurere jobkort for enheder.](media/config-job-card-raf.png "Siden Konfigurere jobkort for enheder")

> [!NOTE]
> Gå til **Lokationsstyring \> Opsætning \> Dokumentrute \> Dokumentrute** for at konfigurere labelen. Yderligere oplysninger finder du i afsnittet [Aktivere udskrivning af id-etiket](../warehousing/tasks/license-plate-label-printing.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]