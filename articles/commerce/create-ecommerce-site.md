---
title: Oprette et websted for e-handel
description: I dette emne beskrives de opgaver, der er knyttet til oprettelsen af et nyt e-handelswebsted i Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697123"
---
# <a name="create-an-e-commerce-site"></a>Oprette et websted for e-handel

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

I dette emne beskrives de opgaver, der er knyttet til oprettelsen af et nyt e-handelswebsted i Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Før du kan udvikle dit e-handelswebsted, skal du først oprette et nyt websted i webstedets oprettelsesmiljø. Før du kan oprette en nyt websted, skal der oprettes mindst én onlinebutik i Dynamics 365 Retail. 

## <a name="set-up-your-site"></a>Konfigurere dit websted

Du kan konfigurere dit websted ved at gøre følgende:

1. I Microsoft Lifecycle Services (LCS) skal du vælge linket til webstedets oprettelsesmiljø. 
1. Vælg **Nyt websted** på startsiden for webstedets oprettelsesmiljø.
1. I dialogboksen **Nyt websted** skal du angive følgende oplysninger.

| Felt                               | Beskrivelse |
|-------------------------------------|-------------|
| Navn på websted                           | Angiv det visningsnavn, der skal bruges til dit websted i webstedets oprettelsesmiljø. Dette navn er kun synligt i oprettelsesmiljøet og vil ikke blive vist for kunderne. |
| Sikkerhedsgruppe for webstedsadministrator | Angiv den Microsoft Azure Active Directory-sikkerhedsgruppe (Azure AD), der administrerer de brugere, der har rollen som webstedsadministrator på dette websted. |
| Standardkanal (driftsenhedsnummer) | Vælg den onlinebutik, som dette websted skal fungere som webstorefront for. Hvis du ønsker, at dit e-handelswebsted skal understøtte flere onlinebutikker, skal du knytte butikkerne til webstedet i **Indstillinger for websted**, efter at webstedet er konfigureret. |
| Standardsprog                            | Angiv standardsproget for denne onlinebutik og dette marked. En onlinebutik kan understøtte flere sprog. Hvis du vil understøtte flere sprog for denne onlinebutik eller en anden onlinebutik, kan du konfigurere denne understøttelse i **Indstillinger for websted**, når webstedet er konfigureret.  |
| Domæne                              | Vælg et domænenavn, der kan fungere som domæne for denne onlinebutik. Hvis du ikke har konfigureret nogen domæner i LCS, kan du lade dette felt være tomt. Når domænet er konfigureret i LCS, skal du føje det til din onlinebutik i **Indstillinger for websted**.  |
| Sti                              | Når webstedet understøtter mere end ét sprog for et bestemt domænenavn, skal du bruge stifeltet til at oprette en entydig URL-adresse til et websted for det pågældende domæne og sprogkombinationen. Hvis det sprog, du har angivet i feltet **Standardsprog**, er det eneste sprog, du vil understøtte for dette domæne, eller som fortsat er standardsproget, når du har lokaliseret dit websted til flere sprog, anbefales det, at du lader dette felt stå tomt. |


Når webstedet er oprettet, kan du kontrollere, om det er knyttet til din onlinebutik, ved at vælge fanen **Produkter**. Du bør kunne se det produktsortiment, der er tildelt til onlinebutikken. Du kan også bruge rullemenuen øverst til venstre på siden til at få adgang til de allokerede produkter efter kategori.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over onlinebutik](online-store-overview.md)

[Implementere et nyt websted for e-handel](deploy-ecommerce-site.md)

[Tilknytte et onlinewebsted til en kanal](associate-site-online-store.md)

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)

[Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)

[Oversigt over startside for oprettelse](authoring-home-overview.md)

[Tilføje en ny webstedsside](add-new-page.md)
