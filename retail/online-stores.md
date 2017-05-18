---
title: Oversigt over Onlinebutik
description: Denne artikel indeholder oplysninger om detailonlinebutikker, og hvordan du konfigurerer dem i Microsoft Dynamics 365 for Operations.
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: c41343c73d01235deee30fed4ff899cb8a6f50a5
ms.contentlocale: da-dk
ms.lasthandoff: 04/26/2017


---

# <a name="online-store-overview"></a>Oversigt over Onlinebutik

[!include[banner](includes/banner.md)]


Denne artikel indeholder oplysninger om detailonlinebutikker, og hvordan du konfigurerer dem i Microsoft Dynamics 365 for Operations.

Detail og handel i Dynamics 365 for Operations understøtter flere detailkanaler. Disse detailkanaler omfatter onlinebutikker, call centre og detailbutikker (også kaldet fysiske butikker). Onlinebutikker giver en detailhandler synlighed på internettet, så kunderne også kan købe produkter fra detailhandlerens onlinebutik ud over fra detailhandlerens fysiske butik. Hvis kunder køber produkter fra onlinebutikken, kan produkterne leveres til dem, eller kunden kan afhente dem i den lokale detailbutik. Du kan oprette en onlinebutik i Dynamics 365 for Operations-klienten. Denne onlinebutik udgives derefter til en tredjeparts onlinebutik, der er integreret i Dynamics 365 for Operations. Onlinebutikken fra tredjepart fungerer som butiksrude (brugergrænseflade) for onlinebutikken og giver dig et udvalg af funktioner til kundestyring og funktioner på brugergrænsefladen. Der findes flere integrationer af denne type til Dynamics 365 for Operations. De egenskaber, du definerer for onlinebutikken i, styrer funktionsmåden i onlinebutikken. Du kan f.eks. definere navigationskategorihierarkiet i Dynamics 365 for Operations og tildele onlinebutikken det. Når du udgiver onlinebutikken i en onlinebutik fra tredjepart, vises navigationskategorihierarkiet i onlineversionen af butikken. Handlende bruger derefter navigationskategorihierarkiet til at browse i onlinebutikken og søge efter produkter. Hvis du vil oprette en onlinebutik, skal du konfigurere de komponenter, der gør det muligt at behandle transaktioner for butikken. Du skal f.eks. tilføje udvalg, anvende attributter og konfigurere betalingsmetoder og forsendelsesmetoder. Du kan også definere priser, kampagner, rabatter, samhandelsaftaler og leveringsbetingelser, der er specifikke for onlinebutikken. Når du har udgivet onlinebutikken i onlinebutikken fra tredjepart, kan du oprette detailproduktkataloger for onlinebutikken. Produkterne i kataloget bliver vist i onlinebutikken. Når en kunde køber produkter fra onlinebutikken, opdateres det tilgængelige lager og synkroniseres i klienten. Desuden oprettes der salgsordrer for købene, og de sendes til klienten med henblik på ordreopfyldning og behandling.

## <a name="set-up-an-online-store"></a>Konfigurere en onlinebutik
Hvis du vil konfigurere en onlinebutik, skal du fuldføre følgende opgaver.

1.  Opret onlinebutikken.
2.  Tilføj onlinebutikken i de relevante organisationshierarkier.
3.  Tilføj sortimenter, der omfatter de produkter, der er tilgængelige i onlinebutikken.
4.  Tildel eller opret prisgrupper for onlinebutikken.
5.  Konfigurer de leveringsmåder, der er tilgængelige i onlinebutikken.
6.  Tildel de betalingsmetoder, der er godkendt af onlinebutikken.
7.  Hvis du tillader, at kunder kan bestille varer online og derefter afhente dem i en lokal butik, skal du tildele butikssøgegrupper til onlinebutikken.
8.  Tildel attributter for kanaler, produkter og salgsordrer til onlinebutikken. Kanalattributter gælder for hele onlinebutikken, produktattributter gælder for de produkter, der tilbydes i onlinebutikken, og salgsordreattributter gælder for de salgsordrer, der er genereret ud fra den onlinebutikken.
9.  Tilknyt attributter for at definere egenskaber, der bestemmer, hvordan disse attributter opfører sig i onlinebutikken. Du kan f.eks. definere attributter, der er nødvendige, eller der kan søges i.
10. Publicer onlinebutikken for at generere butiksstrukturen for dit valg af tredjepartsonlinebutik. **Vigtigt!** Før du publicerer onlinebutikken, skal du angive en distributionsplacering for den.

## <a name="retail-channel-navigation-hierarchies"></a>Navigationshierarkier for detailkanal
Før du opretter en onlinebutik, skal du definere det navigationshierarki for detailkanal, du vil bruge for den. Navigationshierarkiet for detailkanalen repræsenterer det kategorihierarki, der vises i onlinebutikken, når butikken er udgivet. Når du udgiver detailproduktkataloger i onlinebutikken, knyttes produkterne i kataloget til kategorierne i navigationshierarkiet for detailkanalen. Handlende bruger derefter hierarkiet til at navigere i onlinebutikken.

## <a name="organization-hierarchies"></a>Organisationshierarkier
Organisationshierarkier bruges til at strukturere detailkanaler. Organisationshierarkier repræsenterer relationerne mellem de organisationer, som dit firma består af. Når du opretter onlinebutikker, kan du føje dem til et organisationshierarki. Butikkerne deler derefter de data, der bruges til udvalg, genbestilling og rapportering. Når du opretter et organisationshierarki, tildeler du et formål til det. Formålet angiver, hvordan hierarkiet bruges i en forretningsstruktur. Opret et organisationshierarki for butiksdriften, og brug hierarkiet til udvalg, genbestilling og rapportering. Alternativt kan du oprette et separat organisationshierarki til hvert formål. Du kan også oprette flere hierarkier med samme formål og tildele særskilte kanaler til hver af disse. Hvis du vil udgive detailproduktkataloger i onlinebutikken, bør du som minimum føje onlinebutikken til et organisationshierarki for sortimenter. Produkterne i et katalog udvælges fra de sortimenter, der er tildelt onlinebutikken. Når kataloget er udgivet, sammenligner udgivelsesprocessen ikrafttrædelsesdatoerne for det sortiment, der er tildelt onlinebutikken, med produkterne i kataloget, for at bestemme, hvilke produkter der skal være tilgængelige i onlinebutikken.




