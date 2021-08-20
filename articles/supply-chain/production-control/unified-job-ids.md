---
title: Samlet nummerserie for job-id'er
description: Denne funktion indeholder en enkelt samlet nummerserie, der genererer job-id'er til modulerne Produktionsstyring, Produktionsudførelse og Tid og fremmøde.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8ff8fae0bb20b11b15c7520fbb14727ff0372ca0255adc82599c6680a64671af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748709"
---
# <a name="unified-number-sequence-for-job-ids"></a>Samlet nummerserie for job-id'er

[!include [banner](../includes/banner.md)]

Denne funktion indeholder en enkelt samlet nummerserie, der genererer job-id'er til modulerne Produktionsstyring, Produktionsudførelse og Tid og fremmøde. Tidligere kunne du vælge en anden nummerserie til hver af disse moduler, hvilket kunne resultere i konflikter mellem job-id'er, hvis to eller flere af disse nummerserier brugte et identisk format. En sådan konflikt kan bevirke, at data bliver beskadiget.

## <a name="turn-on-this-feature-for-your-system"></a>Aktivere denne funktion i dit system

Hvis systemet ikke allerede indeholder den funktion, der er beskrevet i dette emne, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Samlet nummerserie for job-id'er*.

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>Konfigurere samlet nummerserie for job-id'er

Når denne funktion er aktiveret, bliver de eksisterende indstillinger for nummerserier til **Job-id**, der findes på parametersiderne for Produktionsstyring, Produktionsudførelse og Tid og fremmøde frarådet, og der vil blive tilføjet et nyt **Samlet job-id**-felt. Værdien af **Samlet job-id** deles af alle tre moduler, hvilket sikrer, at alle moduler refererer til samme nummerserie. Job-id'er vil derfor være entydige på tværs af alle tre moduler, og der vil aldrig forekomme en konflikt.

Sådan konfigurerer du en samlet nummerserie for job-id'er:

1. Aktivér funktionen som beskrevet i forrige afsnit.
1. Identificer enten den nummerserie, du vil bruge til dine samlede job-id'er, eller opret en ny. Du kan finde flere oplysninger under [Oversigt over nummerserier](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).
1. Gå til siden **Parametre for produktionsstyring**, **Parametre for produktionsudførelse** eller **Parametre for tid og fremmøde**. Det betyder ikke noget, hvilken af dem du vælger, for når du foretager denne indstilling på en af disse sider, opdateres alle de andre sider automatisk.
1. Åbn fanen **Nummerserier** på den valgte parameterside.
1. Tildel den **Nummerseriekode**, som du tidligere har identificeret, til rækken **Samlede job-id'er** i gitteret.
