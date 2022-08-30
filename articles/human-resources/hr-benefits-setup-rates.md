---
title: Konfigurere satser
description: Satser i Microsoft Dynamics 365 Human Resources definerer, hvor meget arbejdsgivere og medarbejdere bidrager med til et frynsegode.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 37fb24bdda1d49291b88c6728e11aecf9863cc66
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324811"
---
# <a name="configure-rates"></a>Konfigurere satser

Satser definerer, hvor meget arbejdsgivere og medarbejdere bidrager med til et frynsegode. Værdien kan enten være et beløb eller et antal flekskreditter, afhængigt af konfigurationen.

Brug satser til at bestemme, hvor meget medarbejdere og arbejdsgiver betaler for hvert enkelt frynsegode baseret på flere faktorer. Dækningssatser gælder for datoer, så du kan bevare en historisk oversigt over satser. 

## <a name="set-up-rates"></a>Konfigurere satser

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Satser** under **Konfiguration**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Kurs** | Et entydigt navn, der identificerer frynsegodesatsen. |
   | **Beskrivelse** | En beskrivelse af frynsegodesatsen. |
   | **Gyldig fra** | Den dato, hvor satsen træder i kraft. Den aktuelle systemdato er standardværdien. Denne dato skal være på eller før frynsegodeperioden. Det er god praksis at angive denne dato til datoen for frynsegodeplanen. |
   | **Udløb** | Satsens slutdato. 31-12-2154 (som repræsenterer aldrig) er standardværdien. |
   | **Brug lag** |  Brug dette felt, hvis du har logik, der skal bruges til bestemmelse af en sats. Hvis en sats f.eks. skal stige på baggrund af alder, skal du vælge en værdi her. Vælg **Enkelt niveau** for én frynsegodesats med enkelt niveau eller **Dobbeltniveau** for en frynsegodesats med to niveauer. Et eksempel på et dobbeltniveau er et niveau, der er baseret på køn og alder. Når du har valgt en værdi, skal du vælge **Handlinger** og derefter vælge **Niveausatser**. Hvis du har en flad sats, der ikke ændres, skal du lade dette felt være tomt. |
   | **Betalingshyppighed** | Angiv, hvor ofte frynsegodetillægssatsen skal udbetales til frynsegodeudbyderen. De satser, du angiver på den side, der beskrives senere i denne artikel, bliver baseret på den betalingsfrekvens, som du angiver her. Hvis du f.eks. angiver **Månedlig** i dette felt og angiver en medarbejdersats på **$100**, antages det, at frynsegodet vil koste medarbejderen $100 pr. måned. En medarbejder kan dog blive betalt to gange om måneden på baggrund af den betalingsfrekvens for frynsegodet, som er angivet i medarbejderposten. Når medarbejderen i dette tilfælde logger på **medarbejderens selvbetjening**, vil det beløb, de betaler, være $50, fordi den sats, som **medarbejderens selvbetjening** viser, er baseret på medarbejderens betalingsfrekvens. |
   | **Afrunding af lønfrekvenssats** | Der findes følgende metoder til afrunding af satser: Standard, Afkortet, Normal, Nedad og Oprunding. </br></br><ul><li>**Standard** – Rund altid op. 10,611 afrundes for eksempel til 10,62. -10,231 afrundes til -10,23. </li><li>**Afkortet** – Rund altid ned. 10,619 afrundes for eksempel til 10,61. -10,231 afrundes til -10,24. </li><li>**Normal** – Decimalværdier, der slutter på eller er større end 5, afrundes fra nul. Decimalværdier, der slutter på eller er mindre end 4, afrundes mod nul. 10,615 afrundes for eksempel til 10,62. -10,235 afrundes til -10,24. 10,614 afrundes til 10,61. -10,234 afrundes til -10,23. </li><li>**Nedad** – Afrund mod nul. 10,619 afrundes for eksempel til 10,61. -10,231 afrundes til -10,23. </li><li>**Oprunding** – Afrund væk fra nul. 10,619 afrundes for eksempel til 10,62. -10,231 afrundes til -10,24. |
   | **Medarbejderbeløb for ikke-ryger** | Det beløb, som frynsegodeudbyderen fakturerer for en medarbejder, der ikke ryger. Det er det beløb, som arbejdsgiveren betaler til frynsegodeudbyderen og bør baseres på betalingsfrekvensen for satsopsætningen. |
   | **Arbejdsgiverbeløb for ikke-ryger** | Det beløb, som frynsegodeudbyderen fakturerer for en medarbejder, der ikke ryger. Det er det beløb, som arbejdsgiveren betaler til frynsegodeudbyderen, og det bør baseres på betalingsfrekvensen for satsopsætningen. |
   | **Medarbejderbeløb for ryger** | Det beløb, som frynsegodeudbyderen fakturerer for en medarbejder, der ryger. Det er det beløb, som arbejdsgiveren betaler til frynsegodeudbyderen og bør baseres på betalingsfrekvensen for satsopsætningen. |
   | **Arbejdsgiverbeløb for ryger** | Det beløb, som frynsegodeudbyderen fakturerer for en medarbejder, der ryger. Det er det beløb, som arbejdsgiveren betaler til frynsegodeudbyderen og bør baseres på betalingsfrekvensen for satsopsætningen. |
   | **Administrativt beløb** | Det administrationsbeløb, som en tredjepartsadministrator opkræver. Det er det beløb, som arbejdsgiveren betaler til tredjepartsadministratoren, og det bør baseres på betalingsfrekvensen for satsopsætningen. |
   | **Sats for fleksibel kredit** | Det antal flekskreditter, som frynsegoderne koster. Dette gælder kun for satser, der er oprettet for frynsegodeplaner, som er tilknyttet flekskreditprogrammer. Hvis du bruger niveausatser, defineres flekskreditter i Handlinger > Niveausatser. |
   | **Skift ikrafttrædelsesdato** | Den dato, hvor ændringen af frynsegodesatsen træder i kraft. Systemet vil automatisk ændre frynsegodesatsen og opdatere alle de frynsegodeplaner, der er tilknyttet denne sats, forudsat du behandler opdatering af satsændring. Du må ikke angive denne dato, medmindre systemet automatisk skal opdatere medarbejdernes frynsegodeplaner baseret på denne sats. Dette er normalt reserveret til automatisk behandling af fremtidige satsændringer. **Ændringens ikrafttrædelsesdato** skal ligge inden for frynsegodesatsens gyldigheds- og udløbsdato. |
   | **Satsændring fuldført** | Afkrydsningsfeltet **Ændret sats er fuldført** markeres automatisk, når ændringen af frynsegodesatsen er fuldført af fradrag af behandlingen af opdatering af ændret sats. |

4. Hvis du vil spore og vedligeholde ændringer af opsætningen af frynsegodesatsen, skal du vælge **Handlinger** og derefter vælge **Vedligehold versioner**.

5. Vælg **Gem**. 

## <a name="set-up-tier-rates"></a>Konfigurere niveausatser

Du kan bruge niveausatser i din satsopsætning, hvis satsen varierer, afhængigt af forskellige faktorer. Du kan f.eks. konfigurere niveausatser for at angive, at hvis alderen er op til 34,99, er beløbet for en ikke-ryger 2. Hvis alderen er op til 39,99, er beløbet for en ikke-ryger 3.

Du kan også bruge dobbelte niveauer. Hvis du vælger **Dobbelt niveau** for værdien for **Brug niveauer** i formularen **Satsopsætning**, kan du definere satser baseret på to dimensioner. Du kan f.eks. konfigurere et system for dobbeltniveau for at angive, at hvis du er en mand, og din alder er op til 34,99, er beløbet for en ikke-ryger 2. Hvis du er en mand, og din alder er op til 39,99, er beløbet for en ikke-ryger 3. Hvis du er en kvinde, og din alder er op til 34,99, er beløbet for en ikke-ryger 1,8. Hvis du er en kvinde, og din alder er op til 39,99, er beløbet for en ikke-ryger 2,8.

> [!IMPORTANT]
> En indstilling under **Personlige oplysninger** i arbejderposten bruges til at angive, om medarbejderen er ryger. Hvis medarbejderen registreres som ryger, anvendes rygersatsen. (Rygerangivelsen kan aldrig ses af medarbejderen).
   
1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Satser** under **Konfiguration**.

2. Vælg en eller flere satser på listen, vælg **Handlinger**, og vælg derefter **Niveausatser**.

3. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivende tekst |
   | --- | --- | 
   | **Beskrivelse** | Værdien i feltet **Beskrivelse** anvendes fra beskrivelsen i posten for satsopsætningen. Dette hjælper dig med at identificere, hvilken satsopsætning niveausatserne er knyttet til. |
   | **Lagkode** | Vælg en niveaukode. Niveaukoder defineres i siden **Niveaukoder**. Systemet vil automatisk vise beskrivelsen af niveaukoden i gitteret til venstre. |
   | **Lagtype** | Angiver, hvilket felt der skal bruges som valgkriterie for processen til beregning af niveausatsen. F.eks.:</br></br><ul><li>Hvis der bruges **Alder**, vil systemet bruge medarbejderens fødselsdato til at behandle beregningen af frynsegodesatsen.</li><li>Hvis der bruges **Løn**, vil systemet bruge medarbejderens årlige frynsegodeløn i processen for beregning af frynsegodesatsen.</li><li>Hvis der bruges **Jobtype**, vil systemet bruge medarbejderens aktuelle aktive stillingspost til at bestemme jobtypen, afhængigt af den post der er knyttet til stillingen.</li></ul></br></br>Niveautyperne er **Alder**, **Løn**, **Fysisk**, **Køn**, **Fuldtidsækvivalent**, **Jobtype**, **Kompensationsområde** og **Niveau**. | 
   | **Niveau** | Den værdi, der skal bruges sammen med niveautypen i processen til beregning af frynsegodesats. F.eks.:</br></br><ul><li>Hvis niveautypen er **Alder**, er dette aldersværdien.</li><li>Hvis niveautypen er **Løn**, er dette lønbeløbet.</li><li> Hvis niveautypen er **Jobtype**, er dette jobtypen.</li></ul></br></br>Med niveautypen **Alder** eller **Løn** repræsenterer værdien i feltet **Niveau** den nedre grænse for niveauet. Hvis niveauet er **Jobtype**, bruger systemet en tilgang med et nøjagtig match under valg af niveausats. |
   | **Kalkulationstype** | Angiver, hvordan beløbet i feltet med beregningsbeløb skal bruges, og hvilken matematisk beregning der skal udføres, hvis det er nødvendigt. Hvis beregningstypen er et fladt beløb, bruger systemet beløbsfelterne, som de er. Hvis beregningstypen er pr. $ løn- eller dækningsbeløb, bruger systemet beregningsbeløbet og beregningsretning i beregningen af matematiske beregninger.</br></br>Hvis beregningstypen er pr. $ lønbeløb, bruger systemet følgende matematiske ligning:</br></br>Årlig frynsegodeløn divideret med beregningsbeløb (rundet op eller ned) gange beløbene for rygere eller ikke-rygere for medarbejder eller arbejdsgiver.</br></br>Hvis beregningstypen er pr. $ lønbeløb, bruger systemet følgende matematiske ligning:</br></br>Dækningsbeløb divideret med beregningsbeløb (rundet op eller ned) gange beløbene for rygere eller ikke-rygere for medarbejder eller arbejdsgiver.</br></br>I begge beregninger bruges beregningsretning til at bestemme, om det årlige frynsegode- eller dækningsbeløb, der er divideret med beregningsbeløbet, skal rundes op eller ned. |
   | **Beregningsbeløb** | Det beløb, der skal bruges under processen til beregning af frynsegodesatsen. Dette beløb vil være divisoren under den matematiske beregning af niveausatsen. |
   | **Beregningsretning** | Den retning, som det beregnede resultatbeløb skal afrundes til. Systemet understøtter tre beregningsretninger: Tom (nøjagtig metode), **Forøg** og **Formindsk**.</br></br><ul><li>Hvis feltet ikke udfyldes, vil systemet bruge den nøjagtige beregning af løn-/dækningsbeløbet divideret med beregningsbeløbet. Hvis denne værdi har en brøkdel, vil systemet bruge dette i beregningen.</li><li>Hvis **Forøg** er valgt, vil systemet øge den matematiske beregning af løn-/dækningsbeløbet divideret med beregningsbeløbet til det nærmeste heltal, hvilket betyder, at 12,25 vil stige til 13.</li><li>Hvis **Formindsk** er valgt, vil systemet formindske den matematiske beregning af løn-/dækningsbeløbet divideret med beregningsbeløbet til det aktuelle heltal, hvilket betyder, at 12,25 vil formindskes til 12.</li></ul> |
   | **Medarbejderbeløb for ikke-ryger** | Det beløb, som en frynsegodeudbyder fakturerer for en medarbejder, der ikke ryger. Det er det beløb, som arbejdsgiveren betaler til frynsegodeudbyderen, og det bør baseres på betalingsfrekvensen for satsopsætningen. |
   | **Arbejdsgiverbeløb for ikke-ryger** | Det beløb, som en frynsegodeudbyder fakturerer for en medarbejder, der ikke ryger. Det er det beløb, som arbejdsgiveren betaler til frynsegodeudbyderen, og det bør baseres på betalingsfrekvensen for satsopsætningen. |
   | **Medarbejderbeløb for ryger** | Det beløb, som en frynsegodeudbyder fakturerer for en medarbejder, der ikke ryger. Det er det beløb, som arbejdsgiveren betaler til frynsegodeudbyderen, og det bør baseres på betalingsfrekvensen for satsopsætningen. |
   | **Arbejdsgiverbeløb for ryger** | Det beløb, som en frynsegodeudbyder fakturerer for en medarbejder, der ikke ryger. Det er det beløb, som arbejdsgiveren betaler til frynsegodeudbyderen, og det bør baseres på betalingsfrekvensen for satsopsætningen. |
   | **Administrativt beløb** | Det administrationsbeløb, som en tredjepartsadministrator opkræver. Det er det beløb, som arbejdsgiveren betaler til tredjepartsadministratoren, og det bør baseres på betalingsfrekvensen for satsopsætningen. |
   | **Flekskreditsats for ikke-ryger** | Antallet af flekskreditter, som frynsegodet koster, baseret på den beregning, der er defineret for niveauet for ikke-rygere. Hvis beregningstypen f.eks. er **Pr. $ dækningsbeløbet**, er beregningsbeløbet 10.000, og flekskreditsatsen for ikke-rygere er 6, dvs. at hvis en medarbejder, der er ikke-ryger, vælger en dækning på $10.000, vil det koste 6 flekskreditter. Hvis de vælger en dækning på $20.000, koster det 12 flekskreditter osv. |
   | **Flekskreditsats for rygere** | Antallet af flekskreditter, som frynsegodet koster, baseret på den beregning, der er defineret for niveauet for rygere. |

5. Vælg **Gem**. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
