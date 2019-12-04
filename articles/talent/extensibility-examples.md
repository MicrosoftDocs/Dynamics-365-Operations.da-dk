---
title: Udvid Talent med Power Apps og Power Automate
description: Dette emne beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 Talent ved hjælp af Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 3bb61297e294aa3f2d06f542bebe29d7afae9c3b
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832832"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Udvid Talent med Power Apps og Power Automate

[!include [banner](includes/banner.md)]

Dette emne beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 Talent ved hjælp af Microsoft Power Apps og Microsoft Power Automate. Du kan importere løsningspakken, der er tilknyttet hvert eksempel, til dit Power Apps-miljø. Du kan dernæst anvende pakkerne enten som vejledning eller som udgangspunktet for at implementere scenarier, der er anvendelige for din organisation.

> [!IMPORTANT]
> Såfremt du ønsker at anvende de i dette emne beskrevne skabeloner og appen "som de er", skal du afprøve dem for at sikre dig, at de omfatter alle de scenarier, der er specifikke for din implementering.


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

I Microsoft Dynamics 365: Attract kan formularer fremgå af en kandidats portal, og kandidaterne kan udfylde detaljerne. Formularerne kan ligeledes indlejres som aktiviteter i en jobskabelon.

Når en kandidat indsender en formular, henter Microsoft Power Automate formularen, læser dataene og lagre den i Common Data Service-enheden.

Du kan downloade skabelonen **Power Automate – Tilknyt formular** og Brugertilpasset enhedsstruktur i [Power Automate – Tilknyt formular](https://go.microsoft.com/fwlink/?linkid=2081988) i Microsoft Download Center.

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a>Påbegyndelse og udtræk af de parametre, der er overført til Power Apps

Skabelonen **Påbegyndelse og udtræk af de parametre, der er overført til Power Apps** kan anvendes som udgangspunktet for alle Power Apps-scenarier, der er specifikke for Attract. Den omfatter alle standardparametre, som overføres fra Attract, såsom **Jobansøgning**, **Kandidat-id** og **Job-id**.

Denne skabelon kan anvendes til at hente en kandidats vurderingsformular, således at en ansættelsesansvarlig kan gennemgå den vurdering, kandidaten har udfyldt.

Apps, der er oprettet ved hjælp af Power Apps, kan integreres i jobskabelonen i Attract.

Du kan downloade skabelonen **Påbegyndelse og udtræk af parametre, der overføres til Power Apps** under [Påbegyndelse og udtræk af parametre, der overføres til Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) i Microsoft Download Center.

## <a name="integration-with-office-365"></a>Integration med Office 365

Appen **Integration med Office 365** kan anvendes til at udtrække teamoplysninger for brugere, der er logget på Microsoft Office 365. Den henviser arbejdere i Talent til at udtrække detaljer om arbejdsdagens start- og sluttidspunkt samt fortegnelser over undtagelser. Detaljer om arbejdsdagens start- og sluttidspunkt lagres i brugertilpassede Common Data Service-enheder. Det forudsættes, at disse detaljer udfyldes af tredjepartssystemer via integration.

Denne app kan udvides, således at den kan anvendes i andre scenarier. Den kan eksempelvis anvendes til at vise oplysninger om teamets ferie, kalenderhændelser og alle teamspecifikke hændelser.

Du kan downloade appen **Integration med Office 365** og "Brugertilpasset enhedsstruktur" i Microsoft Download Center ved hjælp af følgende link: [Integration med Office 365](https://go.microsoft.com/fwlink/?linkid=2081787).

## <a name="power-automate--email-notification"></a>Power Automate – E-mailbesked

Skabelonen **Power Automate– E-mailbesked** kan anvendes i scenarier omhandlende e-mailbeskeder. Den kan anvendes til at udløse e-mailbeskeder til kandidater vedrørende ansættelsesteamets afslag på alle stadier i rekrutteringsprocessen.

Denne skabelon kan udvides til at spore ændringer i kandidatstadiet i hele rekrutteringsprocessen og til at sende beskeder til ansættelsesteamet og kandidaten.

Der kan generelt set, for de enheder, som er lagret i Common Data Service, konfigureres processer til at sende beskeder vedrørende hændelser, der finder sted i Core HR, Attract eller Onboard.

Du kan downloade skabelonen **Power Automate – E-mailbesked** i Microsoft Download Center ved hjælp af følgende link: [Power Automate – E-mailbesked](https://go.microsoft.com/fwlink/?linkid=2082103).

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – Forbindelse til SQL og udførelse

Skabelonen **Power Automate – Forbindelse til SQL og udførelse** forbinder til Microsoft SQL Server og gør det muligt at køre SQL-forespørgsler.

Selv om denne skabelon er designet til at læse og opdatere SQL-tabeller, kan den udvides, således at den kan anvendes i andre scenarier. Den kan eksempelvis anvendes til at udfylde en stadieinddelt tabel i Common Data Service med poster fra SQL-serveren og til at synkronisere den stadieinddelte tabel periodisk ved hjælp af en trinvis overførelse fra SQL-serveren.

Du kan downloade skabelonen **Power Automate – Forbindelse til SQL og udførelse** i Microsoft Download Center ved hjælp af følgende link: [Power Automate – Forbindelse til SQL og udførelse](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePoint-integration

Skabelonen **Power Automate – SharePoint-integration** kan anvendes til at læse data fra en Microsoft SharePoint-liste, sammenligne listen med feltværdierne for alle Common Data Service-enheder og sende resultaterne af sammenligningen som en e-mailbesked. 

En organisation har muligvis akut mangel på et bestemt sæt færdigheder. Disse færdigheder kan lagres i SharePoint som en SharePoint-liste. Når en kandidat søger et hvilket som helst job, som indeholder det sæt færdigheder, der er anført på listen, fremsendes en e-mailbesked, såfremt der er væsentligt sammenfald mellem kandidatens færdigheder og de færdigheder, der er lagret i SharePoint. Derved kan stillinger, hvor der er akut behov for ansættelse, hurtigere besættes, da beskeden hjælper rekrutteringsmedarbejdere med at indlede kontakten og ansætte kandidater på tværs af hele organisationen.

Denne skabelon kan udvides, så den kan anvendes i alle scenarier, der omfatter SharePoint-integration.

Du kan downloade skabelonen **Power Automate – SharePoint-integration** i Microsoft Download Center ved hjælp af følgende link: [Power Automate – SharePoint-integration](https://go.microsoft.com/fwlink/?linkid=2082109).

## <a name="referral-app"></a>Appen Henvisning
Du kan bruge appen Henvisning til at føje kandidater til en delt talentpulje. Den, der henviser, kan angive **Fornavn**, **Efternavn**, **Mail** og **URL-adresse til LinkedIn** ved indsendelse af en kandidat. Metadata til kandidatkilden udfyldes derefter med oplysningerne fra den, der henviser.

Du kan integrere denne app i Medarbejderselvbetjening (ESS) for at sende henvisninger, eller du kan bruge den som et link i firmaportalen og køre den som en fritstående app.

Du kan downloade **appen Henvisning** ved at gå til [Dynamics 365 Talent-udvidelsesløsning: appen Henvisning](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) i Microsoft Download Center. Du kan importere denne app og tilpasse den for at tilføje yderligere funktioner.

## <a name="additional-resources"></a>Yderligere ressourcer

[Klientens Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Overfør app mellem lejere og miljøer](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
