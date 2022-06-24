---
title: Oprette gebyrer på interne ordrer
description: Denne artikel forklarer, hvordan du konfigurerer gebyrer på interne ordrer
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7b84c0bac6c31139170a99afc65cd08d70bd018e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885835"
---
# <a name="set-up-charges-on-intercompany-orders"></a>Oprette gebyrer på interne ordrer

[!include [banner](../../includes/banner.md)]

Du kan definere gebyrer, der skal føjes til interne ordrer. Når et gebyr føjes til en intern salgsordre, synkroniseres den automatisk med den interne indkøbsordre. Det fungerer begge veje – fra den interne salgsordre til indkøbsordren og modsat.

Du kan bruge gebyrer til at føje avance til en intern salgsordre ved at definere gebyret som en intern procent.

Når du definerer gebyrer, der skal anvendes på interne ordrer, aktiverer du beregningen af intern avance for en intern salgsordre på basis af nettobeløbet i den oprindelige salgsordre. Det kan du f.eks. gøre, hvis den interne kreditor sælger til dig til kostpris. Følgende fremgangsmåde beskriver, hvordan dette gøres for interne debitorer. Du kan bruge samme fremgangsmåde til kreditorer.

1. Gå til **Debitor \> Konfiguration \> Gebyrer \> Debitorgebyrgrupper**.
1. Opret en gebyrgruppe.
1. Gå til **Debitorer \> Kunder \> Alle kunder**. Vælg debitorkontolink. Vælg **Kunde** i handlingsruden, og vælg derefter oversigtspanelet **Salgsordre**.
1. Vælg **Rediger** i handlingsruden for at aktivere redigering i feltet. Vælg den interne gebyrgruppe, som du oprettede i trin 2, i feltet **Gebyrgruppe**.
1. Gå til **Debitor \> Konfiguration \> Gebyrer \> Automatiske gebyrer**.
1. Definer gebyrerne ved at udfylde de relevante felter.
1. Vælg den interne gebyrgruppe, som du oprettede i trin 2, i feltet **Kunderelation**.
1. I oversigtspanelet **Linjer** i feltet **Kategori**, vælg **Intern procent**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
