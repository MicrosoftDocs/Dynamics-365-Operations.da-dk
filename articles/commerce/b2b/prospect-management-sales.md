---
title: Administrere forretningspartnerbrugere på B2B-e-handelswebsteder ved hjælp af Dynamics 365 Sales
description: Dette emne beskriver, hvordan du bruger Microsoft Dynamics 365 Sales til at administrere godkendelser af forretningspartnere for Dynamics 365 Commerce business-to-business-handelswebsteder (B2B).
author: shajain
ms.date: 2/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 540e8f26d7f2a08060a3839f9e4f97bf8ddcafac
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692557"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>Administrere forretningspartnerbrugere på B2B-e-handelswebsteder ved hjælp af Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du bruger Microsoft Dynamics 365 Sales til at administrere godkendelser af forretningspartnere for Dynamics 365 Commerce business-to-business-handelswebsteder (B2B). Organisationer, der allerede har købt Dynamics 365 Sales-løsningen, kan bruge de potentielle kunde- og salgsmulighedsbegreber til godkendelsesprocessen for B2B-e-handelsforretningspartner.

Du kan finde baggrundsoplysninger om godkendelsesprocessen for B2B-forretningspartnere i [Administrere forretningspartnerbrugere på B2B-e-handelswebsteder](manage-b2b-users.md).

Potentielle forretningspartnere kan igangsætte onboardingprocessen på et B2B-e-handelswebsted ved at sende en anmodning om onboarding via et link til B2B-webstedet. Når anmodningen er sendt, og de relevante job (f.eks. **P-0001** og **Synkroniser ordrer og kanalanmodninger**) køres i Commerce-hovedkontoret, gemmes anmodningen om onboarding på siden **Alle kundeemner** i Commerce-hovedkontoret. Godkendelsesprocessen for forretningspartnerens kundeemne kan derefter fuldføres i Salg.

Når integration mellem Sales og Commerce er aktiveret, vil oprettelsen af et kundeemne for forretningspartneren i Commerce forårsage oprettelsen af et *kundeemne* i Sales.

I følgende illustration vises et eksempel på en side til oprettelse af kundeemner for et kundeemne hos en forretningspartner i Sales.

![Siden til oprettelse af kundeemne i Dynamics 365 Sales.](../media/LeadInSales.png)

I illustrationen viser afsnittet **Kontakt** den person, der sendte anmodningen om onboarding, og afsnittet **Firma** viser organisationen. En note i afsnittet **Tidslinje** angiver, at kundeemnet blev genereret af infrastrukturen for dobbeltskrivning. Da den er oprettet af infrastrukturen til dobbeltskrivning, vises dette kundeemne ikke på rullelisten **Mine åbne kundeemner**. Den vises i stedet under en ny visning med navnet **Alle B2B-kundeemner til handel**.

Pr. standardproces for kvalificering af kundeemne i Sales, når en bruger "kvalificerer" kundeemnet, oprettes der en *salgsmulighed*-post, en *kontakt*-post og en *konto*-post. Infrastrukturen til dobbeltskrivning bruges til at skrive kontakt- og kontoposterne til Commerce. Kontakten oprettes som en kunde af typen *Person*, og firmaet oprettes som en kunde af typen *organisation*. Hvis en bruger vælger **Luk som vundet** for salgsmuligheden, godkendes kundeemnet i Commerce. Godkendelsen af et kundeemne bevirker, at der oprettes et kundehierarki.

Alle resterende forretningsprocesser forekommer i Commerce. Disse processer omfatter afsendelse af mails til forretningspartneren, definition af administration af kreditmaksimum for brugerne og tilføjelse af flere brugere til B2B-webstedet. Hvis en bruger diskvalificerer kundeemnet eller markerer salgsmuligheden som tabt i stedet for at kvalificere kundeemnet, markeres kundeemnet i Commerce som afvist, og der sendes en afvisende onboardingmail til anmoderen.

## <a name="enable-integration-between-sales-and-commerce"></a>Aktivere integration mellem Sales og Commerce

Integration mellem Sales og Commerce er afhængig af infrastrukturen for dobbeltskrivning. Derfor skal dobbeltskrivning aktiveres og fungere for at få kunder, der oprettes i ét system, skrevet til det andet system. Du kan finde flere oplysninger om infrastrukturen til dobbeltskrivning i [Oversigt over dobbeltskrivning](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview).

Når konfigurationen af dobbeltskrivning er fuldført, kan implementeringspartneren gå til [Microsoft AppSource](https://appsource.microsoft.com/) og søge efter den løsning, der hedder [Commerce-dobbeltskrivningsløsninger](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview). Installer pakken ved hjælp af guiden Standardinstallation, og test den derefter ved at oprette et kundeemne på et B2B-websted. Når kundeemnet er oprettet, skal du kontrollere, at anmodningen vises i **Alle kundeemner** i Commerce, og kontrollér derefter, at kundeemnet vises som et emne i Sales.

## <a name="additional-resources"></a>Yderligere ressourcer

[Administrere forretningspartnerbrugere på B2B-e-handelswebsteder](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
