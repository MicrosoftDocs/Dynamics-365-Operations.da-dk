---
title: Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services
description: Dette emne forklarer, hvordan du henter elektronisk indberetning (ER) konfigurationer fra Microsoft Dynamics livscyklus Services (LCS).
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 9dca5dec846670da25926826f59d7bce0fa0dcea
ms.lasthandoff: 03/31/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services

Dette emne forklarer, hvordan du henter elektronisk indberetning (ER) konfigurationer fra Microsoft Dynamics livscyklus Services (LCS).

Dette selvstudium fører dig gennem processen med at hente den nyeste version af konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).

1.  Log på Dynamics 365 for Operations ved hjælp af en af følgende roller:
    -   Udvikler til elektronisk rapportering
    -   Funktionel konsulent i elektronisk rapportering
    -   Systemadministrator

2.  Gå til **virksomhedsadministration**&gt;**elektronisk indberetning**.
3.  I sektionen **Konfigurationsudbydere** skal du vælge feltet **Microsoft**.
4.  I feltet **Microsoft** skal du klikke på **Lagre**. [![Update-er-from-LCS-for-MS-Open-MS-repositories-List](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  På siden **Konfigurationslagre** i gitteret, skal du vælge det eksisterende lager for **LCS**-typen. Hvis lageret ikke vises i gitteret, skal du følge disse trin:
    1.  Klik på **Tilføj** for at tilføje et nyt lager.
    2.  Vælg **LCS** som lagertype.
    3.  Klik på **Opret lager**.
    4.  Angiv et navn og en beskrivelse til lageret.
    5.  Klik på **OK** at bekræfte den nye lagerpost.
    6.  I gitteret skal du vælge det nye lager for **LCS**-typen.

6.  Klik på **Åbn** for at få vist listen over ER-konfigurationer for det valgte lager. [![Update-er-from-LCS-for-MS-Make-LCS-Repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  I konfigurationstræet i venstre rude skal du vælge de ER-konfigurationer, du har brug for.
8.  I oversigtspanelet **Versioner** skal vælge den krævede version af den valgte ER-konfiguration.
9.  Klik på **Importér** for at hente den valgte version fra LCS til den aktuelle Dynamics 365 for Operations-forekomst. **Bemærk!** Knappen **Importér** er ikke tilgængelig for ER-konfigurationsversioner, der allerede findes i den aktuelle Dynamics 365 for Operations-forekomst. [![Update-er-from-LCS-for-MS-Download-Configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Bemærk!** Konfigurationer valideres, efter de er importeret, afhængigt af ER-indstillingerne. Du kan blive underrettet om eventuelle uoverensstemmelsesproblemer, der er opdaget. Du skal løse disse problemer, før du kan bruge den importerede konfigurationsversion. Se listen over relaterede artikler om dette emne for at få yderligere oplysninger.

<a name="see-also"></a>Se også
--------

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)


