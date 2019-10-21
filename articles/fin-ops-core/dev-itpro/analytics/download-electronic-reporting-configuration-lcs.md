---
title: Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services
description: I dette emne beskrives det, hvordan du henter konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 561187343073a84b152151abe8770e89196eaa56
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174115"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan du henter konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).

Dette selvstudium fører dig gennem processen med at hente den nyeste version af konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).

1. Log på programmet ved hjælp af en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

2. Gå til **Virksomhedsadministration** &gt; **Elektronisk rapportering**.
3. I sektionen **Konfigurationsudbydere** skal du vælge feltet **Microsoft**.
4. I feltet **Microsoft** skal du klikke på **Lagre**.

    [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. På siden **Konfigurationslagre** i gitteret, skal du vælge det eksisterende lager for **LCS**-typen. Hvis lageret ikke vises i gitteret, skal du følge disse trin:

    1. Klik på **Tilføj** for at tilføje et nyt lager.
    2. Vælg **LCS** som lagertype.
    3. Klik på **Opret lager**.
    4. Hvis du bliver spurgt, skal du følge godkendelsesinstruktionerne.
    5. Angiv et navn og en beskrivelse til lageret.
    6. Klik på **OK** at bekræfte den nye lagerpost.
    7. I gitteret skal du vælge det nye lager for **LCS**-typen.

6. Klik på **Åbn** for at få vist listen over ER-konfigurationer for det valgte lager.

    [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

7. I konfigurationstræet i venstre rude skal du vælge de ER-konfigurationer, du har brug for.
8. I oversigtspanelet **Versioner** skal vælge den krævede version af den valgte ER-konfiguration.
9. Klik på **Importer** til at hente den valgte version fra LCS til den aktuelle forekomst.

    > [!NOTE]
    > Knappen **Importer** er ikke tilgængelig for ER-konfigurationsversioner, der allerede findes på den aktuelle forekomst.

    [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Konfigurationer valideres, efter de er importeret, afhængigt af ER-indstillingerne. Du kan blive underrettet om eventuelle uoverensstemmelsesproblemer, der er opdaget. Du skal løse disse problemer, før du kan bruge den importerede konfigurationsversion. Se listen over relaterede artikler i dette emne for at få flere oplysninger.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)
