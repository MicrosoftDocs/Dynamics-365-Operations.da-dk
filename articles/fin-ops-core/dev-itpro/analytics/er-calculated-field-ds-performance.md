---
title: Forbedre ydeevnen af ER-løsninger ved at tilføje parameteriserede BEREGNET FELT-datakilder
description: Denne artikel forklarer, hvordan du kan forbedre ydeevnen for løsninger til Elektronisk rapportering (ER) ved at tilføje parametre for BEREGNET FELT-datakilder.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 34bb7c6256994f103c4da599157c06bd9d0795ef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288252"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>Forbedre ydeevnen af ER-løsninger ved at tilføje parameteriserede BEREGNET FELT-datakilder

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du kan tage [ydeevnespor](trace-execution-er-troubleshoot-perf.md) af [elektroniske rapporteringsformater (ER)](general-electronic-reporting.md), som er kørt, og derefter bruge oplysningerne fra disse spor til at forbedre ydeevnen ved at konfigurere en parameteriseret **Beregnet felt**-datakilde.

Som en del af processen med at udvikle elektroniske rapporteringskonfigurationer (ER) til generering af forretningsdokumenter definerer du den metode, der bruges til at hente data fra programmet og indtaste dem i det output, der genereres. Ved at designe en parameteriseret datakilde af typen **Beregnet felt**, kan du mindske antallet af databasekald og reducere den tid og de omkostninger, der er involveret i indsamlingen af detaljer om udførelse af ER-format.

## <a name="prerequisites"></a>Forudsætninger

- Hvis du vil fuldføre eksemplerne i denne artikel, skal du have adgang til en af følgende [roller](../sysadmin/tasks/assign-users-security-roles.md):

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

- Virksomheden skal angives til **DEMF**.
- Følg trinnene i [Appendiks 1](#appendix1) i denne artikel for at downloade komponenterne til Microsoft ER-eksempelløsningen, der er nødvendige for at fuldføre eksemplet i denne artikel.
- Følg trinnene i [Appendiks 2](#appendix2) i denne artikel for at konfigurere det minimale sæt af ER-parametre, der kræves for at bruge ER-strukturen til at forbedre ydeevnen i eksemplet på Microsoft ER-løsningen.

## <a name="import-the-sample-er-solution"></a>Importere ER-eksempelløsningen

Antag, at du skal designe en ER-løsning for at generere en ny rapport, der viser kreditorposteringer. I øjeblikket kan du finde posteringerne for en valgt kreditor på siden **Kreditorposteringer** (gå til **Kreditor** \> **Kreditorer** \> **Alle kreditorer**, vælg en kreditor, og vælg derefter en kreditor i handlingsruden under fanen **Kreditor** i gruppen **Transaktioner** på **Posteringer**). Men skal have alle kreditorposteringer samlet i et elektronisk dokument i XML-format. Denne løsning består af flere ER-konfigurationer, der indeholder den nødvendige datamodel, modeltilknytning og formatkomponenter.

Det første trin er at importere ER-løsningseksemplet for at generere en rapport over kreditorposteringer.

1. Log på den forekomst af Microsoft Dynamics 365 Finance, der er klargjort for dit firma.
2. I denne artikel skal du oprette og ændre ER-konfigurationerne for eksempelfirmaet **Litware Inc.**. Sørg for, at denne konfigurationsudbyder er føjet til din Finance-forekomst og markeret som aktiv. Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. I arbejdsområdet **Elektronisk rapportering** skal du vælge feltet **Rapporteringskonfigurationer**.
4. På siden **Konfigurationer** skal du importere de ER-konfigurationer, som du har hentet som en forudsætning i Finance, i følgende rækkefølge: datamodel, modeltilknytning, format. Benyt følgende fremgangsmåde for hver konfiguration:

    1. Vælg **Exchange** \> **Indlæs fra XML-fil** i handlingsruden.
    2. Vælg **Gennemse**, og vælg den relevante fil til ER-konfigurationen i XML-format.
    3. Vælg **OK**.

![Importerede konfigurationer på siden Konfigurationer.](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>Gennemgå ER-eksempelløsningen

### <a name="review-the-model-mapping"></a>Gennemse modeltilknytningen

1. På siden **Konfigurationer** skal du i konfigurationstræet udvide **Model til forbedret ydeevne** og derefter vælge **Tilknytning af forbedret ydeevne**.
2. Vælg **Designer** i handlingsruden.
3. Vælg **Designer** i handlingsruden på siden **Tilknytning af model til datakilde**.

    Denne ER-modeltilknytning er beregnet til at udføre følgende handlinger:

    - Hent listen over kreditorposteringer, der er gemt i tabellen VendTrans (**Trans**-datakilde).
    - For hver postering skal du fra tabellen VendTable hente den post for en kreditor, som posteringen er bogført for (**\#Vend**-datakilde).

    > [!NOTE]
    > Datakilden **\#Vend** er konfigureret til at hente den tilsvarende kreditorpost ved hjælp af den eksisterende mange til én-relation **\@.'\>Relations'.VendTable\_AccountNum**.

    Modeltilknytningen i denne konfiguration implementerer basisdatamodellen for ethvert af de ER-formater, der er oprettet for denne model og kørt i Finance. Derfor vises indholdet af **Trans**-datakilden for ER-formater, f.eks. abstrakte **model**-datakilder.

    ![Trans-datakilde på siden for modeltilknytningsdesigneren.](media/er-calculated-field-ds-performance-mapping-1.png)

4. Luk siden **Modeltilknytningsdesigner**.
5. Luk siden **Tilknytning af model til datakilde**.

### <a name="review-format"></a>Gennemse format

1. På siden **Konfigurationer** skal du i konfigurationstræet udvide **Model til forbedret ydeevne** og derefter vælge **Format af forbedret ydeevne**.
2. Vælg **Designer** i handlingsruden.
3. Vælg fanen **Tilknytning** på siden **Formatdesigner**, og vælg **Udvid/skjul**.
4. Udvid elementerne **Model**, **Data** og **Transaktion**.

    Dette ER-format er beregnet til at oprette en rapport over kreditorposteringer i XML-format.

    ![Formatere datakilder og konfigurerede bindinger af formatelementer på formatdesignsiden.](media/er-calculated-field-ds-performance-format.png)

5. Luk siden **Formatdesigner**.

## <a name="run-the-sample-er-solution-to-trace-execution"></a>Køre ER-eksempelløsningen for at spore kørslen

Forestil dig, at du er færdig med at designe den første version af ER-løsningen. Du vil nu teste løsningen i din Finance-forekomst og analysere kørselsydeevnen.

### <a name="turn-on-the-er-performance-trace"></a>Aktivere ER-performancesporing

1. Vælg firmaet **DEMF**.
2. Følg trinnene i [Aktivere ER-performancesporing](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) for at generere en performancesporing, mens et ER-format køres.

    ![Dialogboksen Brugerparametre.](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>Køre ER-formatet

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du vælge elementet **Format af forbedret ydeevne** i konfigurationstræet.
3. Vælg **Kør** i handlingsruden.

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>Brug performancesporing til at analysere ydeevne af modeltilknytning

1. På siden **Konfigurationer** skal du vælge elementet **Tilknytning af forbedret ydeevne** i konfigurationstræet.
2. Vælg **Designer** i handlingsruden.
3. Vælg **Designer** i handlingsruden på siden **Modeltilknytninger**.
4. I oversigtspanelet på siden **Modeltilknytningsdesigner** skal du vælge **Performancesporing**.
5. Vælg den seneste sporing, der blev genereret, og vælg derefter **OK**.

Nye oplysninger er nu tilgængelige for nogle datakildeelementer i den aktuelle modeltilknytning:

- Den tid, det faktisk blev brugt på at hente data vha. datakilden
- Den samme tid angivet som en procentdel af den samlede tid, der blev brugt på at køre hele modeltilknytningen

![Detaljer om udførelsestiden på designersiden Modeltilknytning.](./media/er-calculated-field-ds-performance-mapping-2.png)

Gitteret **Statistik for ydeevne** viser, at **Trans**-datakilden kalder tabellen VendTrans én gang. Værdien **\[265\]\[Q:265\]** i **Trans**-datakilden angiver, at 265 kreditorposteringer er hentet fra programtabellen og returneret til datamodellen.

Gitteret **Statistik for ydeevne** viser også, at den aktuelle modeltilknytning duplikerer databaseanmodninger, mens datakilden **\#Vend** køres. Denne duplikering udføres af følgende årsager:

- Kreditortabellen kaldes to gange for hver af de 265 gentagne kreditorposteringer, med en total på 530 kald.

    - Der foretages et kald for at angive kreditorkontonummeret.
    - Der foretages et kald for at angive kreditornavnet.

- Kreditortabellen kaldes for hver af de gentagne kreditorposteringer, selvom de hentede posteringer kun er bogført for fem kreditorer. Af 530 kald er 525 dubletter. I følgende illustration vises den meddelelse, du har modtaget om dubletopkald (databaseanmodninger).

![Meddelelse om dublerede databaseanmodninger på siden Modeltilknytningsdesigner.](./media/er-calculated-field-ds-performance-mapping-2a.png)

Den samlede udførelsestid for modeltilknytning (cirka otte sekunder). Bemærk, at mere end 80 procent (cirka seks sekunder) er blevet brugt på at hente værdier fra programtabellen VendTable. Denne procentdel er for stor til to attributter af fem leverandører sammenlignet med oplysningerne om mængden fra VendTrans-programtabellen.

Hvis du vil reducere antallet af kald, der oprettes for at få leverandøroplysningerne for hver transaktion og forbedre modeltilknytningens ydeevne, kan du bruge cachelagring til datakilden **\#Vend**.

> [!NOTE]
> Datakilden **Trans\\\#Vend** cachelagres i området for den aktuelle transaktion i **Trans**-datakilden under kørslen.

Ved at cachelagre datakilden **\#Vend** skal du reducere antallet af dublerede kald fra 525 til 260, men du fjerner ikke dubleringen fuldstændigt. Hvis du vil fjerne dubletter helt, kan du konfigurere en ny parameterdatakilde af typen **Beregnede felt**.

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Forbedre modeltilknytningen på baggrund af oplysninger fra kørselssporing

### <a name="change-the-logic-of-the-model-mapping"></a>Ændre modeltilknytningens logik

Udfør følgende trin for at bruge cachelagring og en datakilde af typen **Beregnet felt** for at forhindre, at der foretages dubletkald til databasen.

1. På siden **Konfigurationer** skal du vælge elementet **Tilknytning af forbedret ydeevne** i konfigurationstræet.
2. Vælg **Designer** i handlingsruden.
3. Vælg **Designer** i handlingsruden på siden **Modeltilknytninger**.
4. På siden **Modeltilknytningsdesigner** skal du følge disse trin for at tilføje en datakilde af typen **Tabelpost** for at få adgang til poster i programtabellen VendTable:

    1. I ruden **Datakildetyper** skal du udvide **Dynamics 365 for Operations** og vælge **Tabelposter**.
    2. Vælg **Tilføj rod**.
    3. I dialogboksen skal du angive **Vend** i feltet **Navn**.
    4. Indtast **VendTable** i feltet **Tabel**.
    5. Vælg **OK**.

5. Du kan kun parameterisere kald til datakilder af typen **Beregnet felt**, hvis disse datakilder er placeret i en container. Benyt derfor følgende fremgangsmåde for at føje en datakilde af typen **Tom container** til en ny parameteriseret datakilde af typen **Beregnet felt**:

    1. I ruden **Datakildetyper** skal du udvide **Generelt** og vælge **Tom container**.
    2. Vælg **Tilføj rod**.
    3. I dialogboksen skal du angive **Box** i feltet **Navn**.
    3. Vælg **OK**.

    ![Box-datakilde på siden for modeltilknytningsdesigneren.](./media/er-calculated-field-ds-performance-mapping-3.png)

6. Udfør følgende trin for at tilføje en parameteriseret datakilde af typen **Beregnet felt**:

    1. Vælg **Box** i ruden **Datakilder**.
    2. Udvid **Funktioner** i ruden **Datakildetyper**, og vælg **Beregnet felt**.
    3. Vælg **Tilføj**.
    4. I dialogboksen skal du angive **Vend** i feltet **Navn**.
    5. Vælg **Rediger formel**.
    6. På siden **Formeldesigner** skal du vælge **Parametre** for at angive de parametre, der skal leveres, når denne datakilde kaldes.
    7. Vælg **Ny** i dialogboksen **Parametre**.
    8. Angiv **parmVendAccNumber** i feltet **Navn**.
    9. I feltet **Type** skal du vælge **Streng**.
    10. Vælg **OK**.
    11. I feltet **Formel** skal du angive **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.
    12. Vælg **Gem**, og luk derefter siden **Formeldesigner**.
    13. Vælg **OK** for at tilføje den nye datakilde.

7. Benyt følgende fremgangsmåde for at markere den tilføjede datakilde som cachelagret under udførelsen:

    1. Vælg **Box\\Vend** i ruden **Datakilder**.
    2. Vælg **Cache**.

    > [!NOTE]
    > Datakilden **Box\\Vend** cachelagres i området for alle leverandørtransaktioner i **Trans**-datakilden under kørslen.

8. Udfør følgende trin for at opdatere den indlejrede **Trans\\\#Vend**-datakilde, så den bruger datakilden **Box\\Vend**:

    1. Udvid **Trans** i ruden **Datakilder**.
    2. Vælg datakilden **Trans\\\#Vend**, og vælg derefter **Rediger** \> **Rediger formel**.
    3. På siden **Formeldesigner** skal du i feltet **Formel** angive **Box.Vend(\@.AccountNum)**.
    4. Vælg **Gem**, og luk derefter siden **Formeldesigner**.
    5. Vælg **OK** for at fuldføre ændringerne af den valgte datakilde.

9. Vælg **Gem**.

    ![Vend-datakilde på siden for modeltilknytningsdesigneren.](./media/er-calculated-field-ds-performance-mapping-4.png)

10. Luk siden **Modeltilknytningsdesigner**.
11. Luk siden **Modeltilknytninger**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>Fuldføre den ændrede version af ER-modeltilknytningen

1. På siden **Konfigurationer** skal du i oversigtspanelet **Versioner** vælge version **1.2** af konfigurationen af **Tilknytning af forbedret ydeevne**.
2. Vælg **Skift status** \> **Fuldført**, og vælg derefter **OK**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Køre den ændrede ER-løsning for at spore kørslen

Gentag trinnene i afsnittet [Køre ER-formatet](#run-format) tidligere i denne artikel for at generere en ny performancesporing.

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>Brug performancesporing til at analysere justeringer af modeltilknytning 

1. På siden **Konfigurationer** skal du vælge elementet **Tilknytning af forbedret ydeevne** i konfigurationstræet.
2. Vælg **Designer** i handlingsruden.
3. Vælg **Designer** i handlingsruden på siden **Modeltilknytninger**.
4. I oversigtspanelet på siden **Modeltilknytningsdesigner** skal du vælge **Performancesporing**.
5. Vælg den seneste sporing, der blev genereret, og vælg derefter **OK**.

Bemærk, at de justeringer, du har foretaget for modeltilknytningen, har elimineret dubletter af forespørgsler til databasen. Antallet af kald til databasetabeller og datakilder for denne modeltilknytning er også blevet reduceret.

![Sporingsoplysninger på side 1 af modeltilknytningsdesigneren.](./media/er-calculated-field-ds-performance-mapping-5.png)

Den samlede udførelsestid er blevet reduceret ca. 20 gange (fra ca. 8 sekunder til ca. 400 millisekunder). Derfor er ydeevnen i hele ER-løsningen blevet forbedret.

![Sporingsoplysninger på side 2 af modeltilknytningsdesigneren.](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>Appendiks 1: Download komponenterne i Microsoft ER-eksempelløsningen

Du skal også downloade og lokalt gemme følgende filer.

| Filer                                        | Indhold |
|---------------------------------------------|---------|
| Model til forbedret ydeevne.version.1     | [Eksempler på ER-datamodelkonfiguration](https://download.microsoft.com/download/4/6/f/46f0f3fa-782b-414a-8f7b-b6c64a388661/Performance_improvement_model.version.1.xml) |
| Tilknytning af forbedret ydeevne.version.1.1 | [Eksempler på ER-modeltilknytningskonfiguration](https://download.microsoft.com/download/8/9/1/8913a763-afb8-4bf4-aaf1-95ad793ffc5a/Performance_improvement_mapping.version.1.1.xml) |
| Format af forbedret ydeevne.version.1.1  | [Eksempler på ER-formatkonfiguration](https://download.microsoft.com/download/9/0/c/90c75963-bc78-4edc-9096-556bbe281f10/Performance_improvement_format.version.1.1.xml) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>Appendiks 2: Konfigurere ER-strukturen

Før du kan begynde at bruge ER-strukturen til at forbedre ydeevnen i eksemplet med Microsoft ER-løsningen, skal du konfigurere det minimale sæt med ER-parametre.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Konfigurere ER-parametre

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Parametre til elektronisk rapportering** i sektionen **Relaterede links**.
3. På siden **Parametre til elektronisk rapportering** under fanen **Generelt** skal du vælge **Ja** i indstillingen **Aktiver designtilstand** .
4. På fanen **Vedhæftede filer** kan du angive følgende parametre:

    - I feltet **Konfigurationer** skal du vælge typen **Fil** for **DEMF**-virksomheden.
    - I felterne **Jobarkiv**, **Midlertidig**, **Grundlag** og **Andre** skal du vælge typen **Fil**.

Du kan finde flere oplysninger om ER-parametre under [Konfigurere ER-strukturen](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Aktivere en udbyder af ER-konfigurationer

Alle ER-konfigurationer, der tilføjes, er markeret som ejet af en udbyder af ER-konfigurationer. Den udbyder af ER-konfigurationer, der aktiveres i arbejdsområdet **Elektronisk rapportering**, bruges til dette formål. Du skal derfor aktivere en udbyder af ER-konfigurationer i arbejdsområdet **Elektronisk rapportering**, før du begynder at tilføje eller redigere ER-konfigurationer.

> [!NOTE]
> Det er kun ejeren af en ER-konfiguration, der kan redigere konfigurationen. Før du kan redigere en ER-konfiguration, skal den relevante udbyder af ER-konfiguration aktiveres i arbejdsområdet **Elektronisk rapportering**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Gennemse listen over udbydere af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Konfigurationsudbydere** i sektionen **Relaterede links**.
3. På siden **Tabel over konfigurationsudbydere** har hver udbyderpost et entydigt navn og en entydig URL-adresse. Gennemse indholdet af denne side. Hvis der allerede findes en post for **Litware, Inc.**, skal du springe den næste procedure over, [Tilføje en ny udbyder af ER-konfigurationer](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Tilføje en ny udbyder af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Konfigurationsudbydere** i sektionen **Relaterede links**.
3. På siden **Konfigurationsudbydere** skal du vælge **Ny**.
4. I feltet **Navn** skal du angive **Litware, Inc.**
5. I feltet **Internetadresse** skal du angive `https://www.litware.com`.
6. Vælg **Gem**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivere en udbyder af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Gå til siden **Lokaliseringskonkfigurationer**, og vælg feltet **Litware, Inc.** i sektionen **Konfigurationsudbydere**, og vælg derefter **Angiv som aktive**.

Få flere oplysninger om udbydere af ER-konfigurationer under [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering](general-electronic-reporting.md)
- [Spore kørslen af ER-formater til fejlfinding af problemer med ydeevnen](trace-execution-er-troubleshoot-perf.md)
- [Understøtte parameteriserede kald af ER-datakilder for typen Beregnet felt](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
