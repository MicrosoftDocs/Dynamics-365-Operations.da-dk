---
title: Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration
description: Dette emne beskriver, hvordan du aktiverer Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eb0b8b419b302fbd0bc107bca22f8b26774ba3c7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019829"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du aktiverer Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.

Hvis du vil klargøre Teams med oplysninger fra Dynamics 365 Commerce og synkronisere funktionerne til opgavestyring mellem Teams og POS-programmet (POS), skal du aktivere integrationsfunktionerne i Commerce-hovedkontoret.

> [!NOTE]
> Når du aktiverer integration med Teams, giver du dit samtykke til at dele dine data med Teams. Data, der deles med Teams, kan være i et andet land end dine Commerce-data, og de kan være underlagt forskellige overholdelser af angivne standarder. Der er flere oplysninger i [Microsofts Sikkerhedscenter](https://www.microsoft.com/trust-center). Du kan finde oplysninger om Microsofts politikker for beskyttelse af personlige oplysninger i [Microsofts erklæring om beskyttelse af personlige oplysninger](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Aktivere Teams-integration

Før du kan aktivere Microsoft Teams-integration med Commerce, skal du registrere Teams-programmet hos din lejer på Azure-portalen.

Du kan registrere Teams-programmet hos din lejer på Azure-portalen ved at følge disse trin.

1. Følg trinnene i [Hurtig start: Registrer en app på Microsofts id-platform](/azure/active-directory/develop/quickstart-register-app) for at registrere Teams-programmet hos din lejer på Azure-portalen.
1. Kopiér værdien af **Program-id (klient)** fra siden **Oversigt** for den registrerede app. Du skal bruge denne værdi til at aktivere Team-integration i Commerce-hovedkontoret.
1. Kopiér den certifikatværdi, der blev angivet, da du [tilføjede et certifikat](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) i trin 1. Certifikatet kaldes også den offentlige nøgle eller programnøglen. Du skal bruge denne værdi til at aktivere Team-integration i Commerce-hovedkontoret.

Hvis du vil aktivere Teams-integration i Commerce-hovedkontoret, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Konfiguration af Microsoft Teams-integration**.
1. Vælg **Rediger** i handlingsruden.
1. Angiv indstillingen **Aktivér Microsoft Teams-integration** til **Ja**.
1. I felterne **Program-id** og **Programnøgle** skal du angive de værdier, du fik, da du registrerede Teams-programmet på Azure-portalen.
1. Vælg **Gem** i handlingsruden.

I følgende illustration vises et eksempel på konfigurationen af Teams-integration i Commerce-hovedkontoret.

![Konfiguration af Teams-integration i Commerce-hovedkontoret](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Deaktivere Teams-integration

Hvis du vil deaktivere Microsoft Teams-integration i Commerce-hovedkontoret, skal du følge disse trin.

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