---
title: Konfigurere betalingsmåden for debitorkonti for B2B-e-handelswebsteder
description: Dette emne beskriver, hvordan du kan konfigurere debitorkontobetalingsmåden for business-to-business (B2B)-e-handelswebsteder.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 628f3b3b2d86154190dfdcc82b8b391c2facce103f607519514c65b5fba26653
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738047"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Konfigurere betalingsmåden for debitorkonti for B2B-e-handelswebsteder

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du kan konfigurere debitorkontobetalingsmåden for business-to-business (B2B)-e-handelswebsteder.

Detailhandlende kan acceptere forskellige former for betalinger for de produkter og tjenester, de sælger i en e-handelskanal. De enkelte betalingstyper, som en detailhandlende accepterer, skal konfigureres i Microsoft Dynamics 365 Commerce, når systemet konfigureres. Betalingsmåden for debitorkontoen (eller "akonti") skal understøttes på B2B-e-handelswebsteder. 

## <a name="prerequisites"></a>Forudsætninger

1. Tilføj debitorkontobetalingsmåden i Commerce Headquarters.
2. Tilknyt betalingsmåden for debitorkontoen til e-handelskanalen.
3. Sørg for, at **Tillad på konto** er aktiveret for kunden i **Retail og Commerce \> Kunder \> Alle kunder \> Betalingsstandarder** i Commerce Headquarters. Sørg også for, at parametrene for **kreditmaksimum** er angivet korrekt for kunden i **Retail og Commerce \> Kunder \> Alle kunder \> Kredit og rykkere** i Commerce Headquarters. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Aktivere betalingsmåden for debitorkonti i Commerce-webstedsgenerator 

Følg disse trin for at aktivere betalingsmåden for debitorkonti i Commerce-webstedsgenerator.

1. Gå til **Webstedsindstillinger \> Udvidelser**.
1. Angiv egenskaben **Aktiver debitorkontobetalinger** til **Aktiveret for B2B-debitorer**. 
1. Vælg **Gem og udgiv**.

> [!NOTE]
> De nye indstillinger for webstedet træder først i kraft, når app.settings.json-filen er opdateret. Yderligere oplysninger finder du i [SDK- og modulbiblioteksopdateringer](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Aktivere betalingsmetoden for debitorkontoen på siden til betaling ved kassen for E-handelswebstedet for B2B

Følg disse trin for at aktivere betalingsmetoden for debitorkontoen på siden til betaling ved kassen for E-handelswebstedet for B2B.

1. I Commerce site builder skal du finde og redigere den side eller det system til betaling ved kassen, som indeholder modulet til betaling ved kassen for webstedet B2B-e-handel.
1. I **Container til betalingssektion**-kassen skal du vælge **Tilføj modul** og derefter tilføje et **Debitorkontobetaling**-modul.
1. Placer **Debitorkontobetaling**-modulet ved at vælge ellipsen (**...**) og derefter vælge **Flyt op** eller **Flyt ned** efter behov.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Bekræft, at betalingsmetoden for debitorkonti er aktiveret og udgivet

Følg disse trin for at bekræfte, at betalingsmetoden for debitorkonti er aktiveret.

1. Log på e-handelswebsted.
1. Tilføjet produkt til indkøbsvognen.
1. Gå til betalingssiden. Du bør se den nye betalingsmåde for **Debitorkonto**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere et B2B-e-handelswebsted](set-up-b2b-site.md)

[Oprette organisationsmodelhierarkier for B2B-organisationer](org-model.md)

[Administrere forretningspartnerbrugere på B2B-e-handelswebsteder](manage-b2b-users.md)

[Angive produktantalsgrænser for B2B-e-handelswebsteder](quantity-limits.md)

[Opdateringer til SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]