---
title: Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services
description: I dette emne beskrives det, hvordan du henter konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 418586113c038c3227f0704495a561eac319bdc9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745081"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du henter den nyeste version af [Konfigurationer af elektronisk rapportering (ER)](general-electronic-reporting.md#Configuration) fra det [delte aktivbibliotek](../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).

1. Log på programmet ved hjælp af en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

2. Gå til **Organisationsadministration** &gt; **Arbejdsområder** &gt; **Elektronisk rapportering**.
3. I sektionen **Konfigurationsudbydere** skal du vælge feltet **Microsoft**.
4. I feltet **Microsoft** skal du vælge **Lagre**.

    [![Microsoft-felt på siden Lokaliseringskonfigurationer](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. På siden **Konfigurationslagre** i gitteret, skal du vælge det eksisterende lager for **LCS**-typen. Hvis lageret ikke vises i gitteret, skal du følge disse trin:

    1. Vælg **Tilføj** for at tilføje et lager.
    2. Vælg **LCS** som lagertype.
    3. Vælg **Opret lager**.
    4. Hvis du bliver spurgt om godkendelse, skal du følge vejledningen på skærmen.
    5. Angiv et navn og en beskrivelse til lageret.
    6. Vælg **OK** for at bekræfte den nye lagerpost.
    7. I gitteret skal du vælge det nye lager for **LCS**-typen.

6. Vælg **Åbn** for at få vist listen over ER-konfigurationer for det valgte lager.

    [![Siden Konfigurationslagre](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > Hvis du har problemer med at få adgang til LCS-lageret for at kunne hente konfigurationer fra det delte aktivbibliotek i LCS, kan du i stedet hente konfigurationer fra det [globale lager](er-download-configurations-global-repo.md).

7. I konfigurationstræet i venstre rude skal du vælge den ER-konfiguration, du har brug for.
8. I oversigtspanelet **Versioner** skal vælge den krævede version af den valgte ER-konfiguration.
9. Vælg **Importér** for at download den valgte version fra LCS til den aktuelle forekomst.

    > [!NOTE]
    > Knappen **Importer** er ikke tilgængelig for ER-konfigurationsversioner, der allerede findes på den aktuelle forekomst.

    [![Siden Konfigurationslager](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Konfigurationer valideres, efter de er importeret, afhængigt af ER-indstillingerne. Du kan blive underrettet om eventuelle uoverensstemmelsesproblemer, der er opdaget. Du skal løse disse problemer, før du kan bruge den importerede konfigurationsversion. Se listen over relaterede emner til dette emne for at få flere oplysninger.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Hente ER-konfigurationer fra det globale lager til Konfigurationstjenesten](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]