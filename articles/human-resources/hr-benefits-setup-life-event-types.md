---
title: Konfigurere livsbegivenhedstyper
description: Microsoft Dynamics 365 Human Resources bruger livshændelsestyper til at definere hændelser, når det er relevant at opdatere tilmelding til medarbejderfrynsegoder.
author: andreabichsel
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8f04be1c0852970db337766757ff6f412bbf5c38
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921111"
---
# <a name="configure-life-event-types"></a>Konfigurere livsbegivenhedstyper

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources bruger livshændelsestyper, når det er relevant at opdatere tilmelding til medarbejderfrynsegoder, f.eks. i forbindelse med bryllup eller barsel. Hvert livshændelsestype-id kan kun knyttes til én livshændelsestype. Hvis du f.eks. opretter et livshændelses-id, der kaldes Adresseændring, som er knyttet til livshændelsestypen Medarbejderens adresseændring, kan du ikke oprette et nyt id med navnet Medarbejderens adresseændring og knytte det til en livshændelsen Medarbejderens adresseændring. Hvis en levetidshændelsestype ikke er knyttet til en plantype, udløser levetidshændelsestypen ikke en levetidshændelse. Yderligere oplysninger finder du i [Oprette plantyper](hr-benefits-setup-plan-types.md).

## <a name="create-a-life-event-type"></a>Oprette en livshændelsestype

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Livshændelsestyper** under **Konfiguration**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Livshændelsestype-id** | Det entydige id for livshændelsestypen. |
   | **Beskrivelse** | En beskrivelse af livshændelsestypen. |
   | **Livshændelsestype** | En katalysator til opdatering af en medarbejders tilmelding til frynsegoder. Du kan se en liste over livshændelser under [Livshændelser](hr-benefits-setup-payment-frequencies.md?life-events) nedenfor. |

4. Vælg **Gem**.

## <a name="view-attached-plans"></a>Få vist tilknyttede planer

Du kan få vist en liste over planer, der er knyttet til den valgte livshændelsestype. Livshændelser knyttes til en plantype, og plantyper knyttes til en plan.

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Livshændelsestyper** under **Konfiguration**.

2. Vælg **Handlinger**.

3. Vælg **Tilknyttede planer**.

## <a name="life-events"></a>Livshændelser

Du kan vælge mellem følgende livshændelser, når du opretter en livshændelsestype:

| Livshændelse | Adresse | Udløser |
| --- | --- | --- |
| **Ændring af ægteskabelig status** | Arbejder > Profil > > Personlige oplysninger > Ægteskabelig status| Ændring af ægteskabelig status |
| **Ændring af ansættelsesstatus** | Arbejder > Ansættelse<br>Side med ansættelseshistorik | Hvis der oprettes en ny ansættelsesdetalje med en anden ansættelsesstatus for en arbejder med en eksisterende ansættelsesdetalje, udløses en levetidshændelse.  Opdatering af en eksisterende ansættelsesdetalje med en anden ansættelsesstatus vil også udløse en levetidshændelse.  |
| **Ændring af medarbejders adresse** | Arbejder > Profil > Adresser<br>Arbejder > Personlige oplysninger > Personlige kontakter > Adresse | Skift adresse. Adressen skal være primær for at udløse en levetidshændelse. |
| **Ændring af afhængig** | Arbejder > Profil > Personlige oplysninger > Personlige kontakter<br>Medarbejderselvbetjening | Tilføj en personlig kontakt, hvor du angiver kontakten som afhængig og definerer **Gyldig fra**. Opdater afhængige oplysninger for **Gyldig til** for en personlig kontaktperson. Den personlige kontaktrelation skal være barn, ægtefælle, samlever eller tidligere ægtefælle.  |
| **Fødsel eller adoption (afhængig)** | Arbejder > Profil > Personlige oplysninger > Personlige kontakter<br>Medarbejderselvbetjening > Rediger personlige oplysninger > Personlige kontakter | **Fødselsdato** eller **Adoptionsdato** tilføjes eller opdateres. Barnets **Fødselsdato** er påkrævet. |
| **Tab af dækning (ægtefælle/samlever)** | Arbejder > Profil > Personlige oplysninger > Personlige kontakter > Oplysninger om afhængig > Tab af dækning | **Tab af dækning** valgt for en personlig kontakt sammen med **Ikrafttrædelsesdato** |
| Ændring i ansættelse for samlever | Arbejder > Profil > Personlige oplysninger > Personlige kontakter > Oplysninger om afhængig > Ansat | Oprette en personlig kontakt og angive indstillingen **Ansat** til **Ja**. Opdatering af en personlig kontakt og ændring af **Ansat**.  |
| **Orlov (ægtefælle/samlever)** | Arbejder > Profil > Personlige oplysninger > Personlige kontakter > Oplysninger om afhængig > Orlov | Personlig kontaktperson oprettes, og **Ikrafttrædelsesdato for orlov** defineres. **Orlov** for personlig kontakt opdateres. **Ikrafttrædelsesdato for orlov** for personlig kontakt opdateres.  |
| **Ændring i dækning (stilling)** | Arbejder > Stillingstildeling > Tildeling af arbejderstillinger<br>Stillinger > Stillinger | Skift til stillingen i posterne for arbejderens tildeling af stilling. Skift arbejdertildelingen i stillingen. |
| **Ændring i dækning (løn)** | Arbejder > Kompensation > Fast plan<br>Arbejder > Personlige oplysninger > Årlig løn som frynsegoder | Hvis Administration af frynsegoder > Delte parametre for personale > Frynsegoder > Årlig løn som frynsegoder ikke er aktiveret, kan du opdatere Arbejder > Kompensation > Fast plan vil oprette en livshændelse. Hvis Administration af frynsegoder > Delte parametre for personale > Frynsegoder > Årlig løn som frynsegoder er aktiveret, vil opdatering af Arbejder > Personlige oplysninger > Årlig løn som frynsegoder oprette en livshændelse. |
| **Sygeforsikring (medarbejder/afhængig)** | Arbejder > Profil > Personlige oplysninger > Personlige kontakter > Oplysninger om afhængig > Ikrafttrædelsesdato for sygeforsikring | Tilføjelse eller opdatering af **Ikrafttrædelsesdato for sygeforsikring** for en personlig kontakt opretter denne livshændelse. |
| **Støtte ifølge dommerkendelse** | Arbejder > Profil > Personlige oplysninger > Personlige kontakter > Afhængigt > Støtte ifølge dommerkendelse (QMSCO/QDRO) og ikrafttrædelsesdatoer | Når der oprettes en personlig kontakt, oprettes der en livshændelse, hvis **Støtte ifølge dommerkendelse** er **Ja**. Opdatering **Støtte ifølge dommerkendelse** eller **Udløbsdato ifølge dommerkendelse** vil også udløse en livshændelse. |
| **Medarbejders død** | Arbejder > Profil > > Personlige oplysninger > Dato for medarbejders død | Der angives eller opdateres en dato for medarbejders død. |
| **EOI (forsikringsbar)** | Arbejder > Arbejder > Versioner > Ansættelseshistorik > Håndtering af datoer > Frynsegodedetaljer | **EOI (forsikringsbar)** er angivet til **Ja**. **Bekræftelsesdato for EOI (forsikringsbar)** er defineret. |
| **Modtager** | Arbejder > Profil > Personlige oplysninger > Personlige kontakter | Der tilføjes en personlig kontakt, og feltet **Modtager** og **Ikrafttrædelsesdato** udfyldes. Den personlige kontakt skal være af typen **Barn**, **Ægtefælle**, **Samlever**, **Søskende**, **Familiekontakt**, **Anden kontakt** eller **Forælder**, |
| **Medarbejders sygeforsikring** | Arbejder > Arbejder > Versioner > Ansættelseshistorik > Håndtering af datoer > Frynsegodedetaljer | **Berettigelse til sygeforsikring** er angivet til **Ja**. **Dato for berettigelse til sygeforsikring** er ændret. |
| **Fødselsdag** | Administration af frynsegoder > Behandling af ændring af livshændelser | Disse livshændelser oprettes fra **Behandling af ændring af livshændelser**. Processen analyserer den valgte periode og juridiske enhed, og finder de tilknyttede arbejdere. Den beregner deres sidste fødselsdag og opretter en livshændelse for fødselsdage, hvis der ikke allerede er oprettet en. |
| **Ændring af arbejders berettigelse (ikke specifik for USA)** | Arbejder > Ansættelse<br>Arbejder > Arbejder > Versioner > Ansættelseshistorik | Opretter en livshændelse, når:<br><ul><li>Når du opretter en ny ansættelse, og der er en tidligere ansættelse, ændres arbejdertypen.</li><li>Når du opretter en ny ansættelsesdetalje, og der er en tidligere ansættelsesdetalje, ændres ansættelsestypen eller -kategorien.</li><li>Opdatering af en ansættelsespost og en anden arbejdertype defineres.</li><li>Opdatering af en ansættelsedetaljepost og en anden ansættelsestype eller -kategori angives.</li></ul> |
| **Tilsidesættelse af ny berettigelse (ikke specifik for USA)** | Udvidet Human Resources > Frynsegoder > Planer > Frynsegoder > Tilsidesæt berettigelsesregler | Bruge behandling af livshændelse<br>Oprettelse af en ny tilsidesættelse af berettigelse til frynsegodeplan for en arbejder udløser denne livshændelse.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Ændring af tilsidesættelse af berettigelsesregler (ikke specifik for USA)** | Udvidet Human Resources > Frynsegoder > Planer > Frynsegoder > Tilsidesæt berettigelsesregler | Opdatering af **Gyldig fra** eller **Gyldig til** for en tilsidesættelse af berettigelse til frynsegodeplan udløser denne livshændelse. |
| **Udløb af tilsidesættelse af berettigelsesregler (ikke specifik for USA)** | Administration af frynsegoder > Behandling af ændring af livshændelser  | Disse livshændelser oprettes fra **Behandling af ændring af livshændelser**. Processen analyserer den valgte periode og juridiske enhed, og finder tilknyttede tilsidesættelser af berettigelse til frynsegodeplan. Der oprettes livshændelser, hvis tilsidesættelserne er udløbet. |
| **Ny frynsegodeplan (ikke specifik for USA)** | Udvidet Human Resources > Frynsegoder > Planer > Ny | Berettigelsesindstillinger føjes til en aktuel plan. Der tilføjes en ny plan med tilknyttede berettigelsesindstillinger.</br></br>Human Resourcesmedarbejdere skal køre behandling af berettigelse til livshændelsen i denne forekomst. |
| **Ændring af berettigelsesregler (ikke specifik for USA)** | Administration af frynsegoder > Berettigelsesregler | Brug behandling af berettigelse til livshændelse. Logges, når poster for **BenefitEligibilityRule** har fået ændret følgende værdier: **UseEmplCategory**, **UseEmplStatus** eller **UseEmplType**. Opdaterer kun livshændelsestransaktioner, der allerede findes for en ændret regel eller kriterier for berettigelse. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]