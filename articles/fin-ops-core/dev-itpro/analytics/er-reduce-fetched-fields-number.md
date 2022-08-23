---
title: Forbedre ydeevne af ER-løsninger ved at reducere antallet af tabelfelter, der hentes under kørsel
description: Denne artikel beskriver, hvordan du kan forbedre ydeevnen ved at reducere antallet af tabelfelter, der hentes under kørsel.
author: kfend
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.28
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 5c9481f1021a5dba6e1d4020bbf85a10bd551ac0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278820"
---
# <a name="improve-performance-of-er-solutions-by-reducing-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Forbedre ydeevne af ER-løsninger ved at reducere antallet af tabelfelter, der hentes under kørsel

[!include[banner](../includes/banner.md)]

Du kan designe [Elektronisk rapportering](general-electronic-reporting.md) (ER)-[formater](er-overview-components.md#format-components-for-outgoing-electronic-documents) for at oprette udgående dokumenter i forskellige formater. Når et dokument er oprettet, kalder et ER-format datakilder, der er konfigureret i en tilsvarende ER-[modeltilknytning](er-overview-components.md#model-mapping-component). Hvis du vil konfigurere adgang til tabeller, forespørgsler eller enheder i programmet for at hente poster, kan du bruge ER-datakilder af typen *Tabelposter*. En datakilde af typen *Tabelposter* henter som standard værdierne i alle felter i de ønskede poster. Du kan dog konfigurere denne type datakilde, så den kun henter de feltværdier, der kræves for det kørende ER-format. Denne konfiguration er med til at reducere forbruget af hukommelse på programserveren, hvor der udføres datahentning og yderligere cachelagring af poster.

Du kan få mere at vide om, hvordan du begrænser listen over hentede datakilder for typen *Tabelposter*, ved at fuldføre eksemplet i denne artikel.

## <a name="example-reduce-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Eksempel: Reducere antallet af tabelfelter, der hentes under kørsel

Følgende procedurer viser, hvordan en bruger i rollen Systemadministrator eller udviklerrollen Elektronisk rapportering kan konfigurere en ER-modeltilknytning, så den kun henter de felter, der kræves for at køre ER-formatet, for at reducere forbruget af programserverhukommelse.

Disse procedurer kan fuldføres i **USMF**-virksomheden i Microsoft Dynamics 365 Finance. Der kræves ingen kodning.

For at fuldføre dette eksempel skal du have adgang til **USMF**-firmaet i en af følgende roller:

- Funktionel konsulent i elektronisk rapportering
- Systemadministrator

I dette eksempel bruger du de ER-[konfigurationer](general-electronic-reporting.md#Configuration), der er leveret til **Litware, Inc.**- eksempelvirksomheden. Sørg for, at konfigurationsudbyderen for eksempelfirmaet **Litware, Inc.** (`http://www.litware.com`) er angivet for ER-strukturen og er markeret som **Aktiv**. Hvis denne konfigurationsudbyder ikke er angivet, eller hvis den ikke er markeret som **Aktiv**, skal du følge trinnene i emnet [Opret en konfigurationsudbyder, og markér den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-the-er-framework"></a>Konfigurere ER-strukturen

Følg trinnene i [Konfigurere ER-strukturen](er-quick-start2-customize-report.md#ConfigureFramework) for at konfigurere det minimale sæt af ER-parametre. Du skal fuldføre denne opsætning, før du begynder at bruge ER-strukturen til at redigere datakilder for ER-løsningen.

### <a name="import-the-sample-er-configurations"></a>Importere ER-eksempelkonfigurationerne

Hvis du endnu ikke har fuldført eksemplet i artiklen [Designe en ny ER-løsning til udskrivning af en brugerdefineret rapport](er-quick-start1-new-solution.md), skal du downloade og gemme XML-filerne lokalt til følgende konfigurationer af den leverede ER-løsning.

| Indholdsbeskrivelse            | Filnavn |
|--------------------------------|-----------|
| ER-datamodelkonfiguration    | [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) |
| ER-modeltilknytningskonfiguration | [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) |
| Konfiguration af ER-format        | [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) |

Følg derefter disse trin for at uploade konfigurationerne af den leverede ER-løsning til din finansforekomst.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Vælg **Rapporteringskonfigurationer**.
3. Importér ER-datamodelkonfiguration på siden **Konfigurationer**.

    1. Vælg **Exchange**, og vælg derefter **Indlæs fra XML-fil**.
    2. Vælg **Gennemse**, find og vælg filen **Questionnaires model.version.1.xml**, og vælg **OK**.

4. Importér konfigurationen af ER-modeltilknytningen.

    1. Vælg **Exchange**, og vælg derefter **Indlæs fra XML-fil**.
    2. Vælg **Gennemse**, find og vælg filen **Questionnaires mapping.1.1.xml**, og vælg **OK**.

5. Importér ER-formatkonfigurationen.

    1. Vælg **Exchange**, og vælg derefter **Indlæs fra XML-fil**.
    2. Vælg **Gennemse**, find og vælg filen **Questionnaires format.1.1.xml**, og vælg **OK**.

6. Udvid **Questionnaires model** i konfigurationstræet.
7. Gennemse listen over importerede ER-konfigurationer i konfigurationstræet.

    ![Gennemgang af listen over importerede ER-konfigurationer på siden Konfigurationer.](./media/er-reduce-fetched-fields-number-configurations.png)

### <a name="review-the-provided-er-model-mapping"></a>Gennemgå den leverede ER-modeltilknytning

1. På siden **Konfigurationer** skal du vælge **Questionnaires mapping**.
2. Vælg **Designer** i handlingsruden.
3. Vælg **Designer** på siden **Tilknytning af model til datakilde**.
4. På siden **Designer for modeltilknytning** skal du vælge **Gruppevisning** i handlingsruden for at aktivere **Gruppevisning**.
5. Udvid **Spørgeskema** i ruden **Datamodel**.

    Bemærk, at datakilden **Spørgeskema** er konfigureret med adgang til programtabellen `KMCollection`.

6. I ruden **Datakilder** skal du udvide **Tabelposter** \> **Spørgeskema** \> **Felter**..

    Bemærk, hvor mange felter fra programtabellen `KMCollection`, der vises af datakilden **Spørgeskema** for *Tabelposter*-typen.

    ![Gennemgå den viste modeltilknytning på siden Designer for modeltilknytning, når Gruppevisning er aktiveret.](./media/er-reduce-fetched-fields-number-mapping1.png)

7. Vælg **Gruppevisning** igen i handlingsruden for at deaktivere **Gruppevisning**, og vælg derefter **Vis alle** \> **Vis kun tilknyttede**.

    Bemærk, at nogle få felter i `KMCollection`-programtabellen bruges til at udfylde postlisten **Spørgeskema** i ER-datamodellen:

    - `Active`
    - `Description`
    - `questionMode`
    - `kmCollectionId`

    ![Gennemgå den viste modeltilknytning på siden Designer for modeltilknytning, når Gruppevisning er deaktiveret.](./media/er-reduce-fetched-fields-number-mapping2.png)

### <a name="turn-on-the-er-performance-trace"></a>Aktivere ER-performancesporing

Følg trinnene i [Aktivere ER-performancesporing](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) for at angive de ER-brugerparametre, der gør det muligt at spore udførelsen af ER-komponenter.

### <a name="run-the-provided-er-format-by-using-the-provided-model-mapping"></a>Køre det angivne ER-format ved hjælp af den angivne modeltilknytning

Følg trinnene i [Køre et designet format fra ER](er-quick-start1-new-solution.md#RunFormatFromER) for at køre det angivne ER-format for et enkelt spørgeskema fra siden **Konfigurationer**.

### <a name="review-the-execution-trace-of-the-first-run"></a>Gennemgå udførelsessporingen af den første kørsel

1. Gå til **Virksomhedsadministration** \> **Elektronisk rapportering \> Konfigurationer**.
2. Udvid **Questionnaires model** på siden **Konfigurationer**, og vælg **Questionnaires mapping**.

    > [!NOTE]
    > Detaljerne i oversigtspanelet **Versioner** angiver, at du har valgt kladdeversionen af konfigurationen **Questionnaires mapping**. Du kan derfor ændre indholdet af denne modeltilknytning.

3. Vælg **Designer** i handlingsruden.
4. Vælg **Designer** på siden **Tilknytning af model til datakilde**.
5. I oversigtspanelet på siden **Modeltilknytningsdesigner** skal du vælge **Performancesporing**.
6. Vælg den sporing , der blev genereret under den seneste formatkørsel, i dialogboksen **Indstillinger for performancesporingsresultat**.

    ![Valg af sporing i dialogboksen Indstillinger for performancesporingsresultat.](./media/er-reduce-fetched-fields-number-select-trace-1.png)

7. Vælg **OK**. 
8. Filtrer den **Spørgeskema**-sti, der peger på datakilden **Spørgeskema**, i oversigtspanelet **Detaljer**.
9. Gennemgå oplysningerne i den databaseforespørgsel, der blev genereret, da datakilden **Spørgeskema** blev kaldt.

    Bemærk, at alle felter i `KMCollection`-programtabellen blev hentet under kørsel, da datakilden **Spørgeskema** blev kaldt.

    ![Gennemgå oplysningerne i databaseforespørgslen på siden Designer for modeltilknytning.](./media/er-reduce-fetched-fields-number-query1.png)

### <a name="modify-the-provided-er-model-mapping"></a>Redigere den leverede ER-modeltilknytning

1. På siden **Designer for modeltilknytning** skal du i ruden **Datakilder** vælge datakilden **Spørgeskema**.
2. Vælg **Rediger** i ruden **Datakilder**.
3. I dialogboksen **Egenskaber for datakilde** skal du vælge **Vælg felter** for at angive listen over felter i den `KMCollection`-programtabel, der refereres til, som hentes under kørslen, når den redigerbare datakilde **Spørgeskema** kaldes.

    ![Valg af Vælg feltet i dialogboksen Egenskaber for datakilde for at starte konfigureringen af listen over felter, der skal hentes i programtabellen, ved hjælp af den redigerbare datakilde.](./media/er-reduce-fetched-fields-number-select-fields1.png)

4. Vælg **Autofyld** på siden **Vælg felter**.

    Listen **Valgte felter** udfyldes automatisk på basis af forhåndskonfigurerede artefakter for modeltilknytningen. Alle felter og relationer i den tabel, der refereres til, og som nævnes i eventuelle bindinger, formler eller datakilder for modeltilknytningen, føjes til listen.

    ![Konfigurering af listen over felter, der hentes fra programtabellen, på siden Vælg felter.](./media/er-reduce-fetched-fields-number-select-fields2.png)

5. Vælg **Gem**, og luk siden **Vælg felter**.
6. Vælg **OK** for at gemme de ændringer, du har foretaget af datakildeindstillingerne.
7. Vælg **Vis alle** i handlingsruden.

    Bemærk, at datakilden **Spørgeskema** nu viser teksten **\<Fields are filtered\>**. Denne tekst angiver, at datakilden er konfigureret til at hente et begrænset antal felter fra den programtabel, der refereres til.

    ![Gennemgang af opdateret modeltilknytning på siden Designer for modeltilknytning.](./media/er-reduce-fetched-fields-number-mapping3.png)

8. Vælg **Gem** for at gemme de ændringer, du har foretaget af den redigerbare modeltilknytning.

    > [!NOTE]
    > Under kørslen analyserer ER de tilføjede relationer og tilføjer alle de felter, der bruges i dem, i databaseforespørgslen, selvom disse felter ikke eksplicit er føjet til listen over hentede felter på designtidspunktet.

### <a name="run-the-provided-er-format-by-using-the-updated-model-mapping"></a>Køre det angivne ER-format ved hjælp af den opdaterede modeltilknytning

Følg trinnene i [Køre et designet format fra ER](er-quick-start1-new-solution.md#RunFormatFromER) for at køre det angivne ER-format for et enkelt spørgeskema fra siden **Konfigurationer**.

### <a name="review-the-execution-trace-of-the-second-run"></a>Gennemgå udførelsessporingen af den anden kørsel

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Udvid **Questionnaires model** på siden **Konfigurationer**, og vælg **Questionnaires mapping**.
3. Vælg **Designer** i handlingsruden.
4. Vælg **Designer** på siden **Tilknytning af model til datakilde**.
5. I oversigtspanelet på siden **Modeltilknytningsdesigner** skal du vælge **Performancesporing**.
6. Vælg den sporing , der blev genereret under den seneste formatkørsel, i dialogboksen **Indstillinger for performancesporingsresultat**.
7. Vælg **OK**.
8. Filtrer den **Spørgeskema**-sti, der peger på datakilden **Spørgeskema**, i oversigtspanelet **Detaljer**.
9. Gennemgå oplysningerne i den databaseforespørgsel, der blev genereret, da datakilden **Spørgeskema** blev kaldt.

    Bemærk, at det kun er de felter, der skal udfylde datakilden, som blev hentet under kørslen fra programtabellen `KMCollection`, da datakilden **Spørgeskema** blev kaldt.

    > [!NOTE]
    > Visse felter, f.eks. felterne til partitions-id'et, dataområde-id og post-id, tilføjes automatisk af Dataadministrationsstrukturen i Finans-appen.

    ![Gennemgå oplysningerne i databaseforespørgslen for den opdaterede modeltilknytning på siden Designer for modeltilknytning.](./media/er-reduce-fetched-fields-number-query2.png)

Du kan bruge denne teknik til at reducere antallet af hentede poster, når du skal reducere forbruget af hukommelse med den kørende ER-modeltilknytning og ER-format.

## <a name="limitations"></a>Begrænsninger

Når du begrænser antallet af hentede felter for en datakilde af typen *Tabelposter*, kan du ikke bruge metoderne i en programtabel, som datakilden refererer til, da programmetadataene ikke indeholder oplysninger om tabelfelter, der er nødvendige for at kalde disse metoder.

## <a name="usage-notes"></a>Bemærkninger til brug

Selvom kommandoen **Autofyld** automatisk tilføjer felter, slettes felter, der er tilføjet tidligere, ikke automatisk, selvom de ikke længere bruges i bindinger, formler og datakilder for den modeltilknytning, der kan redigeres.

Når du vælger **Autofyld**, analyserer ER bindinger, formler og datakilder, som den redigerbare modeltilknytning havde, da du åbnede den til redigering. Hvis du ændrer bindinger, formler og datakilder for den modeltilknytning, der kan redigeres, og du vil bruge kommandoen **Autofyld**, skal du lukke modeltilknytningsdesigneren og derefter åbne den igen for at redigere modeltilknytningen. 

## <a name="additional-resources"></a>Yderligere ressourcer

- [Spore kørslen af ER-formater til fejlfinding af problemer med ydeevnen](trace-execution-er-troubleshoot-perf.md)
- [Fejlfinde problemer med ydeevnen i ER-konfigurationer](er-troubleshoot-perf-issues-in-configurations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
