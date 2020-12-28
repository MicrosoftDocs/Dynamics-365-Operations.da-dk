---
title: Konfigurere personaleparametre
description: Indstillingerne for nogle personaleparametre (HR) deles på tværs af firmaer, mens indstillingerne for andre parametre er firmaspecifikke. Denne artikel forklarer, hvordan du konfigurerer virksomhedsspecifikke parametre for personale.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bac50c5f302797e28df2bc792893c8a682899a93
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417749"
---
# <a name="configure-human-resources-parameters"></a>Konfigurere personaleparametre

Indstillingerne for nogle parametre for personale (HR) deles på tværs af firmaer, mens indstillingerne for andre parametre er firmaspecifikke. Denne artikel forklarer, hvordan du konfigurerer virksomhedsspecifikke parametre for personale.

To sider bruges til at angive personaleparametre. For parametre, der deles på tværs af firmaer, skal du bruge siden **Delte parametre for personale**. For parametre, der er specifikke for virksomheden (med andre ord gælder indstillingerne for en enkelt virksomhed), skal du bruge siden **Personaleparametre**. På siden **Personaleparametre** er indstillingerne fordelt på seks faner:

-   Almindelig
-   Rekruttering - dette er ikke inkluderet i Dynamics 365 Human Resources
-   Kompensation
-   Nummerserier
-   Family and Medical Leave Act (FMLA)
-   Medarbejderselvbetjening

Hver fane indeholder oplysninger, der vedrører en enkelt virksomhed. Indstillingerne på fanen **Generelt** definerer visningen af oplysninger om fravær, skader og sygdom og nye ansættelser. Indstillingerne på denne fane kan også definere nogle standardposter, der vises, mens du arbejder. Specifikt giver denne fane dig mulighed for at vælge en farve, der skal anvendes på åbne fraværsposter, angive typografiark, der skal bruges til rapporter, angive integration mellem undervisningskurser og fraværsregistrering og vælge den fraværskode, der skal bruges til at styre denne integration. Du kan også angive, hvor længe sager om skader og sygdom skal opbevares, og angiv standardidentifikationsnummeret, der vises, når en ny medarbejder ansættes. 

Indstillingerne på fanen **Rekruttering** definerer de dokumenttyper, der bruges til korrespondance, der automatisk sendes til ansøgere og det rekrutteringsprojekt, der bruges til uopfordrede ansøgninger (ansøgninger, der ikke er til et bestemt rekrutteringsprojekt). Den periode, der er defineret for det aldersfordelte rekrutteringsprojekt bestemmer rekrutteringsprojekter, der er medtaget i feltet **Aldersfordelte projekter** i arbejdsområdet **Rekrutteringsstyring**. Den periode, der er defineret for advarsel om deadline for ansøgning bruges til at få vist rekrutteringsprojekter, der nærmer sig deres ansøgningsfrist i feltet den **Deadline for ansøgning nærmer sig** i arbejdsområdet **Rekruttering**. 

Indstillingerne under fanen **Kompensation** definerer, om brugere skal bekræfte, at de vil gemme oplysninger om en fast eller variabel lønstruktur. Hvis du vælger afkrydsningsfeltet **Aktivér validering ved lagring**, får brugerne vist en meddelelse, hver gang de lukker en kompensationsrelateret side, hvor de bliver spurgt, om de vil gemme posten. Nogle sider inden for kompensationsstyring giver ikke brugerne mulighed for at slette information. Når brugeren får besked på at bekræfte, om oplysningerne skal gemmes, kan det hjælpe med at begrænse mængden af oplysninger, der gemmes, men ikke senere kan slettes. Hvis afkrydsningsfeltet **Aktiver validering ved lagring** ikke er markeret, gemmes poster altid med det samme, eventuelt før brugeren er klar. Hvis du bruger performancestyring, giver fanen **Kompensation** dig også mulighed for at vælge en rangeringsmodel, der skal bruges i stedet for den model, der er tildelt til kompensationsstrukturerne, når performance vurderes. 

### <a name="previously-released-functionality"></a>Tidligere frigiven funktionalitet

Indstillingerne på fanen **Nummerserie** bestemmer de serier, der skal bruges til automatisk tildeling af id'er til elementer i personalemodulet, f.eks. ansøgninger, fraværsregistreringer, kompensationsprocesresultater, sagsnumre, kurser og kursusagendaer. Hvis du vil vedligeholde nummerseriereferencer og -koder skal du bruge listesiden **Nummerserier** (klik på **Organisationsadministration** &gt; **Nummerserier** &gt; **Nummerserier**).

> [!NOTE]
> Antallet af timer, der er arbejdet, må ikke overstige 1.250, og længden af beskæftigelsen må ikke overstige 12 måneder. Disse maksimale værdier er i overensstemmelse med gældende lovgivning i USA. Endeligt angiver indstillingerne under fanen **Medarbejderselvbetjening** de oplysninger, som ledere kan angive på vegne af deres medarbejdere.
