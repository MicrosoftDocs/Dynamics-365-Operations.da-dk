---
title: Nyheder eller ændringer i Dynamics 365 Talent (23. april 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
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
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 53faf972759c8f770017fcd3a87920410988e626
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527171"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-23-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (23. april 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract
Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Ændringer i Onboard
Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR
Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2253. Tal i parenteser henviser til supportnumre i Lifecycle Services (LCS).

### <a name="common-data-service-entity-support-for-custom-fields"></a>Understøttelse i Common Data Service-enheden af brugerdefinerede felter
Med denne uges udgivelse understøtter følgende enheder brugerdefinerede felter: kompensationsniveau, frynsegodeindstilling, færdighedstype og kompensationsområde.

### <a name="additional-odata-entities-302992"></a>Yderligere OData-enheder (302992)
Følgende enheder understøttes nu i OData: arbejders erhvervserfaring og arbejderuddannelse.
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a>Vedhæftede filer til performancekladde for ledere og medarbejdere (308248)
Med denne version er de vedhæftede filer nu tilgængelige for både ledere og medarbejdere ved oprettelse og opdatering af performancekladdeposter.

### <a name="employee-rehire-flag-always-available-310047"></a>Flag for genansættelse af medarbejder er altid tilgængeligt (310047)
Du kan nu opdatere indstillingen til genansættelse af medarbejdere uden for fratrædelsesprocessen. 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a>Det er ikke muligt at ændre navnet på **Min betalingsmetode** (308815)
Personlig tilpasning er aktiveret, så det er muligt at ændre etiketten **Min betalingsmetode** i Medarbejderselvbetjening.

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a>Økonomiske dimensioner i forhold til en stilling kan ikke slettes (293908)
Økonomiske dimensioner kan nu fjernes, når der anmodes om en ændring af en eksisterende stilling, og de økonomiske dimensioner krydser firmaets grænser. 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a>Debitor kan ikke publicere data i Talent, når dataene åbnes fra Excel (302955)
Denne ændring løser et udgivelsesproblem, når der bruges relaterede tabeller.

## <a name="in-preview"></a>Som eksempel

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Tilladelse til angivelse af årsagskoder for orlovstyper
Organisationer har muligvis behov for yderligere oplysninger om fritidsanmodninger. Du kan nu angive årsagskoder for orlovstyper og give medarbejderne mulighed for at vælge en årsagskode på deres fritidsanmodninger.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Krav om årsagskoder for visse orlovstyper på fritidsanmodninger
Organisationer kræver muligvis årsagskoder for specifikke orlovstyper, når medarbejderne anmoder om fri. Dette kan skyldes firmapolitik eller lovkrav. Du kan nu angive, hvilke orlovstyper der kræver en årsagskode, og du kan kræve, at medarbejderne oplyser en årsagskode på deres fritidsanmodninger for den pågældende orlovstype.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Udarbejdelse af en transaktionsliste over orlov og fravær til Personale
Sporing af medarbejdernes fridage og forståelse af, hvordan fridagene beregnes, hjælper ikke blot Personale med at besvare medarbejdernes spørgsmål, men sikrer endvidere, at medarbejderne tildeles den korrekte mængde fridage. Personale har nu fået et nyt indblik i transaktionerne (tilskud, periodiseringer, reguleringer og anmodninger) og kan derved se de bagvedliggende årsager til saldiene.

## <a name="coming-soon"></a>Kommer snart

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Forbedringer i brugergrænsefladen for duplikeret medarbejderkontrol
Med denne ændring opdages dubletter i forbindelse med din indtastning i navnefelter, og der vises en status over antallet af fundne dubletter. Du kan vælge, at det angivne link skal åbne en ny side for at vurdere, om du ønsker at anvende det fundne match. Dubletformularen åbner ikke automatisk for at undgå forstyrrelser i forbindelse med indtastning af data.
## <a name="known-issues"></a>Kendte problemer

### <a name="email-support-for-alerts"></a>E-mailunderstøttelse til påmindelser
Med platformsopdatering 26 til Finance and Operations kan brugerne oprette påmindelsesregler, som automatisk fremsender mailbeskeder til kontaktpersoner, når de udløses af en hændelse.


[!INCLUDE[footer-include](../includes/footer-banner.md)]