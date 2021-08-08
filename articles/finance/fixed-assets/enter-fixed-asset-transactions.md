---
title: Posteringsindstillinger for anlægsaktiv
description: I dette emne beskrives de forskellige tilgængelige metoder til oprettelse af anlægsaktivtransaktioner.
author: ShylaThompson
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: roschlom
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f9cd8846688e6b70f3ac2034caa1a9e3015355e
ms.sourcegitcommit: f9b40df70a77136529fbc790325ed657eb203731
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/20/2021
ms.locfileid: "6645366"
---
# <a name="fixed-asset-transaction-options"></a>Posteringsindstillinger for anlægsaktiv

[!include [banner](../includes/banner.md)]

I dette emne beskrives de forskellige tilgængelige metoder til oprettelse af anlægsaktivtransaktioner.

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

### <a name="options-for-entering-fixed-asset-transaction-types"></a>Indstillinger for angivelse af typer af anlægsaktivposteringer


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

Afskrivningsperiodernes restværdi for anlægsaktivet opdateres ikke, når en afskrivningstransaktionstypes kladdelinje oprettes manuelt eller importeres via en dataenhed. Denne værdi opdateres, når afskrivningsforslagsprocessen bruges til at oprette kladdelinjen.

Du kan finde flere oplysninger under [Integration af anlægsaktiver](fixed-asset-integration.md).

### <a name="transactions-that-require-different-voucher-numbers"></a>Transaktioner, der kræver forskellige bilagsnumre

Følgende anlægsaktivtransaktioner vil bruge forskellige bilagsnumre:

- Der foretages en yderligere anskaffelse til et aktiv, og "catch-up"-afskrivning beregnes.
- Et aktiv opdeles.
- En parameter til at beregne afskrivning på kassation aktiveres, og derefter kasseres anlægsaktivet.
- Et aktivs servicedato ligger før anskaffelsesdatoen. Derfor bogføres en afskrivningsregulering.

> [!NOTE]
> Når du indtaster transaktioner, skal du kontrollere, at alle transaktioner gælder for det samme anlægsaktiv. Et bilag bogføres ikke, hvis det indeholder mere end ét anlægsaktiv, selvom feltet **Nyt bilag** kun er angivet som **Ét bilagsnummer** på siden **Kladdenavne** i Finans. Hvis du medtager mere end ét anlægsaktiv i bilaget, modtager du meddelelsen "Der kan kun være én anlægsaktivpostering pr. bilag", og du kan ikke bogføre bilaget.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
