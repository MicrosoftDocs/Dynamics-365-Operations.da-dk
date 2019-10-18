---
title: Afhænd et anlægsaktiv som kasseret
description: Emnet indeholder en beskrivelse af, hvordan du eliminerer posteringer for et anlægsaktiv, der er blevet afhændet som kasseret.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: de105e061712540fc8e3d720a65c029f865b8948
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187285"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a>Afhænd et anlægsaktiv som kasseret

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Emnet indeholder en beskrivelse af, hvordan du eliminerer posteringer for et anlægsaktiv, der er blevet afhændet som kasseret. De posteringstyper, der kan fjernes, omfatter et anlægs anskaffelse og akkumulerede afskrivningsposteringer og andre anlægsaktivposteringer. Eliminering af disse posteringer påvirker statuskonti, f.eks. anskaffelsesregulering, regulering af afskrivning, værdiregulering, opskrivnings- og nedskrivningskonti.

| Postering                                         | Debet (D.) | Kredit (K.) |
|-----------------------------------------------------|-------------|--------------|
| D. Akkumuleret afskrivning                        | X           |              |
| K. Anlægsaktiver gevinst/tab                          |             | X            |
| D. Anlægsaktiver gevinst/tab                          | X           |              |
| K. Konto for anskaffelse af anlægsaktiv                 |             | X            |
| D. Anlægsaktiver gevinst/tab (bogført nettoværdi \[BNV\]) | X           |              |
| K. Anlægsaktiver gevinst/tab (BNV)                    |             | X            |

> [!NOTE]
> Det anbefales, at du arbejder tæt sammen med firmaets regnskabsdirektør eller controller for at identificere de korrekte konti, der skal bruges til hver enkelt posteringstype, og til at kontrollere, at kassationsprocessen og de transaktioner, den genererer, opdaterer disse konti korrekt.

Før du afhænder et anlægsaktiv som kasseret, skal du oprette finanskonti, der er knyttet til anlægsaktivets anskaffelsesværdi, afskrivning for indeværende år, afskrivning for tidligere år og anlægsaktivets BNV. Posteringstyperne for anlægsaktiver vises på siden **Posteringsprofiler for anlægsaktiver**. Gå til **Anlægsaktiver \> Opsætning \> Posteringsprofiler for anlægsaktiver**, og vælg derefter **Kasseres** i feltet over gitteret på oversigtspanelet **Kassation**. I følgende illustration vises listen over posteringstyper for anlægsaktiver på siden **Posteringsprofiler for anlægsaktiver**.


[![Afhændelse af et aktiv som kasseret, fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)

I følgende eksempel blev der anskaffet et anlægsaktiv d. 1. januar 2018, og det vil blive kasseret den 31. marts 2019.

- **Anskaffelsespris** : 24.000,00 amerikanske dollars (USD)
- **Levetid:** To år
- **Afskrivningsmetode:** Lineær afskrivning over servicelevetiden
- **Afskrivningsbeløb:** 1.000,00 USD pr. måned

BNV for et anlægsaktiv beregnes ved hjælp af følgende formel:

Bogført nettoværdi = anskaffelsespris – afskrivning

I dette eksempel blev anlægsaktivet anskaffet og afskrevet over 15 måneder fra januar 2018 til og med marts 2019. Derfor er anlægsaktivets BNV 9.000.00 USD (24.000,00 USD – 15.000,00 USD).

[![Eksempel på afskrivning af anlægsaktiv](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)


Hvis du vil oprette en kassationskladde, skal du gå til **Anlægsaktiver \> Kladdeposteringer \> Anlægsaktivkladde** og derefter vælge **Linjer** i handlingsruden. Vælg **Kassation - spild**, og vælg derefter et anlægsaktiv-id. Hvis du vil afhænde aktivet fuldstændigt, skal du ikke angive en værdi i hverken **Debet**- eller **Kredit**-feltet

[![Anlægsaktivkladde](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)

Spildposteringen for kassation af anlægsaktiver ændrer feltværdierne for anlægsaktivkartoteket på følgende måder:

- I sektionen **Saldo** opdateres feltet **Status** til **Skrottet**.
- Feltet **Afhændelsesdato** i sektionen **Afgang** angives til den dato, hvor aktivet blev kasseret.

[![Oplysninger om anlægsaktivkladde](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)

I følgende illustration vises anlægsaktivets saldo.

[![Saldo for anlægsaktiver](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)

I følgende illustration vises det bilag, der er bogført.

[![Bogført nettoværdi](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)
