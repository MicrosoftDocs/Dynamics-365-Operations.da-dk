---
title: Administrere flere afledte tilknytninger for en enkelt modelrod
description: Dette emne forklarer, hvordan du kan administrere flere afledte tilknytninger, der er konfigureret til en enkelt modelrod.
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb4fcda42361b0f14e37027d21739dfc42b44cb1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565485"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a>Administrere flere afledte tilknytninger for en enkelt modelrod

[!include [banner](../includes/banner.md)]

En [ER-komponent (elektronisk rapportering)](general-electronic-reporting.md) som [datamodel](general-electronic-reporting.md#data-model-and-model-mapping-components) bruges i alle konfigurerede [ER-formatkomponenter](general-electronic-reporting.md#FormatComponentOutbound) som datakilde til generering af udgående dokumenter. Hvis du vil beskrive et enkelt forretningsdomæne, skal du konfigurere en datamodelkomponent med mange roddefinitioner. 

Hver roddefinition giver dig mulighed for at repræsentere data for det pågældende domæne på den måde, der egner sig bedst til specifikke rapporteringsformål. For hver roddefinition kan du konfigurere en ER-[modeltilknytningskomponent](general-electronic-reporting.md#data-model-and-model-mapping-components) som den Microsoft Dynamics 365 Finance-specifikke implementering af datamodellen. På denne måde kan du beskrive, hvordan datamodellen udfyldes under kørslen.

Komponenterne til ER-modeltilknytning kan være i ER-datamodellens [konfigurationer](general-electronic-reporting.md#Configuration) og ER-modeltilknytningens konfigurationer. En enkelt ER-konfiguration kan indeholde mange tilknytningskomponenter, som hver især er konfigureret til en enkelt roddefinition. En enkelt ER-konfiguration kan kun indeholde én tilknytningskomponent, der er konfigureret til en enkelt roddefinition.

Mange konfigurationsudbydere kan tilbyde ER-modeltilknytningskonfigurationer for samme ER-datamodel. Disse modeltilknytningskonfigurationer kan indeholde tilknytningskomponenter for forskellige roddefinitioner. Du kan bruge en modeltilknytning til én roddefinition, der tilbydes af én [udbyder](general-electronic-reporting.md#Provider), og bruge en modeltilknytning til en anden roddefinition, som tilbydes af en anden udbyder.

Procedurerne i dette emne indeholder forklaring på, hvordan du kan administrere flere ER-modeltilknytningskonfigurationer for en ER-datamodel, når de indeholder forskellige modeltilknytningskomponenter, der er konfigureret til samme roddefinition. 

Procedurerne i dette emne kan kun udføres af brugere, der har fået tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler.

Alle de følgende procedurer kan udføres i USMF-virksomheden. Der kræves ingen kodning.

## <a name="configure-the-er-framework"></a>Konfigurere ER-strukturen

Som bruger i rollen Udvikler af elektronisk rapportering skal du [konfigurere det minimale sæt](er-quick-start2-customize-report.md#ConfigureFramework) af ER-parametre, før du kan begynde at bruge ER-strukturen til at oprette forretningsdokumenter.

## <a name="import-the-standard-er-format-configurations"></a>Importere standardkonfigurationer af ER-format

Hvis du vil føje ER-standardkonfigurationerne til din aktuelle forekomst af Finans, skal du importere dem fra det ER-lager, der er konfigureret for den pågældende forekomst. Følg trinnene i [Hente ER-konfigurationer fra det globale lager til Konfigurationstjenesten](er-download-configurations-global-repo.md) for at importere følgende ER-formatkonfigurationer:

- **Fritekstfaktura (Excel)**, version 220.106
- **Projektfaktura (Excel)**, version 226.27

## <a name="review-the-imported-er-configurations"></a>Gennemse de importerede ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.
3. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Fakturamodel**.

    ![Gennemgang af de importerede konfigurationer på siden Konfigurationer](./media/er-multiple-model-mappings-image1.png)

4. Gennemgå formatet **Fritekstfaktura (Excel)**:

    1. Vælg **Fritekstfaktura (Excel)** i konfigurationstræet i ruden til venstre.
    2. Vælg **Designer** i handlingsruden.
    3. På siden **Formatdesigner** under fanen **Tilknytning** skal du vælge **Model** på listen over datakilder.
    4. Vælg **Vis**.
    
       Det aktuelle ER-format er konfigureret til at bruge roddefinitionen **InvoiceCustomer** af **Fakturamodel**. Når dette format køres, og datakilden **Model** kaldes, bruges den modeltilknytning, der er konfigureret for roddefinitionen af **InvoiceCustomer**, til at få adgang til programdata og udfylde datamodellen.

        ![Gennemgang af modeldatakilden på siden Formatdesigner](./media/er-multiple-model-mappings-image2.png)

    6. Luk siden **Formatdesigner**.

5. Gennemgå indholdet af konfigurationen **Tilknytning af fakturamodel**:

    1. Vælg **Fakturamodeltilknytning** i konfigurationstræet i ruden til venstre.
    2. Vælg **Designer** i handlingsruden.
    3. På siden **Model til datakildetilknytning** skal du bemærke, at den aktuelle ER-modeltilknytningskonfiguration indeholder flere modeltilknytningskomponenter:

        + Modeltilknytningen **Kundefaktura** er konfigureret for roddefinitionen **InvoiceCustomer** af **Fakturamodel**. Når ER-formatet **Fritekstfaktura (Excel)** køres, kan du derfor vælge **Kundefaktura**-modeltilknytningen af denne ER-konfiguration for at få adgang til programdata og udfylde datamodellen.
        + Modeltilknytningen **Projektfaktura** er konfigureret for roddefinitionen **InvoiceProject** af **Fakturamodel**. Når ER-formatet **Projektfaktura (Excel)** køres, kan du derfor vælge **Projektfaktura**-modeltilknytningen af denne ER-konfiguration for at få adgang til programdata og udfylde datamodellen.

        ![Tilknytning af fakturamodel på siden Tilknytning af model til datakilde](./media/er-multiple-model-mappings-image3.png)

    4. Luk siden **Tilknytning af model til datakilde**.
    5. Vælg **Slet** i oversigtspanelet **Versioner** for at slette alle versioner af denne ER-konfiguration, som er senere end 240.175.

6. Gennemgå indholdet af konfigurationen **Modeltilknytning af projektfaktura (RDP)**:

    1. Vælg **Modeltilknytning af projektfaktura (RDP)** i konfigurationstræet i ruden til venstre.
    2. Vælg **Designer** i handlingsruden.
    3. Bemærk på siden **Model til tilknytning af datakilder**, at den aktuelle ER-modeltilknytningskonfiguration indeholder modeltilknytningen **InvoiceProject**, og at denne modeltilknytning er konfigureret for roddefinitionen **InvoiceProject** af **Fakturamodel**. Når ER-formatet **Projektfaktura (Excel)** køres, skal du vælge **InvoiceProject**-modeltilknytningen af denne ER-konfiguration for at få adgang til programdata og udfylde datamodellen.

        ![Modeltilknytning af projektfaktura på siden Tilknytning af model til datakilde](./media/er-multiple-model-mappings-image4.png)

    4. Luk siden **Tilknytning af model til datakilde**.
    5. Vælg **Slet** i oversigtspanelet **Versioner** for at slette alle versioner af denne ER-konfiguration, som er senere end 226.35.

## <a name="customize-the-imported-er-configurations"></a>Tilpasse de importerede ER-konfigurationer

I dette afsnit beskrives det, hvordan du kan [tilpasse](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) de modeltilknytninger, der leveres af Microsoft. Det kan f.eks. være nødvendigt med tilpasning for at implementere den brugerdefinerede logik eller tilføje manglende bindinger.

### <a name="customize-the-invoice-model-mapping-configuration"></a>Tilpasse konfigurationen af fakturamodeltilknytning

1. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude vælge **Tilknytning af fakturamodel**.
2. Vælg **Opret konfiguration** i handlingsruden.
3. I dialogboksen skal du på rullelisten **Opret konfiguration** i feltet **Ny** vælge **Afledt fra Navn: Tilknytning af fakturamodel, Microsoft**.
4. Angiv **Tilknytning af fakturamodel Litware** i feltet **Navn**.
5. Vælg **Opret konfiguration**.
6. [Markér](er-quick-start2-customize-report.md#MarkFormatRunnable) [kladdeversionen](general-electronic-reporting.md#component-versioning) af den afledte tilknytning som tilgængelig for brug under kørslen:

    1. I handlingsruden under fanen **Konfigurationer** skal du i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
    2. I dialogboksen **Brugerparametre** skal du angive indstillingen **Kørselsindstillinger** til **Ja** og derefter vælge **OK**.
    3. Vælg **Rediger** for at gøre siden redigerbar efter behov.
    4. Angiv indstillingen **Kør kladde** til **Ja** for den konfiguration af **Tilknytning af fakturamodel Litware**, som aktuelt er valgt i konfigurationstræet.

7. I handlingsruden skal du vælge **Designer** for at gennemgå modeltilknytninger af denne konfiguration.

    ![Gennemgang af fakturamodeltilknytninger på siden Tilknytning af model til datakilde](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > Du kan nu åbne enhver komponent for ER-modeltilknytning i denne ER-konfiguration i designeren for at konfigurere din brugerdefinerede logik. Du kan finde flere oplysninger under [Tilpasse konfigurationen af modeltilknytning](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration).

8. Luk siden **Tilknytning af model til datakilde**.

Du har nu konfigurationer af **Fakturamodeltilknytning** og **Tilknytning af fakturamodel Litware**, som hver især har en modeltilknytning, der er konfigureret for roddefinitionen **InvoiceCustomer**. Tildel udtrykkeligt en af modeltilknytninger som den standardmodeltilknytning, der bruges af et eller flere af ER-formaterne, f.eks. formatet **Fritekstfaktura (Excel)**, der indeholder en modeldatakilde, som har roddefinitionen **InvoiceCustomer**. Ellers opstår følgende undtagelse, når du kører, redigerer eller validerer et af ER-formaterne, for at give dig besked om, at der ikke eksplicit er tildelt nogen standardmodeltilknytning:
 
> Der findes mere end én modeltilknytning for datamodellen '\<model name\> (\<root descriptor\>)' i konfigurationerne \<configuration names separated by commas\>. Angiv en af konfigurationerne som standard.

![Åbning af formatet til redigering på siden Konfigurationer](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a>Tilpasse konfigurationen af Modeltilknytning af projektfaktura (RDP)

1. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude vælge **Modeltilknytning af projektfaktura (RDP)**.
2. Vælg **Opret konfiguration** i handlingsruden.
3. I dialogboksen **Opret konfiguration** skal du i feltet **Ny** vælge **Afledt fra Navn: Modeltilknytning af projektfaktura (RDP), Microsoft**.
4. Angiv **Modeltilknytning af projektfaktura Litware** i feltet **Navn**.
5. Vælg **Opret konfiguration**.
6. Angiv indstillingen **Kør kladde** til **Ja** for den konfiguration af **Modeltilknytning af projektfaktura Litware**, som aktuelt er valgt i konfigurationstræet.
7. I handlingsruden skal du vælge **Designer** for at gennemgå modeltilknytninger af denne konfiguration.

    ![Gennemgå den tilpassede modeltilknytning af projektfaktura på siden Tilknytning af model til datakilde](./media/er-multiple-model-mappings-image7.png)

8. Luk siden **Tilknytning af model til datakilde**.

Du har nu konfigurationerne **Tilknytning af fakturamodel**, **Modeltilknytning af projektfaktura (RDP)** og **Modeltilknytning af projektfaktura Litware**. Hver af disse konfigurationer har en modeltilknytning, der er konfigureret til roddefinitionen **InvoiceProject**. Tildel udtrykkeligt en af modeltilknytninger som den standardmodeltilknytning, der bruges af et eller flere ER-formater. Brug f.eks. formatet **Projektfaktura (Excel)**, der indeholder en modeldatakilde med roddefinitionen **InvoiceProject**. Ellers opstår en undtagelse, når du køre eller, redigerer et af ER-formaterne, for at give dig besked om, at der ikke eksplicit er tildelt nogen standardmodeltilknytning.

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Vælge den afledte konfiguration Tilknytning af fakturamodel Litware som den konfiguration, der indeholder standardmodeltilknytninger

1. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude vælge **Tilknytning af fakturamodel Litware**.
2. Vælg **Ja** i indstillingen **Standard for modeltilknytning**.

    ![Angivelse af modeltilknytning som standardmodeltilknytning på siden Konfigurationer](./media/er-multiple-model-mappings-image8.png)

    På grund af denne indstilling bruges modeltilknytningen **Kundefakturakopi**, når du kører **Fritekstfaktura (Excel)** eller redigerer eller validerer den. Modeltilknytningen **Kundefaktura** fra konfigurationen **Tilknytning af fakturamodel** ignoreres.

    Du kan nu åbne formatet **Fritekstfaktura (Excel)** til gennemgang i formatdesigneren.

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Vælge den afledte konfiguration Modeltilknytning af projektfaktura Litware som den konfiguration, der indeholder standardmodeltilknytninger

1. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude vælge **Modeltilknytning af projektfaktura Litware**.
2. Vælg **Ja** i indstillingen **Standard for modeltilknytning**.

    I dette tilfælde kan du i modsætning til det tilfælde, der er beskrevet for konfigurationen **Tilknytning af fakturamodel Litware** i det foregående afsnit, ikke begynde at bruge modeltilknytningen **Kopi af InvoiceProject** fra konfigurationen **Modeltilknytning af projektfaktura Litware**. To konfigurationer, der indeholder en modeltilknytning for roddefinitionen **InvoiceProject**, er i øjeblikket markeret som standardkonfiguration. Derfor har de samme prioritet ved brug. Du kan løse dette problem ved at udføre de resterende trin i denne procedure.

3. Vælg **Tilknytning af fakturamodel Litware** i konfigurationstræet i ruden til venstre.
4. Vælg **Designer** i handlingsruden.
5. Vælg **Rediger** på siden **Model til tilknytning af datakilder** for at redigere siden efter behov.
6. Vælg modeltilknytningen **Kopi af projektfaktura**, og markér derefter afkrydsningsfeltet **Er slettet** for den.

    ![Angivelse af modeltilknytning som virtuelt slettet på siden Tilknytning af model til datakilde](./media/er-multiple-model-mappings-image9.png)

    På grund af denne indstilling behandles konfigurationen **Tilknytning af fakturamodel Litware**, som om der ikke er nogen modeltilknytning for roddefinitionen **InvoiceProject**. Modeltilknytningen **Kopi af InvoiceProject** er udstedt som standard. Konfigurationen **Modeltilknytning af projektfaktura Litware**, der indeholder denne modeltilknytning, er markeret som standardkonfiguration. Da den er markeret som standard, har den en højere prioritet end modeltilknytningen **InvoiceProject** fra konfigurationen **Modeltilknytning af projektfaktura (RDP)**.

## <a name="other-considerations"></a>Andre overvejelser

Modeltilknytningen **Kopi af InvoiceProject** af konfigurationen **Modeltilknytning af projektfaktura Litware** er designet til at bruge datakilden **ReportDataProvider**. Datakilden er en del af den *Objekt*-type, der henviser til programklassen **PsaProjInvoiceDP**. Denne klasse er implementeret som dataprovider til projektfakturaens SSRS-rapport (SQL Server Reporting Services) for strukturen til udskriftsstyring. Vælg denne datakilde som ER-[integrationspunkt](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents). Den aktuelle ER-implementering for udskriftsstyringsrapporter tager højde for denne indstilling. Yderligere oplysninger finder du ved at gennemgå kildekoden til programklassen **ERPrintMgmtDataProviderReport**. Under kørslen tvinger tildelingen af datakilden **ReportDataProvider** som modeltilknytningsintegrationspunkt Finans til at behandle denne tilknytningskomponent med en højere prioritet end tilknytningskomponenten **InvoiceProject** fra konfigurationen **Modeltilknytning af projektfaktura (RDP)**.

## <a name="see-also"></a>Se også

- [Administrere ER-modeltilknytning i separate ER-konfigurationer](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [Konfigurere landekontekstafhængige ER-modeltilknytninger](er-country-dependent-model-mapping.md)
- [Ændringer af API-struktur til elektronisk rapportering](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]