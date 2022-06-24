---
title: Tilføj nye felter til en skabelon for forretningsdokument i Microsoft Excel
description: Denne artikel indeholder oplysninger om, hvordan du kan tilføje nye felter til en skabelon til forretningsdokument i Microsoft Excel ved hjælp af funktionen Styring af forretningsdokument.
author: NickSelin
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 8395a87e88ebbd1942c87da0cecebe6d25bdf625
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869396"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a>Tilføj nye felter til en skabelon for forretningsdokument i Microsoft Excel

[!include[banner](../includes/banner.md)]

Du kan tilføje nye felter til en skabelon, der bruges til at generere forretningsdokumenter i Microsoft Excel-format. Disse felter kan tilføjes som pladsholdere, der bruges til at udfylde genererede dokumenter med de nødvendige oplysninger fra programmet. For hvert felt, du tilføjer, kan du også angive en binding til datakilderne for at angive, hvilke programdata der skal indsættes i feltet, når skabelonen bruges til at generere forretningsdokumenter.

Hvis du vil vide mere om denne funktion, skal du fuldføre eksemplet i denne artikel. I dette eksempel vises, hvordan du kan opdatere en skabelon for at udfylde de felter, der genereres i fritekstfakturaformler.

## <a name="configure-business-document-management-to-edit-templates"></a>Konfigurer Styring af forretningsdokumenter til at redigere skabeloner

Da Styring af forretningsdokument (BDM) er bygget oven på [Oversigten over Elektronisk rapporteringsstrukturen (ER)](general-electronic-reporting.md), skal du konfigurere de krævede parametre ER og BDM, før du kan begynde at arbejde med BDM.

1.  Log ind på forekomsten af Microsoft Dynamics 365 Finance som systemadministrator.
2.  Fuldfør følgende trin i eksemplet i artiklen [Oversigt over styring af forretningsdokumenter](er-business-document-management.md):

    1.  Konfigurer ER-parametre.
    2.  Aktivér BDM.

Du kan nu begynde at bruge BDM til at redigere skabeloner til forretningsdokumenter.

## <a name="import-er-solutions-that-contain-a-template"></a>Importer løsninger, der indeholder en skabelon

I eksemplet i denne procedure bruges den officielt publicerede ER-løsning. Du skal importere ER-konfigurationerne for denne løsning i den aktuelle forekomst af Finance.

ER-formatkonfigurationen af **Fritekstfakturaen (Excel)** indeholder skabelonen for forretningsdokumenter i Excel, der kan redigeres ved hjælp af BDM. Importer den seneste version af denne ER-formatkonfiguration fra Microsoft Dynamics Lifecycle Service (LCS). Varianter af den tilsvarende ER-datamodel og konfigurationer af ER-modeltilknytninger importeres automatisk.

Du kan finde flere oplysninger om, hvordan du importerer ER-konfigurationer under [Administrere livscyklus for ER-konfiguration](general-electronic-reporting-manage-configuration-lifecycle.md).

![Siden for Delt LCS-aktivbibliotek.](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a>Rediger skabelonen for ER-løsningen

1.  Log på som bruger med adgang til arbejdsområdet **Styring af forretningsdokumenter**.
2.  Åbn arbejdsområdet til **Styring af forretningsdokumenter**.

    ![Arbejdsområdet til Styring af forretningsdokumenter.](./media/BDM-AddFldExcel-Workspace.png)

3.  Vælg skabelonen til **Fritekstfakturaer (Excel)** i gitteret.
4.  I højre rude skal du vælge **Ny skabelon** for at oprette en ny skabelon, der er baseret på den valgte skabelon.
5.  I feltet **Titel** skal du angive **Fritekstfaktura (Excel) Contoso** som titlen på den nye skabelon.
6.  Vælg **OK** for at bekræfte starten af redigeringsprocessen.

Siden BDM-skabeloneditor vises. Du kan bruge Microsoft 365 til at redigere den valgte skabelon online i det integrerede kontrolelement.

![Siden med BDM-skabeloneditor.](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a>Tilføj etiketten for et nyt felt til skabelonen

1.  På siden med BDM-skabeloneditor skal du på Excel-båndet på fanen **Vis** vælge afkrydningsfelterne **Overskrifter og gitterlinjer** for den redigerbare Excel-skabelon.

    ![Afkrydsningsfelterne Overskrifter og Gitterlinjer er markerede.](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  Marker cellerne **E8:F8**.
3.  På Excel-båndet under fanen **Startside** skal du vælge **Flet & Centrer** for at flette de markerede celler ind i en sammenflettet **E8:F8**-celle.
4.  I den sammenflettede celle **E8:F8** skal du indtaste **URL-adressen**.
5.  Vælg flettet celle **E7:F7**, vælg **Formatpensel**, og vælg derefter den sammenflettede celle **E8:F8** for at formatere den på samme måde som den flettede celle **E7:F7**.

    ![Etiketten "Nyt felt" er tilføjet til skabelonen.](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a>Formater skabelonen for at reservere plads til et nyt felt

1.  På siden med BDM-skabeloneditor skal du vælge den sammenflettede celle **G8:H8**.
2.  På Excel-båndet under fanen **Startside** skal du vælge **Flet & Centrer** for at flette de markerede celler ind i en sammenflettet **G8:H8**-celle.
3.  Vælg flettet celle **G7:H7**, vælg **Formatpensel**, og vælg derefter den sammenflettede celle **G8:H8** for at formatere den på samme måde som den flettede celle **G7:H7**.

    ![Plads, der er reserveret til det nye felt.](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  I afkrydsningsfeltet **Navn** skal du vælge **FirmaInfo**.

    Intervallet **FirmaInfo** i den aktuelle Excel-skabelon indeholder alle de felter, der bruges til at udfylde overskriften i en genereret rapport med detaljer om det aktuelle firma som sælgende part.

    ![Interval for FirmaInfo er valgt.](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a>Tilføj et nyt felt til skabelonen

1.  På siden **BDM-skabeloneditor** skal du i handlingsruden vælge **Vis format**.
2.  I ruden **Skabelonstruktur** skal du vælge **Tilføj**.

    > [!NOTE]
    > Du skal justere den sektion i skabelonen, du vil bruge som et nyt felt. Du har allerede gennemført denne justering ved at formatere den flettede celle **G8:H8**.

    ![Sådan tilføjer du et nyt felt til skabelonen.](./media/BDM-AddFldExcel-AddCell.png)

3.  Vælg **Excel\Celle** for at tilføje et nyt felt som en celle i skabelonen.

    Du kan vælge **Excel\Interval**, hvis du vil føje et nyt interval til skabelonen. Det angivne interval kan indeholde flere celler. Du kan tilføje disse celler senere.
    
    Bemærk, at skabelonkomponenten **FirmaInfo** automatisk vælges i ruden **Skabelonstruktur**, fordi det er det mest passende overordnede komponent i den aktuelle skabelonstruktur for det felt, du tilføjer.
    
4.  I feltet **Excel-interval** skal du indtaste **FirmaURL_Værdi**.
5.  Vælg **OK**.

    ![Feltet FirmaURL_Værdi tilføjes til skabelonstrukturen.](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  I ruden **Skabelonstruktur** skal du vælge ellipseknappen (...) og dernæst vælge **Vis bindinger**.

    ![Vis valgte bindinger.](./media/BDM-AddFldExcel-ShowBindings.png)

    I ruden **Skabelonstruktur** vises nu de datakilder, der er tilgængelige i det underliggende ER-format.

7.  Vælg **FirmaInfo_værdi** som det felt, du har planer om at binde til en datakilde for det underliggende ER-format.
8.  I sektionen **Datakilder** i ruden **Skabelonstruktur** skal du udvide **Model \> FakturaGrundlag \> FirmaInfo**.
9.  Under **FirmaInfo** skal du vælge elementet **WebsiteURL**.

    ![Elementet WebsiteURL er valgt.](./media/BDM-AddFldExcel-BindURL.png)

10. Vælg **Bind**.
11. I ruden **Skabelonstruktur** skal du vælge **Gem** og dernæst lukke siden med BDM-skabeloneditor.

I arbejdsområdet **Styring af forretningsdokumenter** vises den opdaterede skabelon på fanen **Skabelon** i højre rude. Bemærk, at feltet **Status** for den redigerede skabelon er ændret til **Kladde** i gitteret, og at feltet **Revision** ikke længere er tomt. Disse ændringer betyder, at processen for redigering af denne skabelon er startet.

![Redigeret skabelon i arbejdsområdet Styring af forretningsdokument.](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a>Gennemgå firmaindstillinger

1.  Gå til **Organisationsadministration \> Organisationer \> Juridiske enheder**.
2.  I oversigtspanelet **Kontaktinformation** skal du verificere, at firmaets URL-adresse er angivet.

![Firmaets URL-adresse angives på siden Juridiske enheder.](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a>Generer forretningsdokumenter for at teste den opdaterede skabelon

1.  I programmets skal du ændre firmaet til **USMF** og gå til **Debitor \> Fakturaer \> Alle fritekstfakturaer**.
2.  Vælg fakturaen **FTI-00000002**, og vælg derefter **Udskriftsstyring**.
3.  I venstre rude skal du udvide **Modul - debitor \> Dokumenter \> Fritekstfaktura**.
4.  Under **Fritekstfaktura** skal du vælge niveauet for det **Originale dokument** for at angive, hvilke fakturaer der skal behandles.
5.  I højre rude i feltet **Rapportformat** skal du vælge skabelonen **Fritekstfaktura (Excel) Contoso** for det angivne dokumentniveau.

    ![Skabelonen Fritekstfaktura (Excel) Contoso er valgt.](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  Tryk på **Esc** for at lukke den aktuelle side.
7.  Vælg **Udskriv \> Valgte**.
8.  Hent det genererede dokument, og åbn det i Excel.

    ![Fritekstfaktura i Excel.](./media/BDM-AddFldExcel-PreviewReport.png)

Den ændrede skabelon bruges til at generere rapporten med fritekstfaktura for den valgte vare. Hvis du vil analysere, hvordan denne rapport påvirkes af de ændringer, du har foretaget i skabelonen, skal du køre denne rapport i én programsession umiddelbart efter, at du har ændret skabelonen i en anden programsession.

## <a name="related-links"></a>Relaterede links

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Oversigt over styring af forretningsdokumenter](er-business-document-management.md)

[Designe en konfiguration til generering af rapporter i OPENXML-format](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]