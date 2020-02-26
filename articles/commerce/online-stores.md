---
title: Konfigurere en onlinebutikskanal
description: Denne artikel indeholder oplysninger om kanaler for onlinebutikker, og hvordan du konfigurerer dem i Dynamics 365 Commerce.
author: kfend
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c427b0eba2120123a47f52029d70896be88b9ec0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022061"
---
# <a name="set-up-an-online-store-channel"></a>Konfigurere en onlinebutikskanal

[!include [banner](includes/banner.md)]

Denne artikel indeholder oplysninger om kanaler for onlinebutikker, og hvordan du konfigurerer dem i Dynamics 365 Commerce.

Commerce understøtter flere detailkanaler. Disse kanaler omfatter onlinebutikker, call centre og detailbutikker (også kaldet fysiske butikker). Onlinebutikker giver en detailhandler synlighed på internettet, så kunderne også kan købe produkter fra detailhandlerens onlinebutik ud over fra detailhandlerens fysiske butik. Hvis kunder køber produkter fra onlinebutikken, kan produkterne leveres til dem, eller kunden kan afhente dem i den lokale butik. 

Du kan oprette en onlinebutik i Commerce-klienten. Denne onlinebutik udgives derefter til en tredjeparts onlinebutik, der er integreret i Commerce. Onlinebutikken fra tredjepart fungerer som butiksrude (brugergrænseflade) for onlinebutikken og giver dig et udvalg af funktioner til kundestyring og funktioner på brugergrænsefladen. Der findes flere integrationer af denne type. 

De egenskaber, du definerer for onlinebutikken i, styrer funktionsmåden i onlinebutikken. Du kan f.eks. definere navigationskategorihierarkiet og tildele det onlinebutikken. Når du udgiver onlinebutikken i en onlinebutik fra tredjepart, vises navigationskategorihierarkiet i onlineversionen af butikken. Handlende bruger derefter navigationskategorihierarkiet til at browse i onlinebutikken og søge efter produkter. 

Hvis du vil oprette en onlinebutik, skal du konfigurere de komponenter, der gør det muligt at behandle transaktioner for butikken. Du skal f.eks. tilføje udvalg, anvende attributter og konfigurere betalingsmetoder og forsendelsesmetoder. Du kan også definere priser, kampagner, rabatter, samhandelsaftaler og leveringsbetingelser, der er specifikke for onlinebutikken. 

Når du har udgivet onlinebutikken i tredjepartens onlinebutik, kan du oprette produktkataloger for onlinebutikken. Produkterne i kataloget bliver vist i onlinebutikken. Når en kunde køber produkter fra onlinebutikken, opdateres det tilgængelige lager og synkroniseres i klienten. Desuden oprettes der salgsordrer for købene, og de sendes til klienten med henblik på ordreopfyldning og behandling.

## <a name="set-up-an-online-store"></a>Konfigurere en onlinebutik

Hvis du vil konfigurere en onlinebutik, skal du fuldføre følgende opgaver.

1. Opret onlinebutikken.
2. Tilføj onlinebutikken i de relevante organisationshierarkier.
3. Tilføj sortimenter, der omfatter de produkter, der er tilgængelige i onlinebutikken.
4. Tildel eller opret prisgrupper for onlinebutikken.
5. Konfigurer de leveringsmåder, der er tilgængelige i onlinebutikken.
6. Tildel de betalingsmetoder, der er godkendt af onlinebutikken.
7. Hvis du tillader, at kunder kan bestille varer online og derefter afhente dem i en lokal butik, skal du tildele butikssøgegrupper til onlinebutikken.
8. Tildel attributter for kanaler, produkter og salgsordrer til onlinebutikken. Kanalattributter gælder for hele onlinebutikken, produktattributter gælder for de produkter, der tilbydes i onlinebutikken, og salgsordreattributter gælder for de salgsordrer, der er genereret ud fra den onlinebutikken.
9. Tilknyt attributter for at definere egenskaber, der bestemmer, hvordan disse attributter opfører sig i onlinebutikken. Du kan f.eks. definere attributter, der er nødvendige, eller der kan søges i.
10. Publicer onlinebutikken for at generere butiksstrukturen for dit valg af tredjepartsonlinebutik.

    > [!IMPORTANT]
    > Før du publicerer onlinebutikken, skal du angive en distributionsplacering for den.

## <a name="commerce-channel-navigation-hierarchies"></a>Navigationshierarkier for Commerce-kanal

Før du opretter en onlinebutik, skal du definere det navigationshierarki for handelskanalen, du vil bruge for den. Navigationshierarkiet for kanalen repræsenterer det kategorihierarki, der vises i onlinebutikken, når butikken er udgivet. Når du udgiver produktkataloger i onlinebutikken, knyttes produkterne i kataloget til kategorierne i navigationshierarkiet for kanalen. Handlende bruger derefter hierarkiet til at navigere i onlinebutikken.

## <a name="organization-hierarchies"></a>Organisationshierarkier

Organisationshierarkier bruges til at strukturere handelskanaler og repræsentere relationerne mellem de organisationer, som dit firma består af. Når du opretter onlinebutikker, kan du føje dem til et organisationshierarki. Butikkerne deler derefter de data, der bruges til udvalg, genbestilling og rapportering. 

Når du opretter et organisationshierarki, tildeler du et formål til det. Formålet angiver, hvordan hierarkiet bruges i en forretningsstruktur. Opret et organisationshierarki for butiksdriften, og brug hierarkiet til udvalg, genbestilling og rapportering. 

Alternativt kan du oprette et separat organisationshierarki til hvert formål. Du kan også oprette flere hierarkier med samme formål og tildele særskilte kanaler til hver af disse. Hvis du vil udgive produktkataloger i onlinebutikken, bør du som minimum føje onlinebutikken til et organisationshierarki for sortimenter. Produkterne i et katalog udvælges fra de sortimenter, der er tildelt onlinebutikken. Når kataloget er udgivet, sammenligner udgivelsesprocessen ikrafttrædelsesdatoerne for det sortiment, der er tildelt onlinebutikken, med produkterne i kataloget, for at bestemme, hvilke produkter der skal være tilgængelige i onlinebutikken.
