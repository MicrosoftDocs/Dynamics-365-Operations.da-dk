---
title: Konfigurere livsbegivenhedstyper
description: Microsoft Dynamics 365 Human Resources bruger livshændelsestyper til at definere hændelser, hvor tilmelding til medarbejderfrynsegoder skal opdateres.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: c382299014e3f823bc2cd210749aae8c091c5f23
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111954"
---
# <a name="configure-life-event-types"></a>Konfigurere livsbegivenhedstyper

Microsoft Dynamics 365 Human Resources bruger livshændelsestyper til at definere hændelser, hvor tilmelding til medarbejderfrynsegoder skal opdateres. Det kan f.eks. være at blive gift eller få børn. Hvert livshændelsestype-id kan kun knyttes til én livshændelsestype. Hvis du f.eks. opretter et livshændelses-id, der kaldes Adresseændring, som er knyttet til livshændelsestypen Medarbejderens adresseændring, kan du ikke oprette et nyt id med navnet Medarbejderens adresseændring og knytte det til en livshændelsen Medarbejderens adresseændring. 

Når du har oprettet livshændelsestyper, skal du knytte dem til plantyper. Yderligere oplysninger finder du i [Oprette plantyper](hr-benefits-setup-plan-types.md).

   > [!NOTE]
   > Når du opretter en livshændelse, skal du knytte den til en plantype. Yderligere oplysninger finder du i [Oprette plantyper](hr-benefits-setup-life-event-types.md).

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
| **Ændring af ansættelsesstatus** | <ul><li>Arbejder > Ansættelse</li><li>Side med ansættelseshistorik</li></ul> | Ændring af ansættelsesstatus |
| **Ændring af medarbejders adresse** | <ul><li>Arbejder > Profil > Adresser </li><li>Arbejder > Personlige oplysninger > Personlige kontakter > Adresse</li></ul> Tilføjet, redigeret eller slettet adresse |
| **Ændring af afhængig** | <ul><li>Arbejder > Profil > Personlige oplysninger > Personlige kontakter > Tilføj eller slet en afhængig</li><li>Medarbejderselvbetjening</li></ul> | Tilføjet eller slettet afhængig. Den personlige kontaktrelation skal være barn, ægtefælle, samlever eller tidligere ægtefælle. Hvis du opdaterer datoen for **Gyldig fra**, udløses der en livshændelse. Hvis du ikke opdaterer denne dato, udløser der ingen livshændelse. |
| **Fødsel eller adoption (afhængig)** | <ul><li>Arbejder > Profil > Personlige oplysninger > Personlige kontakter > Oplysninger om afhængig</li><li>Medarbejderselvbetjening</li></ul> | Feltet **Adoptionsdato** er udfyldt. Barnets fødselsdato er påkrævet. |
| **Tab af dækning (ægtefælle/samlever)** | Arbejder > Profil > Personlige oplysninger > Personlige kontakter > Oplysninger om afhængig > Tab af dækning | **Tab af dækning** valgt for en personlig kontakt sammen med **Ikrafttrædelsesdato** |
| Ændring i ansættelse for samlever | Arbejder > Profil > Personlige oplysninger > Personlige kontakter > Oplysninger om afhængig > Ansat. | <ul><li>Posten Oplysninger om afhængig oprettet, og feltet **Personlig kontakt ansat** = Ja</li><li>Feltet **Personlig kontakt ansat** er ændret (Ja eller Nej)</li></ul> |
| **Orlov (ægtefælle/samlever)** | Arbejder > Profil > Personlige oplysninger > Personlige kontakter > Oplysninger om afhængig > Orlov | <ul><li>Posten Oplysninger om afhængig oprettet, og **EhrLOAEffectiveDate** udfyldt</li><li>**personPrivateDetails.EhrIsLOA** er ændret (Ja eller Nej)</li><li>**personPrivateDetails.EhrLOAEffectiveDate** er ændret</li></ul> |
| **Ændring i dækning (stilling)** | <ul><li>Arbejder > Stillingstildeling > Tildeling af arbejderstillinger</li><li>Stillinger > Stillinger</li></ul> | <ul><li>Skift til stillingen i posterne for tildeling af arbejderstillinger</li><li>Ændring af arbejdertildelingen i stillingen</li></ul> |
| **Sygeforsikring (medarbejder/afhængig)** | Arbejder > Profil > Personlige oplysninger > Personlige kontakter > Oplysninger om afhængig > Ikrafttrædelsesdato for sygeforsikring | Udløses ikke automatisk, når en personlig kontakt angiver en ikrafttrædelsesdato. |
| **Støtte ifølge dommerkendelse** | Arbejder > Profil > Personlige oplysninger > Personlige kontakter > Afhængigt > Støtte ifølge dommerkendelse (QMSCO/QDRO) og ikrafttrædelsesdatoer | Udløser ikke automatiske opdateringer. Den ikke påvirker berettigelsen. Den registrerer en livshændelse. |
| **Medarbejders død** | Arbejder > Profil > > Personlige oplysninger > Dato for medarbejders død | Der angives en dato for medarbejders død |
| **EOI (forsikringsbar)** | <ul><li>Arbejder > Arbejder > Versioner > Ansættelseshistorik > Håndtering af datoer > Frynsegodedetaljer</li><li> Arbejder > Ansættelse > Oplysninger om frynsegoder > Bekræftelsesdato</li></ul> | <ul><li>En arbejder angiver en bekræftelsesdato</li><li>En arbejder angiver feltet EvidenceOfInsurability til **Ja**</li></ul> |
| **Modtager** | Arbejder > Profil > Personlige oplysninger > Personlige kontakter | Der tilføjes en personlig kontakt, og feltet **Modtager** og **Ikrafttrædelsesdato** udfyldes. Den personlige kontakt skal være af typen **Barn**, **Ægtefælle**, **Samlever**, **Søskende**, **Familiekontakt**, **Anden kontakt**, **Forælder**, **Ydelsesmodtagers ejendom**, **Modtagerorganisation** eller **Formueforvalter som modtager**. |
| **Medarbejders sygeforsikring** | Arbejder > Arbejder > Versioner > Ansættelseshistorik > Håndtering af datoer > Frynsegodedetaljer | <ul><li>**EhrMedicareEligibilityDate** er ændret</li><li>**MedicareEligibile** er angivet til **Ja**</li></ul> |
| **Fødselsdag** | Arbejder > Profil > Personlige oplysninger > Personlige kontakter > Oplysninger om afhængig > Fødselsdato | En fødselsdato tilføjes eller opdateres (ikke efter behandling af ændring af livshændelse). Eksempel: Hvis **Indstillinger for berettigelse for personlige kontakter** for et barn er angivet til Alder: 26 i Konfiguration > Frynsegoder > Indstillinger for berettigelse for personlige kontakter, og hvis HR-medarbejdere kører behandling af ændringer af livshændelser en hvilken som helst dag, efter at den afhængige er fyldt 26, vises der en meddelelse med en påmindelse om, at den afhængige ikke længere kan dækkes. |
| **Ændring af arbejders berettigelse (ikke specifik for USA)** | <ul><li>Arbejder > Ansættelse</li><li>Arbejder > Arbejder > Versioner > Ansættelseshistorik</li></ul> | <ul><li>Medarbejdertype, Ansættelseskategori eller de fem brugerdefinerbare berettigelsesfelter ændres</li><li>**HcmEmploymentDetail. EhrEmploymentType** ændres (behandles kun for *ændrede* ansættelsesposter med oplysninger, ikke for *nye* ansættelsesposter, f.eks. genansættelse og fratrædelse)</li></ul> |
| **Tilsidesættelse af ny berettigelse (ikke specifik for USA)** | Udvidet Human Resources > Frynsegoder > Planer > Frynsegoder > Tilsidesæt berettigelsesregler | Bruge behandling af livshændelse | EhrBenefitEligibilityRuleOverride.ValidFrom |
| **Ændring af tilsidesættelse af berettigelsesregler (ikke specifik for USA)** | Udvidet Human Resources > Frynsegoder > Planer > Frynsegoder > Tilsidesæt berettigelsesregler | Brug af behandling af livshændelser (kun **Gyldig fra**- og **Gyldig til**-felter under tilsidesættelse af berettigelsesregel) |
| **Udløb af tilsidesættelse af berettigelsesregler (ikke specifik for USA)** | Udvidet Human Resources > Frynsegoder > Planer > Frynsegoder > Tilsidesæt berettigelsesregler | Brug behandling af ændring af livshændelse. Hvis du f.eks. redigerer udløbsdatoen for tilsidesættelse af en plans berettigelsesregel til dags dato kl. 17:00, et hvilket som helst tidspunkt efter kl. 17:00 eller de følgende dage og derefter udfører behandling af ændringer af en livshændelse, vises der en meddelelse om, at tilsidesættelse af berettigelsesreglen er udløbet. |
| **Ny frynsegodeplan (ikke specifik for USA)** | Udvidet Human Resources > Frynsegoder > Planer > Ny | <ul><li>Berettigelsesindstillinger føjes til en aktuel plan</li><li>Der tilføjes en ny plan med tilknyttede berettigelsesindstillinger</li></ul></br></br>Human Resourcesmedarbejdere skal køre behandling af berettigelse til livshændelsen i denne forekomst. |
| **Ændring af berettigelsesregler (ikke specifik for USA)** | Udvidet Human Resources > Frynsegoder > Regler/indstillinger > Berettigelsesregler | Brug behandling af berettigelse til livshændelse. Logføres, når følgende værdier er ændret for **EhrBenefitEligibilityRule**-poster: **UseEmplCategory**, **UseEmplStatus** eller **UseEmplType**. Opdaterer kun livshændelsestransaktioner, der allerede findes for en ændret regel eller kriterier for berettigelse. |
