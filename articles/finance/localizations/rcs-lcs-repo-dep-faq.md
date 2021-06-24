---
title: RCS (Regulatory Configuration Service) – Lifecycle Services (LCS)-lagerudfasning
description: Dette emne indeholder oplysninger om den udfasning af Microsoft Dynamics Lifecycle Services-lager (LCS), der er planlagt som en del af udrulningen af det globale lager for Regulatory Configuration Service (RCS).
author: JaneA07
ms.date: 05/25/2021
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
ms.openlocfilehash: abaeb34db1d209fa8e5cc83a98c333f42e91f2d2
ms.sourcegitcommit: 7cda434becd198c1cd405e001289777ae7a24fe1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/01/2021
ms.locfileid: "6127913"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>RCS (Regulatory Configuration Service) – Lifecycle Services (LCS)-lagerudfasning

[!include [banner](../includes/banner.md)]

Brugen af Microsoft Dynamics Lifecycle Services (LCS) som opbevaringslager for konfigurationer af elektronisk rapportering (ER) udfases. Denne udfasning omfatter følgende ændringer:

- Microsoft-producerede konfigurationer, der bruges i Microsoft Dynamics 365-programmer, vil ikke længere blive publiceret til biblioteket Delte aktiver i LCS. De vil i stedet kun blive publiceret via RCS Global-lageret. Konfigurationer til Dynamics AX 2012 vil dog fortsat blive udgivet til det delte aktivbibliotek i LCS, indtil den understøttende livscyklussen for AX 2012 slutter.
- De funktioner, du kan bruge til at uploade konfigurationer til biblioteket Projektaktiver i LCS fra Finance and Operations-apps og fra RCS, deaktiveres. Du kan dog stadig bruge browseren i LCS til at uploade konfigurationer til biblioteket Projektaktiver. Du vil derfor stadig kunne føje konfigurationer til LCS, så de kan indgå i løsningspakker.
- Import af konfigurationer fra LCS vil fortsat være tilgængelig og understøttet i Finance and Operations-apps og i RCS i en periode. Men funktionen vil i sidste ende blive udfaset? (Den præcise udfasningsdato oplyses senere).

## <a name="deprecation-notice"></a>Meddelelse om udfasning

Udfasning af brugen af LCS som lager blev oplyst i [Fjernede eller udfasede funktioner i Dynamics 365 Finance – Meddelelse om udfasning af LCS](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Den planlagte dato for udfasning er 1. april 2022.

## <a name="key-features"></a>Hovedfunktioner

- Du kan bruge RCS til at oprette og redigere konfigurationer. Derefter kan du flytte konfigurationerne direkte fra designeren til et tilknyttet program. Du kan derfor hurtigt ændre og teste konfigurationerne.
- Global-lageret er det centraliserede lager for alle ER-konfigurationer.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Vejledning til engangshandlinger og løbende handlinger

I dette afsnit beskrives et sæt trin, der skal fuldføres én gang. Det beskriver også trin, der skal udføres løbende bagefter.

### <a name="one-time-action"></a>Engangshandling

Importér alle nødvendige konfigurationer fra LCS til RCS, og publicer dem derefter fra RCS til det globale lager. Hvis du bruger projektspecifikke aktivbiblioteker til at gemme afledte konfigurationer i LCS, skal du følge nedenstående trin, mens LCS stadig er tilgængelig.

1. Hvis en RCS-forekomst ikke allerede er tilgængelig, kan du klargøre den. Du kan finde flere oplysninger under [Oversigt over RCS](rcs-overview.md).
2. I den klargjorte RCS-forekomst skal du registrere det relevante LCS-lager for alle LCS-projekter i aktivbiblioteket, som omfatter afledte ER-konfigurationer.
3. Importér ER-konfigurationerne fra LCS-lageret til RCS. Du kan finde flere oplysninger under [Importere konfigurationer fra LCS](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md).
4. Hvis det globale lager ikke leveres automatisk, skal du registrere det i RCS.
5. Upload alle afledte konfigurationer fra den aktuelle RCS-forekomst til det globale lager. Brug funktionen **Konfigurationspakker, der giver brugeren mulighed for at uploade alle konfigurationer til GR i én handling** som en hjælp til upload. Yderligere oplysninger finder du i [Uploade et globalt RCS-lager](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Næste trin

Brug de visuelle designere i RCS til at oprette alle nye konfigurationer. Upload derefter konfigurationerne til opbevaring i det globale lager. Du kan finde flere oplysninger under [Oprette ER-konfiguration i RCS og uploade til globalt lager](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Betyder denne ændring, at LCS ikke kan bruges som centrallager til konfigurationer?

Ja. De funktioner, du kan bruge til at uploade konfigurationer til biblioteket Projektaktiver i LCS fra Finance and Operations-apps, udfases. Du kan dog stadig bruge browseren i LCS til at uploade konfigurationer til biblioteket Projektaktiver efter behov.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Jeg troede, at RCS var erstatningslager for import af globale skabelonfiler. Jeg vidste ikke, at det er brugt til butikskonfigurationer. Hvad er korrekt?

RCS er en designtjeneste til oprettelse og redigering af ER-konfigurationer. RCS har sit eget lager, der kaldes det globale lager. Dette lager bruges til at gemme konfigurationer, der er oprettet i RCS. Når brugen af LCS som lager er udfaset, vil det globale lager være den eneste kilde til Microsoft-konfigurationer. Du skal udføre en engangshandling for at importere alle de konfigurationer, du skal bruge, fra LCS til RCS og derefter publicere dem fra RCS til det globale lager.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Uden LCS hvad er så en foreslået metode til butikskonfigurationer, så konfigurationer af "test" og "produktion" nemt kan administreres og overføres?

RCS bruger begrebet *tilsluttet applikation*. Et tilsluttet applikation danner en forbindelse mellem RCS og alle forekomster af Finance and Operations-apps. Da RCS kan bruges til at redigere konfigurationer, kan den tilsluttede applikation bruges til at overføre konfigurationerne direkte fra designeren til Finance and Operations-appmiljøer. Du kan derfor hurtigt ændre og teste konfigurationerne i stedet for at skulle gennemgå LCS-lagring på projektniveau.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Er der nogen eksempler, der viser opsætningen og administrationen?

Der er ingen eksempler, men du kan udføre trinnene tidligere i dette emne for at overflytte dine konfigurationer til det globale RCS-lager.
