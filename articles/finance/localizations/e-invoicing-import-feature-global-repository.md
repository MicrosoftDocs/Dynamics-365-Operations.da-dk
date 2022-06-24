---
title: Importere funktioner fra det globale lager
description: Denne artikel forklarer, hvordan du importerer funktioner til globalisering fra det globale lager.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: bc8f346cdef4aa0b909d75b016b37cbbe3248ebf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865549"
---
# <a name="import-features-from-the-global-repository"></a>Importere funktioner fra det globale lager

[!include [banner](../includes/banner.md)]

Globalt lager indeholder funktioner til elektronisk fakturering, der deles med din konfigurationsudbyder. Alle funktioner for elektronisk fakturering, der leveres af Microsoft, deles med alle regnskaber. Du har automatisk adgang til alle funktioner for elektronisk fakturering, som Microsoft udgiver og publicerer til det globale lager.

Hvis du vil begynde at arbejde med funktioner til elektronisk fakturering, der deles med din konfigurationsudbyder, skal du importere dem til din forekomst af RCS (Regulatory Configuration Service) fra det globale lager. Gennemse derefter funktionsoplysninger som f.eks. ER-konfigurationerne (Elektronisk rapportering) og behandling af pipelines.

## <a name="import-a-feature-from-the-global-repository"></a>Importere en funktion fra det globale lager

1. Log på din RCS-konto.
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Elektronisk fakturering**.
3. Vælg **Importér** for at åbne opslaget **Importér funktion fra globalt lager**.
4. Du kan gennemse de funktioner for elektronisk fakturering, der er tilgængelige i det globale lager for en bestemt konfigurationsudbyder, ved at synkronisere din organisations RCS-forekomst ved at vælge **Synkroniser**. Når synkroniseringen er fuldført, opdateres listen over tilgængelige funktioner for elektronisk fakturering fra det globale lager. Denne opdatering kan tage nogle få minutter.
5. Vælg den funktion, der skal importeres, og vælg derefter **Importér**.

Hvis du vil se den importerede funktion til elektronisk fakturering skal du sørge for, at den korrekte konfigurationsudbyder er valgt. Funktioner, der er oprettet af den aktive konfigurationsudbyder, filtreres som standard automatisk ud. Du kan justere filteret for at få vist funktioner, der er oprettet af andre udbydere, f.eks. Microsoft-konfigurationsudbyderen.

Du kan nu arbejde med den importerede funktion. Du kan gennemse oplysningerne i den og oprette en ny funktion ved at bruge den importerede funktion som en skabelon.

> [!NOTE]
> Du kan kun redigere en funktion, hvis den er oprettet af den aktuelt aktive konfigurationsudbyder. Du kan oprette en ny funktion ved at bruge den oprindelige funktion som basis. Du kan derefter foretage de nødvendige ændringer eller konfigurere parametrene.

Når Microsoft eller et andet firma, der deler globaliseringsfunktioner med dit firma, opdaterer funktioner, du har importeret, kan du kontrollere, om der er opdaterede versioner, ved at vælge **Kontrollér, om der er funktionsopdateringer** i afsnittet **Relaterede indstillinger** i arbejdsområdet til **Globaliseringsfunktioner**.

Hvis du ser, at der er opdateringer til en funktion, du bruger som skabelon, kan du importere en ny version, når du har synkroniseret listen over publicerede funktioner i det globale lager.
