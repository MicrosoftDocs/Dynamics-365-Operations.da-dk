---
title: Analyse af om Planlægningsoptimering passer til
description: Dette emne beskriver, hvordan du kan kontrollere den aktuelle opsætning og de nuværende data i forhold til funktionerne i funktionen Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 769bd84b4ba23c9de4638df9186381936221414a
ms.sourcegitcommit: ae04c7cb48f7ecafe71bbe77a0f97715e6290991
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973446"
---
# <a name="planning-optimization-fit-analysis"></a>Analyse af tilpasning af planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Du skal analysere resultatet fra planlægningsoptimeringen og tilpasse analysen som en del af migreringsprocessen. Bemærk, at omfanget af planlægningsoptimering ikke er lig med den aktuelle indbyggede funktionalitet for varedisponering. Det anbefales, at du samarbejder med partneren og læser dokumentationen for at forberede migreringen. 

Tilpasset analyse af planlægningsoptimering hjælper dig med at identificere, hvor resultatet kan være anderledes mellem det indbyggede varedisponeringsprogram og planlægningsoptimering. Denne analyse foretages på basis af den aktuelle opsætning og dine data. 

Hvis du vil have vist analyseresultatet for tilpasning af planlægningsoptimering, skal du gå til **Varedisponering** \> **Konfiguration** \> **Analyse af tilpasning af planlægningsoptimering** og derefter vælge **Kør analyse**. Hvis analysen finder nogen uoverensstemmelser, vises de på samme side. (Det kan tage et par minutter at køre analysen).

> [!NOTE]
> Hvis der findes uoverensstemmelser, kan du stadig bruge Planlægningsoptimering. Resultaterne af tilpasningsanalysen viser kun de steder, hvor planlægningstjenesten ikke kan overholde din aktuelle opsætning. Det vil sige, at det vises de steder, hvor nogle processer muligvis bliver ignoreret eller ikke understøttes.

## <a name="analysis-results-example-1"></a>Analyseresultater: eksempel 1

- **Funktion:** Produktion
- **Problem:** Varer med et styklisteniveau større end nul: 56
- **Forklaring:** Tilpasningsanalysen fandt 56 varer, der har en styklisteopsætning til produktion. Da den aktuelle version af funktionen Planlægningsoptimering ikke understøtter produktion, vil Planlægningsoptimering oprette indkøbsordreforslag i stedet for produktionsordreforslag. Der vises også en advarsel om, at de berørte varer vises.

## <a name="analysis-results-example-2"></a>Analyseresultater: eksempel 2

- **Funktion:** Handlinger
- **Afgang:** Disponeringsgrupper med aktiveret handlingsberegning: 6
- **Forklaring:** Tilpasningsanalysen fandt seks disponeringsgrupper, hvor handlingsberegningen er aktiveret. Da den aktuelle version af Planlægningsoptimerings ikke understøtter handlinger, vil der ikke blive genereret handlinger ved varedisponering.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Oversigt over mulige resultater fra tilpasningsanalysen

Følgende tabel viser de forskellige resultater, der kan vises efter en tilpasningsanalyse. Nummertegn (_\#_) erstattes med et tal, der angiver antallet af poster, der har den viste fejl.

| Funktion | Vist problem | Forklaring | Forventet tilgængelighed |
| --- | --- | --- | --- |
| Handlinger | Disponeringsgrupper med handlingsberegning aktiveret: _\#_ | Denne funktion afventer. Aktuelt oprettes handlinger ikke under varedisponering, når planlægningsoptimering er aktiveret, uanset denne indstilling. Hovedformålet med handlinger er at foreslå ændringer af eksisterende ordrer. Vurder, om handlinger anvendes aktivt som en del af dine forretningsprocesser, eller om forsinkelsesoplysningerne for ordrerne er tilstrækkelige. | 2021. oktober |
| Basiskalendere | Kalendere, der bruger basiskalender: _\#_ | Denne funktion afventer. Basiskalenderen ignoreres i øjeblikket, når planlægningsoptimering er aktiveret. Vurder, om basiskalenderen skal bruges til dine forretningsprocesser, eller om direkte opsætning i kalendere er tilstrækkelig. | 2021. april | 
| Batchdispositionskoder | Ikke-tilgængelige batchdispositionsmaster: _\#_ | Denne funktion afventer. I øjeblikket ignoreres batchdispositionskoder, når planlægningsoptimering er aktiveret. | 2021. oktober |
| Leveringsevne (LE) | Standardindstillinger for ordre med leveringsdatokontrollen angivet til LE: _\#_ | Denne funktion afventer. I øjeblikket ignoreres LE, når planlægningsoptimering er aktiveret, uanset denne indstilling. | 2021. oktober |
| Kopiér statisk til dynamisk plan | Kopi af statisk til dynamisk plan er aktiveret på varedisponeringsparametrene. | Planlægningsoptimering kopierer ikke den statiske plan til den dynamiske plan, uanset denne indstilling. Generelt er dette koncept ikke så relevant på grund af hastigheden og den fuldstændige genopretning, som planlægningsoptimering giver. Hvis der bruges to eller flere planer, skal varedisponeringen udløses for hver enkelt plan. | 2021. oktober |
| Autorisation | Disponeringsgrupper med automatisk autorisationstidshorisont angivet: _\#_ | I version 10.0.7 og nyere understøttes autorisation som et separat autorisationsbatchjob, efter at varedisponering er fuldført (hvis funktionen _Automatisk autorisation med planlægningsoptimering_ er blevet aktiveret i [funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Bemærk, at automatisk autorisation med planlægningsoptimering er baseret på ordredatoen (startdato), og ikke behovsdatoen (slutdato). Denne funktionsmåde sikrer, at der sker en rettidig autorisation af ordreforslag, uden at leveringstiden i autorisationstidshorisonten skal medtages. | Understøttet |
| Autorisation | Varedisponeringsposter med automatisk autorisation angivet: _\#_ | I version 10.0.7 og nyere understøttes automatisk autorisation som et separat autorisationsbatchjob, efter at varedisponering er fuldført (hvis funktionen _Automatisk autorisation med planlægningsoptimering_ er blevet aktiveret i [funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Bemærk, at automatisk autorisation med planlægningsoptimering er baseret på ordredatoen (startdato), og ikke behovsdatoen (slutdato). Denne funktionsmåde sikrer, at der sker en rettidig autorisation af ordreforslag, uden at leveringstiden i autorisationstidshorisonten skal medtages. | Understøttet |
| Autorisation | Behovsplaner med automatisk autorisation angivet: _\#_ | I version 10.0.7 og nyere understøttes automatisk autorisation som et separat autorisationsbatchjob, efter at varedisponering er fuldført (hvis funktionen _Automatisk autorisation med planlægningsoptimering_ er blevet aktiveret i [funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Bemærk, at automatisk autorisation med planlægningsoptimering er baseret på ordredatoen (startdato), og ikke behovsdatoen (slutdato). Denne funktionsmåde sikrer, at der sker en rettidig autorisation af ordreforslag, uden at leveringstiden i autorisationstidshorisonten skal medtages. | Understøttet |
| FitAnalysisPlanningItems | Planlægningsvarer: _\#_ | Denne funktion afventer. I øjeblikket håndteres planlægningsvarer som almindelige varer, når planlægningsoptimering er aktiveret. | 2021. oktober |
| Prognose | Disponeringsgrupper med "Medtag interne ordrer" aktiveret: _\#_ | Denne funktion afventer. Aktuelt medtager varedisponering ikke downstream-planlagt behov, når planlægningsoptimering er aktiveret, uanset denne indstilling. Bemærk, at frigivne/autoriserede ordrer stadig fungerer sammen med den almindelige interne funktion og vil omfatte de fleste scenarier. | 2020. oktober |
| Prognose | Disponeringsgrupper med indstillingen "Reducer prognose med" indstillet til en anden værdi end "Ordrer": _\#_ | Planlægningsoptimering bruger som standard "Reducer prognose med" for ordrer, uanset denne indstilling. | November 2020 |
| Prognose | Budgetmodeller med undermodeller: _\#_ | Denne funktion afventer. Aktuelt er budgetter, der bruger undermodeller, ikke understøttet, når planlægningsoptimering er aktiveret. De ignoreres, uanset hvilken indstilling der er angivet. | 2021. april |
| Prognose | Behovsplaner med "Medtag forsyningsprognose" aktiveret: _\#_ | Denne funktion afventer. Aktuelt er forsyningsprognoser ikke understøttet, når planlægningsoptimering er aktiveret. De ignoreres, uanset hvilken indstilling der er angivet. | 2021. oktober |
| Låsningstidshorisont | Disponeringsgrupper med låsningstidshorisont angivet: _\#_ | Låsningstidshorisont bruges ofte ikke, og der er i øjeblikket ingen planer om at medtage den i planlægningsoptimering. I øjeblikket ignoreres opsætningen af låsningstidshorisont, når planlægningsoptimering er aktiveret, uanset denne indstilling. | I/T |
| Låsningstidshorisont | Varedisponeringsposter med låsningstidshorisont angivet: _\#_ | Låsningstidshorisont bruges ofte ikke, og der er i øjeblikket ingen planer om at medtage den i planlægningsoptimering. I øjeblikket ignoreres opsætningen af låsningstidshorisont, når planlægningsoptimering er aktiveret, uanset denne indstilling. | I/T |
| Låsningstidshorisont | Behovsplaner med låsningstidshorisont angivet: _\#_ | Låsningstidshorisont bruges ofte ikke, og der er i øjeblikket ingen planer om at medtage den i planlægningsoptimering. I øjeblikket ignoreres opsætningen af låsningstidshorisont, når planlægningsoptimering er aktiveret, uanset denne indstilling. | I/T |
| Intern handel | Behovsplaner, der inkluderer planlagt downstream-efterspørgsel: _\#_ | Denne funktion afventer. Aktuelt medtager varedisponering ikke downstream-planlagt behov, når planlægningsoptimering er aktiveret, uanset denne indstilling. Bemærk, at frigivne/autoriserede ordrer stadig fungerer sammen med den normale interne funktion og vil omfatte de fleste scenarier. | 2020. oktober |
| Kanban | Varedisponeringsposter med ordreforslagstypen kanban: _\#_ | Denne funktion afventer. Aktuelt vil varedisponering, der er angivet til kanban, blive ignoreret, når planlægningsoptimering er aktiveret. Kanban-ordreforslagstypen opretter en advarsel under varedisponeringen, og der oprettes indkøbsordreforslag for at dække det relaterede behov. | 2021. oktober |
| Kanban | Varer med standardordretypen kanban: _\#_ | Aktuelt vil en standardordretype, der er angivet til kanban, blive ignoreret, når planlægningsoptimering er aktiveret. Kanban-standardordretypen opretter en advarsel under varedisponeringen, og der oprettes indkøbsordreforslag for at dække det relaterede behov. | 2021. oktober |
| Status for produktlivscyklus   | Produktlivscyklustilstande er ikke aktive for disponering: _\#_ | Dette er en afventende funktion. Produktlivscyklustilstanden ignoreres i øjeblikket med Planlægningsoptimering aktiveret. Du kan justere produktfilteret på planlægningsniveau for at undgå at medtage produkter, hvor produktlivscyklustilstanden er deaktiveret for planlægning. | November 2020 |
| Produktion | Styklistelinjer med afrunding eller flere opsætninger: _\#_ | Denne funktion afventer. I øjeblikket ignoreres afrunding og flere opsætninger på styklistelinjer, når planlægningsoptimering er aktiveret, uanset denne indstilling. | 2021. april |
| Produktion | Stykliste/formellinjer med formelmåling: _\#_ | Denne funktion afventer. I øjeblikket ignoreres formelmål på styklister og formellinjer, når planlægningsoptimering er aktiveret, uanset denne indstilling. | 2021. oktober |
| Produktion | Stykliste/formellinjer med erstatningsvare (plangrupper): _\#_ | Denne funktion afventer. I øjeblikket ignoreres erstatningsvare (plangrupper) på styklister og formellinjer, når planlægningsoptimering er aktiveret, uanset denne indstilling. | 2021. oktober |
| Produktion | Stykliste/formellinjer med negativt antal: _\#_ | Denne funktion afventer. Styklister og formellinjer, der har et negativt antal, medtages med et antal på 0 (nul), og der udstedes en advarsel, når planlægningsoptimering aktiveres. Opdater masterdata for at undgå advarsler. | 2021. oktober |
| Produktion | Stykliste/formellinjer med ressourceforbrug: _\#_ | Denne funktion afventer. I øjeblikket ignoreres styklister og formellinjer med ressourceforbrug, når planlægningsoptimering er aktiveret. Når denne funktion understøttes, vil materialebehovet blive angivet til startdatoen for produktionen. Før denne funktion understøttes, oprettes der ikke krav for materialer, der er markeret med et flag for ressourceforbrug. | 2021. april |
| Produktion | Stykliste/formellinjer med trinforbrug: _\#_ | Denne funktion afventer. I øjeblikket ignoreres trinforbrug på styklister og formellinjer, når planlægningsoptimering er aktiveret. | 2021. oktober |
| Produktion | Styklister med konstant spild eller variabelt spild defineret: _\#_ | Denne funktion afventer. I øjeblikket ignoreres konstant spild og variabelt spild, der defineres på styklister, når planlægningsoptimering er aktiveret. | 2021. oktober |
| Produktion | Styklister med underleverandørarbejde: _\#_ | Denne funktion afventer. I øjeblikket ignoreres opsætningen af underleverandørarbejde på styklister, når planlægningsoptimering er aktiveret, uanset denne indstilling. | 2021. oktober |
| Produktion | Styklister uden websted: _\#_ | Denne funktion afventer. I øjeblikket ignoreres styklister uden websted, når planlægningsoptimering er aktiveret. | 2020. oktober |
| Produktion | Efterspørgsel, der har defineret specifikke stykliste- eller rutekrav: _\#_ | Denne funktion afventer. Aktuelt ignoreres de specifikke stykliste- eller rutekrav, der er defineret for efterspørgslen (f.eks. en understykliste eller en underrute på en salgsordre), når planlægningsoptimering aktiveres. Standardstyklisten eller -ruten anvendes, uanset denne indstilling. | 2021. oktober |
| Produktion | Formelversioner med sam-/biprodukter: _\#_ | Denne funktion afventer. I øjeblikket ignoreres samprodukter og biprodukter, der er tilknyttet formelversionen, når planlægningsoptimering aktiveres. | 2021. oktober |
| Produktion | Formelversioner med udbytte: _\#_ | Denne funktion afventer. I øjeblikket ignoreres udbytte, der er tilknyttet formelversionen, når planlægningsoptimering aktiveres. | 2021. oktober |
| Produktion | Planer, som inkluderer rækkefølge: _\#_ | Denne funktion afventer. I øjeblikket ignoreres rækkefølge, når planlægningsoptimering er aktiveret, uanset denne indstilling. | 2021. oktober |
| Produktion | Frigivne produktionsordrer, der ikke er startet, hvor den planlagte start er tidligere end i dag: _\#_ | Denne funktion afventer. Hvis en produktionsordre er forsinket, antager varedisponeringen i øjeblikket, at den fuldføres i dag. Dette er relevant for frigivne produktionsordrer, hvor en leveringsdato er passeret, men ikke er fuldført endnu. | 2021. oktober |
| Produktion | Ressourcer, der er planlagt med kapacitetsbegrænsning: _\#_ | Denne funktion afventer. I øjeblikket ignoreres ressourcer, der er planlagt med kapacitetsbegrænsning, når planlægningsoptimering er aktiveret. Planlægningen udføres på basis af standardleveringstiden fra produktet. | 2021. april |
| Produktion | Ruter, der bruges i planlægning: _\#_ | Denne funktion afventer. I øjeblikket ignoreres ruter, når planlægningsoptimering er aktiveret. Standardleveringstiden for produktet bruges. | 2021. april |
| Produktion | Reservation af salgslinje ved hjælp af udfoldning: _\#_ | Salgslinjereservation, der bruger udfoldning, understøttes ikke, når planlægningsoptimering er aktiveret. | 2021. oktober |
| Produktion | Planlægning med udfoldning af produktionsordrer: _\#_ | Planlægning, der bruger udfoldning af produktionsordrer, understøttes ikke, når planlægningsoptimering er aktiveret. Produktionsordrer kan planlægges individuelt. | 2021. oktober |
| Tilbudsanmodning | Behovsplaner med tilbudsanmodninger aktiveret: _\#_ | Denne funktion afventer. På nuværende tidspunkt betragtes tilbudsanmodninger ikke som efterspørgsel, når planlægningsoptimering aktiveres. De ignoreres, uanset hvilken indstilling der er angivet. | 2021. oktober |
| Rekvisitioner | Behovsplaner med rekvisitioner aktiveret: _\#_ | Denne funktion afventer. I øjeblikket ignoreres rekvisitioner, når planlægningsoptimering er aktiveret. De ignoreres, uanset hvilken indstilling der er angivet. | 2021. oktober |
| Sikkerhedsmargener | Disponeringsgrupper med sikkerhedsmargen: _\#_ | Denne funktion afventer. Sikkerhedsmargen ignoreres i øjeblikket, når planlægningsoptimering er aktiveret. Hvis du vil kompensere for denne funktionsmåde, kan du øge leveringstiden, så den omfatter sikkerhedsmargenen. | 2020. oktober |
| Sikkerhedsmargener | Behovsplaner med sikkerhedsmargen: _\#_ | Denne funktion afventer. I øjeblikket ignoreres sikkerhedsmargen, når planlægningsoptimering er aktiveret, uanset denne indstilling. Hvis du vil kompensere for denne funktionsmåde, kan du øge leveringstiden, så den omfatter sikkerhedsmargenen. | 2020. oktober |
| Opfyldning af sikkerhedslager | Varedisponeringsposter med en anden "Opfyld minimum" end fra "Dags dato + fremskaffelsestid": _\#_ | Planlægningsoptimering bruger altid *Dags dato + fremskaffelsestid*. Denne ændring er foretaget for at forberede en forenklet planlægningsopsætning i fremtiden og for at give et resultat, der kan handles ud fra. Hvis indkøbstiden ikke indgår i sikkerhedslageret, vil ordreforslag, der oprettes for den aktuelle begrænsede disponible lagerbeholdning, altid blive forsinket grundet leveringstiden. Denne funktionsmåde kan forårsage betydelige problemer og uønskede ordreforslag. Den bedste praksis er at ændre indstillingen, så *Dags dato + fremskaffelsestid* bruges. Opdater masterdata for at undgå advarsler. | I/T |
| Salgstilbud | Behovsplaner med salgstilbud aktiveret: _\#_ | Denne funktion afventer. I øjeblikket ignoreres tilbud, når planlægningsoptimering er aktiveret. De ignoreres, uanset hvilken indstilling der er angivet. | 2021. oktober |
| Hyldelevetid | Behovsplaner med hyldelevetid aktiveret: _\#_ | Denne funktion afventer. I øjeblikket ignoreres hyldelevetid, når planlægningsoptimering er aktiveret, uanset denne indstilling. | 2021. oktober |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over planlægningsoptimering](planning-optimization-overview.md)

[Kom i gang med planlægningsoptimering](get-started.md)

[Få vist planhistorik og planlægningslogs](plan-history-logs.md)

[Anvend filtre på en plan](plan-filters.md)

[Annullere et planlægningsjob](cancel-planning-job.md)
