---
title: Konfigurere parametrene for et ER-format for hver juridisk enhed
description: Denne artikel forklarer, hvordan du kan konfigurere parametrene for det Elektroniske rapporteringsformat, der er angivet for den enkelte juridiske enhed.
author: kfend
ms.date: 03/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
ms.openlocfilehash: 4b2e91e43938b71b78a4b7bc57b5b16ca174b1b7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291386"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>Konfigurer parametrene for et ER-format for hver juridisk enhed

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a>Forudsætninger

For at fuldføre disse trin, skal du først fuldføre trinnene i [Konfigurer ER-formaterne for at bruge de parametre, der er angivet for hver juridiske enhed](er-app-specific-parameters-configure-format.md).

For at fuldføre eksemplerne i denne artikel, skal du have adgang til Microsoft Dynamics 365 Finance i en af følgende roller:

- Udvikler til elektronisk rapportering
- Funktionel konsulent i elektronisk rapportering
- Systemadministrator

## <a name="import-er-configurations"></a>Importér ER-konfigurationer
Benyt følgende fremgangsmåde for at importere ER-konfigurationer: 

1. Log på dit miljø.
2. Vælg **Elektronisk rapportering** på standarddashboardet.
3. Vælg **Rapporteringskonfigurationer**.
4. Importer de konfigurationer, du har eksporteret fra Regulatory Configuration Services (RCS), i den aktuelle forekomst af Finance, mens du fuldførte trinnene i [Konfigurer ER-formater, så du kan bruge de parametre, der er angivet for hver juridiske enhed](er-app-specific-parameters-configure-format.md). Benyt følgende fremgangsmåde for hver enkelt konfiguration af [Elektronisk rapportering (ER)](general-electronic-reporting.md) i følgende rækkefølge: datamodel, modeltilknytning og formater.

    1. Vælg **Udveksling \> Indlæs fra XML-fil**.
    2. Vælg **Gennemse** for at vælge filen til den krævede ER-konfiguration i XML-format.
    3. Vælg **OK**.

    I følgende illustration vises de konfigurationer, du skal have, når du er færdig.

    ![Siden ER-konfigurationer.](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>Angiv parametrene for DEMF-firmaet

Du kan bruge ER-strukturen til at konfigurere programspecifikke parametre for et ER-format.

1. Vælg den juridiske enhed **DEMF**.
2. I konfigurationstræet skal du vælge elementet **Format for at lære, hvordan man slår LE-data op**.
3. I handlingsruden på fanen **Konfigurationer** skal du i gruppen **Programspecifikke parametre** vælge **Opsætning**.

    ![Er-programspecifik parameterside til opsætning af parametre.](./media/GER-AppSpecParms-LookupForm.PNG)

    På siden **Programspecifikke parametre** kan du konfigurere reglerne for datakilden **Vælger** for formatet **Format til at lære, hvordan man leder efter LE-data**.

    Hvis basis-ER-formatet indeholder flere datakilder af typen **Opslag**, skal du vælge den ønskede datakilde i oversigtspanelet **Opslag**, før du kan konfigurere regelsættet for datakilden.

    For hver datakilde kan du konfigurere separate regler for hver version af det valgte ER-format.

    Hele regelsættet for alle opslagsdatakilder, der er tilgængelige i den valgte version af basis-ER-formatet, udgør de programspecifikke parametre for ER-formatet.

4. Vælg version **1.1.1** af ER-formatet.
5. Vælg **Tilføj** i oversigtspanelet **Betingelser**.
6. I feltet **Kode** for den nye post skal du vælge rullelistens pil for at åbne opslaget.

    Opslaget viser listen over de momskoder, der kan vælges. Denne liste returneres af datakilden **Model.Data.Moms**, der er konfigureret i basis-ER-formatet. Da denne datakilde indeholder feltet **Navn**, vises navnet på hver momskode i opslaget.

    ![Kodefelt-opslag på siden med ER-programspecifikke parametre.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)

7. Vælg momskoden **MOMS19**.
8. I feltet **Opslagsresultat** for den nye post skal du vælge rullelistens pil for at åbne opslaget. Opslaget viser listen over værdier for fasttekstformatet Beskatningsniveau, som du kan markere.

    Bemærk, at hvis tysk er valgt som det foretrukne sprog for den bruger, du er logget på som, vil etiketterne for værdierne i opslaget være på tysk, hvis de er blevet oversat i basis-ER-formatet. Hvis etiketten for en opslagsdatakilde er oversat, vil denne etiket endvidere blive vist på brugerens foretrukne sprog under fanen **Opslag**.

    ![Opslagsfeltet oversat til tysk på ER-programspecifik parameterside.](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9. Vælg værdien for **Almindelig moms**.

    Når du tilføjer denne post, skal du definere følgende regel: Når der anmodes om opslagsdatakilden **Vælger**, og momskoden **MOMS19** sendes som et argument, returneres **Almindelig beskatning** som det ønskede beskatningsniveau.

10. Vælg **Tilføj**, og følg derefter følgende fremgangsmåde:

    1. I feltet **Kode** skal du vælge momskoden **InMOMS19**.
    2. I feltet **Opslagsresultat** skal du vælge værdien **Almindelig beskatning**.

11. Vælg **Tilføj**, og følg derefter følgende fremgangsmåde:

    1. I feltet **Kode** skal du vælge momskoden **MOMS7**.
    2. I feltet **Opslagsresultat** skal du vælge værdien **Reduceret beskatning**.

12. Vælg **Tilføj**, og følg derefter følgende fremgangsmåde:

    1. I feltet **Kode** skal du vælge momskoden **InMOMS7**.
    2. I feltet **Opslagsresultat** skal du vælge værdien **Reduceret beskatning**.

13. Vælg **Tilføj**, og følg derefter følgende fremgangsmåde:

    1. I feltet **Kode** skal du vælge momskoden **TREDJE**.
    2. I feltet **Opslagsresultat** skal du vælge værdien **Ingen beskatning**.

14. Vælg **Tilføj**, og følg derefter følgende fremgangsmåde:

    1. I feltet **Kode** skal du vælge momskoden **InMOMS0**.
    2. I feltet **Opslagsresultat** skal du vælge værdien **Ingen beskatning**.

15. Vælg **Tilføj**, og følg derefter følgende fremgangsmåde:

    1. I feltet **Kode** skal du vælge indstillingen **\*Ikke tom\***.
    2. I feltet **Opslagsresultat** skal du vælge værdien **Andet**.

    Når du tilføjer denne sidste post, skal du definere følgende regel: Når den momskode, der er videregivet som argument, ikke opfylder nogle af de tidligere regler, vil opslagsdatakilden returnere **Andet** som det ønskede beskatningsniveau.

    ![Sidste post tilføjet på siden med ER-programspecifikke parametre.](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)

16. I feltet **Tilstand** skal du vælge **Fuldført**.

    Når du kører en version af ER-formatet, der har status som enten **Fuldført** eller **delt**, skal dette regelsæt være i tilstanden **Fuldført**. Ellers vil udførelsen af basis-ER-formatet blive afbrudt, når formatet forsøger at indlæse data fra dette regelsæt, mens opslagsdatakilden **Vælger** køres.

    Når du kører en version af ER-formatet, der har statussen **Kladde**, har basis-ER-formatet adgang til dette regelsæt, uanset dets tilstand.

17. Vælg **Gem**.
18. Luk siden med **Programspecifikke parametre**.

## <a name="run-the-er-format-in-the-demf-company"></a>Kør ER-formatet i DEMF-firmaet
Udfør følgende trin for at køre ER-formatet i DEMF-firmaet: 

1. I konfigurationstræet skal du vælge elementet **Format for at lære, hvordan man slår LE-data op**.
2. Vælg **Kør** i handlingsruden.
3. Vælg **OK** i dialogboksen, der vises.
4. Hent den opgørelse, der genereres, og gem den lokalt.

    I den genererede opgørelse bemærker du, at opsummeringen af momskoden **InMOMS7** er sat til niveauet **Reduceret**, og opsummeringerne af momskoderne **MOMS19** og **InMOMS19** er sat til niveauet **Almindelig**. Denne funktionsmåde bestemmes af konfigurationen i det regelsæt, der er afhængig af den juridiske enhed.

5. Gå til **Moms \> Indirekte skatter \> Moms \> Momskoder**.
6. Vælg momskoden **InMOMS7**.
7. I handlingspanelet skal du på fanen **Momskode** i gruppen **Forespørgsler** vælge **Bogført moms** for at få vist oplysninger om momsværdien og den anvendte momssats per momskode.

    ![Siden Bogført moms.](./media/GER-AppSpecParms-Statement.PNG)

8. Luk siden **Bogført moms**.

## <a name="set-up-parameters-for-the-usmf-company"></a>Angiv parametrene for USMF-firmaet
Udfør følgende trin for at konfigurere parametre for firmaet USMF: 

1. Vælg den juridiske enhed **USMF**.
2. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
3. I konfigurationstræet skal du udvide elementet **Model til at lære parameteriserede kald**, udvide elementet **Format til at lære parameteriserede kald** og vælge formatet **Format til at lære, hvordan man leder efter LE-data**.
4. I handlingsruden på fanen **Konfigurationer** skal du i gruppen **Programspecifikke parametre** vælge **Opsætning**.
5. Vælg version **1.1.1** af det valgte ER-formatet.
6. Vælg **Tilføj** i oversigtspanelet **Betingelser**.
7. I feltet **Kode** for den nye post skal du vælge rullelistens pil for at åbne opslaget.

    Opslaget indeholder nu listen over momskoder for den **USMF**-virksomhedsmoms, der skal vælges.

    ![Momskoder for firmaet USMF.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)

8. Vælg momskoden **UNDTAGET**.
9. I feltet **Opslagsresultat** for den nye post skal du vælge værdien **Ingen beskatning**.
10. Vælg **Tilføj**.
11. I feltet **Kode** for den nye post skal du vælge indstillingen **\*Ikke tom\***.
12. I feltet **Opslagsresultat** for den nye post skal du vælge værdien **Almindelig beskatning**.
13. I feltet **Tilstand** skal du vælge **Fuldført**.
14. Vælg **Gem**.

    ![Siden med ER-programspecifikke parametre.](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)

15. Luk siden med **Programspecifikke parametre**.

## <a name="run-the-er-format-in-the-usmf-company"></a>Kør ER-formatet i USMF-firmaet
Udfør følgende trin for at køre ER-formatet i USMF-firmaet:

1. I konfigurationstræet skal du vælge elementet **Format for at lære, hvordan man slår LE-data op**.
2. Vælg **Kør** i handlingsruden.
3. Vælg **OK** i dialogboksen, der vises.
4. Hent den opgørelse, der genereres, og gem den lokalt.

    Bemærk, at du nu har genbrugt det samme ER-format for en anden juridisk enhed i den genererede opgørelse, men uden at foretage nogle justeringer af ER-formatet.

## <a name="reuse-legal-entitydependent-parameters"></a>Genbrug de juridisk enhedsafhængige parametre

### <a name="duplicate-existing-parameters"></a>Duplikere eksisterende parametre

#### <a name="export-parameters"></a>Eksporter parametre
Hvis du vil eksportere parametre, skal du benytte følgende fremgangsmåde:

1. Gå til **Virksomhedsadministration \> Arbejdsområder \> Elektronisk rapportering**.
2. Vælg **Rapporteringskonfigurationer**.
3. I konfigurationstræet skal du vælge elementet **Format for at lære, hvordan man slår LE-data op**.
4. I handlingsruden på fanen **Konfigurationer** skal du i gruppen **Programspecifikke parametre** vælge **Opsætning**.
5. Vælg version **1.1.1** af ER-formatet.
6. Vælg **Eksporter** i handlingsruden.
7. Hent den fil, der genereres, og gem den lokalt.

    Det konfigurerede sæt af programspecifikke parametre er nu eksporteret som en XML-fil.

#### <a name="import-parameters"></a>Importer parametre
Hvis du vil importere parametre, skal du benytte følgende fremgangsmåde:

1. Vælg version **1.1.2** af ER-formatet.
2. Vælg **Importér** i handlingsruden.
3. Vælg **Ja** for at bekræfte, at du vil overskrive de eksisterende programspecifikke parametre for denne formatversion.
4. Vælg **Gennemse** for at finde den fil, der indeholder de eksporterede programspecifikke parametre for version **1.1.1**.
5. Vælg **OK**.

    Version **1.1.2** af ER-formatet har nu de samme programspecifikke parametre, som du oprindeligt konfigurerede for version **1.1.1**.

##### <a name="applicability-considerations"></a>Overvejelser omkring anvendelighed

De programspecifikke parametre i et ER-format er afhængige af juridisk enhed. Hvis du vil genbruge de programspecifikke parametre, der er konfigureret for én juridisk enhed i en anden juridisk enhed, skal du eksportere dem, mens du er logget på den første juridiske enhed. Importér dem, når du har logget på den anden juridiske enhed.

Du kan også bruge denne fremgangsmåde for eksport/import til at overføre et ER-format, der er tilknyttet programspecifikke parametre, som oprindeligt blev konfigureret i én Finance-forekomst til en anden Finance-forekomst.

Hvis du konfigurerer programspecifikke parametre for én version af et ER-format og derefter importerer en senere version af samme format til den aktuelle Finance-forekomst, anvendes de eksisterende programspecifikke parametre ikke på den importerede version, medmindre du bruger funktionen **Brug programspecifikke parametre fra tidligere versioner af ER-formater**. Du kan finde flere oplysninger i afsnittet [Genbruge eksisterende parametre](#reuse-existing-parameters) nedenfor i denne artikel.

Når du vælger en fil til import, sammenlignes strukturen for de programspecifikke parametre i den pågældende fil med strukturen i de tilsvarende datakilder for typen **Opslag** i det ER-format, der er valgt til import. Importen udføres som standard kun, hvis strukturen af de programspecifikke parametre stemmer overens med strukturen i den tilsvarende datakilde i det ER-format, der er valgt til import. Hvis strukturerne ikke stemmer overens, får du vist en advarselsmeddelelse om, at importen ikke bliver fuldført. Hvis du gennemtvinger importen, vil de eksisterende programspecifikke parametre for det valgte ER-format blive ryddet op, og du skal konfigurere dem forfra.


Fra og med Finance-version 10.0.24 kan du ændre standardfunktionsmåden og undgå at modtage en advarsel ved at aktivere de funktionen **Juster ER-programspecifikke parametre under import** i arbejdsområdet **Funktionsstyring**. Når denne funktion er aktiveret, og hvis strukturen for de programspecifikke parametre, du importerer, er forskellige fra strukturen i de tilsvarende datakilder i målets ER-format, der er valgt til import, fuldføres importen i følgende tilfælde:

- Strukturen i målets ER-format er ændret ved at føje nye betingelseskolonner til eventuelle eksisterende datakilder af typen **Opslag**. Når importen er fuldført, opdateres de programspecifikke parametre. I alle importerede poster med programspecifikke parametre initialiseres værdierne i hver kolonne med tilføjede betingelser med standardværdien for den pågældende kolonnes [datatype](er-formula-supported-data-types-primitive.md).
- Strukturen i målets ER-format er ændret ved at fjerne nogle betingelseskolonner fra eventuelle eksisterende datakilder af typen **Opslag**. Når importen er fuldført, opdateres de programspecifikke parametre. I alle importerede poster med programspecifikke parametre slettes værdierne i hver fjernet betingelseskolonne.
- Strukturen i målets ER-format er ændret ved at tilføje nye datakilder af typen **Opslag**. Når importen er fuldført, føjes de tilføjede opslag til de programspecifikke parametre.
- Strukturen i målets ER-format er ændret ved at fjerne nogle af de eksisterende datakilder af typen **Opslag**. Når importen er fuldført, slettes alle artefakter, der er relateret til datakilderne af typen **Opslag**, der blev fjernet fra målets ER-format, i de importerede programspecifikke parametre.

Når importen er fuldført, og i tillæg til de ændringer, der lige er beskrevet, ændres status for de importerede programspecifikke parametre til **I gang**. En advarsel fortæller dig, at de automatisk justerede programspecifikke parametre skal redigeres manuelt.

#### <a name="replicate-parameters"></a>Repliker parametre

Fra og med Finance-version 10.0.27 kan du kopiere de parametre, du har konfigureret i ét regnskab, til andre firmaer på samme tid.

Hvis du vil kopiere parametre, skal du benytte følgende trin.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Vælg **Rapporteringskonfigurationer**.
3. I konfigurationstræet skal du vælge elementet **Format for at lære, hvordan man slår LE-data op**.
4. I handlingsruden på fanen **Konfigurationer** skal du i gruppen **Programspecifikke parametre** vælge **Opsætning**.
5. Vælg version **1.1.1** af ER-formatet.
6. Vælg **Repliker** i handlingsruden.
7. Vælg de **regnskaber**, du vil kopiere parametre til under fanen Regnskaber i dialogboksen **Repliker**.

    > [!NOTE]
    > Listen over målfirmaer tilbydes kun til brugere, der er tildelt en [sikkerhedsrolle](../sysadmin/role-based-security.md#security-roles), der er konfigureret til at give adgang til alle organisationer.

8. Vælg **OK**.

    > [!NOTE]
    > I bekræftelsesdialogboksen får du besked, hvis nogle målfirmaer indeholder tidligere konfigurerede parametre for den valgte version af et ER-format. Vælg **Ja**, hvis du vil tilsidesætte parametrene ved at kopiere dem fra det aktuelle regnskab.

    Det konfigurerede sæt programspecifikke parametre kopieres nu til de valgte regnskaber.

### <a name="reuse-existing-parameters"></a>Genbruge eksisterende parametre

Fra og med Finance-version 10.0.23 kan du genbruge programspecifikke parametre, der er konfigureret til én version af et ER-format, når du kører en højere version af samme format. Du kan genbruge parametre ved at aktivere funktionen **Brug programspecifikke parametre fra tidligere versioner af ER-formater** i arbejdsområdet **Funktionsstyring**. Når denne funktion er aktiveret, og du kører én version af et ER-format, der forsøger at læse programspecifikke parametre, forsøger ER at finde programspecifikke parametre, der er konfigureret til den kørende version af dette format. Hvis de ikke er tilgængelige, vil ER forsøge at finde dem til den nærmeste lavere version af formatet.

> [!NOTE]
> Du kan kun genbruge programspecifikke parametre inden for omfanget af den aktuelle juridiske enhed.
>
> Der vises en fejl under kørslen, når du kører en højere version af et ER-format, der prøver at genbruge programspecifikke parametre, der er konfigureret til en lavere version af samme format, og strukturen for mindst én datakilde af typen **Opslag** i den højere formatversion er ændret.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Relation mellem programspecifikke parametre og et ER-format

Relationen mellem et ER-format og dens programspecifikke parametre fastlægges af ER-formatets forekomst-uafhængige entydig identifikationskode. Når du fjerner et ER-format fra Finance, bevares de programspecifikke parametre, der er konfigureret for ER-formatet, derfor i den aktuelle forekomst af Finance. Du kan få adgang til dem, når ER-basisformatet importeres igen til denne forekomst af Finance.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>Få adgang til programspecifikke parametre ved hjælp af ER-strukturen

I det foregående eksempel fik du adgang til programspecifikke parametre for et ER-format ved hjælp af ER-strukturen. Denne fremgangsmåde giver dig ikke mulighed for at begrænse adgangen til de programspecifikke parametre for et bestemt ER-format. Hvis du skal anvende sådanne begrænsninger, skal du følge disse trin. 

1. Du kan enten genbrug en eksisterende **ERSolutionAppSpecificParametersDesigner**-menu eller implementere dit eget **ERSolutionAppSpecificParametersDesigner**-menuelement.

    ![Visning af menupunkt i ERSolutionAppSpecificParametersDesigner.](./media/GER-AppSpecParms-LookupForm-Access1.PNG)

2. Udfør ét af følgende trin:

    1. Opret en ny menuknap, og sammenkæd den med den tilsvarende post fra tabellen **ERSolutionTable** ved at angive dens egenskab **Datakilde** til **ERSolutionTable**.

        ![Visning af nye menupunktsindstillinger.](./media/GER-AppSpecParms-LookupForm-Access2.PNG)

    2. Opret en enkel knap, og overskriv metoden **Klikket på**, som vist i følgende eksempel.

        Ved hjælp af denne fremgangsmåde kan du angive et entydigt løsnings-ID (defineret via værdien **GUID**) for kun at give adgang til de programspecifikke parametre for et bestemt ER-format og de underordnede kopier, der er afledt af den.
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a>Yderligere ressourcer

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Konfigurer ER-formater for at bruge de parametre, der er angivet for den enkelte juridiske enhed](er-app-specific-parameters-configure-format.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
