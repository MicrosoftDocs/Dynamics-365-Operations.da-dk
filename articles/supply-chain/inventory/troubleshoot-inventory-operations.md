---
title: Fejlfinde lagerhandlinger
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med lagerhandlinger.
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 24e41e35b3e810c509a16b91fffd1e796ab9d134
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832052"
---
# <a name="troubleshoot-inventory-operations"></a>Fejlfinde lagerhandlinger

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med lagerhandlinger.

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Jeg kan ikke finde dialogboksen til rullelisten "Arbejdsgang" for lagerkladder.

### <a name="issue-description"></a>Problembeskrivelse

Du kan ikke finde dialogboksen til rullelisten **Arbejdsgang** på kladdesiden, eller relaterede arbejdsgangshandlinger er ikke tilgængelige.

Dette problem kan forekomme af tre årsager som beskrevet i følgende underafsnit.

### <a name="issue-resolution-1"></a>Problemløsning 1

Hvis problemet gælder for alle brugere, kan det være på grund af, at godkendelsesarbejdsgangen ikke er tildelt kladdenavnet. Følg disse trin for at løse dette problem.

1. Gå til **Lagerstyring &gt; Konfiguration &gt; Kladdenavne &gt; Lager**.
1. Vælg et kladdenavn i listeruden for at åbne indstillingerne.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Godkendelsesarbejdsgang** til *Ja*. Klik på **Ja**, hvis du bliver bedt om at bekræfte ændringen.
1. I feltet **Arbejdsgang** skal du vælge den arbejdsgang, du vil bruge til det valgte kladdenavn.

### <a name="issue-resolution-2"></a>Problemløsning 2

Hvis arbejdsgangen bruger tilpasset kode, kan der opstå problemer, efter du har opgraderet systemet. I kladdearbejdsgangen kan knappen **Send** f.eks. være nedtonet, så du ikke kan vælge den for at godkende en afsendelse.

Hvis knappen **Send** er nedtonet, er arbejdsgangen måske blevet tilpasset, hvilket betyder, at metoden for arbejdsgangen `canSubmitToWorkflow()` i `FormDataUtil` er blevet udvidet. Du kan løse dette problem ved at ændre den måde, hvorpå du udvider metoden for `canSubmitToWorkflow()` til at bruge strukturen, i følgende eksempel.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a>Problemløsning 3

Hvis problemet kun gælder for nogle få bestemte brugere, har disse brugere muligvis ikke de sikkerhedsrettigheder, der er nødvendige for at køre arbejdsgangshandlinger i lagerkladder. Kontrollér, at hver påvirket bruger har sikkerhedsrettigheden *Vedligehold arbejdsgang for lagerkladder*. Denne rettighed er som standard tildelt en opgave med samme navn, og denne opgave anvendes til rollerne *Lagerarbejder* og *Lagerchef*.

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a>Min lagerkladde forbliver i statussen systemlåst, og arbejdsgangsbatchjobbet virker ikke.

### <a name="issue-description"></a>Problembeskrivelse

En af lagerkladderne er låst af en eller anden handling, og den frigives ikke. Hvis der f.eks. opstår en ukendt fejl under bogføring (som er en systemlåshandling), kan kladden stadig have statussen systemlåst. I dette tilfælde viser arbejdsgangsopgavehandleren en fejl under låsevalidering.

### <a name="issue-resolution"></a>Problemløsning

Log på SQL Server-forekomsten for Supply Chain Management, og kontrollér, om **InventJournalTable.SystemBlocked** er angivet til *1*. Hvis det er tilfældet, skal du sørge for, at kladden ikke er i låst status og derefter nulstille **InventJournalTable.SystemBlocked** til *0*.

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a>Min arbejdsgang for lagerkladder fuldføres aldrig, og kladden kan ikke redigeres eller bogføres.

### <a name="issue-description"></a>Problembeskrivelse

Når du har sendt en arbejdsgang for lagerkladdegodkendelse, stopper arbejdsgangsbehandlingen med at svare, og du kan ikke redigere eller behandle kladderne.

### <a name="issue-resolution"></a>Problemløsning

Der er flere årsager til, at arbejdsgangsbehandlingen muligvis ikke fuldføres. Kontrollér, om der er følgende problemer:

- Gå til **Lagerstyring &gt; Konfiguration &gt; Arbejdsgange for lagerstyring**, og gennemse konfigurationen af den berørte arbejdsgang. Du kan finde flere oplysninger i [Arbejdsgange for godkendelse af lagerkladde](inventory-journal-workflow.md).
- Der kan opstå en undtagelse eller fejl i arbejdsgangen. Gennemse historikken for arbejdselementet for den berørte arbejdsgang for at se, om den omfatter en applikationsfejl, der afslutter arbejdsgangen.
- Lagerkladden kan kun opdateres eller redigeres, hvis den er godkendt. Hvis tilbagekaldelse er aktiv, kan du prøve at tilbagekalde kladden. Afviklingen af arbejdsgangsbatchjobbet kan være suspenderet af flere årsager. Nogle af disse årsager kan være forårsaget af problemer i arbejdsgangsstrukturen.

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a>Betingelserne for arbejdsgange for lagerkladder gælder kun på kladdeniveau, ikke på linjeniveau

### <a name="issue-description"></a>Problembeskrivelse

Du kan opleve denne fejl, hvis du f.eks. prøver at konfigurere en betingelse for arbejdsgange for lagerkladder for kostbeløbet. Du konfigurerer betingelsen, så trin 1 kun køres, når kostbeløbet er mindre end 100. Du konfigurerer derefter en anden betingelse, så trin 2 kun køres, når kostbeløbet er mere end eller lig med 100. Når arbejdsgangen derefter køres, vises der kun én linje i arbejdsgangshistorikken, og den første betingelse evalueres altid som *sand*, uanset hvilken værdi der sendes.

### <a name="issue-workaround"></a>Problemløsning

I den aktuelle version gælder betingelserne for arbejdsgange for lagerkladder kun på kladdeniveau, ikke på linjeniveau. Denne funktionsmåde er tilsigtet. Det anbefales, at du kun angiver betingelseskriterierne for attributter på kladdeniveau.

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a>Filterruden på listesiden Beholdningsliste filtrerer ikke resultater som forventet.

### <a name="issue-description"></a>Problembeskrivelse

Filtrene i filteruden på siden **Beholdningsliste** filtrerer ikke resultater som forventet.

### <a name="issue-resolution"></a>Problemløsning

Denne funktionsmåde er tilsigtet.

Siden  **Beholdningsliste** samles fra en detaljeret disponibel lagerbeholdningstabel, der omfatter alle tilgængelige dimensioner. Listen på denne side er dog en oversigt. Derfor kan den kombinere rækker fra kildetabellen ved at aggregere værdier i henhold til de viste dimensioner.

Filtre, der er konfigureret i filterruden, gælder for kildetabellen, ikke den samlede liste. Denne adfærd kan nogle gange give uventede resultater, som det fremgår af [disse eksempler](inventory-on-hand-list.md#examples).

De  [filtre, der findes i gitteret](inventory-on-hand-list.md#grid-filters),  *bliver* anvendt på den samlede liste. Disse filtre omfatter både QuickFilter øverst i gitteret og filteret for hver kolonneoverskrift.

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Enheden og enhedsantallet fungerer ikke korrekt i lagerkladden.

### <a name="issue-description"></a>Problembeskrivelse

Der kan opstå en eller begge af følgende fejl, når du arbejder med enheder og antal i en lagerkladde:

- Du kan ikke se enheder eller enhedsantal i lagerkladden, når der er konfigureret en enhedskonvertering for det frigivne produkt, og du kan ikke ændre enheden i lagerkladden.
- Du kan se felterne **Antal** og **Enhed** i lagerkladden, men du kan ikke se feltet **Enhedsantal**. Hvis du ændrer enheden, angiver et antal og bogfører kladden, vises den oprindelige måleenhed for dette antal stadig i kladden.

### <a name="issue-resolution"></a>Problemløsning

Følg disse trin for at løse dette problem.

1. I arbejdsområdet **Funktionsstyring** skal du sørge for, at funktionen *Brug af måleenhed og enhedsantal i lagerkladder* er aktiveret. Denne funktion føjer felterne **Enhed** og **Enhedsantal** til kladden.
1. Når funktionen er aktiveret, skal du benytte felterne **Antal**, **Enhedsantal** og **Enhed** på følgende måde:

    - **Antal** – Angiv antallet ved hjælp af den standardenhed, der er defineret for det frigivne produkt. Selve standardenheden vises dog ikke her. Hvis der er konfigureret en konvertering mellem standardenheden og den valgte enhed i feltet **Enhed**, opdateres feltet **Antal** automatisk baseret på valgene i felterne **Enhedantal** og **Enhed**.
    - **Enhedsantal** – Angiv antallet ved at bruge den enhed, der er valgt i feltet **Enhed**.
    - **Enhed** – Vælg den enhed, der skal anvendes på værdien i feltet **Enhedsantal**.

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Jeg får følgende fejlmeddelelse: "Maks. antal decimaler for lagerenheden er 0".

### <a name="issue-description"></a>Problembeskrivelse

Når du forsøger at bogføre en lagertransaktion eller en lagerreservation, får du vist følgende fejlmeddelelse: "Maks. antal decimaler for lagerenheden er 0".

Denne fejl opstår, når lagertransaktionsantallet angives som en decimalværdi, der er under det præcisionsniveau, som feltet understøtter. Der er f.eks. angivet et antal på *0,5* for en lagertransaktion, men antal understøttes kun i heltal. Derfor skal værdien være *1* i stedet for *0,5*.

### <a name="issue-resolution"></a>Problemløsning

1. Kør følgende script på SQL Server-forekomsten for at afrunde antallet i lagertransaktionerne. Dette script retter værdier i tabellen **InventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Kør en konsistenskontrol beholdningen, hvor indstillingen **ret fejl** er aktiveret. Denne kontrol retter værdier i tabellen **InventSum**.

> [!IMPORTANT]
> Det anbefales på det kraftigste, at du nøje redigerer scriptet i dit miljø, tester det i et testmiljø og derefter kontrollerer de resulterende data, før du kører scriptet i et produktionsmiljø.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]