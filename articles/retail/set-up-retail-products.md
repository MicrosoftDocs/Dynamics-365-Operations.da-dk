---
title: Konfigurere detailprodukter
description: I denne artikel beskrives, hvordan du konfigurerer detailprodukter i Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 991546424a95463315eaa73c2776d0defe66def5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "357398"
---
# <a name="set-up-retail-products"></a>Konfigurere detailprodukter

[!include [banner](includes/banner.md)]

I denne artikel beskrives, hvordan du konfigurerer detailprodukter i Microsoft Dynamics 365 for Retail.

Før du kan tilbyde produkter til videresalg i dine detailkanaler, skal du oprette og konfigurere produkterne i Dynamics 365 for Retail. Detail bruger produktfunktionerne i Dynamics 365 for Retail til at oprette produkter for hele organisationen i produktmasteren. Du kan oprette produkterne, definerer produktegenskaber og -attributter og tildele produkterne til detailkategorien. Hvis du vil gøre produkterne tilgængelige for dine detailkanaler og føje dem til et aktivt udvalg, skal du frigive produkterne til de juridiske enheder, som de er tilgængelige i. Hvis du vil konfigurere de produkter, du sælger, ved at bruge detailkanaler, skal du udføre følgende opgaver.

1. Definer et detailprodukthierarki. Ved hjælp af funktionerne til kategorihierarki i Dynamics 365 for Retail kan du definere detailkategorihierarkier til at gruppere og kategorisere de produkter, du fordeler til dine detailkanaler. Brugerdefinerede attributter og systemattributter kan defineres på kategoriniveau. Alle de produkter, der er knyttet til kategorien, arver derefter disse attributter. Der kan defineres flere kategorihierarkier, og hvert produkt kan tildeles til flere hierarkier. Men i et enkelt hierarki kan hvert produkt kun tildeles til én kategori.
2. Føj produkter og produktvarianter til produktmasteren. Produkter, der er føjet til produktmasteren, repræsenterer en global liste over produkter. Du kan tilføje produkter manuelt, ét ad gangen, eller du kan importere produktdata fra dine leverandører.
3. Frigiv produkterne til juridiske enheder. Det er kun produkter, der er frigivet til juridiske enheder, som kan gøres tilgængelige for detailkanaler. Når du først definere et produkt, kan du definere det på et niveau i hele organisationen. Derefter kan du vælge én eller flere juridiske enheder, som produktet frigives til. Produktet bliver derefter tilgængeligt for flere detailkanaler på tværs af organisationen. Brug denne funktion til at oprette ét produkt ad gangen, tilføje og opdatere produktattributter og -egenskaber på ét sted og derefter distribuere produktet på tværs af organisationen til de detailkanaler, som den er tilgængelig i.
4. Føj produkter til sortimenter. Et udvalg repræsenterer en samling af produkter, som du tilbyder i dine detailkanaler. Du kan definere et eller flere udvalg, og hvert produkt kan tildeles et eller flere udvalg. Hvis du vil tildele produkter til detailkanaler, kan du tildele udvalgene til disse detailkanaler. Når du opretter et udvalg, kan du tilføje produkter, som endnu ikke er frigivet til en juridisk enhed. Du skal dog frigive produkterne til en juridisk enhed, før disse produkter kan gøres tilgængelige for detailkanalerne.
5. Føj produkter til navigationshierarkier. Før produkter kan gennemses online eller ved POS, skal de være kategoriseret i et navigationshierarki for detail.
6. Føj produkter til kataloger. Selvom dette trin er valgfrit for POS, kræver onlinebutikker, at produkter skal medtages i mindst ét katalog.
