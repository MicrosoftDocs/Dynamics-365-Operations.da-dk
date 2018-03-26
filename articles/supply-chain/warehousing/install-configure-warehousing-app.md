---
title: Installere og konfigurere Microsoft Dynamics 365 for Finance and Operations &#8211; Lagersted
description: "I dette emne beskrives, hvordan du installerer og konfigurerer Microsoft Dynamics 365 for Finance and Operations – Lagersted."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 608543c9cfd93c4772e93089e1d174312d8b23a6
ms.openlocfilehash: 411bb28668f5aa9d07774211814da4e9757ac43c
ms.contentlocale: da-dk
ms.lasthandoff: 03/06/2018

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Installere og konfigurere Microsoft Dynamics 365 for Finance and Operations &#8211; Lagersted

[!include[banner](../includes/banner.md)]


> [!NOTE]

> Dette emne beskriver, hvordan du konfigurerer lagerfunktioner for skyinstallationer. Hvis du søger efter, hvordan du konfigurerer lagerfunktioner for lokale installationer, skal du se [Lager for lokale installationer](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


I dette emne beskrives, hvordan du installerer og konfigurerer Microsoft Dynamics 365 for Finance and Operations – Lagersted.

Finance and Operations – Lagersted en applikation, der er tilgængelig i Google Play Butik og Windows Store. Til den aktuelle version af Finance and Operations leveres denne app som en separat komponent, der skal installeres separat på enheder, der bruges til opgaver vedrørende lagersted. For at kunne bruge appen i dit Finance and Operations-miljø skal du hente den ned på hver enhed og konfigurere den til at oprette forbindelse til dit Finance and Operations-miljø. I dette emne beskrives, hvordan du installerer appen på dine enheder. Det forklares også, hvordan du kan konfigurere appen til at oprette forbindelse til dit Finance and Operations-miljø.

## <a name="prerequisites"></a>Forudsætninger
Appen er tilgængelig på Android- og Windows-operativsystemer. Når du vil bruge appen, skal du have et af følgende understøttede operativsystemer installeret på dine enheder. Du skal også have en af følgende understøttede versioner af Finance and Operations. Du kan bruge oplysningerne i tabellen nedenfor til at vurdere, om din hardware og dit softwaremiljø er klar til at understøtte installationen.

| Platform                    | Version                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (alle versioner)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, version 1611 <br>-eller- <br>Microsoft Dynamics AX version 7.0/7.0.1 og opdatering 2 til Microsoft Dynamics AX-platformen med KB 3210014 |

## <a name="get-the-app"></a>Hent appen
-   Windows (UWP)
     - [Finance and Operations - Lagersted i Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - Windows (UWP): [Finance and Operations – Lagersted i Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations – Lagersted i Zebra App Gallery](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Oprette en webtjenesteapplikation i Azure Active Directory
For at aktivere appen til at kommunikere med en bestemt Finance and Operations-server skal du registrere en webtjenesteapplikation i et Azure Active Directory til Finance and Operations-lejeren. Af sikkerhedsmæssige årsager anbefaler vi, at du opretter en webtjenesteapplikation for hver enhed, du bruger. For at oprette en webtjenesteapplikation i Azure Active Directory (AD Azure), skal du udføre følgende trin:

1.  Åbn en webbrowser, og gå til <https://portal.azure.com>.
2.  Angiv brugernavnet og adgangskoden for den bruger, der har adgang til Azure abonnementet.
3.  Klik i venstre navigationsrude i Azure Portal på **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Sørg for, at Active Directory-forekomsten er den, der bruges af Finance and Operations.
5.  Klik på **App registreringer** på listen. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  I den øverste rude skal du klikke på **Registrering af ny ansøgning**. Guiden **Tilføj applikation** starter.
7.  Angiv et navn til applikationen, og vælg **Webapplikation/web-API**. Angiv den logon-URL-adresse, som er URL-adressen til webapp. Denne URL-adresse er den samme som URL-adressen på din installation, men oauth er tilføjet i slutningen. Klik på **Opret**. [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Vælg den nye app på listen. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Husk **program-id'et**, du skal bruge det senere. **Program-Id'et** refereres senere til som **klient-id'et**.
10. Klik på **Nøgler** under ruden **Indstillinger**. Opret en nøgle ved at indtaste en nøglebeskrivelse og en varighed i sektionen **Adgangskoder**. 
11. Klik på **Gem**, og kopier nøglen. Denne nøgle vil senere blive kaldt for **Hemmelighed for klient**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

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
    + **Azure Active Directory klient-id** - Brug klient-id'et fra trin 9 i "Oprette en webtjenesteapplikation i Active Directory". 
    + **Azure Active Directory-klienthemmelighed** - Brug klienthemmeligheden fra trin 11 i "Oprette en webtjenesteapplikation i Active Directory". 
    + **Azure Active Directory-ressource** - Azure AD Directory-ressource viser URL-adressen til Finance and Operations-roden. **Bemærk**: Afslut ikke dette felt med en skråstreg (/). 
    + **Azure Active Directory-lejer** - Azure AD Directory-lejeren bruges sammen med Finance and Operations-serveren: `https://login.windows.net/your-AD-tenant-ID`. F.eks.: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Bemærk**: Afslut ikke dette felt med en skråstreg (/). 
    + **Firma** - Angiv den juridiske enhed i Finance and Operations, som applikationen skal oprette forbindelse til. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Vælg knappen **Tilbage** i applikationens øverste venstre hjørne. Applikationen opretter nu forbindelse til din Finance and Operations-server, og logonskærmen for lagermedarbejderen vises. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Oplysninger om, hvordan du konfigurerer Dynamics 365 for Finance and Operations – Lagersted til at scanne stregkoder ved hjælp af et kamera på en mobilenhed, finder du under [Scanne stregkoder ved hjælp af et kamera i Dynamics 365 for Finance and Operations – Lagersted](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>Fjerne adgang til en enhed
I tilfælde af en mistet eller beskadiget enhed skal du fjerne adgangen til Finance and Operations for enheden. De følgende trin beskriver den anbefalede proces til at fjerne adgangen.

1.  I Finance and Operations skal du gå til **Systemadministration** &gt; **Opsætning** &gt; **Azure Active Directory-applikationer**.
2.  Slet den linje, der svarer til den enhed, du vil fjerne adgangen til. Husk det **klient-id**, der blev brugt til den fjernede enhed, du skal bruge det senere.
3.  Log på Azure-portalen på <https://portal.azure.com>.
4.  Klik på ikonet **Active Directory** ikon i menuen til venstre, og kontrollér, at du er i den rigtige mappe.
5.  Klik på **App registreringer** på listen, og klik derefter på den applikation, du vil konfigurere. Siden **Indstillinger** vises med konfigurationsoplysninger.
6.  Sørg for, at **klient-id'et** til programmet er det samme som i trin 2 i dette afsnit.
7.  Klik på knappen **Slet** i den øverste rude.
8.  Klik på **Ja** i bekræftelsesmeddelelsen.

