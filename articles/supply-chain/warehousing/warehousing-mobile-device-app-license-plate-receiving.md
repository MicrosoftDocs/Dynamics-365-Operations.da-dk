---
title: Modtagelse af nummerplade via lagerstedsappen
description: I dette emne beskrives, hvordan du konfigurerer lagerstedsappen til at understøtte brug af en nummerplademodtagelsesproces for at modtage fysisk lager.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346370"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a>Modtagelse af nummerplade via lagerstedsappen

I dette emne beskrives, hvordan du konfigurerer lagerstedsappen, så den understøtter brug af en nummerplademodtagelsesproces for at modtage fysisk lager.

Du kan bruge denne funktion til hurtigt at registrere modtagelsen af det indgående lager, der er knyttet til en ASN (Advance Ship Notice). Systemet opretter automatisk en ASN, når der bruges lokationsstyringsprocesser til at levere en flytteordre. I forbindelse med indkøbsordreprocessen kan en ASN registreres manuelt, eller den kan importeres automatisk ved hjælp af en indgående ASN-dataenhedsproces.

ASN-dataene er knyttet til laster og forsendelser via *pakkestrukturerne*, hvor paller (overordnede nummerplader) kan indeholde kasser (indlejrede nummerplader).

> [!NOTE]
> Systemet registrerer den fysiske disponible lagerbeholdning på den overordnede nummerplade for at reducere antallet af lagertransaktioner, når der bruges pakkestrukturer med indlejrede nummerplader. Den mobile enhed skal angive et menupunkt, der er baseret på processerne til oprettelse af *Pak til indlejrede nummerplader*, for at udløse bevægelsen af den fysiske disponible lagerbeholdning fra den overordnede nummerplade til de indlejrede nummerplader baseret på pakkestrukturdataene.

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>Få vist eller spring over siden til opsummering af modtagelse

Du kan bruge funktionen *Kontrolelementet til at få vist en side med status for modtagelse på mobilenheder* for at udnytte et mere detaljeret flow i lagerstedsappen som del af nummerplademodtagelsesprocessen.

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises denne funktion på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Bestem, om der skal vises en side med en oversigt på mobilenheder*

Når denne funktion er slået til, indeholder den mobile enhed menupunkter til modtagelse af nummerplader, og læg-på-lager, der viser indstillingen **Oversigtsside til visning af modtagelse**. Denne indstilling har følgende indstillinger:

- **Få vist en detaljeret oversigt** – når du modtager nummerplader, vil arbejderne få vist en ekstra side, der viser fuldstændige ASN-oplysninger.
- **Spring oversigt over** – Arbejdere kan ikke få vist de fuldstændige ASN-oplysninger. Lagermedarbejderne kan heller ikke angive en dispositionskode eller tilføje undtagelser under modtagelsesprocessen.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Undgå, at afsendte, ordreforsendte nummerplader bliver brugt i andre lagersteder end destinationslagerstedet

Der kan ikke bruges en proces til modtagelse af nummerplader, hvis en ASN indeholder et nummerplade-id, der allerede findes, og som har fysiske beholdningsdata på en anden lagerlokation end den lagerlokation, hvor der sker registrering af nummerpladen.

I forbindelse med overflytningsordrescenarier, hvor forsendelseslagerstedet ikke sporer nummerplader (og derfor ikke sporer fysisk disponibel lagerbeholdning pr. nummerplade), kan du bruge metoden *Undgå afsendte, ordreforsendte nummerplader fra at blive brugt på andre lagersteder end destinationslagerstedet* for at forhindre fysisk disponible opdateringer af nummerplader, der er undervejs.

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises denne funktion på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Undgå, at afsendte, ordreforsendte nummerplader fra at blive brugt i andre lagersteder end destinationslagerstedet*

Hvis du vil administrere funktionaliteten, når denne funktion er tilgængelig, skal du følge disse trin.

1. Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.
1. Under fanen **Generelt** i oversigtspanelet **Nummerplader** skal du angive feltet **Politik for transitlagersteds nummerplade** til en af følgende værdier:

    - **Tillad genbrug af nummerplade, der ikke er sporet** – Systemet fungerer på samme måde, som det fungerer, når *Undgå afsendelse af ordreafsendte nummerplader fra at blive brugt på andre lagersteder end destinationslagerstedet* ikke er tilgængeligt. Denne værdi er standardindstillingen, når du første gang aktiverer funktionen.
    - **Undgå genbrug af ikke-sporet nummerplade** – Det er kun de disponible opdateringer, der er relateret til en leveret nummerplade, som tillades på destinationslagerstedet, indtil flytteordren er modtaget.

## <a name="more-information"></a>Flere oplysninger

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

Du kan få flere oplysninger om menupunkter på mobilenheder, i [Konfigurere mobilenheder til lagerstedsarbejde](configure-mobile-devices-warehouse.md).
