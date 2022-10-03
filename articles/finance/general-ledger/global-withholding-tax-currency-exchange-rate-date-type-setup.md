---
title: Aktivere konfigurationen af den globale valutakurs for A-skat og datotype
description: Denne artikel forklarer, hvordan du aktiverer den globale konfiguration af valutakurstypen for A-skat og datotype.
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9db9cf41381b8b4de7dffe1c755a7df805a003ea
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573218"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>Aktivere konfigurationen af den globale valutakurs for A-skat og datotype

[!include[banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du aktiverer den globale konfiguration af valutakurstypen for A-skat og datotype. Du kan nu vælge en bestemt valutakurstype og datotypen til beregning af valutakursen for valutaen i A-skat. Disse valg bestemmer den valutakurs i udenlandsk valuta, der bruges til at beregne beløbet for A-skat i valutaen for A-skat i betalingstransaktionerne.

Denne funktionalitet er tilgængelig i Microsoft Dynamics 365 Finance version 10.0.29 og nyere.

1. Gå til **Skat** \> **Konfiguration** \> **Parametre** \> **Finansparametre**.
2. Angiv indstillingen **Aktivér avanceret valuta for A-skat** til **Ja** under fanen **A-skat**.
3. Vælg en valutakurstype for valutaen til A-skat i feltet **Valutakurstype**.
4. Vælg en beregningsdatotype i feltet **Beregningsdatotype**, der bestemmer valutakursen for A-skat:

    - **Betalingsdato** – Bestem valutakursen på basis af bogføringsdatoen for betalingskladden.
    - **Fakturadato** – Bestem valutakursen på basis af fakturadatoen for fakturakladden. Hvis fakturadatoen for bilaget er tom, bruges fakturabogføringsdatoen. 
    - **Dokumentdato** – Bestem valutakursen på basis af dokumentdatoen for betalingskladden. Hvis dokumentdatoen for bilaget er tom, bruges betalingsdatoen.

5. Vælg **Gem**.

Hvis transaktionsvalutaen er forskellig fra den valuta for A-skat, der er defineret i koden for A-skat, beregnes beløbet i valutaen for A-skat ud fra transaktionsvalutaen på baggrund af de foregående indstillinger og registreres i de bogførte transaktioner for A-skat.
