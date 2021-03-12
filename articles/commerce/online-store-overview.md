---
title: Oversigt over e-handelswebsted
description: Dette emne giver et overblik over understøttelsen af e-handelswebsteder i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ae220e98acbda99255beefea598d973dbaa22368
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997541"
---
# <a name="e-commerce-site-overview"></a>Oversigt over e-handelswebsted

[!include [banner](includes/banner.md)]

Dette emne giver et overblik over understøttelsen af e-handelswebsteder i Microsoft Dynamics 365 Commerce. Det indeholder oplysninger om, hvordan onlinebutikker til e-handel initialiseres og administreres i Dynamics 365 Commerce. Det indeholder også link til flere oplysninger om onlinebutikker og om, hvordan du konfigurerer et e-handelswebsted. Selvom dette emne beskriver mange af de grundlæggende principper, dækker det ikke alt, hvad der kræves for at konfigurere et e-handels-produktionssted. Du kan finde flere avancerede emner i dokumentationen til Dynamics 365 Commerce.

## <a name="online-store-channel"></a>Onlinebutikskanal

Før du kan oprette dit websted i Dynamics 365 Commerce, skal du oprette mindst én onlinebutikskanal. Du kan finde flere oplysninger i [Konfigurere en onlinekanal](channel-setup-online.md). 

I Dynamics 365 Commerce bruger du en onlinebutikskanal til at etablere produkterne, priserne, sproget, betalingsmetoderne, leveringsmåderne, opfyldelsescentrene og andre aspekter af onlineoplevelsen, som bør være tilgængelige for dine kunder.

Der skal kun oprettes én onlinebutikskanal, før du kan komme i gang med Dynamics 365 Commerce. Et enkelt e-handelswebsted kan dog levere onlineoplevelsen for flere onlinebutikker. Hvis eksempelvis flere onlinebutikker er konfigureret til at understøtte forskellige geografiske områder, kan et enkelt sæt e-handelssider bruges til at give de unikke oplevelser, der er defineret af hver butik. Du finder flere oplysninger om, hvordan du konfigurerer et websted til at understøtte flere onlinebutikker under [Knyt et onlinewebsted til en kanal](associate-site-online-store.md).

Efter en onlinebutik er sat op, kan den være tilknyttet det Dynamics 365 Commerce-websted, der skal anvendes som din onlinebutiksfacade. Du finder flere oplysninger om onlinebutikker, og hvordan du konfigurerer dem, under [Konfiguration af onlinebutikker](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores).

## <a name="deploy-a-new-e-commerce-tenant"></a>Implementere en ny e-handelslejer

Under initialiseringen af et e-handelswebsted bliver du bedt om at angive et domænenavn. Du kan finde flere oplysninger om domæner i Commerce under [Konfigurere dit domænenavn](configure-your-domain-name.md) og [Domæner i Dynamics 365 Commerce](domains-commerce.md). Hvis du vil implementere en ny e-handelslejer ved hjælp af [Microsoft Dynamics Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide), skal du følge trinnene i [Implementere en ny e-handelslejer](deploy-ecommerce-site.md). Når din e-handelslejer er konfigureret i LCS, bliver der angivet et link til Commerce-webstedsgeneratoren. Du kan derefter bruge Commerce-webstedsgeneratoren til at initialisere og konfigurere dine e-handelswebsteder.

## <a name="initialize-your-e-commerce-site"></a>Initialisere dit e-handelswebsted

Når du starter Commerce-webstedsgeneratoren fra LCS, vises siden **Websteder**. Denne side indeholder to forudkonfigurerede websteder, **standard** og **fabrikam**, som vist i eksemplet i følgende illustration.

![Siden Websteder i Commerce-webstedsgeneratoren](media/e-commerce-site-01.png)

Når du vælger et af disse websteder, bliver du bedt om at vælge et domænenavn, en standard-onlinebutikskanal, et understøttet sprog for den valgte kanal og en sti. Hvis der kun bruges én kanal, kan du lade den pågældende sti være tom. Flere onlinebutikskanaler eller -sprog kan konfigureres senere i Commerce-webstedsgeneratoren. Der kræves en entydig sti til hver ekstra kanal eller sprog. Du har f.eks. to onlinekanaler, der er knyttet til et enkelt websted, og domænenavnet for webstedet er `www.fabrikam.com`. I dette tilfælde kan stien for en kanal være standardværdien, der ikke har en sti (`https://www.fabrikam.com`), og den anden kanal kan være indstillet til en ny sti, f.eks. **site2**, som vil have URL-adressen `https://www.fabrikam.com/site2`. I følgende illustration vises et eksempel på en dialogboks til initialisering af webstedet i Commerce-webstedsgeneratoren.

![Dialogboks til initialisering af websted i Commerce-webstedsgenerator](media/e-commerce-site-02.png)

Siden **Websteder** indeholder også knappen **Nyt websted**. Den dialogboks, der vises, når du vælger denne knap, minder om dialogboksen til webstedsinitialisering, men den bruges til at oprette et nyt websted. Nye websteder er tomme. De indeholder ikke de samme standardskabeloner, fragmenter, sider og billeder, der leveres på **standard**- og **fabrikam**-webstederne. Men du kan åbne en supportanmodning for at anmode om, at der føjes en kopi af standardindholdet til et nyt tomt websted, hvis du har brug for det. Du kan finde flere oplysninger under [Oprette et websted for e-handel](create-ecommerce-site.md).

Når et nyt websted er initialiseret, vises **Startside** for Commerce-webstedsgeneratoren. Denne side indeholder links til almindelige handlinger og vejledninger, som vist i eksemplet i følgende illustration.

![Links på startsiden i Commerce-webstedsgenerator](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a>Redigere onlinebutikskanaler eller føje onlinebutikskanaler til et e-handelswebsted

Når der er oprettet et e-handelswebsted, kan du ændre den kanal, som stedet er knyttet til, ved at følge trinnene i [Tilknytte et websted til e-handel med en onlinekanal](associate-site-online-store.md). I eksemplet i følgende illustration vises, hvordan et kanalhandlingsnummer (OUN) kan ændres på siden **Kanaler** (**Indstillinger for websted \> Kanaler**). Når du har foretaget en ændring, skal du huske at vælge **Gem og udgiv**. På denne måde sikrer du, at ændringen publiceres.

![Siden Kanaler i Commerce-webstedsgeneratoren](media/e-commerce-site-04.png)

Du kan tilføje nye kanaler ved at vælge **Tilføj en kanal**. Hvis du vil føje nye sprog til en kanal, skal du vælge kanalen og derefter vælge **Tilføj en landestandard** i den kanaldialogboks, der vises. Før landestandarder kan vises i dialogboksen, skal de forudkonfigureres til online butikskanalen i Commerce Headquarters.

![Dialogboksen Kanal i Commerce-webstedsgenerator](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a>Konfigurere en Azure B2C-lejer

Dynamics 365 Commerce bruger Azure Active Directory (Azure AD) B2C (business-to-consumer) til at understøtte brugerlegitimationsoplysninger og -godkendelsesstrømme. Oplysninger om, hvordan du konfigurerer din Azure B2C-lejer, finder du under [Konfigurere en B2C-lejer i Commerce](set-up-b2c-tenant.md), [Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md) og [Konfigurere flere B2C-lejere i et Commerce-miljø](configure-multi-b2c-tenants.md).

## <a name="overview-of-the-default-site-pages"></a>Oversigt over standardwebstedssiderne

Webstederne **standard** og **fabrikam** omfatter forudkonfigurerede skabeloner, fragmenter og sider, der kan hjælpe dig med at komme i gang. Du kan finde flere oplysninger under følgende emner:

- [Oversigt over startside](quick-tour-home-page.md)
- [Oversigt over side med produktdetaljer](quick-tour-pdp.md)
- [Oversigt over sider til indkøbsvogn og betaling ved kassen](quick-tour-cart-checkout.md)
- [Oversigt over sider til kontostyring](quick-tour-account-management.md)

## <a name="manage-site-settings"></a>Administrere webstedsindstillinger

Du kan finde flere oplysninger om, hvordan du administrerer dine webstedsindstillinger, i følgende emner:

- [Administrere e-handelsbrugere og -roller](manage-ecommerce-users-roles.md)
- [Overvejelser om optimering af søgeprogram (SEO) for webstedet](/search-engine-optimization-considerations.md)
- [Administrere sikkerhedspolitik for indhold (CSP)](manage-csp.md)
- [Vælge et tema for webstedet](select-site-theme.md)

## <a name="manage-site-content"></a>Administrere webstedsindhold

Du kan finde flere oplysninger om, hvordan du administrerer webstedsindhold, i følgende emner:

- [Ordliste til sidemodel](page-elements-overview.md)
- [Dokumenttilstande og -livscyklus](document-states-overview.md)
- [Skabeloner og layout](templates-layouts-overview.md)
- [Arbejde med fragmenter](work-with-fragments.md)
- [Arbejde med moduler](work-with-modules.md)
- [Oversigt over styring af digitale aktiver](dam-overview.md)
- [Modulbibliotek, oversigt](starter-kit-overview.md)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette et websted for e-handel](create-ecommerce-site.md)

[Implementere et nyt websted for e-handel](deploy-ecommerce-site.md)

[Tilknytte et onlinewebsted til en kanal](associate-site-online-store.md)

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)

[Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)
