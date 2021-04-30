---
title: Ændre en behovsprognose manuelt
description: Dette emne viser, hvordan du redigerer prognosen for en vare
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889018"
---
# <a name="modify-a-demand-forecast-manually"></a>Ændre en behovsprognose manuelt

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du redigerer prognosen for en vare. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til produktionsplanlæggeren.

## <a name="modify-the-forecast-for-a-selected-item"></a>Redigere prognosen for en valgt vare

Sådan redigerer du prognosen for en valgt vare:

1. Gå til **Moduler \> Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Find og vælg den ønskede post på listen. Vælg den vare, du vil ændre varetypen prognosen for.
1. Åbn fanen **Plan** i handlingsruden, og vælg **Behovsprognose**.
1. Vælg en række på listen. Hvis der ingen prognoselinjer er, kan du oprette en ny linje ved at vælge **Ny** i handlingsruden.  
1. Skriv et positivt tal i feltet **Salgsantal**. Dette tal repræsenterer prognosemængden for varen. Der vises en fejl, hvis du angiver et negativt tal.
1. Udfyld de andre felter efter behov.
1. Vælg **Gem** i handlingsruden.

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a>Redigere prognosen for en eller flere varer i Microsoft Excel

sådan redigerer du prognosen for en eller flere varer i Microsoft Excel:

1. Benyt en af følgende fremgangsmåder:
    - Åbn siden **Behovsprognose** for en vilkårlig vare som beskrevet i forrige afsnit.
    - Gå til **Varedisponering \> Budgettering \> Manuel indtastning af prognose \> Behovsprognoselinjer**.
1. Vælg **Åbn i Microsoft Office \> Behovsprognoseposter** i handlingsruden.
1. Vælg en downloadplacering, gem og åbn derefter den downloadede fil i Excel.
1. Hvis du får vist en advarsel, skal du vælge **Aktivér redigering**.
1. Log på Supply Chain Management i Excel ved hjælp af Microsoft Dynamics-opgaveruden. Du skal logge på med indstillingen **Forbliv logget på**, og du skal have tillid til dataforbindelsesappen.
1. Excel-regnearket viser nu alle dit firmas aktuelle linjer i behovsprognosen.  Du kan tilføje, slette og redigere behovsprognoselinjer efter behov.
1. Vælg **Publicer** i Microsoft Dynamics-opgaveruden for at uploade dine ændringer tilbage til Supply Chain Management.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
