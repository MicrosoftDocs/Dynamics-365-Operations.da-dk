---
title: Prisjusteringer og rabatter
description: Denne artikel indeholder oplysninger om prisjusteringer og rabatter i Dynamics 365 Commerce.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 96a695df250cda514b7bd8b9716c0f03fb2bfd28d3af4daedaf1335c3099fbb6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748492"
---
# <a name="price-adjustments-and-discounts"></a>Prisjusteringer og rabatter

[!include [banner](includes/banner.md)]

Denne artikel indeholder oplysninger om prisjusteringer og rabatter i Dynamics 365 Commerce.

I Commerce kan du foretage prisjusteringer af produkter, og du kan også konfigurere rabatter, der anvendes på et linjeelement eller en transaktion på POS, i et callcenters salgsordre eller i en onlineordre. Både prisjusteringer og rabatter kan være knyttet til prisgrupper. Du kan angive en enkelt startdato og slutdato eller en tilbagevendende periode, en rabatkode og et par ekstra attributter for både prisjusteringer og rabatter. 

Prisjusteringer og rabatter kan anvendes på produkter, varianter eller kategorier. Hvis mere end én rabat gælder for et produkt, kan en kunde måske modtage enten en af rabatterne eller en kombineret rabat, afhængigt af konfigurationen af rabatten. Commerce anvender automatisk rabatten eller den kombination af rabatter, som giver den bedste pris til kunden. Når du opretter en prisjustering eller rabat, skal du kontrollere, at prisgrupper er knyttet til de korrekte kanaler, kataloger, tilhørsforhold eller loyalitetsprogrammer, som du ønsker, at rabatten skal gælde for. Derudover er det sådan, at hvis du vil oprette rabat-id'et automatisk, kan du oprette nummerserier på siden **Commerce-parametre**, inden du definerer en ny prisjustering eller rabat.

> [!NOTE]
> Du kan slette en prisjustering eller en rabat. Statistiske oplysninger går imidlertid tabt.

## <a name="types-of-discounts"></a>Rabattyper

Der findes mange typer rabatter:

- **Enkel rabat** – en enkelt procent eller beløb.
- **Mængderabat** – En rabat, der anvendes, når to eller flere produkter købes.
- **Mix og match-rabat** – En rabat, der anvendes, når der købes en specifik kombination af produkter.
- **Tærskelrabat** – En rabat, der anvendes, når totalen for transaktionen er mere end et bestemt beløb.
- **Betalingsmiddelbaserede rabatter** – En rabat, der anvendes, når totalen for transaktionen overstiger et angivet beløb, og når en bestemt betalingstype (f.eks. kontant, kredit- eller debetkort) bruges til betaling.
- **Forsendelsesrabat** – En rabat, der anvendes, når totalen for transaktionen overstiger et angivet beløb, og når en bestemt leveringsmåde (f.eks. forsendelser over to dage eller samme dag) bruges i ordren.

Både prisjusteringer og rabatter kan være knyttet til prisgrupper. Prisgrupper kan derefter tilknyttes kanaler, kataloger, tilhørsforhold og loyalitetsprogrammer.

> [!NOTE]
> Mix og match-rabatten og tærskelrabatten har egenskaber med henholdsvis navnet "Optæl produkter uden rabat" og "Optæl produkter uden rabat i forhold til tærskel". Hvis disse egenskaber er aktiveret, kan en vare, der ikke er berettiget til rabat, stadig være med til at kvalificere en transaktion til rabatten, men den ikke-berettigede vare kan ikke få rabatten. 
> 
> Hvis du f.eks. opretter en mix og match-rabat med to linjer, A og B, hvor en kunde skal have 10 % rabat på begge varer, men vare A har konfigurationen "Undgå alle rabatter" markeret, vil det typisk forhindre vare A i at blive medtaget i rabatten. Men hvis egenskaben "Optæl produkter uden rabat" er aktiveret, kan vare A bruges til at kvalificere til mix og match-rabatten, men rabatten på 10 % anvendes kun på vare B. Lignende logik gælder for tærskelrabatten. 
>
> Egenskaben "Optæl produkter uden rabat i forhold til tærskel" har dog en ekstra egenskab, når den sammenlignes med egenskaben "Optæl produkter uden rabat" for mix og match-rabatter. Hvis tærskelrabatten er aktiveret, og hvis der er en vare med en eksisterende rabat, som kan forhindre varen i at få andre rabatter, vil den pris, der er betalt for denne vare, være kvalificeret til at nå tærsklen, men denne vare får ikke den ekstra rabat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
