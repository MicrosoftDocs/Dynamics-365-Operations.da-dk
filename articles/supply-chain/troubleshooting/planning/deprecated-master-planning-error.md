---
title: Du får vist en fejlmeddelelse, når du kører det indbyggede program til varedisponering
description: Når du kører det udgåede program til varedisponering, får du vist en fejlmeddelelse.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294039"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a>Du får vist en fejlmeddelelse, når du kører det indbyggede program til varedisponering

Fejlkode: ReqCalcScheduleItemTablePlanningOptimizationFitError

## <a name="symptoms"></a>Symptomer

Når du kører varedisponering ved hjælp af det udgåede program til varedisponering, får du vist følgende fejlmeddelelse:

> Du får vist denne fejlmeddelelse, fordi det indbyggede varedisponeringsprogram blev brugt til scenarier, der understøttes af Planlægningsoptimering. Du bør migrere til Planlægningsoptimering nu, da den aktuelt indbyggede varedisponering udfases. Bemærk, at denne varedisponeringskørsel blev fuldført korrekt. Hvis din migrering har en stærk afhængighed i forhold til ventende funktioner, kan du anmode om en undtagelse for fortsat at bruge det indbyggede varedisponeringsprogram. Udfyld følgende spørgeskema for at komme i gang, og hvis det er relevant, skal du anmode om en undtagelse fra migrering til Planlægningsoptimering. [Spørgeskema om migrering til og undtagelse for Planlægningsoptimering](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a>Årsag

Hvis du kører planlægning, og du ikke bruger funktioner til produktionsstyring, bør du overveje at migrere til Planlægningsoptimering. Det indbyggede program til varedisponering udfases. Så hvis du vil fortsætte med at bruge det uden at modtage fejlmeddelelsen, skal du ansøge om en undtagelse fra Microsoft.

## <a name="resolution"></a>Løsning

Du kan finde flere oplysninger om, hvordan du migrerer til Planlægningsoptimering, eller hvordan du ansøger om en undtagelse, så du fortsat kan bruge det udgåede indbyggede planlægningsprogram i stedet, i [Migrering til planlægningsoptimering for varedisponering](/dynamics365/supply-chain/master-planning/new-master-planning-engine).
