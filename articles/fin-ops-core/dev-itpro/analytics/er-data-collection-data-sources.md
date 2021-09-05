---
title: Bruge datakilder for DATAINDSAMLING i elektroniske rapporteringsformater
description: Dette emne beskriver, hvordan du kan bruge datakilder for DATAINDSAMLING i elektroniske rapporteringsformater (ER).
author: NickSelin
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: f001734baf9aee59f0a61d21ca5a99af0c55b56f
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413586"
---
# <a name="use-data-collection-data-sources-in-electronic-reporting-formats"></a>Bruge datakilder for DATAINDSAMLING i elektroniske rapporteringsformater

[!include [banner](../includes/banner.md)]

Du kan bruge Operationsdesigner i strukturen for [Elektronisk rapportering (ER)](general-electronic-reporting.md) til at konfigurere [format](general-electronic-reporting.md#FormatComponentOutbound)komponenten i en ER-løsning, der bruges til at generere udgående dokumenter i forskellige formater. Den hierarkiske struktur i den konfigurerede formatkomponent består af forskellige formatelementtyper. Disse formatelementer bruges til at udfylde genererede dokumenter med de nødvendige oplysninger på kørselstidspunktet. Når du kører et ER-format, køres formatelementerne som standard i samme rækkefølge, som de vises i i formathierarkiet: ét ad gangen, fra top mod bund.

Når ER kører et formatelement, der indeholder en binding, køres formlen for denne binding, og formatelementet føjer værdien til et genereret dokument. Bindingen kan f.eks. overføre værdien fra et felt i en [datamodel](general-electronic-reporting.md#data-model-and-model-mapping-components) til et formatelement. Du kan konfigurere en datakilde for DATAINDSAMLING for at samle værdier fra datamodelfelter under kørslen, udføre summering af værdier og udfylde et genereret dokument med de indsamlede værdier. Hvis du vil bruge denne fremgangsmåde, skal du ændre den oprindelige binding, så den konfigurerede datakilde for DATAINDSAMLING bruges til at overføre værdien i et datamodelfelt til et formatelement. Når du overfører værdier gennem datakilden for DATAINDSAMLING, kan du indsamle krævede oplysninger til yderligere brug.

Når du konfigurerer en datakilde for DATAINDSAMLING, skal du angive en værditype, der skal administreres i datakilden. Følgende [datatyper](er-formula-supported-data-types-primitive.md) understøttes i øjeblikket ved indsamling af værdier:

- Boolesk
- Dato
- Dato/klokkeslæt
- Guid
- Int64
- Heltal
- Kommatal
- Streng
- Tidspunkt

Du kan bruge metoden `Collect(Value)` til datakilden for DATAINDSAMLING til at overføre en værdi til en datakilde med henblik på dataindsamling. I denne metode er argumentet `Value` enten en konstant eller den gyldige sti til et datakildefelt af den relevante datatype.

Brug egenskaben `Result` for en datakilde for DATAINDSAMLING til at få adgang til listen over indsamlede værdier. Denne egenskab returnerer en [postliste](er-formula-supported-data-types-composite.md#record-list). Posterne på postlisten indeholder feltet `Value`, som du kan bruge til at få adgang til de indsamlede værdier.

En datakilde for INDSAMLING AF DATA indsamler som standard kun entydige værdier.

Hvis du vil indsamle alle værdier, skal du angive feltet **Indsaml alle værdier** for den konfigurerede datakilde for DATAINDSAMLING til **Ja**. Når feltet **Indsaml alle værdier** er angivet til **Ja**, bliver den parameteriserede egenskab `Sum(Flag)` tilgængelig. Du kan bruge denne egenskab til at få totalen for alle aktuelt indsamlede værdier. I denne egenskab er argumentet `Flag` en [Boolesk](er-formula-supported-data-types-primitive.md#boolean) værdi, som bruges til at angive, om den samlede værdi skal nulstilles.

- Når værdien **Falsk** er angivet, fortsættes summeringen fra det tidligere indsamlede beløb.
- Når værdien **Sand** er angivet, startes der en ny summering.

Følgende datatyper understøttes i øjeblikket ved summering:

- Int64
- Heltal
- Kommatal

Hvis du vil vide mere om denne funktion, skal du fuldføre eksemplet nedenfor.

## <a name="example-configure-an-er-format-to-do-counting-and-summing-by-using-a-data-collection-data-source"></a>Eksempel: Konfigurer et ER-format for at udføre optælling og summering ved hjælp af en datakilde for DATAINDSAMLING

Dette eksempel viser, hvordan en bruger med rollen Systemadministrator eller Funktionel konsulent for elektronisk rapportering kan konfigurere et ER-format, der har en datakilde for DATAINDSAMLING, som bruges til at beregne løbende totaler og indsamle summerede værdier.

Procedurerne i dette eksempel kan fuldføres for USMF-firmaet i Microsoft Dynamics 365 Finance.

### <a name="upload-and-use-the-provided-er-solution"></a>Overføre og bruge den medfølgende ER-løsning

1. [Importere ER-eksempelkonfigurationerne](er-defer-sequence-element.md#import-the-sample-er-configurations).
2. [Aktivere en konfigurationsudbyder](er-defer-sequence-element.md#activate-a-configurations-provider).
3. [Gennemse den importerede modeltilknytning](er-defer-sequence-element.md#review-the-imported-model-mapping).
4. [Gennemse det importerede format](er-defer-sequence-element.md#review-the-imported-format).
5. [Køre det importerede format](er-defer-sequence-element.md#run-the-imported-format).

### <a name="run-the-format-of-the-provided-er-solution"></a>Køre formatet for den leverede ER-løsning

1. På siden **Formatdesigner** skal du vælge **Kør**.
2. Vælg **OK** i dialogboksen **Elektroniske rapporteringsparametre**.
3. Download og gennemse den fil, som webbrowseren tilbyder.

    ![Hentet fil, der indeholder resultaterne af den første formatudførelse](./media/er-data-collection-data-sources-01.png)

### <a name="modify-the-format-of-the-er-solution-to-calculate-the-running-tax-total"></a>Redigere ER-løsningens format for at beregne den løbende momstotal

Hvis mængden af transaktioner er meget større end mængden i det aktuelle eksempel, kan summeringen kræve mere tid og forringe ydeevnen. Hvis du ændrer indstillingerne for formatet, kan du afhjælpe disse problemer med ydeevnen. Da du har adgang til momsværdier for at kunne medtage dem i den genererede rapport, kan du genbruge disse oplysninger til summering af momsværdier.

1. Vælg fanen **Tilknytning** på siden **Formatdesigner**, og vælg **Tilføj rod**.
2. I dialogboksen **Tilføj datakilde** skal du vælge **Funktioner** \> **Dataindsamling**.
3. Benyt følgende fremgangsmåde i dialogboksen **Egenskaber for datakilde for dataindsamling**:

    1. Angiv **CollectedTaxValues** i feltet **Navn**.
    2. Vælg **Kommatal** i feltet **Varetype**.
    3. Vælg **Ja** i feltet **Indsaml alle værdier**.
    4. Vælg **OK**.

4. Vælg det numeriske formatelement **Rapport\\Linjer\\Post\\TaxAmount**.

    > [!NOTE]
    > Bindingen `@.Value` er i øjeblikket konfigureret for dette element. Derfor fyldes et oprettet dokument med momsværdier fra feltet `model.Data.List.Value`.

5. Vælg **Rediger formel**.
6. På siden **Formeldesigner** skal du følge disse trin:

    1. I feltet **Formel** skal du erstatte `@.Value` med `CollectedTaxValues.Collect(@.Value)`.
    2. Gem ændringerne, og luk siden.

    > [!NOTE]
    > Den nye binding sender samme momsværdier til et genereret dokument. Disse værdier vil dog også blive indsamlet i datakilden **CollectedTaxValues**.

7. Vælg det numeriske formatelement **Rapport\\Linjer\\Post\\RunningTotal**.
8. Vælg **Rediger formel**.
9. På siden **Formeldesigner** skal du følge disse trin:

    1. I feltet **Formel** skal du angive `CollectedTaxValues.Sum(false)`:
    2. Gem ændringerne, og luk siden.

    > [!NOTE]
    > Den nye binding sender det samlede momsværdibeløb, der allerede er angivet, til et genereret dokument.

    ![Numeriske elementer, der har opdaterede bindinger på siden Formatdesigner](./media/er-data-collection-data-sources-02.png)

10. Vælg **Gem**, og vælg derefter **Kør**.
11. Vælg **OK** i dialogboksen **Elektroniske rapporteringsparametre**.
12. Download og gennemse den fil, som webbrowseren tilbyder.

    ![Hentet fil, der indeholder resultaterne af den ændrede formatudførelse](./media/er-data-collection-data-sources-03.png)

### <a name="modify-the-format-to-evaluate-the-list-of-collected-tax-values"></a>Redigere formatet for at evaluere listen over indsamlede momsværdier

1. Under fanen **Format** på siden **Formatdesigner** skal du vælge det numeriske formatelement **Rapport\\Linjer\\Post\\RunningTotal** og derefter følge disse trin:

    1. Rediger værdien fra **Kommatal** til **Heltal** i feltet **Numerisk type**.
    2. I feltet **Numerisk format** skal du ændre værdien fra **F2** til **F0**.

3. Vælg **Rediger formal** under fanen **Tilknytning**.
4. På siden **Formeldesigner** skal du følge disse trin:

    1. I feltet **Formel** skal du angive `COUNT(CollectedTaxValues.Result)`:
    2. Gem ændringerne, og luk siden.

    > [!NOTE]
    > Den nye binding overfører antallet af poster på den liste, hvor momsværdierne er indsamlet, til i et genereret dokument.

5. Vælg **Gem**, og vælg derefter **Kør**.
6. Vælg **OK** i dialogboksen **Elektroniske rapporteringsparametre**.
7. Download og gennemse den fil, som webbrowseren tilbyder.

    ![Hentet fil, der indeholder resultaterne af en anden ændret formatudførelse](./media/er-data-collection-data-sources-04.png)

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions"></a>Hvis jeg skal beregne løbende totaler og indsamle data, hvad er forskellen mellem at bruge en datakilde for DATAINDSAMLING og de indbyggede funktioner til DATAINDSAMLING?

Både en datakilde for DATAINDSAMLING og de indbyggede funktioner til [DATAINDSAMLING](er-functions-category-data-collection.md) kan bruges til indsamling, summering og optælling af data baseret på de oplysninger, der overføres til et genereret udgående dokument. Når du forsøger at afgøre, hvilken metode der skal anvendes, skal du dog overveje følgende punkter.

| Datakilde | Indbyggede funktioner |
|-------------| ------------------ |
| Der indsamles kun værdier. | <p>Der indsamles navngivne værdier. Totaler kan derfor beregnes for separate grupper af værdier.</p><p>Derudover kan grupper udtrækkes som en liste.</p><p>Der kan også indsamles tekstværdier.</p> |
| Entydige værdier samles automatisk. | Der kræves yderligere indstillinger for at udtrække en liste over entydige værdier fra de indsamlede værdier. |
| Ydeevnen afhænger af mængden af indsamlede værdier. | I praksis afhænger ydeevnen ikke af mængden af indsamlede værdier. |
| Denne metode fungerer for alle typer udgående dokumenter. | Denne metode fungerer kun for tekst- og XML-dokumenter. |

## <a name="additional-resources"></a>Yderligere ressourcer

- [Konfigurere format for at udføre optælling og sammenlægning](./tasks/er-format-counting-summing-1.md)
- [Udskyde udførelse af sekvenselementer i ER-formater](er-defer-sequence-element.md#Example)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
