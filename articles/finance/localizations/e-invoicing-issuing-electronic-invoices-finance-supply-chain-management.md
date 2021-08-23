---
title: Udstede elektroniske fakturaer i Finance og Supply Chain Management
description: Dette emne beskriver, hvordan du udsteder elektroniske fakturaer i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management ved hjælp af Elektronisk fakturering.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 24909c2a2505724c159e939535c1d57cb66e48629862bebb32b3d72c0eb06c97
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752120"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Udstede elektroniske fakturaer i Finans og Supply Chain Management

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du udsteder elektroniske fakturaer i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management ved hjælp af Elektronisk fakturering.


## <a name="feature-activation"></a>Funktionsaktivering

Hvis du skal udstede elektroniske fakturaer via Elektronisk fakturering, skal du først at aktivere funktionsreferencen i Finance og Supply Chain Management.

Hver funktion svarer til en bestemt funktion til elektronisk fakturering, der overholder kravene til elektronisk fakturering for et land/område.

Følgende tabel indeholder listen over funktioner, som kan understøtte Elektronisk fakturering.

| Navn                                              | Land/område |
|---------------------------------------------------|----------------|
|Østrigsk elektronisk faktura                        |Østrig         |
|Belgisk elektronisk faktura                         |Belgien         |
|NF-e Federal - brasiliansk elektronisk faktura       |Brasilien          |
|NFS-e - Brasiliansk tjeneste (by) elektronisk faktura|Brasilien          |
|Dansk elektronisk faktura                          |Danmark         |
|Egyptisk elektronisk faktura                        |Egypten           |
|Estisk elektronisk faktura                        |Estland         |
|Finsk elektronisk faktura                         |Finland         |
|Fransk elektronisk faktura                          |Frankrig          |
|Tysk elektronisk faktura                          |Tyskland         |
|PEPPOL - Global elektronisk faktura                 |Globalt          |
|Italiensk elektronisk faktura                         |Italien           |
|CFDI - mexicansk elektronisk faktura                  |Mexico          |
|Hollandsk elektronisk faktura                           |Nederlandene     |
|Norsk elektronisk faktura                       |Norge          |
|Spansk elektronisk faktura                         |Spanien           |

I de tilfælde, hvor der er en ældre elektronisk faktureringsfunktion, der understøttes af landet/områdets lokaliseringsomfang, giver aktiveringen af disse funktioner mulighed for at lukke den ældre funktion og aktivere de elektroniske fakturaer, der skal udstedes via Elektronisk fakturering.

> [!IMPORTANT]
> Når funktionen til integration af elektronisk fakturering er aktiveret, er den nye erfaring med elektronisk fakturering som standard deaktiveret. Du kan bruge funktionsbegrebet til selektivt at aktivere nye oplevelser for juridiske enheder ved hjælp af specifikke funktioner for lande/områder. Indstillingen **Global** styrer den nye oplevelse for de øvrige lande/områder, der ikke er angivet specifikt i tabellen.

## <a name="submit-electronic-documents"></a>Indsend elektroniske dokumenter

Processen med at sende elektroniske dokumenter repræsenterer det fælles kommunikationspunkt mellem Finance og Supply Chain Management og Elektronisk fakturering. Ved hver afsendelseshændelse går kommunikationsflowet i begge retninger:

- **Fra Finance og Supply Chain Management til Elektronisk fakturering** – Finance og Supply Chain Management sender de abstrakte fakturaer til Elektronisk fakturering. Efter behov sender de også indholdet af variabler, der blev konfigureret som en del af funktionerne til elektronisk fakturering.
- **Fra Elektronisk fakturering til Finance og Supply Chain Management** – Afhængigt af den elektroniske faktureringsfunktion modtager Finance og Supply Chain Management opdateringer fra Elektronisk fakturering om behandlingsresultaterne af fakturaer, der tidligere er sendt. De modtager også indholdet af variabler, der blev konfigureret som en del af funktionerne til elektronisk fakturering.

Hvis du vil sende elektroniske dokumenter til Elektronisk fakturering i Finance og Supply Chain Management, skal du gå til **Organisationsadministration &gt; Periodisk &gt; Elektroniske dokumenter &gt; Send elektroniske dokumenter**.

Udgangspunktet er en bogført faktura. Denne faktura kan komme fra forskellige oprindelser, f.eks. salgsordrer, projektfakturaer eller fritekstfakturaer.

Afsendelsesprocessen kan køres manuelt eller i baggrunden.

- **Manuel kørsel** - I forbindelse med manuel kørsel skal du bruge indstillingen **Filter** til at definere intervallet af dokumenter, der skal sendes. På siden **Filtre** kan du konfigurere din egen forespørgsel, så du kan vælge de bogførte fakturaer, der skal sendes. Når du har valgt, skal du starte afviklingen af behandlingen manuelt og vente på, at det er kørt færdig. Når behandlingen er fuldført, vises antallet af elektroniske dokumenter, der er blevet sendt, i en meddelelse i handlingscenteret.
- **Baggrundsudførelse** – Baggrundsudførelse kører uden at kræve, at du er logget på, eller lade dialogboksen til overførsel være åben. Du kan planlægge, at køre processen og definere udførelsesfrekvensen.

## <a name="view-the-submission-logs"></a>vise indsendelseslogge

I Finance og Supply Chain Management kan du bruge overførselslogfiler til at få vist resultaterne af behandlingen af afsendelsen til Elektronisk fakturering. Gå til **Organisationsadministration &gt; Periodisk &gt; Elektroniske dokumenter &gt; Elektronisk dokumentafsendelse** og derefter i feltet **Dokumenttype** vælge en værdi, der skal filtrere typen af de fakturaer, der vises af logfilerne.

Der er tre mulige afsendelsesstatusser:

- **Planlagt** - Elektronisk fakturering har modtaget afsendelsen fra Finance og Supply Chain Management, og behandlingen af den elektroniske faktureringsfunktion er i gang.
- **Fuldført** - Elektronisk fakturering har behandlet den elektroniske faktureringsfunktion, som den er konfigureret til at køre den.
- **Ikke besvarede** – I elektronisk fakturering opstod en fejl, eller den blev stoppet af en undtagelse under behandlingen af funktionen til elektronisk fakturering.

> [!IMPORTANT]
> Afsendelsesstatus refererer til status for den behandling, som Elektronisk fakturering behandler i forbindelse med funktionen til elektronisk fakturering. Den refererer ikke til den endelige status for selve den elektroniske faktura.
>
> Hvis en elektronisk faktura f.eks. skal sendes til en ekstern webtjeneste til godkendelse, kan afsendelsesstatus være **Fuldført**, men status for den elektroniske faktura kan være **Afvist**. I dette tilfælde kan elektronisk fakturering behandle den elektroniske faktureringsfunktion, som den er konfigureret til at køre funktionen. Den elektroniske faktura blev dog afvist, fordi den ikke opfyldte de kriterier, som webtjenesten blev oprettet til fakturagodkendelse for.

Afsendelseslogfilerne omfatter følgende yderligere funktioner:

- **Detaljer om afsendelse** - Vise detaljer om hovedafsendelsen. En visualisering viser hele udførelsesloggen for de handlinger, der er konfigureret i funktionen til elektronisk fakturering. Det giver også brugerne mulighed for at hente de filer, der oprettes under behandlingen. I scenarier, hvor fakturaen skal godkendes af en ekstern webtjeneste, giver det brugerne mulighed for at få vist fakturaens status.
- **Relaterede afsendelser** - Vise detaljer om underordnede afsendelser.
- **Annuller afsendelser** - Denne funktion aktiverer en særlig afsendelsesproces i scenarier, hvor den elektroniske faktura skal godkendes af en ekstern webtjeneste. Den beder elektronisk fakturering om at sende webtjenesten en bestemt meddelelse, der er beregnet til at annullere statussen for en godkendt elektronisk faktura i webtjenestedatabasen.
- **Send dokument igen** - Send et elektronisk dokument, der allerede er blevet sendt til Elektronisk fakturering. Der oprettes en ny log på siden **Detaljer om afsendelse**.
- **Send relaterede afsendelser**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
