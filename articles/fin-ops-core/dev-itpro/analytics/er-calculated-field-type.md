---
title: Understøtte parameteriserede kald af ER-datakilder for typen Beregnet felt
description: Dette emne indeholder oplysninger om, hvordan du bruger typen Beregnet felt til ER-datakilder.
author: NickSelin
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fb09e1ccd4b2be08e43784330adf4092ca25f5a6
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349154"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a>Understøtte parameteriserede kald af ER-datakilder for typen Beregnet felt

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du kan designe en elektronisk rapport (ER)-datakilde ved at bruge typen **Beregnet felt**. Denne datakilde kan indeholde et ER-udtryk, der, når det udføres, kan styres af værdierne for de parameterargumenter, der er konfigureret i en binding, som kalder denne datakilde. Ved at konfigurere parameteriserede kald af en sådan datakilde kan du genbruge en enkelt datakilde i mange bindinger, hvilket reducerer det samlede antal datakilder, der skal konfigureres i ER-modeltilknytninger eller ER-formater. Det forenkler også den konfigurerede ER-komponent, hvilket reducerer vedligeholdelsesomkostningerne og omkostningerne ved at bruge andre forbrugere.

## <a name="prerequisites"></a>Forudsætninger
Før du kan følge eksemplerne i dette emne, skal du have følgende adgang:

- Adgang til en af disse roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

- Adgang til RCS (Regulatory Configuration Services), der er klargjort til den samme lejer som Finance and Operations for en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

Du skal også hente og lokalt gemme følgende filer.

| **Indhold**                           | **Filnavn**                                        |
|---------------------------------------|------------------------------------------------------|
| Eksempler på ER-datamodelkonfiguration    | [Model til at lære parameteriserede calls.version.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| Eksempler på ER-metadatakonfiguration      | [Metadata til at lære parameteriserede calls.version.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| Eksempler på ER-modeltilknytningskonfiguration | [Tilknytning for at lære parameteriserede calls.version.1.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| Eksempler på ER-formatkonfiguration        | [Format til at lære parameteriserede calls.version.1.1.xml](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a>Log på din RCS-forekomst
I dette eksempel skal du oprette en konfiguration for eksempelfirmaet, Litware Inc. Først skal du i RCS fuldføre disse trin i proceduren [Opret konfigurationsudbydere, og markér dem som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md):

1. Vælg **Elektronisk rapportering** på standarddashboardet.
2. Vælg **Rapporteringskonfigurationer**.
3. Importér de downloadede konfigurationer til RCS i følgende rækkefølge: datamodel, metadata, modeltilknytning, format. Udfør følgende trin for hver ER-konfiguration:

    1. Vælg **Udveksling**.
    2. Vælg **Indlæs fra XML-fil**.
    3. Vælg **Gennemse**, og vælg den krævede ER-konfiguration i XML-format.
    4. Vælg **OK**.

## <a name="review-the-provided-er-solution"></a>Gennemse den leverede ER-løsning

### <a name="review-model-mapping"></a>Gennemse modeltilknytning

1. Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.
2. Vælg **Tilknytning for at lære parameteriserede kald**.
3. Vælg **Designer**.
4. Vælg **Designer**.  
   
    Denne ER-modeltilknytning er beregnet til at gøre følgende:

    - Hent listen over momskoder (**Moms**-datakilde), der findes i **TaxTrans**-tabellen.
    - Hent listen over momstransaktioner (**Trans**-datakilde), der findes i **TaxTrans**-tabellen:
    
        - Grupper listen over hentede transaktioner (**Gr**-datakilde) efter momskode.
        - Beregn for grupperede transaktioner følgende aggregerede værdier pr. momskode:

            - Summen af momsgrundlagsværdier.
            - Summen af momsværdier.
            - Minimumværdi for anvendt momssats.

    Modeltilknytningen i denne konfiguration implementerer basisdatamodellen for ethvert af de ER-formater, der er oprettet for denne model, og udføres i Finance and Operations. Derfor vises indholdet af **Moms**- og **Gr**-datakilderne for ER-formater, f. eks. abstrakte datakilder.

    ![Siden Modeltilknytningsdesigner, der viser moms- og gr-datakilder.](media/er-calculated-field-type-01.png)

5.  Luk siden **Modeltilknytningsdesigner**.
6.  Luk siden **Modeltilknytning**.

### <a name="review-format"></a>Gennemse format

1. Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.
2. Vælg **Format til at lære parameteriserede kald**.
3. Vælg **Designer**. Dette ER-format er designet til at gøre følgende:

    - Generer en momsafstemning i XML-format.
    - Præsenter følgende beskatningsniveauer i momsangivelsen: normal, reduceret og ingen.
    - Vis flere detaljer på hvert beskatningsniveau med forskellige antal detaljer inden for hvert niveau.

    ![Siden Formatdesigner.](media/er-calculated-field-type-02.png)

4. Vælg **Tilknytning**.
5. Udvid elementerne **Model**, **Data** og **Resume**. 

    Det beregnede felt **Model.Data.Summary.Level** indeholder det udtryk, der returnerer koden for beskatningsniveauet (**Almindelig**, **Reduceret**, **Ingen** eller **Andet**) som en tekstværdi for enhver momskode, der kan hentes fra **Model.Data.Summary**-datakilden på kørselstidspunktet.

    ![Siden Formatdesigner, der viser oplysninger om datamodellen Model til at lære om parameteriserede kald.](media/er-calculated-field-type-03.png)

6. Udvid elementet **Model**.**Data2**.
7. Udvid elementet **Model**.**Data2.Summary2**.
   
    **Model**.**Data2.Summary2**-datakilden er konfigureret til at gruppere **Model.Data.Summary**-datakildens transaktionsoplysninger efter beskatningsniveau (returneret af det beregnede felt **Model.Data.Summary.Level**) og beregne aggregeringerne.

    ![Siden Formatdesigner, der viser detaljer om Model.Data2.Summary2-datakilden.](media/er-calculated-field-type-04.png)

8. Gennemse de beregnede felter **Model**.**Data2.Level1**, **Model**.**Data2.Level2** og **Model**.**Data2.Level3.** Disse beregnede felter bruges til at filtrere **Model**.**Data2. Summary2**-postlisten og kun returnere poster, der repræsenterer et bestemt beskatningsniveau.
9. Luk siden **Formatdesigner**.

## <a name="create-a-derived-format"></a>Oprette et afledt format
Du kan forbedre det angivne format ved at tilføje et beregnet felt til at filtrere det krævede beskatningsniveau i stedet for at bruge de tre eksisterende felter: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** og **Model**.**Data2.Level3**. Det krævede beskatningsniveau kan angives på den placering, hvor dette nye beregnede felt skal kaldes.

1. Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.
2. Vælg **Format til at lære parameteriserede kald**.
3. Vælg **Opret konfiguration**.
4. Vælg **Afledt fra navn: Format til at lære parameteriserede kald, Microsoft**.
5. Gå til feltet **Navn**, og angiv **Format til at lære parameteriserede kald (brugerdefineret)**.
6. Vælg **Opret konfiguration**.

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a>Konfigurer et beregnet felt med parametre, der returnerer en liste over poster

### <a name="start-adding-a-new-calculated-field"></a>Begynd tilføjelse af et nyt beregnet felt

1. Vælg **Designer**.
2. Vælg **Udvid/skjul** for at udvide alle formatelementer.
3. Vælg **Tilknytning**.
4. Udvid elementet **Model**.
5. Vælg elementet varen **Model.Data2**.
6. Vælg **Tilføj**.
7. Vælg **Funktioner\\Beregnet felt**.
8. I feltet **Navn** skal du skrive **Niveauer**.
9. Vælg **Rediger formel**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Definer en parameter til tilføjelse af et beregnet felt

1. Vælg **Parametre**.
2. Vælg **Ny**.
3. I feltet **Navn** skal du angive **Beskatningsniveau**.
4. I feltet **Type** skal du vælge **Streng**.

    Der kan kun bruges primitive datatyper til at angive typen af parameterens argument. Derfor kan typerne **Postliste**, **Post** og **Fastteksttype** ikke bruges til dette formål.

    Det maksimale antal parametre, der kan angives for et enkelt beregnet felt, er 8.

    ![Datakildeliste for parameter.](media/er-calculated-field-type-05.png)

5. Vælg **OK**.

Hvis du tilføjer denne parameter, angiver du den betingelse, der skal være angivet for at kalde dette beregnede felt. Når du kalder dette beregnede felt, skal du angive argumentet for parameteren for **Beskatningsniveau** som en værdi med formatet **Streng**.

   Sørg for, at du kun definerer parametre for de beregnede felter, der er placeret i en container (enten **Postliste**, **Post** eller **Container**).

   Den konfigurerede parameter er tilgængelig på listen over datakilder for dette beregnede felt. Du kan føje parameteren til det konfigurerede udtryk ved at vælge **Tilføj datakilde**.

   ![Datakildefelter.](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Definer et udtryk for tilføjelse af et beregnet felt

1. I feltet **Formel** skal du angive: 

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level =**
    
2. Vælg parameteren **Beskatningsniveau** på listen over datakilder.
3. Vælg **Tilføj datakilde**.
4. I feltet **Formel** skal du fuldføre udtrykket som:  

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Beskatningsniveau')**

5. Vælg **Gem**.

    ![Oplysninger om datakildefelt.](media/er-calculated-field-type-07.png)

6. Luk siden **Formeldesigner**.

### <a name="finish-adding-a-new-calculated-field"></a>Afslut tilføjelse af et nyt beregnet felt

- Vælg **OK**.

På siden **Formatdesigner** kræver det konfigurerede beregnede felt med parametre **Niveauer** et **Streng**-argument.

![Udvidet liste over beregnede feltniveauer.](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a>Brug det konfigurerede beregnede felt til bindingsformatelementer

1. Vælg **Model.Data2.Levels** for at vælge det konfigurerede beregnede felt.
2. Vælg formatelementet **Statement.Taxation.Regular**.
3. Vælg **Bind**.
4. Vælg **Ja** for at bekræfte erstatningen af den aktuelt anvendte datakilde **Level1** med den nye datakilde **Niveauer** i alle indlejrede formatelementer i det valgte formatelement.

    Den anvendte binding er oprettet som et kald af det beregnede felt med parametre. Navnet på det bundne formatelement bruges som et argument for det beregnede felt med parametre under følgende betingelser:

      - Det beregnede felt er konfigureret til at bruge en enkelt parameter.
      - Datatypen for denne parameter er defineret som **Streng**.

    Når navnet på det bundne formatelement er tomt, bruges datakildens navn for dette element i anvendt binding.

5. Vælg formatelementet **Statement.Taxation.Reduced**.
6. Vælg **Bind**.
7. Vælg **Ja** for at bekræfte erstatningen af den aktuelt anvendte datakilde **Level2** med den nye datakilde **Niveauer** i alle indlejrede formatelementer under det valgte formatelement.
8. Vælg formatelementet **Statement.Taxation.None**.
9. Vælg **Bind**.
10. Vælg **Ja** for at bekræfte erstatningen af den aktuelt anvendte datakilde, **Level3** med den nye datakilde **Niveauer** i alle indlejrede formatelementer under det valgte formatelement.

   Når du angiver argumentet for det beregnede felt med parametre for det XML-element, der repræsenterer beskatningsniveau (f.eks. **Model.Data2.Levels("Reduced")** som en tekstværdi), behøver du ikke gøre det samme for indlejrede XML-attributter – deres bindinger overtager automatisk værdien af det argument, der er defineret på det overordnede niveau (**Model.Data2.Levels.aggregated.Base**, ikke **Model.Data2.Levels("Reduced").aggregated.Base**).

Tilbagevendende kald af beregnet felt med parametre understøttes ikke.

Du kan vælge **Rediger formel** og ændre det anvendte argument, der er angivet som standard, i det beregnede felt med parametre i den valgte binding. Hvis dette argument mangler, kan det medføre fejl på procestiden – brugerne får besked om denne situation, når det aktuelle format er valideret.

![Meddelelse om valideringsadvarsel.](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a>Konfigurer et beregnet felt med parametre til at returnere en post
Når et beregnet felt med parametre returnerer en post, skal du understøtte binding af individuelle felter i denne post for at formatere elementer. I sådanne tilfælde vil der ikke være nogen overordnet binding, der indeholder værdien af et argument til kald af et beregnet felt med parametre – denne værdi skal defineres i bindingen for en enkelt posts felt.

### <a name="start-adding-a-new-calculated-field"></a>Begynd tilføjelse af et nyt beregnet felt

1. Vælg elementet varen **Model.Data2**.
2. Vælg **Tilføj**.
3. Vælg **Funktioner\\Beregnet felt**.
4. I feltet **Navn** skal du skrive **LevelRecord**.
5. Vælg **Rediger formel**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Definer en parameter til tilføjelse af et beregnet felt

1. Vælg **Parametre**.
2. Vælg **Ny**.
3. I feltet **Navn** skal du angive **Beskatningsniveau**.
4. I feltet **Type** skal du vælge **Streng**.
5. Vælg **OK**.

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Definer et udtryk for tilføjelse af et beregnet felt

1. I feltet **Formel** skal du angive følgende udtryk:  
    
    **FIRSTORNULL(\@.Levels(**

2. Vælg parameteren **Beskatningsniveau**.
3. Vælg **Tilføj datakilde**.
4. I feltet **Formel** skal du føje **'Beskatningsniveau'))** til det, du har angivet i trin 1, for at afslutte udtrykket til:  
    
    **FIRSTORNULL(\@.Levels('Beskatningsniveau'))**

5. Vælg **Gem**.
6. Luk siden **Formeldesigner**.

### <a name="finish-adding-a-new-calculated-field"></a>Afslut tilføjelse af et nyt beregnet felt

-   Vælg **OK**.

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a>Brug det konfigurerede beregnede felt for at binde formatelementer

1. Udvid **Model.Data2.LevelRecord** for at vælge det konfigurerede beregnede felt.
2. Udvid containeren **Model.Data2.LevelRecord.aggregated** for det konfigurerede beregnede felt.
3. Vælg feltet **Model.Data2.LevelRecord.aggregated.Base**.
4. Vælg formatelementet **Statement.Taxation.None**.
5. Vælg **Ophæv binding**.
6. Vælg formatelementet **Statement.Taxation.None.Base**.
7. Vælg **Bind**.
8. Vælg **Rediger formel**.
9. Skift udtrykket til **Model.Data2.LevelRecord("None").aggregated.Base**.

![Opdateret udtryk.](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a>Fjerne beregnede felter, der ikke bruges

1. Vælg **Model.Data2.Level1**.
2. Vælg **Slet**.
3. Vælg **Model.Data2.Level2**.
4. Vælg **Slet**.
5. Vælg **Model.Data2.Level3**.
6. Vælg **Slet**.
7. Vælg **Gem**.

  > [!NOTE]
  > Du har genbrugt det samme beregnede felt **Model.Data2.Levels** flere gange i formatbindinger. Det er meget lettere at bruge og vedligeholde et enkelt beregnet felt i stedet for at gøre dette for flere ens felter.

8. Luk siden **Formatdesigner**.

## <a name="complete-adjusted-version-of-a-derived-format"></a>Fuldfør tilpasset version af et afledt format

1. I oversigtspanelet **Versioner** skal du vælge **Skift status**.
2. Vælg **Fuldfør**.

## <a name="export-completed-version-of-a-derived-format"></a>Eksportér fuldført version af et afledt format

1. Vælg **Format til at lære parameteriserede kald (brugerdefineret)** i konfigurationstræet.
2. I oversigtspanelet **Versioner** skal du vælge den fuldførte version 1.1.1.
3. Vælg **Udveksling**.
4. Vælg **Eksporter som XML-fil**.
5. Gem den hentede konfiguration lokalt i XML-format.

## <a name="test-er-formats"></a>Test ER-formater 
Du kan køre det første og det forbedrede ER-format for at sikre dig, at konfigurerede parameteriserede beregnede felter fungerer korrekt.

### <a name="import-er-configurations"></a>Importér ER-konfigurationer
Du kan importere evaluerede konfigurationer fra RCS ved hjælp af ER-lageret af typen **RCS**. Hvis du allerede har gennemgået trinnene i emnet, kan du [Importere konfigurationer af Elektronisk rapportering (ER) fra Regulatory Configuration Services (RCS)](rcs-download-configurations.md), og bruge det konfigurerede ER-lager til at importere konfigurationer, der er beskrevet tidligere i dette emne, for dit miljø. Ellers kan du udføre disse trin:

1. Vælg **DEMF**-firma, og vælg **Elektronisk rapportering** i standarddashboardet.
2. Vælg **Rapporteringskonfigurationer**.
3. Importér konfigurationer fra Microsoft Download Center i følgende rækkefølge: datamodel, modeltilknytning, format. Udfør følgende trin for hver ER-konfiguration:

    1. Vælg **Udveksling**.
    2. Vælg **Indlæs fra XML-fil**.
    3. Vælg **Gennemse** for at vælge den krævede ER-konfiguration i XML-format.
    4. Vælg **OK**.

4. Importér de eksporterede fra den fuldførte RCS version 1.1.1 i formatet **Format til at lære parameteriserede kald (brugerdefineret)**:

    1. Vælg **Udveksling**.
    2. Vælg **Indlæs fra XML-fil**.
    3. Vælg **Gennemse** for at vælge den lokalt lagrede fil for **Format til at lære parameteriserede kald (brugerdefineret)** i XML-format.
    4. Vælg **OK**.

### <a name="run-er-formats"></a>Kør ER-formater

1. Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.
2. Vælg **Format til at lære parameteriserede kald**.
3. Vælg **Kør** på det øverste niveau af båndet.
4. Gem det lokalt oprettede output.
5. Vælg emnet **Format til at lære parameteriserede kald (brugerdefineret)**.
6. Vælg **Kør** på det øverste niveau af båndet.
7. Gem det oprettede output lokalt. 
8. Sammenlign indholdet af de genererede output.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Formeldesigner i elektronisk rapportering (ER)](general-electronic-reporting-formula-designer.md)
- [Forbedre ydeevnen af ER-løsninger ved at tilføje parameteriserede BEREGNET FELT-datakilder](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]