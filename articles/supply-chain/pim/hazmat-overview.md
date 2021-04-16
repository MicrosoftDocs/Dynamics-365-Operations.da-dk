---
title: Oversigt over farligt materiale
description: Dette emne indeholder en oversigt over funktioner, der vedrører håndtering og dokumentation af farligt materiale under administration af produktoplysninger og lokationsstyring.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 15edf61cba03a57b9b4d2c939228fd064b797942
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829372"
---
# <a name="hazardous-materials-overview"></a>Oversigt over farligt materiale

[!include [banner](../includes/banner.md)]

For at overholde angivne standarder og transportreglementer skal organisationer, der leverer materialer, der er klassificeret som farligt gods, medsende ekstra papirarbejde med forsendelserne. Med funktionen til farlige materialer kan kunder lagre oplysninger, der er relateret til frigivne varer. Disse oplysninger kan derefter bruges til at udarbejde forsendelsesdokumentation. En organisation, der leverer farligt gods, skal have sine egne processer og procedurer til administration af leveringsprocessen. Microsoft Dynamics 365 Supply Chain Management er blot et værktøj, der kan hjælpe dig med at oprette de nødvendige dokumenter.

I følgende diagram illustreres de trin, der er nødvendige for at konfigurere og bruge funktionen for farlige materialer.

![Opsætning og brug af funktionen for farligt materiale](media/hazmat-overview.png "Opsætning og brug af funktionen for farligt materiale")

Funktionen for farlige materialer konfigureres i administration af produktoplysninger og indeholder dokumenter, der kan udskrives via Lokationsstyring. Disse områder er derfor generelt de to hovedområder, hvor du kan gennemse, konfigurere og bruge denne funktionalitet:

- **Administration af produktoplysninger** – Konfigurer de koder, der anvendes til frigivne produkter.
- **Lokationsstyring** – Brug yderligere forsendelsesdokumenter, der udskrives til forsendelser.

> [!IMPORTANT]
> Funktionerne for farlige materialer i Supply Chain Management giver en samling nyttige produktoplysningsfelter og tilhørende funktioner, der kan hjælpe dig med at registrere og henvise til oplysninger, der er relateret til de farlige produkter. Disse funktioner kan også være en hjælp til at designe og udskrive forsendelsesdokumenter, der indeholder nogle af de samme oplysninger om alle former for farligt materiale, som du skal levere. Systemet er dog ikke automatisk kompatibelt med alle gældende regler og bestemmelser i dit land eller område. Selvom disse værktøjer er beregnet til at hjælpe dig med at overholde de fælles regler, er de hverken tilstrækkelige i sig selv eller garanteret for at være det. Din organisation er ansvarlig for at være opmærksom på alle gældende regler og skal træffe alle nødvendige foranstaltninger for at overholde dem.

## <a name="product-information-management"></a>Administration af produktoplysninger

I Administration af produktoplysninger findes en række opsætningstabeller, hvor du kan angive referenceoplysninger til listen over farligt gods til vej-, luft-og søtransport.

Der refereredes til følgende almindelige forordninger, da denne funktion blev udviklet:

- **ADR** – bestemmelser, der er relateret til international transport af farligt gods ad vej
- **CFR 49** – bestemmelser i USA om transport af farligt gods
- **IMDG** – den internationale kode for Marine Dangerous Goods (IMDG)
- **IATA** – bestemmelser i den Internationale Luftfartssammenslutning (IATA) om farligt gods

Hvert sæt regler indeholder standardiserede lister over farligt gods og referencekoder. Supply Chain Management indeholder derfor en referencetabel for de almindelige koder på disse lister. Hver liste indeholder også nogle entydige koder, du kan definere.

Du kan finde flere oplysninger om, hvordan du konfigurerer regler og værdier for farligt materiale, og hvordan du tildeler værdierne på relevante produkter, i følgende emner:

- [Konfigurere farlige materialer](hazmat-setup.md)
- [Farlige materialer i produkter, ordrer, forsendelser og laster](hazmat-items.md)

## <a name="warehouse-management"></a>Lagerstedsstyring

Når du forbereder en forsendelse i Lokationsstyring, kan du udskrive flere nye rapporter, der bruger de oplysninger, du har angivet i administration af produktoplysninger. Yderligere oplysninger om de tilgængelige rapporter og om, hvordan du bruger dem, finder du i [Forespørgsler og rapporter om farligt materiale](hazmat-reports.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]