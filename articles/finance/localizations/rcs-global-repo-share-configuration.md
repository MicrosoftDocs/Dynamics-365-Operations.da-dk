---
title: Dele ER-konfigurationer i RCS/det globale lager med eksterne organisationer
description: Denne artikel forklarer, hvordan du deler ER-konfigurationer (elektronisk rapportering) i Microsoft Regulatory Configuration Services (RCS)/det globale lager direkte med eksterne organisationer.
author: kfend
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
ms.openlocfilehash: d9400ffcede9924a01391a433b570651d3f0c5e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284809"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>Dele ER-konfiguration (Electronic reporting) i Regulatory Configuration Services (RCS)/det globale lager med eksterne organisationer.

[!include [banner](../includes/banner.md)]

Du kan bruge Microsoft RCS (Regulatory Configuration Services) til at dele ER-konfigurationer (Electronic reporting) og derefter udgive dem til eksterne organisationer.

I følgende procedurer forklares det, hvordan en RCS-bruger kan dele en version af en ER-konfiguration, der er konfigureret i en RCS-forekomst, med en ekstern organisation. Før du kan fuldføre disse procedurer, skal du fuldføre følgende forudsætninger:

- Gå til en forekomst.
- Oprette en aktiv konfigurationsudbyder. Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
- Oprette og uploade en ny version af en ER-konfiguration. Få flere oplysninger i [Oprette og uploade en ny version af en ER-konfiguration (Electronic reporting)](rcs-global-repo-upload.md).

Du skal også sikre dig, at der er klargjort et RCS-miljø til dit firma.

1. I program til finans og drift skal du gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Hvis der ikke er klargjort noget RCS-miljø til dit firma, skal du vælge **Regulatory services – ekstern konfiguration** og derefter følge instruktionerne for at klargøre et.

Hvis der allerede er klargjort et RCS-miljø til dit firma, kan du bruge side-URL-adressen til at få adgang til det ved at vælge indstillingen til logon.

## <a name="verify-the-configuration-that-you-want-to-share"></a>Kontrollér den konfiguration, du vil dele

Udfør følgende trin for at kontrollere, at den konfiguration, du vil dele, allerede er uploadet til det globale lager.

1. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Lagre** for din konfigurationsudbyder.

    ![Konfigurationsudbydere.](media/1_RCS_Repo_for_config_provider.JPG)

2. Vælg **Globalt lager** \> **Åbn**.
3. Vælg den konfiguration, du vil dele. Du kan bruge filterfeltet til at indsnævre søgningen. Hvis du ikke kan finde konfigurationen i det globale lager, skal du følge trinnene i [Oprette og uploade en ny version af en ER-konfiguration (Electronic reporting)](rcs-global-repo-upload.md).

## <a name="share-er-configurations-with-external-organizations"></a>Dele ER-konfigurationer med eksterne organisationer

Når der er oprettet en konfiguration under din konfigurationsudbyder, kan du dele den direkte med eksterne organisationer ved hjælp af oversigtspanelet **Delt med** på siden **Globalt konfigurationslager**.

1. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Lagre** for din konfigurationsudbyder.
2. Vælg **Globalt lager** \> **Åbn**. 
3. Vælg den konfiguration, du vil dele.
4. Gå til oversigtspanelet **Delt med**, og vælg **Organisation**.

    ![Delt med oversigtspanel.](media/1_RCS_Repo_for_Share_with_org.JPG)

5. Angiv domænenavnet for den eksterne organisation i dialogboksen, og vælg derefter **OK**.

    ![Dialogboksen Del konfigurationsversion med ekstern organisation.](media/1_RCS_Repo_for_Share_with_form.JPG)

Konfigurationen deles med den eksterne organisation og er tilgængelig for den pågældende organisation i det globale lager. Derfra kan den importeres til organisationens forekomst af RCS eller til dens forekomster af programmer til finans og drift.

6. Hvis du vil annullere delingen af en konfiguration, der tidligere er delt med en ekstern organisation, skal du vælge konfigurationen og klikke på **Fjern deling** og derefter vælge **OK**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
