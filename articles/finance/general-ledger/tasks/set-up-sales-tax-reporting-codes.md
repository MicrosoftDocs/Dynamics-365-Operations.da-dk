---
title: Konfigurer momsrapporteringskoder
description: Momsrapporteringskoderne refererer til et feltnummer i en momsrapport.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4751256858da417ec9bb1b7d9ccd16fb6bef1cac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185928"
---
# <a name="set-up-sales-tax-reporting-codes"></a>Konfigurer momsrapporteringskoder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Momsrapporteringskoderne refererer til et feltnummer i en momsrapport. De bruges i landespecifikke rapportlayout og i rapporten Momsafregning pr. kode til at udskrive momsbeløb for en afregningsperiode, der er opsummeret pr. rapporteringskode. Når du har oprettet momsrapporteringskoderne, kan du referere til dem i oversigtspanelet Rapportopsætning på siden Momskode. 

Denne registrering anvender demofirmaet DEMF.

1. Gå i **Navigationsrude** til **Moms > Opsætning > Moms > Momsrapporteringskoder**.
2. Klik på **Ny**.
3. Vælg det rapportlayout, som rapporteringskoden hører til. Dette layout bruges til at filtrere de tilgængelige rapporteringskoder til en momskode. Hver momskode tilhører en afregningsperiode, der tilhører en momsmyndighed som bruger et rapportlayout.  
4. Angiv et tal i feltet **Rapporteringskode**.
5. Angiv en beskrivelse, der skal vises i rapporter, i feltet **Rapporttekst**.
6. Angiv en beskrivelse til interne formål i feltet **Kort beskrivelse**.
7. Klik på **Gem**.
