---
title: "Fjerne et Talent-miljø"
description: "Dette emne fører dig gennem processen med at fjerne et testdrev eller et produktionsmiljø til Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d1870c84d4d5e7402bae44d192ce7587c2f67fe7
ms.openlocfilehash: 0e7748b079b1cd5c069917d46e05cd281ea6aa01
ms.contentlocale: da-dk
ms.lasthandoff: 04/05/2018

---
# <a name="remove-a-talent-environment"></a>Fjerne et Talent-miljø

Dette emne fører dig gennem processen med at fjerne et testdrev eller et produktionsmiljø til Microsoft Dynamics 365 for Talent.

## <a name="removing-a-test-drive-environment"></a>Fjerne et testdrevmiljø

Testdrev til Talent er klargjort med en 60-dages udløbspolitik. Men ejere af testdrevmiljøer har dog mulighed for at afslutte deres forsøg tidligere ved at følge disse trin. 

1. Naviger til [PowerApps Administration](https://admin.businessplatform.microsoft.com/).
2. Vælg **Miljøer**.
3. Vælg det testdrevmiljø, som har et navngivningsmønster som dette: TestDrive - alias@domain
4. Vælg **Slet**, og bekræft beslutningen. 

Det eksisterende testdrevmiljø fjernes. Når det er fjernet, kan du tilmelde dig til et nyt testdrevmiljø. 

## <a name="removing-a-production-environment"></a>Fjerne et produktionsmiljø

Det antages i emnet, at du har købt Talent via en Cloud Solution Provider (CSP) eller en EA-aftale (Enterprise Architecture). 

Da der er "indeholdt" et enkelt Talent-miljø i hver enkelt PowerApps-miljø, er der to indstillinger, der skal overvejes. Den første indstilling omfatter fjernelse af hele PowerApps-miljøet, den anden mulighed omfatter kun fjernelse af Talent. Den første indstilling foretrækkes, når du har oprettet et PowerApps-miljø udtrykkeligt med henblik på klargøring af Talent, og du kun lige er begyndt implementeringen, eller du ikke har nogen etablerede integrationer. Den anden mulighed er kun relevant, når du har et etableret PowerApps-miljø, der er udfyldt med omfattende data, som udnyttes i PowerApps og processer.

> [!Important]
> Før du fjerner PowerApps-miljøet, skal du sikre dig, at det ikke bruges til omfattende dataintegrationer, som ikke er omfattet af Talent. Bemærk også, at PowerApps-standardmiljøerne ikke kan fjernes. 

Sådan fjernes hele PowerApps-miljøet, herunder Talent og de tilknyttede apps og processer:

1. Naviger til [PowerApps Administration](https://admin.businessplatform.microsoft.com/).
2. Vælg **Miljøer**.
3. Vælg det miljø, der skal fjernes.
4. Vælg **Slet**, og bekræft beslutningen. 
5. Vent, indtil sletningen er fuldført.
6. Log på [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) ved hjælp af den konto, som du brugte til dit abonnement på Talent. 
7. Vælg det Talent-projekt, der indeholder miljøet. 
8. I LCS-projektet skal du vælge feltet **Administration af Talent-app**. 
9. Marker den forekomst, du vil fjerne. 
10. Vælg **Fjern forekomst**, og bekræft sletningen.  

Hvis du vil fjerne et Talent-miljø fra et eksisterende PowerApps-miljø, skal du benytte følgende fremgangsmåde. Bemærk, at behovet for at involvere support og kontakte Talent DevOps-teamet er midlertidig, indtil denne funktion er aktiveret direkte i LCS.

1. Kontakt Support for at starte en anmodning til fjernelse.
2. Support-teamet igangsætter en anmodning om fjernelse hos Talent DevOps-teamet. 
3. Fortsæt, når du får besked om, at miljøet er fjernet.
4.  Log på LCS ved hjælp af den konto, som du brugte til dit abonnement på Talent. 
5. Vælg det Talent-projekt, der indeholder miljøet. 
6. I LCS-projektet skal du vælge feltet **Administration af Talent-app**. 
7. Vælg den forekomst, du vil fjerne, som skal mærkes med installationsstatussen **Mislykket**.
8. Vælg **Fjern forekomst**, og bekræft sletningen. 


