---
title: "Indstillinger for anlægsaktivtransaktioner"
description: "I denne artikel beskrives de forskellige tilgængelige metoder til oprettelse af anlægsaktivtransaktioner."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3d16b43eda0157e63a0d30fe806dac9a359d5fa4
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="fixed-asset-transaction-options"></a>Indstillinger for anlægsaktivtransaktioner

[!include[banner](../includes/banner.md)]


I denne artikel beskrives de forskellige tilgængelige metoder til oprettelse af anlægsaktivtransaktioner.

Du kan oprette anlægsaktiver til integration med Kreditor, Debitor, Indkøb og forsyning samt Finans. Du kan også overføre varer i Lagerstyring til Anlægsaktiver, hvis du vil bruge disse varer internt.

## <a name="accounts-payable"></a>Kreditor
Du kan angive transaktioner for anlægsaktiver på siden Kladdebilag. Denne side kan åbnes fra siden Fakturajournal. Du kan også åbne siden Kladdebilag fra siden Fakturagodkendelseskladde. Vælg Anlægsaktiv i feltet Modkontotype. Vælg derefter et anlægsaktivnummer i feltet Modkonto. Angiv værdier i felterne Transaktionstype og Kartotek under fanen Anlægsaktiver.

## <a name="accounts-receivable"></a>Debitor
Du kan angive transaktioner for anlægsaktiver på siden Fritekstfaktura.  Vælg et linjeelement i gitteret Fakturalinjer på siden Fritekstfaktura. Klik på oversigtspanelet Linjedetaljer. Angiv anlægsaktivnummeret og kartoteket for kassationsposteringen. I fritekstfakturaer er posteringstypen for anlægsaktiver altid Kassation – salg.

## <a name="procurement-and-sourcing"></a>Indkøb og forsyning
Du kan angive transaktioner for anlægsaktiver på siden Indkøbsordre. Angiv de nødvendige oplysninger for at oprette en indkøbsordre, og klik derefter på OK. Klik på oversigtspanelet Linjedetaljer på siden Indkøbsordre. Angiv derefter oplysninger om anlægsaktivet under fanen Anlægsaktiver. 

Hvis du vil bogføre en anskaffelsespostering for et eksisterende anlægsaktiv, skal du angive anlægsaktivnummer, kartotek og posteringstype. Anlægsaktivet kan ikke bogføres, hvis disse oplysninger mangler. Hvis du vil bogføre en anskaffelsespostering for et nyt anlægsaktiv, skal du vælge indstillingen Nyt anlægsaktiv? og derefter vælge anlægsaktivgruppen, som det nye anlæg skal tildeles til. Men der er ingen tilgængelige anlægsaktivfelter for en linje, hvis elementet er en lagermodelgruppe, der bruger lagermodellen Standardomkostning. Desuden bestemmer de indstillinger, der er defineret på siden Anlægsaktivparametre, om du kan bogføre anskaffelsesposteringer fra indkøbsmoduler. 

Når en indkøbsordre eller Lager til anlægsaktivkladde bruges til at anskaffe anlægsaktiver, påvirkes lagerværdien.

## <a name="general-ledger"></a>Finans
Alle posteringstyper for anlægsaktiver kan bogføres på siden Finanskladde. Du kan også bruge kladder i Anlægsaktiver til at bogføre anlægsaktivposteringer.

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Indstillinger for angivelse af typer af anlægsaktivposteringer


| Transaktionstype                    | Modul                   | Indstilling                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Anskaffelse, Anskaffelsesregulering | Anlægsaktiver             | Anlægsaktiver, Lager til anlægsaktiver   |
|                                     | Finans           | Finanskladde                           |
|                                     | Kreditor         | Fakturajournal, Fakturagodkendelseskladde |
|                                     | Indkøb og forsyning | Indkøbsordre                            |
| Afskrivning                        | Anlægsaktiver             | Anlægsaktiver                              |
|                                     | Finans           | Finanskladde                           |
| Kassation                            | Anlægsaktiver             | Anlægsaktiver                              |
| ** **                               | Finans           | Finanskladde                           |
| ** **                               | Debitor      | Fritekstfaktura                         |



Du kan finde flere oplysninger under [Integration af anlægsaktiver](fixed-asset-integration.md).




