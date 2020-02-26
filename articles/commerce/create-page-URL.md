---
title: Oprette en side-URL
description: I dette emne beskrives de grundlæggende begreber og procedurer til oprettelse af en URL-adresse til en side på dit websted.
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 588cbedb077fab0663d3d62fc4a8b8ed915635b3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001915"
---
# <a name="create-a-page-url"></a>Oprette en side-URL


[!include [banner](includes/banner.md)]

I dette emne beskrives de grundlæggende begreber og procedurer til oprettelse af en URL-adresse til en side på dit websted.

## <a name="overview"></a>Oversigt

Den fuldstændige eller absolutte URL-adresse, der peger på en side på dit websted, består af særskilte dele. URL-adressen `https://www.contoso.com/en-us/contactus` har f.eks. følgende dele:

- `https://www.contoso.com` – HTTP-protokollen og webstedets domæne.
- `/en-us` – Webstedets sprogsti.
- `/contactus` – Den relative URL-adresse til siden **Kontakt os**. En relativ URL-adresse kaldes også en *URL-slug*.

Du angiver webstedets domæne og den valgfrie sprogsti, når du konfigurerer webstedet. Du kan føje flere domæner og sprogstier til webstedet via siden for onlinebutikker i indstillingerne for webstedet.

URL-sluggen for en side findes som en selvstændig enhed i webstedets oprettelsesmiljø. En sides URL-adresse består af to dele: et navn, der repræsenterer URL-sluggen, og en pointer til en side på enten webstedet eller et eksternt websted. En side-URL-adresse kan også konfigureres til at fungere som omdirigering til en anden side på enten webstedet eller et eksternt websted.

## <a name="create-a-page-url"></a>Oprette en side-URL

Der er to måder at oprette side-URL-adresser på:

- Automatisk, når du opretter en side
- Manuelt fra siden **URL-adresser**

### <a name="create-a-page-url-when-you-create-a-page"></a>Oprette en side-URL-adresse, når du opretter en side

Hvis du angiver et navn i feltet **URL-adresse**, når du opretter en ny side, oprettes der automatisk en side-URL-adresse, der peger på den pågældende side, på siden **URL-adresser**. Når du har publiceret URL-adressen og den side, den peger på, kan brugerne af webstedet (dine kunder) få adgang til den side, der er knyttet til URL-adressen.

> [!NOTE]
> Hvis du publicerer en URL-adresse uden at publicere den side, den peger på, får webstedets brugere en 404-fejl, når de forsøger at få adgang til siden. Hvis du publicerer en side uden at publicere den URL-adresse, der peger på den, kan der ikke opnås adgang til siden ved hjælp af en URL-adresse.

### <a name="manually-create-a-page-url"></a>Oprette en side-URL-adresse manuelt

Når du opretter nye sider, skal du ikke angive en side-URL-adresse. Hvis du lader feltet URL-adresse være tomt, oprettes siden i en ikke-sammenkædet tilstand. I dette tilfælde kan kunderne ikke få adgang til siden, selvom den er publiceret. Hvis du vil gøre siden tilgængelig, skal du oprette URL-adressen manuelt og knytte den til siden.

Hvis du vil oprette en sides URL-adresse manuelt, skal du følge disse trin.

1. På siden **URL-adresser** skal du vælge **Ny**.
1. Vælg den side på webstedet, som skal tilknyttes URL-adressen.
1. Angiv URL-sluggen, og vælg derefter **OK**.

På dette tidspunkt er URL-adressen i kladdetilstand. Den skal publiceres, før brugerne af webstedet kan få adgang til den tilknyttede side.

## <a name="update-a-page-url"></a>Opdatere en side-URL-adresse

Udfør følgende trin for at opdatere destinationssiden for en side-URL-adresse.

1. Vælg den URL-adresse, der skal opdateres, på siden **URL-adresser**.
1. Vælg ellipseknappen (**...**) ud for destinationssidefeltet i egenskabsruden til højre.
1. I dialogboksen skal du vælge en anden side og derefter vælge **OK**.
1. Gem og udgiv URL-adressen.

## <a name="redirect-a-page-url"></a>Omdirigere en side-URL-adresse

Det kan ske, at du ønsker, at dine kunder skal have vist en anden side, når de anmoder om en bestemt URL-adresse. I disse tilfælde er den bedste og nemmeste fremgangsmåde ofte at ændre den side, som side-URL-adressen peger på. Du kan dog have berettigede grunde til at bruge HTTP 301- eller 3023-omdirigeringer til at omdirigere anmodninger om en URL-adresse til en anden URL-adresse.

Hvis du vil omdirigere en URL-adresse til en anden URL-adresse, skal du følge disse trin.

1. Vælg den URL-adresse, der skal opdateres, på siden **URL-adresser**.
1. Vælg **Omdiriger** i egenskabsruden til højre.
1. Vælg en destination for omdirigeringen:

    - Hvis du vil pege på en anden side på dit websted, skal du vælge **Intern URL-adresse**, vælge ellipseknappen (**...**) og derefter vælge den URL-adresse, der skal omdirigeres til.
    - Hvis du vil pege på en side på det eksterne websted, skal du vælge **Ekstern URL-adresse** og derefter angive den fuldstændige URL-adresse for denne side. Husk at medtage protokollen. Angiv for eksempel `https://domain.com/new/page`. Hvis URL-adressen allerede omdirigerer til en intern URL-adresse, skal du vælge **Ryd valg**, før du kan angive en ekstern URL-adresse.

1. Vælg en omdirigeringstype:

    - **Permanent omdirigering (301)** – Vælg denne indstilling, når du ved, at dit indhold flyttes permanent og ikke vender tilbage til den forrige URL-adresse. Søgemaskiner tildeler SEO-værdien (Search Engine Optimization) for URL-adressen til omdirigering til den URL-adresse, der omdirigeres til, og opdaterer deres post til at vise den nye URL-adresse. 
    - **Midlertidig omdirigering (302)** – Vælg denne indstilling for at omdirigere trafik uden at opdatere søgemaskiner. Denne fremgangsmåde bruges typisk, hvis indholdet hurtigt vender tilbage til den forrige URL-adresse.

1. Når du er klar til at implementere omdirigeringen, skal du gemme og udgive URL-adressen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilpasse navigation på webstedet](customize-site-navigation.md)

[Tilføje en ny webstedsside](add-new-page.md)

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Føje sprog til webstedet](add-languages-to-site.md)
