---
title: Konfigurere detailprodukter
description: I denne artikel beskrives, hvordan du konfigurerer produkter i Dynamics 365 Commerce.
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
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 54551507b2f4ef2f60eecf9d9536a76f33ef4f16
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264426"
---
# <a name="set-up-retail-products"></a>Konfigurere detailprodukter

[!include [banner](includes/banner.md)]

I denne artikel beskrives, hvordan du konfigurerer produkter i Dynamics 365 Commerce.

Før du kan tilbyde produkter til videresalg i dine handelskanaler, skal du oprette og konfigurere produkterne. Commerce opretter produkter i produktmasteren til hele organisationen. Du kan oprette produkterne, definere produktegenskaber og -attributter og tildele produkterne til handelskategorihierarkier. Hvis du vil gøre produkterne tilgængelige for dine kanaler og føje dem til et aktivt udvalg, skal du frigive produkterne til de juridiske enheder, hvor de er tilgængelige. Hvis du vil konfigurere de produkter, du sælger, ved at bruge kanaler, skal du udføre følgende opgaver.

1. **Definer et produkthierarki.** Ved hjælp af funktionerne til kategorihierarki i Commerce kan du definere kategorihierarkier for at gruppere og kategorisere de produkter, du distribuerer til dine kanaler. Brugerdefinerede attributter og systemattributter kan defineres på kategoriniveau. Alle de produkter, der er knyttet til kategorien, arver derefter disse attributter. Der kan defineres flere kategorihierarkier, og hvert produkt kan tildeles til flere hierarkier. Men i et enkelt hierarki kan hvert produkt kun tildeles til én kategori.
2. **Føj produkter og produktvarianter til produktmasteren.** Produkter, der er føjet til produktmasteren, repræsenterer en global liste over produkter. Du kan tilføje produkter manuelt, ét ad gangen, eller du kan importere produktdata fra dine leverandører.
3. **Frigiv produkterne til juridiske enheder.** Det er kun produkter, der er frigivet til juridiske enheder, som kan gøres tilgængelige for dine kanaler. Når du først definere et produkt, kan du definere det på et niveau i hele organisationen. Derefter kan du vælge én eller flere juridiske enheder, som produktet frigives til. Produktet bliver derefter tilgængeligt for flere kanaler på tværs af din organisation. Brug denne funktion til at oprette ét produkt ad gangen, tilføje og opdatere produktattributter og -egenskaber på ét sted og derefter distribuere produktet på tværs af organisationen til de kanaler, som det er tilgængeligt i.
4. **Føj produkter til sortimenter.** Et udvalg repræsenterer en samling af produkter, som du tilbyder i dine kanaler. Du kan definere et eller flere udvalg, og hvert produkt kan tildeles et eller flere udvalg. Hvis du vil tildele produkter til kanaler, kan du tildele disse kanaler sortimenter. Når du opretter et udvalg, kan du tilføje produkter, som endnu ikke er frigivet til en juridisk enhed. Du skal dog frigive produkterne til en juridisk enhed, før disse produkter kan gøres tilgængelige for kanalerne.
5. **Føj produkter til navigationshierarkier.** Før produkter kan gennemses online eller ved POS, skal de være kategoriseret i et navigationshierarki for Commerce.
6. **Føj produkter til kataloger.** Selvom dette trin er valgfrit for POS, kræver onlinebutikker, at produkter skal medtages i mindst ét katalog.


[!INCLUDE[footer-include](../includes/footer-banner.md)]