---
title: Flette værdimodel for anlægsaktiver og afskrivningsmodel
description: I tidligere versioner var der to værdiansættelseskoncepter for anlægsaktiver – værdimodeller og afskrivningsmodeller. I udgivelsen Microsoft Dynamics 365 for Operations (1611) er funktionaliteten af værdimodellen og afskrivningsmodellen blevet flettet ind i et enkelt bogkoncept.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a8e04f89673b3e0eb07e19aa1e14276f1f22c25b9aaabc91e2919892f74ed985
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727977"
---
# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Flette værdimodel for anlægsaktiver og afskrivningsmodel

[!include [banner](../includes/banner.md)]

I tidligere versioner var der to værdiansættelseskoncepter for anlægsaktiver – værdimodeller og afskrivningsmodeller. I udgivelsen Microsoft Dynamics 365 for Operations (1611) er funktionaliteten af værdimodellen og afskrivningsmodellen blevet flettet ind i et enkelt bogkoncept.

Den nye modelfunktionalitet er baseret på tidligere værdimodelfunktionalitet, men indeholder også alle de funktioner, der tidligere blev angivet i afskrivningsmodeller. [![Model som sammenfletning af værdimodellens og afskrivningsmodellens funktionalitet.](./media/fixed-assets.png)](./media/fixed-assets.png) På grund af denne fletning kan du nu bruge et enkelt sæt af sider, forespørgsler og rapporter for alle anlægsaktivprocesser. Tabellerne i dette emne beskriver de tidligere funktioner for afskrivningsmodeller og værdimodeller sammen med den nye funktionalitet til modeller.

## <a name="setup"></a>Konfiguration
Som standard bogfører modellerne til både Finans og reskontro for anlægsaktiv. Modeller har en ny **Bogfør i finans**-indstilling, så du kan deaktivere bogføring til Finans og nøjes med at bogføre til reskontro for anlægsaktiv. Denne funktion minder om den tidligere funktionsmåde for bogføring i afskrivningsmodeller. Opsætningen af kladdenavne har et nyt posteringslag, der hedder Ingen. Dette posteringslag blev tilføjet specifikt for anlægsaktivposteringer. Hvis du vil bogføre posteringer for modeller, der ikke bogføres til Finans, skal du bruge et kladdenavn, hvis posteringslag er angivet til **Ingen**.

| &nbsp;                                           | Afskrivningsmodel               | Værdimodel                     | Bog (ny)                                              |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
| Bogfør i finans                                   | Aldrig                           | Altid                          | Indstilling, der bogfører i finans                                |
| Posteringslag                                   | Ikke tilgængelig                  | 3: Aktuel, Drift og Moms | 11: Aktuel, Drift og Moms, 7 brugerdefinerede lag og Ingen |
| Kladdenavne                                    | Afskrivningskladder | Finans - Kladdenavne              | Finans - Kladdenavne                                      |
| Afledte bøger                                    | Ikke tilladt                     | Tilladt                         | Tilladt                                                 |
| Tilsidesættelse af afskrivningsprofil på aktivniveau | Tilladt                         | Ikke tilladt                     | Tilladt                                                 |

## <a name="processes"></a>Processer
Processer kan nu bruge en fælles side. Nogle processer er kun tilladt, hvis **Bogfør i finans**-indstillingen er angivet til **Nej** i opsætningen af modellen.

| &nbsp;                                           | Afskrivningsmodel               | Værdimodel                     | Bog (ny)                                              |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
| Transaktionspost              | Afskrivningskladde | Anlægsaktivkladde | Anlægsaktivkladde                      |
| Straksafskrivning             | Tilladt                   | Ikke tilladt         | Tilladt                                  |
| Slet historiske transaktioner | Tilladt                   | Ikke tilladt         | Tilladt, medmindre du bogfører i finans |
| Masseopdater                    | Tilladt                   | Ikke tilladt         | Tilladt, medmindre du bogfører i finans |

## <a name="inquiries-and-reports"></a>Forespørgsler og rapporter
Forespørgsler og rapporter understøtter alle modeller. Rapporter, der ikke findes i følgende tabel, understøttede tidligere både afskrivningsmodeller og værdimodeller og fortsætter nu med at understøtte alle modeltyper. Feltet **Posteringslag,** er også føjet til rapporter, så du nemmere kan identificere transaktionen transaktionsbogføringer.

| &nbsp;                                           | Afskrivningsmodel               | Værdimodel                     | Bog (ny)                                              |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
| Forespørgsler                             | Afskrivningstransaktioner | Anlægsaktivposter | Anlægsaktivposter |
| Anlægsaktivopgørelse                 | Ikke tilladt                    | Tilladt                  | Tilladt                  |
| Værdigrundlag for anlægsaktiv                     | Tilladt                        | Ikke tilladt              | Tilladt                  |
| Anvendelse af anlægsaktiver fra midt i kvartalet | Tilladt                        | Ikke tilladt              | Tilladt                  |

## <a name="upgrade"></a>Opgrader
Opgraderingsprocessen flytter din eksisterende installation og alle eksisterende transaktioner til den nye modelstruktur. Værdimodeller forbliver, som de er i øjeblikket, som en model, der bogføres i finans. Afskrivningsmodeller flyttes dog til en model, der har **Bogfør i finans**-indstillingen angivet til **Ingen**. Navne på afskrivningskladder flyttes til et finanskladdenavn med posteringslag angivet til **Ingen**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]