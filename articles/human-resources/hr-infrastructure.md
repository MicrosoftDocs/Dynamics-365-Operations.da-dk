---
title: Dynamics 365 Human Resources-infrastrukturfletning - Opdateringsversion 10.0.25
description: Dette emne indeholder oplysninger om Microsoft Dynamics 365 Human Resources version 10.0.25, som udgør den første bølge af egenskaber i fletningen af infrastrukturen.
author: twheeloc
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a80bedd0224f1e31dfec4e9f4c39ad1ed75d7f2f
ms.sourcegitcommit: 948978183a1da949e35585b28b8e85a63b6c12b1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/25/2022
ms.locfileid: "8024561"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Dynamics 365 Human Resources-infrastrukturfletning - Opdateringsversion 10.0.25

Med version 10.0.25 kommer den første bølge af egenskaber i fletningen af infrastrukturen. Under fletningen af infrastrukturen flettes Microsoft Dynamics 365 Human Resources sammen med infrastrukturen for Finans og drift. Det vil dog fortsat være licenseret som et uafhængigt program, ligesom Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Yderligere oplysninger om fletning af infrastrukturen finder du i [Ofte stillede spørgsmål om fletning af Dynamics 365 Human Resources-infrastruktur](../human-resources/hr-infrastructure-merge-faq.md).

Fletningen giver konsistens for brugere af Human Resources på følgende måder:

- [Miljøstyring og integrationer er konsistente mellem Human Resources og Finans- og driftsapps.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Administrer miljøer i Microsoft Dynamics Lifecycle Services, problemsøgning og Regression Suite Automation Tool.
    - Der findes en enkelt kodebase, hvor de nye funktioner til Human Resources frigives som del af den almindelige opdateringsproces One Version.
    - Den måde, som opgraderinger, opdateringer og hotfixes anvendes på i miljøer, er ensartet.

- [Der er forbedrede udvidelsesmuligheder.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options.md)

    - Du kan fortsætte med at bruge Microsoft Power Platform Tools til at udvide efter behov.
    - Du kan udvide funktionerne via formularer, tabeller, metoder og API'er (Application Programming Interface).
    - Du kan oprette og udvide enheder.

    Du kan finde flere oplysninger om de tilgængelige udvidelsesmuligheder i [Oversigt over udvidelsesmuligheder i Dynamics 365](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

- [Opret ét sæt Human Resources-egenskaber i Dynamics 365.](/dynamics365-release-plan/2021wave2/human-resources/create-one-set-human-resources-capabilities-within-dynamics-365.md)

    I version 10.0.25 er funktionsegenskaber, der kun fandtes i Human Resources, tilgængelige i infrastrukturen for Finans og drift. For at kunderne kan få glæde af disse funktioner i et Finans- og driftsmiljø, skal følgende Human Resources-funktioner være aktiveret i Funktionsstyring.

    | Funktionsnavn | Overblik | Status for frigivelse | 
    |--------------|----------|----------------| 
    | Beregning af Antal års tjeneste | Med en opsætningsindstilling kan du vælge den dato, der bruges til beregning af **Antal års tjeneste**. | Generelt tilgængelig | 
    | Udvidelser til arbejdsgangoplevelsen | Denne funktion giver en forbedret brugeroplevelse ved afsendelse og godkendelse af arbejdsproces. | Generelt tilgængelig | 
    | Udskriv ydeevneevalueringer | Du kan udskrive evalueringer af ydeevne i PDF-format. | Generelt tilgængelig | 
    | Brugerdefinerede links i **Selvbetjening for leder** | Du kan oprette brugerdefinerede links, der vises i afsnittet **Relaterede links** i **Selvbetjening for leder**. | Generelt tilgængelig | 
    | Visning af kompensation på tværs af firmaer | Brugere kan få vist lønstrukturer i **Selvbetjening for leder** på tværs af alle juridiske enheder uden at skulle skifte firmaer. | Generelt tilgængelig | 
    | Konfigurere flere kompensationsniveauer efter job\*&dagger; | Flere kompensationsniveauer understøttes nu for job. | Prøveversion | 
    | Opgavestyring\* | Du kan oprette checklister og opgaver til onboarding-, offboarding- og stillingsskifteprocessen. | Prøveversion | 
    | Strømlinet medarbejderindtastning | Denne funktion giver en opdateret brugeroplevelse på den eksisterende **Arbejder**-side. | Prøveversion | 
    | Forbedringer af brugeroplevelsen for Personale | Se tabellen i næste afsnit.  | Prøveversion | 

\* Denne funktion skal være aktiveret, før funktionen **Forbedringer af brugeroplevelsen med Human Resources**.

&dagger; Denne funktion kan ikke deaktiveres, når den er aktiveret.

## <a name="human-resource-user-experience-enhancements"></a>Forbedringer af brugeroplevelsen i Human Resources

| Funktionsnavn | Overblik | 
|--------------|----------| 
| Slet ansættelse | Du kan slette en ansættelse af en medarbejder. | 
| Jobfamilier | Du kan spore en gruppe job, der involverer lignende arbejde, og som kræver lignende uddannelse, færdigheder, viden og ekspertise. | 
| Yderligere ansættelsesfelter | Følgende felter blev tilføjet: **Ansættelseskategori**, **Ansættelsestype** og **Ansættelsesstatus**. | 
| Siden **Arbejdere uden ansættelse** | På en side vises en liste over arbejdere, der ikke har en ansættelsespost. | 
| Opdatering af brugeroplevelse i stillingsdimension | Der er en forbedret brugeroplevelse med tildeling af stillingsdimensioner pr. juridisk enhed. | 
| Adresseændringer i arbejdsområdet **Personalestyring** | Denne funktion viser antallet af alle adresseændringer, der er foretaget i løbet af det antal dage, der er angivet på siden **Human Resources-parametre**. | 
| Poster, der udløber, i arbejdsområdet **Personalestyring** | Denne funktion indeholder en liste over elementer, der er udløbet eller vil udløbe for certifikater, identifikationer, prøvetider, screeninger eller test. | 
| Siden **Validering af stillingshierarki** | Der kontrolleres for cirkulære referencer i stillingslinjehierarkiet. | 
| Landespecifikke lønoplysninger | Yderligere lønfelter er tilgængelige på siden **Arbejderansættelse**, afhængigt af landet eller området i den juridiske enhed, hvor arbejderne er ansat. | 
| Forbedret rapportering af overholdelse af angivne standarder | Der er flere tilgængelige rapporteringsindstillinger for EKH-1, Vets 4212 og OSHA300a. | 
| Opdateringer til arbejdsområdet **Personalestyring** | Der er foretaget opdateringer til sporing af adresseændringer og poster, der udløber. Nye faner viser desuden arbejder- og stillingshandlinger. | 
