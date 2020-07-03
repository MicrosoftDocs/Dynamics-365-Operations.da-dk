---
title: Fjern en forekomst
description: Denne arikel fører dig gennem processen med at fjerne et testdrev eller produktionsmiljø til Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17f299f81d1326dfb06c11a6125acc54b8ef2a6e
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431193"
---
# <a name="remove-an-instance"></a>Fjern en forekomst

Denne arikel fører dig gennem processen med at fjerne et testdrev eller produktionsmiljø til Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Fjerne et testdrevmiljø

Testdrev til Personale er klargjort med en 60-dages udløbspolitik. Men ejere af testdrevmiljøer har dog mulighed for at afslutte deres forsøg tidligere ved at følge disse trin. 

1. Naviger til [Power Apps Administration](https://admin.businessplatform.microsoft.com/).
2. Vælg **Miljøer**.
3. Vælg det testdrevmiljø, som har et navngivningsmønster som dette: TestDrive - alias@domain
4. Vælg **Slet**, og bekræft beslutningen. 

Det eksisterende testdrevmiljø fjernes. Når det er fjernet, kan du tilmelde dig til et nyt testdrevmiljø. 

## <a name="remove-a-production-environment"></a>Fjerne et produktionsmiljø

Det antages i artiklen, at du har købt Personale via en Cloud Solution Provider (CSP) eller en EA-aftale (Enterprise Architecture). 

Da der er indeholdt et enkelt Personale-miljø i hvert enkelt Power Apps-miljø, er der to indstillinger, der skal overvejes. Den første indstilling omfatter fjernelse af hele Power Apps-miljøet, den anden mulighed omfatter kun fjernelse af Personale. Den første indstilling foretrækkes, når du har oprettet et Power Apps-miljø udtrykkeligt med henblik på klargøring af Personale, og du kun lige er begyndt implementeringen, eller du ikke har nogen etablerede integrationer. Den anden mulighed er kun relevant, når du har et etableret Power Apps-miljø, der er udfyldt med omfattende data, som udnyttes i Power Apps og Power Automate.

> [!Important]
> Før du fjerner Power Apps-miljøet, skal du sikre dig, at det ikke bruges til omfattende dataintegrationer, som ikke er omfattet af Personale. Bemærk også, at Power Apps-standardmiljøerne ikke kan fjernes. 

Sådan fjernes hele Power Apps-miljøet, herunder Personale og de tilknyttede apps og flows:

1. Naviger til [Power Apps Administration](https://admin.businessplatform.microsoft.com/).
2. Vælg **Miljøer**.
3. Vælg det miljø, der skal fjernes.
4. Vælg **Slet**, og bekræft beslutningen. 
5. Vent, indtil sletningen er fuldført.
6. Log på [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) ved hjælp af den konto, som du brugte til dit abonnement på Personale. 
7. Vælg det Personale-projekt, der indeholder miljøet. 
8. I LCS-projektet skal du vælge feltet **Administration af Personale-app**. 
9. Marker den forekomst, du vil fjerne. 
10. Vælg **Fjern forekomst**, og bekræft sletningen.  

Hvis du vil fjerne et Personale-miljø fra et eksisterende Power Apps-miljø, skal du benytte følgende fremgangsmåde. Bemærk, at behovet for at involvere support og kontakte Personale DevOps-teamet er midlertidig, indtil denne funktion er aktiveret direkte i LCS.

1. Kontakt Support for at starte en anmodning til fjernelse.
2. Support-teamet igangsætter en anmodning om fjernelse hos Personale DevOps-teamet. 
3. Fortsæt, når du får besked om, at miljøet er fjernet.
4.  Log på LCS ved hjælp af den konto, som du brugte til dit abonnement på Personale. 
5. Vælg det Personale-projekt, der indeholder miljøet. 
6. I LCS-projektet skal du vælge feltet **Administration af Personale-app**. 
7. Vælg den forekomst, du vil fjerne, som skal mærkes med installationsstatussen **Mislykket**.
8. Vælg **Fjern forekomst**, og bekræft sletningen. 
