---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (13. april 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 711cc4491024e647429b108438ce1d88483ea63c
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259811"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (13. april 2020)

I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3136. Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.

## <a name="new-production-release-cadence"></a>Ny udgivelsestakt for produktionsudgivelser

Med denne uges udgivelse skifter udgivelsestakten for Human Resources fra en ugentlig opdatering til en opdatering hver anden uge. Hvis du vil sikre en justering med sikker implementeringspraksis og vedligeholde høje standarder for stabilitet og pålidelighed i tjenesten, vil processen med at implementere tjenesteopdateringer til alle områder nu være en fase på to uger. Yderligere test og skærme er på plads for at sikre en vellykket implementering på hvert trin i processen. Du kan få flere oplysninger om frigivelsestakt i [Opdateringsproces](hr-admin-setup-update-process.md).

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>Feltet Afrundingspræcision kan ikke redigeres, når der er angivet en Afrundingstype (435616)

Med denne ændring er feltet **Afrundingspræcision** tilgængeligt, når du har opdateret feltet **Afrundingstype**.

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>Kan ikke redigere orlovstilmeldingens slutdatoen, når orlovsplanen ikke har periodiseringsperioder (413628)

Du kan nu redigere orlovstilmeldings slutdatoen, uden at fejlen "Udgangspunktet for feltet periodisering af felter skal udfyldes" vises.

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a>Ansættelsesenhed synkroniseres ikke med Common Data Service (430834)

Denne ændring retter et problem, hvor ansættelsesdataene ikke blev synkroniseret til Common Data Service, efter at der er tilføjet økonomiske dimensioner. 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>Fjern multiovervågning for enheden Arbejdskalenderens tidsinterval (431775)

Denne ændring fjerner multiovervågning for enheden **Arbejdskalenderens tidsinterval**.

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>Filteret med CAST-funktionen fungerer ikke på OData-kaldets enhed Arbejdertildeling til stilling (431699)

Denne opdatering indeholder en ændring, der giver mulighed for at filtrere med CAST-funktionen i OData for enheden **Arbejdertildeling til stilling** .

## <a name="in-preview"></a>Som prøveversion

## <a name="leave-suspension"></a>Forlad suspension

Du kan afbryde orlov og fravær i Human Resources for en medarbejder. Når du suspendere orlov, stoppes orloven for de valgte orlovstyper. Hvis suspensionen finder sted, når en periodisering er blevet behandlet, opretter suspensionen en forholdsmæssig justering til medarbejderens orlov. Du kan finde flere oplysninger i [Suspender orlov](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Overføre regler

Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres. Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage. Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværstyper ](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Kendte problemer

## <a name="employment-details-entity"></a>Enhed med ansættelsesdetaljer

Enheden **Ansættelsesdetaljer** er blevet opdateret med følgende felter:

- **Betalingsfrekvens**
- **Ansættelseskategori-id**
- **Medarbejdertype**
- **Ansættelsestype-id**
- **Status for frynsegodeansættelse**

Opsætningsdataene for disse felter afhænger af, at administration af frynsegoder er aktiveret i arbejdsområdet **Funktionsstyring**. Du må ikke udfylde eller opdatere disse felter i enheden **Ansættelsesoplysninger**, da det vil resultere i fejl under importen.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>Prøveversionen af SharePoint fungerer ikke i visse miljøer

Hvis visning af dokumenter, der er gemt i SharePoint, ikke fungerer, kan du prøve følgende procedure:

1. Kontroller, at administratorbrugerkontoen har en mail tilknyttet brugerposten. Du kan få vist disse oplysninger på siden **Bruger**. Hvis e-mail ikke er konfigureret, skal du tilføje e-mailadressen og udbyderen med OData Excel-tilføjelsesprogrammet. E-mailadressen findes som standard ikke i Excel-designet. Du skal redigere Excel-designet, tilføje alle felter, anvende og opdatere. Når du har fuldført disse trin, kan du opdatere administratorkontoen.

2. Når administratorkontoen har en tilknyttet mailkonto, skal du logge på Personale med administrator-legitimationsoplysninger.

3. Åbn en vedhæftet fil i SharePoint for at starte dokumentvisningen.

4. Log på med en anden brugerkonto, der har adgang til vedhæftede filer, og kontroller, at eksempelvisningen fungerer som forventet.