---
title: Generere rapporter ved at tilføje indhold som ubehandlet XML-dokument
description: Du kan designe elektroniske rapporteringsformater (ER) for at oprette udgående dokumenter i XML-format.
author: kfend
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 87b70d5893d71e5022205a2f39f8263edf6d5280
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277536"
---
# <a name="generate-reports-by-adding-content-as-raw-xml"></a>Generere rapporter ved at tilføje indhold som ubehandlet XML-dokument

[!include[banner](../includes/banner.md)]

Du kan bruge det nye **RAW XML**-formatelement til at designe ER-formater, der genererer udgående dokumenter i XML-format. I nogle tilfælde kan du vælge at føje ubehandlede XML-data til disse rapporter af en eller flere af følgende årsager:

- Det er nemmere at bruge ubehandlede XML-filer til det oprindelige design og løbende vedligeholdelse af en rapport, fordi XML-strukturen automatisk kan genereres ved at udføre et kørselsudtryk. Derfor er det ikke nødvendigt at definere flere bindinger for flere formatelementer på designtidspunktet. Det er muligt, når de datakilder, du bruger, indeholder oplysninger, der kan bruges til at oprette XML-elementer, mens rapporten genereres.
- Ingen anden metode kan bruges til at udfylde rapporten med XML-indhold, der er modtaget tidligere og gemt i systemet. F.eks. kan det XML-svar, der genereres, muligvis indeholde indholdet af en XML-anmodning, der er sendt tidligere.
- Ingen anden metode kan bruges til at indsætte tegn i det genererede dokument baseret på deres numeriske koder. For nogle sprog og tegn findes der ikke kode af denne type. Eksempler omfatter det græske bogstav rho (ρ) og HTML-enhedskoder som \&eacute; for et *e*, der har en aigu (é).

> [!NOTE]
> Vær opmærksom på, at strukturen ikke styrer, om XML-indholdet, der er placeret i det genererede dokument ved hjælp af **RAW XML**-formatelementet, er korrekt.

Du kan finde flere oplysninger om denne funktion ved at afspiller opgaveguiderne **ER Bruge ubehandlede XML-data til at generere XML-rapporter (del 1: Designe datamodellen)** og **ER Bruge ubehandlede XML-data til at generere XML-rapporter (del 2: Designe og køre rapport)**, der er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde komponenter til it-servicer og -løsninger (10677)** og kan hentes fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Disse opgaveguider gennemgår, hvordan du konfigurerer et ER-format for at indsætte ubehandlede XML-data i genererede filer.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
