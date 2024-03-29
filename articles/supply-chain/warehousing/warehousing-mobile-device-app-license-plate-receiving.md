---
title: Modtage id via Warehouse Management-mobilappen
description: Denne artikel beskriver, hvordan du konfigurerer mobilappen Lokationsstyring til at understøtte brug af en nummerplademodtagelsesproces for at modtage fysisk lager.
author: perlynne
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters, WHSRFMenuItem, WHSLicensePlate, WHSPackingStructure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 657c29ec6ddfb2be918424e06eaf219f51a30a02
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069056"
---
# <a name="license-plate-receiving-via-the-warehouse-management-mobile-app"></a>Modtage id via Warehouse Management-mobilappen

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer mobilappen Lokationsstyring, så den understøtter brug af en nummerplademodtagelsesproces for at modtage fysisk lager.

Du kan bruge denne funktion til hurtigt at registrere modtagelsen af det indgående lager, der er knyttet til en ASN (Advance Ship Notice). Systemet opretter automatisk en ASN, når der bruges lokationsstyringsprocesser (WMS) til at levere en flytteordre. I forbindelse med indkøbsordreprocessen kan en ASN registreres manuelt, eller den kan importeres automatisk ved hjælp af en indgående ASN-dataenhedsproces.

ASN-dataene er knyttet til laster og forsendelser via *pakkestrukturerne*, hvor paller (overordnede nummerplader) kan indeholde kasser (indlejrede nummerplader).

> [!NOTE]
> Systemet registrerer den fysiske disponible lagerbeholdning på den overordnede nummerplade for at reducere antallet af lagertransaktioner, når der bruges pakkestrukturer med indlejrede nummerplader. Den mobile enhed skal angive et menupunkt, der er baseret på processerne til oprettelse af *Pak til indlejrede nummerplader*, for at udløse bevægelsen af den fysiske disponible lagerbeholdning fra den overordnede nummerplade til de indlejrede nummerplader baseret på pakkestrukturdataene.

## <a name="warehousing-mobile-device-app-processing"></a>Håndtering af mobilenheds-appen Lagersted

Når en arbejder scanner et indgående nummerplade-id, starter systemet en modtagelsesproces for nummerpladen. På baggrund af disse oplysninger bliver indholdet af nummerpladen (data, der kommer fra ASN) fysisk registreret på modtagelsesstedet. De flow, der følger efter, afhænger af forretningsprocessens behov.

## <a name="work-policies"></a>Arbejdspolitikker

Som ved (f.eks.) processen i forbindelse med mobilenhedens menupunkit *Færdigmelding*, hvor modtagelsesprocessen for nummerpladen understøtter flere arbejdsgange baseret på den definerede opsætning.

### <a name="work-policies-with-work-creation"></a>Arbejdspolitikker med arbejdsoprettelse

Når du registrerer indgående varer ved hjælp af en arbejdspolitik, der opretter arbejde, genererer og gemmer systemet læg-på-lager-arbejdsposter for hver registrering. Hvis du bruger arbejdsprocessen *Modtagelse af nummerplade og placering på lager*, håndteres registrering og læg-på-lager-aktiviteter som en enkelt operation ved hjælp af et enkelt menupunkt i en mobilenhed. Hvis du bruger processen *Nummerplade til modtagelse*, håndteres modtagelses- og læg-på-lager-processerne som to forskellige lagerstedsoperationer, der hver har deres eget menupunkt i mobilenheden.

### <a name="work-policies-without-work-creation"></a>Arbejdspolitikker uden arbejdsoprettelse

Du kan bruge modtagelsesprocessen for nummerplader uden at oprette arbejde. Hvis du definerer arbejdspolitikker, der har en arbejdsordre af typen *Tilgang for overførsel* og/eller *Indkøbsordrer*, og du bruger processen til *Modtagelse af nummerplade (og placering på lager)*, vil de følgende to mobilapp-processer til lagersteder ikke oprette arbejde. De vil i stedet kun registrere det indgående fysiske lager på nummerpladen ved det indgående modtagelsesområde.

- *Nummerplade til modtagelse*
- *Modtagelse af nummerplade og placering på lager*

> [!NOTE]
> - Du skal definere mindst én lokation for en arbejdspolitik i sektionen **Lagerlokationer**. Du kan ikke angive den samme placering for flere arbejdspolitikker.
> - Indstillingen **Udskriv label** til mobilenhedens menupunkter for lagersted udskriver ikke en nummerpladelabel uden at oprette arbejde.

Hvis du vil gøre denne funktionalitet tilgængelig på systemet, skal du aktivere funktionen *Nummerplader, der modtager forbedringer* i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a>Modtage lagerbeholdninger på en lokation, der ikke sporer nummerplader

Det er muligt at bruge en lagerlokation, der er tildelt en lokationsprofil, selv når **Brug nummerpladesporing** ikke er slået til. Når du f.eks. modtager lagerbeholdning, kan du derfor registrere den disponible lagerbeholdning direkte på en lokation uden at oprette en arbejdsgang.

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a>Tilføje menupunkter i mobilenheder for hver modtagelseslokalitet på et lagersted

Med funktionen *Nummerplader, der modtager forbedringer* kan du på enhver lokation på et lagersted modtage ved at føje lokationsspecifikke menupunkter for nummerplademodtagelse (og læg på lager) til Warehousing Mobile App. Tidligere understøttede systemet kun modtagelse på den standardplacering, der er defineret for hvert lagersted. Men når denne funktion er slået til, vil menupunkterne i mobilenheden for nummerplademodtagelse (og lægge på lager) nu levere indstillingen **Brug standarddata**, så du kan vælge en brugerdefineret "til"-placering til hvert menupunkt. (Denne indstilling var allerede tilgængelig for andre typer menupunkter).

Hvis du vil gøre denne funktionalitet tilgængelig på systemet, skal du aktivere funktionen *Nummerplader, der modtager forbedringer* i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="show-or-skip-the-receiving-summary-page"></a>Få vist eller spring over siden til opsummering af modtagelse

Du kan bruge funktionen *Kontrolelementet til at få vist en side med status for modtagelse på mobilenheder* for at udnytte et mere detaljeret flow i mobilappen Lokationsstyring som del af modtagelsesprocessen af nummerplader.

Når denne funktion er slået til, indeholder den mobile enhed menupunkter til modtagelse af nummerplader, og læg-på-lager, der viser indstillingen **Oversigtsside til visning af modtagelse**. Denne indstilling har følgende indstillinger:

- **Få vist en detaljeret oversigt** – når du modtager nummerplader, vil arbejderne få vist en ekstra side, der viser fuldstændige ASN-oplysninger.
- **Spring oversigt over** – Arbejdere kan ikke få vist de fuldstændige ASN-oplysninger. Lagermedarbejderne kan heller ikke angive en dispositionskode eller tilføje undtagelser under modtagelsesprocessen.

Hvis du vil bruge denne funktionalitet, skal funktionen *Kontrollér, om der skal vises en oversigtsside med tilgange på mobilenheder* være slået til i systemet. Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret. Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.25, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Kontrollér, om der skal vises en oversigtsside med tilgange på mobilenheder* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Undgå, at afsendte, ordreforsendte nummerplader bliver brugt i andre lagersteder end destinationslagerstedet

Der kan ikke bruges en proces til modtagelse af nummerplader, hvis en ASN indeholder et nummerplade-id, der allerede findes, og som har fysiske beholdningsdata på en anden lagerlokation end den lagerlokation, hvor der sker registrering af nummerpladen.

I forbindelse med overflytningsordrescenarier, hvor forsendelseslagerstedet ikke sporer nummerplader (og derfor ikke sporer fysisk disponibel lagerbeholdning pr. nummerplade), kan du bruge metoden *Undgå afsendte, ordreforsendte nummerplader fra at blive brugt på andre lagersteder end destinationslagerstedet* for at forhindre fysisk disponible opdateringer af nummerplader, der er undervejs. Hvis du vil gøre denne funktionalitet tilgængelig på dit system, skal du aktivere funktionen *Undgå, at id'er for afsendte flytteordrer bliver brugt på andre lagersteder end destinationslagerstedet*. Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.25, kan administratorer slå denne funktion til eller fra ved at søge efter den i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Hvis du vil administrere funktionaliteten, når denne funktion er tilgængelig, skal du følge disse trin.

1. Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.
1. Under fanen **Generelt** i oversigtspanelet **Nummerplader** skal du angive feltet **Politik for transitlagersteds nummerplade** til en af følgende værdier:

    - **Tillad genbrug af nummerplade, der ikke er sporet** – Systemet fungerer på samme måde, som det fungerer, når *Undgå afsendelse af ordreafsendte nummerplader fra at blive brugt på andre lagersteder end destinationslagerstedet* ikke er tilgængeligt. Denne værdi er standardindstillingen, når du første gang aktiverer funktionen.
    - **Undgå genbrug af ikke-sporet nummerplade** – Det er kun de disponible opdateringer, der er relateret til en leveret nummerplade, som tillades på destinationslagerstedet, indtil flytteordren er modtaget.

## <a name="more-information"></a>Flere oplysninger

Du kan få flere oplysninger om menupunkter på mobilenheder, i [Konfigurere mobilenheder til lagerstedsarbejde](configure-mobile-devices-warehouse.md).

Du kan finde flere oplysninger om produktionsscenariet *Færdigmelding* i [Oversigt over politikker for lagerstedsarbejde](warehouse-work-policies.md).

Du finder flere oplysninger om indgående laststyring i [Lagerstedshåndtering af indgående laster til indkøbsordrer](inbound-load-handling.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]