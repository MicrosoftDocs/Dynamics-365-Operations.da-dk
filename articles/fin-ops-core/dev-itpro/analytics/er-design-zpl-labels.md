---
title: Designe en ny ER-løsning til udskrivning af ZPL-labels
description: Dette emne forklarer, hvordan du kan designe en ny elektronisk rapporteringsløsning (ER) til udskrivning af ZPL-labels (Zebra Programming Language).
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: c1bedf1184b45741102000fa68c8d662c7383301
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612346"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>Designe en ny ER-løsning til udskrivning af ZPL-labels

[!include [banner](../includes/banner.md)]


I dette emne forklares det, hvordan en bruger i rollen Systemadministrator, Udvikler af elektronisk rapportering eller Funktionel konsulent til elektronisk rapportering kan konfigurere parametre for [ER-strukturen](general-electronic-reporting.md), designe de krævede [konfigurationer](general-electronic-reporting.md#Configuration) af en ny ER-løsning for at få adgang til dataene i et bestemt Warehouse Management-system og generere brugerdefinerede lagerstedslabels i ZPL II-format. Disse trin kan udføres i **USRT**-virksomheden.

## <a name="business-scenario"></a>Forretningsscenarie

Du repræsenterer et firma, der implementerede Lokationsstyring i Microsoft Dynamics 365 Finance. Alle lagersteder skal have en etiket med en selvklæbende label, som indeholder en stregkode. Lagerarbejdere skal bruge den håndholdte stregkodelæser til at scanne stregkoderne.

Alle lagersteder er markeret med label i omfanget af aktiviteter før udgivelsen. Du skal dog også kunne udskrive lagerstedslokationslabels efter behov, hvis eksisterende labels bliver beskadiget, eller hvis lagerstedets reolkonfiguration ændres. Ved hjælp af nyudgivne ER-funktioner kan du konfigurere en ny ER-løsning, der giver en lagerchef mulighed for at udskrive labels direkte til en termisk etiketprinter.

## <a name="configure-the-er-framework"></a>Konfigurere ER-strukturen

Følg trinnene i [Konfigurere ER-strukturen](er-quick-start2-customize-report.md#ConfigureFramework) for at konfigurere det minimale sæt af ER-parametre. Du skal fuldføre denne opsætning, før du begynder at bruge ER-strukturen til at designe en ny ER-løsning.

## <a name="design-a-domain-specific-data-model"></a>Designe en domænespecifik datamodel

Opret en ny ER-konfiguration, der indeholder en komponent med [datamodellen](er-overview-components.md#data-model-component) til domænet Lokationsstyring. Denne datamodel vil senere blive brugt som en datakilde, når du designer et ER-format til at generere lagerstedslokationslabels.

### <a name="import-a-data-model-configuration"></a>Importere en datamodelkonfiguration

Følg disse trin for at importere den påkrævede datamodel fra en XML-fil, der leveres af Microsoft. Du kan også oprette din egen datamodel som beskrevet i næste afsnit.

1. Download filen [Warehouse model.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml), og gem den på din lokale computer.
2. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
3. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.
4. Gå til siden **Konfigurationer**, og vælg **Kurs** \> **Indlæs fra XML-fil** i handlingsruden.
5. Vælg **Gennemse**, og find og vælg derefter filen **Warehouse model.version.1.xml**.
6. Vælg **OK** for at importere konfigurationen.

![Importeret ER-datamodelkonfiguration på siden Konfigurationer.](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>Oprette en datamodelkonfiguration

I stedet for at importere den datamodelfil, der leveres af Microsoft, kan du oprette en datamodel fra bunden. Du kan finde et eksempel på, hvordan du fuldfører denne opgave, under [Oprette en ny datamodelkonfiguration ](er-quick-start1-new-solution.md#DesignDataModel).

### <a name="review-the-data-model"></a>Gennemse datamodellen

Du kan få vist en version af den konfigurerede datamodel, der kan redigeres, på siden **Datamodeldesigner**.

![ER-datamodellens struktur på datamodeldesignersiden.](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>Designe en modeltilknytning for den konfigurerede datamodel

Som bruger i rollen Udvikler af elektronisk rapportering skal du oprette en ny ER-konfiguration, der indeholder en komponent for [modeltilknytning](er-overview-components.md#model-mapping-component) til datamodellen Lagersted. Denne komponent implementerer den konfigurerede datamodel for Dynamics 365 Finance og er specifik for denne app. Du skal konfigurere den for at angive de applikationsobjekter, der skal bruges til at udfylde den konfigurerede datamodel med applikationsdata under kørsel. For at fuldføre denne opgave skal du vide, hvordan datastrukturen i forretningsdomænet Lokationsstyring er implementer i Finance.

### <a name="import-a-model-mapping-configuration"></a>Importere en konfiguration af modeltilknytning

Følg disse trin for at importere den påkrævede modeltilknytning fra en XML-fil, der leveres af Microsoft. Du kan også oprette din egen modeltilknytning som beskrevet i næste afsnit.

1. Download filen [Warehouse model mapping.version.1.1.xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml), og gem den på din lokale computer.
2. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
3. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.
4. Gå til siden **Konfigurationer**, og vælg **Kurs** \> **Indlæs fra XML-fil** i handlingsruden.
5. Vælg **Gennemse**, og find og vælg derefter filen **Warehouse model mapping.version.1.1.xml**.
6. Vælg **OK** for at importere konfigurationen.

![Importeret konfiguration af ER-modeltilknytning på siden Konfigurationer.](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>Oprette en konfiguration af modeltilknytning

I stedet for at importere den modeltilknytningsfil, der leveres af Microsoft, kan du oprette en modeltilknytning fra bunden. Du kan finde et eksempel på, hvordan du fuldfører denne opgave, under [Oprette en ny konfiguration af modeltilknytning](er-quick-start1-new-solution.md#CreateModelMapping).

### <a name="review-the-model-mapping"></a>Gennemse modeltilknytningen

Du kan få vist en version af den konfigurerede modeltilknytning, der kan redigeres, på siden **Modeltilknytningsdesigner**.

![ER-modeltilknytningens struktur på siden Modeltilknytningsdesigner.](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>Design et format

Som bruger med rollen Funktionel konsulent i elektronisk rapportering skal du oprette en ny ER-konfiguration, der indeholder en komponent for [format](er-overview-components.md#format-component). Hvis du vil konfigurere denne komponent, skal du bruge ZPL II-kode til at angive layoutet for lagerstedslokationens label.

### <a name="import-a-format-configuration"></a>Importere en formatkonfiguration

Følg disse trin for at importere det påkrævede format fra en XML-fil, der leveres af Microsoft. Du kan også oprette dit eget format som beskrevet i næste afsnit.

1. Download filen [Warehouse location labels.version.1.1.xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml), og gem den på din lokale computer.
2. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
3. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.
4. Gå til siden **Konfigurationer**, og vælg **Kurs** \> **Indlæs fra XML-fil** i handlingsruden.
5. Vælg **Gennemse**, og find og vælg derefter filen **Warehouse location labels.version.1.1.xml**.
6. Vælg **OK** for at importere konfigurationen.

![Importeret ER-formatkonfiguration på siden Konfigurationer.](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>Oprette en formatkonfiguration

I stedet for at importere den formatfil, der leveres af Microsoft, kan du oprette et format fra bunden. Du kan finde et eksempel på, hvordan du fuldfører denne opgave, under [Oprette en ny formatkonfiguration](er-quick-start1-new-solution.md#FormatCreate).

### <a name="review-the-format"></a>Gennemse formatet

Du kan få vist en version af det konfigurerede format, der kan redigeres, på siden **Formatdesigner**.

![ER-formatets struktur på siden Formatdesigner.](./media/er-design-zpl-labels-format.png)

Datakilden `model.Location.Label` for dette format er konfigureret til at generere labels, der indeholder følgende oplysninger:

- Lagerstedets titel som tekst
- Lagerstedets titel som en stregkode
- Lokationens titel
- Kontrolcifre

På siden **Formeldesigner** til datakilden indeholder den ER-formel, der bruges til at generere labels, en `CONCATENATE`-funktion, der kombinerer oplysningerne i det ønskede layout.

![Formel for datakilden på siden Formeldesigner.](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> Labellayoutet er designet, så lokationens titel og kontrolcifre er justeret i midten af labels. ZPL II understøtter dog ikke centerjustering for stregkoder. Formlen for `model.Location.Warehouse.Alignment`-datakilden bruges derfor til at justere stregkoden i midten af labelen. I denne formel beregnes den venstre forskydning af stregkoden på basis af antallet af tegn i lagerstedets titel.

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>Forberede miljøet til forhåndsvisning af genererede labels

I følgende eksempel bruges et printer-emulatorprogram til ZPL-labels til eksempelvisning af genererede labels på skærmen. Følg disse trin for at aktivere funktionen.

1. Tilføj [Printer](er-destination-type-print.md) ER-destinationen for ER-formatet af **Lagerstedslokationens label**, og konfigurer den til at sende genererede labels fra Finans til [DRA (dokumentets ruteplanlægningsagent)](install-document-routing-agent.md).
2. Installer og konfigurer DRA'et, så genererede labels fra Finans dirigeres til en lokal printer, som der er adgang til fra den aktuelle arbejdsstation.
3. Tilføj en lokal printer for den aktuelle arbejdsstation, og konfigurer den til at overføre genererede labels fra DRA til et printer-emulatorprogram.
4. Installer et printer-emulatorprogram som en udvidelse af Chrome-webbrowseren, og konfigurer det til at overføre genererede labels fra en lokal printer til en webtjeneste, der gengiver genererede labels og returnerer dem til printeremulatoren til eksempelvisning.

<table>
<tbody>
<tr align="center">
<td>
<p>Finance</p>
<p>ER-rapport</p>
<p>Printerdestination</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>Dokumentets ruteplanlægningsagent</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>Lokal printer</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>Printeremulator</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>Gengivelseswebtjeneste</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>Installere og konfigurere et printeremulatorprogram

Tilføj et printeremulatorprogram til ZPL-gengivelsesprogrammet til din Chrome-webbrowser. I dette eksempel bruges den [ZPL-printeremulator](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo), der er baseret på [iwebtjenesten Labelary ZPL](http://labelary.com/service.html). Printeremulatorprogrammet sender genererede labels i ZPL-format fra en lokal printer til webtjenesten og returnerer derefter labels som PDF- eller PNG-filer til forhåndsvisning.

1. Find og vælg det printeremulatorprogram, du vil bruge, i Chrome-weblageret. Vælg derefter **Føj til Chrome** for at føje det til din Chrome-webbrowser.

    ![Tilføjelse af printeremulatorprogrammet til Chrome-webbrowseren fra Chrome-webbutikken.](./media/er-design-zpl-labels-add-app.png)

2. Vælg **Start-app** for at køre printeremulatorprogrammet fra Chrome-webbrowseren.

    ![Kørsel af printeremulatorprogrammet fra Chrome-webbrowseren.](./media/er-design-zpl-labels-run-app.png)

3. Konfigurere kørsel af programmet:

    1. Slå programmet fra.
    2. Angiv værtscomputeren til **127.0.0.1** i printerindstillingerne.
    3. Angiv porten til **9100**.

        ![Konfigurering af printeremulatorprogrammet.](./media/er-design-zpl-labels-configure-app.png)

    4. Slå programmet til igen. Du skal modtage en meddelelse om, at printeren blev startet på den angivne vært og port.

        ![Printeremulatorprogrammet aktiveret igen.](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> Da det printeremulatorprogram, der bruges i dette eksempel, er baseret på en webtjeneste, der gengiver labels, skal du sørge for, at sikkerhedsindstillingerne giver dig mulighed for at kommunikere med tjenesten. Ellers modtager programmet ikke de gengivne labels, og det er ikke muligt at få vist disse labels som eksempler.

### <a name="add-and-configure-a-local-printer"></a>Tilføje og konfigurere en lokal printer

[Tilføj en ny lokal printer](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b), som den aktuelle enhed kan bruge til at overføre genererede labels fra DRA til printeremulatorprogrammet.

1. I Windows skal du vælge **Start** \> **Indstillinger** \> **Enheder** \> **Printere \& scannere**.
2. Vælg **Indstillinger for printere \& scannere**.
3. For **Tilføj en printer eller en scanner** skal du vælge **Tilføj enhed**.
4. Vælg **Tilføj manuelt** for **Den printer, jeg søger efter, findes ikke på listen**.
5. Vælg **Tilføj en lokal printer eller netværksprinter med manuelle indstillinger** i feltet **Find en printer efter andre indstillinger**.
6. Vælg **Opret en ny port** i feltet **Vælg en printerport**, og benyt derefter følgende fremgangsmåde:

    1. Vælg **Standard TCP/IP-port** i feltet **Porttype**.
    2. Angiv **127.0.0.1** i feltet **Værtsnavn eller IP-adresse**.
    3. Angiv **ZPL** i feltet **Portnavn**.
    4. Vent, indtil handlingen **Registrerer TCP/IP-port** er fuldført.
    5. Vælg **Brugerdefineret** i feltet **Enhedstype**, og vælg derefter **Indstillinger**.
    6. Kontrollér, at følgende portindstillinger er angivet:

        - **Portnavn:** ZPL
        - **Printernavn eller IP-adresse:** 127.0.0.1
        - **Protokol:** Rå
        - **Portnummer:** 9100

7. Vælg **Generisk / Kun tekst** i feltet **Installer printerdriver**.
8. Angiv **ZebraPrinter** i feltet **Printernavn**.

![Tilføjelse af en lokal printer for den aktuelle enhed.](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>Installere og konfigurere DRA

Forberede DRA til at sende genererede labels fra Finans til den konfigurerede lokale printer.

1. [Installer DRA](install-document-routing-agent.md#install-the-document-routing-agent).
2. [Konfigurer DRA](install-document-routing-agent.md#configure-the-document-routing-agent).
3. [Registrer den lokale printer](install-document-routing-agent.md#register-network-printers) i DRA.
4. [Aktivér den lokale printer](install-document-routing-agent.md#administer-network-printers) i Finans-miljøet.

![Forberede DRA til at udskrive genererede labels.](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>Konfigurere ER-destinationen

Forberede ER-destinationen til at sende genererede labels fra Finans til DRA.

1. Gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Destination for elektronisk rapportering**.
2. Vælg **Ny** i handlingsruden på siden **Destination for elektronisk rapportering**.
3. Vælg **Lagerstedslokationslabels** i feltet **Reference**.
4. Vælg **Ny** i oversigtspanelet **Fildestination**.
5. I feltet **Navn** skal du angive **Labels**.
6. Angiv **Rapport** i feltet **Filkomponentnavn**.
7. Vælg **Indstillinger**.
8. I dialogboksen **Indstillinger for destination**, skal du angive indstillingen **Aktiveret** til **Ja** under fanen **Printer**.
9. Vælg **ZebraPrinter** i feltet **Printernavn**.
10. Vælg **ZPL** i feltet **Dokumentrutetype**.
11. Vælg **OK**.

![Konfiguration af ER-destinationen til formatet Lagerstedslokationslabels på siden Destination for elektronisk rapportering.](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>Gennemgå lagerstedslokationer

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Lagersted** \> **Lokationer**.
2. Filtrer på siden **Lokationer** for kun at få vist lokationer, der har en værdi i feltet **Kontrolcifre**.

![Gennemgå lagerlokationer på siden Lokationer.](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>Udskrive lokationslabels til lagersteder

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet udvide **Model for lagersted** og vælge **Lagerstedslokationslabels**.
3. Vælg **Kør** i handlingsruden.
4. Vælg **Filter** i dialogboksen **Parametre for elektronisk rapport** under fanen **Poster, der skal medtages**.
5. Under fanen **Område** skal du finde den række, hvor feltet **Tabel** er indstillet til **Lokationer**, og feltet **Felt** er indstillet til **Lokation**. Angiv **LPEnabled** i feltet **Kriterier**.
6. Vælg **OK**.
7. Vælg **OK**. Der genereres en label, som vises på eksempelsiden i printeremulatorprogrammet.

![Gennemgang af en genereret label eksempelsiden i ZPL-printeremulatorprogrammet.](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>Redigere layoutet af en label

Du kan ændre det aktuelle layout af lokationslabels til lagersteder. I følgende eksempel vises det, hvordan du kan ændre layoutet, så genererede labels indeholder et lokationsprofil-id.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Angiv **Anvend destinationer for kladdetilstand** som [ER-brugerparameter](electronic-reporting-destinations.md#applicability) til **Ja**.
3. På siden **Konfigurationer** skal du i konfigurationstræet udvide **Model for lagersted** og vælge **Lagerstedslokationslabels**.
4. Vælg **Designer**.
5. På siden **Formatdesigner** under fanen **Tilknytning** kan du udvide datakilden `model.Location.Label`.
6. Vælg **Rediger** \> **Rediger formel** i dialogboksen **Egenskaber for datakilde**.
7. Gennemse den ER-formel, der bruges til at generere labels, i feltet **Formel** på siden **Formeldesigner**.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. Opdater formlen, så der tilføjes et lokationsprofil-id til genererede labels.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^CF0,40,40^FO0,240^FB800,1,0,C,0^FD",@.ProfileID,"\&^FS",CrLf,
    "^XZ")
    ```

9. Vælg **Gem**.
10. Vælg **OK**.
11. Vælg **Kør** i handlingsruden.
12. Vælg **Filter** i dialogboksen **Parametre for elektronisk rapport** under fanen **Poster, der skal medtages**.
13. Under fanen **Område** skal du finde den række, hvor feltet **Tabel** er indstillet til **Lokationer**, og feltet **Felt** er indstillet til **Lokation**. Angiv **Bay** i feltet **Kriterier**.
14. Vælg **OK**.
15. Vælg **OK**. Der genereres en label, som vises på eksempelsiden i printeremulatorprogrammet.

![Gennemse en genereret label, der indeholder et lokationsprofil-id på eksempelsiden i Zpl-printeremulatorprogrammet.](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>Kodning

> [!NOTE]
> Du skal synkronisere kodningsindstillingen for komponenten **Fælles\\Fil** i det redigerbare ER-format og den relevante indstilling af den designede label. Værdien i feltet **[Kodning](er-suppress-bom-characters.md)** for komponenten **Fælles\\Fil** bør ikke modsige en ZPL-kommando, der bruges til at styre labelens kodning (f.eks. kommandoen `^CI`). ER validerer ikke, at disse indstillinger synkroniseres.

## <a name="additional-resources"></a>Yderligere ressourcer

[Printerdestination](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
