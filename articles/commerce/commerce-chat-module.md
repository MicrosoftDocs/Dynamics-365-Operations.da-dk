---
title: Commerce-chat med Omnikanal til Customer Service-modulet
description: Denne artikel beskriver Commerce-chat med Omnikanal til Customer Service-modulet i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: e4a004b929138f0a04c19d6a94278cfad6e83303
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346380"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Commerce-chat med Omnikanal til Customer Service-modulet

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikel beskriver *Commerce-chat med Omnikanal til Customer Service*-modulet i Microsoft Dynamics 365 Commerce.

I Commerce version 10.0.29-udgivelsen er der føjet en ny Commerce Chat med Omnikanal til Customer Service-modulet til biblioteket til Commerce-modulet. Funktionen til Commerce-chat giver e-handelskunder mulighed for at få chat-egenskaberne i Dynamics 365 Omnikanal til Customer Service, som omfatter live helpdesk-medarbejder-understøttelse for at hjælpe med at løse kundeforespørgsler, give kundeservice og lette salget for Commerce-kunder.

Commerce-chatfunktionen gør det muligt for detailforretninger at nå disse mål:

- Øg personaliseret aftale med kunder om at forbedre tilbageholdelse af kundetilbageholdelse.
- Forbedre kundeservice ved hjælp af integration af helpdesk-medarbejderpersonale og selvbetjenings-chatrobotter.
- Hjælpe-helpdesk-medarbejdere får erfaring med kundeprofil, ordre og indkøbsdata i realtid, som styrer forbedringer og ansættelse af operationer.
- Forbedre den generelle kundetilfredshed for at øge salget.

Følgende funktioner er tilgængelige som del af Commerce-chatfunktionen:

- Commerce-chat med Omnikanal til Customer Service
- Tilføjelsen af **Commerce Call Center** som en programfane i helpdesk-medarbejderoplevelsen i Dynamics 365 Omnikanal til Customer Service

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Forudsætninger for Omnikanal til Customer Service

Som en forudsætning skal du konfigurere en chat i Omnikanal til Customer Service-widget, skal du have nogle af parametrene for at konfigurere Commerce-chatoplevelsen. Yderligere oplysninger finder du i [Konfigurere en chat-kanal](/dynamics365/customer-service/set-up-chat-widget).

Når du har konfigureret chat i Omnikanal til Customer Service Administration-widget, får du et script, der ligner følgende eksempel.

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

Kopier dette script, fordi du skal bruge værdierne i det for at konfigurere chatmodulet.

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>Commerce-chat med obligatoriske Omnikanal til Customer Service-felter

I nedenstående tabel vises scriptværdierne fra Omnichannel for Customer Service Administration-widget, der kræves for at konfigurere Commerce Chat med Omnikanal til Customer Service-modulet.

| Widget-egenskab | Beskrivende tekst |
| ------------- |--------------|
| Scriptkilde | Værdien af **src** i scriptet til chat-widget. |
| Dataprogram-id | Værdien af **data-app-id** i scriptet til chat-widget. |
| Dataorganisations-id | Værdien af **data-org-id** i scriptet til chat-widget. |
| Dataorganisations-URL | Værdien af **data-org-url** i scriptet til chat-widget. |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>Konfigurere Commerce-chatoplevelsen for dit e-handelswebsted

En anbefalet måde at implementere chatoplevelsen på dit e-handelswebsted på er at føje Commerce Chat med Omnikanal til Customer Service-modulet til det delte overskriftsområde, der bruges på webstedet med e-handel.

Følg disse trin, hvis du til tilføje chatmodulet til webstedets overskriftsfragment i Commerce-webstedsgenerator.

1. Naviger til **Fragmenter** i webstedsgeneratoren.
1. Vælg **Ny**.
1. I dialogboksen **Vælg et fragment** skal du vælge **Commerce Chat med Omnikanal til customer service**-modulet skal du angive et navn til fragmentet og derefter vælge **OK**.
1. I dispositionsvisningen skal du vælge **Msdyn365 cs chat connector**.
1. Benyt følgende fremgangsmåde i ruden **Chat-egenskaber**:

    1. I feltet **Script-kilde** skal du angive den **scr**-værdi, du har opnået fra Omnikanal til customer service-scriptet.
    1. I feltet **Dataprogram-id** skal du angive den **data-app-id**-værdi, du har opnået fra Omnikanal til customer service-scriptet.
    1. I feltet **Dataorganisations-id** skal du angive den **data-org-id**-værdi, du har opnået fra Omnikanal til customer service-scriptet.
    1. I feltet **Dataorganisations-URL** skal du angive den **data-org-url**-værdi, du har opnået fra Omnikanal til customer service-scriptet.

    ![Oprette et commerce chat-modulfragmenter i Commerce site builder.](media/Commerce-chat-creating-new-fragment.png)

1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.
1. Gå til **Fragmenter**, og åbn overskriftsfragmentet for dit websted.
1. På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj fragment**.
1. Vælg det fragment for chat, du oprettede tidligere, i dialogboksen **Vælg moduler**, og vælg derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>Tilføj Commerce Headquarters som en fanen Program til Omnikanal til Customer Service

Du kan tilføje Commerce Headquarters som fanen Program til Omnikanal til Customer Service. Live helpdesk-medarbejdere kan derefter bruge brugergrænsefladen for Omnikanal til Customer Service-helpdesk-medarbejderoplevelsen til let at få adgang til Dynamics 365 Commerce-modulet Kundeservice, der indeholder kontekstoplysninger om kunden sammen med oplysningerne om salgsordrer. Kundeservicemedarbejdere kan desuden oprette nye ordrer, starte returneringer og kontrollere oplysninger om ordrestatus.

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>Oprette en ny programfan, der indlæser Commerce Headquarters i et iFrame-modul 

Opret en ny programfane, der indlæser Commerce Headquarters i et iFrame-modul ved at følge disse trin.

1. Åbn [Power Apps Maker Portal](https://make.powerapps.com).
1. Vælg **Apps** i navigationsruden til venstre.
1. Vælg **Customer Service Administration**.
1. Gå til **Medarbejderoplevelse**.
1. Vælg **Administrer** for **skabeloner under fanen Applikation**.
1. Opret en ny programfane af typen **tredjepartswebsted**. Yderligere oplysninger findes i [Administrer for skabeloner under fanen Applikation](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter).
1. Under **Parametre** skal du angive følgende URL-adresse i feltet **Værdi** i parameteren **url**, hvor `<YourOrganizationHeadquartersURL>` og `<LegalEntityname>` erstattes med de relevante værdier. Omnikanal til Customer Service læser **{AccountNumber}** fra chatkonteksten. Derfor lad **{AccountNumber}** være.

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. Lad feltet **Værdi** i parameteren **data** være tom.

![Oprette en programfane i Dynamics 365 Omnikanal til Customer Service.](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>Aktivere en ny programfane for kundemedarbejdere i Dynamics 365 Omnikanal til Customer Service

Aktivere en ny programfane for kundemedarbejdere i Dynamics 365 Omnikanal til Customer Service ved at følge disse trin.
    
1. Åbn [Power Apps Maker Portal](https://make.powerapps.com).
1. Vælg **Apps** i navigationsruden til venstre.
1. Vælg **Customer Service Administration**.
1. Gå til **Kundesupport \> Arbejdsstrømme**.
1. Åbn den arbejdsstrøm, du har oprettet til dine medarbejdere, og vælg derefter **sessionsstandard** under **Avancerede indstillinger**.
1. Under **faner til ansøgninger** skal du vælge **Tilføj eksisterende programfane** og derefter tilføje den nye programfane, du oprettede tidligere. Dette trin sikrer, at der vises en programfan, der indlæser Commerce Headquarters i et iFrame-modul, når en medarbejder modtager et indgående chat-opkald fra dit e-handelswebsted.

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>Tilføj kontekstvariabler i Dynamics 365 Omnikanal til Customer Service

Tilføj kontekstvariabler i Dynamics 365 Omnikanal til Customer Service ved at følge disse trin.

1. Åbn [Power Apps Maker Portal](https://make.powerapps.com).
1. Vælg **Apps** i navigationsruden til venstre.
1. Vælg **Customer Service Administration**.
1. Gå til **Kundesupport \> Arbejdsstrømme**.
1. Åbn den arbejdsstrøm, du har oprettet til dine medarbejdere, og vælg derefter **Kontekstvariabel** under **Avancerede indstillinger**.
1. Vælg **Rediger**, og tilføj derefter **AccountNumber** som en kontekstvariabel af **teksttypen**. Denne variabel hjælper Commerce headquarters med at indlæse kundeoplysninger med tilsvarende kontonumre.

> [!NOTE]
> Hvis du vil læse e-mail-adresserne og navnene på brugere, der er logget på fra en e-handelskanal, kan du tilføje **E-mail** og **Navn** som kontekstvariabler af **teksttypen** samt kontekstvariablen **AccountNumber**.
