---
title: Installere tilføjelsesprogrammet til mikroservices i Lifecycle Services
description: Denne artikel forklarer, hvordan du kan installere tilføjelsesprogrammet Elektronisk fakturering i Microsoft Dynamics Lifecycle Services (LCS).
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 938b00192acc0ff5534239f2f280792471181fad
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710802"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Installere tilføjelsesprogrammet til mikroservices i Lifecycle Services

[!include [banner](../includes/banner.md)]

Godkendelse i tjenesten Elektronisk fakturering kræver, at du registrerer dit Microsoft Dynamics 365 Finance- eller Dynamics 365 Supply Chain Management-miljø på tjenesteplatformen ved at installere tilføjelsesprogrammet til dit miljø i Microsoft Dynamics Lifecycle Services (LCS).

Følg disse trin for at registrere et miljø.

1. Log på din LCS-konto.
2. Vælg et LCS-projekt på projektdashboardet.
2. I projektet skal du vælge dit implementeringsmiljø på **Miljøer**-dashboardet. Det miljø, du vælger, skal køre.
3. Under fanen **Power Platform Integration** i sektionen **Tilføjelsesprogrammer for miljø** skal du vælge **Installer et nyt tilføjelsesprogram**.
4. Vælg **Elektronisk fakturering**.
5. I feltet **AAD-program-id** skal du angive den faste værdi **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Denne værdi er altid fastlagt. Sørg for kun at angive en Globally Unique Identifier (GUID). Medtag ikke andre symboler, f.eks. mellemrum, kommaer, punktummer eller anførselstegn.
6. Angiv lejer-id for din Azure-abonnementskonto i feltet **AAD-lejer-id**. Den Azure Active Directory (Azure AD) lejer, du angiver, skal være den samme lejer, som bruges til Regulatory Configuration Service (RCS).
7. Gennemse vilkår og betingelser, og markér derefter afkrydsningsfeltet.
8. Vælg **Installer**. Efter nogle få minutter skal status ændres fra **Installerer** til **Installeret**. Du skal måske opdatere siden for at se denne ændring.

Elektronisk fakturering er nu klar til brug.

> [!NOTE]
> Virksomheder har normalt flere Finans- eller Supply Chain Management-miljøer. Disse miljøer omfatter produktionsmiljøer, UAT-miljøer (User Accept Test) og udviklingsmiljøer (sandkasse). Du skal fuldføre ovenstående procedure for alle miljøer, som du vil forbinde med Elektronisk fakturering.
