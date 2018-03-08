---
title: Udvide funktionaliteten i Microsoft Dynamics 365 for Talent
description: Hvis du har oprettet Microsoft PowerApps, kan du starte disse programmer fra hyperlinks i Microsoft Dynamics 365 for Talent.
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
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
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cfd3b475b113fdab4ceeb3e636fea6c9134ab982
ms.openlocfilehash: 0ab829803634871c9060daa381bd02d7d2bbdf42
ms.contentlocale: da-dk
ms.lasthandoff: 12/01/2017

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a>Udvide funktionaliteten i Microsoft Dynamics 365 for Talent

[!include[banner](includes/banner.md)]

Hvis du har oprettet Microsoft PowerApps, kan du starte disse programmer fra hyperlinks i Microsoft Dynamics 365 for Talent. Når du vil oprette adgang til dine programmer, skal du angive nogle oplysninger i Talent på en konfigurationsside, som du kan åbne fra arbejdsområdet **Systemadministration**.

## <a name="configuring-embedded-powerapps-within-talent"></a>Konfiguration af integrerede PowerApps i Talent
Brug siden **Indstil integrerede Microsoft PowerApps** til at konfigurere Talent-sider for at starte PowerApps-programmer. Du kan åbne siden **Indstil integrerede Microsoft PowerApps** ved at åbne arbejdsområdet **Systemadministration** og derefter åbne fanen **Links**. Vælg **Microsoft PowerApps** i gruppen **Opsætning**. 

Følgende oplysninger angives eller indstilles på denne side: 

> - Et beskrivende navn eller id til hvert PowerApps-program.
> - Et entydigt id (GUID) for hvert program, du føjer til en Talent-side. Program-id'et findes på webstedet PowerApps-webstedet [powerapps.com](http://powerapps.com/). 
> - Den side, hvorfra brugere kan åbne et program eller en rapport. Ikke alle Talent-sider understøtter integrerede PowerApps og Power BI-rapporter. 

 > [!NOTE]
 >  Angiv det interne navn på siden i stedet for det viste navn, der vises øverst på siden. Du kan finde det interne navn ved at åbne den side, du skal bruge interne navn på, og højreklikke på et vilkårligt sted på siden. Når menuen åbnes, skal du pege på elementet **Oplysninger om formular**. Det interne formularnavn, der vises ud for elementet **Oplysninger om formular** i menuen.
 
> - Angiv det kontrolelement i formularen, som programmet kan hente kontekstdata fra. Et program kan for eksempel bruge data om en arbejder. Hvis du angiver siden **Arbejder** i feltet **Kontekst**, åbnes siden **Arbejder**, når du starter programmet. En post i **Kontekstfelt** er valgfri. 
> - Angiv størrelsen på den dialogboks, hvor PowerApps-programmet skal køre. Dialogboksene er angivet som "små" eller "store" for at optimere brugergrænsefladen, når programmet kører på henholdsvis en telefon eller en større enhed. 

Du kan også angive, hvilke juridiske enheder et program er tilgængeligt til, eller du kan gøre det tilgængeligt for alle juridiske enheder. PowerApps-programmerne er som standard tilgængelige for alle juridiske enheder.

## <a name="opening-an-application"></a>Åbning af et program
Når du har konfigureret integrerede PowerApps-programmer, føjes links til de programmer, du har angivet, til siderne i Talent. Klik på et link for at åbne et program. 



