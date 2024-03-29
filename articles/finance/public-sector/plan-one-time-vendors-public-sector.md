---
title: Planlægning af engangsleverandører i den offentlige sektor
description: Denne artikel beskriver, hvordan organisationer i den offentlige sektor kan forberede import og oprettelse af flere engangskreditorer og fakturaer.
author: v-kiarnd
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: v-kiarnd
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27251
ms.assetid: 936570cb-932f-4027-b3c7-2235ad79bc1c
ms.search.industry: Public sector
ms.search.form: LedgerTransVoucher, SysConfiguration, Tax1099Summary, VendTableListPage
ms.openlocfilehash: 72b22521e73e4c068ba27550ef73ea70bf3c8ec8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277132"
---
# <a name="plan-for-one-time-vendors-in-the-public-sector"></a>Planlægning af engangsleverandører i den offentlige sektor

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du forbereder import og oprettelse af flere engangskreditorer og fakturaer. 

Hvis du planlægger at masseimportere leverandør- og importoplysninger, skal du typisk først oprette en datafil i regnearksformat og gemme den i CSV-format (kommaseparerede værdier).

-   Da der bruges komma til at adskille felterne i en CSV-fil, må du ikke bruge kommaer i teksten i en post. Hvis du f.eks. vil angive firmanavnet "Smith, Jensen og Jensen", skal du indtaste det som **Smith Jensen og Jensen**.
-   Hvis du ikke angiver værdier for felter på denne side, bruger de nyoprettede kreditorkonti værdier fra den engangskreditorprofil, der er henvist til på siden **Kreditorparametre**. Hvis betalingsmetoden f.eks. er angivet til **Bankcheck** for engangskreditorprofilen på siden **Kreditorparametre**, så angives denne betalingsmetode også for de engangskreditorer, som du tilføjer.
-   Kreditornummerserien **Engangsleverandør** bruges til at tildele engangskreditorkontiene og må ikke være angivet til **Fortløbende** for denne tjeneste. Fakturaer genereres i kladdetilstand. Før du opretter betalingsforslag til betaling, skal du bogføre fakturaerne.

Følgende tabel viser de felter, som den importerede fil skal indeholde. Hver enkelt feltetiket svarer til en kolonneoverskrift i et regneark, og hver række i regnearket indeholder dataene for hver relevant kolonne.

**Kreditorsektion**

| Felt                                          | Oplysninger                                                 |
|------------------------------------------------|---------------------------------------------------------|
|Posttype                                     | **Person** eller **Organisation**                          |
| Fornavn                                     | (Hvis posttypeværdien er **Person**)                |
| Mellemnavn (valgfrit).                         | (Hvis posttypen er **Person**)                      |
| Efternavn                                      | (Hvis posttypen er **Person**)                      |
| Navn på kreditor                                    | (Hvis posttypen er **Organisation**)                |
| Gruppe                                          | Grænse på 10 tegn                                     |
| Land/område                                 | Grænse på 10 tegn                                     |
| Postnummer                                |                                                         |
| Gade                                         |                                                         |
| By                                           |                                                         |
| By                                           |                                                         |
|Federal Tax ID (valgfrit)                       | (Kun USA) 1099-nummer                                 |
| 1099-nummertype                                    | (Kun USA) Værdierne kan være **Ukendt**, **Employer Identification Number (EIN - US)**, **Social Security Number (SSN - US)**, **Individuelt Taxpayer Identification Number (TIN - US)**, eller **Anvendt Taxpayer Identification Number (TIN - US)**.  **Bemærk:** Hvis der ikke er angivet noget Federal Tax ID, indstilles feltet til **ukendt**.                                               |
| Bankkonto (valgfrit)                        | Bankkontonavn                                       |
| Bankkontonummer                            |                                                         |
| Registreringsnummer (valgfrit)                      |                                                         |
| SWIFT-kode (valgfrit)                          | Også kaldet BIC-kode (Bank Identifier Code).                |
|IBAN (valgfrit)                                 | IBAN (International Bank Account Number). Maks. 34 tegn   |



**Fakturasektion**

| Felt                                                | Oplysninger                                           |
|------------------------------------------------------|---------------------------------------------------|
| Fakturanummer                                       | Fakturanummer. Maks. 20 tegn                |
| Fakturabeskrivelse (valgfrit)                       |                                                   |
| Bogføringsdato (valgfrit)                              | Datoformat                                       |
| Fakturadato                                         | Datoformat                                       |
| Forfaldsdato (valgfrit)                                  | Datoformat                                       |
| Linjenummer                                          |                                                   |
|Varenummer (valgfrit)                                | Grænse på 20 tegn   **Bemærk!** Hvis der ikke er angivet noget varenummer, skal du angive værdier i felterne **Indkøbskategori** og **Indkøbskategorihierarki**. Hvis ingen indkøbskategori og intet indkøbskategorihierarki er angivet, skal du angive en værdi i feltet **Varenummer**.                    |
| Varenavn (valgfrit)                                 |  Maks. 60 tegn                               |
| Indkøbskategorihierarki (valgfrit)            |    **Bemærk!** Hvis du angiver en værdi for dette felt, skal feltet **Indkøbskategori** også udfyldes.                                                                         |
| Indkøbskategori (valgfrit)                      | **Bemærk!** Hvis du angiver en værdi for dette felt, skal feltet **Indkøbskategorihierarki** også udfyldes.                                                                        |
| Antal (valgfrit)                                  |                                                   |
| Enhed (valgfrit)                                      | Grænse på 10 tegn                               |
|Linjenettobeløb                                       | Decimalværdier er tilladt.                       |
| Enhedspris (valgfrit)                                | Decimalværdier er tilladt.                       |


**Distributionssektion**

| Felt                                                | Oplysninger                                  |
|------------------------------------------------------|------------------------------------------|
| Tal                                               | Regnskabsfordelingslinjenummer      |
| Økonomiske dimensioner                                 | Hvis den importerede fil har økonomiske dimensioner, skal du medtage alle økonomiske dimensioner med den rette navngivning, ellers vises der en fejlmeddelelse, som angiver, at finansdimensionen er ugyldig. Derefter skal du rette de økonomiske dimensioner eller fjerne kolonnerne fra filen.                                         |
| Procent                                              | Decimalværdier er tilladt.              |




## <a name="what-do-i-do-next"></a>Hvad skal jeg gøre nu?
Når du har konfigureret de forudsætninger, skal du læse [Engangsleverandører i den offentlige sektor](one-time-vendors-public-sector.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Engangsleverandører i den offentlige sektor](one-time-vendors-public-sector.md)

[Oversigt over kreditor i den offentlige sektor](accounts-payable-public-sector.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
