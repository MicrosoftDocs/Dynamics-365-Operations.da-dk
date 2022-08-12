---
title: RCS (Regulatory Configuration Service) – Lifecycle Services (LCS)-lagerudfasning
description: Denne artikel indeholder oplysninger om den udfasning af Microsoft Dynamics Lifecycle Services-lager (LCS), der er planlagt som en del af udrulningen af det globale lager for Regulatory Configuration Service (RCS).
author: JaneA07
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: 65d45eaf618075e0c78881634fc77bda0fab277e
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065668"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>RCS (Regulatory Configuration Service) – Lifecycle Services (LCS)-lagerudfasning

[!include [banner](../includes/banner.md)]

Brugen af Microsoft Dynamics Lifecycle Services (LCS) som opbevaringslager for konfigurationer af elektronisk rapportering (ER) udfases. Denne udfasning omfatter følgende ændringer:

- Microsoft-producerede konfigurationer, der bruges i Microsoft Dynamics 365-programmer, vil ikke længere blive publiceret til biblioteket Delte aktiver i LCS. De vil i stedet kun blive publiceret via RCS Global-lageret. Konfigurationer til Dynamics AX 2012 vil dog fortsat blive udgivet til det delte aktivbibliotek i LCS, indtil den understøttende livscyklussen for AX 2012 slutter.
- De funktioner, du kan bruge til at uploade konfigurationer til biblioteket Projektaktiver i LCS fra programmer til finans og drift og fra RCS, deaktiveres. Du kan dog stadig bruge browseren i LCS til at uploade konfigurationer til biblioteket Projektaktiver. Du vil derfor stadig kunne føje konfigurationer til LCS, så de kan indgå i løsningspakker.
- Import af konfigurationer fra LCS vil fortsat være tilgængelig og understøttet i programmer til finans og drift og i RCS i en periode. Men funktionen vil i sidste ende blive udfaset? (Den præcise udfasningsdato oplyses senere).

## <a name="deprecation-notice"></a>Meddelelse om udfasning

Udfasning af brugen af LCS som lager blev oplyst i [Fjernede eller udfasede funktioner i Dynamics 365 Finance – Meddelelse om udfasning af LCS](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Den planlagte dato for udfasning er 1. april 2022.

## <a name="key-features"></a>Hovedfunktioner

- Bruge RCS til at oprette og redigere ER-konfigurationer og globaliseringsfunktioner.
- Push konfigurationer direkte fra RCS-designeren til et tilknyttet program, for eksempel et Dynamics 365 Finance-miljø, så du hurtigt kan foretage og teste ændringer i konfigurationerne.
- Du kan lagre, dele og administrere livscyklussen centralt for både ER-konfigurationer og globaliseringsfunktioner via det globale lagers centraliserede lager.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Vejledning til engangshandlinger og løbende handlinger

I dette afsnit beskrives et sæt trin, der skal fuldføres én gang. Det beskriver også trin, der skal udføres løbende bagefter.

### <a name="one-time-action"></a>Engangshandling

Importér alle nødvendige konfigurationer fra LCS til RCS, og publicer dem derefter fra RCS til det globale lager. Hvis du bruger projektspecifikke aktivbiblioteker til at gemme afledte konfigurationer i LCS, skal du følge nedenstående trin, mens LCS stadig er tilgængelig.

1. Hvis en RCS-forekomst ikke allerede er tilgængelig, kan du klargøre den. Du kan finde flere oplysninger under [Oversigt over RCS](rcs-overview.md).
2. I den klargjorte RCS-forekomst skal du registrere det relevante LCS-lager for alle LCS-projekter i aktivbiblioteket, som omfatter afledte ER-konfigurationer.
3. Importér ER-konfigurationerne fra LCS-lageret til RCS. Du kan finde flere oplysninger under [Importere konfigurationer fra LCS](/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services).
4. Hvis det globale lager ikke leveres automatisk, skal du registrere det i RCS.
5. Upload alle afledte konfigurationer fra den aktuelle RCS-forekomst til det globale lager. Brug funktionen **Konfigurationspakker** for at få hjælp til at uploade. Yderligere oplysninger finder du i [Uploade et globalt RCS-lager](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Næste trin

Brug de visuelle designere i RCS til følgende formål:

- Udvide de skabeloner, der er leveret af Microsoft.
- Oprette nye konfigurationer, som organisationen kræver.
- Tilpasse globaliseringsfunktionerne for elektronisk fakturering og tjenesten Momsberegning.

Brug globaliseringslageret til følgende formål:

- Få adgang til konfigurationer oprettet af Microsoft og globaliseringsfunktioner.
- Overføre konfigurationer, som du har oprettet eller udvidet til det globale lager til opbevaring, og dele dem på tværs af organisationens Dynamics 365-programmiljøer eller med eksterne organisationer. Du kan finde flere oplysninger under [Oprette ER-konfiguration i RCS og uploade til globalt lager](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Betyder denne ændring, at LCS ikke kan bruges som centrallager til konfigurationer?

Ja. De funktioner, du kan bruge til at uploade konfigurationer til biblioteket Projektaktiver i LCS fra programmer til finans og drift, udfases. Du kan dog stadig bruge browseren i LCS til at uploade konfigurationer til biblioteket Projektaktiver efter behov.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Jeg troede, at RCS var erstatningslager for import af globale skabelonfiler. Jeg vidste ikke, at det er brugt til butikskonfigurationer. Hvad er korrekt?

RCS er en designtjeneste til oprettelse og redigering af ER-konfigurationer. RCS har sit eget lager, der kaldes det globale lager. Dette lager bruges til at gemme konfigurationer, der er oprettet i RCS. Når brugen af LCS som lager er udfaset, vil det globale lager være den eneste kilde til Microsoft-konfigurationer. Du skal udføre en engangshandling for at importere alle de konfigurationer, du skal bruge, fra LCS til RCS og derefter publicere dem fra RCS til det globale lager.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Uden LCS hvad er så en foreslået metode til butikskonfigurationer, så konfigurationer af "test" og "produktion" nemt kan administreres og overføres?

RCS bruger begrebet *tilsluttet applikation*. Et tilsluttet applikation danner en forbindelse mellem RCS og alle forekomster af programmer til finans og drift. Da RCS kan bruges til at redigere konfigurationer, kan den tilsluttede applikation bruges til at overføre konfigurationerne direkte fra designeren til miljøer for programmer til finans og drift. Du kan derfor hurtigt ændre og teste konfigurationerne i stedet for at skulle gennemgå LCS-lagring på projektniveau.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Er der nogen eksempler, der viser opsætningen og administrationen?

Der er ingen eksempler, men du kan udføre trinnene tidligere i denne artikel for at overflytte dine konfigurationer til det globale RCS-lager.

### <a name="is-rcs-a-prerequisite-to-configure-electronic-reporting"></a>Er RCS en forudsætning for at kunne konfigurere elektronisk rapportering?

Ja. RCS indeholder egenskaber, der understøtter opsætningen af globaliseringsfunktioner, som bruges af globaliseringstjenester som for eksempel tjenesten Elektronisk fakturering og Momsberegning. Tjenesten har dog de samme funktioner til visuel design, som giver dig mulighed for at udvide eller oprette nye ER-konfigurationer. RCS leverer også livscyklusstyring til både ER-konfigurationer og globaliseringsfunktioner.

### <a name="which-regions-can-rcs-be-deployed-in"></a>Hvilke områder kan RCS implementeres i?

RCS er tilgængelig i følgende Azure-områder:

- USA
- Indien
- Frankrig
- Europa

Du kan finde flere oplysninger om produktsupport i [oversigten Dynamics-globaliseringstjenester](globalization-services-overview.md). Du kan finde flere oplysninger om geografisk support i [Dynamics 365 og Power Platform : Tilgængelighed, dataplacering, sprog og lokalisering](https://aka.ms/rcs/D365Productavailabilityguide).

### <a name="whats-the-cost-of-using-rcs"></a>Hvad er omkostningerne for at bruge RCS?

RCS og globaliseringslageret leveres gratis som en del af eksisterende licenser til programmer til finans og drift. Der er ikke særlige omkostninger for brugen af RCS-designtjenesten eller lagring af konfigurationer i det globale lager. Der er i øjeblikket ingen grænser for antallet af konfigurationer eller tilknyttede programmer.
