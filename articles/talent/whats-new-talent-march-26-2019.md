---
title: Nyheder eller ændringer i Dynamics 365 Talent (26. marts 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b23860a7eda0ec9d75cca04728b7fc11d01bf967
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812735"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-26-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (26. marts 2019)

[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

### <a name="enhancements-to-interview-scheduling"></a>Forbedringer i samtaleplanlægning
Følgende forbedringer er til rådighed for planlægning af samtaler.

- Rekrutteringsmedarbejdere eller ansættelsesansvarlige kan nu manuelt udløse en påmindelse til en interviewer om at indsende en tilbagemelding. Den tilknyttede e-mailskabelon for påmindelsen kan ligeledes konfigureres.
- Når samtaleplanlæggeren deler samtaleoversigten med kandidaten, kan denne vælge at skjule navnet på interviewerne og ligeledes vælge at skjule rækker i sammendraget af samtaleoversigten.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

### <a name="embedded-images-in-activities"></a>Integrerede billeder i aktiviteter
Du kan nu integrere billeder direkte i aktiviteter. Udover at kunne kopiere og indsætte billeder fra internettet kan du også uploade billeder fra dit lokale filsystem. Størrelsen på aktiviteten er begrænset til 1 MB. Hvis billedet er for stort, skal du ændre størrelsen og prøve at uploade det igen.

[![Overførsel](./media/embedimages.png)](./media/embedimages.png)

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR
**Build 8.1.2210**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>Understøttelse til brugertilpassede felter er tilgængelig for udvalgte enheder i Common Data Service 

Følgende Common Data Service-enheder understøtter nu brugertilpassede felter, der oprettes i Talent:

- Arbejdstråd
- Etnisk oprindelse
- Veteranstatus
- Sprogkode
- Stilling
- Jobtype
- Jobfunktion
- Stilling
- Stillingstype
 
### <a name="employment-history-not-displayed-chronologically"></a>Medarbejderhistorikken vises ikke kronologisk
Med denne ændring vil medarbejderens historikside nu vise ansættelsesposterne i kronologisk orden uafhængigt af virksomheden. Du kan også bruge sorteringsindstillingerne til at sortere efter virksomhed.

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>Faste lønplaner vises ikke, når brugeren begrænses af virksomheden i relation til sikkerhed.
I forbindelse med denne udgivelse vil faste lønplaner nu blive vist, når brugerne begrænses af virksomheden i relation til sikkerhed. Alle sikkerhedsindstillinger bliver overholdt, og faste lønplaner vil blive vist for de virksomheder, som brugeren har rettighederne til at tilgå. 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>Kan ikke slette jobposter ved at anvende "Åben i Excel"-indstillingen i Talent
Med denne udgivelse kan du nu fjerne jobposterne ved at anvende indstillingen **Åbn i Excel** i Talent.

### <a name="upgrade-to-common-data-service"></a>Opgrader til Common Data Service
Fristerne for at opgradere til Common Data Service nærmer sig med hastige skridt. Log på Power Apps Administration for at finde ud af, om din database skal opgraderes. Du kan finde flere oplysninger om frister og de nødvendige trin for at opgradere under [Opgrader til Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Som eksempel

Du kan finde oplysninger om aktivering af funktioner til forhåndsvisning under [Få adgang til funktioner i prøveversioner af Microsoft Dynamics 365 Talent](./access-preview-feature.md).

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Tilladelse til angivelse af årsagskoder for orlovstyper
Organisationer har muligvis behov for yderligere oplysninger i forbindelse med fritidsanmodninger. For at få disse oplysninger er medarbejderne nødt til at angive en årsagskode, når de anmoder om fri. Med denne udgivelse kan du nu angive de årsagskoder, der er tilknyttet en given orlovstype, og give medarbejderne mulighed for at vælge en årsagskode på deres fritidsanmodninger.

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>Krav om konfigurering af årsagskoder for visse orlovstyper i forbindelse med indgivelse af fritidsanmodninger
Organisationer kan kræve, at der angives årsagskoder for specifikke orlovstyper, når medarbejderne anmoder om fri. Dette kan skyldes lovkrav i deres land/region eller firmapolitik. Denne udgivelse giver Personale mulighed for at angive, hvilke orlovstyper der kræver en årsagskode. Dette vil blive håndhævet, når medarbejderne indsender fritidsanmodninger, såfremt orloven kræver en årsagskode.

## <a name="coming-soon"></a>Kommer snart

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Avanceret lønsikkerhed (fast og variabel)
I mange organisationer har de ansvarlige for kompensationer og frynsegoder muligvis kun har adgang til visse kompensationsposter. Disse kan være til ledere eller medarbejdere i bestemte områder. Med denne ændring kan Personale administrere og vedligeholde kompensationsplaner for forskellige medarbejdergrupper i organisationen. Du kan tildele sikkerhedsroller til faste og variable planer, som bestemmer adgangen til planerne og medarbejderdata tilknyttet til planerne, såsom løn eller bonusposter. Alene de roller, der har fået tildelt adgang, kan behandle kompensation for disse medarbejdere.

###  <a name="email-support-for-alerts"></a>E-mailunderstøttelse til påmindelser
Med Platform update 25 til Finance and Operations kan brugerne oprette påmindelsesregler, som automatisk udsender mailbeskeder til kontakter, når beskeder udløses af en hændelse. 

### <a name="duplicate-employee-checks-user-interface-changes"></a>Duplikerede medarbejderkontroller: ændringer i brugergrænsefladen
Med denne ændring opdages dubletter i forbindelse med din indtastning i navnefelter, og der vises en status over antallet af fundne dubletter. Du kan vælge, at det angivne link skal åbne en ny side for at vurdere, om du ønsker at anvende det fundne match. Dubletformularen åbner ikke automatisk for at undgå forstyrrelser i forbindelse med indtastning af data.
