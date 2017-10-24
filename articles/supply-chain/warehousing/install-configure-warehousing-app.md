---
title: Installere og konfigurere Microsoft Dynamics 365 for Finance and Operations &#8211; Lagersted
description: "I dette emne beskrives, hvordan du installerer og konfigurerer Microsoft Dynamics 365 for Finance and Operations – Lagersted."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 31e77b27d4bf95c997817b3a053b33119562adf8
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Installere og konfigurere Microsoft Dynamics 365 for Finance and Operations &#8211; Lagersted

[!include[banner](../includes/banner.md)]


I dette emne beskrives, hvordan du installerer og konfigurerer Microsoft Dynamics 365 for Finance and Operations – Lagersted.

Finance and Operations – Lagersted en applikation, der er tilgængelig i Google Play Butik og Windows Store. Til den aktuelle version af Finance and Operations leveres denne app som en separat komponent, der skal installeres separat på enheder, der bruges til opgaver vedrørende lagersted. For at kunne bruge appen i dit Finance and Operations-miljø skal du hente den ned på hver enhed og konfigurere den til at oprette forbindelse til dit Finance and Operations-miljø. I dette emne beskrives, hvordan du installerer appen på dine enheder. Det forklares også, hvordan du kan konfigurere appen til at oprette forbindelse til dit Finance and Operations-miljø.

## <a name="prerequisites"></a>Forudsætninger
Appen er tilgængelig på Android- og Windows-operativsystemer. Når du vil bruge appen, skal du have et af følgende understøttede operativsystemer installeret på dine enheder. Du skal også have en af følgende understøttede versioner af Finance and Operations. Du kan bruge oplysningerne i tabellen nedenfor til at vurdere, om din hardware og dit softwaremiljø er klar til at understøtte installationen.

| Platform                    | Version                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (alle versioner)                                                                                                                                                   |
| Finance and Operations | Microsoft Finance and Operations version 1611 <br>-eller- <br>Microsoft Dynamics AX version 7.0/7.0.1 og opdatering 2 til Microsoft Dynamics AX-platformen med KB 3210014 |

## <a name="get-the-app"></a>Hent appen
-   Windows (UWP): [Finance and Operations – Lagersted i Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android:
    - Windows (UWP): [Finance and Operations – Lagersted i Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations – Lagersted i Zebra App Gallery](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-active-directory"></a>Oprette en webtjenesteapplikation i Active Directory
For at aktivere appen til at kommunikere med en bestemt Finance and Operations-server skal du registrere en webtjenesteapplikation i et Azure Active Directory til Finance and Operations-lejeren. Af sikkerhedsmæssige årsager anbefaler vi, at du opretter en webtjenesteapplikation for hver enhed, du bruger. For at oprette en webtjenesteapplikation i Azure Active Directory (AD Azure), skal du udføre følgende trin:

1.  I en webbrowser skal du gå til <https://manage.windowsazure.com>.
2.  Angiv brugernavnet og adgangskoden for den bruger, der har adgang til Azure abonnementet.
3.  Klik i venstre navigationsrude i Azure Portal på **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Vælg den forekomst af Active Directory, der bruges af Finance and Operations, i gitteret.
5.  Klik på **Applikationer** på værktøjslinjen. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Klik på **Tilføj** i den nederste rude. Guiden **Tilføj applikation** starter.
7.  Angiv et navn til applikationen, og vælg **Webapplikation og/eller web-API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Angiv den logon-URL-adresse, som er URL-adressen til webapp. Denne URL-adresse er den samme som URL-adressen på din installation, men oauth er tilføjet i slutningen. Angiv program-ID-URI. Denne værdi er obligatorisk, men er ikke påkrævet for godkendelsen. Sørg for, at denne App ID-URI er en mock URI som f.eks. https://contosooperations/wmapp, da brug af URL-adressen til installationen kan medføre logonproblemer i andre AAD-programmer, f.eks. Excel-tilføjelsesprogrammet. [![WH-04-AD-add-properties3](./media/WH-04-AD-add-properties3.png)](./media/WH-04-AD-add-properties3.png)
9.  Gå til fanen **Konfigurer**. [![h-05-ad-Konfigurer-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Rul ned, indtil du ser afsnittet **Tilladelser til andre applikationer**. Klik på **Tilføj applikation**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Vælg **Microsoft Dynamics ERP** på listen. Klik på knappen **Fuldfør tjek** i højre hjørne af siden. [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. På listen **Deleger tilladelser** skal du markere alle afkrydsningsfelter. Klik på **Gem**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Noter de følgende oplysninger:
    -   **Klient-id** - Når du ruller op på siden, kan du se **Klient-id**.
    -   **Nøgle** – I afsnittet **Nøgler** skal du oprette en nøgle ved at vælge varigheden og kopiere nøglen. Denne nøgle vil senere blive kaldt for **Hemmelighed for klient**.

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Oprette og konfigurere en brugerkonto i Finance and Operations
For at aktivere Finance and Operations til at bruge din AD Azure-applikation, skal du fuldføre følgende konfiguration:

1.  Opret en ny brugerkonto i Azure Active Directory til Finance and Operations-lejeren. Formålet med denne brugerkonto er at få adgang til bestemte brugerdefinerede tjenester i lagerstedsappen, som vises i Finance and Operations-serveren. Når du har fuldført dette trin, har du WMDP-brugerlegitimationsoplysninger, som består af en WMDP e-mailadresse og en WMDP-adgangskode. Du kan finde oplysninger om de grundlæggende trin til at føje brugere til Azure AD og Finance and Operations i dette selvstudium: [Tilmelding til et Finance and Operations-abonnement](../../dev-itpro/dev-tools/sign-up-preview-subscription.md).
2.  Opret en Finance and Operations-bruger, der svarer til lagerstedsappens brugerlegitimationsoplysninger.
    1.  I Finance and Operations skal du gå til **Systemadministration** &gt; **Generelt** &gt; **Brugere**.
    2.  Opret en ny bruger.
    3.  Tildel Mobilenhedsbruger for lagersted, som vist på følgende skærmbillede. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Knyt din Azure Active Directory-applikation til brugeren af lagerstedsappen.
    1.  I Finance and Operations skal du gå til **Systemadministration** &gt; **Opsætning** &gt; **Azure Active Directory-applikationer**.
    2.  Opet en ny linje.
    3.  Angiv **Klient-ID** (fra det sidste afsnit), giv det et navn, og vælg den bruger, der er oprettet tidligere. Vi anbefaler, at du mærker alle dine enheder, så du nemt kan fjerne deres adgang til Finance and Operations fra denne side i tilfælde af, at de går tabt. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigurere applikationen
Du skal konfigurere appen på enheden at oprette forbindelse til Finance and Operations-serveren via Azure AD-applikationen. Dette gøres ved at gennemføre følgende trin.

1.  I appen skal du gå til **Forbindelsesindstillinger**.
2.  Ryd feltet **Demotilstand**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Angiv følgende oplysninger: 
    + **Azure Active Directory klient-id** - Brug klient-id'et fra trin 13 i "Oprette en webtjenesteapplikation i Active Directory". 
    + **Azure Active Directory-klienthemmelighed** - Brug klienthemmeligheden fra trin 13 i "Oprette en webtjenesteapplikation i Active Directory". 
    + **Azure Active Directory-ressource** - Azure AD Directory-ressource viser URL-adressen til Finance and Operations-roden. **Bemærk**: Afslut ikke dette felt med en skråstreg (/). 
    + **Azure Active Directory-lejer** - Azure AD Directory-lejeren bruges sammen med Finance and Operations-serveren: https://login.windows.net/dit-AD-lejer-ID. For eksempel: https://login.windows.net/contosooperations.onmicrosoft.com.
    <br>**Bemærk**: Afslut ikke dette felt med en skråstreg (/). 
    + **Firma** - Angiv den juridiske enhed i Finance and Operations, som applikationen skal oprette forbindelse til. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Vælg knappen **Tilbage** i applikationens øverste venstre hjørne. Applikationen opretter nu forbindelse til din Finance and Operations-server, og logonskærmen for lagermedarbejderen vises. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Fjerne adgang til en enhed
I tilfælde af en mistet eller beskadiget enhed skal du fjerne adgangen til Finance and Operations for enheden. De følgende trin beskriver den anbefalede proces til at fjerne adgangen.

1.  I Finance and Operations skal du gå til **Systemadministration** &gt; **Opsætning** &gt; **Azure Active Directory-applikationer**.
2.  Slet den linje, der svarer til den enhed, du vil fjerne adgangen til. Noter det **Klient-id**, der bruges til den fjernede enhed.
3.  Log på den klassiske Azure-portal på <https://manage.windowsazure.com>.
4.  Klik på ikonet **Active Directory** i menuen til venstre, og klik derefter på den ønskede mappe.
5.  Klik i den øverste menu på **Applikationer**, og klik derefter på den applikation, du vil konfigurere. Siden **Hurtig start** vises med single sign-on og andre konfigurationsoplysninger.
6.  Klik på fanen **Konfigurer**, rul ned, og sørg for, at **Klient-ID** for applikationen er det samme som i trin 2 i dette afsnit.
7.  Klik på knappen **Slet** på kommandolinjen.
8.  Klik på **Ja** i bekræftelsesmeddelelsen.





