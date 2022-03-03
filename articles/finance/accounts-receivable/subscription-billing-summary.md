---
title: Oversigt over abonnementsfakturering
description: I dette emne beskrives abonnementsfakturering i Microsoft Dynamics 365 Finance.
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: b94ac36e49d55ad42909877d77903cd40cb22cbe
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182677"
---
# <a name="subscription-billing-overview"></a>Oversigt over abonnementsfakturering

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Abonnementsfakturering giver organisationer mulighed for at administrere salgsmuligheder for abonnementsindtægter og tilbagevendende fakturering via faktureringsplaner. Det er nemt at administrere komplekse pris- og faktureringsmodeller og indtægtsfordeling, og de faktureres og registreres på linjeniveau. Fordeling af omsætning for flere elementer gør det muligt for fordeling af omsætning at overholde internationale regnskabsstandarder (International Financial Reporting Standard 15 \[IFRS 15\]) og almindeligt anerkendte regnskabsprincipper (US GAAP)-standarder (Accounting Standards Codification Topic 606 \[ASC 606\]).

Løsningen indeholder tre moduler, der kan bruges uafhængigt. Alternativt kan alle tre moduler bruges sammen.

- **Fakturering af tilbagevendende kontrakter** – Dette modul giver mulighed for tilbagevendende fakturering og prisstyring for at kunne styre pris- og faktureringsparametre, kontraktfornyelse og konsolideret fakturering.
- **Indtægts- og udgiftsudskydelser** – Dette modul eliminerer manuelle processer og afhængigheder af eksterne systemer ved at administrere indtægter og aktivere indsigt i realtid i månedlige tilbagevendende indtægter.
- **Indtægtsfordeling for flere elementer** – Dette modul hjælper med overholdelse af angivne standarder for omsætning ved at håndtere prissætning og indtægtsfordeling på tværs af flere varer.

Abonnementsfakturering aktiveres via **Funktionsstyring**. Den kan dog ikke bruges med funktionen **Indtægtsføring**. Du skal derfor deaktivere denne funktion, før du aktiverer abonnementsfakturering.

1. I arbejdsområdet **Funktionsstyring** skal du angive **Indtægtsføring** i filteret under fanen **Alle** og derefter vælge funktionsnavnet som filter.
2. Vælg funktionen **Indtægtsføring**, og vælg derefter knappen **Deaktiver**.
3. Angiv **Abonnementsfakturering** i filteret **Funktionsnavn**, og vælg derefter modulfilteret.
4. Vælg funktionen **Abonnementsfakturering**, og vælg derefter **Aktivér**.
5. Vælg et af de tre moduler på den forrige liste, og vælg derefter **Aktivér**. Gentag dette trin for hvert af de to andre moduler.

    > [!IMPORTANT]
    > Funktionen **Abonnementsfakturering** skal være aktiveret, før du kan aktivere et af de tre moduler.
