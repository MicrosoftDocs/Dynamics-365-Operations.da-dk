---
title: Nyheder eller ændringer i Dynamics 365 Talent (2. april 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/02/2019
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
ms.search.validFrom: 2019-04-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 04b5a006d4580fe419d81986a90851bc8d611722
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528213"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-2-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (2. april 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

### <a name="approval-emails-in-attract"></a>Godkendelsesmails i Attract
Nye godkendelsesmails forbedrer synligheden i godkendelsesprocessen. E-mails fremsendes til godkenderne, når et af følgende scenarier finder sted:

- En anmoder indgiver et job til godkendelse.
- Et job afslås eller godkendes.
- En godkender har ikke handlet på en godkendelsesanmodning inden 24 timer.

Du kan tilpasse indholdet af godkendelsesmails med de nye skabeloner.

### <a name="application-and-profile-attachments"></a>Vedhæftelse af ansøgning og profil
Forbedringer under fanen **Dokumenter** på ansøgnings- og talentpuljeprofiler, hvor både dokumentnavnet og -typen nu vises.

## <a name="changes-in-onboard"></a>Ændringer i Onboard
Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="coming-soon-attract-and-onboard"></a>Kommer snart (Attract og Onboard)

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Integration af Lifecycle Services (LCS) med rapportering af problemer
I Attract og Onboard vil problemer, der bliver rapporteret af slutbrugere via funktionen "rapporter et problem", nu automatisk oprette supportproblemer i kundens LCS-projekt. Administratorer kan derefter tildele problemerne og om fornødent indsende dem til Microsoft. Dette er i overensstemmelse med Core HR's håndtering af slutbrugernes supportproblemer.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR
Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2216.

### <a name="platform-update-25-for-finance-and-operations"></a>Platform update 25 til Finance and Operations
Du kan finde yderligere oplysninger om Platform update 25 til Finance and Operations under [Funktioner i prøveversionen af Dynamics 365 for Finance and Operations-platformsopdatering 25 (april 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-25).

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Avanceret lønsikkerhed (fast og variabel)
I mange organisationer har de ansvarlige for kompensationer og frynsegoder muligvis kun har adgang til visse kompensationsposter. Disse kan omfatte poster til ledere eller medarbejdere i bestemte områder. Denne ændring giver Personale mulighed for at administrere og vedligeholde kompensationsplaner for forskellige medarbejdergrupper i organisationen. Du kan tildele sikkerhedsroller til faste og variable planer. Disse sikkerhedsroller bestemmer adgangen til planer og hertil relaterede medarbejderdata, såsom løn eller bonusposter, således at alene de pågældende roller kan behandle kompensation for medarbejdergrupperne.

### <a name="upgrade-to-common-data-service"></a>Opgrader til Common Data Service
Fristerne for at opgradere til Common Data Service nærmer sig hurtigt. Log på Microsoft Power Apps Administration for at finde ud af, om din database skal opgraderes. Du kan finde flere oplysninger om frister og de nødvendige trin for at opgradere under [Opgrader til Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Som eksempel

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Tilladelse til angivelse af årsagskoder for orlovstyper
Organisationer har muligvis behov for yderligere oplysninger om fritidsanmodninger. Du kan nu angive årsagskoder for orlovstyper og give medarbejderne mulighed for at vælge en årsagskode på deres fritidsanmodninger.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Krav om årsagskoder for visse orlovstyper på fritidsanmodninger
Organisationer kræver muligvis årsagskoder for specifikke orlovstyper, når medarbejderne anmoder om fri. Dette kan skyldes firmapolitik eller lovkrav. Du kan nu angive, hvilke orlovstyper der kræver en årsagskode, og du kan kræve, at medarbejderne oplyser en årsagskode på deres fritidsanmodninger for den pågældende orlovstype.

## <a name="coming-soon"></a>Kommer snart

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Forbedringer i brugergrænsefladen for duplikeret medarbejderkontrol
Med denne ændring opdages dubletter i forbindelse med din indtastning i navnefelter, og der vises en status over antallet af fundne dubletter. Du kan vælge, at det angivne link skal åbne en ny side for at vurdere, om du ønsker at anvende det fundne match. Dubletformularen åbner ikke automatisk for at undgå forstyrrelser i forbindelse med indtastning af data.

###  <a name="email-support-for-alerts"></a>E-mailunderstøttelse til påmindelser
Med platformsopdatering 25 til Finance and Operations kan brugerne oprette påmindelsesregler, som automatisk fremsender mailbeskeder til kontaktpersoner, når de udløses af en hændelse. 
