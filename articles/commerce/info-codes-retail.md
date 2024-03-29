---
title: Infokoder og infokodegrupper
description: Denne artikel indeholder en oversigt over oplysninger om infokoder, infokodegrupper, og hvordan de bruges.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.industry: Retail
ms.search.form: RetailInfocodeTable
ms.openlocfilehash: a6fc84db368c602f74778eb0a44ac52798dc5161
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273497"
---
# <a name="info-codes-and-info-code-groups"></a>Infokoder og infokodegrupper

[!include [banner](includes/banner.md)]

Denne artikel indeholder en oversigt over oplysninger om infokoder, infokodegrupper, og hvordan de bruges.

Infokoder giver mulighed for at registrere data ved et kasseapparat (POS). Du kan bruge infokoder til at bede kassereren om at angive oplysninger under forskellige handlinger på salgsstedet, f-eks. varesalg, varereturnering eller valg af debitorer. Kassereren kan vælge input fra en liste eller angive den som en kode, et tal, en dato eller tekst. Du kan knytte infokoder til foruddefinerede butikshandlinger, detailvarer, betalingsmetoder, kunder eller specifikke POS-aktiviteter. Du kan bruge infokoder til at gøre følgende:

- Registrere flere oplysninger på transaktionstidspunktet, som f.eks. et flynummer eller årsagen til en returnering.
- Bed kassereren ved kasseapparatet om at vælge priser på bestemte produkter på en liste.
- Knytte en underkode til en infokode, hvor kassereren bliver bedt om at angive input, når der udføres en bestemt aktivitet. Når en kunde returnerer et produkt, kan du spørge kassereren om, hvorfor produktet returneres. Du kan derefter bruge underkoder til at få vist en liste over årsager, som kassereren kan vælge imellem.
- Sælge et produkt som almindeligt salg, et salg med rabat eller et gratis produkt.
- Bede kassereren om at angive en værdi eller vælge fra en liste med underkoder, når kasseapparatets pengeskuffe åbnes, uden at der sælges noget.

## <a name="info-codes-group"></a>Infokodegruppe

I Commerce kan du oprette grupper af infokoder. Infokodegrupper giver fleksibilitet ved at give dig mulighed for at definere færre infokoder og derefter bruge dem på en mere alsidig måde. Du kan bruge infokodegrupper på følgende måder:

- Definere færre infokoder og nemt bruge dem igen. Infokoder, der er inkluderet i infokodegrupper, har ingen foruddefinerede afhængigheder i forhold til andre infokoder. Du kan medtage den samme infokode i flere infokodegrupper og derefter bruge prioritering for at vise de samme infokoder i en rækkefølge, der giver mening i en given situation.
- Sammenkæd infokoder med andre infokoder eller infokodegrupper for at indsamle oplysninger om et produkt eller en postering uden at skulle definere en separat infokode eller sammenkædet infokode for hvert scenarie.

## <a name="info-code-examples"></a>Eksempler på infokoder

**Eksempel 1: Genbrug infokoder**

Du kan sammenkæde infokæder på en måde, så hvis én infokode udløses, udløses en anden infokode omgående derefter. Når du f.eks. sælger bestemte produkter, foretrækker du, at ekspedienten tilbyder kunden at købe batterier eller en produktgaranti. For andre produkter vil du gerne have, at ekspedienten spørger kunden, om han/hun vil købe batterier, og indhenter kundens postnummer. Hvis du opretter sammenkædede infokoder for disse scenarier, skal du konfigurere alle variationer af infokoden, så kassereren bliver bedt om at spørge efter de rigtige oplysninger. Hvis du bruger infokodegrupper, kan almindelige infokoder, som f.eks. at spørge efter batterier, konfigureres én gang og derefter genbruges i flere infokodegrupper. Du kan også bruge prioritering i infokodegrupperne for at identificere rækkefølgen, hvori anmodningerne vises.

**Eksempel 2: Sammenkæd infokoder med infokodegrupper**

Når du sælger bestemte produkter, f.eks. mobilenheder, vil det altid være i din interesse at indsamle bestemte oplysninger såsom telefonnummer, mobiludstyrs-id (MEID) og serienummer. Det vil dog også være i din interesse at indsamle forskellige oplysninger til en tablet i forhold til en mobiltelefon. Du kan oprette en infokodegruppe, der omfatter anmodninger om telefonnummer, MEID og serienummeret, og derefter sammenkæde infokodegruppen med en individuel infokode. Når den produktspecifikke infokode udløses, kan infokodegruppen udløses derefter, så du kan indsamle generelle data uden at skulle definere flere sæt af sammenkædede infokoder for hver enhed.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
