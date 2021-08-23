---
title: Hente ER-konfigurationer fra det globale lager til Konfigurationstjenesten
description: Dette emne forklarer, hvordan du kan hente ER-konfigurationer (elektronisk rapportering) fra det globale lager til Konfigurationstjenesten.
author: NickSelin
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 6923954e2d287a16425a9f823e8f8800503735ec0b3837cff764cf8d6e752039
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724411"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>Hente ER-konfigurationer fra det globale lager til Konfigurationstjenesten

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du kan hente [ER-konfigurationer (elektronisk rapportering)](general-electronic-reporting.md#Configuration) fra det globale lager til konfigurationstjenesten. Du kan finde flere oplysninger under [Microsoft Dynamics 365 for Finance and Operations – Regulatory Services, konfigurationstjeneste](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="open-configurations-repository"></a>Åbn konfigurationslageret

1. Log på programmet Dynamics 365 Finance ved hjælp af en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

2. Gå til **Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering**.
3. I sektionen **Konfigurationsudbydere** skal du vælge feltet **Microsoft**.
3. I feltet **Microsoft** skal du vælge **Lagre**.

    ![Arbejdsområde til elektronisk rapportering.](./media/er-download-configurations-global-repo-er-workspace.png)

4. På siden **Konfigurationslagre** i gitteret skal du vælge det eksisterende lager for **Global**-typen. Hvis lageret ikke vises i gitteret, skal du følge disse trin:

    1. Vælg **Tilføj** for at tilføje et nyt lager.
    2. Vælg **Global** som lagertype, og vælg derefter **Opret lager**.
    3. Hvis du bliver spurgt, skal du følge godkendelsesinstruktionerne.
    4. Angiv et navn til og en beskrivelse af lagringsstedet, og vælg derefter **OK** for at bekræfte den nye lagerpost.
    5. I gitteret skal du vælge det nye lager for **Global**-typen.

5. Vælg **Åbn** for at få vist listen over ER-konfigurationer for det valgte lager.

    ![Siden Konfigurationslagre.](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>Importere en enkelt konfiguration

1. På siden **Konfigurationslagre** skal du i konfigurationstræet vælge den ER-konfiguration, du vil bruge.
2. I oversigtspanelet **Versioner** skal vælge den krævede version af den valgte ER-konfiguration.
3. Vælg **Importér** for at hente den valgte version fra Global-lager til den aktuelle Finans-forekomst.

    > [!NOTE]
    > Knappen **Importer** er ikke tilgængelig for ER-konfigurationsversioner, der allerede findes i den aktuelle Finans-forekomst.

    ![Siden Konfigurationslager.](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>Importere filtrerede konfigurationer

1. På siden **Konfigurationslagre** skal du i konfigurationstræet udvide oversigtspanelet **Filter**.
2. I gitteret **Koder** skal du tilføje eventuelle koder, der skal bruges.
3. I feltet **Land/område** skal du vælge de relevante land/område-koder og derefter vælge **Anvend filter**.

    > [!NOTE]
    > Oversigtspanelet **Konfigurationer** viser alle de konfigurationer, der opfylder de angivne udvælgelsesbetingelser.

4. I oversigtspanelet **Konfigurationer** skal du vælge **Importér** for at hente de filtrerede konfigurationer fra det globale lager til den aktuelle forekomst.
5. I oversigtspanelet **Konfigurationer** skal du vælge **Nulstil filter** for at rydde op i de angivne udvælgelsesbetingelser.

    ![Siden Konfigurationslager.](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> Konfigurationer valideres, efter de er importeret, afhængigt af ER-indstillingerne. Du kan blive underrettet om eventuelle uoverensstemmelsesproblemer, der er opdaget. Før du kan bruge den importerede konfigurationsversion, skal du løse problemerne. Se listen over relaterede ressourcer i dette emne for at få flere oplysninger.

> [!NOTE]
> ER-konfigurationer kan konfigureres som værende afhængige af andre konfigurationer. Sammen med en valgt konfiguration kan andre konfigurationer derfor blive importeret automatisk. Yderligere oplysninger om konfigurationsafhængigheder finder du i [Definere afhængigheden for ER-konfigurationer af andre komponenter](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]