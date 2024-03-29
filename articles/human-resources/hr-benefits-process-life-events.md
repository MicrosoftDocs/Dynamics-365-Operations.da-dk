---
title: Behandle livshændelser
description: Under hele medarbejderens livscyklus i Microsoft Dynamics 365 Human Resources, kan de enkelte medarbejdere opleve forskellige ændringer i livshændelser.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ef160af483f81b8c1e60a274029b77c3cd34f924
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324782"
---
# <a name="process-life-events"></a>Behandle livshændelser

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Under hele medarbejderens livscyklus i Microsoft Dynamics 365 Human Resources, kan de enkelte medarbejdere opleve forskellige ændringer i livshændelser. Det kan f.eks. være ægteskab, ændring i ansættelsesforhold eller ændringer af afhængig/modtager-forhold. Hvis du vil bruge livshændelser, skal du aktivere livshændelser på siden **Parametre for frynsegoder**, konfigurere typer af livshændelser og angive indstillinger for livshændelser for plantyper.

Før du kan behandle livshændelser, skal du allerede have kørt åben tilmelding mindst en gang i løbet af en ansættelsesperiode. I USA sker åbne tilmeldinger typisk én gang om året. Uden for USA kan der køres en åben tilmelding på tidspunktet for ansættelsen. En arbejder behøver ikke at vælge en frynsegodeplan, for at der kan behandles livshændelser, men de skal have været medtaget i en åben tilmeldingsbehandling. 

Brug behandling af livshændelser, når du har arbejdere, der har en livshændelse, som finder sted på en fremtidig dato. Denne hændelse behandler alle de livshændelser, der ikke er behandlet (som f.eks. fremtidige livshændelser eller livshændelser, der er tilføjet, og som ikke er specifikke for én arbejder – det kan f.eks. være et nyt frynsegode). Realtidslivshændelser er skjulte.

Hvis dags dato f.eks. er 1. februar, og arbejder Karina Smith er den 14. februar planlagt til at ændre juridisk enhed, vil systemet behandle alle hændelser indtil den 15. februar, hvis du kører behandling af livshændelser for 15. februar. 

1. Vælg **Behandling af livshændelser** under **Behandling** i arbejdsområdet **Frynsegodeadministration**.

2. Angiv værdier for følgende felter i dialogboksen **Kør behandling af livshændelse**:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Tilmeldingsperiode** | Den tilmeldingsperiode, der skal behandles livshændelser for. |
   | **Juridisk enhed** | Den juridiske enhed, der skal behandles livshændelser for. |
   | **Dato for livshændelse** | Systemet behandler alle hændelser under den tilmeldingsperiode, der indtræffer indtil denne dato. |
   | **Arbejdstråd** | Den arbejder, der skal behandles livshændelser for. Hvis du ikke udfylder dette felt, behandles livshændelser for alle arbejdere. |

3. Hvis du vil køre processen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:

   1. Angiv oplysninger om processen.

   2. Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.

   3. Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.

   4. Vælg **OK**. Processen køres med de parametre, du angiver.

4. Vælg **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
