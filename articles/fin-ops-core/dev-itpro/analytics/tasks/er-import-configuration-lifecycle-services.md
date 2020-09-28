---
title: Importere en konfiguration fra Lifecycle Services
description: Dette emne beskriver, hvordan en bruger i rollen som Systemadministrator eller Udvikler af elektronisk rapportering kan importere en ny version af en elektronisk rapporteringskonfiguration (ER) fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59dbbf820f7a3de1e5fb31f781943320b8b1a60a
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810637"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Importere en konfiguration fra Lifecycle Services

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan en bruger i rollen som Systemadministrator eller Udvikler af elektronisk rapportering kan importere en ny version af en [Elektronisk rapporteringskonfiguration (ER)](../general-electronic-reporting.md#Configuration) fra [aktivbiblioteket på projektniveau](../../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).

I dette eksempel skal du vælge den ønskede version af ER-konfigurationen og importere den til eksempelfirmaet med navnet Litware, Inc. Denne fremgangsmåde kan fuldføres i alle virksomheder, fordi ER-konfigurationer deles af firmaer. For at fuldføre disse trin skal du først fuldføre trinnene i proceduren [Overføre en ER-konfiguration til Lifecycle Services](er-upload-configuration-into-lifecycle-services.md). Der kræves også adgang til LCS.

1. Log på programmet ved hjælp af en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Systemadministrator

2. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
3. Vælg **Konfigurationer**.

<a name="accessconditions"></a>
> [!NOTE]
> Sørg for, at den aktuelle Dynamics 365 Finance-bruger er medlem af det LCS projekt, der indeholder det aktivbibliotek, som brugeren vil [have adgang](../../lifecycle-services/asset-library.md#asset-library-support) til for at importere ER-konfigurationer.
>
> Du kan ikke få adgang til et LCS-projekt fra et ER-lager, der repræsenterer et andet domæne end det domæne, der bruges i Finance. Hvis du forsøger, vises der en tom liste over LCS-projekter, og du kan ikke importere ER-konfigurationer fra aktivbiblioteket på projektniveau i LCS. Hvis du vil have adgang til aktivbiblioteker på projektniveau fra et ER-lager, der bruges til at importere ER-konfigurationer, skal du logge på Finance ved hjælp af legitimationsoplysningerne for en bruger, der tilhører den lejer (domæne), som den aktuelle Finance-forekomst er klargjort til.

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>Slette en delt version af en datamodelkonfiguration

1. På siden **Konfigurationer** skal du i konfigurationstræet vælge **Eksempemodellkonfiguration**.

    Den første version af en eksempeldatamodelkonfiguration har du oprettet og udgivet til LCS, da du fuldførte proceduren [Overføre en ER-konfiguration til Lifecycle Services](er-upload-configuration-into-lifecycle-services.md). I denne procedure skal du slette den version af ER-konfigurationen. Derefter skal du importere denne version fra LCS senere i dette emne.

2. Find og vælg den ønskede post på listen.

    I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Delt**. Denne status angiver, at konfigurationen er blevet publiceret til LCS.

3. Vælg **Skift status**.
4. Vælg **Annuller**.

    Ved at skifte status for den valgte version fra **Delt** til **Annulleret** gøres versionen tilgængelig for sletning.

5. Vælg **OK**.
6. Find og vælg den ønskede post på listen.

    I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Annulleret**.

7. Vælg **Slet**.
8. Vælg **Ja**.

    Bemærk, at kun kladdeversion 2 af den valgte datamodelkonfiguration nu er tilgængelig.

9. Luk siden.

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a>Importere en delt version af en datamodelkonfiguration fra LCS

1. Gå til **Virksomhedsadministration \> Arbejdsområder \> Elektronisk rapportering**.

2. I sektionen **Konfigurationsudbydere** skal du vælge feltet **Litware, Inc.**.

3. I feltet **Litware, Inc.** skal du vælge **Lagre**.

    Nu kan du åbne listen over lagre for konfigurationsudbyderen Litware, Inc.

4. Vælg **Åbn**.

    I dette eksempel skal du vælge **LCS**-lageret og åbne det. Du skal have [adgang](#accessconditions) til det LCS-projekt og til det aktivbibliotek, som det valgte ER-lager har adgang til.

5. Markér den valgte række på listen.

    Vælg i dette eksempel den første version af **Eksempelmodelkonfiguration** på versionslisten.

6. Vælg **Importér**.
7. Vælg **Ja** for at bekræfte importen af den valgte version fra LCS.

    En informationsmeddelelse bekræfter, at den valgte version er blevet importeret.

8. Luk siden.
9. Luk siden.
10. Vælg **Konfigurationer**.
11. Vælg **Eksempelmodelkonfiguration** i træet.
12. Find og vælg den ønskede post på listen.

    I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Delt**.

    Bemærk, at den delte version 1 af den valgte datamodelkonfiguration nu også er tilgængelig.
