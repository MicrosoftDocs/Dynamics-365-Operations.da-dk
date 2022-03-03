---
title: Konfigurere betalingsmåden for debitorkonti for B2B-e-handelswebsteder
description: I dette emne beskrives, hvordan du kan konfigurere debitorkontobetalingsmåden i Microsoft Dynamics 365 Commerce. Det beskriver også, hvordan kreditmaks. påvirker registrering af acontobetaling på business-to-business (B2B)-e-handelswebsteder.
author: josaw1
ms.date: 02/16/2022
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
ms.openlocfilehash: 0366f7b51ac138cc7305f98d5607c554440e6d34
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323349"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Konfigurere betalingsmåden for debitorkonti for B2B-e-handelswebsteder

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du kan konfigurere debitorkontobetalingsmåden i Microsoft Dynamics 365 Commerce. Det beskriver også, hvordan kreditmaks. påvirker registrering af acontobetaling på business-to-business (B2B)-e-handelswebsteder.

Detailhandlende kan acceptere forskellige former for betalinger for de produkter og tjenester, de sælger i en e-handelskanal. De enkelte betalingstyper, som en detailhandlende accepterer, skal konfigureres i Dynamics 365 Commerce, når systemet konfigureres. Betalingsmåden for debitorkontoen (eller "aconto") skal understøttes på B2B-e-handelswebsteder. 

## <a name="prerequisites"></a>Forudsætninger

1. Tilføj debitorkontobetalingsmåden i Commerce Headquarters.
2. Tilknyt betalingsmåden for debitorkontoen til e-handelskanalen.
3. Sørg for, at egenskaben **Tillad aconto** er aktiveret for kunden i **Retail og Commerce \> Kunder \> Alle kunder \> Betalingsstandarder** i Commerce-hovedkontoret.

    > [!NOTE]
    > Hvis alle kunder skal have mulighed for at få betalingsmåden aconto aktiveret, kan du angive **Tillad aconto**-egenskaben til **Ja** for standardkunden for den kanal, der er tilknyttet B2B-webstedet. 

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

## <a name="work-with-credit-limits"></a>Arbejde med kreditmaksimum

Når egenskaberne for debitorkontobetalinger er aktiveret på B2B-webstedet, ønsker organisationer normalt at få vist oplysninger om kreditmaksimum og saldi for kreditmaksimum under ordreregistreringsprocessen. En kundes kreditmaksimum defineres af egenskaben **Kreditmaks.** i oversigtspanelet **Kredit og rykkere** for debitorposten i Commerce-hovedkontoret. Men i B2B-scenarier skal en ordre, som en kunde afgiver, ofte faktureres til kontoen hos den organisation, som kunden tilhører. Du skal derfor angive egenskaben **Fakturakonto** i oversigtspanelet **Faktura og levering** for debitorposten til organisationens debitorkonto-id. Når kunden derefter afgiver en ordre på B2B-webstedet, faktureres ordren til organisationen. B2B-webstedet bruger også organisationens kreditmaksimum i stedet for det kreditmaksimum, der er angivet i debitorposten.

Beregningen og saldoen for kreditmaksimum, der vises på B2B-webstedet, afhænger af indstillingen af egenskaben **Kreditmaks.type** i Commerce-hovedkontoret. Placeringen af denne egenskab varierer, afhængigt af om funktionen **Kreditstyring** er aktiveret i arbejdsområdet **Funktionsstyring**:

- Hvis funktionen **Kreditstyring** er aktiveret, findes egenskaben i oversigtspanelet **Kreditmaks.** på **Kredit og rykkere \> Opsætning \> Kredit og Rykkerparametre \> Kredit**. 
- Hvis funktionen **Kreditstyring** er deaktiveret, findes egenskaben under **Kreditvurdering** i **Debitor \> Konfiguration \> Debitorparametre \> Kreditvurdering**.

De værdier, der understøttes af egenskaben **Kreditmaks.type**, er **Ingen**, **Saldo**, **Saldo + følgeseddel eller produktkvittering** og **Saldo + Alle**. Yderligere oplysninger om disse værdier finder du i [værdierne for kreditmaksimumtyper](/dynamics365/supply-chain/sales-marketing/credit-limits-customers).

> [!NOTE]
> Det anbefales, at du angiver egenskaben **Kreditmaks.type** til **Saldo + følgeseddel eller produktkvittering**, så åbne salgsordrer ikke bidrager til saldoberegningen. Hvis kunderne derefter kommer med fremtidige ordrer, behøver de ikke at være bange for, at disse ordrer påvirker deres aktuelle saldo.

En anden egenskab, der påvirker acontobestillinger, er egenskaben **Tvungen kreditmaksimum**, der findes i oversigtspanelet **Kredit og rykkere** for debitorposten. Hvis du angiver denne egenskab til **Ja** for bestemte debitorer, kan du tvinge systemet til at kontrollere deres kreditmaksimum, selvom egenskaben **Kreditmaksimumtype** er angivet til **Ingen** for at angive, at kreditmaksimum ikke skal kontrolleres for nogen debitorer.

Aktuelt har B2B-websteder, hvor egenskaben **Tvungen kreditmaksimum** er aktiveret, yderligere funktioner. Hvis egenskaben er aktiveret i en debitorpost, når kunden afgiver en ordre, forhindrer B2B-webstedet dem i at bruge acontobetalingsmåden til at betale mere end den resterende kreditsaldo. Hvis kundens resterende kreditsaldo f.eks. er $1.000, men ordren er $1.200, kan kunden kun betale $1.000 ved hjælp af acontometoden. De skal bruge en anden betalingsmåde for at betale saldoen. Hvis egenskaben **Obligatorisk kreditmaksimum** deaktiveres for en debitorpost, kan debitoren betale et vilkårligt beløb ved hjælp af acontobetalingsmåden. Men selvom en kunde kan afgive ordrer, vil systemet ikke tillade, at disse ordrer opfyldes, hvis de overskrider kreditmaksimum. Hvis du skal kontrollere kreditmaksimum for alle de debitorer, der er berettiget til acontobetalinger, anbefales det, at du angiver egenskaben **Kreditmaksimumtype** til **Saldo + følgeseddel eller produktseddel** og egenskaben **Tvungen kreditmaksimum** til **Nej**.

Modulet **Kredit og rykkere** har nye funktioner til kreditstyring. Hvis du vil aktivere disse egenskaber, skal du aktivere funktionen **Kreditstyring** i arbejdsområdet **Funktionsstyring**. En af de nye egenskaber gør det muligt at sætte salgsordrer på hold baseret på blokeringsregler. Kreditchefen kan derefter frigive eller afvise ordrerne efter nærmere analyse. Funktionen til at sætte salgsordrer på hold gælder dog ikke for Commerce-ordrer, da salgsordrer ofte indeholder en forudbetaling, og funktionen **Kreditstyring** ikke fuldt ud understøtter forudbetalingsscenarier. 

Uanset, om funktionen **Kreditstyring** er aktiveret, vil salgsordrerne ikke blive sat på hold, hvis en debitorsaldo kommer over kreditmaksimum under ordreopfyldelse. I stedet genererer Commerce enten en advarsel eller en fejlmeddelelse afhængigt af værdien af feltet **Meddelelse ved overskridelse af kreditmaks.** i oversigtspanelet **Kreditmaks**.

Egenskaben **Udeluk fra kreditstyring**, der forhindrer, at Commerce-salgsordrer går på hold, findes i salgsordrehovedet (**Detail og handel \> Kunder \> Alle salgsordrer**). Hvis denne egenskab er angivet til **Ja** (standardværdien) for Commerce-salgsordrer, ekskluderes ordrerne fra arbejdsgangen på hold i kreditstyring. Bemærk, at selvom egenskaben hedder **Udeluk fra kreditstyring**, bruges det definerede kreditmaksimum stadig i forbindelse med ordreopfyldelse. Ordrerne vil dog ikke blive sat på hold.

Muligheden for at sætte Commerce-salgsordrer på hold baseret på blokeringsregler er planlagt til fremtidige Commerce-versioner. Indtil den understøttes, kan du tilpasse følgende XML-filer i Visual Studio-løsningen, hvis du skal tvinge Commerce-salgsordrer til at gennemgå de nye flow i kreditstyring. Rediger logikken i filerne, så flaget **CredManExcludeSalesOrder** angives til **Nej**. På denne måde angives egenskaben **Udeluk fra kreditstyring** til **Nej** som standard for Commerce-salgsordrer.

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

Bemærk, at hvis flaget **CredManExcludeSalesOrder** er angivet til **Nej**, og en B2B-kunde kan købe hos butikker ved hjælp af POS-programmet, kan bogføringen af cash and carry-transaktioner mislykkes. Der er f.eks. en blokeringsregel for kontantbetalingstypen, og B2B-kunden har købt nogle varer i butikken ved hjælp af kontanter. I dette tilfælde kan den resulterende salgsordre ikke faktureres, da den bliver sat på hold. Derfor mislykkes bogføringen. Derfor anbefales det, at du gennemfører en totaltest, når du har implementeret denne tilpasning.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette et B2B-e-handelswebsted](set-up-b2b-site.md)

[Administrere B2B-forretningspartnere ved hjælp af kundehierarkier](partners-customer-hierarchies.md)

[Administrere forretningspartnerbrugere på B2B-e-handelswebsteder](manage-b2b-users.md)

[Angive produktantalsgrænser for B2B-e-handelswebsteder](quantity-limits.md)

[Opdateringer til SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
