---
title: Overføre en konfiguration til Lifecycle Services
description: I dette emne beskrives det, hvordan du opretter en ny konfiguration af elektronisk rapportering (ER) og uploader den til Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92fc6d7a8b2508c9a1f7b56ca8115adbd6ae00ea
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092535"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>Overføre en konfiguration til Lifecycle Services

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan en bruger i rollen som Systemadministrator eller Udvikler af elektronisk rapportering kan oprette en ny [Elektronisk rapporteringskonfiguration (ER)](../general-electronic-reporting.md#Configuration) og uploade den til [aktivbiblioteket på projektniveau](../../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).

I dette eksempel skal du oprette en konfiguration og uploade den til LCS for eksempelfirmaet med navnet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationer deles af alle firmaer. For at fuldføre disse trin skal du først fuldføre trinnene under [Oprette konfigurationsudbydere og markere dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). Der kræves også adgang til LCS.

1. Log på programmet ved hjælp af en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Systemadministrator

2. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
3. Vælg **Litware, Inc.**, og angiv **Aktiv**.
4. Vælg **Konfigurationer**.

<a name="accessconditions"></a>
> [!NOTE]
> Sørg for, at den aktuelle Dynamics 365 Finance-bruger er medlem af det LCS projekt, der indeholder det [aktivbibliotek](../../lifecycle-services/asset-library.md#asset-library-support), som bruges til at importere ER-konfigurationer.
>
> Du kan ikke få adgang til et LCS-projekt fra et ER-lager, der repræsenterer et andet domæne end det domæne, der bruges i Finans. Hvis du forsøger, vises der en tom liste over LCS-projekter, og du kan ikke importere ER-konfigurationer fra aktivbiblioteket på projektniveau i LCS. Hvis du vil have adgang til aktivbiblioteker på projektniveau fra et ER-lager, der bruges til at importere ER-konfigurationer, skal du logge på Finans ved hjælp af legitimationsoplysningerne for en bruger, der tilhører den lejer (domæne), som den aktuelle Finans-forekomst er klargjort til.

## <a name="create-a-new-data-model-configuration"></a>Opret en ny datamodelkonfiguration

1. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
2. Vælg **Opret konfiguration** på siden **Konfigurationer** for at åbne dialogboksen med rullemenu.

    I dette eksempel skal du oprette en konfiguration, der indeholder en eksempeldatamodel for elektroniske dokumenter. Denne datakonfigurationsmodel overføres senere til LCS.

3. Skriv **Eksempelmodelkonfiguration** i feltet **Navn**.
4. Skriv **Eksempelmodelkonfiguration** i feltet **Beskrivelse**.
5. Vælg **Opret konfiguration**.
6. Vælg **Modeldesigner**.
7. Vælg **Ny**.
8. I feltet **Navn** skal du angive **Indgangspunkt**.
9. Vælg **Tilføj**.
10. Vælg **Gem**.
11. Luk siden.
12. Vælg **Skift status**.
13. Vælg **Fuldfør**.
14. Vælg **OK**.
15. Luk siden.

## <a name="register-a-new-repository"></a>Registrere et nyt lager

1. Gå til **Virksomhedsadministration \> Arbejdsområder \> Elektronisk rapportering**.

2. I sektionen **Konfigurationsudbydere** skal du vælge feltet **Litware, Inc.**.

3. I feltet **Litware, Inc.** skal du vælge **Lagre**.

    Nu kan du åbne listen over lagre for konfigurationsudbyderen Litware, Inc.

4. Vælg **Tilføj** for at åbne dialogboksen med rullemenu.

    Nu kan du tilføje et nyt lager.

5. Vælg **LCS** i feltet **Konfigurationslagertype**.
6. Vælg **Opret lager**.
7. Indtast eller vælg en værdi i feltet **Projekt**.

    Vælg det ønskede LCS-projekt til dette eksempel. Du skal have [adgang](#accessconditions) til projektet.

8. Vælg **OK**.

    Udfyld en ny lagerpost.

9. Markér den valgte række på listen.

    I dette eksempel skal du vælge **LCS**-lagerposten.

    Bemærk, at et registreret lager er markeret af den aktuelle udbyder. Det vil sige, at det kun er de konfigurationer, der ejes af den pågældende udbyder, der kan placeres i lageret og derfor overføres til det valgte LCS-projekt.

10. Vælg **Åbn**.

    Åbn lageret for at få vist listen over ER-konfigurationer. Den vil være tom, hvis projektet endnu ikke er blevet brugt til deling af ER-konfigurationer.

11. Luk siden.
12. Luk siden.

## <a name="upload-a-configuration-into-lcs"></a>Uploade en konfiguration til LCS

1. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet vælge **Eksempemodellkonfiguration**.

    Du skal vælge en oprettet konfiguration, der allerede er fuldført.

3. Find og vælg den ønskede post på listen.

    I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Fuldført**.

4. Vælg **Skift status**.
5. Vælg **Del**.

    Status for konfigurationen ændres fra **Fuldført** til **Delt**, når konfigurationen er udgivet i LCS.

6. Vælg **OK**.
7. Find og vælg den ønskede post på listen.

    I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Delt**.

    Bemærk, at statussen for den valgte version er ændret fra **Fuldført** til **Delt**.

8. Luk siden.
9. Vælg **Lagre**.

    Nu kan du åbne listen over lagre for konfigurationsudbyderen Litware, Inc.

10. Vælg **Åbn**.

    I dette eksempel skal du vælge **LCS**-lageret og åbne det.

    Bemærk, at den valgte konfiguration vises som et aktiv for det valgte LCS-projekt.

11. Åbn LCS ved at gå til <https://lcs.dynamics.com>.
12. Åbn et projekt, der er brugt tidligere til registrering af lager.
13. Åbn aktivbiblioteket for projektet.
14. Vælg **GER-konfiguration** som aktivtype.

    Den ER-konfiguration, du har uploadet, skal være vist på listen.

    Bemærk, at den uploadede LCS-konfiguration kan importeres til en anden forekomst, hvis udbyderne har adgang til dette LCS-projekt.
