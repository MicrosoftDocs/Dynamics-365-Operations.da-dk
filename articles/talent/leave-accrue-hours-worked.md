---
title: Periodisering af fravær baseret på antal arbejdstimer
description: Dette emne beskriver, hvordan orlovsplaner kan konfigureres til at periodisere fravær baseret på timearbejde.
author: Jcart1106
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2018-09-17
ms.dyn365.ops.version: ''
ms.openlocfilehash: f6489b84c71f2ac5a492b2d19cf087a05de8a599
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303699"
---
# <a name="accrue-time-off-based-on-hours-worked"></a>Periodisering af fravær baseret på antal arbejdstimer

[!include [banner](includes/banner.md)]


## <a name="overview"></a>Overblik

Organisationer med timeansatte kan tildele fravær baseret på arbejdstimer i stedet for ansættelse i organisationen. Data med arbejdstimer er typisk gemt i et system for tid og fremmøde. I Talent: Core HR kan de normale og overtidens arbejdstimer importeres og bruges som grundlag for en medarbejders bonus.

## <a name="leave-plans"></a>Orlovsplaner

I orlovsplanen kan periodiseringstypen enten være måneders tjeneste eller udførte arbejdstimer. Når arbejdstimer er valgt, findes der to typer timer, der skal bruges til periodisering: normale og overtid.

Du kan oprette en orlovsplan, der bruger arbejdstimer, ved at følge disse trin:

1. På siden **Orlovs- og fraværsplaner** skal du klikke på **Opret nye plan**.
2. Angiv et navn til orlovsplanen.
3. Vælg periodiseringsfrekvensen for planen.
5. Vælg startdatoen for planen.
6. Vælg periodiseringsperiodens grundlag, og vælg medarbejderspecifik dato, hvis det er relevant.
7. Til periodiseringens tidsplan skal du vælge **Antal arbejdstimer** for periodiseringstypen.
8. Vælg den type af timer, der skal bruges til periodiseringen.
9. Angiv antallet af arbejdstimer og det tilknyttede periodiseringsbeløb, minimumsaldo og maksimal overførsel eller tilskudsbeløb.

Periodiseringsplaner for behandling af arbejdstimer bruger periodiseringsfrekvensen sammen med grundlaget for periodiseringsperioden til at bestemme timerne, der skal periodiseres.

## <a name="annual-accrual-frequency"></a>Årlig periodiseringsfrekvens

| Dato for periodiseringsbonus    | Niveau for antal arbejdstimer    | Periodiseringsbeløb        | Datoer for antal arbejdstimer   | Faktiske antal arbejdstimer| Bonus               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 01-01-2018 til 31-12-2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 01-01-2018 til 31-12-2018  | 2000                | 0                 |


## <a name="monthly-accrual-frequency"></a>Månedlig periodiseringsfrekvens

| Dato for periodiseringsbonus    | Niveau for antal arbejdstimer    | Periodiseringsbeløb        | Datoer for antal arbejdstimer   | Faktiske antal arbejdstimer| Bonus               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 01-08-2018 til 31-08-2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 01-08-2018 til 31-08-2018   | 184                 | 3                   |

## <a name="semi-monthly-accrual-frequency"></a>Halvmånedlig periodiseringsfrekvens

| Dato for periodiseringsbonus    | Niveau for antal arbejdstimer    | Periodiseringsbeløb        | Datoer for antal arbejdstimer   | Faktiske antal arbejdstimer| Bonus               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6                     | 16-08-2018 til 31-08-2018  | 81                  | 6                  |        
| 8/31/2018             | 80                   | 6                     | 16-08-2018 til 31-08-2018  | 75                  | 0                   |

## <a name="weekly-accrual-frequency"></a>Ugentlig periodiseringsfrekvens

| Dato for periodiseringsbonus    | Niveau for antal arbejdstimer    | Periodiseringsbeløb        | Datoer for antal arbejdstimer   | Faktiske antal arbejdstimer| Bonus               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 27-08-2018 til 31-08-2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 27-08-2018 til 31-08-2018  | 35                  | 0                   |

## <a name="employee-assigned-leave-plans"></a>Medarbejdertildelte orlovsplaner

I medarbejderens tildelte orlovsplaner er niveaugrundlaget og typen af timer vist for de planer, hvor antal arbejdstimer defineres som periodiseringstypen. For aktive planer vises de faktiske arbejdstimer for periodiseringsperioder pr. dags dato også som reference. 

## <a name="loading-data"></a>Indlæser data

Faktiske timer kan importeres ved hjælp af enheden Antal brugte timer til orlov og fravær i datastyringen. Hvis du bruger arbejdstidskalendere, vil importen validere, at de normale arbejdstimer ikke overskrider de planlagte timer i døgnet, der er defineret af kalenderen. Importen validerer også, at antal arbejdstimer for en given dag ikke overstiger 24 timer. 

Følgende oplysninger skal bruges til at importere faktiske timer, der skal bruges i processen til periodisering af orlov:

+ Personalenummer 
+ Dato for arbejdsdag
+ Type
+ Timer

En enkelt dato kan kun have én af hver type tilknyttet.

| PERSONNELNUMBER       | DATEWORKED           | TYPE                  | HOURS                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Regulær               | 8                    |       
| 000337                | 8/7/2018             | Regulær               | 8                    |
| 000337                | 8/7/2018             | Overtid              | 3                    |
| 000337                | 8/8/2018             | Regulær               | 8                    |
| 000337                | 8/7/2018             | Regulær               | 8                    |
| 000337                | 8/9/2018             | Regulær               | 8                    |
