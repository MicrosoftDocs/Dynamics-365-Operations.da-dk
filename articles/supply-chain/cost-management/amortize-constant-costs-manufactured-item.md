---
title: Amortisere konstante omkostninger for en produceret vare
description: "En produceret vares konstante omkostninger afspejler opstillingstiderne for operationer og komponenter, der har et konstant antal eller et konstant skrotbeløb."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 75c0f5bcff0aae63aa8c7dae9b0767f8c7e6a81c
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a>Amortisere konstante omkostninger for en produceret vare

[!INCLUDE [banner](../includes/banner.md)]

En produceret vares konstante omkostninger afspejler opstillingstiderne for operationer og komponenter, der har et konstant antal eller et konstant skrotbeløb. 

Begrebet efterkalkulationslotstørrelse bruges til at amortisere disse konstante omkostninger i den beregnede kostpris for en produceret vare. Der er adskillige synonymer til begrebet, et af dem regnskabsmæssig lotstørrelse. Begrebet amortisering af konstante omkostninger har også adskillige synonymer, hvoraf et er proportionale konstante omkostninger.

Antallet i en efterkalkulationslotstørrelsen for en produceret vare bruges i en styklistekalkulation. Antallet afhænger af, hvordan du starter og udfører styklistekalkulationen, som det vises af følgende:

-   Standardberegningsmængden i styklistekalkulationen for en vare – Standardordreantallet for lager for varen fungerer som efterkalkulationslotstørrelse, men standardværdien kan være et større antal, sådan at den afspejler kvoten for varens ordreantal. Varens standardordreantal og -kvote kan angives inden for varens standardordreindstillinger eller lokationsspecifikke ordreindstillinger.
-   Angivet beregningsantal i styklistekalkulationen for en vare − Den angivne beregningsmængde fungerer som efterkalkulationslotstørrelse for varen. Antallet for beregningsmængden bruger først varens standardordreantal, men standardværdien kan tilsidesættes manuelt. Den angivne beregningsmængde repræsenterer efterkalkulationslotstørrelsen for den angivne vare og for fremstillede komponenter, der har en styklistelinje af typen produktion. Det er fordi, det antages, at komponenten skal fremstilles i nøjagtigt antal. Efterkalkulationslotstørrelsen for andre fremstillede komponenter, der har styklistelinjetypen Vare, vil afspejle deres standardordreantal.
-   Angiven beregningsmængde for Fremstil til ordre i styklistekalkulationen for en vare – Den angivne beregningsmængde fungerer som efterkalkulationslotstørrelse for varen og dens fremstillede komponenter, når styklistekalkulationer bruger udfoldningstilstanden Fremstil til ordre. De forudsættes, at de fremstillede komponenter vil blive fremstillet i nøjagtigt antal på samme måde som en fremstillet komponent, der har styklistetypen Produktion.
-   Den angivne beregningsmængde i en ordrespecifik styklistekalkulation – Der kan udføres en ordrespecifik styklistekalkulation for en varelinje på en salgsordre, et salgstilbud eller en serviceordre. Antallet for den angivne beregningsmængde bruger antallet på den oprindelige varelinje, men standardantallet kan tilsidesættes. Du kan vælge, om den ordrespecifikke styklistekalkulation bruger udfoldningstilstanden Fremstil til ordre eller Flere niveauer.

Det beregnede beløb af en produceret vares amortiserede konstante omkostninger kaldes gebyrer.






