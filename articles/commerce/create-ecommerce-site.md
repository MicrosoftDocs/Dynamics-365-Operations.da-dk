---
title: Oprette et websted for e-handel
description: Denne artikel beskriver de trin og oplysninger, der er nødvendige for at oprette et nyt e-handels-websted i Dynamics 365 Commerce-webstedsgeneratoren.
author: bicyclingfool
ms.date: 03/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: ea9afd89ce9ff79edbe5bff609b9843026005493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270231"
---
# <a name="create-an-e-commerce-site"></a>Oprette et websted for e-handel

[!include [banner](includes/banner.md)]

Denne artikel beskriver de trin og oplysninger, der er nødvendige for at oprette et nyt e-handels-websted i Dynamics 365 Commerce-webstedsgeneratoren.

Når du licenserer Dynamics 365 Commerce-funktionerne til e-handel, vil webstedsgeneratoren blive klargjort til et startsted, som du kan bruge som udgangspunkt for dit eget websted. Men hvis du vil starte fra bunden, eller hvis du vil oprette endnu et websted, skal du oprette et nyt websted i området til oprettelse af websted. 

## <a name="site-creation-prerequisites"></a>Forudsætninger for oprettelse af websted

En webstedsgenerator-bruger skal have en Microsoft Azure Active Directory-brugerkonto (Azure AD) inkluderet i den Azure AD-sikkerhedsgruppe, der er tildelt til e-handlens systemadministratorer. Du kan finde flere oplysninger i [Implementere en ny e-handelslejer](deploy-ecommerce-site.md).

> [!NOTE]
> Azure AD-gæstebrugere kan have forskellige adgangsrettigheder i din Azure AD-lejer. Selv hvis den er inkluderet i den Azure AD-sikkerhedsgruppe, der er tildelt systemadministratorer af e-handel,vil en gæstebruger muligvis have brug for, at Azure AD-rettighedsindstillingerne af **Eksterne brugere** skal ændres for at kunne oprette et e-handelswebsted i Commerce. 

Hvis du vil justere indstillinger for Azure AD **Eksterne brugere** , skal du følge disse trin.

1. Naviger til din Azure AD-lejer i Azure-portalen.
1. Gå til **Brugerindstillinger \> Eksterne brugere**, og vælg linket **Administrer eksterne samarbejdsindstillinger**. Derved åbnes siden **Indstillinger for eksternt samarbejde**, hvor gæstebrugeradgang, indstillinger for gæsteinvitationer og begrænsninger for samarbejde kan angives. 
1. Juster indstillingerne for eksternt samarbejde i overensstemmelse med dit firmas sikkerhedspolitikker. 

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

## <a name="rename-your-site"></a>Omdøbe dit websted

Hvis du vil omdøbe dit websted i webstedsgenerator, skal du følge disse trin.

1. Hvis du vil åbne webstedslistevisning, skal du vælge **Webstedsskifter** øverst til højre og derefter vælge **Administrer websteder**. 
1. Markér afkrydsningsfeltet ud for det websted, du vil omdøbe, og vælg derefter **Omdøb** på kommandolinjen.
1. Angiv det nye navn på webstedet i dialogboksen **Nyt navn på websted**, og vælg derefter **OK**. Listen med websteder opdateres, så den viser det nye navn.

## <a name="delete-a-site"></a>Slette et websted

Udfør følgende trin for at slette et websted i webstedsgeneratoren.

1. Hvis du vil åbne webstedslistevisning, skal du vælge **Webstedsskifter** øverst til højre og derefter vælge **Administrer websteder**.
1. Vælg det websted, du vil slette, og vælg **Slet** på kommandolinjen.
1. Angiv navnet på webstedet i dialogboksen **Slet \<site name\>**, og vælg derefter **Slet**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Implementere en ny e-handelslejer](deploy-ecommerce-site.md)

[Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Masseoverføre omdirigeringer af URL-adresser](upload-bulk-redirects.md)

[Konfigurere en B2C-lejer i Commerce](set-up-B2C-tenant.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)

[Konfigurere flere B2C-lejere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)

[Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
