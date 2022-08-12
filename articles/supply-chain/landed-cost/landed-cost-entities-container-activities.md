---
title: Enheder til containeraktiviteter
description: Denne artikel indeholder oplysninger om containeraktiviteter, der bruges til at spore status for forsendelsescontainere.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 6a518003f8624ef05ac86be1b963c3f916420278
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167567"
---
# <a name="container-activities-entity"></a>Enhed for containeraktiviteter

[!include [banner](../includes/banner.md)]

Containeraktiviteter bruges til at spore status for forsendelsescontainere. Der oprettes en post for hver etape, som tildeles den ruteskabelon, som vælges, når der oprettes containere til forsendelse. Der oprettes også poster, når forsendelsescontaineren oprettes via en dataenhed.

Der modtages ofte oplysninger om status for en forsendelsescontainer i transit fra en ekstern kilde. Containeraktivitetsenheden giver en ekstern kilde som f.eks. en speditør mulighed for at opdatere posten direkte. Derfor kræves der ingen manuel opdatering af data.

## <a name="container-activities-itmcontaineractivityentity"></a>Containeraktiviteter (ITMContainerActivityEntity)

Du kan bruge containeraktivitetsenheden (`ITMContainerActivityEntity`) til at oprette flere aktivitetsposter. En speditør kan også sende opdateringer for en bekræftet værdi af **Faktisk slutdato**.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Faktisk slutdato | ITMContainerActivityTable.ActualEndDate | Datetime | Nej | Nej |
| Leveringsmåde | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | Nej | Nej |
| Forventet slutdato | ITMContainerActivityTable.EsimatedDate | Datetime | Nej | Nej |
| Linjenummer | ITMContainerActivityTable.LineNum | Numeric(32, 16) | **Ja** | Nej |
| Notater | ITMContainerActivityTable.Notes | nvarchar(MAX) | Nej | Nej |
| Aktivitet | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | Nej | **Ja** |
| Forsendelsescontainer | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **Ja** | **Ja** |
| Fragt | ITMContainerActivityTable.ShipId | Nvarchar(20) | **Ja** | **Ja** |
| Etape | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | Nej | **Ja** |
| Tjenesteudbyder | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | Nej | Nej |
| Temperatur | ITMContainerActivityTable.ShipTemperature | Numeric(32, 6) | Nej | Nej |
| Fartøj | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | Nej | Nej |
| Igangsæt dato | ITMContainerActivityTable.StartDate | Datetime | Nej | Nej |

## <a name="tracking-control"></a>Sporingskontrol

Sporingskontrolcenteret aktiverer en opdatering af et angivet kildefelt, der udløses af en opdatering af et angivet målfelt. Hvis både værdien i kildefeltet og værdien i målfeltet opdateres ved hjælp af containeraktivitetsenheden, vil målfeltet vise enhedsværdien. Denne funktionalitet er relateret til sporingskontrolposter, der har værdien **Opret type** i *Leveringstid*.

For omkostningsområder, der har **Opret type**-værdien *Statusopdatering* eller *Blank* (som er en brugerdefineret værdi), vil systemet opdatere rutestatussen eller målfeltet i henhold til sporingskontrolkonfigurationen.

## <a name="calculated-fields"></a>Beregnede felter

Værdierne i følgende felter i en containeraktivitetspost beregnes ud fra værdierne i de andre felter. Selvom disse beregnede felter ikke indgår i dataenheden, angives de, hvis de felter, som beregningerne er baseret på, er angivet.

- **Forventede dage** = **Forventet slutdato** – **Startdato**
- **Faktiske dage** = **Faktisk slutdato** – **Startdato**
