---
title: Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services
description: I dette emne beskrives det, hvordan du henter konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: be77d76194e9d38589548113cc650599d5af4323
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services

[!include[banner](../includes/banner.md)]


I dette emne beskrives det, hvordan du henter konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).

Dette selvstudium fører dig gennem processen med at hente den nyeste version af konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).

1.  Log på Finance and Operations ved hjælp af en af følgende roller:
    -   Udvikler til elektronisk rapportering
    -   Funktionel konsulent i elektronisk rapportering
    -   Systemadministrator

2.  Gå til **Virksomhedsadministration** &gt; **Elektronisk rapportering**.
3.  I sektionen **Konfigurationsudbydere** skal du vælge feltet **Microsoft**.
4.  I feltet **Microsoft** skal du klikke på **Lagre**. [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  På siden **Konfigurationslagre** i gitteret, skal du vælge det eksisterende lager for **LCS**-typen. Hvis lageret ikke vises i gitteret, skal du følge disse trin:
    1.  Klik på **Tilføj** for at tilføje et nyt lager.
    2.  Vælg **LCS** som lagertype.
    3.  Klik på **Opret lager**.
    4. Hvis du bliver spurgt, skal du følge godkendelsesinstruktionerne.
    5.  Angiv et navn og en beskrivelse til lageret.
    6.  Klik på **OK** at bekræfte den nye lagerpost.
    7.  I gitteret skal du vælge det nye lager for **LCS**-typen.

6.  Klik på **Åbn** for at få vist listen over ER-konfigurationer for det valgte lager. [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  I konfigurationstræet i venstre rude skal du vælge de ER-konfigurationer, du har brug for.
8.  I oversigtspanelet **Versioner** skal vælge den krævede version af den valgte ER-konfiguration.
9.  Klik på **Importér** for at hente den valgte version fra LCS til den aktuelle Finance and Operations-forekomst. **Bemærk!** Knappen **Importér** er ikke tilgængelig for ER-konfigurationsversioner, der allerede findes i den aktuelle Finance and Operations-forekomst. [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Bemærk!** Konfigurationer valideres, efter de er importeret, afhængigt af ER-indstillingerne. Du kan blive underrettet om eventuelle uoverensstemmelsesproblemer, der er opdaget. Du skal løse disse problemer, før du kan bruge den importerede konfigurationsversion. Se listen over relaterede artikler i dette emne for at få flere oplysninger.

<a name="see-also"></a>Se også
--------

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)




