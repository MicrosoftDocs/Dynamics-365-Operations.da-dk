---
title: Udvide Talent ved hjælp af PowerApps og Microsoft Flow - eksempelscenarier
description: Dette emne beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 for Talent ved hjælp af Microsoft PowerApps og Microsoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
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
ms.openlocfilehash: c113b0f4ab2c8e44d00fcfca3f0a6ca828a854ae
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517596"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a>Udvide Talent ved hjælp af PowerApps og Microsoft Flow - eksempelscenarier

Dette emne beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 for Talent ved hjælp af Microsoft PowerApps og Microsoft Flow. Du kan importere løsningspakken, der er tilknyttet hvert eksempel, til dit PowerApps-miljø. Du kan dernæst anvende pakkerne enten som vejledning eller som udgangspunktet for at implementere scenarier, der er anvendelige for din organisation.

> [!IMPORTANT]
> Såfremt du ønsker at anvende de i dette emne beskrevne skabeloner og appen "som de er", skal du afprøve dem for at sikre dig, at de omfatter alle de scenarier, der er specifikke for din implementering.


## <a name="prerequisites"></a>Forudsætninger

- For at importere pakker skal brugerne have rettigheden **Miljøoprettelse**.
- For at eksportere eller importere apps skal brugerne have en licens til en PowerApps Plan 2 eller en PowerApps Plan 2-prøveversion.

## <a name="flow--form-connect"></a>Proces – Tilknyt formular

Skabelonen **Proces – Tilknyt formular** kan anvendes til at læse data fra Microsoft-formularer og lagre det i en Common Data Service-enhed.

Denne skabelon kan udvides, således at den kan anvendes i andre scenarier. Her er nogle eksempler:

- Hent kandidatvurderinger.
- Hent resultater fra kursusspørgeskemaer.
- Kompiler et bibliotek med samtalespørgsmål til personaleansvarlige.
- Hent en kandidats vurdering af samtaleprocessen

I Microsoft Dynamics 365: Attract kan formularer fremgå af en kandidats portal, og kandidaterne kan udfylde detaljerne. Formularerne kan ligeledes indlejres som aktiviteter i en jobskabelon.

Når en kandidat indsender en formular, henter Microsoft Flow formularen, læser dataene og lagre den i Common Data Service-enheden.

Du kan downloade skabelonen **Proces – Tilknyt formular** og "Brugertilpasset enhedsstruktur" i Microsoft Download Center ved hjælp af følgende link: [Proces – Tilknyt formular](https://go.microsoft.com/fwlink/?linkid=2081988).

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a>Påbegyndelse og udtræk af de parametre, der er overført til PowerApps

Skabelonen **Påbegyndelse og udtræk af de parametre, der er overført til PowerApps** kan anvendes som udgangspunktet for alle PowerApps-scenarier, der er specifikke for Attract. Den omfatter alle standardparametre, som overføres fra Attract, såsom **Jobansøgning**, **Kandidat-id** og **Job-id**.

Denne skabelon kan anvendes til at hente en kandidats vurderingsformular, således at en ansættelsesansvarlig kan gennemgå den vurdering, kandidaten har udfyldt.

Apps, der udvikles ved hjælp af PowerApps, kan integreres i jobskabelonen i Attract.

Du kan downloade skabelonen **Påbegyndelse og udtræk af parametre, der overføres til PowerApps** og "Brugertilpasset enhedsstruktur" i Microsoft Download Center ved hjælp af følgende link: [Påbegyndelse og udtræk af parametre, der overføres til PowerApps](https://go.microsoft.com/fwlink/?linkid=2081991).

## <a name="integration-with-office-365"></a>Integration med Office 365

Appen **Integration med Office 365** kan anvendes til at udtrække teamoplysninger for brugere, der er logget på Microsoft Office 365. Den henviser arbejdere i Talent til at udtrække detaljer om arbejdsdagens start- og sluttidspunkt samt fortegnelser over undtagelser. Detaljer om arbejdsdagens start- og sluttidspunkt lagres i brugertilpassede Common Data Service-enheder. Det forudsættes, at disse detaljer udfyldes af tredjepartssystemer via integration.

Denne app kan udvides, således at den kan anvendes i andre scenarier. Den kan eksempelvis anvendes til at vise oplysninger om teamets ferie, kalenderhændelser og alle teamspecifikke hændelser.

Du kan downloade appen **Integration med Office 365** og "Brugertilpasset enhedsstruktur" i Microsoft Download Center ved hjælp af følgende link: [Integration med Office 365](https://go.microsoft.com/fwlink/?linkid=2081787).

## <a name="flow--email-notification"></a>Proces – E-mailbesked

Skabelonen **Proces – E-mailbesked** kan anvendes i scenarier omhandlende e-mailbeskeder. Den kan anvendes til at udløse e-mailbeskeder til kandidater vedrørende ansættelsesteamets afslag på alle stadier i rekrutteringsprocessen.

Denne skabelon kan udvides til at spore ændringer i kandidatstadiet i hele rekrutteringsprocessen og til at sende beskeder til ansættelsesteamet og kandidaten.

Der kan generelt set, for de enheder, som er lagret i Common Data Service, konfigureres processer til at sende beskeder vedrørende hændelser, der finder sted i Core HR, Attract eller Dynamics 365 Talent: Onboard.

Du kan downloade skabelonen **Proces – E-mailbesked** i Microsoft Download Center ved hjælp af følgende link: [Proces – E-mailbesked](https://go.microsoft.com/fwlink/?linkid=2082103).

## <a name="flow--sql-connect-and-execute"></a>Proces – Forbindelse til SQL og udførelse

Skabelonen **Proces – Forbindelse til SQL og udførelse** forbinder til Microsoft SQL Server og gør det muligt at køre SQL-forespørgsler.

Selv om denne skabelon er designet til at læse og opdatere SQL-tabeller, kan den udvides, således at den kan anvendes i andre scenarier. Den kan eksempelvis anvendes til at udfylde en stadieinddelt tabel i Common Data Service med poster fra SQL-serveren og til at synkronisere den stadieinddelte tabel periodisk ved hjælp af en trinvis overførelse fra SQL-serveren.

Du kan downloade skabelonen **Proces – Forbindelse til SQL og udførelse** i Microsoft Download Center ved hjælp af følgende link: [Proces – Forbindelse til SQL og udførelse](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="flow--sharepoint-integration"></a>Proces – SharePoint-integration

Skabelonen **Proces – SharePoint-integration** kan anvendes til at læse data fra en Microsoft SharePoint-liste, sammenligne listen med feltværdierne for alle Common Data Service-enheder og sende resultaterne af sammenligningen som en e-mailbesked. 

En organisation har muligvis akut mangel på et bestemt sæt færdigheder. Disse færdigheder kan lagres i SharePoint som en SharePoint-liste. Når en kandidat søger et hvilket som helst job, som indeholder det sæt færdigheder, der er anført på listen, fremsendes en e-mailbesked, såfremt der er væsentligt sammenfald mellem kandidatens færdigheder og de færdigheder, der er lagret i SharePoint. Derved kan stillinger, hvor der er akut behov for ansættelse, hurtigere besættes, da beskeden hjælper rekrutteringsmedarbejdere med at indlede kontakten og ansætte kandidater på tværs af hele organisationen.

Denne skabelon kan udvides, så den kan anvendes i alle scenarier, der omfatter SharePoint-integration.

Du kan downloade skabelonen **Proces – SharePoint-integration** i Microsoft Download Center ved hjælp af følgende link: [Proces – SharePoint-integration](https://go.microsoft.com/fwlink/?linkid=2082109).

## <a name="admin-console-to-manage-talent-pools"></a>Administrationskonsol til styring af talentpuljer

Når du aktiverer integration med LinkedIn, opretter Attract automatisk en LinkedIn-talentgruppe. Når en rekrutteringsmedarbejder udveksler InMail med en rekrutteret via LinkedIn, opretter Attract en profil til den rekrutterede person, og vedkommende bliver medlem af LinkedIn-talentpuljen. Denne PowerApps-app er nyttig til reorganisering af kandidater i talentpuljer baseret på færdigheder.

Kør denne PowerApps-app som en administratorkonsol for at udføre følgende opgaver:

- Angive kandidater i en talentpulje
- Føje kandidater til og fjerne kandidater fra en talentpulje
- Flytte kandidater fra én talentpulje til en anden
- Afklare, om kandidater allerede er en del af en talentpulje, før de flyttes
- Kontrollere kandidaternes færdigheder, før du flytter dem til andre talentpuljer

Denne PowerApps-app bruger mange-til-mange-relationer, så du kan bruge den som skabelon for andre scenarier, hvor du skal uddrage poster, der har mange-til-mange-relationer.

Du kan hente skabelonen **Administrationskonsol til styring af talentpuljer** ved at gå til [Administrationskonsol til styring af talentpuljer](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) i Microsoft Download Center.

## <a name="additional-resources"></a>Yderligere ressourcer

[Klientens Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Overfør app mellem lejere og miljøer](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
