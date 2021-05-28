---
title: Opsætning af bogføring af rabatstyring
description: Dette emne beskriver, hvordan du konfigurerer posteringsprofiler. Posteringsprofiler bruges til at bestemme bogføringsposterne for beregningslinjer i Rabatstyring.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: b52a1720077c055d416f04cbbe9ec46cbcf319bc
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020405"
---
# <a name="rebate-management-posting-setup"></a>Opsætning af bogføring af rabatstyring

[!include [banner](../includes/banner.md)]

Posteringsprofiler bruges til at bestemme bogføringsposterne for beregningslinjer i Rabatstyring. Når der er valgt en posteringsprofil i aftalehovedet, gælder den for alle aftalelinjer.

Denne funktion fungerer på tværs af firmaer (juridiske enheder). Du kan angive det firma, som hensættelser skal periodiseres til, og hvilke krav der skal betales af det. Du kan også angive forskellige konti til hensættelsesdebet og afskrivningskredit pr. kildebogføringsfirma.

Hvis du vil oprette posteringsprofiler for rabatstyring til debitorer og kreditorer, skal du gå til **Rabatstyring \> Opsætning af bogføring af rabatstyring \> Posteringsprofiler til rabatstyring**. Siden **Posteringsprofiler til rabatstyring** indeholder en listerude, der viser alle eksisterende profiler. Du kan tilføje eller fjerne profiler på listen ved at bruge knapperne i handlingsruden.

I de resterende afsnit i dette emne beskrives, hvordan du kan bruge de tilgængelige felter, når du opretter eller redigerer en profil.

## <a name="posting-profile-header"></a>Overskrift i posteringsprofil

I følgende tabel beskrives de indstillinger, der er tilgængelige i hovedsektionen i hver posteringsprofil til rabatstyring.

| Felt | Betegnelse |
|---|---|
| Posteringsprofil | Angiv et entydigt navn til profilen. |
| Betegnelse | Indtast en beskrivelse af profilen. |
| Modul | Vælg den type rabatter og royalties, som profilen er tilknyttet (*Kunde* eller *Leverandør*). |
| Type | Vælg profiltypen (*Rabat* eller *Royalty*). |
| Betalingstype | <p>Dette felt bestemmer formatet for det bogførte rabatoutput.<p><p>Når feltet **Type** er angivet til *Rabat*, er følgende værdier tilgængelige:</p><ul><li>*Ingen* – Der findes ingen standardbogføringstype. Du skal derfor definere typen, når du behandler den.</li><li>*Betal ved hjælp af kreditor* – Når du bogfører rabatten, oprettes der en kreditorfaktura for den remitteringsleverandør, der er konfigureret for rabatkunden.</li><li>*Debitorfradrag* – Når du bogfører rabatten, oprettes der en debitorfradragskladde for rabatkunden.</li><li>*Debitorfradrag på momsfaktura* – Når du bogfører rabatten, oprettes der en fritekstfaktura for rabatkunden.</li><li>*Samhandelsforbrug* – Når du bogfører rabatten, oprettes der en debitorfradragskladde for rabatkunden.</li><li>*Rapportering* – Når du bogfører rabatten, oprettes der en debitorfradragskladde for rabatkunden.</li></ul><p>Når feltet **Type** er angivet til *Royalty*, er følgende værdier tilgængelige:</p><ul><li>*Ingen* – Der findes ingen standardbogføringstype. Du skal derfor definere typen, når du behandler den.</li><li>*Betal ved hjælp af kreditor* – Når du bogfører rabatten, oprettes der en kreditorfaktura for den rabatkreditorkonto, der er oprettet.</li><li>*Rapportering* – Når du bogfører rabatten, oprettes der en kreditorfaktura for den rabatkreditorkonto, der er oprettet.</li></ul><p>Du kan finde flere oplysninger i afsnittet [Betalingstyper](#payment-types) nedenfor. |
| Firma | Vælg det firma (juridisk enhed), som hensættelser skal periodiseres til, og hvilke krav der skal betales af det. |

### <a name="payment-types"></a>Betalingstyper

I følgende tabel opsummeres, hvordan de forskellige indstillinger i feltet **Betalingstype** påvirker, hvor betalinger bogføres. Betalinger kan bogføres på en debitorkonto, kreditorkonto eller remitteringskonto, afhængigt af måltransaktionen og rabattypen.

| Betalingstype | Måltransaktionstype | Rabattype | Betaling til (fakturakonto) |
|---|---|---|---|
| Betal via kreditor | kreditorfakturakladde | Debitorrabat | Kundens remitteringskreditorkonto |
| Betal via kreditor | kreditorfakturakladde | Kunderoyalty | Kreditorkonto |
| Betal via kreditor | kreditorfakturakladde | Kreditorrabat | Kreditorkonto |
| Debitorfradrag | Kassekladde | Debitorrabat | Kundekonto |
| Debitorfradrag på momsfaktura | Fritekstfaktura | Debitorrabat | Kundekonto |
| Samhandelsforbrug | Kassekladde | Debitorrabat | Kundekonto |
| Rapportering | Kassekladde | Debitorrabat | Kundekonto |
| Rapportering | kreditorfakturakladde | Kunderoyalty | Kreditorkonto |
| Rapportering | kreditorfakturakladde | Kreditorrabat | Kreditorkonto |

> [!NOTE]
> Overvej følgende punkter, når du konfigurerer [rabatstyringsaftaler](rebate-management-deals.md):
>
> - Til aftaler, hvor feltet **Afstem efter** er angivet til *Aftale*, kan du ikke bruge den dynamiske aftalekonto ved bogføring. Du skal bruge en angivet debitor- eller kreditorkonto.
> - Til aftaler, hvor feltet **Afstem efter** er angivet til *Linje*, kan du bruge en posteringsprofil, der udligner mod en dynamisk aftalekonto på aftalelinjen, fordi debitoren angives pr. aftalelinje.

## <a name="posting-fasttab"></a>Oversigtspanelet Bogføring

I følgende tabel beskrives de indstillinger, der er tilgængelige i oversigtspanelet **Bogføring** i hver posteringsprofil til rabatstyring.

| Felt | Betegnelse |
|---|---|
| Kredittype | Vælg, om du vil kreditere en finanskonto eller en debitor eller kreditor. |
| Kreditkonto | Den konto, som kreditbeløb bogføres på, når der foretages rabathensættelser. Denne konto bruges også som debetkonto, når rabatten bogføres for at kreditere debitoren. |
| Kladdenavn<br>(I sektionen **Hensættelse**) | Vælg navnet på den kladde, der skal bruges til registrering af den bogførte hensættelse. |
| Type | Vælg, om du vil bogføre rabatten til en finanskonto eller en debitor eller kreditor. Hvis feltet **Betalingstype** i hovedet er angivet til *Debitorfradrag på momsfaktura*, angives dette felt til *Debitor/Kreditor*. |
| Brug kontokilde | <p>Vælg en af følgende værdier:</p><ul><li>*Ingen* – Hvis du vælger denne værdi, skal du angive en konto i feltet **Rabatkonto**.</li><li>*Aftalekonto* – Brug den debitor- eller kreditorkonto, der er angivet på rabatlinjen. Du kan kun vælge denne værdi for aftaler, hvor feltet **Afstem efter** er angivet til *Linje*, og tilbudslinjer, hvor feltet **Kontokode** er angivet til *Tabel*. Den gælder ikke for posteringsprofiler til kunderoyalty.</li></ul> |
| Rabatkonto | Den konto, som de faktiske rabatudgifter bogføres på. |
| Kladdenavn<br>(I sektionen **Rabatstyring**) | Vælg navnet på den kladde, der skal bruges til at bogføre en kreditnota for rabatbeløbet på debitoren. Dette felt er ikke tilgængeligt, når feltet **Betalingstype** i hovedet er angivet til *Debitorfradrag på momsfaktura*. |
| Varemomsgruppe | Angiv, om rabatten er momspligtig. |
| Kladdenavn<br>(I sektionen **Afskrivning**) | Hvis den rabat, der bogføres, ikke er lig med hensættelsen, kan differencen afskrives. Vælg navnet på den kladde, der skal bruges til registrering af den bogførte afskrivning. |

## <a name="posting-by-company-fasttab"></a>Oversigtspanelet Bogføring efter firma

I oversigtspanelet **Bogføring efter firma** for hver posteringsprofil til rabatstyring kan du angive den bogføringskonto, der bruges af det enkelte firma (juridisk enhed) i gitteret.

Brug knapperne på værktøjslinjen til at tilføje firmaer i gitteret eller fjerne dem. Hver gang du føjer en række til gitteret, skal du bruge feltet **Firma** til at angive den juridiske enhed for den pågældende række. Feltet **Navn** udfyldes automatisk.

Vælg rækken for hvert firma, og angiv derefter følgende oplysninger ved at bruge felterne under gitteret:

- **Debettype** – Vælg, om du vil debitere en finanskonto eller en debitor eller kreditor.
- **Debetkonto** – Angiv den konto, som debetbeløbet bogføres på, når der foretages rabathensættelser.
- **Hovedkonto** – Vælg hovedkontoen til afskrivninger.
