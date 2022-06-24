---
title: Kopiere et e-handelswebsted
description: Denne artikel beskriver, hvordan du kopierer et eksisterende e-handelswebsted i eller mellem e-handelsmiljøer i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: psimolin
ms.date: 06/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: cb53a76b2ebe5b511bf5009727f20f20755e5720
ms.sourcegitcommit: 13c7a1cc4c90417e3e88db59b7d2165b3c40a56c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2022
ms.locfileid: "8935738"
---
# <a name="copy-an-e-commerce-site"></a>Kopiere et e-handelswebsted

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du kopierer et eksisterende e-handelswebsted i eller mellem e-handelsmiljøer i Microsoft Dynamics 365 Commerce-webstedsgenerator.

Dynamics 365 Commerce understøtter kopiering eller kloning af websteder som en selvbetjeningshandling i Commerce-webstedsgenerator. Websteder kan kopieres i et enkelt e-handelsmiljø eller mellem to e-handelsmiljøer. Den bruger, der starter kopieringen af webstedet, skal være lejeradministrator i både kilde- og destinations-e-handelsmiljøet.

Kopieringen af webstedet kopierer alt e-handelsindhold fra kildewebstedet. Dette indhold omfatter sider, fragmenter, skabeloner, URL-adresser og aktiver. Før et nyt websted kan bruges, skal det initialiseres via processen for første kørsel (FRE). Kanaler kan tilknyttes og administreres i webstedsgeneratoren med **Indstillinger for websted \> Kanaler**.

Varigheden af operationen for kopiering af websted afhænger primært af antallet af aktiver på kildewebstedet. I forbindelse med særligt store websteder anbefales det, at du i stedet overvejer at bruge miljøkopieringshandlingen. (Denne operation kaldes også dataportabilitet).

> [!NOTE]
> - Kildewebstedet er skrivebeskyttet, så længe kopieringen af webstedet varer.
> - Kun publicerede versioner af dokumenter kopieres. Hvis der ikke er publiceret nogen versioner, kopieres kun de seneste versioner.
> - Versionshistorikken for indhold vil ikke være tilgængelig på destinationswebstedet.

## <a name="copy-a-site-within-an-e-commerce-environment"></a>Kopiere et websted i et e-handelsmiljø

Hvis du vil kopiere et websted i et e-handelsmiljø, skal du følge disse trin.

1. Log på webstedsgeneratoren for det miljø, hvor du vil udføre kopieringshandlingen.
1. Åbn webstedslistevisning ved at vælge **Webstedsskifter** øverst til højre og derefter vælge **Administrer websteder**.
1. Find det websted, du vil kopiere eller klone, og markér afkrydsningsfeltet ud for navnet på webstedet.
1. Vælg **Kopier websted** på kommandolinjen.
1. Angiv et navn til det nye websted i feltet **Navn på nyt websted** i pop-op-menuen **Kopiér websted**. Det nye webstedsnavn skal være entydigt i e-handelsmiljøet. Felterne **Kildelejer** og **Kildewebsted** indstilles automatisk til oplysningerne for den aktuelle lejer og det valgte websted.
1. Vælg **Opret kopi**.

Når oplysningerne er valideret, viser en besked om, at der er oprettet et nyt job til kopiering af webstedet. Du kan overvåge status for jobbet i [højre rude på siden **Lejerjob**](#monitor-the-site-copy-operation). Når kopieringsoperationen er fuldført korrekt, vises det nye websted på listen over websteder i webstedslistevisning.

I følgende illustration vises et eksempel i pop-op-menuen **Kopiér websted** i webstedsgeneratoren.

![Pop-op-menuen Kopiér websted i webstedsgenerator.](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>Kopiere et websted mellem to e-handelsmiljøer

Hvis du vil kopiere et websted mellem to e-handelsmiljøer, skal du følge disse trin.

1. Log på webstedsgenerator for destinations-e-handelsmiljøet.
1. Vælg **Kopier websted** på kommandolinjen.
1. Angiv et navn til det nye websted i feltet **Navn på nyt websted** i pop-op-menuen **Kopiér websted**. Det nye webstedsnavn skal være entydigt i e-handelsmiljøet.
1. Vælg navnet på kildelejeren i feltet **Kildelejer**.
1. Vælg kildewebstedet i feltet **Kildewebsted**.
1. Vælg **Opret kopi**.

> [!NOTE]
> Administratortilladelser for lejere er påkrævet for både kilde- og destinations-e-handelsmiljøerne.

Når oplysningerne er valideret, viser en besked om, at der er oprettet et nyt job til kopiering af webstedet. Du kan overvåge status for jobbet i [højre rude på siden **Lejerjob**](#monitor-the-site-copy-operation). Når kopieringsoperationen er fuldført korrekt, vises det nye websted på listen over websteder i webstedslistevisning.

## <a name="map-channels-during-the-site-copy-operation-optional"></a>Tilknytte kanaler under kopiering af websted (valgfrit)

Kildekanaler og landestandarder kan knyttes til destinationskanaler og landelande som en del af kopieringshandlingen for webstedet. Hvis kanaltilknytning udføres som en del af kopieringshandlingen til webstedet, er det ikke nødvendigt at initialisere webstedet ved hjælp af den GRATIS process og konfigurere kanalerne i indstillinger for lokation. 

Benyt følgende fremgangsmåde for at tilknytte alle kanaler og landestandarder (1-til-1) i Site Builder.

1. Åbn webstedslistevisning ved at vælge **Webstedsskifter** øverst til højre og derefter vælge **Administrer websteder**.
1. Find det websted, du vil kopiere eller klone, og markér afkrydsningsfeltet ud for navnet på webstedet.
1. Vælg **Kopier websted** på kommandolinjen.
1. I menuen **Kopier websted** skal du angive værdier for **Nyt webstednavn**, **Kildelejer** og **Kildewebsted** (hvis det ikke allerede findes).
1. Vælg **Tilføj kanaltilknytninger**.
1. Vælg **Kildekanaler** i menuen **Konfigurer webstedskanaler og landestandarder**, og vælg derefter kildekanalen.  
1. Vælg **destinationskanal**, og vælg derefter samme kanal som kildekanalen. 
1. Vælg **Tilføj landestandard**.
1. Vælg **Kildelandestandard**, og vælg derefter kildelandestandard.
1. Vælg **destinationslandestandard**, og vælg derefter samme landestandard som kildelandestandarden. 
1. I forbindelse med **URL-stien** skal du angive en entydig URL-sti, der ikke bruges i destinationsmiljøet i øjeblikket.
1. Gentag trin 8-11 for hver landestandard, der skal knyttes til kanalen.
1. Vælg **Anvend**.
1. Gentag trin 6 til 11 for hver ekstra kildekanal.
1. Vælg **Luk**.
1. Gennemse konfigurationen for nøjagtighed, og vælg derefter **Kopiér websted**.

> [!NOTE]
> Alle kildekanaler og landestandarder skal tilknyttes, og de kan kun tilknyttes én gang.

## <a name="monitor-the-site-copy-operation"></a>Overvåge kopieringshandlingen for websted

Hvis du vil overvåge statussen for kopieringshandlingen for websted, skal du følge disse trin.

1. Log på webstedsgenerator for destinations-e-handelsmiljøet.
1. Vælg **Lejerjob** i navigationsruden til venstre.
1. Find og vælg jobbet til webstedets kopiering på listen på siden **Lejerjob**. Der vises en rude til højre med status og detaljer om det valgte job.

Du kan annullere et job, der har statussen **I gang**. Vælg jobbet på listen, og vælg derefter **Annuller** i kommandolinjen.

Du kan prøve et job igen, der har statussen **Mislykket** eller **Fuldført med fejl**. Vælg jobbet på listen, og vælg derefter **Nyt forsøg** i kommandolinjen.

> [!NOTE]
> Behandling af videoaktiver kan fortsætte, når et job til kopiering af et websted er fuldført.

Følgende illustration viser et eksempel på højre rude på siden **Lejerjob** i webstedsgenerator.

![Jobdetaljer i højre rude på siden Lejerjob i webstedsgenerator.](media/site-copy_2.png)

## <a name="initialize-a-new-site-by-using-the-fre-process"></a>Initialisere et nyt websted ved hjælp af processen FRE

Før et nyt websted kan bruges, skal det initialiseres via FRE-processen for første kørsel.

Hvis du vil initialisere et nyt websted ved hjælp af FRE-processen, skal du følge disse trin.

1. Log på webstedsgeneratoren for det nye websted.
1. Åbn webstedslistevisning ved at vælge **Webstedsskifter** øverst til højre og derefter vælge **Administrer websteder**.
1. Find og vælg det nye websted, du vil initialisere.
1. Vælg et domæne i feltet **Vælg domæne** i dialogboksen **Konfigurer dit websted**. Alle domæner, der var tilknyttet e-handelsmiljøet under initialisering, kan vælges.
1. Vælg den tilknyttede kanal for onlinebutik i feltet **Vælg en standardkanal**. Den valgte kanal indeholder sortimenter og andre oplysninger, der er gemt i Commerce Headquarters.
1. Vælg standardoprettelsessproget i feltet **Vælg et standardsprog**. Alle sprog, der er konfigureret til den valgte onlinebutikskanal, kan vælges.
1. Værdien i feltet **Sti** består af basisdomænet og en valgfri URL-sti, som du kan angive. Du kan lade URL-stien være tom, hvis kanalen skal betjenes fra domæneroden, eller hvis du vil angive disse oplysninger senere i kanalkonfigurationsvisningen i webstedsgeneratoren. Det webstedsstien skal være entydig i e-handelsmiljøet.
1. Vælg **OK**. Webstedet initialiseres med de oplysninger, du har angivet, og du sendes til administrationsvisningen for webstedet.

I følgende illustration vises et eksempel på dialogboksen **Konfigurer dit websted** i webstedsgeneratoren.

![Dialogboksen Konfigurer dit websted i webstedsgenerator.](media/site-copy_3.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Implementere en ny e-handelslejer](deploy-ecommerce-site.md)

[Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Masseoverføre omdirigeringer af URL-adresser](upload-bulk-redirects.md)

[Konfigurere en B2C-lejer i Commerce](set-up-b2c-tenant.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)

[Konfigurere flere B2C-lejere i et Commerce-miljø](configure-multi-b2c-tenants.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)

[Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)
