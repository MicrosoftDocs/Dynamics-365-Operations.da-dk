---
title: Konfigurere berettigelsesregler og -indstillinger
description: Angiv berettigelsesregler og -indstillinger i Frynsegodeadministration i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 70054acafc3aec35fd985c0ca81e928519ddd0a3
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430664"
---
# <a name="configure-eligibility-rules-and-options"></a>Konfigurere berettigelsesregler og -indstillinger

Når du har konfigureret de nødvendige parametre for Frynsegodeadministration i Microsoft Dynamics 365 Human Resources, kan du oprette berettigelsesregler, bundter, perioder og programmer, som du vil knytte til dine frynsegodeplaner.

## <a name="create-an-eligibility-rule"></a>Oprette en berettigelsesregel

Berettigelsesregler definerer, hvilke medarbejdere der kan tilmelde sig de enkelte frynsegodeplaner. Når du har defineret berettigelsesregler, kan du tildele dem til frynsegodeplaner. Derefter kan du behandle tilmeldingsberettigelse for at se, hvilke medarbejdere der er berettiget til de enkelte planer. 

Under åben tilmelding kan medarbejdere vælge frynsegodeplaner. Hvis de bliver ikke-berettiget til en frynsegodeplan på baggrund af berettigelsesregler, efter at de allerede er tilmeldt, afmeldes de ikke automatisk. Når der opstår en livshændelse, der påvirker berettigelse til en plan, startes der typisk en tilmeldingsperiode, hvor medarbejderen kan vælge planer, som de er berettiget til. 

1. Vælg **Berettigelsesregler og -indstillinger** under **Konfiguration** i arbejdsområdet **Frynsegodeadministration**.

2. Vælg **Ny** under fanen **Berettigelsesregler** for at oprette en berettigelsesregel. Hvis du vil se de planer, der er knyttet til en berettigelsesregel, skal du vælge de **Tilknyttede planer**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Berettigelsesregel** | Entydigt id for berettigelsesreglen. |
   | **Beskrivelse** | En beskrivelse af berettigelsesreglen. |
   | **Dato og tidspunkt for Gyldig fra** | Startdatoen for berettigelsesreglen. | 
   | **Dato og tidspunkt for Gyldig til** | Slutdatoen for berettigelsesreglen. |
   | **Brugermedarbejdertype** | Angiver, om medarbejderens medarbejdertype skal bruges i reglen for frynsegodeberettigelse. |
   | **Arbejdertype** | Arbejdertypen, hvis **Brug medarbejdertype** er angivet til **Ja**. |
   | **Brug medarbejderstatus** | Angiver, om medarbejderens ansættelsesstatus skal bruges i reglen for frynsegodeberettigelse. |
   | **Status** | Medarbejderstatus, hvis **Brug medarbejderstatus** er angivet til **Ja**. Hvis **Brug medarbejderstatus** er angivet til **Nej**, bruges feltet ikke. |
   | **Brug ansættelseskategori** | Angiver, om medarbejderens værdi i **Medarbejderkategori** skal bruges som en del af reglen for frynsegodeberettigelse. | 
   | **Ansættelseskategori** | Medarbejderens ansættelseskategori, hvis **Brug ansættelseskategori** er angivet til **Ja**. |
   | **Brug ny ansættelsesregel** | Angiver, om der skal bruges en nyansats nye ansættelsesperiode som en del af berettigelsesreglen for frynsegoder. |
   | **Tilmeldingsperiode** | Den tidsperiode, hvor tilmelding for den nye ansættelse er tilladt. Hvis du også angiver dette i parametre, tilsidesætter parameterindstillingen dette. |
   | **Brug tidligere ansættelsesstatus** | Angiver, om en medarbejders tidligere ansættelsesstatus er del af reglen for frynsegodeberettigelse. Du kan f.eks. angive en berettigelsesregel, der frafalder en forsikrings venteperiode for alle medarbejdere, som er overgået fra statussen **Afskediget** til **Ansat** inden for 90 dage efter den tidligere ansættelse. |

4. Under **Yderligere kriterier** skal du vælge følgende indstillinger og tilføje oplysninger efter behov:

   | Indstilling | Beskrivelse |
   | --- | --- |
   | **Berettiget alder** | Angiver det eller de aldersintervaller, der kræves for at opfylde berettigelsesreglen. |
   | **Berettiget afdeling** | Angiver den eller de afdelinger, som en medarbejder skal være i for at opfylde berettigelsesreglen. |
   | **Berettiget ansættelsestype** | Angiver den eller de ansættelsestyper, som en medarbejder skal være kategoriseret som for at opfylde berettigelsesreglen. F.eks. fuld tid eller deltid. |
   | **Berettiget job** | Angiver det eller de job, der opfylder berettigelsesreglen. Jobbene knyttes til stillinger, og stillingerne udfyldes af medarbejdere. |
   | **Berettiget jobfunktion** | Angiver den eller de jobfunktioner, der opfylder en berettigelsesregel. F.eks. salgsmedarbejdere eller teknikere. |
   | **Berettiget jobtype** | Angiver den eller de jobtyper, der opfylder berettigelsesreglen. Det kan f.eks. være kontormedarbejdere eller ledelse. |
   | **Berettiget juridisk enhed** | Angiver den eller de juridiske enheder, der er gyldige for berettigelsesreglen. F.eks. Contoso Entertainment System USA. |
   | **Område for berettiget kompensation** | Angiver den medarbejderlokalitet, der opfylder berettigelsesreglen. Det kan f.eks. være det centrale USA. |
   | **Berettiget stilling** | Angiver den eller de stillinger, der opfylder berettigelsesreglen. F.eks. personalemedarbejder eller personalechef. |
   | **Berettiget stillingstype** | Angiver den eller de stillingstyper, der opfylder berettigelsesreglen. F.eks. fuld tid. |
   | **Berettiget delstat** | Angiver de stater eller provinser, der opfylder berettigelsesreglen. Det kan f.eks. være North Dakota USA eller British Columbia, Canada. |
   | **Berettigede vilkår for ansættelse** | Angiver de ansættelsesvilkår, der opfylder berettigelsesreglen. F.eks. efter ønske eller via gruppekontrakt. |
   | **Berettiget fagforening** | Angiver det medlemskab af en fagforening, der opfylder berettigelsesreglen. Det kan f.eks. være Forklift Drivers of America. </br></br>Når der bruges en fagforeningsbaseret berettigelsesregel, skal slutdatoen være angivet i arbejderens fagforeningspost. Du må ikke lade feltet være tomt. |
   | **Berettiget postnummer** | Angiver de postnumre, der opfylder berettigelsesreglen. For eksempel 58104. |

5. Du kan få vist følgende yderligere detaljer under **Flere oplysninger**:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Berettiget bruger-felt** | Angiver yderligere berettigelsesregler baseret på kundedefinerede felter. |
   | **Berettigelsestype** | Angiver den kriteriekategori, du valgte under **Yderligere kriterier**. |
   | **Berettigelsesreference** | Angiver de værdier, du valgte under **Yderligere kriterier**. |
   | **Beskrivelse** | Den beskrivelse, du valgte under **Yderligere kriterier**. |

6. Vælg **Gem**.

## <a name="configure-bundles"></a>Konfigurere bundter

Bundter er et sæt relaterede frynsegodeplaner. Du kan bruge frynsegodebundter til at gruppere frynsegodeplaner, som en medarbejder skal vælge for at kunne tilmelde sig visse frynsegodeplaner, der kan være afhængige af andre tilmeldingsplaner. Eksempler på, hvornår du kan bruge et bundt, omfatter:

- Et bundt med sygesikringsplaner, der omfatter helbredsforsikringer med høje fradrag med en tilknyttet sundhedsopsparingskonto (HSA).

- En livsforsikringsplan med en obligatorisk plan for medarbejderlivsforsikring, der er bundtet med en afhængig livsplan. Dette sikrer, at en medarbejder ikke kan vælge den afhængige livsforsikringsdækning uden at tilmelde sig medarbejderdækningen.

1. Vælg **Berettigelsesregler og -indstillinger** under **Konfiguration** i arbejdsområdet **Frynsegodeadministration**.

2. Vælg **Ny** under fanen **Bundter** for at oprette et bundt. Hvis du vil se de planer, der er knyttet til et bundt, skal du vælge de **Tilknyttede planer**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Bundt** | Et entydigt id for bundtet. |
   | **Beskrivelse** | En beskrivelse af bundtet. |
   | **Hoved** | Angiver, om en af planerne i bundtet skal markeres som behovsplan. Behovsplanen skal vælges under åben tilmelding som en del af bundtet, før frynsegodeadministratoren kan bekræfte medarbejderens valg af frynsegoder. |
   | **Dato og tidspunkt for Gyldig fra** | Den dato og det klokkeslæt, hvor bundet bliver aktivt. |
   | **Gyldig til** | Den dato, hvor bundtet udløber. Standarden er 31-12-2154, som repræsenterer aldrig. |

4. Vælg **Gem**.

## <a name="configure-periods"></a>Konfigurere perioder

Perioder definerer, hvornår frynsegoder er gældende, og hvornår medarbejdere har tilladelse til at tilmelde sig. Du kan oprette lige så mange perioder, som du ønsker, for at opretholde åben tilmelding til frynsegoder og disponeringsperioder for frynsegoder. Årene for frynsegodeplaner følger eller følger måske ikke kalenderåret. 

1. Vælg **Berettigelsesregler og -indstillinger** under **Konfiguration** i arbejdsområdet **Frynsegodeadministration**.

2. Vælg **Ny** under fanen **Perioder** for at oprette en periode. Hvis du vil køre en proces, der knytter alle gyldige aktive frynsegodeplaner til frynsegodeperioden, skal du vælge **Tilknyt planer**. Hvis du vil se de planer, der er knyttet til et bundt, skal du vælge de **Tilknyttede planer**. 

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Termin** | Et entydigt id for perioden. |
   | **Dato og tidspunkt for Gyldig fra** | Startdatoen og tidspunktet, hvor frynsegodeperioden bliver aktiv. |
   | **Dato og tidspunkt for Gyldig til** | Datoen og tidspunktet, hvor frynsegodeperioden bliver inaktiv. |
   | **Tilmeldingsstart** | Startdatoen for åben tilmelding. Åben tilmelding er, når en medarbejder kan vælge frynsegoder i forbindelse med selvbetjeningsfrynsegoder. |
   | **Afslutning af tilmelding** | Slutdatoen for åben tilmelding. |
   | **Åbne** | Angiver, om perioden er åben baseret på systemdatoen og datoer og klokkeslæt for gyldig fra og gyldig til. | 
   | **Forrige periode** | Angiver frynsegodeperioden, der går forud for den valgte frynsegodeperiode. Disse oplysninger bruges under tilmelding til frynsegodeberettigelse til at tildele planer, disponeringsindstillinger og udpegede fra et tidligere år. |
 
4. Vælg **Gem**.

## <a name="use-a-flex-credit-program"></a>Bruge et flekskreditprogram

Du kan bruge flekskreditprogrammer til at tilmelde medarbejdere til frynsegoder i overensstemmelse med et foruddefineret antal flekskreditter. Medarbejderne kan vælge, hvordan deres flekskreditter skal fordeles. Hvis en medarbejder f.eks. er dækket af ægtefællens sundhedsforsikring, kan vedkommende evt. bruge de kreditter, der ellers ville være anvendt på sundhedsforsikring, til andre frynsegoder.

1. Vælg **Berettigelsesregler og -indstillinger** under **Konfiguration** i arbejdsområdet **Frynsegodeadministration**.

2. Vælg **Flekskreditprogrammer** under fanen **Perioder**.

3. Vælg et flekskreditprogram, der skal anvendes. Felterne indeholder følgende oplysninger:

   | Felt | Beskrivelse |
   | --- | --- |
   | Frynsegodekredit-id | Det entydige id for flekskreditprogrammet. |
   | Beskrivelse | En beskrivelse af flekskreditprogrammet. | 
   | Fra-dato | Den dato og det klokkeslæt, hvor flekskreditprogrammet bliver aktivt. |
   | Til-dato | Slutdatoen for flekskreditprogrammet. Du kan beholde standardværdien (31/12/2154) for at angive, at der ikke er et planlagt udløb for flekskreditprogrammet. |
   | Kreditværdi i alt | Det antal kreditter, hver medarbejder skal bruge til deres frynsegoder. |
   | Regel for forholdsmæssig beregning | Den regel, der skal bruges til forholdsmæssig beregning af flekskreditter, når der ansættes en medarbejder midt i flekskreditperioden. </br></br><ul><li>**Ingen** – medarbejderen får ingen flekskreditter, hvis de er ansat efter starten på perioden for flekskreditprogrammet.</li><li>**Fuld kredit** – medarbejderen modtager det fulde beløb af flekskreditter, uanset hvornår de er ansat.</li><li>**Beregn forholdsmæssigt** – medarbejderen modtager et forholdsmæssigt beløb af flekskreditter baseret på deres startdato.</li></ul> |
   | Formel for forholdsmæssig beregning af flekskredit | Den regel, der skal bruges til forholdsmæssig beregning af flekskreditter for medarbejdere, som ansættes midt i en frynsegodeperiode for flekskreditprogrammet. Forholdsberegningen er baseret på ansættelsens startdato. Dette felt bruges kun, hvis du vælger **Beregn forholdsmæssigt** i feltet **Regel for forholdsmæssig beregning**. </br></br><ul><li>**Dagligt** – laver en forholdsmæssig beregning af det antal flekskreditter, en medarbejder modtager til dagsniveauet. Det samlede antal flekskreditter divideres med antallet af dage i perioden. Hvis din frynsegodeperiode f.eks. er 400 dage, vil systemet dividere det samlede antal flekskreditter med 400 for at beregne antallet af flekskreditter, som medarbejderne får pr. dag.</li><li>**Aktuel måned** – laver en forholdsmæssig beregning af flekskreditter, som en medarbejder modtager til månedsniveauet, afrundet til den aktuelle måned. Det samlede antal flekskreditter divideres med antallet af måneder i perioden. Hvis din frynsegodeperiode f.eks. er 15 måneder, vil systemet dividere det samlede antal flekskreditter med 15 for at beregne antallet af flekskreditter, som medarbejderne får pr. måned.</li><li>**Følgende måned** – laver en forholdsmæssig beregning af flekskreditter, som en medarbejder modtager til månedsniveauet, afrundet til den næste måned. Det samlede antal flekskreditter divideres med antallet af måneder i perioden. Hvis din frynsegodeperiode f.eks. er 15 måneder, dividerer systemet det samlede antal flekskreditter med 15 for at beregne antallet af flekskreditter, som medarbejderne får pr. måned.</li></ul> |
   
   Sørg for, at de enkelte frynsegodeplaner kun er tilmeldt i ét flekskreditprogram pr. frynsegodeperiode. Ellers ved systemet ikke, hvilket flekskreditprogram der skal bruges til at tildele flekskreditter, og der vil opstå problemer. 

## <a name="configure-programs"></a>Konfigurere programmer

Programmer er et sæt frynsegodeplaner, der deler et fælles sæt berettigelsesregler. Du kan definere berettigelsesregler for hele programmet i stedet for de enkelte plan. Det kan f.eks. være et Contoso Canada-program for fuldtidsansatte eller et Contoso Europa-program for ledelse. 

1. Vælg **Berettigelsesregler og -indstillinger** under **Konfiguration** i arbejdsområdet **Frynsegodeadministration**.

2. Vælg **Ny** under fanen **Programmer** for at oprette et program. Hvis du vil gøre undtagelser for medarbejdere, som ikke opfylder kravene i berettigelsesreglen, skal du vælge **Tilsidesættelse af berettigelsesregel**. Hvis du vil se de planer, der er knyttet til et program, skal du vælge **Tilknyttede planer**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Program** | Et entydigt id for programmet. |
   | **Beskrivelse** | En beskrivelse af programmet. | 
   | **Dato og tidspunkt for Gyldig fra** | Den dato og det klokkeslæt, hvor programmet bliver aktivt. |
   | **Dato og tidspunkt for Gyldig til** | Den dato og det klokkeslæt, hvor programmet udløber. Standarden er 31-12-2154, som repræsenterer aldrig. |
   | **Karenstid for dækning** | Den periode, som en medarbejder skal vente, før dækningen starter for frynsegodeprogrammet. |
   | **Karenstid for fradrag** | Den periode, som en medarbejder venter, før fradraget træder i kraft for frynsegodeprogrammet. |
   | **Berettigelsesregler** | Vælg de berettigelsesregler, der skal anvendes på frynsegodeprogrammet. Du kan definere berettigelsesreglerne under fanen **Berettigelsesregler** på denne side. |
   
4. Vælg **Gem**.
