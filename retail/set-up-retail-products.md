---
title: Konfigurer detailprodukter
description: "I denne artikel beskrives, hvordan du konfigurerer detailprodukter i Microsoft Dynamics 365 for operationer – Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 116c49174989ff14982027cc235640c2ad7322f2
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-retail-products"></a>Konfigurer detailprodukter

I denne artikel beskrives, hvordan du konfigurerer detailprodukter i Microsoft Dynamics 365 for operationer – Retail.

Før du kan tilbyde produkter til videresalg i dine detailkanaler, skal du oprette og konfigurere produkterne i Dynamics 365 til operationer AX - Retail. Retail bruger produktfunktionerne i Dynamics 365 for operationer til at oprette globale produkter i produktmasteren. Du kan oprette produkterne, definerer produktegenskaber og -attributter og tildele produkterne til detailkategorien. Hvis du vil gøre produkterne tilgængelige for dine detailkanaler og føje dem til et aktivt udvalg, skal du frigive produkterne til de juridiske enheder, som de er tilgængelige i. Hvis du vil konfigurere de produkter, du sælger, ved at bruge detailkanaler, skal du udføre følgende opgaver.

1.  Definer et detailprodukthierarki. Ved hjælp af funktionerne til kategorihierarki for operationer i Dynamics 365, kan du definere detailkategorihierarkier for at gruppere og kategorisere de produkter, du leverer til dine detailkanaler. Brugerdefinerede attributter og systemattributter kan defineres på kategoriniveau. Alle de produkter, der er knyttet til kategorien, arver derefter disse attributter. Der kan defineres flere kategorihierarkier, og hvert produkt kan tildeles til flere hierarkier. Men i et enkelt hierarki kan hvert produkt kun tildeles til én kategori.
2.  Føj produkter og produktvarianter til produktmasteren. Produkter, der er føjet til produktmasteren, repræsenterer en global liste over produkter. Du kan tilføje produkter manuelt, ét ad gangen, eller du kan importere produktdata fra dine leverandører.
3.  Frigiv produkterne til juridiske enheder. Det er kun produkter, der er frigivet til juridiske enheder, som kan gøres tilgængelige for detailkanaler. Når du først definere et produkt, kan du definere det på et niveau i hele organisationen. Derefter kan du vælge én eller flere juridiske enheder, som produktet frigives til. Produktet bliver derefter tilgængeligt for flere detailkanaler på tværs af organisationen. Brug denne funktion til at oprette ét produkt ad gangen, tilføje og opdatere produktattributter og -egenskaber på ét sted og derefter distribuere produktet på tværs af organisationen til de detailkanaler, som den er tilgængelig i.
4.  Føj produkter til sortimenter. Et udvalg repræsenterer en samling af produkter, som du tilbyder i dine detailkanaler. Du kan definere et eller flere udvalg, og hvert produkt kan tildeles et eller flere udvalg. Hvis du vil tildele produkter til detailkanaler, kan du tildele udvalgene til disse detailkanaler. Når du opretter et udvalg, kan du tilføje produkter, som endnu ikke er frigivet til en juridisk enhed. Du skal dog frigive produkterne til en juridisk enhed, før disse produkter kan gøres tilgængelige for detailkanalerne.
5.  Føj produkter til navigationshierarkier. Før produkter kan gennemses online eller in point of salg (POS), skal de være kategoriseret i et navigationshierarki.
6.  Føj produkter til kataloger. Men dette trin er valgfrit for POS, kræver onlinebutikker, at produkter, der skal medtages i mindst ét katalog.


