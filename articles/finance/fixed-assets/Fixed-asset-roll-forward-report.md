---
title: Rapporten Rul anlægsaktiver fremad
description: Dette emne forklarer, hvordan du kan bruge rapporten Rul anlægsaktiver fremad.
author: saraschi2
manager: ''
ms.date: 01/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: b91da4679a23ba0a70c18e2bcae1b7f757f661ca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969147"
---
# <a name="fixed-assets-roll-forward-report"></a>Rapporten Rul anlægsaktiver fremad

[!include [banner](../includes/banner.md)]

Rapporten **Rul anlægsaktiver fremad** indeholder, i et letlæseligt Microsoft Excel-format, de detaljerede data om anlægsaktiver, du har brug for til lukning af periode, regnskaber og skatterapportering. Rapporten omfatter start- og slutsaldi for anlægsaktiver, sammen med værdibevægelser for perioden, og eventuelle nye anskaffelser og salg, der er opstået i løbet af perioden. Data rapporteres for de enkelte anlægsaktiver, og der opsummeres også værdierne for anlægsaktivgrupper og den juridiske enhed.

Rapporten **Rul anlægsaktiver fremad** bruger strukturen til elektronisk rapportering (ER). Før du kan køre rapporten, skal modellen for anlægsaktiver og konfigurationer for fremadrulning af anlægsaktiver importeres fra Microsoft Dynamics Lifecycle Services (LCS). Du kan finde vejledning i [Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Denne rapport er tilgængelig i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3, eller som et hotfix til Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017). Tre hotfixes, der skal anvendes på miljøer, der har versionen fra juli 2017:

- **KB 4041754:** Konfiguration af elektronisk rapportering (ER) kan ikke hentes fra LCS, da det ikke er relevant for den aktuelle version efter anvendelse af platform update-pakken
- **KB 4056107:** Elektronisk indberetning (TYSK) kumulativ opdatering 5
- **KB 4056353:** Rapporter for opgørelse og noter om anlægsaktiver, der ikke opfylder kravene i GAAP og IFRS

I følgende tabel forklares de felter, der er tilgængelige på rapporten.


|                    Felt                    |                                                                                                                                Betegnelse                                                                                                                                |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              Saldi: Åbnings              |                                                                                           Anlægsaktivets bogførte nettoværdi fra den "fra"-dato, der er angivet i rapporten.                                                                                           |
|              Saldi: Ultimo              |                                                                                            Anlægsaktivets bogførte nettoværdi fra den "til"-dato, der er angivet i rapporten.                                                                                            |
|         Anskaffelser: Åbningsværdi         |                                                 Summen af alle transaktioner af typerne <strong>Anskaffelse</strong> og <strong>Anskaffelsesregulering</strong> op til den "fra"-dato, der er angivet i rapporten.                                                  |
|      Anskaffelser: Periodeanskaffelser      |                                                 Summen af alle transaktioner af typerne <strong>Anskaffelse</strong> og <strong>Anskaffelsesregulering</strong>, der blev posteret i datointervallet for rapporten.                                                  |
|       Anskaffelser: Periodekassationer        |                                                                        Summen af alle tilbageførsler af anskaffelser, der blev posteret, som havde en kassationstransaktion i datointervallet for rapporten.                                                                        |
|         Anskaffelser: Ultimoværdi         |                                                  Summen af alle transaktioner af typerne <strong>Anskaffelse</strong> og <strong>Anskaffelsesregulering</strong> op til den "til"-dato, der er angivet i rapporten.                                                   |
|        Afskrivninger: Åbningsværdi         | Summen af alle posteringer af typerne <strong>Afskrivning</strong>, <strong>Afskrivningsregulering</strong>, <strong>Særlig afskrivning</strong> og <strong>Ekstraordinær afskrivning</strong> op til den "fra"-dato, der er angivet i rapporten. |
|     Afskrivninger: Periodeafskrivninger     |                         Summen af alle transaktioner af typerne <strong>Afskrivning</strong>, <strong>Afskrivningsjustering</strong> og <strong>Ekstraordinær afskrivning</strong>, der blev posteret i datointervallet for rapporten.                          |
| Afskrivninger: Særlige afskrivninger i perioden |                                                              Summen af alle transaktioner af typen <strong>Særlig afskrivning</strong>, der blev posteret i datointervallet for rapporten.                                                               |
|       Afskrivninger: Periodekassationer       |                                                                       Summen af alle tilbageførsler af afskrivninger, der blev posteret, som havde en kassationstransaktion i datointervallet for rapporten.                                                                        |
|        Afskrivninger: Ultimoværdi         |  Summen af alle posteringer af typerne <strong>Afskrivning</strong>, <strong>Afskrivningsregulering</strong>, <strong>Særlig afskrivning</strong> og <strong>Ekstraordinær afskrivning</strong> op til den "til"-dato, der er angivet i rapporten.  |
|    Opskrivninger/nedskrivninger: Åbningsværdi     |                              Summen af alle transaktioner af typerne <strong>Opskrivningsregulering</strong>, <strong>Nedskrivningsregulering</strong> og <strong>Værdiregulering</strong> op til den "fra"-dato, der er angivet i rapporten.                               |
|   Opskrivninger/nedskrivninger: Periodens opskrivninger   |                                                                    Summen af alle transaktioner af typen <strong>Opskrivningsregulering</strong>, der blev posteret i datointervallet for rapporten.                                                                    |
|  Opskrivninger/nedskrivninger: Periodens nedskrivninger  |                                                                   Summen af alle transaktioner af typen <strong>Nedskrivningsregulering</strong>, der blev posteret i datointervallet for rapporten.                                                                   |
| Opskrivninger/nedskrivninger: Periodens værdireguleringer  |                                                                        Summen af alle transaktioner af typen <strong>Værdiregulering</strong>, der blev posteret i datointervallet for rapporten.                                                                        |
|   Opskrivninger/nedskrivninger: Periodens kassationer   |                                                           Summen af alle tilbageførsler af opskrivninger, nedskrivninger og værdireguleringer, der blev posteret, som havde en kassationstransaktion i datointervallet for rapporten.                                                           |
|    Opskrivninger/nedskrivninger: Ultimoværdi     |                               Summen af alle transaktioner af typerne <strong>Opskrivningsregulering</strong>, <strong>Nedskrivningsregulering</strong> og <strong>Værdiregulering</strong> op til den "til"-dato, der er angivet på rapporten.                                |
|          Kassationer: Kassationsdato           |                                                                                                                Kassationsdatoen for anlægsaktivet.                                                                                                                |
|    Kassationer: Bogført nettoværdi ved kassation    |                                                                                                    Anlægsaktivets bogførte nettoværdi på kassationstidspunktet.                                                                                                    |
|            Kassationer: Salgsværdi            |                                                                                               Salgsværdien for anlægsaktivet med en kassation – salgstransaktion.                                                                                                |
|           Kassationer: Scrapværdi            |                                                                                               Scrapværdien for anlægsaktivet med en kassation – scraptransaktion.                                                                                               |
|           Kassationer: Gevinst/tab            |                                                                                 Gevinst- eller tabsværdien beregnes som en del af kassationsposteringen for anlægsaktivet.                                                                                 |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]