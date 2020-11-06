---
title: Skifte mellem kreditordesign
description: I dette emne beskrives det, hvordan du kan skifte integrationen af kreditordata mellem Finance and Operations-apps og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997546"
---
# <a name="switch-between-vendor-designs"></a>Skifte mellem kreditordesign

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a>Kreditordataflow 

Hvis du vælger at bruge enheden **Konto** til at gemme kreditorer af typen **Organisation** og enheden **Kontaktperson** til at gemme kreditorer af typen **Person** , skal du konfigurere følgende arbejdsgange. Ellers kræves denne konfiguration ikke.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Bruge det udvidede kreditordesign til kreditorer af typen Organisation

Løsnings pakken **Dynamics365FinanceExtended** indeholder følgende arbejdsgangsskabeloner. Du skal oprette en arbejdsgang for hver skabelon.

+ Opret kreditorer i enheden Konti
+ Opret kreditorer i enheden Kreditorer
+ Opdater kreditorer i enheden Konti
+ Opdater kreditorer i enheden Kreditorer

Følg disse trin for at oprette nye arbejdsgangsprocesser ved hjælp af arbejdsgangsprocesskabeloner:

1. Opret en ny arbejdsgangsproces for enheden **Kreditor** , og vælg skabelonen **Opret kreditorer i enheden Konti** for arbejdsgangsprocessen. Vælg derefter **OK**. Denne arbejdsgang håndterer leverandøroprettelsesscenariet for enheden **Konto**.

    ![Oprette kreditorer i arbejdsgangprocessen for enheden Konti](media/create_process.png)

2. Opret en ny arbejdsgangsproces for enheden **Kreditor** , og vælg skabelonen **Opdater kreditorer i enheden Konti** for arbejdsgangsprocessen. Vælg derefter **OK**. Denne arbejdsgang håndterer opdateringsscenariet for leverandører for enheden **Konto**.
3. Opret en ny arbejdsgangsproces for enheden **Konto** , og vælg skabelonen **Opret kreditorer i enheden Kreditorer** for arbejdsgangsprocessen.
4. Opret en ny arbejdsgangsproces for enheden **Konto** , og vælg skabelonen **Opdater kreditorer i enheden Kreditorer** for arbejdsgangsprocessen.
5. Du kan konfigurere arbejdsprocesser som enten realtids- eller baggrundsarbejdsgange, afhængigt af dine krav. Hvis du vil konfigurere en arbejdsgang som en baggrundsarbejdsgang, skal du vælge **Konverter til en baggrundsarbejdsgang**.

    ![Konvertere til en baggrundsarbejdsgangsknap](media/background_workflow.png)

6. Aktiver de arbejdsgange, du har oprettet for enhederne **Konto** og **Kreditor** for at påbegynde anvendelsen af enheden **Konto** til lagring af oplysninger til kreditorer af typen **Organisation**.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Bruge det udvidede kreditordesign til kreditorer af typen Person

Løsnings pakken **Dynamics365FinanceExtended** indeholder følgende arbejdsgangsskabeloner. Du skal oprette en arbejdsgang for hver skabelon.

+ Oprette kreditorer af typen Person i enheden Kreditorer
+ Oprette kreditorer af typen Person i enheden Kontaktpersoner
+ Opdatere kreditorer af typen Person i enheden Kontaktpersoner
+ Opdatere kreditorer af typen Person i enheden Kreditorer

Følg disse trin for at oprette nye arbejdsgangsprocesser ved hjælp af arbejdsgangsprocesskabeloner:

1. Opret en ny arbejdsgangsproces for enheden **Kreditor** , og vælg skabelonen **Opret kreditorer af typen Person i enheden Kontaktpersoner** for arbejdsgangsprocessen. Vælg derefter **OK**. Denne arbejdsgang håndterer kreditoroprettelsesscenariet for enheden **Kontaktperson**.
2. Opret en ny arbejdsgangsproces for enheden **Kreditor** , og vælg skabelonen **Opdater kreditorer af typen Person i enheden Kontaktpersoner** for arbejdsgangsprocessen. Vælg derefter **OK**. Denne arbejdsgang håndterer opdateringsscenariet for kreditorer for enheden **Kontaktperson**.
3. Opret en ny arbejdsgangsproces for enheden **Kontaktperson** , og vælg skabelonen **Opret kreditorer af typen Person i enheden Kreditorer** for arbejdsgangsprocessen.
4. Opret en ny arbejdsgangsproces for enheden **Kontaktperson** , og vælg skabelonen **Opdater kreditorer af typen Person i enheden Kreditorer** for arbejdsgangsprocessen.
5. Du kan konfigurere arbejdsprocesser som enten realtids- eller baggrundsarbejdsgange, afhængigt af dine krav. Hvis du vil konfigurere en arbejdsgang som en baggrundsarbejdsgang, skal du vælge **Konverter til en baggrundsarbejdsgang**.
6. Aktiver de arbejdsgange, du har oprettet i enhederne **Kontaktperson** og **Kreditor** for at påbegynde anvendelsen af enheden **Kontaktperson** til lagring af oplysninger til kreditorer af typen **Person**.
