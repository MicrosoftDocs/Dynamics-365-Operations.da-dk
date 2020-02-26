---
title: Ny brugergrænseflade i dokumenter i styring af forretningsdokumenter
description: Dette emne indeholder oplysninger om, hvordan du kan bruge den nye brugergrænseflade i dokumenter i funktionen Styring af forretningsdokumenter i den elektroniske rapporteringsstruktur (ER).
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4acde9703c721ab7c20d1603299a10dda91b23c4
ms.sourcegitcommit: b8f8ccab2cd9d848e5ecd71caaf0a63237e2236b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2020
ms.locfileid: "2957057"
---
# <a name="new-document-user-interface-in-business-document-management"></a>Ny brugergrænseflade i dokumenter i styring af forretningsdokumenter

[!include [banner](../includes/banner.md)]

Styring af forretningsdokumenter gør det muligt for erhvervsbrugere at redigere forretningsdokumentskabeloner ved at bruge en Microsoft Office 365-tjeneste eller det relevante Microsoft Office-skrivebordsprogram. Redigeringer kan omfatte designændringer eller nye installationer, eller brugerne kan tilføje pladsholdere for at medtage yderligere data uden at skulle ændre kildekoden. Du kan finde flere oplysninger om, hvordan du arbejder med Styring af forretningsdokumenter, i [Oversigt over styring af forretningsdokumenter](er-business-document-management.md).

Den nye brugergrænseflade i dokumentet er klarere og mere praktisk at bruge. Området **Forretningsdokument** viser kun de skabeloner, der er tilgængelige for den aktuelle udbyder.

Knappen **Nyt dokument** giver brugerne mulighed for at oprette og redigere en skabelon i en formatkonfiguration for elektronisk rapportering (ER), der er leveret af en anden udbyder. I eksemplet i dette emne er udbyderen Microsoft.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Gøre den nye brugergrænseflade i dokumenter i Styring af forretningsdokumenter tilgængeligt

Hvis du vil begynde at bruge den nye brugergrænseflade i dokumenter i Styring af forretningsdokumenter, skal du aktivere funktionen **Office-lignende brugergrænsefladeoplevelse for Styring af forretningsdokumenter** i arbejdsområdet **Administration af funktioner**.

Udfør følgende trin for at aktivere denne funktion for alle juridiske enheder.

1. I arbejdsområdet **Funktionsstyring** under fanen **Ny** skal du vælge funktionen **Office-lignende brugergrænsefladeoplevelse for Styring af forretningsdokumenter** på listen.
2. Vælg **Aktivér nu** for at aktivere den valgte funktion.
3. Opdater siden for at få adgang til den nye funktion.

### <a name="edit-templates-that-are-owned-by-other-providers"></a>Rediger skabeloner, der ejes af andre udbydere

1. I arbejdsområdet **Styring af forretningsdokumenter** skal du vælge **Nyt dokument**.

    ![Arbejdsområdet til Styring af forretningsdokumenter](./media/BDM_overview_new_template1.png)

2. Vælg i dialogboksen det dokument, der skal bruges som skabelon, og vælg derefter **Opret dokument**.

    ![Dialogboksen Forretningsdokumenter](./media/BDM_overview_new_template2.png)

3. I den nye dialogboks skal du i feltet **Titel** ændre titlen efter behov. Titelteksten bruges til at navngive den nye ER-formatkonfiguration, der oprettes automatisk. Kladdeversionen af denne konfiguration (**FTI-debitorrapport (GER) Kopi**) vil indeholde den redigerede skabelon og vil blive brugt til at køre dette ER-format for den aktuelle bruger. Den oprindelige skabelon fra ER-basisformatkonfigurationen vil blive brugt til at køre dette ER-format for enhver anden bruger.
4. I feltet **Navn** skal du ændre navnet på den første revision af den redigerbare skabelon, der oprettes automatisk.
5. I feltet **Kommentar** skal du opdatere bemærkningerne til revisionen af den redigerbare skabelon, der oprettes automatisk.
6. Vælg **OK** for at bekræfte starten af redigeringsprocessen.

    ![Dialogboksen Dokumentoprettelse](./media/BDM_overview_new_template3.png)

Knappen **Nyt dokument** bruges til at oprette og redigere en skabelon i en ER-formatkonfiguration, der er leveret af en anden udbyder. I dette eksempel er udbyderen Microsoft. Når du vælger **Nyt dokument**, kan du se alle de skabeloner, der ejes af den aktuelle udbyder og andre udbydere. Når du har valgt skabelonen, vil den blive åbnet til redigering. Den redigerede skabelon gemmes derefter i en ny ER-formatkonfiguration, der genereres automatisk.

Yderligere oplysninger finder du i [Oversigt over styring af forretningsdokumenter](er-business-document-management.md).
