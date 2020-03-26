---
title: Oprette et websted for e-handel
description: I dette emne beskrives de trin og oplysninger, der er nødvendige for at oprette et nyt e-handels-websted i Dynamics 365 Commerce-webstedsgeneratoren.
author: bicyclingfool
manager: AnnBe
ms.date: 03/02/2020
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
ms.openlocfilehash: 7177bae911dfa91a645b40581bf23b3ed76562a3
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096768"
---
# <a name="create-an-e-commerce-site"></a>Oprette et websted for e-handel


[!include [banner](includes/banner.md)]

I dette emne beskrives de trin og oplysninger, der er nødvendige for at oprette et nyt e-handels-websted i Dynamics 365 Commerce-webstedsgeneratoren.

Før du kan gå i gang med at udvikle dit e-handelswebsted, skal du først oprette et nyt websted i webstedsgeneratoren. 


Før du kan udvikle dit e-handelswebsted, skal du først oprette et nyt websted i webstedets oprettelsesmiljø. Før du kan oprette et nyt websted, skal der oprettes mindst én onlinebutik i Commerce. 


## <a name="set-up-your-site"></a>Konfigurere dit websted

Du kan konfigurere dit websted ved at gøre følgende:

1. Åbn webstedsgeneratormiljøet. Du kan finde et link til webstedsgeneratoren i Microsoft Lifecycle Services (LCS) på siden med miljøfunktioner til Commerce.
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

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Implementere et nyt websted for e-handel](deploy-ecommerce-site.md)

[Konfigurere en onlinebutikskanal](online-stores.md)

[Tilknytte et onlinewebsted til en kanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Masseoverføre omdirigeringer af URL-adresser](upload-bulk-redirects.md)

[Konfigurere en B2C-lejer i Commerce](set-up-B2C-tenant.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)

[Konfigurere flere B2C-lejere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)

[Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)
