---
title: Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration
description: Denne artikel beskriver, hvordan du aktiverer Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f8b84938c2047ab1102864cc203e0ec853160bb1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274307"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du aktiverer Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.

Hvis du vil klargøre Teams med oplysninger fra Dynamics 365 Commerce og synkronisere funktionerne til opgavestyring mellem Teams og POS-programmet (POS), skal du aktivere integrationsfunktionerne i Commerce Headquarters.

> [!NOTE]
> Når du aktiverer integration med Teams, giver du dit samtykke til at dele dine data med Teams. Data, der deles med Teams, kan være i et andet land end dine Commerce-data, og de kan være underlagt forskellige overholdelser af angivne standarder. Der er flere oplysninger i [Microsofts Sikkerhedscenter](https://www.microsoft.com/trust-center). Du kan finde oplysninger om Microsofts politikker for beskyttelse af personlige oplysninger i [Microsofts erklæring om beskyttelse af personlige oplysninger](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Aktivere Teams-integration

Før du kan aktivere Microsoft Teams-integration med Commerce, skal du registrere Teams-programmet hos din lejer på Azure-portalen.

Du kan registrere Teams-programmet hos din lejer på Azure-portalen ved at følge disse trin.

1. Følg trinnene i [Hurtig start: Registrer en app på Microsofts id-platform](/azure/active-directory/develop/quickstart-register-app) for at registrere Teams-programmet hos din lejer på Azure-portalen.
1. Vælg den app, du oprettede i det forrige trin, under fanen **Appregistrering**. Vælg derefter **Tilføj en platform** under fanen **Godkendelse**.
1. Vælg **Web** i dialogboksen. Angiv derefter en URL-adresse i formatet **\<HQUrl\>/oauth** i feltet **URL-adresse til omdirigering**. Erstat **\<HQUrl\>** med URL-adressen til Commerce Headquarters (f.eks. `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`).
1. Kopiér værdien af **Program-id (klient)** fra siden **Oversigt** for den registrerede app. Du skal angive denne værdi for at aktivere Team-integration i Commerce Headquarters i næste afsnit.
1. Følg instruktionerne i [Tilføje en klienthemmelighed](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) for at tilføje en klienthemmelighed. Kopier derefter værdien af **Hemmelig værdi** for klienten. Du skal angive denne værdi for at aktivere Team-integration i Commerce Headquarters i næste afsnit.
1. Vælg **API-tilladelser**, og vælg derefter **Tilføje en tilladelse**.
1. Vælg **Microsoft Graph** i dialogboksen **Anmod om API-tilladelser**, vælg **Delegerede tilladelser**, udvid **Gruppe**, vælg **Group.ReadWrite.All**, og vælg derefter **Tilføj tilladelser**.
1. Vælg **Tilføj en tilladelse**, vælg **Microsoft Graph** i dialogboksen **Anmod om API-tilladelser**, vælg **Program tilladelser**, udvid **Gruppe**, vælg **Group.ReadWrite.All**, og vælg derefter **Tilføj tilladelser**.
1. Vælg **Tilføj en tilladelse** i dialogboksen **Anmod om API-tilladelser**. Søg under fanen **API'er, som min organisation bruger** efter **Microsoft Teams Detailtjeneste**, og vælg den.
1. Vælg **Delegerede tilladelser**, udvid **TaskPublishing**, vælg **TaskPublising.ReadWrite.All**, og vælg derefter **Tilføj tilladelser**. Yderligere oplysninger finder du i [Konfigurere et klientprogram til at få adgang til en web-API](/azure/active-directory/develop/quickstart-configure-app-access-web-apis).

Hvis du vil aktivere Teams-integration i Commerce Headquarters, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Konfiguration af Microsoft Teams-integration**.
1. Vælg **Rediger** i handlingsruden.
1. Angiv indstillingen **Aktivér Microsoft Teams-integration** til **Ja**.
1. I feltet **Program-id** skal du angive den værdi af **Applikations-id (klient)**, du fik, da du registrerede Teams-programmet på Azure-portalen.
1. I feltet **Programnøgle** skal du angive den **Hemmelig værdi**, du fik, da du tilføjede en klienthemmelighed på Azure-portalen.
1. Vælg **Gem** i handlingsruden.

I følgende illustration vises et eksempel på konfigurationen af Teams-integration i Commerce Headquarters.

![Konfiguration af Teams-integration i Commerce Headquarters.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Deaktivere Teams-integration

Hvis du vil deaktivere Microsoft Teams-integration i Commerce Headquarters, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Konfiguration af Microsoft Teams-integration**.
1. Vælg **Rediger** i handlingsruden.
3. Angiv indstillingen **Aktivér Microsoft Teams-integration** til **Nej**.
4. Ryd værdierne i felterne **Program-id** og **Programnøgle**.
1. Vælg **Gem** i handlingsruden.

> [!NOTE]
> Når du har deaktiveret Teams-integration med Commerce, viser POS-terminaler ikke længere opgaver, der er udgivet fra Teams-programmet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration](commerce-teams-integration.md)

[Klargøre Microsoft Teams fra Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Administrere brugerroller i Microsoft Teams](manage-user-roles-teams.md)

[Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams](map-stores-existing-teams.md)

[Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration](teams-integration-faq.md)
