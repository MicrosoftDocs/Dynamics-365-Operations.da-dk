---
title: Kuponer
description: Denne artikel indeholder en oversigt over kuponrelaterede funktioner i Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.openlocfilehash: 20427a04a552ddec013daa6576ec64ab7046e95f
ms.sourcegitcommit: 87e75aa6af2c3280316d7d73eafa14a52353a5e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/21/2022
ms.locfileid: "9709753"
---
# <a name="coupons"></a>Kuponer

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over kuponrelaterede funktioner i Microsoft Dynamics 365 Commerce.

Kuponer er koder og stregkoder, der bruges til at føje rabatter til transaktioner. Detailhandlende distribuerer kuponer til mulige eller eksisterende kunder for at forbedre deres mærkegenkendelse, skabe konvertering, bevare deres kundebase, generere salg og øge indtjeningen i sidste ende. Kuponer er blevet et af de mest populære marketingværktøjer og er en ny norm i e-handelssalg.

I Dynamics 365 Commerce er kuponer knyttet til rabatter og betragtes som en ekstra validering ud over rabatter. Hver kupon er relateret til én rabat, og den sammenkædede rabat definerer det sæt produkter, som kuponen gælder for.

Prisgrupper, der er tilknyttet en rabat, definerer de berettigede betingelser, som en kupon kan bruges til. Disse betingelser omfatter kundegrupper og salgskanaler. Kuponer indeholder også egenskaberne **Brugsbegrænsning** og **Debitor påkrævet**, som kan bruges til at konfigurere valgfrie brugsbegrænsninger.

Hver kupon kan have flere kuponkoder og kuponstregkoder, og hver kode kan have sine egne gyldighedsdatoer og status. Hvis status for en kode er angivet til **Inaktiv**, kan koden ikke bruges i nogen kanal.

## <a name="set-up-a-coupon"></a>Konfigurere en kupon

Når du vil konfigurere en kupon, skal du først angive kuponens stregkode og to kuponnummerserier.

Gør følgende for at konfigurere en kupon i Commerce headquarters.

1. Gå til **Retail og Commerce \> Lagerstyring \> Stregkoder og labels \> Masketegn**.
1. Vælg **Tilføj** for at oprette et masketegn af typen **Kuponkode**. I feltet **Tegn** kan du vælge et vilkårligt ubrugt tegn.
1. Gå til **Retail og Commerce \> Lagerstyring \> Stregkoder og labels \> Opsætning af stregkodemaske**.
1. Vælg **Ny** for at oprette en stregkodemaske af typen **Kupon**.
1. Gå til **Retail og Commerce \> Lagerstyring \> Stregkoder og labels \> Stregkodeopsætning**.
1. Vælg **Ny** for at oprette en stregkode, der bruger den stregkodemaske, du har oprettet.
1. Gå til **Organisationsadministration \> Nummerserier**.
1. Opret to nummerserier:

    1. Én sekvens for referencen **Kuponnummer**. Denne sekvens definerer den entydige identifikator for kuponen.
    1. Én sekvens for referencen **Kuponkode-id**. Den definerer den entydige identifikator for hver kuponkode til en kupon.

    For begge nummerserier skal du indstille feltet **Interval** til **Firma**. I de fleste tilfælde burde begge serienumre genereres automatisk.

1. Gå til **Handelsparametre \> Priser og rabatter \> Kuponer**.
1. Angiv feltet **Kuponens stregkodemaske** til den stregkode, du oprettede tidligere.
1. Gå til **Handelsparametre \> Nummerserier**.
1. Vælg de nummerserier, du oprettede tidligere for referencer til **Kuponnummer** og **Kuponkode-id**.

Hvis du vil konfigurere en kupon, skal du oprette rabatten og kuponen separat og derefter tilknytte dem ved at vælge rabatten i **Rabat**-feltet for kuponkonfigurationen. Når en kupon er knyttet til en rabat, bliver felterne **Status**, **Ikrafttrædelsesdato** og **Udløbsdato** for den tilknyttede rabat skrivebeskyttede, da værdierne bestemmes af kuponens status og gyldighedsperiode. Når status for en kupon angives til **Aktiv**, opdateres status for den tilknyttede rabat automatisk til **Aktiveret**. Og når status for en kupon angives til **Inaktiv**, opdateres status for den tilknyttede rabat automatisk til **Deaktiveret**.

## <a name="use-a-coupon"></a>Bruge en kupon

Hvis du vil føje en kupon til en salgstransaktion i Commerce POS, kan du bruge en kuponkode eller kuponstregkode. Hvis du vil bruge en kuponkode, skal du vælge operationen **Tilføj kuponkode** og derefter angive koden. Du kan også enten scanne stregkoden eller indtaste stregkoden med en scanningsenhed eller det numeriske tastatur på **Transaktion**-skærmbilledet, hvis du vil bruge en kuponstregkode.

Det kan ske, at forhandlere ønsker, at kassereren skal kunne give et fast rabatbeløb til kunderne efter aftale eller på grund af produktfejl, men de ønsker ikke at udskrive kuponkoder og distribuere dem til kassererne. I dette tilfælde kan du angive indstillingen **Anvend uden kuponkode** for kuponen til **Ja**. POS-kasserere kan derefter bruge funktionen **Anvend kupon** i handlingen **Vis tilgængelige rabatter** til at føje en kupon til en transaktion uden at indtaste koden manuelt. Hvis der findes flere kuponkoder for en kupon, vælger systemet automatisk den første aktive kode og anvender den på transaktionen.

Hvis du vil føje en kupon til en callcenter-salgsordre, skal en callcenter-bruger vælge **Kuponer** under fanen **Administrer** i handlingsruden på salgsordresiden.

Hvis en kunde vil føje en kupon til en e-handelsordre, kan kunden angive kuponkoden i feltet i **Kampagnekode** i indkøbsvognen.

Når en kupon føjes til en salgsordre, udløser prissætningsprogrammet straks genberegning af hele ordren, uanset om forsinkede beregninger er aktiveret.

> [!NOTE]
> I Commerce version 10.0.30 og tidligere skal de, efter at call center-brugerne har føjet en kupon til en salgsordre, vælge **Genberegn** i gruppen **Beregn** under fanen **Sælg** i handlingsruden for at anvende den rabat, der er knyttet til denne kupon.

## <a name="coupon-usage-limit"></a>Brugsbegrænsning for kupon

Kuponer kan konfigureres til begrænset brug. Anvendelsesgrænsen kan defineres pr. kunde eller kanal eller globalt. Brugsbegrænsningen gennemtvinges pr. kuponkode på en kupon. F.eks. kan en engangskupon, der har to kuponkoder, bruges to gange: én gang for hver kuponkode.

Kuponer kan bruges på tværs af salgskanaler. For callcenter kan kuponer med begrænset brug dog kun anvendes, når indstillingen **Aktivér ordrefuldførelse** er aktiveret for callcenter-kanalen. Hvis indstillingen **Aktivér ordrefuldførelse** er deaktiveret, kan kun kuponer, der ikke har begrænset brug, anvendes.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
