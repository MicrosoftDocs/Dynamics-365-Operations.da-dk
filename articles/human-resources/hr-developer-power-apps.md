---
title: Udvide Talent med Power Apps og Power Automate
description: Denne artikel beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 Human Resources ved hjælp af Microsoft Power Apps og Microsoft Power Automate.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4036378ca70089a9978a9bf5fb48c058a2064cdc
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689488"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Udvide med Power Apps og Power Automate


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Denne artikel beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 Human Resources ved hjælp af Microsoft Power Apps og Microsoft Power Automate. Du kan importere løsningspakken, der er tilknyttet hvert eksempel, til dit Power Apps-miljø. Du kan dernæst anvende pakkerne enten som vejledning eller som udgangspunktet for at implementere scenarier, der er anvendelige for din organisation.

> [!IMPORTANT]
> Såfremt du ønsker at anvende de i dette emne beskrevne skabeloner og apps "som de er", skal du afprøve dem for at sikre dig, at de omfatter alle de scenarier, der er specifikke for din implementering.

## <a name="prerequisites"></a>Forudsætninger

- For at importere pakker skal brugerne have rettigheden **Miljøoprettelse**.
- For at eksportere eller importere apps skal brugerne have en licens til en Power Apps Plan 2 eller en Power Apps Plan 2-prøveversion.

## <a name="integration-with-microsoft-365-power-automate"></a>Integration med Microsoft 365, Power Automate

Appen **Integration med Microsoft 365** kan anvendes til at udtrække teamoplysninger for brugere, der er logget på Microsoft 365. Den refererer til arbejdere i personale for at udtrække medarbejderidentifikationstyper. Ledere kan kontrollere udløbsdatoer for medarbejder-id-typer. De kan også sende en påmindelse via mail, hvis medarbejder-id-typen udløber. Power Automate kan integreres med Power Apps for at sende denne påmindelse. Der sendes en bekræftelse tilbage til Power Apps fra Power Automate, når påmindelsen er sendt. Identifikationstyper omfatter chaufførens kørekort, pas og andre acceptable former for id.

Du kan udvide denne app til andre scenarier. Du kan eksempelvis anvende den til at vise oplysninger om teamets ferie, kalenderhændelser og alle teamspecifikke hændelser.

Du kan downloade appen **Integration med Microsoft 365, Power Automate** ved at gå til [Integration med Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) i Microsoft Download Center.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – Forbindelse til SQL og udførelse

Skabelonen **Power Automate – Forbindelse til SQL og udførelse** forbinder til Microsoft SQL Server og gør det muligt at køre SQL-forespørgsler.

Selvom denne skabelon læser og opdaterer SQL-tabeller, kan du udvide den og bruge den til andre scenarier. Du kan eksempelvis anvende den til at udfylde en stadieinddelt tabel i Dataverse med poster fra SQL-serveren og til at synkronisere den stadieinddelte tabel periodisk ved hjælp af en trinvis overførelse fra SQL-serveren.

En avanceret forespørgsel er integreret med flow, der muliggør datatransformation og trinvis push.

Du kan downloade skabelonen **Power Automate – Forbindelse til SQL og udførelse** i Microsoft Download Center ved hjælp af følgende link: [Power Automate – Forbindelse til SQL og udførelse](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="additional-resources"></a>Yderligere ressourcer

[Klientens Microsoft Power Platform](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
