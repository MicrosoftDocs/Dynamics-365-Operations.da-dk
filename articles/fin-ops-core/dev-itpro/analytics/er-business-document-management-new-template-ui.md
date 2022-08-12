---
title: Microsoft Office-brugergrænsefladestil i styring af forretningsdokumenter (indeholder video)
description: Denne artikel indeholder oplysninger om, hvordan du kan bruge den nye brugergrænseflade til dokumenter i funktionen Styring af forretningsdokumenter i den elektroniske rapportering (ER).
author: v-anamir
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 208cfc91f11d4893785538ce4874e85a5725e993
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109254"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Microsoft Office-brugergrænsefladestil for nyt dokument i styring af forretningsdokumenter

[!include [banner](../includes/banner.md)]

Styring af forretningsdokumenter gør det muligt for erhvervsbrugere at redigere forretningsdokumentskabeloner ved at bruge en Microsoft Office 365-tjeneste eller det relevante Microsoft Office-skrivebordsprogram. Redigeringer kan omfatte designændringer eller nye installationer, eller brugerne kan tilføje pladsholdere for at medtage yderligere data uden at skulle ændre kildekoden. Du kan finde flere oplysninger om, hvordan du arbejder med Styring af forretningsdokumenter, i [Oversigt over styring af forretningsdokumenter](er-business-document-management.md).

Den nye brugergrænseflade er klarere og mere praktisk at bruge. Området **Forretningsdokument** viser kun de skabeloner, der ejes af den aktuelle [aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md) [udbyder](general-electronic-reporting.md#Provider) og findes i den aktuelle forekomst af Dynamics 365 Finance. På den tidligere brugergrænseflade har fanen **Skabelon** vist alle de skabeloner, der var tilgængelige for enhver udbyder. Den viste også alle de skabeloner, der blev oprettet og redigeret af enhver bruger, der havde samme rolle.

Du kan bruge knappen **Nyt dokument** i arbejdsområdet **Forretningsdokumentstyring** til at oprette og redigere en skabelon i et [Elektronisk rapporteringsformats (ER)](general-electronic-reporting.md) [konfiguration](general-electronic-reporting.md#Configuration), der leveres af en anden udbyder og findes i den aktuelle finansforekomst, eller til at overføre en ny skabelon fra en Excel-projektmappe. Derudover kan du i version 10.0.25 og senere bruge knappen **Nyt dokument** til at oprette og redigere en skabelon i en ER-formatkonfiguration, der er gemt i det [Globale lager](general-electronic-reporting.md#Repository).

I eksemplerne i denne artikel er den aktive udbyder Contoso, og du kan bruge den til at oprette en skabelon, der er baseret på en skabelon, der leveres af Microsoft. Du kan også oprette en skabelon ved at overføre din egen skabelon i Excel-format.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

Videoen [Oprette et nyt forretningsdokument ved hjælp af Styring af forretningsdokumenter](https://youtu.be/gAIYl-mM_pw) (vist ovenfor) er medtaget i afspilningslisten [finans og drift](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Gøre den nye brugergrænseflade i dokumenter i Styring af forretningsdokumenter tilgængeligt

Hvis du vil begynde at bruge den nye brugergrænseflade i dokumenter i Styring af forretningsdokumenter, skal du aktivere funktionen **Office-lignende brugergrænsefladeoplevelse for Styring af forretningsdokumenter** i arbejdsområdet **Administration af funktioner**.

Udfør følgende trin for at aktivere denne funktion for alle juridiske enheder.

1. I arbejdsområdet **Funktionsstyring** under fanen **Alle** skal du vælge funktionen **Office-lignende brugergrænsefladeoplevelse for Styring af forretningsdokumenter** på listen.
2. Vælg **Aktivér nu** for at aktivere den valgte funktion.
3. Opdater siden for at få adgang til den nye funktion.

## <a name="add-or-activate-a-provider"></a>Tilføje eller aktivere en udbyder

Hver skabelon i et forretningsdokument gemmes i en ER-formatkonfiguration, der er markeret som ejet af en bestemt konfigurationsudbyder. Når du opretter en ny skabelon, oprettes der en ny ER-formatkonfiguration, som indeholder den. Derfor skal der identificeres en udbyder til denne konfiguration. Den aktive udbyder af ER-strukturen bruges til dette formål. Hvis der ikke findes en udbyder i ER, kan du oprette en. Hvis der ikke findes en *aktiv* udbyder, kan du aktivere en af de eksisterende udbydere. Der åbnes en dialogboks til tilføjelse eller aktivering af en udbyder, når det er nødvendigt, mens du begynder at tilføje en ny skabelon.

### <a name="add-a-new-provider"></a>Tilføj en ny udbyder

Hvis du vil oprette en ny udbyder, skal du følge disse trin i dialogboksen **Konfigurationsudbyder**:

1.  Angiv navnet på den nye udbyder i feltet **Navn** under fanen **Vælg konfigurationsudbyder**.
2.  Angiv udbyderens URL-adresse i feltet **Internetadresse**. 
3.  Vælg **OK**.

    ![Oprettelse af en ny udbyder i Styring af forretningsdokumenter.](./media/bdm_create_provider.png)

Den tilføjede udbyder aktiveres automatisk.

### <a name="activate-a-provider"></a>Aktivere en udbyder

Du kan aktivere en udbyder ved at følge disse trin i dialogboksen **Konfigurationsudbyder**:

1.  Vælg udbyderen i feltet **Konfigurationsudbyder** under fanen **Vælg konfigurationsudbyder**.
2.  Vælg **OK**.

    ![Aktivering af en udbyder i Styring af forretningsdokumenter.](./media/bdm_choose_provider.png)

Den valgte udbyder aktiveres automatisk.

> [!NOTE]
> De enkelte skabeloner til forretningsdokumentstyring findes i en ER-formatkonfiguration, der refererer til udbyderen som konfigurations forfatter. Derfor kræves der en aktiv udbyder for hver skabelon.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Redigere en skabelon, der ejes af en anden udbyder

Dette eksempel viser, hvordan du kan bruge knappen **Nyt dokument** i arbejdsområdet **Forretningsdokumentstyring** til at oprette og redigere en skabelon i et Elektronisk rapporteringsformats konfiguration, der leveres af en anden udbyder og findes i den aktuelle finansforekomst. I dette eksempel er den aktive udbyder Contoso, der bruger den ER-formatkonfiguration, der leveres af Microsoft. Når du har valgt **Nyt dokument**, vises alle skabelonerne i den aktuelle finansforekomst, der ejes af den aktuelle udbyder og andre udbydere, under fanen **Vælg** på siden **Opret en ny skabelon**. Vælg en skabelon for at åbne den. Derefter kan du oprette en ny kopi af skabelonen, der kan redigeres. Den redigerede skabelon gemmes i en ny ER-formatkonfiguration, der genereres automatisk.

1. I arbejdsområdet **Styring af forretningsdokumenter** skal du vælge **Nyt dokument**.

    ![Arbejdsområdet til Styring af forretningsdokumenter.](./media/BDM_overview_new_template1.png)

2. På siden **Opret en ny skabelon** skal du vælge det dokument, der skal bruges som skabelon, under fanen **Vælg** og derefter vælge **Opret dokument**.

    ![Dialogboksen Forretningsdokumenter.](./media/BDM_overview_new_template2.png)

3. I den nye dialogboks skal du i feltet **Titel** ændre titlen efter behov. Titelteksten bruges til at navngive den nye ER-formatkonfiguration, der oprettes automatisk. Kladdeversionen af denne konfiguration (**FTI-debitorrapport (GER) Kopi**) vil indeholde den redigerede skabelon og vil blive brugt til at køre dette ER-format for den aktuelle bruger. Den oprindelige skabelon fra ER-basisformatkonfigurationen vil blive brugt til at køre dette ER-format for enhver anden bruger.
4. I feltet **Navn** skal du ændre navnet på den første revision af den redigerbare skabelon, der oprettes automatisk.
5. I feltet **Kommentar** skal du opdatere bemærkningerne til revisionen af den redigerbare skabelon, der oprettes automatisk.
6. Vælg **OK** for at bekræfte starten af redigeringsprocessen.

    ![Dialogboksen Dokumentoprettelse.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Uploade en skabelon, der bruger en eksisterende Excel-projektmappe

Dette eksempel viser, hvordan du kan bruge knappen **Nyt dokument** i arbejdsområdet **Forretningsdokumentstyring** til at oprette og redigere en skabelon i en ER-formatkonfiguration baseret på den tilgængelige Excel-projektmappe. I dette eksempel er den aktive udbyder Contoso, og du bruger de konfigurationer af [ER-datamodel](er-overview-components.md#data-model-component) og [ER-modeltilknytning](er-overview-components.md#model-mapping-component), der leveres af Microsoft. Når du har valgt **Nyt dokument**, skal du vælge fanen **Upload** på siden **Opret en ny skabelon**. Her kan du angive detaljerne om upload af en Excel-projektmappe. Når du har uploadet Excel-projektmappen, er den konverteret til en forretningsdokumentskabelon, der åbnes til redigering. Den redigerede skabelon gemmes i en ny ER-formatkonfiguration, der genereres automatisk.

Følg disse trin for at angive påkrævede oplysninger, før du uploader en skabelon.

1. I arbejdsområdet **Styring af forretningsdokumenter** skal du vælge **Nyt dokument**.
2. På siden **Opret en ny skabelon** under fanen **Upload** under fanen **Skabelon** skal du vælge **Gennemse** for at finde og vælge den Excel-fil, du vil bruge som skabelon. I afsnittet **Skabelon** udfyldes felterne **Titel** og **Beskrivelse** automatisk. De angiver navnet på og beskrivelsen af den nye ER-formatkonfiguration, der oprettes automatisk. Hvis det er nødvendigt, kan du redigere felterne.
3. Angiv typen af forretningsdokument i feltet **Navn** i sektionen **Dokumenttype**. Denne værdi bruges til at søge i den korrekte datakilde (det vil sige konfigurationen af ER-modellen).

    ![Fanen Skabelon under fanen Upload på siden Opret en ny skabelon.](./media/BDM_overview_new_UI_import_21.jpg)

4. Vælg **Anvend filter** i oversigtspanelet **Filter** under fanen **Datakilde**. I sektionen **Datakilde** udfyldes feltet **Navn** automatisk, eller du kan vælge en værdi manuelt. Du kan bruge filteret til at søge efter det relevante datakildenavn ved hjælp af navn, beskrivelse, lande-/områdekode og forretningsdokumenttype.

    ![Fanen Datakilde under fanen Upload på siden Opret en ny skabelon.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > Oversigtspanelet **Filter** bruges til at søge i den korrekte datakilde (det vil sige konfigurationen af ER-modellen). Du kan redigere alle filterfelter for at finde den datakilde, der passer bedst til det dokument, du uploader.
    > 
    > Betingelserne i oversigtspanelet **Filter** bruges som **ELLER**-betingelser.

5. Vælg **Registrer automatisk** under fanen **Tilknytning**. Feltet **Roddefinition** udfyldes automatisk, eller du kan vælge en værdi manuelt. Denne fane viser sluttilknytningen for elementerne fra skabelonen og modellen.

    ![Fanen Tilknytning under fanen Upload på siden Opret en ny skabelon.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > Tilknytningen i sektionen **Skabelonstruktur** bruger det fulde match af navne eller beskrivelser i datakilden på brugerens sprog og i cellenavnet i skabelonen.

6. Vælg **Opret dokument** for at bekræfte, at du vil oprette en skabelon og starte redigeringsprocessen.

Yderligere oplysninger finder du i [Oversigt over styring af forretningsdokumenter](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Uploade en skabelon fra det globale lager

Dette eksempel viser, hvordan du kan bruge knappen **Nyt dokument** i arbejdsområdet **Forretningsdokumentstyring** til at oprette og redigere en skabelon i en ER-formatkonfiguration, der leveres af Microsoft og placeres i det globale lager. I dette eksempel er den aktive udbyder Contoso, der bruger den ER-formatkonfiguration, der leveres af Microsoft. Når du har valgt **Nyt dokument**, viser fanen **Import fra globalt lager** på siden **Opret en ny skabelon** alle de forretningsdokumentskabeloner, der er gemt i det globale lager, men mangler i den aktuelle finansforekomst. Når du har valgt en skabelon, importeres den fra det globale lager til den aktuelle finansforekomst for at oprette en ny redigerbar kopi. Den redigerede skabelon gemmes i en ny ER-formatkonfiguration, der genereres automatisk.

1. I arbejdsområdet **Styring af forretningsdokumenter** skal du vælge **Nyt dokument**.
2. På siden **Opret en ny skabelon** skal du vælge det dokument, der skal bruges som skabelon, under fanen **Import fra globalt lager** og derefter vælge **Opret dokument**.

    ![Fanen Import fra globalt lager på siden Opret en ny skabelon.](./media/BDM_overview_new_template22.png)

3. Vælg **Ja** i meddelelsesfeltet for at bekræfte, at du vil importere det valgte dokument fra det globale lager til den aktuelle finansforekomst. Hvis du bliver spurgt om godkendelse, skal du følge vejledningen på skærmen.
4. I den nye dialogboks skal du i feltet **Titel** ændre titlen efter behov. Titelteksten bruges til at navngive den nye ER-formatkonfiguration, der oprettes automatisk. Kladdeversionen af denne konfiguration (**Rykkernota (Excel) Kopi**) vil indeholde den redigerede skabelon og vil blive brugt til at køre dette ER-format for den aktuelle bruger. Den oprindelige skabelon fra ER-basisformatkonfigurationen vil blive brugt til at køre dette ER-format for enhver anden bruger.
5. I feltet **Navn** skal du ændre navnet på den første revision af den redigerbare skabelon, der oprettes automatisk.
6. I feltet **Kommentar** skal du opdatere bemærkningerne til revisionen af den redigerbare skabelon, der oprettes automatisk.
7. Vælg **OK** for at bekræfte starten af redigeringsprocessen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

