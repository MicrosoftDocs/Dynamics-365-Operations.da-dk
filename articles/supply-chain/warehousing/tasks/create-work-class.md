---
title: Oprette en arbejdsklasse
description: Denne procedure viser, hvordan du opretter en arbejdsklasse.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkClass
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed9b72d891df4d40213d4854da6b09bd9876effa
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424986"
---
# <a name="create-a-work-class"></a>Oprette en arbejdsklasse

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du opretter en arbejdsklasse. Arbejdsklasser bruges til at dirigere og/eller begrænse typen af arbejdsordrelinjer, som en lagermedarbejder kan behandle på en mobilenhed. De linjer, som en medarbejder kan behandle, bestemmes fra arbejdsklasserne på de varer i mobilenhedsmenuen, som lagermedarbejderen har adgang til, og arbejdsklassen, der er angivet på arbejdslinjerne. Arbejdsklasser kan også bruges til at validere placeringslokalitet for en arbejdsordrelinje. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data. Denne procedure er beregnet til lagerchefen.

1. Gå til Lagerstyring > Opsætning > Arbejde > Arbejdsklasser.
2. Klik på Ny.
3. Skriv en værdi i feltet Arbejdsklasse-id.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg en indstilling i feltet Arbejdsordretype.
6. Klik på Ny.
7. Indtast en værdi i feltet Lokalitetstype.
    * Hvis du vælger en lokalitetstype, angiver dette en begrænsning på, hvor varer kan placeres, når de er valgt. Denne indstilling bruges, når en lokalitetsvejledning forsøger at finde lokaliteten, eller hvis en lagermedarbejder manuelt angiver lokaliteten for varen i mobilenhedsmenuen.  
8. Luk siden.

