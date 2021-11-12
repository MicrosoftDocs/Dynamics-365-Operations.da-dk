---
title: Konfigurere hævede felter til trin i Warehouse Management-mobilappen
description: I dette emne beskrives, hvordan du kan hæve og fremhæve bestemte oplysninger for et hvilket som helst trin i opgaveflow for mobilappen Warehouse Management.
author: MarkusFogelberg
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 05ca38e366331c2132bb46eddf77ae2ef371256b
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678636"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Konfigurere hævede felter til trin i Warehouse Management-mobilappen

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!--KFM: GA with 10.0.23 -->

> [!IMPORTANT]
> De funktioner, der er beskrevet i dette emne, gælder kun for den nye Warehouse Management-mobilapp. De påvirker ikke den gamle lagerstedsapp, der nu er udgået og frarådes.

I dette emne beskrives, hvordan du kan hæve og fremhæve bestemte oplysninger for et hvilket som helst trin i opgaveflow for mobilappen Warehouse Management. Denne egenskab kan hjælpe medarbejderne med at fokusere på de vigtigste felter, efterhånden som de gennemgår et flow. For hvert trin i hver proces kan administratorer vælge, hvilke felter der skal hæves, og hvilke felter der skal fremhæves.

## <a name="enable-promoted-fields-in-your-system"></a>Aktivere hævede felter i systemet

Før du kan konfigurere hævede felter, skal du gennemføre følgende procedure for at aktivere de påkrævede funktioner og generere de nødvendige feltnavne i mobilappen Warehouse Management.

1. Gå til **Systemadministration \> Arbejdsområder \> Funktionsstyring**.
1. I [arbejdsområdet **Funktionsstyring**](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) skal du aktivere funktionen, der vises, på følgende måde:

    - **Modul:** *Warehouse Management*
    - **Funktionsnavn:** *Trininstruktioner for lagerstedsappen*

    Du kan finde flere oplysninger om trinnet *Vejledninger til trin i lagerstedsapp* i [Tilpasse trintitler og instruktioner til Warehouse Management-mobilappen](mobile-app-titles-instructions.md). Denne funktion er en forudsætning for funktionen *Hævede felter i appen Warehouse*.

1. Aktivér funktionen, der vises, på følgende måde:

    - **Modul:** *Warehouse Management*
    - **Funktionsnavn:** *Hævede felter i appen Warehouse*

    Denne funktion er den funktion, der er beskrevet i dette emne.

1. Opdater feltnavnene i Warehouse Management-mobilappen ved at gå til **Warehouse Management \> Opsætning \> Mobilenhed \> Feltnavne for lagerstedsapp** og vælge **Opret standardkonfiguration**. Du kan finde flere oplysninger i [Konfigurere felter til mobilappen Lokationsstyring](configure-app-field-names-priorities-warehouse.md).
1. Gentag det forrige trin for hver juridisk enhed (firma), hvor du bruger mobilappen Warehouse Management.

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Konfigurere hævede felter fra en menuspecifik tilsidesættelse

Benyt følgende fremgangsmåde til at definere hævede felter.

1. Opret en menuspecifik tilsidesættelse for den relevante menu og det relevante trin som beskrevet i [Tilpasse trintitler og instruktioner til Warehouse Management-mobilappen](mobile-app-titles-instructions.md).
1. Find kombinationen af værdier for **Trin-id** og **Menupunktnavn**, som du vil redigere, og vælg derefter værdien i kolonnen **Trin-id**.
1. På den side, der vises, skal du gå til oversigtspanelet **Vælg hævede felter** og vælge **Vælg felter** på værktøjslinjen.
1. Vælg de felter, du vil hæve, i dialogboksen **Hævede felter**. Du kan også fremhæve op til to af de valgte felter. Fremhævede felter vises med fed skrift i mobilappen Warehouse Management. Når du markerer felter, skal du tænke på, at visse skærmbilleder er så store, at der kun vises et eller to af de felter, der er hævet. Du kan finde et eksempel, der viser, hvordan du bruger disse indstillinger, i scenariet senere i dette emne.

    > [!NOTE]
    > Listen **Tilgængelige felter** er begrænset til de felter, der kan vises for menupunktet. Men andre faktorer (for eksempel varesammensætning) afgør, om et felt rent faktisk vises i mobilappen Warehouse Management. Hvis du har konfigureret hævede felter, er det kun de valgte felter, der vises på hovedsiden i mobilappen Warehouse Management. Men medarbejdere kan stadig se de resterende felter ved at trykke på detaljesiden.

1. Vælg **OK** for at anvende dine indstillinger. De valgte felter vises nu i oversigtspanelet **Vælg hævede felter**.

## <a name="example-scenario"></a>Eksempelscenario

### <a name="enable-sample-data"></a>Aktivér eksempeldata

Hvis du vil bruge de angivne eksempelposter og -værdier, når du arbejder i dette scenarie, skal du bruge et system, hvor standarddemodataene er installeret. Du skal også vælge den juridiske enhed **USMF**, før du starter.

### <a name="configure-sales-picking-with-promoted-steps-on-the-license-plate-step"></a>Konfigurere salgspluk med hævede trin i id-trinnet

I denne procedure konfigurerer du hævede og fremhævede felter for menupunktet **Salgspluk** i id-trinnet.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Trin for mobilenhed**.
1. Find det trin-id, der hedder *LicensePlateId*, og vælg det.
1. Vælg **Tilføj trinkonfiguration** i handlingsruden.
1. Brug feltet **Menupunkt** i dialogboksen med rullelisten til at finde og vælge *Salgspluk*.
1. Vælg **OK**.
1. Detaljesiden for den tilsidesættelse, du netop har oprettet, vises. I oversigtspanelet **Vælg hævede felter** skal du vælge **Vælg felter** på værktøjslinjen.
1. Du kan vælge de felter, du vil hæve og fremhæve, i dialogboksen **Hævede felter**. Søg efter og vælg følgende felter på listen **Tilgængelige felter**, og brug knapperne til at flytte dem til listen **Valgte felter**:

    - Lokation
    - Vare
    - Produktnavn
    - Lagerstatus

1. Brug pil op og pil ned til at ændre rækkefølgen af felterne på listen **Valgte felter**. I mobilappen Warehouse Management vises felterne i den rækkefølge, du angiver her.
1. Vælg feltet **Placering**, og vælg derefter **Fremhæv**.
1. Vælg **OK** for at gemme konfigurationen.

### <a name="view-the-promoted-fields-in-the-warehouse-management-mobile-app"></a>Få vist de hævede felter i Warehouse Management-mobilappen

I denne procedure åbner du mobilappen Warehouse Management og gennemgår trinnene for at få vist de felter, du har hævet og fremhævet i den forrige procedure.

1. I Microsoft Dynamics 365 Supply Chain Management kan du oprette en salgsordre, der skal bruge et pluktrin til at plukke fra en placering, som id'et har sporet. Frigiv derefter salgsordren til lagerstedet. Notér det arbejds-id, der genereres.
1. Åbn mobilappen Warehouse Management, og log på lagersted 24. (I standarddemodataene skal du logge på ved at bruge *24* som bruger-id og *1* som adgangskode.)
1. Vælg menuen **Udgående**, og vælg derefter menupunktet **Salgspluk**.
1. Følg instruktionerne til dataindtastning på skærmen for at angive det arbejds-id, der blev genereret i trin 1.
1. I trinnet, der indeholder teksten **Scan et id**, kan du se de ændringer, du har foretaget på detaljesiden. Felterne vises i den rækkefølge, du har angivet for de hævede felter, og feltet **Placering** vises med fed skrift.
