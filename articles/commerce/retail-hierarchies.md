---
title: Commerce-hierarkier
description: I denne artikel beskrives hierarkier i Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e1b9fc647ccaa3caeec0d0e3a8594fd6a2a8be0f
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070730"
---
# <a name="commerce-hierarchies"></a>Commerce-hierarkier

[!include [banner](includes/banner.md)]

I denne artikel beskrives hierarkier i Dynamics 365 Commerce.

Du kan oprette et kategorihierarki for at organisere de produkter, du sælger gennem dine kanaler. Du kan bruge produkthierarkier til at kategorisere eller gruppere produkter. Du kan derefter bruge disse produkter til at oprettet produktudvalg og fordelskundeprogrammer. Du kan også tildele produktattributter og egenskaber, tildele en prisstruktur, inkludere produkterne i produktkampagner og bruge produkterne til rapportering. Du kan oprette ét kategorihierarki til at repræsentere alle produkter og kategorier i organisationen og derefter bruge kategorihierarkiet til flere formål. Du kan også oprette flere kategorihierarkier til særlige formål, som produktkampagner. Når du opretter et produkthierarki, skal du tildele en kategorihierarkitype for at identificere formålet med kategorihierarkiet. Det er f.eks. kun produkthierarkier, som er tildelt typen **Commerce-navigationshierarki**, der refereres til, når du gennemser produkter efter kategori, online eller ved POS.

## <a name="hierarchy-types"></a>Hierarkityper

Følgende tabel viser de typer kategorihierarkier, der er tilgængelige, og det generelle formål med hver type.

| Kategori for hierarkitype       | Formål |
|-------------------------------|---------|
| Produkthierarki      | Brug denne type hierarki for at definere det generelle produkthierarki for organisationen. Du kan bruge denne type hierarki til merchandising, priser og kampagner, rapportering og planlægning af udvalg. Kun ét produkthierarki kan få tildelt denne hierarkitype. |
| Supplerende hierarki | Brug denne hierarkitype til eventuelle yderligere kategorihierarkier, du vil oprette. I foråret er der for eksempel et salgsfremstød for badetøj. Derfor skal du medtage dine badetøjsprodukter i et separat kategorihierarki og anvende salgsfremmende priser til de forskellige produktkategorier. |
| Navigationshierarki   | Brug denne hierarkitype til at gruppere og organisere produkter i kategorier, så produkterne kan gennemses online eller i POS. |

Når du bruger et kategorihierarki til at strukturere dine produkter, kan du definere og vedligeholde produktattributter og egenskaber på kategoriniveau. Disse attributter og egenskaber omfatter indstillinger for produktdimensioner og POS. Evt. produkter, som du automatisk tildeler kategorierne, arver automatisk de attributter og egenskaber, du definerer. Du kan også kopiere flere egenskabsindstillinger for et vilkårligt produkt til flere produkter i en valgt kategori på samme tid.
