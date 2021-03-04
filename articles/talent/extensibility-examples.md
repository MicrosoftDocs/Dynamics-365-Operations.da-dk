---
title: Udvide Talent med Power Apps og Power Automate
description: Denne artikel beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 Talent - Attract ved hjælp af Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529628"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Udvide Talent med Power Apps og Power Automate

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Denne artikel beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 Talent: Attract ved hjælp af Microsoft Power Apps og Microsoft Power Automate. Du kan importere løsningspakken, der er tilknyttet hvert eksempel, til dit Power Apps-miljø. Du kan dernæst anvende pakkerne enten som vejledning eller som udgangspunktet for at implementere scenarier, der er anvendelige for din organisation.

> [!IMPORTANT]
> Såfremt du ønsker at anvende de i denne artikel beskrevne skabeloner og appen "som de er", skal du afprøve dem for at sikre dig, at de omfatter alle de scenarier, der er specifikke for din implementering.


## <a name="prerequisites"></a>Forudsætninger

- For at importere pakker skal brugerne have rettigheden **Miljøoprettelse**.
- For at eksportere eller importere apps skal brugerne have en licens til en Power Apps Plan 2 eller en Power Apps Plan 2-prøveversion.

## <a name="power-automate--form-connect"></a>Power Automate – Tilknyt formular

Skabelonen **Power Automate – Tilknyt formular** kan anvendes til at læse data fra Microsoft Forms og lagre dem i en Common Data Service-enhed.

Denne skabelon kan udvides, således at den kan anvendes i andre scenarier. Her er nogle eksempler:

- Hent kandidatvurderinger.
- Hent resultater fra kursusspørgeskemaer.
- Kompiler et bibliotek med samtalespørgsmål til personaleansvarlige.
- Hent en kandidats vurdering af samtaleprocessen

I Microsoft Dynamics 365: Attract, du kan bruge formularer i kandidatportalen, hvor kandidaterne udfylder detaljerne. Du kan ligeledes integrere formularer som aktiviteter i en jobskabelon.

Når en kandidat indsender en formular, henter Microsoft Power Automate formularen, læser dataene og lagre den i Common Data Service-enheden.

Du kan downloade skabelonen **Power Automate – Tilknyt formular** og Brugertilpasset enhedsstruktur i [Power Automate – Tilknyt formular](https://go.microsoft.com/fwlink/?linkid=2081988) i Microsoft Download Center.

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePoint-integration

Skabelonen **Power Automate – SharePoint-integration** kan anvendes til at læse data fra en Microsoft SharePoint-liste, sammenligne listen med feltværdierne for alle Common Data Service-enheder og sende resultaterne af sammenligningen som en e-mailbesked. 

En organisation har muligvis akut mangel på et bestemt sæt færdigheder. Disse færdigheder kan lagres i SharePoint som en SharePoint-liste. Når en kandidat søger et hvilket som helst job, som indeholder det sæt færdigheder, der er anført på listen, fremsendes en e-mailbesked, såfremt der er væsentligt sammenfald mellem kandidatens færdigheder og de færdigheder, der er lagret i SharePoint. På den måde kan stillinger, hvor der er akut behov for ansættelse, hurtigere besættes, da beskeden hjælper rekrutteringsmedarbejdere med at ansætte kandidater på tværs af hele organisationen.

Denne skabelon kan udvides, så den kan anvendes i alle scenarier, der omfatter SharePoint-integration.

Du kan downloade skabelonen **Power Automate – SharePoint-integration** i Microsoft Download Center ved hjælp af følgende link: [Power Automate – SharePoint-integration](https://go.microsoft.com/fwlink/?linkid=2082109).

## <a name="referral-app"></a>Appen Henvisning

Du kan bruge appen Henvisning til at føje kandidater til en delt talentpulje. Den, der henviser, kan angive **Fornavn**, **Efternavn**, **Mail** og **URL-adresse til LinkedIn** ved indsendelse af en kandidat. Metadata til kandidatkilden udfyldes derefter med oplysningerne fra den, der henviser.

Du kan integrere denne app i Medarbejderselvbetjening (ESS) for at sende henvisninger, eller du kan bruge den som et link i firmaportalen og køre den som en enkeltstående app.

Du kan downloade **appen Henvisning** ved at gå til [Dynamics 365 Talent-udvidelsesløsning: appen Henvisning](https://www.microsoft.com/download/details.aspx?id=58497) i Microsoft Download Center. Du kan importere denne app og tilpasse den for at tilføje yderligere funktioner.

## <a name="additional-resources"></a>Yderligere ressourcer

[Klientens Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[Overfør app mellem lejere og miljøer](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)


[!INCLUDE[footer-include](../includes/footer-banner.md)]