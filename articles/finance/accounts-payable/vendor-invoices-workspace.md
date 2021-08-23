---
title: Arbejdsområde for automatisering af kreditorfakturaer
description: Dette emne forklarer, hvordan du konfigurerer det arbejdsområde, der er relateret til kreditorfakturaer, og som viser de oplysninger, der er tilgængelige via Microsoft Power BI.
author: abruer
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2020-09-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dde77a19fae9af8f40af8b14259a29db80f4a80cf8be75233a463d6fec2dac46
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722713"
---
# <a name="vendor-invoice-automation-workspace"></a>Arbejdsområde for automatisering af kreditorfakturaer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emne forklarer, hvordan du konfigurerer det arbejdsområde, der er relateret til kreditorfakturaer, og som viser de oplysninger, der er tilgængelige via Microsoft Power BI. Oplysningerne om kreditorfakturaen i dette arbejdsområde filtreres for bestemte brugere og vises i grafisk format.

## <a name="overview"></a>Overblik

Arbejdsområdet **Automatisering af kreditorfakturaer** viser oplysninger, der vedrører behandling af kreditorfakturaer. Det indeholder en **Mit arbejde**-visning og siden **Analyser – Alle firmaer**. Visningen **Mit arbejde** viser oversigtsfelter, gitre til kreditorpostering og relaterede kreditoroplysninger. Siden **Analyser – Alle firmaer** bruger funktionerne i Power BI til at vise visualiseringer, der vedrører kreditorfakturaer.

## <a name="set-up-the-workspace-to-show-power-bi-content"></a>Konfigurere arbejdsområdet til at vise Power BI-indhold

Du skal fuldføre denne opsætning, før data kan vises i Power BI-visualiseringer i arbejdsområdet **Automatisering af kreditorfakturaer**.

1. I arbejdsområdet **Funktionsstyring** skal du filtrere listen for at finde funktionen **Automatisering af kreditorfaktura**.
3. Vælg **Aktiver nu**.
4. Hvis du vil sikre, at fakturaer kan behandles fra start til slut, uden at kræve manuel indgriben, skal du konfigurere en arbejdsproces for kreditorfakturaer. Gå til **Kreditor \> Opsætning \> Kreditorarbejdsgange** for at konfigurere en arbejdsproces.
5. Gå til **Kreditor \> Konfiguration \> Kreditorparametre**, og vælg fanen **Automatisering af kreditorfakturaer**. Du kan finde flere oplysninger under [Konfigurationsindstillinger for automatisering af kreditorfakturaer](vnd-invoice-set-up-options.md).
6. Angiv indstillingen **Send automatisk importerede fakturaer til arbejdsgang** til **Ja**.
7. Hvis produktkvitteringer automatisk skal sammenholdes, skal du angive indstillingen **Afstem automatisk produktkvitteringer med fakturalinjer** til **Ja**.
8. Gennemgå de resterende, valgfrie indstillinger, og konfigurer dem i overensstemmelse med din organisations krav.
9. Gå til **Systemadministration \> Konfiguration \> Systemparametre** for at angive felterne **Systemvaluta** og **Systemvalutakurs**.
10. Gå til **Finans \> Opsætning \> Finans** for at angive **Regnskabsvaluta** og **Valutakurstype**.
11. Gå til **Finans \> Valutaer \> Valutakurser**, og angiv valutakurserne mellem transaktionsvalutaen og regnskabsvalutaen og mellem regnskabsvalutaen og systemvalutaen.
12. Gå til **Systemadministration \> Konfiguration \> Enhedslager**, og se efter **Automatisering af kreditorfaktura**. Vælg **Opdater**.

Hvis du vil have vist de oplysninger, der vises i arbejdsområdet, skal du have sikkerhedsrollen Kreditorchef eller Kreditorassistent.

## <a name="my-work-view"></a>Visningen Mit arbejde

### <a name="company-selection"></a>Firmavalg

Når funktionen **Automatisering af kreditorfakturaer** er aktiveret, vises feltet **Virksomhed** øverst i arbejdsområdet. Valget i feltet **Firma** påvirker alle de oplysninger, der vises i arbejdsområdet. I visningen ses standardoplysninger om det firma, du har logget på. Hvis du vælger et andet firma i feltet **Firma**, kan du få vist oplysninger om det pågældende firma i arbejdsområdet. Du kan derefter vælge et felt i arbejdsområdet for at gå til den relaterede side i det valgte firma.

### <a name="summary-tiles"></a>Oversigt over felter

Felterne i sektionen **Oversigt over ventende fakturaer** i visningen **Mit arbejde** giver en oversigt over kreditorfakturaernes status. Du kan se kladder, der endnu ikke er bogført, og fakturaer, der er på hold. Derudover er der fire felter, der er knyttet til funktionen til automatisering af kreditorfakturaer:

- Matchning med manuel kvittering er nødvendig
- Matchningsvalidering blev ikke fuldført
- Fakturaer blev ikke sendt til arbejdsproces
- Fakturaer blev ikke importeret

(Disse fire felter kræver, at funktionen til automatisering af kreditorfakturaer aktiveres i Funktionsstyring).

Hvis du vil bruge feltet **Gendan kreditorfakturaer**, skal funktionen være aktiveret i Kreditorparametre. Gå til **Kreditor \> Kreditorparametre**, og angiv derefter indstillingen **Tillad gendannelse af kreditorfaktura** til **Ja** under fanen **Faktura**.

Når funktionen er slået til, vil du også have grupperet tre felter sammen i arbejdsområdet i et afsnit, der kaldes **Kladder**. Felterne har navnene **Kladder**, **Kladder, der er tildelt mig** og **Fakturapulje**. 

Oplysningerne i sektionen **Oversigt over ventende fakturaer** er for det firma, der er angivet som standardfirma for dit logon.

### <a name="creating-new-records"></a>Oprette nye poster

Hvis du vil oprette en ny fakturapost, skal du vælge **Ny** og derefter vælge en af følgende posttyper på listen:

- Kreditorfaktura
- Fakturajournal
- Global fakturajournal
- Indgangsbog
- Godkendelse af faktura

Bemærk, at den post, du opretter, er baseret på firmafilteret, og ikke det firma, du er logget på. Du er f.eks. logget på firmaet **UMSF**, men firmafilteret er angivet til **GBSI**. Hvis du i dette tilfælde vælger **Ny** og derefter vælger en posttype på listen, oprettes posten i GBSI-firmaet.

### <a name="documents-not-invoiced-grids"></a>Dokumenter, der ikke er fakturerede, i gitre

Sektionen **Dokumenter, der ikke er faktureret**, indeholder gitre, der viser dokumenter, der afventer kreditorfakturaer.

I gitteret **Åbne indkøbsordrer** vises alle indkøbsordrer, der endnu ikke er fuldt faktureret. Du kan bruge knappen **Fakturer nu** til at oprette en kreditorfaktura for en indkøbsordre. Du kan bruge knappen **Forudbetalingsfaktura nu** til at oprette en forudbetalingsfaktura for en indkøbsordre.

I gitteret **Produktkvitteringer** vises alle købskvitteringstransaktioner, der endnu ikke er fuldt faktureret. Du kan bruge knappen **Fakturer nu** til at oprette en kreditorfaktura for en indkøbsordre.

I gitteret **Ventende kreditorfakturaer** vises alle kreditorfakturaer, der ikke er sendt til arbejdsprocessystemet. Du kan bruge feltet **Søg** og/eller firmafilteret til at søge efter en bestemt kreditorfaktura. Du kan bruge knappen **Rediger** til at redigere en transaktion, der vises i gitteret.

I gitteret **Find indkøbsordre** kan du bruge **Søg**-feltet til at søge efter en bestemt indkøbsordre.

### <a name="related-information"></a>Relaterede oplysninger

Du kan få vist oplysninger om bogførte fakturaer ved hjælp af linkene i højre side af arbejdsområdet. Disse links omfatter **Åbne kreditorfakturaer**, **Fakturakladde** og **Fakturahistorik og tilsvarende detaljer**. I sektionen **Kreditorer** kan du få adgang til en filtreret liste, der viser alle kreditorer, som er på hold, eller du kan bruge linket **Alle kreditorer**. **Alle indkøbsordrer** og **Åbne forudbetalinger** er også tilgængelige.

### <a name="analytics--all-companies-page"></a>Siden Analyse – alle firmaer

Når indstillingen **Send automatisk importerede fakturaer til arbejdsgang** er angivet til **Ja** på siden **Kreditorparametre**, kan du få vist automatiseringsanalyse. Siden **Analyse - alle firmaer** indeholder vigtige målepunkter, f.eks. kreditorfakturaer, der er under godkendelse af en godkender og af et firma. Denne side indeholder fem rapportsider. En side indeholder en oversigt, og de andre otte sider indeholder oplysninger om målepunkter for automatisering af kreditorbetalinger.

Følgende tabel viser de visualiseringer, der er tilgængelig på hver rapportside.

| Rapportside                    | Visualiseringer |
|--------------------------------|----------------|
| Oversigt over kreditorfakturaer        | <ul><li>Ventende kreditorfakturaer i automatisering i systemvaluta</li><li>Fakturaer, der ikke blev importeret</li><li>Fakturaer i arbejdsproces</li><li>Berøringsfrie fakturaer sidste 30 dage</li><li>Samlet antal automatiske fakturaer sidste 30 dage</li><li>Saldo for åbne fakturaer i systemvaluta</li><li>Fejlårsager de seneste 30 dage</li><li>Procentdel af bogførte fakturaer, der blev behandlet automatisk</li><li>Dage til behandling af en faktura</ul></li> |
| Automatiseringsstatus              | <ul><li>Berøringsfrie fakturaer sidste 30 dage</li><li>Berøringsfrie fakturaer sidste 30 dage efter firma</li><li>Berøringsfrie fakturaer sidste 30 dage efter kreditorgruppe</li><li>Procentdel af bogførte fakturaer, der blev behandlet automatisk</li><li>Dage til behandling af en faktura</li></ul> |
| Fakturaer, der ikke blev importeret | <ul><li>Fakturaer, der ikke blev importeret</li><li>Fakturaer, der ikke blev importeret, efter firma</li></ul> |
| Årsager til automatiseringsfejl | <ul><li>Mislykkede fakturaer</li><li>Mislykkede fakturaer efter firma</li><li>Mislykkede fakturaer efter kreditorgruppe</li></ul> |
| Workflowsstatus                | <ul><li>Fakturaer i arbejdsproces</li><li>Arbejdsprocesforekomster af kreditorfaktura</li><li>Tildeling pr. godkender</li><li>Arbejdsproces for kreditorfakturaer pr. firma</li><li>Gennemsnitligt antal dage i arbejdsgang pr. godkender</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
