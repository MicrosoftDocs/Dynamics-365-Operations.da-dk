---
title: Registrere leasingaftaler i udenlandsk valuta
description: Dette emne forklarer, hvordan du registrerer leasingaftaler i andre valutaer end regnskabs- eller rapporteringsvalutaen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 989977fd038ecc6e3276085d795192f5dcab42eb
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881584"
---
# <a name="record-leases-in-foreign-currencies"></a>Registrere leasingaftaler i udenlandsk valuta

[!include [banner](../includes/banner.md)]

Der oprettes aktivleasingkonti for leasingaftaler, der er i andre valutaer end regnskabsvalutaen eller rapporteringsvalutaen på siden **Opsætning af Finans**. Alle rettigheder skal angives i transaktionsvalutaen. De skal med andre ord angives i den valuta, der er angivet i leasingkontrakten. Dette emne forklarer, hvordan du registrerer leasingaftaler i andre valutaer end regnskabs- eller rapporteringsvalutaen.

Hvis du angiver en leasingaftale i en fremmed valuta, afskrives ROU-rettighedsaktivet i både regnskabsvalutaen og rapporteringsvalutaen. Disse valutaer konfigureres på siden **Opsætning af Finans**. Denne funktionsmåde bruges også i anlægsaktiver. Når du opretter en leasingaftale i udenlandsk valuta, skal du vælge transaktionsvalutaen i feltet **Valuta**.

Valutakursen for regnskabsvalutaen er standardværdien i feltet **Regnskabsvalutakurs**. Valutakursen for rapporteringsvalutaen er standardværdien i feltet **Rapporteringsvalutakurs**. Disse valutakurser var gældende på ikrafttrædelsesdatoen for leasingaftalen. Felterne **Regnskabsvalutakurs** og **Valutakurs for rapportering** findes i oversigtspanelet **Finans- og rapportudvekslingsoplysninger** på siden **Leasingoplysninger**.

1. Marker afkrydsningsfeltet **Fast kurs** for at tilsidesætte den valutakurs, der er angivet automatisk, og angiv derefter den nye sats.
2. Angiv de oplysninger, der kræves til leasingaftalen, i de andre felter, og vælg derefter **Opret planer**.
3. På siden **Leasingdetaljer** skal du vælge **Kartoteker**.
4. På siden **Leasingkartotek** skal du under fanen **Finans-og rapporteringskursoplysninger** kontrollere værdierne i **Regnskabsvalutaens indledende brugsretsaktiv** og felterne **Rapporteringsvalutaens indledende brugsretsaktiv**. Hvert af disse felter viser det oversatte ROU-aktivsaldo i den tilsvarende valuta. Disse felter opdateres, når du ændrer økonomiske oplysninger. Vælg **Opret planer**, før du bekræfter betalingsplanen.

    Den oprindelige genkendelseskladdepostering registrerer det ROU-aktiv, der bruger de valutakurser, der er angivet for leasingaftalen. Kladdeposten indeholder også værdierne fra felterne **Regnskabsvalutaen indledende brugsretsaktiv** og **Rapporteringsvalutaens indledende brugsretsaktiv**.

## <a name="subsequent-measurement-for-foreign-currency-leases"></a>Efterfølgende måling af leasingaftaler med fremmed valuta

Afskrivningsplanen viser de forventede afskrivningsudgiftsbeløb i rapporteringsvalutaen, regnskabsvalutaen og transaktionsvalutaen.

Hvis du vil have vist ROU-aktivsaldi og afskrivningsbeløb i enten rapporteringsvalutaen eller regnskabsvalutaen, skal du åbne siden **Afskrivningsplan for aktiver** og markere afkrydsningsfeltet **Vis regnskabsvalutabeløb** eller **Vis rapporteringsvalutabeløb**.

Når du opretter afskrivningskladdeposteringerne i forhold til en leasingaftale, der er angivet i en fremmed valuta, bruger posten de valutakurser, der vises på leasingaftalen. Den bruger også værdierne fra felterne **Regnskabsvalutaen indledende brugsretsaktiv** og **Rapporteringsvalutaens indledende brugsretsaktiv**.

Det endelige afskrivningsbeløb for udligningsudgifter kan beregnes ved hjælp af en lidt anden valutakurs, så ROU aktivet afskrives fuldt ud i regnskabsvalutaen og rapporteringsvalutaen.

Hvis rettigheden er blevet genklassificeret som **Udskudt leje**, fjerner systemet automatisk valutakurserne for regnskabs- og rapporteringsvaluta, hvis de allerede er defineret.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
