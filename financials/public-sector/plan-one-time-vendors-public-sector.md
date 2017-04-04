---
title: "Planen for engangsleverandører i den offentlige sektor"
description: Denne artikel beskriver, hvordan du forbereder at importere og oprette flere engangskreditorer og fakturaer.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27251
ms.assetid: 936570cb-932f-4027-b3c7-2235ad79bc1c
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a76abfa35e53673f9780d1a6f8816bd24f9f8e48
ms.openlocfilehash: ddf990bb29dde89c267b4aed169948d7a7925433
ms.lasthandoff: 03/31/2017


---

# <a name="plan-for-one-time-vendors-in-the-public-sector"></a>Planen for engangsleverandører i den offentlige sektor

Denne artikel beskriver, hvordan du forbereder at importere og oprette flere engangskreditorer og fakturaer. 

Hvis du planlægger at masseimportere leverandør- og importoplysninger, skal du typisk først oprette en datafil i regnearksformat og gemme den i CSV-format (kommaseparerede værdier).

-   Da der bruges komma til at adskille felterne i en CSV-fil, må du ikke bruge kommaer i teksten i en post. Hvis du f.eks. vil angive firmanavnet "Smith, Jensen og Jensen", skal du indtaste det som **Smith Jensen og Jensen**.
-   Hvis du ikke angiver værdier for felterne på denne side, de nyoprettede kreditorkonti bruge værdier fra profilen engangsleverandør, der refereres til i den **konti Kreditorparametre** side. For eksempel, hvis betalingsmåden er indstillet til **se** for enkeltstående leverandørprofilen på den **konti Kreditorparametre** side, at betalingsmetoden også angives for engangskreditorer, du tilføjer.
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
| 1099-nummertype                                    | (Kun USA) Værdier kan være **ukendt**, **Employer Identification Number**, **CPR-nummer**, **individuelle Taxpayer Identification Number**, eller **vedtaget betaler momsidentifikationsnummer**.  **Bemærk:** Hvis nogen federal tax ID er angivet, indstilles feltet **ukendt**.                                               |
| Bankkonto (valgfrit)                        | Bankkontonavn                                       |
| Bankkontonummer                            |                                                         |
| Registreringsnummer (valgfrit)                      |                                                         |
| SWIFT-kode (valgfrit)                          | Også kaldet BIC-kode (Bank Identifier Code).                |
|IBAN (valgfrit)                                 | IBAN (International Bank Account Number). Maks. 34 tegn   |



**Invoice section**

| Felt                                                | Oplysninger                                           |
|------------------------------------------------------|---------------------------------------------------|
| Fakturanummer                                       | Fakturanummer. Maks. 20 tegn                |
| Fakturabeskrivelse (valgfrit)                       |                                                   |
| Bogføringsdato (valgfrit)                              | Datoformat                                       |
| Fakturadato                                         | Datoformat                                       |
| Forfaldsdato (valgfrit)                                  | Datoformat                                       |
| Linjenummer                                          |                                                   |
|Varenummer (valgfrit)                                | 20 tegn **Bemærk:** Hvis nogen varenummer, skal du angive værdier i den **indkøbskategori** og **indkøbskategorihierarkiet** felter. Hvis ingen indkøbskategori og intet indkøbskategorihierarki er angivet, skal du angive en værdi i feltet **Varenummer**.                    |
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
| Antal                                               | Regnskabsfordelingslinjenummer      |
| Finanskonto                                       |                                          |
| Procent                                              | Decimalværdier er tilladt.              |




## <a name="what-do-i-do-next"></a>Hvad skal jeg gøre nu?
Når du har konfigureret forudsætninger, du skal bruge, kan du se [Engangsleverandører i den offentlige sektor](one-time-vendors-public-sector.md).

<a name="see-also"></a>Se også
--------

[One-time vendors in the public sector](one-time-vendors-public-sector.md)

[Kreditorbetalinger i den offentlige sektor](accounts-payable-public-sector.md)


