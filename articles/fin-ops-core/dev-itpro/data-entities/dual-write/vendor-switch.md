---
title: Skifte mellem kreditordesign
description: I dette emne beskrives det, hvordan du kan skifte integrationen af leverandørdata mellem Finans- og driftsapps og Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 80de21b5e46e4f274626fa311f16e81312a2f5ab
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062744"
---
# <a name="switch-between-vendor-designs"></a>Skifte mellem kreditordesign

[!include [banner](../../includes/banner.md)]





## <a name="vendor-data-flow"></a>Kreditordataflow 

Hvis du vælger at bruge tabellen **Konto** til at gemme kreditorer af typen **Organisation** og tabellen **Kontaktperson** til at gemme kreditorer af typen **Person**, skal du konfigurere følgende arbejdsgange. Ellers kræves denne konfiguration ikke.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Bruge det udvidede kreditordesign til kreditorer af typen Organisation

Løsnings pakken **Dynamics365FinanceExtended** indeholder følgende arbejdsgangsskabeloner. Du skal oprette en arbejdsgang for hver skabelon.

+ Opret kreditorer i tabellen Konti
+ Opret kreditorer i tabellen Kreditorer
+ Opdater kreditorer i tabellen Konti
+ Opdater kreditorer i tabellen Kreditorer

Følg disse trin for at oprette nye arbejdsgangsprocesser ved hjælp af arbejdsgangsprocesskabeloner:

1. Opret en arbejdsgangsproces for tabellen **Kreditor**, og vælg skabelonen **Opret kreditorer i tabellen Konti** for arbejdsgangsprocessen. Vælg derefter **OK**. Denne arbejdsgang håndterer leverandøroprettelsesscenariet for tabellen **Konto**.

    ![Oprette kreditorer i arbejdsgangprocessen for tabellen Konti.](media/create_process.png)

2. Opret en arbejdsgangsproces for tabellen **Kreditor**, og vælg skabelonen **Opdater kreditorer i tabellen Konti** for arbejdsgangsprocessen. Vælg derefter **OK**. Denne arbejdsgang håndterer opdateringsscenariet for leverandører for tabellen **Konto**.
3. Opret en arbejdsgangsproces for tabellen **Konto**, og vælg skabelonen **Opret kreditorer i tabellen Kreditorer** for arbejdsgangsprocessen.
4. Opret en arbejdsgangsproces for tabellen **Konto**, og vælg skabelonen **Opdater kreditorer i tabellen Kreditorer** for arbejdsgangsprocessen.
5. Du kan konfigurere arbejdsprocesser som enten realtids- eller baggrundsarbejdsgange, afhængigt af dine krav. Hvis du vil konfigurere en arbejdsgang som en baggrundsarbejdsgang, skal du vælge **Konverter til en baggrundsarbejdsgang**.

    ![Konvertere til en baggrundsarbejdsgangsknap.](media/background_workflow.png)

6. Aktiver de arbejdsgange, du har oprettet for tabellerne **Konto** og **Kreditor** for at påbegynde anvendelsen af tabellen **Konto** til lagring af oplysninger til kreditorer af typen **Organisation**.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Bruge det udvidede kreditordesign til kreditorer af typen Person

Løsnings pakken **Dynamics365FinanceExtended** indeholder følgende arbejdsgangsskabeloner. Du skal oprette en arbejdsgang for hver skabelon.

+ Opret kreditorer af typen Person i tabellen Kreditorer
+ Opret kreditorer af typen Person i tabellen Kontakter
+ Opdater kreditorer af typen Person i tabellen Kontakter
+ Opdater kreditorer af typen Person i tabellen Kreditorer

Følg disse trin for at oprette nye arbejdsgangsprocesser ved hjælp af arbejdsgangsprocesskabeloner:

1. Opret en ny arbejdsgangsproces for tabellen **Kreditor**, og vælg skabelonen **Opret kreditorer af typen Person i tabellen Kontaktpersoner** for arbejdsgangsprocessen. Vælg derefter **OK**. Denne arbejdsgang håndterer kreditoroprettelsesscenariet for tabellen **Kontaktperson**.
2. Opret en ny arbejdsgangsproces for tabellen **Kreditor**, og vælg skabelonen **Opdater kreditorer af typen Person i tabellen Kontaktpersoner** for arbejdsgangsprocessen. Vælg derefter **OK**. Denne arbejdsgang håndterer opdateringsscenariet for kreditorer for tabellen **Kontaktperson**.
3. Opret en ny arbejdsgangsproces for tabellen **Kontaktperson**, og vælg skabelonen **Opret kreditorer af typen Person i tabellen Kreditorer** for arbejdsgangsprocessen.
4. Opret en ny arbejdsgangsproces for tabellen **Kontaktperson**, og vælg skabelonen **Opdater kreditorer af typen Person i tabellen Kreditorer** for arbejdsgangsprocessen.
5. Du kan konfigurere arbejdsprocesser som enten realtids- eller baggrundsarbejdsgange, afhængigt af dine krav. Hvis du vil konfigurere en arbejdsgang som en baggrundsarbejdsgang, skal du vælge **Konverter til en baggrundsarbejdsgang**.
6. Aktiver de arbejdsgange, du har oprettet i tabellerne **Kontaktperson** og **Kreditor** for at påbegynde anvendelsen af tabellen **Kontaktperson** til lagring af oplysninger til kreditorer af typen **Person**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]