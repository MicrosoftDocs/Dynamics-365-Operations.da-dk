---
title: "Bogføringskonti for anskaffelse af anlægsaktiver"
description: "I denne artikel beskrives det, hvordan du konfigurerer finansbogføringskonti til anskaffelse af anlægsaktiver."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d89bff85317a6aee952d32a9c29f0ebdd27934ec
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="fixed-asset-acquisition-posting-accounts"></a>Bogføringskonti for anskaffelse af anlægsaktiver

[!include[banner](../includes/banner.md)]


I denne artikel beskrives det, hvordan du konfigurerer finansbogføringskonti til anskaffelse af anlægsaktiver.

Konti, der bruges til at bogføre anskaffelser af anlægsaktiver kan variere afhængigt af den metode, der bruges til at anskaffe aktivet. På siden Posteringsprofiler for anlægsaktiver under fanen Finans skal du vælge Anskaffelse og Anskaffelsesregulering for at konfigurere konti til anlægsaktiver, der skal bogføres i Finans. 

I kladder og på indkøbsordrer er finanskontoen normalt den statuskonto, hvor det nye anlægsaktivs anskaffelsesværdi debiteres. Denne konto kan ikke ses i kladden og kan ikke erstattes under posteringer. 

Modkonto er ligeledes en statuskonto. I finanskladden og anlægsaktivkladden er denne konto ofte den bankkonto, der bruges til at betale for anskaffelsen af anlægsaktivet. Modkontoen er en standardkonto, der foreslås automatisk i kladderne. Den kan ændres i kladden til en hvilken som helst anden konto fra kontoplanen eller til en kreditorkonto, hvis anlægsaktivet er købt hos en leverandør. 

Når Fakturajournal eller Indkøbsordrer i Kreditor bruges til anskaffelse af anlægsaktiver, erstattes modkontoen for anlægsaktivposteringen med den kreditorkonto, der er valgt til posteringen.

For anskaffelser, der bogføres vha. kladden Lager til anlægsaktiver i Finans, købes anlægsaktivet ikke fra eksterne kilder, men overføres fra firmaets eget lager. Derfor er modkontoen en lagerafgangskonto for lagervaren i Lagerstyring.

Du kan finde flere oplysninger under [Anskaffelse af aktiver via indkøb](acquire-assets-procurement.md).



