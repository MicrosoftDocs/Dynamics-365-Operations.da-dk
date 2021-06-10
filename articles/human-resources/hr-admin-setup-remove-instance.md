---
title: Fjern en forekomst
description: Denne arikel fører dig gennem processen med at fjerne et testdrev eller produktionsmiljø til Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72a5b99150e5ccdf9a542b569c94c64cb95923fd
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053605"
---
# <a name="remove-an-instance"></a>Fjern en forekomst

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne arikel fører dig gennem processen med at fjerne et testdrev eller produktionsmiljø til Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Fjerne et testdrevmiljø

Testdrev til Human Resources er klargjort med en 60-dages udløbspolitik. Men ejere af testdrevmiljøer har dog mulighed for at afslutte deres forsøg tidligere ved at følge disse trin. 

1. Naviger til [Power Apps Administration](https://admin.businessplatform.microsoft.com/).
2. Vælg **Miljøer**.
3. Vælg det testdrevmiljø, som har et navngivningsmønster som dette: TestDrive - alias@domain
4. Vælg **Slet**, og bekræft beslutningen. 

Det eksisterende testdrevmiljø fjernes. Når det er fjernet, kan du tilmelde dig til et nyt testdrevmiljø. 

## <a name="remove-a-production-environment"></a>Fjerne et produktionsmiljø

Det antages i artiklen, at du har købt Human Resources via en Cloud Solution Provider (CSP) eller en EA-aftale (Enterprise Architecture). 

Da der er indeholdt et enkelt Human Resources-miljø i hvert enkelt Power Apps-miljø, er der to indstillinger, der skal overvejes. Den første indstilling omfatter fjernelse af hele Power Apps-miljøet, den anden mulighed omfatter kun fjernelse af Human Resources. Den første indstilling foretrækkes, når du har oprettet et Power Apps-miljø udtrykkeligt med henblik på klargøring af Human Resources, og du kun lige er begyndt implementeringen, eller du ikke har nogen etablerede integrationer. Den anden mulighed er kun relevant, når du har et etableret Power Apps-miljø, der er udfyldt med omfattende data, som udnyttes i Power Apps og Power Automate.

> [!Important]
> Før du fjerner Power Apps-miljøet, skal du sikre dig, at det ikke bruges til omfattende dataintegrationer, som ikke er omfattet af Human Resources. Bemærk også, at Power Apps-standardmiljøerne ikke kan fjernes. 

Sådan fjernes hele Power Apps-miljøet, herunder Human Resources og de tilknyttede apps og flows:

1. Naviger til [Power Apps Administration](https://admin.businessplatform.microsoft.com/).
2. Vælg **Miljøer**.
3. Vælg det miljø, der skal fjernes.
4. Vælg **Slet**, og bekræft beslutningen. 
5. Vent, indtil sletningen er fuldført.
6. Log på [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) ved hjælp af den konto, som du brugte til dit abonnement på Human Resources. 
7. Vælg det Human Resources-projekt, der indeholder miljøet. 
8. I LCS-projektet skal du vælge feltet **Administration af Human Resources-app**. 
9. Marker den forekomst, du vil fjerne. 
10. Vælg **Fjern forekomst**, og bekræft sletningen.  

Hvis du vil fjerne et Human Resources-miljø fra et eksisterende Power Apps-miljø, skal du benytte følgende fremgangsmåde. Bemærk, at behovet for at involvere support og kontakte Human Resources DevOps-teamet er midlertidig, indtil denne funktion er aktiveret direkte i LCS.

1. Kontakt Support for at starte en anmodning til fjernelse.
2. Support-teamet igangsætter en anmodning om fjernelse hos Human Resources DevOps-teamet. 
3. Fortsæt, når du får besked om, at miljøet er fjernet.
4. Log på LCS ved hjælp af den konto, som du brugte til dit abonnement på Human Resources. 
5. Vælg det Human Resources-projekt, der indeholder miljøet. 
6. I LCS-projektet skal du vælge feltet **Administration af Human Resources-app**. 
7. Vælg den forekomst, du vil fjerne, som skal mærkes med installationsstatussen **Slettet**.
8. Vælg **Fjern forekomst**, og bekræft sletningen. 

## <a name="recover-a-soft-deleted-environment"></a>Gendanne et ikke-permanent slettet miljø

Hvis du sletter det Power Apps-miljø, som personalemiljøet er forbundet med, vil status for personalemiljøet i tjenesten Lifecycle Services være **Ikke-permanent slettet**. I dette tilfælde kan brugere ikke oprette forbindelse til personale.

Sådan gendannes miljøet:

1. Følg vejledningen i [Gendanne Power Apps-miljøet](/power-platform/admin/recover-environment.md).

2. Kontakt support for at gendanne personalemiljøet. Du kan finde flere oplysninger under [Få support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> Power Apps-miljøer gemmes kun i syv dage efter sletning. Du skal gendanne miljøet inden for perioden på syv dage.


[!INCLUDE[footer-include](../includes/footer-banner.md)]