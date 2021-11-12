---
title: Modulet Ordreopslag
description: Dette emne omhandler ordreopslagsmodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 0ae5c8a2eea84a9aa707f7c2f6f29950f2f48faa
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675111"
---
# <a name="order-lookup-module"></a>Modulet Ordreopslag

[!include [banner](includes/banner.md)]

Dette emne omhandler ordreopslagsmodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.

Ordreopslagsmodulet indeholder en form, som kunder kan bruge til at slå ordrer op, som de har placeret på et e-handelswebsted. Det bruges som en del af funktionen [Aktiver ordreopslag for gæsteudbetaling](order-lookup-guest.md). Ordreopslagsmodulet kan bruges til at slå ordrer op, der er sendt via en e-handelswebsted, POS (Retail POS) eller et callcenter. Formen kan hente ordrer, der både er sendt af gæstebrugere og registrerede brugere.

I følgende illustration vises et eksempel på den form, der gengives af ordreopslagsmodulet. Når kunder udfylder formularen og vælger **Find din ordre**, bliver de omdirigeret til siden med ordredetaljer.

![Formen Til ordreopslagsmodulet på en side.](./media/OrderLookup_module.PNG)

## <a name="order-lookup-module-properties"></a>Modulet egenskaber til ordreopslag

| Egenskabsbetegnelse     | Værdi     | Betegnelse |
|-------------------|-----------|-------------|
| Overskrift           | Tekst      | Den overskrift, der vises øverst i formen (f.eks. "Find din ordre"). |
| RTF         | RTF | Valgfri forklaring, der vises under overskriften. |
| Typen ordrestatus | Enum      | <p>Vælg den type oplysninger, som formen skal anmode om fra kunden ud over ordrebekræftelses-id'et. Følgende værdier understøttes i øjeblikket:</p><ul><li><b>E-mail</b> – Formen indeholder et felt, hvor debitorer kan angive den e-mailadresse, de brugte, da de afgav ordren.</li><li><b>Ingen</b> – Formen anmoder ikke om yderligere oplysninger end ordrebekræftelses-id.</li></ul> |

## <a name="add-an-order-lookup-module-to-a-page"></a>Føj et ordreopslagmodul til en side

Ordreopslagsmodulet kan føjes til brødteksten på enhver side på e-handelswebstedet. Hvis du vil bruge ordreopslagsmodulet til at aktivere ordreopslag for gæsteudbetaling, skal du sørge for at føje den til en side, der ikke kræver, at brugeren er logget på. Hvis du vil finde indstillingen For en sides **Kræver log på?** i trævisningen Commerce site builder, skal du vælge **standardsiden (Obligatorisk)** og se nederst i højre rude.

## <a name="additional-resources"></a>Yderligere ressourcer

[Aktivere ordreopslag for gæsteudbetaling](order-lookup-guest.md)

[Modulbibliotek, oversigt](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
