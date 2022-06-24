---
title: Konfigurere avanceret import af bankafstemning ved hjælp af elektronisk rapportering
description: Denne artikel forklarer, hvordan du bruger elektronisk rapportering til at konfigurere importprocessen til avanceret bankafstemning.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 2ac8811a5c10490d90f782472d3c198474c7edc0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889114"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Konfigurere avanceret import af bankafstemning ved hjælp af elektronisk rapportering

[!include [banner](../includes/banner.md)]

Med den avancerede bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme dem med banktransaktioner i Microsoft Dynamics 365 Finance. I denne artikel beskrives, hvordan du konfigurerer importfunktionen for dine kontoudtog fra banken. Konfigurationen for import af bankkontoudtog varierer afhængigt af formatet på dit elektroniske bankkontoudtog. Microsoft Dynamics 365 Finance understøtter tre formater for bankkontoudtog: ISO20022, MT940 og BAI2. 

## <a name="set-up-the-electronic-reporting-configuration"></a>Konfigurere elektronisk rapportering

1. Gå til **Arbejdsområder \> Elektronisk rapportering**.
2. På feltet for **Microsoft**-konfigurationsudbyderen skal du vælg **Lagre**.
3. Vælg **Global**, og vælg derefter **Åbn**.
4. Hvis der skal oprettes en forbindelse til lageret, skal du vælge det blå link i dialogboksen.
5. Find **Bankkontoudtogsmodel \> Bankkontoudtogsmodel for BAI2** på konfigurationslisten.
6. Vælg formatet **BAI2**.
7. I oversigtspanelet **Versioner** skal du vælge den seneste version og derefter vælge **Importér**.

## <a name="set-up-the-bank-statement-format"></a>Konfigurere formatet af bankkontoudtog

1. Gå til **Kontant- og bankstyring \> Konfiguration \> Konfiguration af avanceret bankafstemning \> Bankkontoudtogsformat**.
2. Vælg **Ny**.
3. Angiv felterne **Kontoudtogsformat** og **Navn**.
4. Markér afkrydsningsfeltet **Generisk elektronisk importformat**.
5. Angiv feltet **Konfiguration af importformat** til **BAI2**.

## <a name="set-up-the-bank-account"></a>Konfigurere bankkontoen

1. Gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**.
2. Åbn bankkontoen.
3. I oversigtspanelet **Afstemning** skal du vælge indstillingen **Ja** for **Avanceret bankafstemning**.
4. Indstil feltet **Kontoudtogsformat** til det **BAI2**-format, du oprettede tidligere.

## <a name="import-the-bank-statement"></a>Importere bankkontoudtoget

1. Gå til **Kontant- og bankstyring \> Afstemning af bankkontoudtog \> Bankkontoudtog**.
2. Vælg **Importér kontoudtog** øverst på siden **Bankkontoudtog**.
3. Indstil feltet **Bankkonto** til bankkontoen i kontoudtoget.
4. Indstil feltet **Kontoudtogsformat** til det **BAI2**-format, du oprettede tidligere.
5. Vælg **Gennemse**, og vælg **BAI**-filen.
6. Vælg **Overfør**.
7. Vælg **OK** for at importere den valgte fil.


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Eksempler på bankkontoudtogsformater og tekniske layout
Nedenfor vises eksempler på avancerede definitioner af teknisk layout for bankafstemnings importfil og tre relaterede eksempelfiler på bankkontoudtog: [Import af fileksempler](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Teknisk layoutdefinition                             | Eksempelfil med bankkontoudtog          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

