---
title: Oprette firmaspecifikke parametre for personale
description: "Indstillingerne for nogle parametre for personale (HR) deles på tværs af firmaer, mens indstillingerne for andre parametre er firmaspecifikke. Denne artikel forklarer, hvordan du konfigurerer virksomhedsspecifikke parametre for personale."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: aaf5c93a1ac71de27338c13218407616808ee001
ms.openlocfilehash: 39f2904a6b722ad0048ba1d94651098ee642079b
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-company-specific-hr-parameters"></a>Oprette firmaspecifikke parametre for personale

Indstillingerne for nogle parametre for personale (HR) deles på tværs af firmaer, mens indstillingerne for andre parametre er firmaspecifikke. Denne artikel forklarer, hvordan du konfigurerer virksomhedsspecifikke parametre for personale.

To sider bruges til at angive personaleparametre. For parametre, der deles på tværs af firmaer, skal du bruge siden **Delte parametre for personale**. For parametre, der er specifikke for virksomheden (med andre ord gælder indstillingerne for en enkelt virksomhed), skal du bruge siden **Personaleparametre**. På siden **Personaleparametre** er indstillingerne fordelt på seks faner:

-   Generel
-   Rekruttering
-   Kompensation
-   Nummerserier
-   Family and Medical Leave Act (FMLA)
-   Medarbejderselvbetjening

Hver fane indeholder oplysninger, der vedrører en enkelt virksomhed. Indstillingerne på fanen **Generelt** definerer visningen af oplysninger om fravær, skader og sygdom og nye ansættelser. Indstillingerne på denne fane kan også definere nogle standardposter, der vises, mens du arbejder. Specifikt giver denne fane dig mulighed for at vælge en farve, der skal anvendes på åbne fraværsposter, angive typografiark, der skal bruges til rapporter, angive integration mellem undervisningskurser og fraværsregistrering og vælge den fraværskode, der skal bruges til at styre denne integration. Du kan også angive, hvor længe sager om skader og sygdom skal opbevares, og angiv standardidentifikationsnummeret, der vises, når en ny medarbejder ansættes. 

Indstillingerne på fanen **Rekruttering** definerer de dokumenttyper, der bruges til korrespondance, der automatisk sendes til ansøgere og det rekrutteringsprojekt, der bruges til uopfordrede ansøgninger (ansøgninger, der ikke er til et bestemt rekrutteringsprojekt). Den periode, der er defineret for det aldersfordelte rekrutteringsprojekt bestemmer rekrutteringsprojekter, der er medtaget i feltet **Aldersfordelte projekter** i arbejdsområdet **Rekrutteringsstyring**. Den periode, der er defineret for advarsel om deadline for ansøgning bruges til at få vist rekrutteringsprojekter, der nærmer sig deres ansøgningsfrist i feltet den **Deadline for ansøgning nærmer sig** i arbejdsområdet **Rekruttering**. 

Indstillingerne på den **løn** fane definerer, om brugere skal bekræfte, at de vil gemme oplysninger om en fast eller variabel lønstruktur. Hvis du vælger den **Aktiver Gem validering** afkrydsningsfelt, helst brugere om at lukke en kompensation-relaterede side, vises en meddelelse, der spørger, om de vil gemme posten. Nogle sider i kompensationsstyring lade ikke brugere slette oplysninger. Når brugeren får besked på at bekræfte, om oplysningerne skal gemmes, kan det hjælpe med at begrænse mængden af oplysninger, der gemmes, men ikke senere kan slettes. Hvis afkrydsningsfeltet **Aktiver validering ved lagring** ikke er markeret, gemmes poster altid med det samme, eventuelt før brugeren er klar. Hvis du bruger performancestyring, giver fanen **Kompensation** dig også mulighed for at vælge en rangeringsmodel, der skal bruges i stedet for den model, der er tildelt til kompensationsstrukturerne, når performance vurderes. 

Indstillingerne på fanen **Nummerserie** bestemmer de serier, der skal bruges til automatisk tildeling af id'er til elementer i personalemodulet, f.eks. ansøgninger, fraværsregistreringer, kompensationsprocesresultater, sagsnumre, kurser og kursusagendaer. Hvis du vil vedligeholde nummerseriereferencer og -koder, kan du bruge den **nummerserier** listeside (Klik på **virksomhedsadministration**&gt;**nummerserier**&gt;**nummerserier**). 

Indstillingerne på fanen **FMLA** definerer, hvor mange timer en medarbejder skal arbejde for at være berettiget til FMLA-ydelser, længde af beskæftigelse, der kræves for berettigelse og beskæftigelsens startdato, der bruges til at bestemme længden af beskæftigelse. Indstillingerne også definere antallet af FMLA-timer, som medarbejderne har ret til, og FMLA-orlovskalender, der bruges til at beregne, hvor mange FMLA-timer medarbejdere har brugt. Fanen **FMLA** er kun tilgængelig for virksomheder i USA. 

**Bemærk:** Antallet timer, der er arbejdet, må ikke overstige 1,250, og længden af beskæftigelsen må ikke overstige 12 måneder. Disse maksimale værdier er i overensstemmelse med gældende lovgivning i USA. Endeligt angiver indstillingerne på fanen **Medarbejderselvbetjening** de oplysninger, som en leder kan angive på vegne af hans eller hendes medarbejdere.

<a name="see-also"></a>Se også
--------

[Konfigurer parametre for personale på tværs af juridiske enheder](set-up-hr-parameters-across-legal-entities.md)

