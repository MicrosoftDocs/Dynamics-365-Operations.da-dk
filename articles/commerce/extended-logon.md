---
title: Konfigurere og bruge den udvidede logonfunktionalitet
description: Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere og bruge den udvidede logonfunktionalitet til Microsoft Dynamics 365 Commerce POS-programmet.
author: boycez
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d211ecfe1550f6093e1d35e7c2b37c036b50dd4a
ms.sourcegitcommit: 5aebb181004eb63210503fb566dcda5c55032bee
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/29/2022
ms.locfileid: "8491433"
---
# <a name="set-up-and-use-the-extended-logon-capability"></a>Konfigurere og bruge den udvidede logonfunktionalitet

[!include [banner](includes/banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere og bruge den udvidede logonfunktionalitet til Microsoft Dynamics 365 Commerce POS-programmet.

Cloud POS (CPOS) og Modern POS (MPOS) giver en udvidet logonfunktionalitet, så detailbutiksmedarbejdere kan logge på POS-programmet ved at scanne en stregkode eller føre et kort gennem en magnetstribelæser (MSR).

## <a name="set-up-extended-logon"></a>Konfigurere udvidet logon

Hvis du vil konfigurere udvidet logon for POS-kasseapparater i en detailbutik, skal du følge disse trin.

1. Gå i Commerce-hovedkontoret til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**. 
2. Vælg den funktionalitetsprofil, der er tilknyttet detailbutikken, i navigationsruden til venstre.
3. Angiv følgende indstillinger til **Ja** eller **Nej** under **Yderligere indstillinger for logongodkendelse** i oversigtspanelet **Funktioner**:

    - **Logon med medarbejderstregkode** – Angiv denne indstilling til **Ja**, hvis arbejderne skal logge på POS ved at scanne en stregkode. 
    - **Medarbejderlogon med stregkode kræver adgangskode** – Angiv denne indstilling til **Ja**, hvis arbejderne skal angive en adgangskode, når de logger på POS ved at scanne en stregkode.
    - **Logon med medarbejderkort** – Angiv denne indstilling til **Ja**, hvis arbejderne skal logge på POS ved at bruge et kort.
    - **Logon med medarbejderkort kræver adgangskode** – Angiv denne indstilling til **Ja**, hvis arbejderne skal angive en adgangskode, når de logger på POS ved at bruge et kort.

Stregkoden eller kortet er knyttet til legitimationsoplysninger, der kan tildeles til en arbejder. Legitimationsoplysningerne skal indeholde mindst seks tegn. Den streng, der indeholder de første fem tegn, skal være entydig og betragtes som et *legitimations-id*, der bruges til at slå en arbejder op. De resterende tegn bruges til sikkerhedsbekræftelse. Du kan f.eks. have to kort, hvoraf det ene har legitimationsoplysningerne 12345DGYDEYTDW, og det andet har legitimationsoplysningerne 12345EWUTBDAJH. Da disse to kort har samme legitimations-id, 12345, kan de ikke begge tildeles til arbejdere.

## <a name="assign-extended-logon"></a>Tildele udvidet logon

Som standard er det kun chefer, der kan tildele udvidet logon til medarbejdere. Hvis du vil tildele udvidet logon, skal du gå til **Udvidet logon** i POS. Søg derefter efter en medarbejder ved at angive vedkommendes operatør-id i søgefeltet. Vælg medarbejderen, og klik derefter på **Tildel**. På næste side skal det udvidede logon stryges eller scannes for at tildele medarbejderen. Hvis strygningen eller scanning indlæses, bliver knappen **OK** tilgængelig. Klik på **OK** for at gemme det udvidede logon for den medarbejder.

## <a name="delete-extended-logon"></a>Slette udvidet logon

Hvis du vil slette det udvidede logon, der er tildelt til en medarbejder, søger du efter medarbejderen ved hjælp af handlingen **Udvidet logon**. Vælg medarbejderen, og klik derefter på **Fjern tildeling**. Alle udvidede logonoplysninger, som er knyttet til medarbejderen, er fjernet.

## <a name="use-extended-logon"></a>Bruge udvidet logon

Når udvidet logon er konfigureret, og en medarbejder har fået tildelt en stregkode eller magnetstribe, skal medarbejderen blot stryge eller scanne sit kort, mens POS-logonsiden vises. Hvis der også kræves en adgangskode, før logon kan fortsætte, bliver medarbejderen bedt om at indtaste sin adgangskode.

## <a name="extend-extended-logon"></a>Udvide udvidet logon

Standardimplementeringen af den udvidede logonfunktionalitet kræver, at legitimationsoplysningerne har en minimumlængde på seks tegn, og at de første fem tegn (legitimationsoplysnings-id) skal være entydige. Det var oprindeligt beregnet som et eksempel, som udviklere kunne tilpasse for at opfylde kravene til en bestemt implementering. (Det kan f.eks. være tilpasset for at understøtte flere tegn eller bruge forskellige regler for sikkerhedsbekræftelse). Du kan finde detaljerede oplysninger om, hvordan du bygger udvidelser til udvidet logon, under [Udvide den udvidede logonfunktionalitet til MPOS og Cloud POS](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/).

Logontjenesten kan også udvides til at understøtte yderligere enheder med udvidet logon, f.eks. håndfladescannere. Yderligere oplysninger finder du i [dokumentationen til POS-udvidelsesmuligheder](dev-itpro/pos-extension/pos-extension-overview.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
