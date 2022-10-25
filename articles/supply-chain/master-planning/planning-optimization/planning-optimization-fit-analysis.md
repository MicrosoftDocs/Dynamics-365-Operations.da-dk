---
title: Analyse af tilpasning af planlægningsoptimering
description: Denne artikel beskriver, hvordan du kan kontrollere den aktuelle opsætning og de nuværende data i forhold til funktionerne i funktionen Planlægningsoptimering.
author: t-benebo
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 15ec53c1f13b3017fb6e829bd1c8e99fbb938ce3
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689988"
---
# <a name="planning-optimization-fit-analysis"></a>Analyse af tilpasning af planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Du skal analysere resultatet fra planlægningsoptimeringen og tilpasse analysen som en del af migreringsprocessen. Bemærk, at omfanget af planlægningsoptimering ikke er lig med den aktuelle indbyggede funktionalitet for varedisponering. Det anbefales, at du samarbejder med partneren og læser dokumentationen for at forberede migreringen. 

Tilpasset analyse af planlægningsoptimering hjælper dig med at identificere, hvor resultatet kan være anderledes mellem det indbyggede varedisponeringsprogram og planlægningsoptimering. Denne analyse foretages på basis af den aktuelle opsætning og dine data. 

Hvis du vil have vist analyseresultatet for tilpasning af planlægningsoptimering, skal du gå til **Varedisponering** \> **Konfiguration** \> **Analyse af tilpasning af planlægningsoptimering** og derefter vælge **Kør analyse**. Hvis analysen finder nogen uoverensstemmelser, vises de på samme side. (Det kan tage et par minutter at køre analysen).

> [!NOTE]
>
> - Visse uoverensstemmelser kan ikke identificeres af tilpasningsanalysen for Planlægningsoptimering. Du kan finde flere oplysninger i [Forskelle mellem klassisk behovsplanlægning og planlægningsoptimering](planning-optimization-differences-with-built-in.md).
>
> - Hvis der findes uoverensstemmelser, kan du stadig bruge Planlægningsoptimering. Resultaterne af tilpasningsanalysen viser kun de steder, hvor planlægningstjenesten ikke kan overholde din aktuelle opsætning. Det vil sige, at det vises de steder, hvor nogle processer muligvis bliver ignoreret eller ikke understøttes.

## <a name="analysis-results-example-1"></a>Analyseresultater: eksempel 1

- **Funktion:** Produktion
- **Problem:** Varer med et styklisteniveau større end nul: 56
- **Forklaring:** Tilpasningsanalysen fandt 56 varer, der har en styklisteopsætning til produktion. Da den aktuelle version af funktionen Planlægningsoptimering ikke understøtter produktion, vil Planlægningsoptimering oprette indkøbsordreforslag i stedet for produktionsordreforslag. Der vises også en advarsel om, at de berørte varer vises.

## <a name="analysis-results-example-2"></a>Analyseresultater: eksempel 2

- **Funktion:** Handlinger
- **Afgang:** Disponeringsgrupper med aktiveret handlingsberegning: 6
- **Forklaring:** Tilpasningsanalysen fandt seks disponeringsgrupper, hvor handlingsberegningen er aktiveret. Da den aktuelle version af Planlægningsoptimerings ikke understøtter handlinger, vil der ikke blive genereret handlinger ved varedisponering.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Oversigt over mulige resultater fra tilpasningsanalysen

Følgende tabel viser de forskellige resultater, der kan vises efter en tilpasningsanalyse. Nummertegn (*\#*) erstattes med et tal, der angiver antallet af poster, der har den viste fejl.

> [!IMPORTANT]
> For funktioner, der endnu ikke understøttes, indeholder følgende tabel oplysninger om forventet tilgængelighed, der er estimeret ud fra vores aktuelle oversigt. Disse estimater kan ændres uden forudgående varsel.

| Funktion | Vist problem | Forklaring | Forventet tilgængelighed |
| --- | --- | --- | --- |
| Handlinger | Disponeringsgrupper med handlingsberegning aktiveret: *\#* | Denne funktion understøttes nu. | Understøttet |
| Basiskalendere | Kalendere, der bruger basiskalender: *\#* | Denne funktion understøttes nu. | Understøttet | 
| Batchdispositionskoder | Ikke-tilgængelige batchdispositionsmaster: *\#* | Denne funktion understøttes nu. Du kan finde flere oplysninger i [Bruge batchdispositionskoder til at markere batches som disponible eller ikke til rådighed](../../inventory/batch-disposition-codes.md) | Understøttet |
| Leveringsevne (LE) | Standardindstillinger for ordre med leveringsdatokontrollen angivet til LE: *\#* | I Supply Chain Management 10.0.28 og nyere gør en proces kaldet *CTP for Planlægningsoptimering* bekræftede afsendelses- og tilgangsdatoer tilgængelige, når den dynamiske plan er kørt. I ældre versioner af Supply Chain Management ignoreres den tidligere CTP-indstilling, når Planlægningsoptimering er aktiveret. | Understøttet |
| Kopiér statisk til dynamisk plan | Kopi af statisk til dynamisk plan er aktiveret på varedisponeringsparametrene. | Planlægningsoptimering kopierer ikke den statiske plan til den dynamiske plan, uanset denne indstilling. Generelt er dette koncept ikke så relevant på grund af hastigheden og den fuldstændige genopretning, som planlægningsoptimering giver. Hvis der bruges to eller flere planer, skal varedisponeringen udløses for hver enkelt plan. | I/T |
| Autorisation | Disponeringsgrupper med automatisk autorisationstidshorisont angivet: *\#* | I version 10.0.7 og nyere understøttes autorisation som et separat autorisationsbatchjob, efter at varedisponering er fuldført (hvis funktionen *Automatisk autorisation med planlægningsoptimering* er blevet aktiveret i [funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Bemærk, at automatisk autorisation med planlægningsoptimering er baseret på ordredatoen (startdato), og ikke behovsdatoen (slutdato). Denne funktionsmåde sikrer, at der sker en rettidig autorisation af ordreforslag, uden at leveringstiden i autorisationstidshorisonten skal medtages. | Understøttet |
| Autorisation | Varedisponeringsposter med automatisk autorisation angivet: *\#* | I version 10.0.7 og nyere understøttes automatisk autorisation som et separat autorisationsbatchjob, efter at varedisponering er fuldført (hvis funktionen *Automatisk autorisation med planlægningsoptimering* er blevet aktiveret i [funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Bemærk, at automatisk autorisation med planlægningsoptimering er baseret på ordredatoen (startdato), og ikke behovsdatoen (slutdato). Denne funktionsmåde sikrer, at der sker en rettidig autorisation af ordreforslag, uden at leveringstiden i autorisationstidshorisonten skal medtages. | Understøttet |
| Autorisation | Behovsplaner med automatisk autorisation angivet: *\#* | I version 10.0.7 og nyere understøttes automatisk autorisation som et separat autorisationsbatchjob, efter at varedisponering er fuldført (hvis funktionen *Automatisk autorisation med planlægningsoptimering* er blevet aktiveret i [funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Bemærk, at automatisk autorisation med planlægningsoptimering er baseret på ordredatoen (startdato), og ikke behovsdatoen (slutdato). Denne funktionsmåde sikrer, at der sker en rettidig autorisation af ordreforslag, uden at leveringstiden i autorisationstidshorisonten skal medtages. | Understøttet |
| FitAnalysisPlanningItems | Planlægningsvarer: *\#* | Denne funktion afventer. I øjeblikket håndteres planlægningsvarer som almindelige varer, når planlægningsoptimering er aktiveret. | 2022 udgivelsesbølge 2 eller senere |
| Prognose | Disponeringsgrupper med "Medtag interne handelsordrer" aktiveret: *\#* | Denne funktion understøttes nu. Yderligere oplysninger finder du i [Planlægning af intern handel](Intercompany-planning.md) | Understøttet |
| Prognose | Disponeringsgrupper med indstillingen "Reducer prognose med" indstillet til en anden værdi end "Ordrer": *\#* | Denne funktion understøttes nu. Du kan finde flere oplysninger under [Varedisponering med behovsprognoser](demand-forecast.md) | Understøttet |
| Prognose | Prognosemodeller med undermodeller: *\#* |  Denne funktion understøttes nu. Du kan finde flere oplysninger under [Varedisponering med behovsprognoser](demand-forecast.md) | Understøttet |
| Prognose | Behovsplaner med "Medtag forsyningsprognose" aktiveret: *\#* | Denne funktion afventer. Aktuelt er forsyningsprognoser ikke understøttet, når planlægningsoptimering er aktiveret. De ignoreres, uanset hvilken indstilling der er angivet. | 2022 udgivelsesbølge 2 eller senere |
| Låsningstidshorisont | Disponeringsgrupper med låsningstidshorisont angivet: *\#* | Denne funktion afventer. I øjeblikket ignoreres opsætningen af låsningstidshorisont, når planlægningsoptimering er aktiveret, uanset denne indstilling. | 2022 udgivelsesbølge 2 |
| Låsningstidshorisont | Varedisponeringsposter med låsningstidshorisont angivet: *\#* | Denne funktion afventer. I øjeblikket ignoreres opsætningen af låsningstidshorisont, når planlægningsoptimering er aktiveret, uanset denne indstilling. | 2022 udgivelsesbølge 2 |
| Låsningstidshorisont | Behovsplaner med låsningstidshorisont angivet: *\#* | Denne funktion afventer. I øjeblikket ignoreres opsætningen af låsningstidshorisont, når planlægningsoptimering er aktiveret, uanset denne indstilling. | 2022 udgivelsesbølge 2 |
| Intern handel | Behovsplaner, der inkluderer planlagt downstream-efterspørgsel: *\#* | Denne funktion understøttes nu. Yderligere oplysninger finder du i [Planlægning af intern handel](Intercompany-planning.md) | Understøttet |
| Kanban | Varedisponeringsposter med ordreforslagstypen kanban: *\#* | Denne funktion afventer. Aktuelt vil varedisponering, der er angivet til kanban, blive ignoreret, når planlægningsoptimering er aktiveret. Kanban-ordreforslagstypen opretter en advarsel under varedisponeringen, og der oprettes indkøbsordreforslag for at dække det relaterede behov. | Fremtidig bølge |
| Kanban | Varer med standardordretypen kanban: *\#* | Aktuelt vil en standardordretype, der er angivet til kanban, blive ignoreret, når planlægningsoptimering er aktiveret. Kanban-standardordretypen opretter en advarsel under varedisponeringen, og der oprettes indkøbsordreforslag for at dække det relaterede behov. | Fremtidig bølge |
| Status for produktlivscyklus | Status for produktlivscyklus er ikke aktive for disponering: *\#* | Denne funktion understøttes nu. Du kan finde flere oplysninger under [Udelade produkter, der har specifikke statusser for produktlivscyklus](product-lifecycle-state.md) | Understøttet |
| Produktion | Styklistelinjer med afrunding eller flere opsætninger: *\#* | Denne funktion afventer. I øjeblikket ignoreres afrunding og flere opsætninger på styklistelinjer, når planlægningsoptimering er aktiveret, uanset denne indstilling. | Fremtidig bølge|
| Produktion | Stykliste/formellinjer med formelmåling: *\#* | Denne funktion afventer. I øjeblikket ignoreres formelmål på styklister og formellinjer, når planlægningsoptimering er aktiveret, uanset denne indstilling. | 2022 udgivelsesbølge 2 |
| Produktion | Stykliste/formellinjer med erstatningsvare (plangrupper): *\#* | Denne funktion afventer. I øjeblikket ignoreres erstatningsvare (plangrupper) på styklister og formellinjer, når planlægningsoptimering er aktiveret, uanset denne indstilling. | 2022 udgivelsesbølge 2 |
| Produktion | Stykliste/formellinjer med negativt antal: *\#* | Denne funktion afventer. Styklister og formellinjer, der har et negativt antal, medtages med et antal på 0 (nul), og der udstedes en advarsel, når planlægningsoptimering aktiveres. Opdater masterdata for at undgå advarsler. | 2022 udgivelsesbølge 2 |
| Produktion | Stykliste/formellinjer med ressourceforbrug: *\#* | Denne funktion afventer. I øjeblikket ignoreres styklister og formellinjer med ressourceforbrug, når planlægningsoptimering er aktiveret. Når denne funktion understøttes, vil materialebehovet blive angivet til startdatoen for produktionen. Før denne funktion understøttes, oprettes der ikke krav for materialer, der er markeret med et flag for ressourceforbrug. | 2022 udgivelsesbølge 2 |
| Produktion | Stykliste/formellinjer med trinforbrug: *\#* | Denne funktion afventer. I øjeblikket ignoreres trinforbrug på styklister og formellinjer, når planlægningsoptimering er aktiveret. | 2022 udgivelsesbølge 2 |
| Produktion | Styklister med konstant spild eller variabelt spild defineret: *\#* | Denne funktion afventer. I øjeblikket ignoreres konstant spild og variabelt spild, der defineres på styklister, når planlægningsoptimering er aktiveret. | 2022 udgivelsesbølge 2 |
| Produktion | Styklister med underleverandørarbejde: *\#* | Denne funktion understøttes nu. | Understøttet |
| Produktion | Styklister uden websted: *\#* | Denne funktion understøttes nu. Yderligere oplysninger finder du i [Produktionsplanlægning](production-planning.md) | Understøttet |
| Produktion | Efterspørgsel, der har defineret specifikke stykliste- eller rutekrav: *\#* | Denne funktion afventer. Aktuelt ignoreres de specifikke stykliste- eller rutekrav, der er defineret for efterspørgslen (f.eks. en understykliste eller en underrute på en salgsordre), når planlægningsoptimering aktiveres. Standardstyklisten eller -ruten anvendes, uanset denne indstilling. | 2022 udgivelsesbølge 2 |
| Produktion | Formelversioner med sam-/biprodukter: *\#* | Denne funktion afventer. I øjeblikket ignoreres samprodukter og biprodukter, der er tilknyttet formelversionen, når planlægningsoptimering aktiveres. | 2022 udgivelsesbølge 2 |
| Produktion | Formelversioner med udbytte: *\#* | Denne funktion afventer. I øjeblikket ignoreres udbytte, der er tilknyttet formelversionen, når planlægningsoptimering aktiveres. | 2022 udgivelsesbølge 2 |
| Produktion | Planer, som inkluderer rækkefølge: *\#* | Denne funktion afventer. I øjeblikket ignoreres rækkefølge, når planlægningsoptimering er aktiveret, uanset denne indstilling. | 2022 udgivelsesbølge 2 |
| Produktion | Frigivne produktionsordrer, der ikke er startet, hvor den planlagte start er tidligere end i dag: *\#* | Denne funktion afventer. Hvis en produktionsordre er forsinket, antager varedisponeringen i øjeblikket, at den fuldføres i dag. Dette er relevant for frigivne produktionsordrer, hvor en leveringsdato er passeret, men ikke er fuldført endnu. | Fremtidig bølge |
| Produktion | Ressourcer, der er planlagt med kapacitetsbegrænsning: *\#* | Denne funktion understøttes nu.| Understøttet |
| Produktion | Ruter, der bruges i planlægning: *\#* | Denne funktion understøttes. | Understøttet |
| Produktion | Reservation af salgslinje ved hjælp af udfoldning: *\#* | Salgslinjereservation, der bruger udfoldning, understøttes ikke, når planlægningsoptimering er aktiveret. | Fremtidig bølge |
| Produktion | Planlægning med udfoldning af produktionsordrer: *\#* | Planlægning, der bruger udfoldning af produktionsordrer, understøttes ikke, når planlægningsoptimering er aktiveret. Produktionsordrer kan planlægges individuelt. | Fremtidig bølge |
| Tilbudsanmodning | Behovsplaner med tilbudsanmodninger aktiveret: *\#* | Denne funktion afventer. På nuværende tidspunkt betragtes tilbudsanmodninger ikke som efterspørgsel, når planlægningsoptimering aktiveres. De ignoreres, uanset hvilken indstilling der er angivet. | 2022 udgivelsesbølge 2 |
| Rekvisitioner | Behovsplaner med rekvisitioner aktiveret: *\#* | Denne funktion understøttes nu. Du kan finde flere oplysninger under [Indkøbsrekvisitioner](purchase-requisitions.md) | Understøttet |
| Sikkerhedsmargener | Disponeringsgrupper med sikkerhedsmargen: *\#* | Denne funktion understøttes nu. Du kan finde flere oplysninger i [Sikkerhedsmargener](safety-margins.md) | Understøttet |
| Sikkerhedsmargener | Behovsplaner med sikkerhedsmargen: *\#* | Denne funktion understøttes nu. Du kan finde flere oplysninger i [Sikkerhedsmargener](safety-margins.md) |  Understøttet |
| Opfyldning af sikkerhedslager | Varedisponeringsposter med en anden "Opfyld minimum" end fra "Dags dato + fremskaffelsestid": *\#* | Planlægningsoptimering bruger altid *Dags dato + fremskaffelsestid*. Denne ændring er foretaget for at forberede en forenklet planlægningsopsætning i fremtiden og for at give et resultat, der kan handles ud fra. Hvis indkøbstiden ikke indgår i sikkerhedslageret, vil ordreforslag, der oprettes for den aktuelle begrænsede disponible lagerbeholdning, altid blive forsinket grundet leveringstiden. Denne funktionsmåde kan forårsage betydelige problemer og uønskede ordreforslag. Den bedste praksis er at ændre indstillingen, så *Dags dato + fremskaffelsestid* bruges. Opdater masterdata for at undgå advarsler. | I/T |
| Salgstilbud | Behovsplaner med salgstilbud aktiveret: *\#* | Denne funktion afventer. I øjeblikket ignoreres tilbud, når planlægningsoptimering er aktiveret. De ignoreres, uanset hvilken indstilling der er angivet. | 2022 udgivelsesbølge 2 eller senere |
| Hyldelevetid | Behovsplaner med hyldelevetid aktiveret: *\#* | Denne funktion afventer. | 2022 udgivelsesbølge 2 |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over planlægningsoptimering](planning-optimization-overview.md)

[Start her med planlægningsoptimering](get-started.md)

[Forskelle mellem klassisk behovsplanlægning og planlægningsoptimering](planning-optimization-differences-with-built-in.md)

[Parametre, der ikke bruges af planlægningsoptimering](not-used-parameters.md)

[Få vist planhistorik og planlægningslogfiler](plan-history-logs.md)

[Anvend filtre på en plan](plan-filters.md)

[Annullere et planlægningsjob](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
