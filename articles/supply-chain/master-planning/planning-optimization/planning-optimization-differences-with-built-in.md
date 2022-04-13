---
title: Forskelle mellem indbygget behovsplanlægning og planlægningsoptimering
description: Dette emne viser funktioner, som Planlægningsoptimering endnu ikke understøtter, og som ikke vises på siden for analyse af tilpasning af Planlægningsoptimering.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 642ba812156a95e9b0be2e996d4a93096a5809a9
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468322"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Forskelle mellem indbygget behovsplanlægning og planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Resultater af planlægningsoptimering kan være forskellige fra resultaterne af det indbyggede system til behovsplanlægning. Forskellene kan også skyldes ventende funktioner. Dette emne viser funktioner, som Planlægningsoptimering endnu ikke understøtter, og som ikke vises på siden **[Analyse af tilpasning af Planlægningsoptimering](planning-optimization-fit-analysis.md)]**.

| Funktion | Aktuel funktionsmåde i Planlægningsoptimering |
|---|---|
| Fastvægtprodukter | Fastvægtprodukter betragtes som almindelige produkter.|
| Dimensioner, der kan udvides | Dimensioner, der kan udvides, er tomme på ordreforslag, også selvom afkrydsningsfeltet **Dækningsplan efter dimension** er markeret på siden **Lagringsdimensionsgrupper** eller **Sporingsdimensionsgrupper**. |
| Filtrerede produktionskørsler | Yderligere oplysninger finder du i [Produktionsplanlægning – Filtre](production-planning.md#filters). |
| Hovedplanlægning | Budgetplanlægning understøttes ikke. Det anbefales, at du bruger behovsplanlægning, når der er knyttet en budgetmodel til behovsplanen. |
| Nummerserier for ordreforslag | Nummerserier for ordreforslag understøttes ikke. Ordreforslagsnumre genereres på tjenestesiden. Ordreforslagsnummeret vises normalt med 10 cifre, men rækkefølgen er faktisk bygget på 20 tegn, hvor der er tildelt 10 cifre til den planlagte kørsel, og de øvrige 10 cifre i ordreforslagene tæller. |
| Plankopiering, sletning af plan og oprydning af planversion | <p>Følgende elementer deaktiveres under **Varedisponering \> Varedisponering \> Vedligeholdelse af planer** i navigationsruden:</p><ul><li>Plankopiering</li><li>Sletning af plan</li><li>Oprydning af planversion</li></ul> |
| Returordrer | Returordrer tages ikke i betragtning. |
| Planlægningsrelaterede funktioner | Nærmere oplysninger finder du under [Planlægning med ubegrænset kapacitet](infinite-capacity-planning.md#limitations). |
| Opfyldning af sikkerhedslager | Planlægningsoptimering bruger altid indstillingen *Dags dato + indkøbstid* for feltet **Udfyldning af minimum** på siden **Varedisponering**. Det er med til at undgå uønskede ordreforslag og andre problemer, for hvis indkøbstiden ikke indgår i sikkerhedslageret, vil ordreforslag, der oprettes for den aktuelle begrænsede disponible lagerbeholdning, altid blive forsinket grundet leveringstiden. |
| Sikkerhedslagerudligning og nettobehov | *Sikkerhedslager*-behovstypen medtages ikke og vises ikke på siden **Nettobehov**. Sikkerhedslager repræsenterer ikke behov og har ikke en behovsdato tilknyttet. Den angiver i stedet en begrænsning på, hvor meget lager der altid skal være til stede. Der tages dog stadig højde for værdien af feltet **Minimum** ved beregning af ordreforslag under varedisponering. Vi foreslår, at du undersøger kolonnen **Akkumuleret antal** på siden **Nettobehov** for at se, at denne værdi blev taget i betragtning. |
| Transportkalendere | Værdien i kolonnen **Transportkalender** på siden **Leveringsmåder** ignoreres. |
| Min./maks. disponeringskode uden værdier| Med det indbyggede planlægningsprogram behandles disponeringskoden som et krav, når du bruger en minimal/maksimal disponeringskode, hvor der ikke er angivet nogen minimum- eller maksimumværdier, og det opretter én ordre for hvert krav. Med planlægningsoptimering vil systemet oprette én ordre pr. dag for at dække det fulde beløb for den pågældende dag.  |

## <a name="additional-resources"></a>Yderligere ressourcer

- [Analyse af tilpasning af planlægningsoptimering](planning-optimization-fit-analysis.md)
- [Parametre, der ikke bruges af planlægningsoptimering](not-used-parameters.md)
- [Dato- og klokkeslætsparametre, der bruges af planlægningsoptimering](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
