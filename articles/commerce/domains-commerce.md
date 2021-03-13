---
title: Domæner i Dynamics 365 Commerce
description: Dette emne beskriver, hvordan domæner håndteres i Microsoft Dynamics 365 Commerce.
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: d855f2164e4ee0f0cdb220787eb96217523137e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010241"
---
# <a name="domains-in-dynamics-365-commerce"></a>Domæner i Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan domæner håndteres i Microsoft Dynamics 365 Commerce.

Domæner er webadresser, der bruges til at navigere til Dynamics 365 Commerce-websteder i en webbrowser. Du styrer administrationen af dit domæne hos en valgt DNS-serverudbyder (Domain Name Server). Der henvises til domæner i hele Dynamics 365 Commerce-webstedsgeneratoren for at koordinere, hvordan der er adgang til et websted, når det udgives. I dette emne gennemgås, hvordan domæner håndteres og henvises til i hele livscyklussen for udviklingen og lanceringen af Commerce-webstedet.

## <a name="provisioning-and-supported-host-names"></a>Klargøring og understøttede værtsnavne

Når der klargøres et e-handelsmiljø i [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), bruges feltet **Understøttede værtsnavne** på skærmen for klargøring af e-handel til at angive domæner, der knyttes til det udrullede Commerce-miljø. Disse domæner er kundeorienterede DNS-servernavne, som er vært for e-handelswebsteder. Hvis du angiver et domæne på dette stadie, starter det ikke omdirigering af trafik for domænet til Dynamics 365 Commerce. Trafik for et domæne sendes kun til Commerce-slutpunktet, når DNS CNAME-posten opdateres til at bruge Commerce-slutpunktet sammen med domænet.

> [!NOTE]
> Der kan angives flere domæner i feltet **Understøttede værtsnavne** ved at adskille dem med semikoloner.

I følgende illustration vises LCS-skærmen til klargøring af e-handel, hvor feltet **Understøttede værtsnavne** er fremhævet. 

![LCS-skærmen til klargøring af e-handel, hvor feltet **Understøttede værtsnavne** er fremhævet](./media/Domains_ProvisioningeCommerceScreen.png)

Du kan oprette en serviceanmodning for at føje flere domæner til et miljø, hvis der allerede er foretaget klargøring. Hvis du vil oprette en serviceanmodning i LCS, skal du i dit miljø gå til **Support \> Supportproblemer** og vælge **Send en hændelse**.

## <a name="commerce-generated-urls"></a>Commerce-genererede URL-adresser

Ved klargøring af et Dynamics 365 Commerce-e-handelsmiljø vil Commerce generere en URL-adresse, der er arbejdsadressen for miljøet. Der henvises til denne URL-adresse i linket til e-handelwebstedet, som vises i LCS, efter at miljøet er klargjort. En Commerce-genereret URL-adresse har formatet `https://<e-commerce tenant name>.commerce.dynamics.com`, hvor navnet på e-handelslejeren er det navn, der er angivet i LCS for Commerce-miljøet.

Du kan også bruge værtsnavne for produktionswebsteder i et sandkassemiljø. Denne mulighed er ideel, når du kopierer et websted fra et sandkassemiljø til produktion.

## <a name="site-setup"></a>Webstedopsætning

Når dit e-handelsmiljø er klargjort, skal du konfigurere webstedet i Commerce-webstedsgeneratoren for at kunne knytte dit websted til URL-arbejdsadressen.

Første gang du konfigurerer et websted i webstedsgeneratoren, vises dialogboksen **Konfigurer dit websted**.

I følgende illustration vises dialogboksen **Konfigurer dit websted** for et websted med navnet "standard", når du får adgang til webstedet for første gang i webstedsgeneratoren.

![Dialogboksen **Konfigurer dit websted**](./media/Domains_SetupyoursiteScreen.png)

I feltet **Vælg et domæne** kan du knytte et af de understøttede værtsnavne, der er leveret til dit websted i LCS, til dit websted i webstedsgeneratoren.

Feltet **Sti** kan være tomt, eller der kan tilføjes en ekstra stistreng, som afspejles i din URL-arbejdsadresse. Når du feltet **Sti** være tomt, knyttes den Commerce-genererede URL-basisadresse til webstedet i webstedsgeneratoren. Stier skal være entydige for de enkelte par af websted/domæne. Inden for webstedet og domænet kan kun ét websted i miljøet bruge den tomme sti eller være tilknyttet en entydig stistreng. Enhver streng, der føjes til feltet **Sti** under opsætningen af webstedet, bliver en understi til den Commerce-genererede URL-basisadresse, der bruges til at få adgang til webstedet i en webbrowser.

> [!NOTE]
> Stien kaldes også den **matchende sti**, når der tilføjes en kanal i konfigurationssektionen **Indstillinger for websted \> Kanaler** i webstedsgeneratoren.

Hvis du f.eks. har et websted i webstedsgeneratoren kaldet "fabrikam" i en e-handelslejer med navnet "xyz", og hvis du konfigurerer webstedet med en tom sti, vil du få adgang til det udgivne websteds indhold i en webbrowser ved at gå direkte til den Commerce-genererede URL-basisadresse:

`https://xyz.commerce.dynamics.com`

Hvis du også har tilføjet en sti til "fabrikam" under dette websteds opsætning, kan du få adgang til det udgivne websteds indhold i en webbrowser ved hjælp af følgende URL-adresse:

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a>Sider og URL-adresser

Når webstedet er konfigureret med en sti, bygger alle URL-adresser, der er knyttet til sider i webstedsgeneratoren, på URL-arbejdsadressen (den Commerce-genererede URL-adresse eller den Commerce-genererede URL-adresse plus stien) til webstedet. Oprettelse af en ny URL-adresse i webstedsgenerator (**URL-adresser/> + Ny**) ved at vælge en side på listen i dialogboksen **Ny URL-adresse** og angive URL-stien til siden vil knytte URL-adressen til den valgte side. Værdien af URL-stien føjes derefter til webstedets URL-arbejdsadresse for at give adgang til siden, og den angives som `./<URL path>` på URL-adresselisten på **URL-adresse**-siden i webstedsgenerator.

Følgende illustration viser dialogboksen **Ny URL-adresse** i webstedsgenerator med eksempel på en URL-sti fremhævet. 

![Dialogboksen **Ny URL-adresse** i webstedsgenerator](./media/Domains_PageSetup2a.png)

Følgende illustration viser siden **URL-adresser** i webstedsgenerator med eksempel på en URL-adresse fremhævet på listen.

![Kør indstillingen brugerstrøm i politikstrøm](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Domæner i webstedsgenerator

De understøttede værdier for værtsnavne kan knyttes til et domæne, når der konfigureres et websted. Når du vælger en understøttet værdi for et værtsnavn som domænet, får du vist refererer til det valgte domæne fra hele webstedsgeneratoren. Dette domæne er kun en reference i Commerce-miljøet, så der videresendes ikke direkte trafik til det pågældende domæne i Dynamics 365 Commerce.

Når du arbejder med websteder i webstedsgenerator, og du har to websteder konfigureret med to forskellige domæner, kan du føje attributten **?domain=** til din URL-arbejdsadresse for at få adgang til det udgivne websteds indhold i en browser.

Miljøet "xyz" er f.eks. blevet klargjort, og to websteder er blevet oprettet og tilknyttet i webstedsgenerator: en med domænet `www.fabrikam.com` og det andet med domænet `www.constoso.com`. Hvert websted er konfigureret ved hjælp af en tom sti. Du kan få adgang til disse to websteder i en webbrowser på følgende måde ved hjælp af attributten **?domain=**:
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

Når der ikke er angivet en domæneforespørgselsstreng i et miljø med flere domæner, bruger Commerce det første domæne, du har angivet. Hvis f.eks. stien "fabrikam" blev angivet først under opsætningen af webstedet, kan URL-adressen `https://xyz.commerce.dynamics.com` bruges til at få adgang til det indhold, der er udgivet til webstedet for `www.fabrikam.com`.

## <a name="traffic-forwarding-in-production"></a>Videresendelse af trafik i produktion

Du kan simulere flere domæner ved hjælp af parametre for domæneforespørgselsstrenge på selve commerce.dynamics.com slutpunktet. Men når du skal aktivere det i produktionen, skal du videresende trafikken for dit brugerdefinerede domæne til slutpunktet for `<e-commerce tenant name>.commerce.dynamics.com`.

Slutpunktet `<e-commerce tenant name>.commerce.dynamics.com` understøtter ikke brugerdefinerede SSL'er (Secure Sockets Layer), så du skal konfigurere brugerdefinerede domæner ved hjælp af en Front Door Service eller et Content Delivery Network (CDN). 

Hvis du vil konfigurere brugerdefinerede domæner ved hjælp af en Front Door Service eller CDN, har du to muligheder:

- Konfigurer en Front Door Service som Azure Front Door for at håndtere frontend-trafik og oprette forbindelse til Commerce-miljøet. Det giver større kontrol over domæne- og certifikatstyring og mere detaljerede sikkerhedspolitikker.
- Brug den Commerce-leverede Azure Front Door-forekomst. Det kræver en handling til koordinering med Dynamics 365 Commerce-teamet i forbindelse med domænebekræftelse og anskaffelse af SSL-certifikater til dit produktionsdomæne.

Du kan finde oplysninger om, hvordan du konfigurerer en CDN-tjeneste direkte, under [Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md).

Hvis du vil bruge den Commerce-leverede Azure Front Door forekomst, skal du oprette en serviceanmodning til CDN-opsætningen fra Commerce-onboarding-teamet. 

- Du skal angive firmanavn, produktionsdomæne, miljø-id og produktionens e-handelslejernavn. 
- Du skal bekræfte, om dette er et eksisterende domæne (bruges til et aktuelt aktivt websted) eller et nyt domæne. 
- I forbindelse med et nyt domæne kan domænebekræftelse og SSL-certifikatet foretages i et enkelt trin. 
- I forbindelse med et domæne, der betjener et eksisterende websted, kræves der en proces med flere trin for at fastlægge domænebekræftelse og SSL-certifikat. Denne proces har en 7-dages serviceniveauaftale (SLA) for et domæne, der skal være aktivt, fordi det omfatter flere sekventielle trin.

Hvis du vil oprette en serviceanmodning i LCS, skal du i dit miljø gå til **Support \> Supportproblemer** og vælge **Send en hændelse**.

> [!NOTE]
> Brugerdefinerede domæner med SSL understøttes kun i produktionsmiljøer. I forbindelse med ikke-produktionsmiljøer som f.eks. sandkasse og test af brugeraccept (UAT) skal du bruge den Commerce-genererede URL-adresse til at få adgang til udgivet indhold i en webbrowser.

## <a name="ssl-certificate-process"></a>SSL-certifikatproces

Når en serviceanmodning er blevet gemt, koordinerer Commerce-teamet følgende trin med dig.

For nye domæner:
- Commerce-teamet konfigurerer forekomsten af Azure Front Door (Commerce-vært).
- Derefter giver Commerce-teamet CNAME-posten mulighed for at henvise til dit brugerdefinerede domæne.
- Når CNAME-posten er opdateret, vil forekomsten af Azure Front Door med Commerce-vært være i stand til at kontrollere domæneejerskabet og få SSL-certifikatet.

For eksisterende/aktive domæner:
- Commerce-teamet vil bede dig om at tilføje en `afdverify.<custom-domain>`-CNAME-post, som du kan levere til din DNS-domæneudbyder.
- Derefter vil Commerce-teamet føje domænet til Azure Front Door-forekomsten og levere yderligere DNS TXT-poster, der skal tilføjes DNS for domænet.
- Når TXT-posterne er fuldført, vil Commerce-teamet fuldføre opdateringen af Azure Front Door for det domæne, der skal konfigurere SSL-certifikatet.

## <a name="apex-domains"></a>Toppunktdomæner

Den Commerce-leverede Azure Front Door-forekomst understøtter ikke toppunktdomæner (roddomæner, der ikke indeholder underdomæner). Toppunktdomæner kræver en IP-adresse for at kunne fortolkes, og der findes kun virtuelle slutpunkter for Commerce Azure Front Door-forekomsten. Hvis du vil bruge et toppunktdomæne, har du to muligheder:

- **Mulighed 1** - Brug DNS-udbyderen til at omdirigere toppunktdomænet til et "www"-domæne. F.eks. omdirigerer fabrikam.com til `www.fabrikam.com`, hvor `www.fabrikam.com` er den CNAME-post, der peger på den Commerce-tilknyttede Azure Front Door-forekomst.

- **Mulighed 2** - Konfigurer selv en CDN/front door-forekomst som vært for toppunktdomænet.

> [!NOTE]
> Hvis du bruger Azure Front Door, skal du også konfigurere en Azure DNS i det samme abonnement. Toppunktdomænet, der har Azure DNS som vært, kan pege på din Azure Front Door som en aliaspost. Dette er den eneste løsning, da toppunktdomæner altid skal pege på en IP-adresse.

  ## <a name="additional-resources"></a>Yderligere ressourcer

  [Implementere en ny e-handelslejer](deploy-ecommerce-site.md)

  [Konfigurere en onlinebutikskanal](online-stores.md)

  [Oprette et websted for e-handel](create-ecommerce-site.md)

  [Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal](associate-site-online-store.md)

  [Administrere robots.txt-filer](manage-robots-txt-files.md)

  [Masseoverføre omdirigeringer af URL-adresser](upload-bulk-redirects.md)

  [Konfigurere en B2C-lejer i Commerce](set-up-B2C-tenant.md)

  [Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)

  [Konfigurere flere B2C-lejere i et Commerce-miljø](configure-multi-B2C-tenants.md)

  [Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)

  [Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)
