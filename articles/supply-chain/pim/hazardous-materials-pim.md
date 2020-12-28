---
title: Farlige materialer
description: Dette emne indeholder oplysninger om dokumenter og oplysninger om farligt materiale, der er gemt i dit miljø.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: feee6b348ac1870295a894ad988278b23a3f30a3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424774"
---
# <a name="hazardous-materials"></a>Farlige materialer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Oplysninger om farligt materiale konfigureres i Administration af produktoplysninger. Dette modul har desuden også dokumenter, der kan udskrives via lokationsstyring.

Når du sender materialer, der klassificeres som farligt gods, kræves der flere papirer, der skal følge forsendelserne. Funktionen til farlige materialer giver kunder mulighed for at lagre klassifikationsoplysninger og knytte dem til frigivelse af varer. Disse oplysninger kan derefter bruges til at udarbejde forsendelsesdokumentation.

> [!IMPORTANT]
> Funktionerne for farlige materialer i Microsoft Dynamics 365 Supply Chain Management giver en samling nyttige produktoplysningsfelter og tilhørende funktioner, der kan hjælpe dig med at registrere og henvise til oplysninger, der er relateret til de farlige produkter. Disse funktioner kan også være en hjælp til at designe og udskrive forsendelsesdokumenter, der indeholder nogle af de samme oplysninger om alle former for farligt materiale, som du skal levere. Systemet er dog ikke automatisk kompatibelt med alle gældende regler og bestemmelser i dit land eller område. Selvom disse værktøjer er beregnet til at hjælpe dig med at overholde de fælles regler, er de hverken tilstrækkelige i sig selv eller garanteret for at være det. Din organisation er ansvarlig for at være opmærksom på alle gældende regler og skal træffe alle nødvendige foranstaltninger for at overholde dem.

Før du kan bruge denne funktion, kræves følgende opsætning:

- **Administration af produktoplysninger**: Konfigurer koder, der kan anvendes til frigivne produkter.
- **Lokationsstyring**: Brug flere forsendelsesdokumenter til at udskrive forsendelsesoplysninger.

## <a name="product-information-management"></a>Administration af produktoplysninger

I Administration af produktoplysninger findes der et interval af opsætningstabeller, hvor du kan tilføje referenceoplysninger, der findes på listen over farligt gods til vej-, luft-og søtransport.

Her er nogle af de bestemmelser, der ofte refereres til:

- **ADR** – bestemmelser, der er relateret til international transport af farligt gods ad vej
- **CFR 49** – bestemmelser i USA om transport af farligt gods
- **IMDG** – den internationale kode for Marine Dangerous Goods (IMDG)
- **IATA** – bestemmelser i den Internationale Luftfartssammenslutning (IATA) om farligt gods

Alle disse bestemmelser har en liste over farligt gods med referencekoder. Listerne for hver transporttype kombineres i delte internationale klassifikationer. Supply Chain Management indeholder en referencetabel for de delte koder på disse lister. Hver liste indeholder også nogle entydige koder, der kan defineres.

Hvis du vil konfigurere disse oplysninger, skal du oprette en bestemmelse, som du kan bruge til at konfigurere de første parametre.

## <a name="warehouse-management"></a>Lokationsstyring

Når en forsendelse udarbejdes, kan der udskrives flere nye rapporter. Disse rapporter bruger de oplysninger, du har angivet i Administration af produktoplysninger.
