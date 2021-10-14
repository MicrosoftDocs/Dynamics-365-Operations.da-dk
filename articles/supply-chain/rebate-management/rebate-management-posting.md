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
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: edffccfec552d90ce704190b4be0b4594964fa81
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574323"
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
| Modul | Vælg det modul, som rabatter og royalties for profilen er tilknyttet (*Kunde* eller *Leverandør*). |
| Type | Vælg profiltypen (*Rabat* eller *Royalty*). |
| Betalingstype | <p>Dette felt bestemmer formatet for det bogførte rabatoutput.<p><p>Når feltet **Type** er angivet til *Rabat*, er følgende værdier tilgængelige:</p><ul><li>*Betal ved hjælp af kreditor* – Når du bogfører en debitorrabat, oprettes der en kreditorfaktura for den remitteringsleverandør, der er konfigureret for rabatkunden. Når du bogfører en kreditorrabat, oprettes der en kreditorfaktura for den rabatkreditorkonto.</li><li>*Debitorfradrag* – Når du bogfører rabatten, oprettes der en debitorfradragskladde for rabatkunden.</li><li>*Debitorfradrag på momsfaktura* – Når du bogfører rabatten, oprettes der en fritekstfaktura for rabatkunden.</li><li>*Samhandelsforbrug* – Når du bogfører rabatten, oprettes der en debitorfradragskladde for rabatkunden.</li><li>*Rapportering* – Når du bogfører rabatten, oprettes der en debitorfradragskladde for rabatkunden.</li></ul><p>Når feltet **Type** er angivet til *Royalty*, er følgende værdier tilgængelige:</p><ul><li>*Betal ved hjælp af kreditor* – Når du bogfører rabatten, oprettes der en kreditorfaktura for den rabatkreditorkonto, der er oprettet.</li><li>*Rapportering* – Når du bogfører rabatten, oprettes der en kreditorfaktura for den rabatkreditorkonto, der er oprettet.</li></ul><p>Du kan finde flere oplysninger i afsnittet [Betalingstyper](#payment-types) nedenfor. |
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
> - Til aftaler, hvor feltet **Afstem efter** er angivet til *Linje*, kan du bruge en posteringsprofil, der udligner mod en dynamisk aftalekonto på aftalelinjen, fordi debitoren eller kreditoren angives pr. aftalelinje.

## <a name="posting-fasttab"></a>Oversigtspanelet Bogføring

I følgende tabel beskrives de indstillinger, der er tilgængelige i oversigtspanelet **Bogføring** i hver posteringsprofil til rabatstyring.

| Felt | Betegnelse |
|---|---|
| Kredittype | Vælg, om du vil kreditere en finanskonto eller en debitor. Hvis feltet **Betalingstype** i overskriften er angivet til *Debitorfradrag på momsfaktura*, angives dette felt til *Finanskonto*. Dette felt angives til *Finanskonto* for kreditorrabatter. |
| Kreditkonto | Vælg den konto, som kreditbeløb bogføres på, når der foretages rabathensættelser. Denne konto bruges også som modkonto, når rabatten bogføres for at kreditere debitoren eller debitere kreditoren. |
| Kladdenavn<br>(I sektionen **Hensættelse**) | Vælg navnet på den kladde, der skal bruges til registrering af den bogførte hensættelse. |
| Type | Vælg, om du vil bogføre rabatten til en finanskonto eller en debitor eller kreditor. Hvis feltet **Betalingstype** i hovedet er angivet til *Debitorfradrag på momsfaktura*, angives dette felt til *Debitor/Kreditor*. |
| Brug kontokilde | <p>Vælg en af følgende værdier:</p><ul><li>*Fast konto* – Hvis du vælger denne værdi, skal du angive en konto i feltet **Rabatkonto**.</li><li>*Aftalelinjekonto* – Brug den debitor- eller kreditorkonto, der er angivet på rabatlinjen. Du kan kun vælge denne værdi for aftaler, hvor feltet **Afstem efter** er angivet til *Linje*, og tilbudslinjer, hvor feltet **Kontokode** er angivet til *Tabel*. Den gælder ikke for posteringsprofiler til kunderoyalty eller kreditorrabatter, der er baseret på salgsordrer.</li></ul> |
| Rabatkonto | Den konto, som de faktiske rabatudgifter bogføres på. |
| Kladdenavn<br>(I feltgruppen **Rabatstyring**) | Vælg navnet på den kladde, der skal bruges til at bogføre en kreditnota for rabatbeløbet for debitoren eller kreditoren. Dette felt er ikke tilgængeligt, når feltet **Betalingstype** i hovedet er angivet til *Debitorfradrag på momsfaktura*. For debitorrabatter vil kladdenavne af kladdetypen *Daglig* være tilgængelige. For debitorroyalties og kreditorrabatter er kladdenavnene for kladdetypen *Kreditorfaktura, registrering* tilgængelige. |
| Varemomsgruppe | Angiv, om rabatten er momspligtig. |
| Kladdenavn<br>(I feltgruppen **Afskrivning**) | Hvis den rabat, der bogføres, ikke er lig med hensættelsen, kan differencen afskrives. Vælg navnet på den kladde, der skal bruges til registrering af den bogførte afskrivning. |

## <a name="posting-by-company-fasttab"></a>Oversigtspanelet Bogføring efter firma

I oversigtspanelet **Bogføring efter firma** for hver posteringsprofil til rabatstyring kan du angive den bogføringskonto, der bruges af det enkelte firma (juridisk enhed) i gitteret.

Brug knapperne på værktøjslinjen til at tilføje firmaer i gitteret eller fjerne dem. Hver gang du føjer en række til gitteret, skal du bruge feltet **Firma** til at angive den juridiske enhed for den pågældende række. Feltet **Navn** udfyldes automatisk.

Vælg rækken for hvert firma, og angiv derefter følgende oplysninger ved at bruge felterne under gitteret:

- **Debettype** – Vælg, om du vil debitere en finanskonto eller en kreditor. Dette felt angives til *Finanskonto* for debitorrabatter og royalties.
- **Debetkonto** – Angiv den konto, som debetbeløbet bogføres på, når der foretages rabathensættelser.
- **Hovedkonto** – Vælg hovedkontoen til afskrivninger.
