---
title: Prissætningsfunktioner i POS
description: Denne artikel beskriver forskellige pris- og rabatfunktioner i Microsoft Dynamics 365 Commerce POS-programmet.
author: boycez
ms.date: 08/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-14
ms.openlocfilehash: 92bbc3b81b889f106dc113528afbdc37d1106ff3
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2022
ms.locfileid: "9294114"
---
# <a name="pricing-functions-in-pos"></a>Prissætningsfunktioner i POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikel beskriver forskellige pris- og rabatfunktioner i Microsoft Dynamics 365 Commerce POS-programmet.

POS-programmet i Dynamics 365 Commerce indeholder udvidede egenskaber, der gør det muligt for frontlinjemedarbejdere at udføre handlinger for butikshandel. I følgende tabel vises de pris- og rabatfunktioner, der aktuelt er tilgængelige i programmet.

| Funktion                       | POS-handlinger |
|--------------------------------|----------------|
| Vise priser                    | [Pristjek](#price-check) |
| Vise rabatter                 | [Få vist alle rabatter](#view-all-discounts)<br>[Vis tilgængelige rabatter](#view-available-discounts) |
| Tilsidesætte priser                | [Prisændring](#price-override) |
| Anvende eller fjerne rabatter      | [Linjerabatbeløb](#line-discount-amount)<br>[Linjerabatprocent](#line-discount-percent)<br>[Slutrabatbeløb](#total-discount-amount)<br>[Slutrabatprocent](#total-discount-percent)<br>[Fjern systemrabatter fra transaktion](#remove-system-discounts-from-transaction)<br>[Anvend systemrabatter igen](#reapply-system-discounts) |
| Anvende eller fjerne kuponer        | [Tilføj kuponkode](#add-coupon-code)<br>[Fjern kuponkode](#remove-coupon-code) |
| Beregne priser og rabatter | [Genberegn](#recalculate) |

Oplysninger om, hvordan de foregående handlinger kan konfigureres i POS-programmet, og om de understøtter offlinetilstand, finder du i [POS-handlinger, online og offline](pos-operations.md).

## <a name="price-check"></a>Pristjek

Handlingen **Pristjek** sætter POS-brugere i stand til at slå forudkonfigurerede priser op for et bestemt produkt.

## <a name="view-all-discounts"></a>Få vist alle rabatter

Handlingen **Få vist alle rabatter** giver POS-brugere mulighed for at slå alle gældende kampagner op, der aktuelt kører i butikskanalen. Denne handling angiver specifikt alle rabatter, der opfylder en af følgende betingelser:

- Prisgruppen for rabatten svarer til butikkens prisgruppe.
- Prisgruppen for rabatten er knyttet til et tilhørsforholds- eller fordelskundeprogram.
- Prisgruppen for rabatten er tilknyttet et katalog, der er tilknyttet butikken.

Siden **Få vist alle rabatter** viser kun rabatter, der ikke konkurrerer med nogen af de allerede anvendte rabatter. Denne funktionsmåde sikrer, at en salgsmedarbejder informerer kunden om en rabat, og kunden udfører den påkrævede handling (f.eks. hvis kunden køber én mere vare for at opnå en rabat på 10 %), anvendes rabatten på transaktionen. De kuponbaserede rabatter vises kun, når parameteren **Anvend uden en kuponkode** er slået til.

I handlingen **Få vist alle rabatter** kan POS-brugere søge efter rabatter ud fra navn og beskrivelse, og de kan filtrere rabatter baseret på, om de skal bruge en kupon.

## <a name="view-available-discounts"></a>Vis tilgængelige rabatter

Handlingen **Vis tilgængelige rabatter** giver POS-brugere mulighed for at se alle rabatter, der gælder for en valgt linje i en transaktion eller for hele transaktionen. De rabatter, der gælder for en valgt linje, omfatter rabatter, der allerede er anvendt, og rabatter, der endnu ikke er blevet anvendt, men kan anvendes (f.eks. mix og match-rabatter, der kræver yderligere varer). Hvis en gældende rabat er knyttet til en kupon, hvor parameteren **Anvend uden kuponkode** er aktiveret, kan POS-brugeren også bruge funktionen **Anvend kupon** i denne handling til at indløse kuponen direkte uden at skulle indtaste eller scanne kuponkoder eller kuponstregkoder.

## <a name="price-override"></a>Prisændring

Handlingen **Prisændring** sætter POS-brugere i stand til at tilsidesætte salgsprisen på et produkt i en transaktion. Denne handling fungerer kun for produkter, der er konfigureret til at tillade prisændringer.

## <a name="line-discount-amount"></a>Linjerabatbeløb

Operationen **Linjerabatbeløb** sætter POS-brugere i stand til at angive et rabatbeløb for en linjevare i en transaktion. Denne handling gælder kun for varer, der kan gives rabat på, og den overholder værdien af **Maks. linjerabatbeløb**, der er angivet i POS-tilladelsesgruppen for brugeren.

## <a name="line-discount-percent"></a>Linjerabatprocent

Operationen **Linjerabatprocent** sætter POS-brugere i stand til at angive en rabatprocent for en linjevare i en transaktion. Denne handling gælder kun for varer, der kan gives rabat på, og den overholder værdien af **Maks. linjerabatprocent**, der er angivet i POS-tilladelsesgruppen for brugeren.

## <a name="total-discount-amount"></a>Slutrabatbeløb

Operationen **Slutrabatbeløb** sætter POS-brugere i stand til at angive et rabatbeløb for en transaktion. Denne handling gælder kun for varer, der kan gives rabat på, og den overholder værdien af **Maks. slutrabatbeløb**, der er angivet i POS-tilladelsesgruppen for brugeren. Hvis det rabatbeløb, der angives, overstiger det maksimale slutrabatbeløb, spærres handlingen, og der udløses ingen ændring af tilladelser. I øjeblikket kan et slutrabatbeløb ikke anvendes på en indkøbsvogn, der indeholder en miks af salgsvarer og returvarer.

## <a name="total-discount-percent"></a>Slutrabatprocent

Operationen **Slutrabatprocent** sætter POS-brugere i stand til at angive en rabatprocent for en transaktion. Denne handling gælder kun for varer, der kan gives rabat på, og den overholder værdien af **Maks. rabatprocent i alt**, der er angivet i POS-tilladelsesgruppen for brugeren. Hvis den rabatprocent, der angives, overstiger den maksimale rabatprocent i alt, spærres handlingen, og der udløses ingen ændring af tilladelser. I øjeblikket kan en rabatprocent i alt ikke anvendes på en indkøbsvogn, der indeholder en miks af salgsvarer og returvarer.

## <a name="remove-system-discounts-from-transaction"></a>Fjern systemrabatter fra transaktion

Med handlingen **Fjern systemrabatter fra transaktion** kan POS-brugere rydde alle anvendte systemrabatter (herunder kuponbaserede rabatter) fra en transaktion. Når denne handling er udført, starter prissætningsprogrammet for at udelukke systemrabatter fra området for rabatberegning. Handlingen **Fjern systemrabatter fra transaktion** fjerner ikke manuelle rabatter.

## <a name="reapply-system-discounts"></a>Anvend systemrabatter igen

Handlingen **Anvend systemrabatter igen** giver POS-brugere mulighed for at genanvende systemberegnende rabatter på en transaktion, hvis rabatterne er fjernet ved hjælp af handlingen **Fjern systemrabatter fra transaktioner**. Når denne handling er udført, starter prissætningsprogrammet for at medtage alle systemrabatter fra området for rabatberegning.

## <a name="add-coupon-code"></a>Tilføj kuponkode

Handlingen **Tilføj kuponkode** giver POS-brugere mulighed for at føje en kupon til en transaktion ved at indtaste en kuponkode. POS-brugere kan også scanne en kuponstregkode eller indtaste den på det numeriske tastatur på **Transaktioner**-skærmbilledet.

## <a name="remove-coupon-code"></a>Fjern kuponkode

Handlingen **Fjern kuponkode** giver POS-brugere mulighed for at vælge og fjerne en eller flere kuponer, der aktuelt anvendes til en transaktion.

## <a name="recalculate"></a>Genberegn

Handlingen **Genberegn** giver POS-brugere mulighed for at udløse beregning af prissætning efter behov. Denne handling er påkrævet, når prislås og/eller forsinket prisberegning er aktiveret, og POS-brugeren ønsker at genberegne priser og rabatter efter ændringer i indkøbsvognen eller ordren. Handlingen **Genberegn** genberegner altid hele ordren. Den kan ikke bruges til at genberegne udvalgte salgslinjer. Hvis du vil anvende manuelle rabatter på en låst salgslinje i POS, skal POS-brugere først bruge handlingen **Genberegn** for at låse alle salgslinjer op.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
