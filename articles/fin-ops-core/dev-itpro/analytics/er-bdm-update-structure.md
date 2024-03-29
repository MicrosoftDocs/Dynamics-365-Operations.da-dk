---
title: Opdatere strukturen for en forretningsdokumentskabelon
description: Denne artikel forklarer, hvordan du opdaterer strukturen i en skabelon til et forretningsdokument ved hjælp af funktionen til administration af forretningsdokumenter.
author: kfend
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.custom: ''
ms.assetid: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
ms.openlocfilehash: 793f327a3e5861e03b6ae67da8149f1db11e47bd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285509"
---
# <a name="update-the-structure-of-a-business-document-template"></a>Opdatere strukturen for en forretningsdokumentskabelon 

[!include[banner](../includes/banner.md)]

I ruden **Skabelonstruktur** i editoren for skabeloner til [administration af forretningsdokumenter](er-business-document-management.md) kan du redigere en skabelon til forretningsdokumenter ved at [føje nye felter](er-bdm-add-field-to-excel-template.md) til skabelonen i Microsoft Excel. Skabelonens struktur opdateres derefter automatisk i Dynamics 365 Finance, så den afspejler de ændringer, du har foretaget i ruden **Skabelonstruktur**.

Du kan også redigere en skabelon ved hjælp af Office 365-onlinefunktioner. Du kan f.eks. føje et nyt navngivet element, f.eks. et billede eller en figur, til det redigerbare regneark. I dette tilfælde opdateres skabelonens struktur ikke automatisk i Finans, og det element, du har tilføjet, vises ikke i ruden **Skabelonstruktur**. Opdater skabelonstrukturen manuelt i Finans ved at vælge **Opdater struktur** på editorsiden for skabelonen.

Du kan få flere oplysninger om denne funktion ved at udføre følgende eksempel.

## <a name="example-update-the-structure-of-a-business-document-template"></a>Eksempel: Opdatere strukturen for en forretningsdokumentskabelon

Dette eksempel viser, hvordan en systemadministrator kan opdatere strukturen i en skabelon til et forretningsdokument i Finans, når skabelonen er ændret i Office Online. I følgende afsnit beskrives de trin, der skal udføres.

### <a name="prepare-a-business-document-template-for-editing"></a>Forberede en skabelon til forretningsdokumenter til redigering

Gennemfør følgende procedurer i [Oversigt over styring af forretningsdokumenter](er-business-document-management.md).

1. [Konfigurere ER-parametre](er-business-document-management.md#configure-er-parameters)
2. [Importere ER-løsninger](er-business-document-management.md#import-er-solutions)
3. [Aktivere styring af forretningsdokumenter](er-business-document-management.md#enable-business-document-management)
4. [Konfigurere parametre](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>Redigere en forretningsdokumentskabelon

1. I arbejdsområdet **Styring af forretningsdokumenter** skal du vælge **Nyt dokument**.
2. Vælg skabelonen **Fritekstfaktura (ER-eksempel) (Excel)** på siden **Opret en ny skabelon**.
3. Vælg **Opret dokument**.
4. I feltet **Titel** skal du angive **FTI-eksempel Litware**.
5. Vælg **OK** for at oprette den nye skabelon.

    > [!NOTE]
    > Hvis du endnu ikke er logget på Office Online, bliver du [omdirigeret til Office 365-logonsiden](er-business-document-management.md#frequently-asked-questions). Hvis du vil vende tilbage til Finans-miljøet, skal du vælge knappen **Tilbage** i browseren.

    Den nye skabelon åbnes til redigering i det integrerede Excel Online-kontrolelement på editorsiden for skabelonen.

[![Bruge arbejdsområdet Styring af forretningsdokumenter til at starte redigering af en skabelon til forretningsdokumenter.](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>Gennemse den aktuelle struktur i den redigerbare skabelon

1. I Excel Online skal du gå til båndet, vælge fanen **Vis** og vælge **Gitterlinjer** i gruppen **Vis**.
2. Vælg rektanglet oven over skabelonens titel i den redigerbare skabelon. Dette rektangel er et billede med navnet **rptHeaderCompLogo**.
3. Hvis ruden **Skabelonstruktur** er skjult, skal du vælge **Vis struktur**.
4. I ruden **Skabelonstruktur** skal du udvide **Rapport \> Faktura \> rptHeader \> rptHeaderPart1**.
5. Bemærk, at elementet **rptHeaderCompLogo** i skabelonstrukturen i Finans vises som underordnet element til **Rapport \> Faktura \> rptHeader \> rptHeaderPart1**.

[![Bruge arbejdsområdet Styring af forretningsdokumenter til at gennemse den aktuelle struktur i en redigerbar skabelon.](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>Opdatere strukturen for en forretningsdokumentskabelon ved at slette et billede

1. Vælg billedet **rptHeaderCompLogo** i den redigerbare skabelon i Excel Online.
2. Benyt en af følgende fremgangsmåder for at slette det valgte billede fra den redigerbare skabelon:

    - Vælg **Slet**-tasten på tastaturet.
    - Vælg og hold nede på (eller højreklik på) billedet, og vælg derefter **Klip**.

    > [!NOTE]
    > Elementet **RptHeaderCompLogo** findes i øjeblikket stadig i skabelonstrukturen i Finans, selvom billedet ikke længere er medtaget i Excel-skabelonen.

3. Vælg **Opdater struktur** for at synkronisere den redigerbare skabelons struktur i Excel og Finans.
4. I ruden **Skabelonstruktur** skal du udvide **Rapport \> Faktura \> rptHeader \> rptHeaderPart1**.
5. Bemærk, at elementet **rptHeaderCompLogo** ikke længere er medtaget i skabelonstrukturen i Finans.

[![Bruge arbejdsområdet Styring af forretningsdokumenter til at slette et billede fra en skabelon til forretningsdokumenter.](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>Opdatere strukturen for en forretningsdokumentskabelon ved at tilføje et billede

1. I Excel Online skal du gå til båndet, vælge fanen **Indsæt** og vælge **Billede** i gruppen **Illustrationer**.
2. Vælg **Vælg fil**, gå til det billede, du vil tilføje, markér det, og vælg derefter **OK**.
3. Vælg **Indsæt**.
4. Flyt det nye billede, indtil det er på det rigtige sted. Som standard navngiver Excel billedet. Det kan f.eks. give billedet navnet **Billede 2**.
5. Vælg **Opdater struktur** for at synkronisere den redigerbare skabelons struktur i Excel og Finans.
6. I ruden **Skabelonstruktur** skal du udvide **Rapport \> Faktura \> rptHeader \> rptHeaderPart1**.
7. Bemærk, at det nye billede nu er medtaget som et element i skabelonstrukturen i Finans.

[![Bruge arbejdsområdet Styring af forretningsdokumenter til at føje et billede til en skabelon til forretningsdokumenter.](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>Relaterede links

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Oversigt over styring af forretningsdokumenter](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
