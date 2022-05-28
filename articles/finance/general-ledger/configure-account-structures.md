---
title: Konfigurer kontostrukturer
description: Dette emne indeholder oplysninger om kontostrukturer og økonomiske dimensioner.
author: aprilolson
ms.date: 06/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c775703047f4d2ccf2b1c35e2810c015ee1c1506
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722598"
---
# <a name="configure-account-structures"></a>Konfigurer kontostrukturer

[!include[banner](../includes/banner.md)]

Kontostrukturer bruger hovedkontoen og økonomiske dimensioner til at oprette et sæt regler, der bestemmer den rækkefølge og de værdier, der bruges, når du angiver kontonummeret. Du kan oprette lige så mange kontostrukturer, som du har brug for til din virksomhed. Kontostrukturerne tildeles et firmas finansopsætning, så de kan deles.

Når du opretter en kontostruktur, er det maksimale antal segmenter 11. Hvis du har brug for flere segmenter end dette, skal du grundigt evaluere din opsætning og krav, som påvirker brugeroplevelsen. Overvej, om et segment kan udledes i forbindelse med rapportering ved hjælp af et hierarki i stedet for under dataindtastning eller ved at bruge et brugerdefineret felt. Hvis du f.eks. vil rapportere om placering, men du kan finde stedet ud fra afdeling eller bærer, behøver du ikke placering som en økonomisk dimension. Hvis du efter din vurdering finder ud af, at der skal bruges mere end 11 segmenter, kan du tilføje flere segmenter ved hjælp af avancerede regler.

Kontostrukturer kræver hovedkontoen. Hovedkontoen behøver ikke at være det første segment i strukturen, men den identificerer, hvilken kontostrukturen der er i brug under indtastningen af kontonummeret. Derfor kan en hovedkontoværdi kun findes i en struktur, der er knyttet til finans, så de ikke overlapper hinanden. Når kontostrukturen er identificeret, filtreres de tilladte værdier på listen for at sikre, at brugeren kun plukker de gyldige dimensionsværdier, så risikoen for en forkert kladdepostering reduceres.

> [!NOTE] 
> Hvis du planlægger at budgettere mod en økonomisk dimension, skal den være en del af en kontostruktur. Der anvendes ikke i øjeblikket avancerede regler ved budgettering.

## <a name="example"></a>Eksempel
For at illustrere den bedste fremgangsmåde for oprettelse af en kontostruktur vil vi antage, at en virksomhed ønsker at spore deres statuskonti (100000..399999) på økonomisk dimensionsniveau for konto og virksomhedsenheder. For indtægts- og udgiftskonti (400000..999999) sporer virksomheden økonomiske dimensioner for virksomhedsenhed, afdeling og bærer. Hvis de foretager et salg, vil de også gerne kunne spore kunden. I dette scenario kan det anbefales at have to kontostrukturer, der er tildelt til firmaets Finans - én til balancekonti og én til driftskonti. For at optimere brugeroplevelsen og validering skal kunden være en avanceret regel, der kun bruges, når der bruges en salgskonto.

**Statuskontostruktur**

|Hovedkonto          | Virksomhedsenhed    |
|----------------------|-----------|
|100000..399999 | *;” “|

**Driftskontostruktur**

|Hovedkonto          | Forretningsenhed    |Afdeling          | Bærer    | &nbsp; |
|----------------------|------------------|--------------------|-----------|---|
|400000..999999 | \*;” “| \*;” “| \*;” “| \*;” “|

**Avanceret regel for tilføjelse af en kunde**

Kriterium: Når Hovedkonto er mellem 400000 og 499999, skal du tilføje kunde. Feltet må ikke være tomt.

|Kunde         |
|-----------------|
|* |

I dette forenklede eksempel er alle værdier og tom felter tilladt, så * og " " bruges.

## <a name="segments-and-allowed-values"></a>Segmenter og tilladte værdier
Sektionen **Segmenter** og **Oplysninger om tilladt værdier** giver en gitterlignende oplevelse til angivelse af de regler, der skal anvendes ved validering under bogføringen. Kan du skrive direkte i cellerne i gitteret, importere dem fra Excel, eller du kan bruge sektionen **Oplysninger om tilladt værdi** som en vejledning til den.

Sektionen **Oplysninger om tilladt værdi** fører dig gennem oprettelsen af kriterier ved hjælp af **Operatorer** som begynder med, er mellem, omfatter og mange andre.

[![Tillad værdier.](./media/account.png)](./media/account.png) 

Tilladte værdier sættes som standard til en postside for en kladde eller en regnskabsfordeling, når der ikke er andre mulige værdier, der kan vælges i henhold til opsætningen af kontostrukturen.

Her er et eksempel på **Driftskontostruktur**.

|Hovedkonto          | Virksomhedsenhed    |Afdeling          | Bærer    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | 002 | 022 | 014 |

Når du angiver en kladde og vælger en konto i driftsområdet og afdeling '002', medfører det, at værdierne 022 og 014 er standard ved kontokontrol. Dette sker også med regnskabsfordelingssiden. 

## <a name="more-than-7-criteria-needed"></a>Der skal bruges mere end 7 kriterier

Hvis du skal bruge mere end 7 kriterier, kan du fortsætte med at tilføje dem på den næste linje. Du kan se, når du arbejder i sektionen **Oplysninger om tilladt værdi**, at kriteriet **+ Tilføj ny** ikke længere er aktivt, når det syvende kriterium er angivet. Det skyldes blandt andet: 
 - Kolonnebredde 
 - Hvordan dataene er gemt 
 - Udførelsen af kontrolelementet **Oplysninger om tilladt værdi**
 - Anvendelighed  
 
Hvis du vil fortsætte med at tilføje yderligere kriterier, skal du klikke på **Gentag i segmentet** og **Sektionen Tilladte værdier**. Kriterierne kopieres til en ny linje. Du kan derefter overskrive eller undlade at ændre sektionen **Oplysninger om tilladt værdi**.

## <a name="best-practices"></a>Bedste fremgangsmåder
Når du konfigurerer dine kontostrukturer, der er nogle bedste fremgangsmåder, som du kan følge. Dette er dog kun en vejledning, så en holistisk diskussion om din virksomhed, vækstplan og vedligeholdelsesplan bør indgå som en del af diskussionen.

- Placér hovedkontoen først eller så tæt på forsiden af kontostrukturen som muligt, så brugerne får den bedst mulige automatiserede oplevelse under kontoindtastningen.

- Genbrug kontostrukturer så meget som muligt for at reducere vedligeholdelsen på tværs af juridiske enheder.

- For variationer på tværs af juridiske enheder kan du overveje at bruge avancerede regler, så kontostrukturerne kan genbruges.

- Når du definerer tilladte værdier, skal du bruge afgrænsninger og jokertegn så meget som muligt. Dette giver dig ikke kun mulighed at udvide og ændre uden vedligeholdelse, men også systemet fungerer også mere ideelt med denne konfiguration.

- Du skal ikke bare indsætte en stjerne for hvert segment i kontostrukturen og derefter udelukkende stole på de avancerede regler. Dette vil være svært at administrere og vil ofte medføre brugerfejl under vedligeholdelsen, så systemet ikke kan bogføre værdierne.

## <a name="account-structure-activation"></a>Aktivering af kontostruktur
Når du er tilfreds med den nye konfiguration eller en ændring i en kontostruktur, skal du aktivere den. Hvis en kontostruktur tildeles til en finanskonto, kan denne aktivering være en længerevarende proces, fordi alle ikke-bogførte posteringer i systemet skal synkroniseres med den nye struktur. Bogførte posteringer berøres ikke af ændringer af kontostrukturen.

Du kan finde flere oplysninger under [Planlægge dine kontoplaner](plan-chart-of-accounts.md), [Økonomiske dimensioner](financial-dimensions.md) og [Angive kombinationer af konto og dimension (segmenteret adgangsstyring)](enter-account-dimension-combinations-segmented-entry-control.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
