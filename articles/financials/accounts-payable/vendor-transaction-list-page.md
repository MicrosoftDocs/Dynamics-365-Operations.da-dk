---
title: Listesiden Kreditortransaktion
description: Dette emne indeholder oplysninger om listesiden Kreditortransaktion til Microsoft Dynamics 365 for Finance and Operations.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 1ef7d97f059801f2fb2c0d451546b57055208f81
ms.contentlocale: da-dk
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-transaction-list-page"></a>Listesiden Kreditortransaktion

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Vis udligninger

Fanen **Vis udligninger** i handlingsruden giver hurtig adgang til udligningshistorikken og yderligere oplysninger om hele udligningsposteringen. Du kan også vise ekstra posteringer, der vedrører den valgte postering, enten fordi de var en del af samme udligning, eller fordi de er betalinger, der er oprettet i samme betalingskladde.

1. Vælg **Kreditor \> Alle kreditorer**.
2. Vælg en kreditor med posteringer, og vælg derefter **Kreditor \> Transaktioner**.
3. Vælg en postering, der skal undersøges.
4. Vælg fanen **Vis udligninger** i handlingsruden.

    Dialogboksen **Vis udligninger** åbnes og viser den valgte postering og alle dokumenter, der er udlignet mod den. Denne dialogboks ligner udligningshistorikvisningen, men den omfatter alle relaterede dokumenter.

5. Du kan udføre forskellige opgaver i denne dialogboks. Vælg en eller flere bilag, og vælg derefter en af følgende menuer:

   - **Vis regnskab** – Alle bilag, der har relation til de valgte dokumenter, vises. Vælg **Luk** for at lukke dialogboksen.
   - **Eksporter** – Eksporter de valgte bilag til Microsoft Excel.
   - **Vis relaterede betalinger** – Alle betalingskladdeposterne, der er oprettet i den betalingskladde, som er relateret til det valgte dokument, vises. Derudover vises alle de udligninger, der er knyttet til disse betalinger. Navnet på denne menu ændres også til **Vis udligninger**. Vælg **Vis udligninger** for kun at vise de posteringer, der blev vist, da du oprettede dialogboksen **Vis udligninger**.
    - **Udlign posteringer** – Denne menu vises, hvis det oprindelige dokument, der blev valgt, ikke blev fuldt udlignet. Når du vælger det, vises dialogboksen **Udlign posteringer**, hvor du kan vælge transaktioner til udligning.
    - **Fortryd udligning** – Denne menu vises, hvis det oprindelige dokument, der blev valgt, blev fuldt udlignet. Når du vælger det, vises dialogboksen **Fortryd udligning**, hvor du kan fortryde udligninger, der blev udført for det pågældende dokument.

