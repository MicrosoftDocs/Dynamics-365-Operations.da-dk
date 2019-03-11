---
title: Detailhierarkier
description: I denne artikel beskrives detailhierarkier i Microsoft Dynamics 365 for Retail.
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
ms.openlocfilehash: 198c8da336f3e225c5d6da2eb02c86581dc9b4d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "341896"
---
# <a name="retail-hierarchies"></a>Detailhierarkier

[!include [banner](includes/banner.md)]

I denne artikel beskrives detailhierarkier i Microsoft Dynamics 365 for Retail.

Du kan oprette et detailkategorihierarki for at organisere de produkter, du sælger gennem dine detailkanaler. Du kan bruge detailprodukthierarkier til at kategorisere eller gruppere produkter. Du kan derefter bruge disse produkter til at oprettet produktudvalg og fordelskundeprogrammer. Du kan også tildele produktattributter og egenskaber, tildele en prisstruktur, inkludere produkterne i produktkampagner og bruge produkterne til rapportering. Du kan oprette ét detailkategorihierarki til at repræsentere alle produkterne og kategorierne i organisationen og derefter bruge kategorihierarkiet til flere formål. Du kan også oprette flere detailkategorihierarkier til særlige formål, f.eks. produktkampagner. Når du opretter et detailprodukthierarki, skal du tildele en kategorihierarkitype for at identificere formålet med kategorihierarkiet. Det er f.eks. kun produkthierarkier, som er tildelt typen **Detailnavigationshierarki**, der refereres til, når du gennemser produkter efter kategori, online eller ved POS.

## <a name="retail-hierarchy-types"></a>Detailhierarkityper

Følgende tabel viser de typer detailkategorihierarkier, der er tilgængelige, og det generelle formål med hver type.

| Kategori for hierarkitype       | Formål |
|-------------------------------|---------|
| Detailprodukthierarki      | Brug denne type hierarki for at definere det generelle produkthierarki for organisationen. Du kan bruge denne type hierarki til merchandising, priser og kampagner, rapportering og planlægning af udvalg. Kun ét detailprodukthierarki kan få tildelt denne hierarkitype. |
| Supplerende detailhierarki | Brug denne hierarkitype til eventuelle yderligere detailkategorihierarkier, du vil oprette. I foråret er der for eksempel et salgsfremstød for badetøj. Derfor skal du medtage dine badetøjsprodukter i et separat kategorihierarki og anvende salgsfremmende priser til de forskellige produktkategorier. |
| Detailnavigationshierarki   | Brug denne hierarkitype til at gruppere og organisere produkter i kategorier, så produkterne kan gennemses online eller i POS. |

Når du bruger et detailkategorihierarki til at strukturere dine produkter, kan du definere og vedligeholde produktattributter og egenskaber på kategoriniveau. Disse attributter og egenskaber omfatter indstillinger for produktdimensioner og POS. Evt. produkter, som du automatisk tildeler kategorierne, arver automatisk de attributter og egenskaber, du definerer. Du kan også kopiere flere egenskabsindstillinger for et vilkårligt produkt til flere produkter i en valgt kategori på samme tid.
