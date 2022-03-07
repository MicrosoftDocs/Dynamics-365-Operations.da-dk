---
title: Konfigurere berettigelsesregler og -indstillinger
description: Dette emne beskriver, hvordan du angiver berettigelsesregler og -indstillinger i Frynsegodeadministration i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e87bef8994fe1eac0089764c8d4f9b18289c13ea
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069624"
---
# <a name="configure-eligibility-rules-and-options"></a>Konfigurere berettigelsesregler og -indstillinger 


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Når du har konfigureret de krævede parametre for Frynsegodeadministration , kan du oprette de berettigelsesregler, bundter, perioder og programmer, som du vil knytte til dine frynsegodeplaner.

Berettigelsesregler bruges til at bestemme, om medarbejdere er berettiget til en plan. Medarbejdere skal overholde betingelsen i mindst én regel for at være berettiget til frynsegodet. Du har f.eks. to regler for en plan. Den første regel (linje 1) viser, at medarbejdertypen skal være **Medarbejder**. Den anden regel (linje 2) viser, at medarbejderen skal være fuldtidsansat. Medarbejdere, der lever op til regel 1, er derfor berettigede, selvom de kun er ansat på deltid.

Du kan dog konfigurere en enkelt regel, der har flere betingelser. I dette tilfælde skal medarbejdere opfylde alle betingelser for reglen for at være berettiget til frynsegodet. Du har f.eks. en regel med navnet **Medarbejder på fuld tid**. Denne regel viser, at medarbejdertypen skal være **Medarbejder**, *og* at medarbejderen skal være ansat på fuld tid. Medarbejderne skal derfor opfylde begge betingelser i reglen for at være berettigede.

> [!IMPORTANT]
> Der skal knyttes mindst én berettigelsesregel til hver frynsegodeplan. Du kan knytte flere regler til et frynsegode.

## <a name="create-an-eligibility-rule"></a>Oprette en berettigelsesregel

Berettigelsesregler definerer, hvilke medarbejdere der kan tilmelde sig de enkelte frynsegodeplaner. Når du har defineret berettigelsesregler, kan du tildele dem til frynsegodeplaner. Derefter kan du behandle tilmeldingsberettigelse for at se, hvilke medarbejdere der er berettiget til de enkelte planer. 

Under åben tilmelding kan medarbejdere vælge frynsegodeplaner. Hvis de mister berettigelsen til en frynsegodeplan på baggrund af berettigelsesregler, efter at de allerede er tilmeldt, afmeldes de ikke automatisk. Når der opstår en livshændelse, der påvirker berettigelse til en plan, startes der typisk en tilmeldingsperiode, hvor medarbejderen kan vælge planer, som de er berettiget til. 

1. Vælg **Berettigelsesregler og -indstillinger** under **Konfiguration** i arbejdsområdet **Frynsegodeadministration**.

2. Vælg **Ny** under fanen **Berettigelsesregler** for at oprette en berettigelsesregel. Hvis du vil se de planer, der er knyttet til en berettigelsesregel, skal du vælge de **Tilknyttede planer**.

3. Angiv værdier for følgende felter.

   | Felt | Betegnelse |
   | --- | --- |
   | **Berettigelsesregel** | Entydigt id for berettigelsesreglen. |
   | **Beskrivelse** | En beskrivelse af berettigelsesreglen. |
   | **Dato og tidspunkt for Gyldig fra** | Startdatoen for berettigelsesreglen. | 
   | **Dato og tidspunkt for Gyldig til** | Slutdatoen for berettigelsesreglen. |
   | **Brugermedarbejdertype** | Angiver, om medarbejderens medarbejdertype skal bruges i reglen for frynsegodeberettigelsen. |
   | **Arbejdertype** | Arbejdertypen, hvis **Brug medarbejdertype** er angivet til **Ja**. |
   | **Brug medarbejderstatus** | Angiver, om medarbejderens ansættelsesstatus skal bruges i reglen for frynsegodeberettigelse. |
   | **Status** | Medarbejderstatus, hvis **Brug medarbejderstatus** er angivet til **Ja**. Hvis **Brug medarbejderstatus** er angivet til **Nej**, bruges feltet ikke. |
   | **Brug ansættelseskategori** | Angiver, om medarbejderens værdi i **Medarbejderkategori** skal bruges som en del af reglen for frynsegodeberettigelse. | 
   | **Ansættelseskategori** | Medarbejderens ansættelseskategori, hvis **Brug ansættelseskategori** er angivet til **Ja**. |
   | **Brug ny ansættelsesregel** | Angiver, om der skal bruges en nyansats nye ansættelsesperiode som en del af berettigelsesreglen for frynsegoder. |
   | **Tilmeldingsperiode** | Den tidsperiode, hvor tilmelding for den nye ansættelse er tilladt. Hvis du også angiver dette i parametre, tilsidesætter parameterindstillingen dette. |
   | **Brug tidligere ansættelsesstatus** | Angiver, om en medarbejders tidligere ansættelsesstatus er del af reglen for frynsegodeberettigelse. Du kan f.eks. angive en berettigelsesregel, der frafalder en forsikrings venteperiode for alle medarbejdere, som er overgået fra statussen **Afskediget** til **Ansat** inden for 90 dage efter den tidligere ansættelse. |

4. Under **Yderligere kriterier** skal du vælge følgende indstillinger og tilføje oplysninger efter behov.

   | Indstilling | Betegnelse |
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
   | **Berettiget fagforening** | Angiver det medlemskab af en fagforening, der opfylder berettigelsesreglen. Det kan f.eks. være Forklift Drivers of America.</br></br>Når der bruges en fagforeningsbaseret berettigelsesregel, skal slutdatoen være angivet i arbejderens fagforeningspost. Du må ikke lade feltet være tomt. |
   | **Berettiget postnummer** | Angiver de postnumre, der opfylder berettigelsesreglen. For eksempel 58104. |

5. Du kan få vist følgende yderligere detaljer under **Flere oplysninger**.

   | Felt | Betegnelse |
   | --- | --- |
   | **Berettiget bruger-felt** | Angiver yderligere berettigelsesregler baseret på kundedefinerede felter. |
   | **Berettigelsestype** | Angiver den kriteriekategori, du valgte under **Yderligere kriterier**. |
   | **Berettigelsesreference** | Angiver de værdier, du valgte under **Yderligere kriterier**. |
   | **Beskrivelse** | Den beskrivelse, du valgte under **Yderligere kriterier**. |

6. Vælg **Gem**.

## <a name="using-custom-fields-in-eligibility-rules"></a>Bruge brugerdefinerede felter i berettigelsesregler

I Human Resources kan der oprettes [brugerdefinerede felter](hr-developer-custom-fields.md) for at spore yderligere oplysninger. Disse felter kan føjes direkte til brugergrænsefladen, og en kolonne føjes dynamisk til den underliggende tabel.  

Brugerdefinerede felter kan bruges i berettigelsesprocessen. Berettigelsesregler kan bruge en eller flere brugerdefinerede feltværdier til at afgøre en medarbejders berettigelse.  Hvis du vil føje et brugerdefineret felt til en eksisterende regel eller oprette en ny regel, skal du gå til **Frynsegodeadministration > Links > Konfiguration > Berettigelsesregler > Berettigelse til brugerdefinerede felter**. På denne side kan du oprette en regel, der bruger et eller flere brugerdefinerede felter, og du kan definere flere værdier for hvert brugerdefineret felt for at afgøre berettigelse.

Følgende tabeller understøtter brugerdefinerede felter, der kan bruges i behandling af berettigelse:

- Arbejder (HcmWorker)  
- Job (HcmJob)  
- Stilling (HcmPosition)  
- Oplysninger om stilling (HcmPositionDetail)  
- Arbejdertildeling til stilling  
- Ansættelse (HcmEmployment)  
- Detaljer om ansættelse (HcmEmploymentDetails)  
- Jobdetaljer (HcmJobDetails)  

Følgende brugerdefinerede felttyper understøttes i behandling af berettigelse:

- Tekst  
- Valgliste  
- Tal  
- Decimal  
- Afkrydsningsfelt  

I følgende tabel vises oplysninger om formularfeltet for berettigelse til brugerdefinerede felter.

| Felt  | Betegnelse |
|--------|-------------|
| Navn | Navnet på de kriterier, der oprettes. |
| Tabel-label | Det tabelnavn, der indeholder det brugerdefinerede felt, der bruges til berettigelsesreglen. |
| Feltnavn | Det felt, der skal bruges til berettigelsesreglen. |
| Operatortype | Viser den operator, der bruges i konfigurationen af berettigelse til brugerdefinerede felter. |
| Værdi | Viser den værdi, der bruges i konfigurationen af berettigelse til brugerdefinerede felter. |

## <a name="eligibility-logic"></a>Logik for berettigelse

I følgende afsnit beskrives, hvordan berettigelse til frynsegoder behandles.

### <a name="rules-assigned-to-a-plan"></a>Regler, der er tildelt til en plan 
Når der er tildelt flere berettigelsesregler til en frynsegodeplan, skal en medarbejder opfylde mindst én regel for at være berettiget til at tilmelde sig frynsegodeplanen.  I følgende eksempel skal medarbejderen enten opfylde kravene i reglen for **Jobtype** eller reglen for **Aktive medarbejdere**.

![Medarbejderen skal enten opfylde kravene i reglen for Jobtype eller reglen for Aktive medarbejdere.](media/RulesAssignedToAPlan.png)
 
### <a name="criteria-within-an-eligibility-rule"></a>Kriterier i en berettigelsesregel 
I en regel definerer du de kriterier, der udgør reglen. I ovenstående eksempel er kriteriet for reglen **Jobtype** det sted, hvor Jobtype = Direktører. Derfor skal medarbejderen være direktør for at være berettiget. Dette er en regel, hvor der kun er ét kriterie i reglen.

Du kan definere regler, der har flere kriterier. Når du definerer flere kriterier i en berettigelsesregel, skal en medarbejder opfylde alle kriterier i reglen for at være berettiget til frynsegodeplanen. 

Reglen **Aktive medarbejdere** består f.eks. af følgende kriterier. For at medarbejderen kan være berettiget på baggrund af reglen om **Aktive medarbejdere**, skal medarbejderen være ansat i den juridiske enhed USMF *og* have en stilling på fuld tid.  

![Kriterier i en berettigelsesregel.](media/CriteriaWithinAnEligibilityRule.png) 
 
### <a name="multiple-conditions-within-criteria"></a>Flere betingelser i kriterier

Regler kan udvides yderligere til at bruge flere betingelser i et enkelt kriterie. Medarbejderen skal opfylde mindst én betingelse for at være berettiget. For at bygge videre på ovenstående eksempel kan reglen for **Aktive medarbejdere** udvides yderligere til at omfatte medarbejdere, der også er deltidsansatte. Som følge heraf skal medarbejderen nu være ansat i USMF *og* enten være fuldtidsansat eller deltidsansat.  

![Flere betingelser i kriterier.](media/MultipleConditionsWithinCriteria.png) 
 
### <a name="eligibility-conditions-within-a-custom-field-criterion"></a>Betingelser for berettigelse i et kriterie for brugerdefinerede felter 
I lighed med ovenstående kan brugerdefinerede felter bruges, når du opretter berettigelsesregler og arbejde på samme måde. Du kan for eksempel tilbyde internetrefusion til medarbejdere i Fargo og København, der arbejder hjemmefra, da internetomkostningerne er højere disse steder. Det kan du gøre ved at oprette to brugerdefinerede felter: **Kontorets placering** (valgliste) og **Arbejde hjemmefra** (afkrydsningsfelt). Opret derefter en regel med navnet **WFH-medarbejdere**. Kriteriet for reglen er der, hvor **Kontorets placering = Fargo** eller **København**, *og* hvor **Arbejde hjemmefra = Ja**.

De brugerdefinerede regler for berettigelse skal konfigureres som angivet i følgende billede. 

![Betingelser for berettigelse i et kriterie for brugerdefinerede felter.](media/EligibilityConditionsWithinACustomFieldCriterion.png) 
 
## <a name="configure-bundles"></a>Konfigurere bundter

Bundter er et sæt relaterede frynsegodeplaner. Du kan bruge frynsegodebundter til at gruppere frynsegodeplaner, som en medarbejder skal vælge for at kunne tilmelde sig visse frynsegodeplaner, der kan være afhængige af andre tilmeldingsplaner. Eksempler på, hvornår du kan bruge et bundt, omfatter:

- Et bundt med sygesikringsplaner, der omfatter helbredsforsikringer med høje fradrag med en tilknyttet sundhedsopsparingskonto (HSA).

- En livsforsikringsplan med en obligatorisk plan for medarbejderlivsforsikring, der er bundtet med en afhængig livsplan. Dette sikrer, at en medarbejder ikke kan vælge den afhængige livsforsikringsdækning uden at tilmelde sig medarbejderdækningen.

1. Vælg **Berettigelsesregler og -indstillinger** under **Konfiguration** i arbejdsområdet **Frynsegodeadministration**.

2. Vælg **Ny** under fanen **Bundter** for at oprette et bundt. Hvis du vil se de planer, der er knyttet til et bundt, skal du vælge de **Tilknyttede planer**.

3. Angiv værdier for følgende felter.

   | Felt | Betegnelse |
   | --- | --- |
   | **Bundt** | Et entydigt id for bundtet. |
   | **Beskrivelse** | En beskrivelse af bundtet. |
   | **Hoved** | Angiver, om en af planerne i bundtet skal markeres som behovsplanen. Behovsplanen skal vælges under åben tilmelding som en del af bundtet, før frynsegodeadministratoren kan bekræfte medarbejderens valg af frynsegoder. |
   | **Dato og tidspunkt for Gyldig fra** | Den dato og det klokkeslæt, hvor bundet bliver aktivt. |
   | **Gyldig til** | Den dato, hvor bundtet udløber. Standarden er 31-12-2154, som repræsenterer aldrig. |

4. Vælg **Gem**.

## <a name="configure-periods"></a>Konfigurere perioder

Perioder definerer, hvornår frynsegoder er gældende, og hvornår medarbejdere har tilladelse til at tilmelde sig. Du kan oprette lige så mange perioder, som du ønsker, for at opretholde åben tilmelding til frynsegoder og dækningsperioder for frynsegoder. Årene for frynsegodeplaner følger eller følger måske ikke kalenderåret. 

1. Vælg **Berettigelsesregler og -indstillinger** under **Konfiguration** i arbejdsområdet **Frynsegodeadministration**.

2. Vælg **Ny** under fanen **Perioder** for at oprette en periode. Hvis du vil køre en proces, der knytter alle gyldige aktive frynsegodeplaner til frynsegodeperioden, skal du vælge **Tilknyt planer**. Hvis du vil se de planer, der er knyttet til et bundt, skal du vælge de **Tilknyttede planer**. 

3. Angiv værdier for følgende felter.

   | Felt | Betegnelse |
   | --- | --- |
   | **Termin** | Et entydigt id for perioden. |
   | **Dato og tidspunkt for Gyldig fra** | Startdatoen og tidspunktet, hvor frynsegodeperioden bliver aktiv. |
   | **Dato og tidspunkt for Gyldig til** | Datoen og tidspunktet, hvor frynsegodeperioden bliver inaktiv. |
   | **Tilmeldingsstart** | Startdatoen for åben tilmelding. Åben tilmelding er, når en medarbejder kan vælge frynsegoder i forbindelse med selvbetjeningsfrynsegoder. |
   | **Afslutning af tilmelding** | Slutdatoen for åben tilmelding. |
   | **Åbne** | Angiver, om perioden er åben baseret på systemdatoen og datoer og klokkeslæt for gyldig fra og gyldig til. | 
   | **Forrige periode** | Angiver frynsegodeperioden, der går forud for den valgte frynsegodeperiode. Disse oplysninger bruges under tilmelding til frynsegodeberettigelse til at tildele planer, dækningsindstillinger og udpegede fra et tidligere år. |
 
4. Vælg **Gem**.

## <a name="use-a-flex-credit-program"></a>Bruge et flekskreditprogram

Du kan bruge flekskreditprogrammer til at tilmelde medarbejdere til frynsegoder i overensstemmelse med et foruddefineret antal flekskreditter. Medarbejderne kan vælge, hvordan deres flekskreditter skal fordeles. Hvis en medarbejder f.eks. er dækket af ægtefællens sundhedsforsikring, kan vedkommende evt. bruge de kreditter, der ellers ville være anvendt på sundhedsforsikring, til andre frynsegoder.

1. Vælg **Berettigelsesregler og -indstillinger** under **Konfiguration** i arbejdsområdet **Frynsegodeadministration**.

2. Vælg **Flekskreditprogrammer** under fanen **Perioder**.

3. Vælg et flekskreditprogram, der skal anvendes. Felterne indeholder følgende oplysninger.

   | Felt | Betegnelse |
   | --- | --- |
   | **Personalegodekredit-id** | Det entydige id for flekskreditprogrammet. |
   | **Beskrivelse** | En beskrivelse af flekskreditprogrammet. | 
   | **Fra-dato** | Den dato og det klokkeslæt, hvor flekskreditprogrammet bliver aktivt. |
   | **Til-dato** | Slutdatoen for flekskreditprogrammet. Du kan beholde standardværdien (12/31/2154) for at angive, at der ikke er et planlagt udløb for flekskreditprogrammet. |
   | **Kreditværdi i alt** | Det antal kreditter, hver medarbejder skal bruge til deres frynsegoder. |
   | **Regel for forholdsmæssig beregning** | Den regel, der skal bruges til forholdsmæssig beregning af flekskreditter, når der ansættes en medarbejder midt i flekskreditperioden. </br></br><ul><li>**Ingen** – medarbejderen får ingen flekskreditter, hvis de er ansat efter starten på perioden for flekskreditprogrammet.</li><li>**Fuld kredit** – medarbejderen modtager det fulde beløb af flekskreditter, uanset hvornår de er ansat.</li><li>**Beregn forholdsmæssigt** – medarbejderen modtager et forholdsmæssigt beløb af flekskreditter baseret på deres startdato.</li></ul> |
   | **Formel for forholdsmæssig beregning af flekskredit** | Den regel, der skal bruges til forholdsmæssig beregning af flekskreditter for medarbejdere, som ansættes midt i en frynsegodeperiode for flekskreditprogrammet. Forholdsberegningen er baseret på ansættelsens startdato. Dette felt bruges kun, hvis du vælger **Beregn forholdsmæssigt** i feltet **Regel for forholdsmæssig beregning**. </br></br><ul><li>**Dagligt** – laver en forholdsmæssig beregning af det antal flekskreditter, en medarbejder modtager til dagsniveauet. Det samlede antal flekskreditter divideres med antallet af dage i perioden. Hvis din frynsegodeperiode f.eks. er 400 dage, vil systemet dividere det samlede antal flekskreditter med 400 for at beregne antallet af flekskreditter, som medarbejderne får pr. dag.</li><li>**Aktuel måned** – laver en forholdsmæssig beregning af flekskreditter, som en medarbejder modtager til månedsniveauet, afrundet til den aktuelle måned. Det samlede antal flekskreditter divideres med antallet af måneder i perioden. Hvis din frynsegodeperiode f.eks. er 15 måneder, vil systemet dividere det samlede antal flekskreditter med 15 for at beregne antallet af flekskreditter, som medarbejderne får pr. måned.</li><li>**Følgende måned** – laver en forholdsmæssig beregning af flekskreditter, som en medarbejder modtager til månedsniveauet, afrundet til den næste måned. Det samlede antal flekskreditter divideres med antallet af måneder i perioden. Hvis din frynsegodeperiode f.eks. er 15 måneder, dividerer systemet det samlede antal flekskreditter med 15 for at beregne antallet af flekskreditter, som medarbejderne får pr. måned.</li></ul> |
   
   Sørg for, at de enkelte frynsegodeplaner kun er tilmeldt i ét flekskreditprogram pr. frynsegodeperiode. Ellers ved systemet ikke, hvilket flekskreditprogram der skal bruges til at tildele flekskreditter, og der vil opstå problemer. 

## <a name="configure-programs"></a>Konfigurere programmer

Programmer er et sæt frynsegodeplaner, der deler et fælles sæt berettigelsesregler. Du kan definere berettigelsesregler for hele programmet i stedet for de enkelte plan. Det kan f.eks. være et Contoso Canada-program for fuldtidsansatte eller et Contoso Europa-program for ledelse. 

1. Vælg **Berettigelsesregler og -indstillinger** under **Konfiguration** i arbejdsområdet **Frynsegodeadministration**.

2. Vælg **Ny** under fanen **Programmer** for at oprette et program. Hvis du vil gøre undtagelser for medarbejdere, som ikke opfylder kravene i berettigelsesreglen, skal du vælge **Tilsidesættelse af berettigelsesregel**. Hvis du vil se de planer, der er knyttet til et program, skal du vælge **Tilknyttede planer**.

3. Angiv værdier for følgende felter.

   | Felt | Betegnelse |
   | --- | --- |
   | **Program** | Et entydigt id for programmet. |
   | **Beskrivelse** | En beskrivelse af programmet. | 
   | **Dato og tidspunkt for Gyldig fra** | Den dato og det klokkeslæt, hvor programmet bliver aktivt. |
   | **Dato og tidspunkt for Gyldig til** | Den dato og det klokkeslæt, hvor programmet udløber. Standarden er 31-12-2154, som repræsenterer aldrig. |
   | **Karenstid for dækning** | Den periode, som en medarbejder skal vente, før dækningen starter for frynsegodeprogrammet. |
   | **Karenstid for fradrag** | Den periode, som en medarbejder venter, før fradraget træder i kraft for frynsegodeprogrammet. |
   | **Berettigelsesregler** | Vælg de berettigelsesregler, der skal anvendes på frynsegodeprogrammet. Du kan definere berettigelsesreglerne under fanen **Berettigelsesregler** på denne side. |
   
4. Vælg **Gem**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
