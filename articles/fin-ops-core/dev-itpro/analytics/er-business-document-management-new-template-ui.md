---
title: Microsoft Office-brugergrænsefladestil for nyt dokument i styring af forretningsdokumenter
description: Dette emne indeholder oplysninger om, hvordan du kan bruge den nye brugergrænseflade til dokumenter i funktionen Styring af forretningsdokumenter i den elektroniske rapportering (ER).
author: v-anamir
ms.date: 04/12/2021
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
ms.openlocfilehash: 4d4c256b2384f14fd8439c4a9263860f504113de369142d0913a2538f1f0939f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737945"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Microsoft Office-brugergrænsefladestil for nyt dokument i styring af forretningsdokumenter

[!include [banner](../includes/banner.md)]

Styring af forretningsdokumenter gør det muligt for erhvervsbrugere at redigere forretningsdokumentskabeloner ved at bruge en Microsoft 365-tjeneste eller det relevante Microsoft Office-skrivebordsprogram. Redigeringer kan omfatte designændringer eller nye installationer, eller brugerne kan tilføje pladsholdere for at medtage yderligere data uden at skulle ændre kildekoden. Du kan finde flere oplysninger om, hvordan du arbejder med Styring af forretningsdokumenter, i [Oversigt over styring af forretningsdokumenter](er-business-document-management.md).

Den nye brugergrænseflade er klarere og mere praktisk at bruge. Området **Forretningsdokument** viser kun de skabeloner, der er tilgængelige for den aktuelle udbyder. På den tidligere brugergrænseflade har fanen **Skabelon** vist alle de skabeloner, der var tilgængelige for alle leverandører. Den viste også alle de skabeloner, der blev oprettet og redigeret af enhver bruger, der havde samme rolle.

Knappen **Nyt dokument** giver dig mulighed for at oprette og redigere en skabelon i en formatkonfiguration for elektronisk rapportering (ER), der er leveret af en anden udbyder. I eksemplet i dette emne er udbyderen Microsoft. Du kan også oprette en skabelon ved at overføre din egen skabelon i Excel-format.


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

Videoen [Oprette et nyt forretningsdokument ved hjælp af Styring af forretningsdokumenter](https://youtu.be/gAIYl-mM_pw) (vist ovenfor) er medtaget i den [Finance and Operations-afspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Gøre den nye brugergrænseflade i dokumenter i Styring af forretningsdokumenter tilgængeligt

Hvis du vil begynde at bruge den nye brugergrænseflade i dokumenter i Styring af forretningsdokumenter, skal du aktivere funktionen **Office-lignende brugergrænsefladeoplevelse for Styring af forretningsdokumenter** i arbejdsområdet **Administration af funktioner**.

Udfør følgende trin for at aktivere denne funktion for alle juridiske enheder.

1. I arbejdsområdet **Funktionsstyring** under fanen **Alle** skal du vælge funktionen **Office-lignende brugergrænsefladeoplevelse for Styring af forretningsdokumenter** på listen.
2. Vælg **Aktivér nu** for at aktivere den valgte funktion.
3. Opdater siden for at få adgang til den nye funktion.

## <a name="edit-templates-that-are-owned-by-other-providers"></a>Redigere skabeloner, der ejes af andre udbydere

1. I arbejdsområdet **Styring af forretningsdokumenter** skal du vælge **Nyt dokument**.

    ![Arbejdsområdet til Styring af forretningsdokumenter.](./media/BDM_overview_new_template1.png)

2. Vælg det dokument, der skal bruges som skabelon, under fanen **Vælg**, og vælg derefter **Opret dokument**.

    ![Dialogboksen Forretningsdokumenter.](./media/BDM_overview_new_template2.png)

3. I den nye dialogboks skal du i feltet **Titel** ændre titlen efter behov. Titelteksten bruges til at navngive den nye ER-formatkonfiguration, der oprettes automatisk. Kladdeversionen af denne konfiguration (**FTI-debitorrapport (GER) Kopi**) vil indeholde den redigerede skabelon og vil blive brugt til at køre dette ER-format for den aktuelle bruger. Den oprindelige skabelon fra ER-basisformatkonfigurationen vil blive brugt til at køre dette ER-format for enhver anden bruger.
4. I feltet **Navn** skal du ændre navnet på den første revision af den redigerbare skabelon, der oprettes automatisk.
5. I feltet **Kommentar** skal du opdatere bemærkningerne til revisionen af den redigerbare skabelon, der oprettes automatisk.
6. Vælg **OK** for at bekræfte starten af redigeringsprocessen.

    ![Dialogboksen Dokumentoprettelse.](./media/BDM_overview_new_template3.png)

Knappen **Nyt dokument** bruges til at oprette og redigere en skabelon i en ER-formatkonfiguration, der er leveret af en anden udbyder. I dette eksempel er udbyderen Microsoft. Når du vælger **Nyt dokument**, kan du se alle de skabeloner, der ejes af den aktuelle udbyder og andre udbydere. Når du har valgt skabelonen, vil den blive åbnet til redigering. Den redigerede skabelon gemmes derefter i en ny ER-formatkonfiguration, der genereres automatisk.

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a>Uploade en skabelon, der bruger et eksisterende Excel-format
Følg disse trin for at angive påkrævede oplysninger, før du uploader en skabelon.

1. I arbejdsområdet **Styring af forretningsdokumenter** skal du vælge **Nyt dokument**.

    ![Arbejdsområdet til Styring af forretningsdokumenter.](./media/BDM_overview_new_template1.png)
    
2. På siden **Opret en ny skabelon** under fanen **Upload** under fanen **Skabelon** skal du vælge **Gennemse** for at finde og vælge den Excel-fil, du vil bruge som skabelon. I afsnittet **Skabelon** udfyldes felterne **Titel** og **Beskrivelse** automatisk. De angiver navnet på og beskrivelsen af den nye ER-formatkonfiguration, der oprettes automatisk. Hvis det er nødvendigt, kan du redigere felterne.
3. Angiv typen af forretningsdokument i feltet **Navn** i sektionen **Dokumenttype**. Denne værdi bruges til at søge i den korrekte datakilde (det vil sige konfigurationen af ER-modellen).

    ![Fanen Skabelon.](./media/BDM_overview_new_UI_import_21.jpg)

4. Vælg **Anvend filter** i oversigtspanelet **Filter** under fanen **Datakilde**. I sektionen **Datakilde** udfyldes feltet **Navn** automatisk, eller du kan vælge en værdi manuelt. Du kan bruge filteret til at søge efter det relevante datakildenavn ved hjælp af navn, beskrivelse, lande-/områdekode og forretningsdokumenttype.

    ![Fanen Datakilde.](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > Oversigtspanelet **Filter** bruges til at søge i den korrekte datakilde (det vil sige konfigurationen af ER-modellen). Du kan redigere alle filterfelter for at finde den datakilde, der passer bedst til det dokument, du uploader.
    > 
    > Betingelserne i oversigtspanelet **Filter** bruges som **ELLER**-betingelser.
    
5. Vælg **Registrer automatisk** under fanen **Tilknytning**. Feltet **Roddefinition** udfyldes automatisk, eller du kan vælge en værdi manuelt. Denne fane viser sluttilknytningen for elementerne fra skabelonen og modellen.

    ![Fanen Tilknytning.](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > Tilknytningen i sektionen **Skabelonstruktur** bruger det fulde match af navne eller beskrivelser i datakilden på brugerens sprog og i cellenavnet i skabelonen.

6. Vælg **Opret dokument** for at bekræfte, at du vil oprette en skabelon og starte redigeringsprocessen.

Yderligere oplysninger finder du i [Oversigt over styring af forretningsdokumenter](er-business-document-management.md).

Hvis der ikke er en udbyder i Elektronisk rapportering, kan du oprette en. Hvis der ikke findes en aktiv udbyder, kan du vælge at aktivere en.

- Hvis du vil oprette en udbyder, skal du ændre navnet på udbyderen i feltet **Navn**, opdatere den nye udbyders internetadresse i feltet **Internetadresse** og vælge **OK** for at bekræfte.

    ![Oprette en ny udbyder i BDM.](./media/bdm_create_provider.png)
    
- Hvis du vil aktivere en eksisterende udbyder, skal du vælge navnet på udbyderen i feltet **Konfigurationsudbyder** og vælge **OK** for at indstille udbyderen til aktiv.

    ![Aktivere udbyder i BDM.](./media/bdm_choose_provider.png)

> [!NOTE]
> Hver BDM-skabelon refererer til udbyderen som konfigurations forfatter. Derfor kræves der en aktiv udbyder for skabelonen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
