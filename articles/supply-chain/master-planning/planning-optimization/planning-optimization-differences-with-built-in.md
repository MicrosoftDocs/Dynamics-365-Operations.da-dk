---
title: Forskelle mellem planlægningsoptimering og det udfasede program til varedisponering
description: Denne artikel viser funktioner, som Planlægningsoptimering endnu ikke understøtter, og som ikke vises på siden for analyse af tilpasning af Planlægningsoptimering.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6e1671a508b85a94ac9687af15e898d885ea94c1
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745355"
---
# <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Forskelle mellem planlægningsoptimering og det udfasede program til varedisponering

[!include [banner](../../includes/banner.md)]

Resultater af planlægningsoptimering kan være forskellige fra resultaterne af det udfasede varedisponeringsprogram. Forskellene kan også skyldes ventende funktioner. Denne artikel viser funktioner, som Planlægningsoptimering endnu ikke understøtter, og som ikke vises på siden **[Analyse af tilpasning af Planlægningsoptimering](planning-optimization-fit-analysis.md)]**.

| Funktion | Aktuel funktionsmåde i Planlægningsoptimering |
|---|---|
| Fastvægtprodukter | Fastvægtprodukter betragtes som almindelige produkter.|
| Dimensioner, der kan udvides | Dimensioner, der kan udvides, understøttes ikke af planlægningsoptimering. Når du bruger planlægningsoptimering, er dimensioner, der kan udvides, tomme på ordreforslag, også selvom afkrydsningsfeltet **Dækningsplan efter dimension** er markeret på siden **Lagringsdimensionsgrupper** eller **Sporingsdimensionsgrupper**. |
| Filtrerede produktionskørsler | Yderligere oplysninger finder du i [Produktionsplanlægning – Filtre](production-planning.md#filters). |
| Hovedplanlægning | Budgetplanlægning understøttes ikke. Det anbefales, at du bruger behovsplanlægning, når der er knyttet en budgetmodel til behovsplanen. |
| Nummerserier for ordreforslag | Nummerserier for ordreforslag understøttes ikke. Ordreforslagsnumre genereres på tjenestesiden. Ordreforslagsnummeret vises normalt med 10 cifre, men rækkefølgen er faktisk bygget på 20 tegn, hvor der er tildelt 10 cifre til den planlagte kørsel, og de øvrige 10 cifre i ordreforslagene tæller. |
| Plankopiering, sletning af plan og oprydning af planversion | <p>Følgende elementer deaktiveres under **Varedisponering \> Varedisponering \> Vedligeholdelse af planer** i navigationsruden:</p><ul><li>Plankopiering</li><li>Sletning af plan</li><li>Oprydning af planversion</li></ul> |
| Returordrer | Returordrer tages ikke i betragtning. |
| Planlægningsrelaterede funktioner | Nærmere oplysninger finder du under [Planlægning med ubegrænset kapacitet](infinite-capacity-planning.md#limitations). |
| Opfyldning af sikkerhedslager | Planlægningsoptimering bruger altid indstillingen *Dags dato + indkøbstid* for feltet **Udfyldning af minimum** på siden **Varedisponering**. Det er med til at undgå uønskede ordreforslag og andre problemer, for hvis indkøbstiden ikke indgår i sikkerhedslageret, vil ordreforslag, der oprettes for den aktuelle begrænsede disponible lagerbeholdning, altid blive forsinket grundet leveringstiden. |
| Sikkerhedslagerudligning og nettobehov | *Sikkerhedslager*-behovstypen medtages ikke og vises ikke på siden **Nettobehov**. Sikkerhedslager repræsenterer ikke behov og har ikke en behovsdato tilknyttet. Den angiver i stedet en begrænsning på, hvor meget lager der altid skal være til stede. Der tages dog stadig højde for værdien af feltet **Minimum** ved beregning af ordreforslag under varedisponering. Vi foreslår, at du undersøger kolonnen **Akkumuleret antal** på siden **Nettobehov** for at se, at denne værdi blev taget i betragtning. Da udligningen er forskellig, kan der blive foreslået forskellige handlinger. |
| Transportkalendere | Værdien i kolonnen **Transportkalender** på siden **Leveringsmåder** ignoreres. |
| Min./maks. disponeringskode uden værdier| Med det udfasede varedisponeringsprogram behandles disponeringskoden som et krav, når du bruger en minimal/maksimal disponeringskode, hvor der ikke er angivet nogen minimum- eller maksimumværdier, og det opretter én ordre for hvert krav. Med planlægningsoptimering vil systemet oprette én ordre pr. dag for at dække det fulde beløb for den pågældende dag.  |
| Nettobehov og manuelt oprettede ordreforslag | Med det udfasede varedisponeringsprogram vises manuelt oprettede forsyningsordrer for en vare automatisk blandt nettobehovet for den pågældende vare. Når der f.eks. oprettes en indkøbsordre fra en salgsordre, vises indkøbsordren på siden **Nettobehov** uden at kræve nogen forudgående handlinger. Det skyldes, at det udfasede varedisponeringsprogram registrerer lagertransaktioner i `inventLogTTS`-tabellen og viser ændringer på siden **Nettobehov** for dynamiske planer. Med planlægningsoptimering vises manuelt oprettede ordrer dog ikke blandt nettobehovet for en vare, før planlægningsoptimering køres (ved hjælp af en plan, der omfatter varen), eller indtil du vælger **Opdater \> Varedisponering** i handlingsruden på siden **Nettobehov**, som vil køre varedisponering for varen. Yderligere oplysninger om, hvordan denne side fungerer med **Nettobehov**, finder du i [Nettobehov og udligningsoplysninger](net-requirements.md). |
| Ressourcetildeling | Når du arbejder med ubegrænset kapacitet, tildeler det udfasede varedisponeringsprogram alle ordreforslag til den samme ressource i en given ressourcegruppe. Planlægningsoptimering forbedrer dette ved at vælge tilfældige ressourcer, så forskellige produktionsordrer kan bruge forskellige ressourcer. Hvis du vil bruge den samme ressource til alle ordreforslag, skal du angive ressourcen i ruten. |
| Udvidede datatyper (EDT'er) | Planlægningsoptimering understøtter ikke ændringer af præcisionen for EDT'er. Det betyder, at denne proces ikke officielt understøttes og ikke nødvendigvis fungerer. |
| Opfyldning af sikkerhedslager | Planlægningsoptimering bruger altid **Opfyld minimum** som *Dags dato + fremskaffelsestid*. Dette forbereder systemet på at bruge en forenklet planlægningsopsætning i fremtiden og giver et resultat, der kan handles ud fra. Hvis fremskaffelsestiden ikke medtages i sikkerhedslageret, vil ordreforslag, der oprettes for lav disponibel lagerbeholdning, altid blive forsinket grundet leveringstiden. Denne funktionsmåde kan forårsage betydelige problemer og uønskede ordreforslag. Den bedste praksis er at ændre indstillingen, så *Dags dato + fremskaffelsestid* bruges. Opdater masterdata for at undgå advarsler. |
| Kopiér statisk til dynamisk plan | Planlægningsoptimering kopierer ikke statiske planer til dynamiske planer, uanset indstilling på siden **Varedisponeringsparametre**. Generelt er denne handling ikke så relevant på grund af hastigheden og den fuldstændige genopretning, som planlægningsoptimering giver. Hvis der bruges to eller flere planer, skal varedisponeringen udløses for hver enkelt plan. |

## <a name="additional-resources"></a>Yderligere ressourcer

- [Analyse af tilpasning af planlægningsoptimering](planning-optimization-fit-analysis.md)
- [Parametre, der ikke bruges af planlægningsoptimering](not-used-parameters.md)
- [Dato- og klokkeslætsparametre, der bruges af planlægningsoptimering](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
