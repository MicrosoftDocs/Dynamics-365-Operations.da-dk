---
title: Oprette en frynsegodeplan
description: Denne artikel viser, hvordan du kan oprette frynsegodeplaner i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitPlanListPage, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c8d4488f1782d80484a8b91f4ae7303fea0e464
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336917"
---
# <a name="create-a-benefit-plan"></a>Oprette en frynsegodeplan

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel viser, hvordan du kan oprette frynsegodeplaner i Dynamics 365 Human Resources.

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Frynsegodeplaner** under **Planer**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter under fanen **Generelt**:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Plan** | Et entydigt id for planen. |
   | **Beskrivelse** | En beskrivelse af planen. |
   | **Plantype** | Når du opretter en ny plan, skal du angive plantypen. En plantype er en overordnet gruppering af bestemte typer frynsegoder. Hver enkelt plantype angiver, om en medarbejder kan tilmelde sig flere planer af den pågældende type, og angiver, om kontaktpersoner er modtagere eller afhængige, og definerer dækningsindstillinger. Du kan oprette nye brugerdefinerede plantyper for at imødekomme behovet for dine tilbudte frynsegoder. De vigtigste typer af frynsegodeplaner er: <ul><li>401K</li><li>ADD</li><li>Tandlægearbejde</li><li>Fitness</li><li>FSA</li><li>Liv</li><li>LTD</li><li>Medicinsk</li><li>PTO</li><li>STD</li><li>Vision</li></ul> |
   | **Kode for plantype** | Kodetypekoden for plantypen. |
   | **Program** | Angiver et program, som planen eventuelt kan tildeles til. |
   | **Bundt** | Angiver et bundt, som planen eventuelt kan tildeles til. |
   | **Hoved** | Angiver, om planen er behovsplanen i det bundt, den er tildelt til. |
   | **Dato og tidspunkt for Gyldig fra** | Dato og klokkeslæt, som planen starter. Standardværdien er den aktuelle systemdato. |
   | **Dato og tidspunkt for Gyldig til** | Dato og klokkeslæt, hvor planen slutter. Standardværdien er 31-12-2154, som angiver aldrig. |

4. Under fanen **Konfiguration** skal du angive værdier for følgende felter, afhængigt af den plantype, du er ved at oprette:

   | Plantype | Felt | Beskrivelse |
   | --- | --- | --- |
   | Medicinsk (læge, tandlæge, optiker, HMO) | COBRA | Angiver, om planen er berettiget til COBRA (Consolidated Omnibus Budget Reconciliation Act). |
   | Medicinsk (læge, tandlæge, optiker, HMO) | HIPAA | Angiver, om planen er berettiget til HIPAA (Health Insurance Portability and Accountability Act). |
   | Medicinsk (læge, tandlæge, optiker, HMO)<br><br>Andet (PTO, fitness)<br><br>Diverse<br><br>Langvarigt handicap<br><br>ADD (basisliv, frivilligt liv)<br><br>Opsparing (f.eks. 401(k))<br><br>FSA | Beløb før skat, der er berettiget | Angiver, om der kan betales bidrag til planen, før der beregnes moms. |
   | Medicinsk (læge, tandlæge, optiker, HMO)<br><br>Andet (PTO, fitness)<br><br>Langvarigt handicap<br><br>ADD (basisliv, frivilligt liv)<br><br>Opsparing (f.eks. 401(k))<br><br>FSA | Bogfør berettiget moms | Angiver, om der kan betales bidrag til planen, efter der beregnes moms. |
   | Medicinsk (læge, tandlæge, optiker, HMO)<br><br>Andet (PTO, fitness)<br><br>Langvarigt handicap<br><br>ADD (basisliv, frivilligt liv)<br><br>Opsparing (f.eks. 401(k))<br><br>FSA | Bidragyder | Angiver, hvem der bidrager til planen – medarbejderen, arbejdsgiveren eller begge. |
   | Langvarigt handicap<br><br>ADD (basisliv, frivilligt liv) | Minimumsdækning | Det minimumbeløb for forsikringsdækning, der er påkrævet for planen. |
   | Langvarigt handicap<br><br>ADD (basisliv, frivilligt liv) | Maksimum dækning | Det maksimumbeløb for forsikringsdækning, der er påkrævet for planen. |
   | Langvarigt handicap<br><br>ADD (basisliv, frivilligt liv) | Brug trinvise intervaller for dækning | Angiver, om det skal kontrolleres, om dækningsbeløbet svarer til et gyldigt trinvist beløb. |
   | Langvarigt handicap<br><br>ADD (basisliv, frivilligt liv) | Trinvise intervaller for beløb | Det trinvise beløb for forsikringsdækning for planen. Hvis det trinvise beløb f.eks. er 1.000, kan en medarbejder ikke have en forsikring på 200.500 DKK, de skal runde op til 201.000 DKK eller ned til 200.000 DKK. |
   | Langvarigt handicap<br><br>ADD (basisliv, frivilligt liv) | Retning med trinvise intervaller | Angiver den retning, der skal afrundes – enten op eller ned – når dækningsbeløbet ikke opfylder den trinvist stigende beløbsværdi. |
   | ADD (basisliv, frivilligt liv) | EOI (Evidence of insurability - forsikringsbar) | Angiver, om en medarbejder skal fremvise bevis på, at medarbejderen er forsikringsberettiget. |
   | ADD (basisliv, frivilligt liv) | Beløb | Beløbet i regnskabsvaluta. Dette felt er kun aktivt, hvis afkrydsningsfeltet Bevis på forsikringsberettigelse er markeret. |
   | Opsparing (f.eks. 401(k))<br><br>FSA | Årligt minimumsbidrag | Det minimumbidragsbeløb, der er påkrævet for planen. |
   | Opsparing (f.eks. 401(k))<br><br>FSA | Maksimalt årligt bidrag | Det maksimumbidragsbeløb, der er påkrævet for planen. |
   | Opsparing (f.eks. 401(k)) | Arbejdsgivers maksimale årlige beløb | Det maksimumbeløb, en arbejdsgiver må bidrage med til en medarbejders opsparingsplan i løbet af en frynsegodeperiode. Du skal markere afkrydsningsfeltet Medarbejdermatch for at bruge dette felt. |
   | Opsparing (f.eks. 401(k)) | Arbejdsgivermatch | Angiver, om arbejdsgiveren bidrager til en medarbejders opsparingsplan. |
   | Opsparing (f.eks. 401(k)) | Procentdel for arbejdsgivermatch | Den procentdel af et medarbejderbidrag, som arbejdsgiveren vil betale. |
   | Opsparing (f.eks. 401(k)) | Beløbsgrænse for arbejdsgivermatch | Den maksimale procentdel, som arbejdsgiveren vil betale. Hvis en arbejdsgiver f.eks. modsvarer 100 % af medarbejderens bidrag med op til 6 % af medarbejderens løn, er arbejdsgivers match 6 %. |

5. Angiv værdier for følgende felter under fanen **Konfiguration**:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Tillad/fortsæt tilmelding** | Angiver, om medarbejdere kan tilmelde sig planen, hvis de overholder berettigelseskrav.</br></br>Hvis dette er angivet til Nej, vil planen ikke være tilgængelig for medarbejdere, når du behandler berettigelse. |
   | **Tilmeld automatisk fra forrige år** | Angiver, om der automatisk skal tilmeldes en berettiget medarbejder i planen, hvis vedkommende er tilmeldt i løbet af det foregående år. |
   | **Tilmeld automatisk som standard** | Angiver, om planen for tilmelding som standard skal vælges. Planen er ikke obligatorisk, så medarbejderen kan ændre standardvalget. |
   | **Lukket for nye tilmeldinger** | Angiver, om planen kun skal begrænses til de berettigede medarbejdere, der var tilmeldt planen i det foregående år. |
   | **Obligatorisk plan** | Angiver, om medarbejdere automatisk skal tilmeldes planen. Medarbejdere kan ikke ændre tilmeldingsvalget. |
   | **Dato for start** | Den dato, hvor planen blev oprettet i firmaet. |
   | **Kreditorkonto** (leverandør af frynsegode) | Den leverandør, som firmaet betaler præmier for planen. |
   | **Navn** (leverandør af frynsegode) | Kreditorens navn. |
   | **Kreditorreference** (leverandør af frynsegode) | Kreditorens reference til planen. F.eks. firmaets gruppeplannummer. |
   | **Alternativ reference** (leverandør af frynsegode) | Kreditorens alternative reference til planen. F.eks. firmaets kontonummer. |
   | **Valuta** (leverandør af frynsegode) | Den valuta, der bruges til at betale præmie til leverandøren. |
   | **Udgiftskonto** (leverandør af frynsegode) | Den finanskontoen, der bruges som udgiftskonto til betaling af præmie for planen. |
   | **Kreditorkonto** (administrator af frynsegode) | Den leverandør, som firmaet betaler for at administrere planen. Hvis planen er selvadministreret, skal feltet ikke udfyldes. |
   | **Navn** (administrator af frynsegode) | Navnet på administratorleverandøren af frynsegode. |
   | **Kreditorreference** (administrator af frynsegode) | Administratorleverandørs reference til planen. |
   | **Alternativ reference** (administrator af frynsegode) | Administratorleverandørs alternative reference til planen. |
   | **Valuta** (administrator af frynsegode) | Den valuta, der bruges til at betale administratoren af frynsegode. |
   | **Udgiftskonto** (administrator af frynsegode) | Den finanskonto, der bruges som udgiftskonto for de omkostninger, der er knyttet til administrationen af planen. |

6. Filtrer efter behov under fanen **Filtre**. Du kan filtrere efter følgende felter:

   - **Virksomhedsenhed**
   - **Afdeling**
   - **Juridisk enhed**
   - **Adresse**
   - **Stilling**

7. Angiv værdier for følgende felter under fanen **Berettigelsesregler**:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Linjenummer** | Berettigelsesreglens linjenummer. |
   | **Berettigelsesregel** | En berettigelsesregel, der skal anvendes på frynsegodeplanen. Denne berettigelsesregel anvendes på den tilsvarende handlingstype og knyttes til den angivne venteperiode for dækning og fradrag. |
   | **Handlingstype** | Den handling, som berettigelsesreglen skal anvendes på: tilmelding til frynsegoder eller udløb af frynsegoder. |
   | **Karenstid for dækning** | En værdi fra formularen Venteperioder. Venteperioden for dækning er det antal dage eller måneder, en medarbejder venter på dækning af frynsegoder eller udløb af frynsegoder baseret på kriterierne i berettigelsesreglen og handlingstypen. |
   | **Karenstid for fradrag** | En værdi fra formularen Venteperioder. Venteperioden for fradrag er det antal dage eller måneder, en medarbejder venter på fradrag for frynsegoder på lønsedlen baseret på kriterierne i berettigelsesreglen og handlingstypen. |

8. Vælg **Gem**.

## <a name="view-enrolled-workers"></a>Se tilmeldte arbejdere

Du kan se de arbejdere, der er tilmeldt til en valgt frynsegodeplan.

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Frynsegodeplaner** under **Planer**.

2. Vælg **Tilmeldte arbejdere** på navigationslinjen under fanen **Frynsegoder**.

## <a name="attach-coverage-options"></a>Tilknyt dækningsindstillinger

Du kan tilføje dækningsindstillinger for den valgte frynsegodeplan. Hvis du tilknytter dækningsindstillinger, samles sats- og fradragsopsætningen til en dækningsindstilling.  Eksempel: For en medicinsk plan kan brugeren vælge en familiedækningsindstilling.  Det ville så være nødvendigt at vælge familiesatsen for den tilknyttede plan (angivet i satsopsætning) og fradrag for den tilknyttede plan (angivet i satsopsætning). Dette giver arbejdsgiverens og medarbejderens kostpris for en valgt dækning. Derefter skal du gentage processen for en medarbejder + 1 dækning eller medarbejderdækning.

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Frynsegodeplaner** under **Planer**.

2. Vælg **Tilknyt dækningsindstillinger** på navigationslinjen under fanen **Frynsegoder**.

## <a name="override-eligibility-rules"></a>Tilsidesæt berettigelsesregler

Du kan føje arbejdere til en plan som undtagelser til berettigelsesreglerne. Hver medarbejder, som du tilføjer, vil være berettiget til frynsegodeplanen.

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Frynsegodeplaner** under **Planer**.

2. Vælg **Tilsidesæt berettigelsesregler** på navigationslinjen under fanen **Frynsegoder**.

## <a name="view-attached-periods"></a>Vis tilknyttede perioder

Du kan få vist en liste over tilgængelige frynsegodeperioder.

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Frynsegodeplaner** under **Planer**.

2. Vælg fanen **Perioder** på navigationslinjen.

## <a name="view-plan-description"></a>Se planbeskrivelse

Du kan angive en beskrivelse af planen for at hjælpe medarbejderne med at vælge frynsegoder. Den planbeskrivelse, du angiver her, vises i medarbejdernes selvbetjening, når de peger på planen på listen over dækningsindstillinger.

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Frynsegodeplaner** under **Planer**.

2. Vælg **Planbeskrivelse** på navigationslinjen under fanen **Frynsegoder**.

## <a name="view-flex-credit-programs"></a>Vis programmer for fleksibel kredit

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Frynsegodeplaner** under **Planer**.

2. Vælg **Programmer for fleksibel kredit** på navigationslinjen under fanen **Frynsegoder**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
