---
title: Oprette en faktureringskode for den offentlige sektor
description: Brugerdefinerede felter til faktureringskoder gør det muligt at indsamle værdier for faktureringskodefelter, når der oprettes fritekstfakturaer.
author: twheeloc
ms.date: 02/14/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustCustomField
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 849f5342273c4440e60ebf6d19c77829eb483d9e
ms.sourcegitcommit: 6a269db08e8bb3bb3405c9f4a512091d13c80faa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119572"
---
# <a name="create-a-billing-code-for-the-public-sector"></a>Oprette en faktureringskode for den offentlige sektor

[!include [banner](../../includes/banner.md)]

Brugerdefinerede felter til faktureringskoder gør det muligt at indsamle værdier for faktureringskodefelter, når der oprettes fritekstfakturaer. Når du har tildelt det brugerdefinerede felt til faktureringskoder, kan brugerne få adgang til feltet, når faktureringskoden vælges på en fritekstfakturalinje. Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.

1. Gå til **Debitor > Konfiguration > Brugerdefinerede felter for faktureringskode**.
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Navn**.
4. Vælg en indstilling i feltet **Type**.
    * Når du vælger en indstilling, ændres felterne i sektionen **Beskrivelse** til de indstillinger, der er tilgængelige for denne indstilling.  
    * Angiv standardværdien for dette brugerdefinerede felt og andre værdier, der skal bruges, i afsnittet **Detaljer**.  
5. Åbn afsnittet **Beskrivelse**.
6. Valgfrit: I feltet **Beskrivelse af forbrug** kan du beskrive, hvordan det brugerdefinerede felt skal bruges. Oplysningerne anvendes kun internt. De er ikke synlige for brugeren.
7. Åbn sektionen **Referencer til faktureringskode**. Når du tildeler dette brugerdefinerede felt til en faktureringskode, vises den faktureringskoden her.
8. Klik på **Gem**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
