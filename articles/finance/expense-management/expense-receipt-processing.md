---
title: Behandling af udgiftskvittering
description: Dette emne indeholder oplysninger om behandling af kvitteringer med brug af optisk tegngenkendelse (OCR). Denne funktion er beregnet til at forbedre brugeroplevelsen, når der oprettes udgiftsrapporter i Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 49cdfeac8cda9f1ddd3aca61f902f00f30f3485b
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154034"
---
# <a name="expense-receipt-processing"></a>Behandling af udgiftskvittering

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Udgiftsregistrering er blevet forbedret via indførelsen af OCR-behandling (optisk tegngenkendelse) af kvitteringer. Denne funktion er beregnet til at forbedre brugeroplevelsen, når der oprettes udgiftsrapporter.

## <a name="key-features"></a>Hovedfunktioner

- Forhandlerens navn, dato og det samlede beløb udtrækkes fra kvitteringerne.
- Funktionen forsøger at afstemme ikke-tilknyttede kvitteringer med ikke-tilknyttede udgiftstransaktioner.
- Brugerne kan oprette manuelt indtastede udgiftstransaktioner fra kvitteringer.

## <a name="usage-examples"></a>Eksempler på anvendelse

- **Tilknyt automatisk kvitteringer, der indeholder kreditkorttransaktioner, når der oprettes en udgiftsrapport.**

    1. Åbn arbejdsområdet **Udgiftsstyring**.
    2. Kontroller under fanen **Kvitteringer**, at der findes ikke-tilknyttede kvitteringer. Du kan også overføre kvitteringer under fanen **Kvitteringer**.
    3. Under fanen **Udgifter** skal du kontrollere, at der findes ikke-tilknyttede udgifter. Udgiftsadministratoren importerer typisk disse udgifter fra udbyderen af kreditkortet.
    4. Vælg **Ny udgiftsrapport**. Bemærk, at du nu også kan medtage udgifter og kvitteringer, når du opretter en udgiftsrapport. Hvis du tilføjer både udgifter og kvitteringer, udløses automatisk afstemning af kvitteringer med udgifter.

- **Opret en udgift, eller afstem en udgift fra en kvittering.**

    1. I en udgiftsrapport skal du under fanen **Kvitteringer** tilknytte en kvittering ved at vælge **Tilføj kvitteringer**.
    2. Bemærk indstillingerne **Opret** og **Afstem** under det overførte billede af kvitteringen.

        - Vælg **Opret** for at oprette en manuelt indtaste udgiftstransaktion, og indsæt de værdier, der er udtrukket fra kvitteringen.
        - Hvis du vælger **Afstem**, forsøger systemet at afstemme en eksisterende udgift med kvitteringen.

## <a name="installation"></a>Installation

Denne funktion fungerer sammen med funktionen **Udgiftsrapporter nyfortolkede** for at gøre udgiftsangivelsesoplevelsen mere enkel.

Hvis du vil bruge disse avancerede udgiftsfunktioner, skal du installere tilføjelsesprogrammet til Udgiftsstyring-tjeneste til Microsoft Dynamics 365 Finance, og aktivere funktionerne i din forekomst. Du kan få adgang til tilføjelsesprogrammet fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS).

1. Log på LCS, og åbn det ønskede miljø.
2. Gå til **Alle detaljer**.
3. Vælg **Vedligehold**, eller rul ned til oversigtspanelet **Tilføjelsesprogrammer for miljø**.
4. Vælg **Installer et nyt tilføjelsesprogram**.
5. Vælg **Udgiftsstyring-tjeneste**.
6. Følg installationsvejledningen, og accepter vilkårene og betingelserne.
7. Vælg **Installer**.

I arbejdsområdet **Funktionsstyring** skal du aktivere følgende funktioner:

- Udgiftsrapporter nyfortolkede
- Match og opret udgift automatisk fra tilgang

Når du aktiverer disse funktioner, udføres følgende handlinger:

- Det eksisterende arbejdsområde **Udgiftsstyring** erstattes med det nye arbejdsområde.
- Der tilføjes et nyt menupunkt for synlighed af udgiftsfelter.
- Du kan stadig åbne den tidligere side **Udgiftsrapporter** ved at gå til **Udgiftsstyring > Mine udgifter > Udgiftsrapporter**.
- Arbejdsgange og eventuelle godkendelser fører stadig til den eksisterende side med udgiftsrapporter.
- Kvitteringer vil blive behandlet via Microsoft Azure Cognitive Services, og metadata vil blive udtrukket og tilføjet.
- Der tilføjes en indstilling, du kan bruge til at oprette en udgiftsrapport, der indeholder afstemte ikke-tilknyttede kvitteringer.
- En indstilling, der føjes til udgiftsrapporter, giver dig mulighed for at oprette en udgiftslinje ud fra en kvittering eller forsøge at afstemme en eksisterende kvittering med en eksisterende udgiftslinje.

Yderligere oplysninger om den nyfortolkede funktion til udgiftsrapporter finder du i [Udgiftsrapporter i nyfortolkning](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

**Bruger Microsoft mine data til sine modeller?**

Nej, Microsoft har udviklet en generel model til maskinel indlæring til tjenesten til behandling af kvitteringer. Denne model er ikke baseret på de kvitteringer, du overfører.

**Hvor er denne funktion tilgængelig, og hvor behandles den?**

I øjeblikket understøttes USA.

**Hvor sendes mine kvitteringer hen?**

Finance kontakter Cognitive Services for at udtrække feltdata. Cognitive Services bevarer en kopi af din kvittering i op til 24 timer, mens behandlingen pågår. Når behandlingen er fuldført, fjerner Cognitive Services kvitteringen. Kvitteringer gemmes stadig i Finance.

Du kan finde flere oplysninger [Få forståelse af kvitteringer med ny funktion i Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
