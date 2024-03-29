---
title: Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services
description: Denne artikel beskriver, hvordan du henter konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).
author: kfend
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.form: ERSolutionImport, ERWorkspace
ms.openlocfilehash: f48dd14bc3009550d78bd71db030c172d2ef6450
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277810"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du henter den nyeste version af [Konfigurationer af elektronisk rapportering (ER)](general-electronic-reporting.md#Configuration) fra det [delte aktivbibliotek](../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).

> [!IMPORTANT]
> Brugen af LCS som opbevaringslager for ER-konfigurationer [udfases](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Du kan finde flere oplysninger under [RCS (Regulatory Configuration Service) – Lifecycle Services (LCS)-lagerudfasning](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

1. Log på programmet ved hjælp af en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

2. Gå til **Organisationsadministration** &gt; **Arbejdsområder** &gt; **Elektronisk rapportering**.
3. I sektionen **Konfigurationsudbydere** skal du vælge feltet **Microsoft**.
4. I feltet **Microsoft** skal du vælge **Lagre**.

    [![Microsoft-felt på siden Lokaliseringskonfigurationer.](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. På siden **Konfigurationslagre** i gitteret, skal du vælge det eksisterende lager for **LCS**-typen. Hvis lageret ikke vises i gitteret, skal du følge disse trin:

    1. Vælg **Tilføj** for at tilføje et lager.
    2. Vælg **LCS** som lagertype.
    3. Vælg **Opret lager**.
    4. Hvis du bliver spurgt om godkendelse, skal du følge vejledningen på skærmen.
    5. Angiv et navn og en beskrivelse til lageret.
    6. Vælg **OK** for at bekræfte den nye lagerpost.
    7. I gitteret skal du vælge det nye lager for **LCS**-typen.

6. Vælg **Åbn** for at få vist listen over ER-konfigurationer for det valgte lager.

    [![Siden Konfigurationslagre.](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > Hvis du har problemer med at få adgang til LCS-lageret for at kunne hente konfigurationer fra det delte aktivbibliotek i LCS, kan du i stedet hente konfigurationer fra det [globale lager](er-download-configurations-global-repo.md).

7. I konfigurationstræet i venstre rude skal du vælge den ER-konfiguration, du har brug for.
8. I oversigtspanelet **Versioner** skal vælge den krævede version af den valgte ER-konfiguration.
9. Vælg **Importér** for at download den valgte version fra LCS til den aktuelle forekomst.

    > [!NOTE]
    > Knappen **Importer** er ikke tilgængelig for ER-konfigurationsversioner, der allerede findes på den aktuelle forekomst.

    [![Siden Konfigurationslager.](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Konfigurationer valideres, efter de er importeret, afhængigt af ER-indstillingerne. Du kan blive underrettet om eventuelle uoverensstemmelsesproblemer, der er opdaget. Du skal løse disse problemer, før du kan bruge den importerede konfigurationsversion. Se listen over relaterede emner til denne artikel.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Hente ER-konfigurationer fra det globale lager til Konfigurationstjenesten](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
