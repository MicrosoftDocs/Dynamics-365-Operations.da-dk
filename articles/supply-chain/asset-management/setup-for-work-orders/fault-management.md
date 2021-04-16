---
title: Fejlhåndtering
description: I dette emne beskrives fejlhåndtering i Styring af aktiver.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c87bfa057fd2808551674f2acb9d654ad47e9a42
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825656"
---
# <a name="fault-management"></a>Fejlhåndtering

[!include [banner](../../includes/banner.md)]

 

I Styring af aktiver kan du bruge fejldesigneren til at konfigurere fejlsymptomer, fejlområder og fejltyper for aktivtyper. På denne måde kan du styre fejl, der er registreret på aktiver. Desuden kan fejlårsager og forslag til rettelse af fejl registreres på en arbejdsordre.

Processen for registrering og administration af fejl består af disse trin.

1. Opret en liste over fejlsymptomer, fejlområder og fejltyper, der kan opstå på dine aktivtyper.
2. Konfigurer symptomer, fejlområder og fejltyper i fejldesigneren.

Her er nogle eksempler, der kan hjælpe dig med at forstå forskellen mellem fejlsymptomer, fejlområder og fejltyper.

**Fejlsymptomer:**

- Ubalanceret spænding
- Kortslutning
- Støj
- Lækage
- Vibrationer

**Fejlområder:**

- Elektrisk
- Mekanisk
- Hydraulisk
- Pneumatisk

**Fejltyper:**

- Defekt hovedstatorvikling
- Defekt diode
- Snavsede viklinger
- Defekt generator
- Defekt sensor

## <a name="create-fault-symptoms"></a>Oprette fejlsymptomer

Udfør følgende trin for at oprette en liste over symptomer, der kan bruges i fejldesigneren.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Fejl** \> **Fejlsymptomer**.
2. Vælg **Ny** for at oprette en post.
3. Angiv et navn til fejlsymptomet i feltet **Fejlsymptom**.
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. Vælg **Gem**.

## <a name="create-fault-areas"></a>Oprette fejlområder

Udfør følgende trin for at oprette en liste over områder eller steder, der kan bruges i fejldesigneren.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Fejl** \> **Fejlområder**.
2. Vælg **Ny** for at oprette en post.
3. Angiv et navn til fejlområdet i feltet **Fejlområde**.
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. Vælg **Gem**.

## <a name="create-fault-types"></a>Oprette fejltyper

Udfør følgende trin for at oprette en liste over fejltyper, der kan bruges i fejldesigneren.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Fejl** \> **Fejltyper**.
2. Vælg **Ny** for at oprette en post.
3. Angiv et navn for fejltypen i feltet **Fejltype**.
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. Vælg **Gem**.

## <a name="set-up-the-fault-designer"></a>Konfigurere fejldesigneren

I fejldesigneren konfigurerer du fejldata på aktivtyper.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Fejl** \> **Fejldesigner**.
2. Vælg den type aktiv, du vil oprette en fejlpost for, i ruden til venstre.
3. Vælg **Tilføj linje** i oversigtspanelet **Fejlsymptom**, og vælg derefter et fejlsymptom i feltet **Fejlsymptom**.
4. Vælg **Tilføj linje** i oversigtspanelet **Fejlområde**, og vælg derefter et fejlområde i feltet **Fejlområde**.
5. Vælg **Tilføj linje** i oversigtspanelet **Fejltype**, og vælg derefter en fejltype i feltet **Fejltype**.
6. Hvis du hurtigt vil oprette kombinationer af alle eksisterende fejlsymptomer, -områder og -typer for den valgte aktivtype, skal du vælge **Opret fejlkombinationer**. Denne funktion er nyttig, hvis du har tilføjet mange fejlsymptomer, -områder og -typer. Det er nemmere at slette linjer for kombinationer, der ikke er relevante for aktivtypen, end at oprette nye linjer manuelt.

    > [!NOTE]
    > Hvis du vil kopiere opsætningen af fejlsymptomer, -områder og -typer fra én aktivtype til den valgte aktivtype, skal du vælge **Kopiér fra aktivtype**.

7. Vælg **Gem** for at gemme ændringerne.

![Siden Fejldesigner](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a>Oprette fejlårsager

Udfør følgende trin for at oprette en liste over kendte fejlårsager, der kan føjes til en arbejdsordre eller en vedligeholdelsesanmodning.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Fejl** \> **Fejlårsager**.
2. Vælg **Ny** for at oprette en post.
3. Angiv et navn for fejlårsagen i feltet **Fejlårsag**.
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. Vælg **Gem**.

## <a name="create-fault-remedies"></a>Oprette fejlrettelser

Udfør følgende trin for at oprette en liste over forslag til rettelser og reparationer, der kan føjes til en arbejdsordre eller en vedligeholdelsesanmodning.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Fejl** \> **Fejlrettelser**.
2. Vælg **Ny** for at oprette en post.
3. Angiv et navn til fejlrettelsen i feltet **Fejlrettelse**.
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. Vælg **Gem**.

> [!NOTE]
> Du kan ændre navnene på dine fejlsymptomer, -områder, -typer, -årsager og -rettelser efter behov. Navneændringerne afspejles automatisk i de relaterede fejlregistreringer.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]