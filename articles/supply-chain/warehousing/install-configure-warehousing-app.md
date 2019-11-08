---
title: Oversigt over installation og konfiguration af appen Lagersted
description: I dette emne beskrives, hvordan du installerer og konfigurerer Dynamics 365 for Finance and Operations – appen Lagersted.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f629fffc5c424c244a25bb8faef0435814398ee1
ms.sourcegitcommit: 4aac45c84b87f463b22b318f5f6f729f8d737090
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2548962"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a>Oversigt over installation og konfiguration af appen Lagersted

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> Dette emne beskriver, hvordan du konfigurerer lagerfunktioner for skyinstallationer. Hvis du søger efter, hvordan du konfigurerer lagerfunktioner for lokale installationer, skal du se [Lager for lokale installationer](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


I dette emne beskrives, hvordan du installerer og konfigurerer Dynamics 365 for Finance and Operations – appen Lagersted.

Lagerstedsappen er tilgængelig i Google Play Butik og Microsoft Store. Til den aktuelle version af Dynamics 365 Supply Chain Management leveres denne app som en separat komponent, der skal installeres separat på enheder, der bruges til opgaver vedrørende lagersted. For at kunne bruge appen skal du downloade den til hver enhed og konfigurere den til at oprette forbindelse til dit Supply Chain Management-miljø. I dette emne beskrives, hvordan du installerer appen på dine enheder. Det forklares også, hvordan du kan konfigurere appen til at oprette forbindelse til dit Supply Chain Management-miljø.

## <a name="prerequisites"></a>Forudsætninger
Appen er tilgængelig på Android- og Windows-operativsystemer. Når du vil bruge appen, skal du have et af følgende understøttede operativsystemer installeret på dine enheder. Den skal også have en af følgende understøttede versioner. Du kan bruge oplysningerne i tabellen nedenfor til at vurdere, om din hardware og dit softwaremiljø er klar til at understøtte installationen.

| Platform                    | Version                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0, 9.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (alle versioner)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, version 1611 <br>-eller- <br>Microsoft Dynamics AX version 7.0/7.0.1 og Microsoft Dynamics AX platformsopdatering 2 med hotfix KB 3210014 |

## <a name="get-the-app"></a>Hent appen
-   Windows (UWP)
     - [Finance and Operations - Lagersted i Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - Windows (UWP): [Finance and Operations – Lagersted i Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> Zebra App Gallery findes ikke længere, hvilket betyder, at lagerstedsappen ikke længere kan downloades fra den pågældende placering.

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Oprette en webtjenesteapplikation i Azure Active Directory
For at aktivere appen til at kommunikere med en bestemt Supply Chain Management-server skal du registrere en webtjenesteapplikation i et Azure Active Directory til Supply Chain Management-lejeren. Af sikkerhedsmæssige årsager anbefaler vi, at du opretter en webtjenesteapplikation for hver enhed, du bruger. Når du vil oprette en webtjenesteapplikation i Azure Active Directory (Azure AD), skal du udføre følgende trin:

1.  Åbn en webbrowser, og gå til <https://portal.azure.com>.
2.  Angiv brugernavnet og adgangskoden for den bruger, der har adgang til Azure abonnementet.
3.  Klik i venstre navigationsrude i Azure Portal på **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Sørg for, at Active Directory-forekomsten er den, der bruges af Supply Chain Management.
5.  Klik på **App registreringer** på listen. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  I den øverste rude skal du klikke på **Ny registrering**. Guiden **Registrer en applikation** starter.
7.  Angiv et navn til applikationen, og vælg **Kun konti i denne organisations bibliotek**. Klik på **Tilmeld**.  [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Den nye appregistrering åbnes. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Husk **program-id'et**, du skal bruge det senere. **Program-Id'et** refereres senere til som **klient-id'et**.
10. Klik på **Certifikat og hemmeligheder** i ruden **Administrer**. Klik på **Ny klienthemmelighed**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)
11. Opret en nøgle ved at indtaste en nøglebeskrivelse og en varighed i sektionen **Adgangskoder**. Klik på **Tilføj**, og kopier nøglen. Denne nøgle vil senere blive kaldt for **Hemmelighed for klient**. [![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Opret og konfigurer en brugerkonto i Supply Chain Management
For at aktivere Supply Chain Management til at bruge din Azure AD-applikation skal du fuldføre følgende konfigurationstrin:

1.  Opret en bruger, der svarer til lagerstedsappens brugerlegitimationsoplysninger.
    1.  Gå til **Systemadministration** &gt; **Generelt** &gt; **Brugere**.
    2.  Opret en ny bruger.
    3.  Tildel Mobilenhedsbruger for lagersted, som vist på følgende skærmbillede. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Knyt din Azure Active Directory-applikation til brugeren af lagerstedsappen.
    1.  I Supply Chain Management skal du gå til **Systemadministration** &gt; **Opsætning** &gt; **Azure Active Directory-programmer**.
    2.  Opet en ny linje.
    3.  Angiv **Klient-ID** (fra det sidste afsnit), giv det et navn, og vælg den bruger, der er oprettet tidligere. Vi anbefaler, at du mærker alle dine enheder, så du nemt kan fjerne deres adgang til Supply Chain Management fra denne side i tilfælde af, at du mister dem. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigurere applikationen
Du skal konfigurere appen på enheden at oprette forbindelse til Supply Chain Management-serveren via Azure AD-applikationen. Dette gøres ved at gennemføre følgende trin.

1.  I appen skal du gå til **Forbindelsesindstillinger**.
2.  Ryd feltet **Demotilstand**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Angiv følgende oplysninger: 
    + **Azure Active Directory klient-id** - Brug klient-id'et fra trin 9 i "Oprette en webtjenesteapplikation i Active Directory". 
    + **Azure Active Directory-klienthemmelighed** - Brug klienthemmeligheden fra trin 11 i "Oprette en webtjenesteapplikation i Active Directory". 
    + **Azure Active Directory-ressource** - Azure AD Directory-ressource viser URL-adressen til Supply Chain Management-roden. **Bemærk**: Afslut ikke dette felt med en skråstreg (/). 
    + **Azure Active Directory-lejer** - Azure AD Directory-lejeren bruges sammen med Supply Chain Management-serveren: `https://login.windows.net/your-AD-tenant-ID`. F.eks.: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Bemærk**: Afslut ikke dette felt med en skråstreg (/). 
    + **Firma** - Angiv den juridiske enhed i Supply Chain Management, som applikationen skal oprette forbindelse til. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Vælg knappen **Tilbage** i applikationens øverste venstre hjørne. Applikationen opretter nu forbindelse til din Supply Chain Management-server, og logonskærmen for lagermedarbejderen vises. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Du kan finde oplysninger om, hvordan du konfigurerer lagerstedsappen til at scanne stregkoder ved hjælp af et kamera på en mobilenhed, i [Scanne stregkoder ved hjælp af et kamera i Dynamics 365 for Finance and Operations – Lager](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>Fjerne adgang til en enhed
I tilfælde af en mistet eller beskadiget enhed skal du fjerne adgangen til Supply Chain Management for enheden. De følgende trin beskriver den anbefalede proces til at fjerne adgangen.

1.  Gå til **Systemadministration** &gt; **Opsætning** &gt; **Azure Active Directory-programmer**.
2.  Slet den linje, der svarer til den enhed, du vil fjerne adgangen til. Husk det **klient-id**, der blev brugt til den fjernede enhed, du skal bruge det senere.
3.  Log på Azure-portalen på <https://portal.azure.com>.
4.  Klik på ikonet **Active Directory** ikon i menuen til venstre, og kontrollér, at du er i den rigtige mappe.
5.  Klik på **App registreringer** på listen, og klik derefter på den applikation, du vil konfigurere. Siden **Indstillinger** vises med konfigurationsoplysninger.
6.  Sørg for, at **klient-id'et** til programmet er det samme som i trin 2 i dette afsnit.
7.  Klik på knappen **Slet** i den øverste rude.
8.  Klik på **Ja** i bekræftelsesmeddelelsen.
