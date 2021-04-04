---
title: Konfigurer ER-modeltilknytninger ud fra landeafhængighed
description: Dette emne beskriver, hvordan du kan konfigurere ER-modeltilknytninger, så de afhænger af den juridiske enheds land/område-kontekst, der styrer brugen af dem.
author: NickSelin
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 48d2e3c81d038cc55f6f100f3081561506946199
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562280"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a>Konfigurer ER-modeltilknytninger ud fra landeafhængighed

[!include[banner](../includes/banner.md)]

Du kan konfigurere modeltilknytninger for Elektronisk rapportering (ER), så de implementerer en generisk ER-datamodel, men er specifikke for Dynamics 365 Finance. Dette emne beskriver, hvordan du kan designe flere ER-modeltilknytninger for en ER-datamodel til at styre, hvordan de bruges af tilsvarende ER-formater, der køres fra firmaer, der har forskellige land/område-kontekster.

## <a name="prerequisites"></a>Forudsætninger

Før du kan følge eksemplerne i dette emne, skal du have følgende adgang:

- Adgang til Finance for en af følgende roller:
    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

- Adgang til den forekomst af Regulatory Configuration Service (RCS), der er klargjort til den samme lejer som Finance, for en af følgende roller:
    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

Visse trin i dette emne kræver kørsel af et ER-format. I nogle tilfælde påvirkes udførelsen af et ER-format af den land/område-kontekst, som det firma, du aktuelt er logget på. Du kan køre et ER-format i den aktuelle RCS-forekomst, hvis det firma, der har den krævede land/område-kontekst, er tilgængelig i RCS. Ellers skal du overføre en fuldført version af den ER-modeltilknytning og ER-format, der bruger ER-datamodellen, til din Finance-forekomst, og derefter køre ER-formatet i den pågældende Finance-forekomst. Du kan finde oplysninger om, hvordan du importerer konfigurationer, der er placeret i RCS, til en Finance-forekomst under [Importer konfigurationer fra RCS](rcs-download-configurations.md).

## <a name="single-model-mapping-case"></a>En enkel modeltilknytningscase

Følg trinnene i [Bilag 1](#appendix1) i dette emne for at designe de påkrævede ER-komponenter. Du har nu modeltilknytningskonfigurationen **Tilknytning (generel)**, der indeholder modeltilknytningen for definitionen **Indgangspunktet 1**.

![Siden ER-konfigurationer](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a>Kør det konfigurerede format

1.  På **Konfigurationssiden** i oversigtspanelet **Versioner** skal du vælge **Kør**.
2.  Vælg **OK**.

Bemærk, at webbrowseren tilbyder at hente den tekstfil, der blev genereret af det udførte ER-format. Da dette format blev konfigureret til at bruge definitionen **Indgangspunkt 1**, og der i øjeblikket kun findes en enkelt modeltilknytning for den basismodel, der indeholder en tilknytning til denne definition, skal det udførte ER-format anvende **Tilknytning (generel)**-modeltilknytning for konfigurationen **Tilknytning (generel)** som datakilde. Den hentede fil indeholder derfor teksten **Generisk funktionalitet 1**.

## <a name="multiple-shared-model-mappings-case"></a>Case med delte modeltilknytninger

Følg trinnene i [Bilag 2](#appendix2) i dette emne for at designe de påkrævede ER-komponenter. Du har nu modeltilknytningskonfigurationerne **Tilknytning (generel)** og **Tilpasset tilknytning (generel)**, der indeholder modeltilknytningen for definitionen **Indgangspunktet 1**.

![Siden ER-konfigurationer](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a>Kør det konfigurerede format

1.  På siden **Konfigurationer** skal du i konfigurationstræet vælge **Format til at lære tilknytninger**.
2.  Gå til oversigtspanelet **Versioner**, og vælg **Kør**.
3.  Vælg **OK**.

Bemærk, at udførelsen af det valgte ER-format mislykkedes. En fejlmeddelelse oplyser dig om, at der forefindes mere end én modeltilknytning for modellen **Model til at lære tilknytninger** og definitionen **Indgangspunkt 1** i modeltilknytningskonfigurationerne **Tilknytning (generel)** og **Tilpasset tilknytning (generel)**. I meddelelsen anbefales det også, at du vælger en af disse konfigurationer som standardkonfiguration.

![Siden ER-konfigurationer](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a>Definer en standardkonfiguration for tilknytning

Benyt følgende fremgangsmåde for at definere modeltilknytningkonfigurationen **Tilpasset tilknytning (generel)** som standardkonfiguration, således at dennes tilknytninger kan anvendes som datakilder for ER-formatet **Format til at lære tilknytninger**.

1.  På siden **Konfigurationer** skal du i konfigurationstræet vælge **Tilpasset tilknytning (generel)**.
2.  Vælg **Rediger** efter behov for at gøre den aktuelle side klar til redigering.
3.  Vælg **Ja** i indstillingen **Standard for modeltilknytning**.
4.  Vælg **Gem**.

![Siden ER-konfigurationer](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a>Kør det konfigurerede format

1.  På siden **Konfigurationer** skal du i konfigurationstræet vælge **Format til at lære tilknytninger**.
2.  Gå til oversigtspanelet **Versioner**, og vælg **Kør**.
3.  Vælg **OK**.

Bemærk, at udførelsen af det valgte ER-format lykkedes. Webbrowseren tilbyder at hente den tekstfil, der blev genereret af det udførte ER-format. Da dette format blev konfigureret til at bruge definitionen **Indgangspunkt 1**, og modeltilknytningskonfigurationen **Tilpasset tilknytning (generel)** blev valgt som standardkonfiguration, anvendte det udførte ER-format modeltilknytningen **Kopi at tilknytning (generel)** for konfigurationen **Tilpasset tilknytning (generel)** som datakilde. Den hentede fil indeholder derfor den tilpassede tekst for **Generisk funktionalitet 1**.

> [!NOTE]
> Hvis du ændrer det firma, du aktuelt er logget på, og kører dette ER-format igen, får du samme indhold i den genererede fil, fordi standardkonfigurationen for ER-modeltilknytning ikke indeholder firmaafhængige begrænsninger.

## <a name="multiple-mixed-model-mappings-case"></a>Case med blandede modeltilknytninger

Følg trinnene i [Bilag 3](#appendix3) i dette emne for at designe de påkrævede ER-komponenter. Du har nu konfigurationerne **Tilknytning (generel)**, **Tilpasset tilknytning (generel)** og **Modeltilknytning (FR)**, der indeholder modeltilknytningen for definitionen **Indgangspunktet 1**.

Bemærk, at version 1 af modeltilknytningskonfigurationen **Tilknytning (FR)** er konfigureret, så den kun gælder for ER-formater for **Model til at lære tilknytninger**, der køres i Finance-firmaer, som har fransk land/område-kontekst.

![Siden ER-konfigurationer](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a>Kør det konfigurerede format

1.  Skift firma til **FRSI**.
2.  På siden **Konfigurationer** skal du i konfigurationstræet vælge **Format til at lære tilknytninger**.
3.  Gå til oversigtspanelet **Versioner**, og vælg **Kør**.
4.  Vælg **OK**.

Bemærk, at udførelsen af det valgte ER-format lykkedes. Webbrowseren tilbyder at hente den tekstfil, der blev genereret af det udførte ER-format. Da dette format blev konfigureret til at bruge definitionen **Indgangspunkt 1**, og modeltilknytningskonfigurationen **Tilpasset tilknytning (generel)** blev valgt som standardkonfiguration, anvendte det udførte ER-format modeltilknytningen **Kopi at tilknytning (generel)** for konfigurationen **Tilpasset tilknytning (generel)** som datakilde. Den hentede fil indeholder derfor den tilpassede tekst for **Generisk funktionalitet 1**.

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a>Definer den for Frankrig specifikke tilknytningskonfiguration som standardkonfiguration

Udfør følgende trin for at definere den brugerdefinerede modeltilknytningskonfiguration for **Tilknytning (FR)** som standardkonfigurationen. Bemærk, at da denne tilknytning er specifik for Frankrig, vil den blive betragtet som standardtilknytning mellem alle de modeltilknytningskonfigurationer, der har landekoden **FR** angivet i feltet **ISO-land/område-kode**.

1.  På siden **Konfigurationer** skal du i konfigurationstræet vælge **Tilknytning (FR)**.
2.  Vælg **Rediger** efter behov for at gøre den aktuelle side klar til redigering.
3.  Vælg **Ja** i indstillingen **Standard for modeltilknytning**.
4.  Vælg **Gem**.

![Siden ER-konfigurationer](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a>Kør det konfigurerede format

1.  På siden **Konfigurationer** skal du i konfigurationstræet vælge **Format til at lære tilknytninger**.
2.  Gå til oversigtspanelet **Versioner**, og vælg **Kør**.
3.  Vælg **OK**.

Bemærk, at udførelsen af det valgte ER-format lykkedes. Webbrowseren tilbyder at hente den tekstfil, der blev genereret af det udførte ER-format. Da dette format blev konfigureret til at bruge definitionen **Indgangspunkt 1**, og modeltilknytningskonfigurationen **Tilknytning (FR)** blev valgt som standardkonfiguration, anvendte det udførte ER-format modeltilknytningen **Tilknytning (FR)** for konfigurationen **Tilknytning (FR)** som datakilde. Den hentede fil indeholder derfor teksten **FR funktionalitet 1**.

> [!NOTE]
> Hvis du ændrer det firma, du aktuelt er logget på, og kører dette Er-format igen, afhænger outputtet af det valgte firmas land/område-kontekst.

## <a name="other-model-mapping-cases"></a>Andre cases med modeltilknytning

Som du har set, fungerer valget af en modeltilknytning til udførsel af et ER-format på følgende måde:

- Den modeltilknytningsdefinition, som et ER-format bruger, er angivet (**Indgangspunkt 1** i eksemplerne i dette emne).
- Alle tilknytningskonfigurationer, der indeholder en tilknytning, som har den angivne definition, og som opfylder eventuelle begrænsninger af land/område-kontekster, der er konfigureret, kan muligvis bruges til at køre ER-formatet (**Tilknytning (generel)**, **Tilpasset tilknytning (generel)** og **Tilknytning (FR)** i eksemplerne i dette emne).
- Enhver standardmodeltilknytning, der har begrænsninger for land/område-kontekst, har den højeste prioritet i forbindelse med udvælgelse (**Tilknytning (FR)** i eksemplerne i dette emne).
- Enhver standardmodeltilknytning, der ikke har begrænsninger for land/område-kontekst, har den næsthøjeste prioritet i forbindelse med udvælgelse (**Tilpasset tilknytning (generel)** i eksemplerne i dette emne).
- Enhver modeltilknytning, der har begrænsninger for land/område-kontekst, har højere prioritet i forbindelse med udvælgelse end en modeltilknytning, der ikke har begrænsninger for land/område-kontekst.

Følgende tabel viser oplysninger om resultaterne af valg af modeltilknytning for alle mulige modeltilknytningindstillinger:

- Kolonne 1 angiver, om den første modeltilknytning, der ikke har begrænsninger for land/område-kontekst (f.eks. hvis den delte tilknytning **Tilknytning (generel)**) vises, og i så fald, hvorvidt indstillingen **Standard for modeltilknytning** er angivet til **Ja** for den.
- Kolonne 2 angiver, om den anden modeltilknytning, der ikke har begrænsninger for land/område-kontekst (f.eks. hvis den delte tilknytning **Tilpasset tilknytning (generel)**) vises, og i så fald, hvorvidt indstillingen **Standard for modeltilknytning** er angivet til **Ja** for den.
- Kolonne 3 angiver, om den første modeltilknytning, der har begrænsninger for land/område-kontekst (f.eks. hvis den for Frankrig specifikke tilknytning **Tilknytning (FR)**) vises, og i så fald, hvorvidt indstillingen **Standard for modeltilknytning** er angivet til **Ja** for den.
- Kolonne 4 angiver, om den anden modeltilknytning, der har begrænsninger for land/område-kontekst vises, og i så fald, hvorvidt indstillingen **Standard for modeltilknytning** er angivet til **Ja** for den.
- Kolonne 5 viser resultatet af en valgmulighed for modeltilknytning for udførelse af et ER-format i forbindelse med kontrol af et firma, der har et land/område som A-kontekst.
- Kolonne 6 viser resultatet af en valgmulighed for modeltilknytning for udførelse af et ER-format i forbindelse med kontrol af et firma, der har et land/område som B-kontekst.

Et plustegn (+) i tabellen angiver tilstedeværelsen af en modeltilknytningskonfiguration i den aktuelle forekomst af Microsoft Azure-tjenesten, der bruges til at køre et ER-format (enten Finance eller RCS).

| Sag | Modeltilknytning 1 uden land/område-kontekst (MM1) | Modeltilknytning 2 uden land/område-kontekst (MM2) | Modeltilknytning 1 med A-kontekst for land/område (MM1A) | Modeltilknytning 2 med A-kontekst for land/område (MM2A) | Køres i forbindelse med kontrol af et firma, der har et land/område som en A-kontekst | Køres i forbindelse med kontrollen af et firma, der har et land/område som en B-kontekst |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     1   |     2   |    3    |    4    |           5               |            6               |
|     1   |         |         |         |         | Fejl (manglende tilknytning)   | Fejl (manglende tilknytning)    |
|     2   |     +   |         |         |         | MM1                       | MM1                        |
|     3   |     +   |     +   |         |         | Fejl (flere tilknytninger) | Fejl (flere tilknytninger)  |
|     4   |     +   |         |    +    |         | MM1A                      | MM1                        |
|     5   |     +   |         |    +    |    +    | Fejl (flere tilknytninger) | MM1                        |
|     6   |     +   | standard |    +    |    +    | MM2                       | MM2                        |
|     7   |     +   |         | standard |         | MM1A                      | MM1                        |
|     8   |     +   |         | standard |    +    | MM1A                      | MM1                        |
|     9   |     +   |         | standard | standard | Fejl (flere tilknytninger) | MM1                        |
|    10   | standard |         |         |         | MM1                       | MM1                        |
|    11   | standard |    +    |         |         | MM1                       | MM1                        |
|    12   | standard |         |    +    |         | MM1                       | MM1                        |
|    13   | standard | standard |         |         | Fejl (flere tilknytninger) | Fejl (flere tilknytninger)  |
|    14   | standard |         | standard |         | MM1A                      | MM1                        |
|    15   | standard |         | standard | standard | MM1A                      | MM2A                       |
|    16   |         |         |    +    |    +    | MM1A                      | MM2A                       |
|    17   |         |         | standard | standard | MM1A                      | MM2A                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a>Få mere at vide om, hvilken tilknytning der bruges i udførelsen af et ER-format

### <a name="configure-er-user-parameters"></a>Konfigurere ER-brugerparametre

1.  På siden **Konfigurationer** skal du i handlingsruden på fanen **KONFIGURATIONER** vælge **Brugerparametre**.
2.  Angv indstillingen **Kør i fejlfindingstilstand** til **Ja**.
4.  Vælg **Ok**.

### <a name="run-the-configured-format"></a>Kør det konfigurerede format

1.  På siden **Konfigurationer** skal du i konfigurationstræet vælge **Format til at lære tilknytninger**.
2.  Gå til oversigtspanelet **Versioner**, og vælg **Kør**.
3.  Vælg **Ok**.

### <a name="review-the-er-debug-log"></a>Gennemse ER-fejlfindingsloggen

1.  I navigationsruden skal du gå til **Moduler \> Organisationsadministration \> Elektronisk rapportering \> Konfiguration af fejlfindingslog**.
2.  Vælg knappen **Genindlæs denne side**.

![ER kører logsiden](./media/RCS-Context-specific-mapping-DebugLog.PNG)

Bemærk, at der er tilføjet en ny post til ER-fejlfindingsloggen for det udførte ER-format. Da feltet **Niveau** i denne post er angivet til **Info**, er posten blot til orientering. Da feltet til Formatkomponent er indstillet til **Tilknytningskonfiguration**, oplyser posten dig om en modeltilknytning, der blev brugt under udførelsen af ER-formatet **Format til at lære tilknytninger** (valgt i feltet **Konfigurationsnavn**). Indholdet i feltet **Genereret tekst** informerer dig om, at tilknytningskomponentet **Tilknytning (FR)**, der findes i konfigurationen **Tilknytning (FR)** er blevet brugt til at køre denne rapport.

## <a name="appendix-1"></a><a name="appendix1"></a> Bilag 1

### <a name="configure-a-sample-data-model"></a>Konfigurer en model til eksempeldata

Log på din RCS-forekomst.

I dette eksempel skal du oprette en konfiguration for eksempelfirmaet, Litware Inc. For at fuldføre disse trin skal du i RCS først fuldføre disse trin i proceduren [Opret en konfigurationsudbyder, og markér den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

#### <a name="create-an-er-data-model-configuration"></a>Opret en ER-datamodelkonfiguration

1.  Vælg **Elektronisk rapportering** på standarddashboardet.
2.  Vælg feltet **Rapporteringskonfigurationer**.
3.  På siden **Konfigurationer** skal du vælge **Opret konfiguration**.
4.  I feltet **Navn** i rulledialogboksen skal du angive **Model til at lære tilknytninger**.
5.  Vælg **Opret konfiguration**.
6.  Vælg oversigtspanelet **Konfigurationskomponenter**.

Bemærk, at konfigurationen af kladdeversion 1 af denne ER konfiguration er klar til redigering. Denne version indeholder datamodelkomponenten.

#### <a name="design-a-sample-data-model"></a>Design en model til eksempeldata

1.  På siden **Konfigurationer** skal du vælge **Designer**.
2.  Vælg **Ny**.
3.  Gå til rulledialogboksen, og angiv i feltet **Navn** **Indgangspunkt 1**.
4.  Vælg **Tilføj**.
5.  Vælg **Ny**.
6.  I feltet **Navn** i rulledialogboksen skal du angive **Beskrivelse af funktionalitet**.
7.  Vælg **Tilføj**.
8.  Vælg **Ny**.
9.  I feltgruppen **Ny node** i rulledialogboksen skal du vælge **Modelrod**.
10. I feltet **Navn** skal du angive **Indgangspunkt 2**.
11. Vælg **Indgangspunkt 2**.
12. Vælg **Tilføj**.
13. Vælg **Ny**.
14. I feltet **Navn** i rulledialogboksen skal du angive **Beskrivelse af funktionalitet**.
15. Vælg **Tilføj**.

    ![Side for ER-datamodeldesigner](./media/RCS-Context-specific-mapping-Model.PNG)

16. Vælg **Gem**.
17. Luk siden.

#### <a name="complete-the-modified-version-of-the-model-configuration"></a>Fuldfør den ændrede version af modelkonfigurationen

1.  På siden **Konfigurationer** i oversigtspanelet **Versioner** skal du vælge **Skift status**.

    > Skift status for modelkonfigurationen, der er designet ud fra **Kladde**, til **Fuldført**, så den kan bruges til at designe de nødvendige modeltilknytninger og formater.

2.  Vælg **Fuldfør**.
3.  Vælg **OK**.

Læg mærke til, at den konfiguration, du oprettede, gemmes som fuldført version 1.

### <a name="configure-a-sample-model-mapping"></a>Konfigurer et eksempel for modeltilknytning

#### <a name="create-an-er-model-mapping-configuration"></a>Opret en ER-modeltilknytningskonfiguration

1.  På siden **Konfigurationer** skal du vælge **Opret konfiguration**.
2.  Gå til rulledialogboksen, og vælg i feltgruppen **Ny** **Modeltilknytning baseret på datamodel Model til at lære tilknytninger**.
3.  I feltet **Navn** skal du angive **Tilknytning (generel)**.
4.  I feltet **Definition af datamodel** skal du vælge **Indgangspunkt 1**.
5.  Vælg **Opret konfiguration**.

Bemærk, at konfigurationen af kladdeversion 1 af denne ER konfiguration er klar til redigering. Denne version indeholder komponenten modeltilknytning.

#### <a name="design-a-sample-model-mapping"></a>Design et eksempel for modeltilknytning

1.  På siden **Konfigurationer** skal du vælge **Designer**.

    Bemærk, at modeltilknytningen af retningstypen **Til model** automatisk er tilføjet til denne komponent for definitionen **Indgangspunkt 1**.
    
2.  Vælg **Designer** for at begynde at redigere den tilføjede modeltilknytning.
3.  I sektionen **Datamodel** skal du vælge **Rediger**.
4.  I feltet **Formel** skal du angive **"Generisk funktionalitet 1"**.
5.  Vælg **Gem**.
6.  Luk siden **Formeldesigner**.

    ![Side for ER-modeltilknytningsdesigner](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  Vælg **Gem**.
8.  Luk siden **Modeltilknytningsdesigner**.
9.  Vælg **Ny**.
10. I feltet **Definition** skal du vælge **Indgangspunkt 2**.
11. I feltet **Navn** skal du angive **Tilknytning (generel) 2**.
12. Vælg **Designer**.
13. I sektionen **Datamodel** skal du vælge **Rediger**.
14. I feltet **Formel** skal du angive **"Generisk funktionalitet 2"**.
15. Vælg **Gem**.
16. Luk siden **Formeldesigner**.

    ![Side for ER-modeltilknytningsdesigner](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. Vælg **Gem**.
18. Luk siden **Modeltilknytningsdesigner**.

    ![Side med ER-modeltilknytninger](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. Luk siden **Modeltilknytninger**.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Fuldfør den ændrede version af konfiguration af modeltilknytning

1.  På siden **Konfigurationer** i oversigtspanelet **Versioner** skal du vælge **Skift status**.

    > Skift status for konfigurationen af den modeltilknytning, der er designet ud fra **Kladde**, til **Fuldført**, så den kan bruges af ER-formater.

2.  Vælg **Fuldfør**.
3.  Vælg **OK**.

Læg mærke til, at den konfiguration, der blev oprettet, gemmes som fuldført version 1.

### <a name="configure-a-sample-format"></a>Konfigurer et eksempelformat

#### <a name="create-an-er-format-configuration"></a>Opret en ER-formatkonfiguration

1.  På siden **Konfigurationer** skal du i konfigurationstræet vælge **Model til at lære tilknytninger**.
2.  Vælg **Opret konfiguration**.
3.  I dialogboksen for rullelisten skal du i feltgruppen **Ny** vælge **Format baseret på datamodel Model til at lære tilknytninger**.
4.  Gå til feltet **Navn**, og angiv **Format til at lære tilknytninger**.
5.  I feltet **Definition af datamodel** skal du vælge **Indgangspunkt 1**.
6.  Vælg **Opret konfiguration**.

Bemærk, at konfigurationen af kladdeversion 1 af denne ER konfiguration er klar til redigering. Denne version indeholder komponenten format.

#### <a name="design-a-sample-format"></a>Design et eksempelformat

1.  På siden **Konfigurationer** skal du vælge **Designer**.
2.  Vælg **Tilføj rod**.
3.  I gruppen **Tekst** skal du vælge elementet **Streng**.
4.  Vælg **OK**.

#### <a name="bind-format-elements-to-a-data-source"></a>Kæd formatelementer til en datakilde

1.  På siden **Formatdesigner** under fanen **Tilknytning** kan du udvide datakilden for modellen.
2.  Vælg feltet **Beskrivelse af funktionalitet**.
3.  Vælg **Bind**.

    ![Side med ER-formatdesigner](./media/RCS-Context-specific-mapping-Format.PNG)

4.  Vælg **Gem**.
5.  Luk siden.

## <a name="appendix-2"></a><a name="appendix2"></a> Bilag 2

### <a name="configure-a-sample-model-mapping-for-general-customization"></a>Konfigurer et eksempel på modeltilknytning til generel tilpasning

Det kan være en god ide at tilpasse en modeltilknytning, som en konfigurationsudbyder (partner) har leveret til dig, og derefter bruge den tilpassede version som datakilde til dine ER-formater. I dette tilfælde skal du oprette en brugerdefineret konfiguration af ER-modeltilknytningen for at foretage de nødvendige ændringer i eksisterende modeltilknytninger. I procedurerne i dette bilag anvendes modeltilknytningen **Tilknytning (generel)** som et eksempel.

#### <a name="create-an-er-model-mapping-configuration"></a>Opret en ER-modeltilknytningskonfiguration

1.  På siden **Konfigurationer** skal du i konfigurationstræet vælge **Tilknytning (generel)**.
2.  Vælg **Opret konfiguration**.
3.  I dialogboksen for rullelisten skal du i feltgruppen **Ny** vælge **Afledt fra Navn: Tilknytning (generel), Litware, Inc.**.
4.  I feltet **Navn** skal du angive **Tilpasset tilknytning (generel)**.
5.  Vælg **Opret konfiguration**.

Bemærk, at konfigurationen af kladdeversion 1 af denne ER konfiguration er klar til redigering.

#### <a name="design-a-sample-model-mapping"></a>Design et eksempel for modeltilknytning

1.  På siden **Konfigurationer** skal du vælge **Designer**.

    > Bemærk, at modeltilknytningerne i basiskonfigurationen automatisk er blevet kopieret til denne konfiguration.

2.  Vælg tilknytningen **Kopi af tilknytning (generel)**.
3.  Vælg **Designer**.
4.  I sektionen **Datamodel** skal du vælge **Rediger**.
5.  I feltet **Formel** skal du angive **"Tilpasset generisk funktionalitet 1"**.
6.  Vælg **Gem**.
7.  Luk siden.

    ![Side for ER-modeltilknytningsdesigner](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  Vælg **Gem**.
9.  Luk siden.
10. Vælg tilknytningen **Kopi af tilknytning (generel) 2**.
11. Vælg **Designer**.
12. I sektionen **Datamodel** skal du vælge **Rediger**.
13. I feltet **Formel** skal du angive **"Tilpasset generisk funktionalitet 2"**.
14. Vælg **Gem**.
15. Luk siden.

    ![Side for ER-modeltilknytningsdesigner](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. Vælg **Gem**.
17. Luk siden.

    ![Side med ER-modeltilknytninger](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. Luk siden.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Fuldfør den ændrede version af konfiguration af modeltilknytning

1.  På siden **Konfigurationer** i oversigtspanelet **Versioner** skal du vælge **Skift status**.

    > Skift status for konfigurationen af den modeltilknytning, der er designet ud fra **Kladde**, til **Fuldført**, så den kan bruges af ER-formater.

2.  Vælg **Fuldfør**.
3.  Vælg **OK**.

Læg mærke til, at den konfiguration, der blev oprettet, gemmes som fuldført version 1.

## <a name="appendix-3"></a><a name="appendix3"></a> Bilag 3

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a>Konfigurer et eksempel på modeltilknytning til land/område-specifik tilpasning

For visse ER-formater kan der være land/område-specifikke krav til dataforberedelse. I dette tilfælde kan du administrere en konfiguration for en separat ER-modeltilknytning og isolere implementeringen af disse land/område-specifikke krav fra den generelle implementering. I procedurerne i dette bilag anvendes ER-formatet **Format til at lære tilknytninger** og krav specifikke for fransk som eksempel.

#### <a name="create-an-er-model-mapping-configuration"></a>Opret en ER-modeltilknytningskonfiguration

Først skal du oprette en ny konfiguration af ER-modeltilknytningen for at implementere de land/område-specifikke krav. Brug din brugerdefinerede konfiguration for ER-modeltilknytning som basis.

1.  På siden **Konfigurationer** skal du i konfigurationstræet vælge **Tilpasset tilknytning (generel)**.
2.  Vælg **Opret konfiguration**.
3.  I dialogboksen for rullelisten skal du i feltgruppen **Ny** vælge **Afledt fra Navn: Tilpasset tilknytning (generel), Litware, Inc.**.
4.  I feltet **Navn** skal du angive **Tilknytning (FR)**.
5.  Vælg **Opret konfiguration**.

Bemærk, at konfigurationen af kladdeversion 1 af denne ER konfiguration er klar til redigering.

#### <a name="design-a-sample-model-mapping"></a>Design et eksempel for modeltilknytning

1.  På siden **Konfigurationer** skal du vælge **Designer**.

    > Bemærk, at modeltilknytningerne i basiskonfigurationen automatisk er blevet kopieret til denne konfiguration.

2.  Vælg tilknytningen **Kopi af kopi af tilknytning (generel)**.
3.  Omdøb den til **Tilknytning (FR)**.
4.  Vælg **Designer**.
5.  I sektionen **Datamodel** skal du vælge **Rediger**.
6.  I feltet **Formel** skal du angive **"FR-funktionalitet 1"**.
7.  Vælg **Gem**.
8.  Luk siden.

    ![Side for ER-modeltilknytningsdesigner](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  Vælg **Gem**.
10. Luk siden.
11. Vælg tilknytningen **Kopi af kopi af tilknytning (generel) 2**.
12. Omdøb den til **Tilknytning (FR) 2**.
13. Vælg **Designer**.
14. I sektionen **Datamodel** skal du vælge **Rediger**.
15. I feltet **Formel** skal du angive **"FR-funktionalitet 2"**.
16. Vælg **Gem**.
17. Luk siden.

    ![Side for ER-modeltilknytningsdesigner](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. Vælg **Gem**.
19. Luk siden.

    ![Side med ER-modeltilknytninger](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. Luk siden.

#### <a name="specify-countryregion-context-restrictions-for-use"></a>Angiv brugen af land/område-kontekstbegrænsningerne

1.  På siden **Konfigurationer** skal du i oversigtspanelet **ISO-land/område-koder** vælge **Ny**.
2.  I feltet **ISO** skal du vælge **FR**.
3.  Vælg **Gem**.

Bemærk, at du skal logge på et bestemt regnskab i Finance for at køre et ER-format. Derfor kan dette firma betragtes som part, der kontrollerer udførslen af begge ER-formater og valg af korrekt ER-modeltilknytning af den grundlæggende ER-datamodel. Hvis du tilføjer landekoden **FR**, angiver du, at denne modeltilknytning kun er tilgængelig for et ER-format af den grundlæggende datamodel, når det pågældende format køres i forbindelse med kontrol af et firma, der har fransk land/område-kontekst.

Du kan føje flere land/område-koder til en enkelt version af en konfiguration af en ER-modeltilknytning. På denne måde kan modeltilknytninger, der findes i den pågældende konfiguration af en modeltilknytning, bruges af et ER-format, der køres i forbindelse med kontrol af firmaer, der har en anden land/område-kontekst.

Bemærk, at listen over land/område-koder er angivet for hver version af en ER-modeltilknytningskonfiguration og kan variere fra version til version.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Fuldfør den ændrede version af konfiguration af modeltilknytning

1.  På siden **Konfigurationer** i oversigtspanelet **Versioner** skal du vælge **Skift status**.

    > Skift status for konfigurationen af den modeltilknytning, der er designet ud fra **Kladde**, til **Fuldført**, så den kan bruges af ER-formater.

2.  Vælg **Fuldfør**.
3.  Vælg **OK**.

Læg mærke til, at den konfiguration, der blev oprettet, gemmes som fuldført version 1.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Administrere ER-modeltilknytning i separate ER-konfigurationer](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[Anvende land/område-kontekst](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a>Jeg har konfigureret to delte ER-modeltilknytningskonfigurationer i RCS og markeret en af dem som standardkonfigurationen for modeltilknytningen. Jeg har kørt et ER-format, der er oprettet til den samme grundlæggende ER-datamodelkonfiguration, for at teste modeltilknytningerne. Derefter importerede jeg hele ER-løsningen (ER-datamodel, to ER-modeltilknytningskonfigurationer og ER-formatkonfiguration) i Finance. Hvorfor får jeg vist en fejlmeddelelse, når jeg forsøger at køre samme ER-format i Finance?
Standardindstillingen for modeltilknytning er miljøspecifik. Den er konfigureret i RCS, men eksporteres ikke til Finance. For at kunne køre dette ER-format, skal du også markere en af de ER-modeltilknytningskonfigurationer som standardmodeltilknytningskonfiguration i Finance.

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a>Jeg har konfigureret én modeltilknytning som en delt modeltilknytning og fuldført kladdeversionen af den. Derefter har jeg tilføjet en ny modeltilknytningskonfiguration for samme datamodel og konfigureret den specifikt for fransk. Hvorfor er den delte modeltilknytning markeret, når jeg kører et ER-format, selvom dette ER-format bruger den korrekte definition for rodobjekt og udførelse udføres i forbindelse med kontrollen af det firma, der har fransk land/område-kontekst?
Sørg for, at den delte modeltilknytningskonfiguration ikke er markeret som standardmodeltilknytningskonfiguration. Ellers vil den have højere prioritet i forbindelse med udvælgelse af tilknytning. Kontroller også, at den for fransk specificerede modeltilknytningskonfiguration tages i betragtning, når der vælges en tilknytning under udførsel af ER-format. Konfiguration af en ER-modeltilknytning kan kun vælges, hvis mindst én af følgende betingelser er opfyldt:
- Statussen for mindst én version af ER-modeltilknytningkonfiguration er **Fuldført** eller **Delt**. I dette tilfælde bruges den version, der indeholder det højeste versionsnummer, til udførsel af ER-format.
- Indstillingen **Kør kladde** for ER-modeltilknytningkonfiguration er aktiveret. I dette tilfælde bruges den version, der har statussen **Kladde** til udførsel af ER-format.
> Indstillingen **Kør kladde** er tilgængelig på siden **Konfigurationer** for hver enkelt ER-modeltilknytningskonfiguration, når **Indstillingen Kør** ER-brugerparameter er aktiveret.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]