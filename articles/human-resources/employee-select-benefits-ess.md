---
title: Medarbejderne vælger planer via medarbejderselvbetjening (valgfrit)
description: Denne artikel beskriver, hvordan medarbejdere kan vælge eller opdatere deres frynsegoder.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 162cf2bfb6d382d270e0a5af42a739a390397153
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324436"
---
# <a name="employees-select-plans-by-using-employee-self-service-optional"></a>Medarbejderne vælger planer via medarbejderselvbetjening (valgfrit)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Når en ny medarbejder ansættes, eller der indtræffer en livshændelse, kan medarbejderen bruge **Medarbejderselvbetjening** til at vælge eller opdatere deres frynsegoder under åben tilmelding.

For at få adgang til deres frynsegoder for tilmelding går medarbejderen til **Medarbejderselvbetjening** og vælger derefter **Frynsegodeselvbetjening** på feltet **Frynsegoder**.

På siden **Frynsegodeselvbetjening** grupperes frynsegodeplaner efter plantype. Hvis de vil have vist frynsegodeplaner i en plantype, vælger medarbejderne et felt på siden **Medarbejderfrynsegoder**. Medarbejderen kan kun se de frynsegoder, de er berettiget til.

> [!IMPORTANT]
> Før en plantype kan vises i **Medarbejderselvbetjening**, skal den konfigureres. Du kan finde flere oplysninger under [Konfigurere medarbejderselvbetjening](/dynamics365/human-resources/hr-benefits-setup-employee-self-service).

Afhængigt af plantypen kan der vælges en eller flere frynsegoder ved tilmelding. En sundhedsplantype kan f.eks. konfigureres for at begrænse medarbejderen til én sundhedsplan. En livsforsikringsplantype kan give medarbejderen mulighed for at vælge flere livsforsikringsplaner.

Når medarbejderen har besluttet, hvilken plan der skal tilmeldes, kan det være nødvendigt at vælge afhængige. Hvis medarbejderen har valgt en dækningsindstilling, der er **Medarbejder +1**, **Medarbejder + børn** eller **Familie**, skal de afhængige vælges. Du kan finde flere oplysninger om dækningsindstillinger under [Oprette dækningsindstillinger](/dynamics365/human-resources/hr-benefits-setup-coverage-options).

For at vælge en frynsegodeplan vælger medarbejderen enten ellipseknappen (**...**) eller **Tilføj til indkøbsvogn**. Når medarbejderen er færdig med at føje alle frynsegodevalg til indkøbsvognen, vælger de **Vis indkøbsvogn**. Medarbejderen tages derefter til siden **Planer**, hvor de kan få vist de valgte og fravalgte frynsegodeplaner.

Medarbejderen skal vælge indstillingen **Jeg accepterer**, før medarbejderen kan vælge knappen **Kasse**. Den sætning, der vises til højre for indstillingen **Jeg accepterer**, kan tilpasses under fanen **Frynsegodeadministration** på siden **Delte Human Resources-parametre**.

Når medarbejderen bekræfter valgene af frynsegodeplanen ved hjælp af **Medarbejderselvbetjening**, registreres disse valg, og de vises på siderne **Frynsegodeplaner for arbejder** og **Masseopdatering af medarbejderes frynsegoder**.

Når medarbejderen har valgt planer, vises status for frynsegoderne som **Valgt**. Når medarbejderen vælger **Check ud** på siden **Frynsegodeselvbetjening**, er indstillingen **Tjekket ud** valgt.

> [!IMPORTANT]
> For at fuldføre tilmeldingen skal administratoren af frynsegoder vælge **Bekræft** for hver valgte medarbejderfrynsegode. Bekræftelsen kan fuldføres på siden **Frynsegodeplan for arbejder** eller **Masseopdatering af medarbejderes frynsegoder**.
>

Medarbejdere behøver ikke vælge frynsegoder ved brug af **Medarbejderselvbetjening**. Frynsegoder kan vælges på vegne af en medarbejder på siden **Frynsegodeplan for arbejder** eller **Masseopdatering af medarbejderes frynsegoder**. Medarbejderen bliver først tilmeldt disse frynsegoder, når administratoren af frynsegoder har bekræftet dem.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
