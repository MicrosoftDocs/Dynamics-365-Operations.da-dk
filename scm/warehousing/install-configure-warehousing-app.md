---
title: 'Installere og konfigurere Microsoft Dynamics 365 til operationer & #8211; Opbevaring'
description: Dette emne beskriver, hvordan du installerer og konfigurerer Microsoft Dynamics 365 for operationer - lager.
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Installere og konfigurere Microsoft Dynamics 365 til operationer & #8211; Opbevaring

Dette emne beskriver, hvordan du installerer og konfigurerer Microsoft Dynamics 365 for operationer - lager.

Dynamics 365 for operationer - lager er et program, der er tilgængelige på Google Play butik og Windows Store. Denne app leveres som en separat komponent, hvilket betyder, at selv installation på enheder, der bruges til lager-opgaver for den aktuelle version af Microsoft Dynamics 365 for operationer. For at bruge app i din Dynamics 365 for driftsmiljø, skal du hente app på hver enhed og konfigurere det til at oprette forbindelse til din Dynamics 365 for handlingsmiljø. Dette emne beskriver, hvordan du installerer programmet på dine enheder. Det forklarer også, hvordan du kan konfigurere programmet til at oprette forbindelse til din Dynamics 365 for handlingsmiljø.

## <a name="prerequisites"></a>Forudsætninger
Programmet er tilgængelig på Android og Windows-operativsystemer. Hvis du vil bruge dette program, skal du have en af følgende understøttede operativsystemer installeret på dine enheder. Du skal også have en af følgende understøttede versioner af Dynamics 365 for operationer. Du kan bruge oplysningerne i tabellen nedenfor til at vurdere, om din hardware og software miljø er klar til understøttelse af installationen.

| Platform                    | Version                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows-10 (alle versioner)                                                                                                                                                   |
| Dynamics 365 til operationer | Microsoft Dynamics 365 for operationer version 1611 opdager - eller - version 7.0/7.0.1 for Dynamics AX i Microsoft Dynamics og Microsoft Dynamics AX-platform update 2 med hotfix KB 3210014 |

## <a name="get-the-app"></a>Hent programmet
-   Windows (UWP) - [Dynamics 365 for operationer - lager til Windows store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 for operationer - opbevaring på Google Play butik](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Opret et webprogram til tjeneste i Active Directory
For at aktivere app til at kommunikere med en bestemt Dynamics 365 for operationer server, skal du registrere et webprogram til service i en Azure Active Directory til Dynamics-365 for lejeradministration operationer. Af sikkerhedsmæssige årsager anbefaler vi, at du opretter et webprogram til service for hver enhed, du bruger. For at oprette et webprogram til service i Azure Active Directory (AD Azure), skal du udføre følgende trin:

1.  I en webbrowser, gå til <https://manage.windowsazure.com>.
2.  Angiv brugernavn og adgangskode for den bruger, der har adgang til Azure abonnementet.
3.  Klik på i venstre navigationsrude i Azure Portal **Active Directory**. [](./media/wh-01-active-directory-example.png)[![HV-01-active-directory-eksempel](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Vælg forekomsten af Active Directory, der bruges af Dynamics 365 for operationer i gitteret.
5.  Klik på den øverste værktøjslinje, **programmer**. [![HV-02-active-directory-programmer](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  I den nederste rude, skal du klikke på **Tilføj**. Den **Tilføj program** starter guiden.
7.  Angiv et navn til det program, og vælg **-webprogrammet og/eller web API**. [![wh-03-Active-Directory-Add-Application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Angive Log på URL-adressen, som er programmet URL-adressen i din lejer, rod-URL-adresse til operationer. URL-on bruges i øjeblikket ikke aktivt i godkendelse af programmet, men det er et obligatorisk felt. Angiv den samme URL-adresse i feltet App ID URI. [![HV-04-ad-Tilføj-egenskaber](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Gå til den **Konfigurer** tab. [![HV-05-ad-konfiguration-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Rul ned, indtil du ser den **tilladelser til andre programmer** afsnit. Klik på **ansøgning om tilføjelse af**. [![wh-06-AD-App-Add-Permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Vælg **Microsoft Dynamics ERP** på listen. Klik på den **gennemføre** i højre hjørne af siden. [![HV-07-ad-select-tilladelser](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. I den **adgangstilladelser som stedfortræder** skal du vælge alle afkrydsningsfelter. Click **Save**. [![HV-08-ad--adgangstilladelser som stedfortræder](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Noter de følgende oplysninger:
    -   **Klient-ID** - når du ruller op siden, kan du se **klient-ID** vises.
    -   **Nøgle** – i den **nøgler** kan du oprette en nøgle ved at vælge varigheden og kopiere nøglen. Denne nøgle skal senere kaldes den **klient secret**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Oprette og konfigurere en brugerkonto i Dynamics 365 til operationer
For at aktivere Dynamics 365 for operationer til at bruge din AD Azure-program, skal du fuldføre følgende konfiguration:

1.  Opret en ny brugerkonto i Azure Active Directory til Dynamics-365 for lejeradministration operationer. Formålet med denne brugerkonto er adgang til bestemte brugerdefinerede af logistikfunktionerne app, som Fremviser Dynamics-365 for operationer server. Når du har fuldført dette trin, har du WMDP brugerlegitimationsoplysninger, som består af en WMDP e-mail-adresse og en adgangskode i WMDP. Til at lære de grundlæggende trin til at føje brugere til Azure AD og Dynamics 365 for operationer, referere til dette selvstudium: [tilmelding til en Microsoft Dynamics-365 operationer abonnement](/dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  Oprette en Dynamics 365 for operationer bruger, der svarer til lager app brugerens legitimationsoplysninger.
    1.  Dynamics 365 for operationer, gå til **systemadministration**&gt;**almindelige**&gt;**brugere**.
    2.  Opret en ny bruger.
    3.  Tildele brugeren lagersted mobil enhed, som vist på følgende skærmbillede. [![wh-09-Add-User-Security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Knytte programmet Azure Active Directory til brugeren logistikfunktionerne app.
    1.  Dynamics 365 for operationer, gå til **systemadministration**&gt;**Setup**&gt;**Azure Active Directory programmer**.
    2.  Opet en ny linje.
    3.  Angiv den **klient-ID** (fremstillet i det sidste afsnit), give den et navn, og vælg den bruger, der er oprettet tidligere. Vi anbefaler, at du mærker dine enheder, så du kan nemt fjerne deres adgang til Dynamics 365 for operationer fra denne side i tilfælde af, at de er tabt. [![HV-10-ad-programmer-formular](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigurere programmet
Du skal konfigurere app på enheden at oprette forbindelse til Dynamics-365 for operationer server via programmet Azure AD. Dette gøres ved at benytte følgende fremgangsmåde.

1.  I app, gå til **forbindelsesindstillinger**.
2.  Ryd den **Demo mode** felt. [![wh-11-App-Connection-Settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Indtast følgende oplysninger:- **Azure Active directory klient-ID** -klienten ID er fremstillet i trin 13 i "Oprette et webprogram til tjeneste i Active Directory". - **Azure Active directory-klienten secret** -klienten hemmeligheden er fremstillet i trin 13 i "Oprette et webprogram til tjeneste i Active Directory". - **Azure Active directory-ressource** -Azure AD directory ressource skildrer Dynamics-365 for URL-roden af operationer. **Bemærk**: ikke slutter dette felt med en skråstreg (/). - **Azure Active directory lejer** -Azure AD directory lejeradministration bruges sammen med Dynamics-365 for operationer server: https://login.windows.net/&lt;af-AD-lejer-ID&gt;. For eksempel: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Bemærk**: ikke slutter dette felt med en skråstreg (/). - **Virksomhed** -Angiv den juridiske enhed i Dynamics 365 for handlinger, som du vil programmet til at oprette forbindelse. [![HV-12-app--forbindelsesindstillinger](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Vælg den **tilbage** i øverste venstre hjørne af programmet. Programmet opretter nu forbindelse til din Dynamics 365 for operationer server og lagermedarbejderen-logonskærmen vises. [![Hva 13-login-skærm](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Fjern adgang til en enhed
I tilfælde af en mistet eller beskadiget enhed, skal du fjerne adgangen til Dynamics 365 for operationer for enheden. De følgende trin beskriver den anbefalede proces for at fjerne adgangen.

1.  Dynamics 365 for operationer, gå til **systemadministration**&gt;**Setup**&gt;**Azure Active Directory programmer**.
2.  Slet den linje, der svarer til den enhed, du vil fjerne adgangen. Skrive ned, den **klient-ID** bruges til den fjernede enhed.
3.  Log på Azure klassiske portalen på <https://manage.windowsazure.com>.
4.  Klik på den **Active Directory** ikon i menuen til venstre, og klik derefter på den ønskede mappe.
5.  Klik på den øverste menu **programmer**, og klik derefter på det program, du vil konfigurere. Den **Hurtig Start** side vises med single sign-on og andre konfigurationsoplysninger.
6.  Klik på den **Konfigurer** under fanen, Rul ned, og sikre, at den **klient-ID** er den samme som i trin 2 i dette afsnit af ansøgningen.
7.  Klik på den **slette** knap på kommandolinjen.
8.  Klik på **Ja** i bekræftelsesmeddelelsen.



