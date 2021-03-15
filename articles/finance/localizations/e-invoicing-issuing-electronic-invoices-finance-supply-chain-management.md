---
title: Udstede elektroniske fakturaer i Finance og Supply Chain Management
description: Dette emne beskriver, hvordan du udsteder elektroniske faktura i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management ved hjælp af tilføjelsesprogrammet Elektronisk fakturering.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 187f5a20d088b4fcd7af2a6576357a69c2efc2c6
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104359"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Udstede elektroniske fakturaer i Finance og Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dette emne beskriver, hvordan du udsteder elektroniske faktura i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management ved hjælp af tilføjelsesprogrammet Elektronisk fakturering.


## <a name="feature-activation"></a>Funktionsaktivering

Før du kan begynde at udstede elektroniske fakturaer via tilføjelsesprogrammet Elektronisk fakturering er det nødvendigt at aktivere funktionsreferencen i Finans og Supply Chain Management.

Hver funktionsreference svarer til en bestemt funktion til elektronisk fakturering, der overholder kravene til elektronisk fakturering fra et land/område.

Følgende tabel indeholder listen over funktionsreferencer, som understøtter tilføjelsesprogrammet Elektronisk fakturering.

| Funktionsreference | Navn                                              | Land/område |
|-------------------|---------------------------------------------------|----------------|
| BR-00053          | NF-e Federal - brasiliansk elektronisk faktura       | Brasilien         |
| BR-00095          | NFS-e brasilianske elektroniske fakturaer               | Brasilien         |
| DK-00001          | E-fakturering til den offentlige sektor (OIOUBL) - DK    | Danmark        |
| EG-00008          | E-fakturering for Egypten                             | Egypten          |
| ES-00025          | Elektronisk faktura til den offentlige sektor           | Spanien          |
| EUR-00023         | Den europæiske union, e-fakturering til den offentlige sektor       | Europa         |
| ITA-00036         | IT - e-fakturering til den offentlige sektor (FatturaPA) | Italien          |
| MX-00010          | CFDI for e-fakturering                                  | Mexico         |
| MX-00016          | E-fakturering CFDI - annulleringsproces           | Mexico         |

I de tilfælde, hvor der er en ældre elektronisk faktureringsfunktion, der understøttes af landets lokaliseringsomfang, giver aktiveringen af funktionsreferencen mulighed for at udstede elektroniske fakturaer via tilføjelsesprogrammet Elektronisk fakturering og deaktivere den tidligere funktion.

## <a name="submit-electronic-documents"></a>Indsend elektroniske dokumenter

Processen med at sende elektroniske dokumenter repræsenterer det fælles kommunikationspunkt mellem Finans og Supply Chain Management og tilføjelsesprogrammet Elektronisk fakturering. Ved hver afsendelseshændelse går kommunikationsflowet i begge retninger:

- **Fra Finans og Supply Chain Management til tilføjelsesprogrammet Elektronisk fakturering** – Finans og Supply Chain Management sender de abstrakte fakturaer til tilføjelsesprogrammet Elektronisk fakturering. Efter behov sender de også indholdet af variabler, der blev konfigureret som en del af funktionerne til elektronisk fakturering.
- **Fra tilføjelsesprogrammet Elektronisk fakturering til Finans og Supply Chain Management** – Afhængigt af den elektroniske faktureringsfunktion modtager Finans og Supply Chain Management opdateringer fra tilføjelsesprogrammet Elektronisk fakturering om behandlingsresultaterne af fakturaer, der tidligere er sendt. De modtager også indholdet af variabler, der blev konfigureret som en del af funktionerne til elektronisk fakturering.

Hvis du vil sende elektroniske dokumenter til tilføjelsesprogrammet Elektronisk fakturering i Finans og Supply Chain Management, skal du gå til **Organisationsadministration &gt; Periodisk &gt; Elektroniske dokumenter &gt; Send elektroniske dokumenter**.

Udgangspunktet er en bogført faktura. Denne faktura kan komme fra forskellige oprindelser, f.eks. salgsordrer, projektfakturaer eller fritekstfakturaer.

Afsendelsesprocessen kan køres manuelt eller i baggrunden.

- **Manuel kørsel** - I forbindelse med manuel kørsel skal du bruge indstillingen **Filter** til at definere intervallet af dokumenter, der skal sendes. På siden **Filtre** kan du konfigurere din egen forespørgsel, så du kan vælge de bogførte fakturaer, der skal sendes. Når du har valgt, skal du starte afviklingen af behandlingen manuelt og vente på, at det er kørt færdig. Når behandlingen er fuldført, vises antallet af elektroniske dokumenter, der er blevet sendt, i en meddelelse i handlingscenteret.
- **Baggrundsudførelse** – Baggrundsudførelse kører uden at kræve, at du er logget på, eller lade dialogboksen til overførsel være åben. Du kan planlægge, at køre processen og definere udførelsesfrekvensen.

## <a name="view-the-submission-logs"></a>vise indsendelseslogge

I Finans og Supply Chain Management kan du bruge overførselslogfiler til at få vist resultaterne af behandlingen af afsendelsen til tilføjelsesprogrammet Elektronisk fakturering. Gå til **Organisationsadministration &gt; Periodisk &gt; Elektroniske dokumenter &gt; Elektronisk dokumentafsendelse** og derefter i feltet **Dokumenttype** vælge en værdi, der skal filtrere typen af de fakturaer, der vises af logfilerne.

Der er tre mulige afsendelsesstatusser:

- **Planlagt** - Tilføjelsesprogrammet elektronisk fakturering har modtaget afsendelsen fra Finans og Supply Chain Management, og behandlingen af den elektroniske faktureringsfunktion er i gang.
- **Fuldført** - Tilføjelsesprogrammet elektronisk fakturering har behandlet den elektroniske faktureringsfunktion, som den er konfigureret til at køre den.
- **Ikke besvarede** – Det tilføjelsesprogrammet elektronisk fakturering, der opstod en fejl, eller som blev stoppet af en undtagelse under behandlingen af funktionen til elektronisk fakturering.

> [!IMPORTANT]
> Afsendelsesstatus refererer til status for den behandling, som tilføjelsesprogrammet Elektronisk fakturering behandler i forbindelse med funktionen til elektronisk fakturering. Den refererer ikke til den endelige status for selve den elektroniske faktura.
>
> Hvis en elektronisk faktura f.eks. skal sendes til en ekstern webtjeneste til godkendelse, kan afsendelsesstatus være **Fuldført**, men status for den elektroniske faktura kan være **Afvist**. I dette tilfælde kan tilføjelsesprogrammet elektronisk fakturering behandle den elektroniske faktureringsfunktion, som den er konfigureret til at køre funktionen. Den elektroniske faktura blev dog afvist, fordi den ikke opfyldte de kriterier, som webtjenesten blev oprettet til fakturagodkendelse for.

Afsendelseslogfilerne omfatter følgende yderligere funktioner:

- **Detaljer om afsendelse** - Vise detaljer om hovedafsendelsen. En visualisering viser hele udførelsesloggen for de handlinger, der er konfigureret i funktionen til elektronisk fakturering. Det giver også brugerne mulighed for at hente de filer, der oprettes under behandlingen. I scenarier, hvor fakturaen skal godkendes af en ekstern webtjeneste, giver det brugerne mulighed for at få vist fakturaens status.
- **Relaterede afsendelser** - Vise detaljer om underordnede afsendelser.
- **Annuller afsendelser** - Denne funktion aktiverer en særlig afsendelsesproces i scenarier, hvor den elektroniske faktura skal godkendes af en ekstern webtjeneste. Den beder webtjenesten om at sende webtjenesten en bestemt meddelelse, der er beregnet til at annullere statussen for en godkendt elektronisk faktura i webtjenestedatabasen.
- **Send dokument igen** - Send et elektronisk dokument, der allerede er blevet sendt til tilføjelsesprogrammet Elektronisk fakturering. Der oprettes en hel ny log på siden **Detaljer om afsendelse**.
- **Send relaterede afsendelser**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]