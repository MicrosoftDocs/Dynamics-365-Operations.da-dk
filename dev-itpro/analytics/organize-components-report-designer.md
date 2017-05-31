---
title: Organisere rapportkomponenter i Report Designer
description: "Når du har udviklet komponentdokumenter og oprettet rapporter, er det nyttigt at organisere disse objekter, så de er lettere for brugerne at finde. I denne artikel beskrives, hvordan du organiserer eksisterende rapporter, dokumentkomponenter og objekter i Report Designer."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a8739f426c401aacbab56179bad429a231060f57
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="organize-report-components-in-report-designer"></a>Organisere rapportkomponenter i Report Designer

[!include[banner](../includes/banner.md)]


Når du har udviklet komponentdokumenter og oprettet rapporter, er det nyttigt at organisere disse objekter, så de er lettere for brugerne at finde. I denne artikel beskrives, hvordan du organiserer eksisterende rapporter, dokumentkomponenter og objekter i Report Designer.

Du kan omdøbe mapper, rapporter, dokumentkomponenter og andre objekter i Report Designer for at organisere dine filer. Afhængigt af hvilken type objekt, du omdøber, skal du muligvis opdatere tilknytninger til det pågældende objekt.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Omdøbe en mappe eller en dokumentkomponent i Report Designer
Du kan omdøbe mapper, rapportdefinitioner, rækkedefinitioner, kolonnedefinitioner og rapporteringstrædefinitioner i Report Designer. **Bemærk:** Når du omdøber en dokumentkomponent, skal du opdatere alle rapportdefinitioner, der bruger dokumentkomponenten. Ellers kan der ikke oprettes en ny rapport.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Omdøbe en mappe eller en dokumentkomponent i Report Designer

1.  I Report Designer kan du bruge navigationsruden til at finde den mappe eller det objekt, der skal omdøbes.
2.  Højreklik på mappen eller objektet, og klik derefter på **Omdøb**. Feltet **Navn** i navigationsruden bliver tilgængeligt.
3.  Skriv et nyt navn, og tryk derefter på Enter.
4.  Hvis dokumentkomponenten er en rækkedefinition, kolonnedefinition eller rapporteringstrædefinition, skal du opdatere andre komponenter, der er knyttet til den. Højreklik på den dokumentkomponent, du omdøbte i trin 3, vælg **Tilknytninger**, og vælg derefter et element på listen for at opdatere det.
5.  Gentag trin 4, indtil alle tilknyttede elementer er opdateret.

## <a name="create-and-manage-report-groups"></a>Oprette og administrere rapportgrupper
Du kan gruppere rapportdefinitioner for at generere flere rapporter på samme tid. Du skal have designer- eller administratorrollen for at oprette, redigere, slette og oprette rapportgrupper. Brugere, der har generatorrollen, kan generere rapportgrupper og kan også ændre brugerindstillingen for rapportdefinitioner for rapportgrupper.

### <a name="create-a-report-group"></a>Oprette en rapportgruppe

1.  Klik på **Rapportgrupper** i navigationsruden i Report Designer.
2.  I menuen **Filer** skal du klikke på **Ny** &gt; **Rapportgruppedefinition** for at åbne en ny rapportgruppe i fremviservinduet. Du kan også klikke på knappen **Rapportgruppe** ![Rapportgruppe](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Rapportgruppe") på værktøjslinjen.
3.  Klik på fanen **Rapportgruppe**. Hvis du vil tilsidesætte oplysningerne om de enkelte rapportdefinitioner til generering af denne rapport, skal du markere afkrydsningsfeltet **Tilsidesæt regnskab, detaljer og datoindstillinger fra individuelle rapportdefinitioner**. Firmanavnet, detaljeringsniveauet, foreløbig-indstillingen og datooplysninger angives automatisk, men du kan stadig foretage opdateringer.
4.  Hvis du vil have genereret flere rapporter, der viser rapporteringsvalutaerne, skal du markere afkrydsningsfeltet **Medtag alle rapporteringsvalutaer**. Derefter kan du åbne flere visninger ved at klikke på knappen **Valuta** i webfremviseren, når du får vist rapporten.
5.  I feltet **Rapporter i gruppe** skal du klikke på **Tilføj** for at vælge de rapporter, der skal medtages i rapportgruppen. Hvis du vil vælge flere rapporter i dialogboksen **Tilføj**, skal du holde tasten Ctrl nede, mens du markerer rapporter. Når du er færdig med at vælge rapporter, skal du klikke på **OK**.
6.  Klik på **Filer** &gt; **Gem** for at gemme den nye rapportgruppe.

### <a name="modify-a-report-group"></a>Redigere en rapportgruppe

1.  Klik på **Rapportgrupper** i navigationsruden i Report Designer.
2.  Dobbeltklik på den rapportgruppe, der skal redigeres.
3.  Under fanen **Rapportgruppe** kan du foretage de ønskede ændringer.
4.  I menuen **Filer** skal du klikke på **Gem** for at gemme den ændrede rapportgruppe, eller du kan klikke på knappen **Gem** ![Gem](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Gem") på værktøjslinjen.

**Bemærk:** Hvis du har planlagt, at rapporter skal genereres med faste intervaller, kan du tilsidesætte disse indstillinger og generere en rapport med det samme.

### <a name="generate-a-report-group-report"></a>Generere en rapportgrupperapport

1.  Klik på **Rapportgrupper** i navigationsruden i Report Designer.
2.  Åbn den rapportgruppe, der skal genereres.
3.  Klik på knappen **Opret rapport** ![Opret rapport](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Opret rapport") for at oprette rapporter.

### <a name="delete-a-report-group"></a>Slette en rapportgruppe

1.  Klik på **Rapportgrupper** i navigationsruden i Report Designer.
2.  Højreklik på rapportgruppen, og vælg derefter **Slet**.
3.  Klik på **Ja**, når der vises en bekræftelsesmeddelelse.

## <a name="report-group-tab-controls"></a>Fanebladskontrolelementer til Rapportgruppe
Følgende tabel indeholder beskrivelser af kontrolelementerne under fanen **Rapportgruppe**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Styring</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tilsidesætte regnskab, detaljer og datoindstillinger fra individuelle rapportdefinitioner</td>
<td>Markér dette afkrydsningsfelt for at tilsidesætte individuelle rapportdefinitioner af rapporterne i denne rapportgruppe udelukkende i forbindelse med oprettelse af disse rapporter.</td>
</tr>
<tr class="even">
<td>Firmanavn</td>
<td>Vælg det regnskab, der skal bruges til rapporterne.</td>
</tr>
<tr class="odd">
<td>Detaljeringsniveau</td>
<td>Angiv det detaljeringsniveau, som rapporterne indeholder.
<ul>
<li><strong>Finansiel</strong>– en oversigtsrapport på højt niveau. Du kan ikke rulle ned til konti og dimensioner, med undtagelse af de konti og dimensioner, der er tilføjet via et rapporteringstræ.</li>
<li><strong>Finans og konto</strong> – en rapport, der indeholder en oversigt på højt niveau og kontooplysninger.</li>
<li><strong>Finans, Konto og Transaktion</strong> – en rapport, der indeholder en oversigt på højt niveau og transaktionsoplysninger.</li>
</ul></td>
</tr>
<tr class="even">
<td>Midlertidig</td>
<td>Angiv de aktivitetstyper, som rapporterne indeholder.
<ul>
<li><strong>Kun bogført aktivitet</strong> − Omfatter kun de transaktioner og saldi, der er bogført i dine finansielle data.</li>
<li><strong>Bogført og ikke-bogført aktivitet</strong> − Omfatter alle de transaktioner og saldi, der er indtastet og bogført i dine finansielle data.</li>
<li><strong>Kun ikke-bogført aktivitet</strong> − Omfatter kun de transaktioner, der er indtastet men ikke bogført i dine finansielle data.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Medtag alle rapporteringsvalutaer</td>
<td>Hvis der konfigureres yderligere rapporteringsvalutaer i Microsoft Dynamics ERP-systemet, vises de her. Markér dette afkrydsningsfelt for at få genereret flere rapporter i de angivne valutaer. Du kan få vist disse rapporter i webfremviseren ved at klikke på knappen <strong>Valuta</strong> og derefter vælge en valuta.</td>
</tr>
<tr class="even">
<td>Datooplysninger gemmes ikke sammen med rapportdefinitionen</td>
<td><ul>
<li>Basisperiode</li>
<li>Basisår</li>
<li>Periode, der er omfattet</li>
</ul>
Kun indstillinger for standardbasisperiode gemmes sammen med rapportdefinitionen.</td>
</tr>
<tr class="odd">
<td>Datooplysninger, der er gemt sammen med rapportdefinitionen</td>
<td><ul>
<li>Rapportdato</li>
<li>Standardbasisperiode</li>
</ul></td>
</tr>
<tr class="even">
<td>Rapporter i gruppe</td>
<td>Tilføje, fjerne og ændre rækkefølgen af rapporter i rapportgruppen.
<ul>
<li>Hvis du vil tilføje rapportdefinitioner til rapportgruppen, skal du dobbeltklikke på rapportgruppen for at åbne den og derefter klikke på <strong>Tilføj</strong>. Markér de rapporter, der skal medtages i rapportgruppen, og klik derefter på <strong>OK</strong>.</li>
<li>Hvis du vil fjerne en rapport fra rapportgruppen, skal du markere den og derefter klikke på <strong>Fjern</strong>.</li>
<li>Hvis du vil ændre den rækkefølge, rapporterne genereres i, skal du vælge en rapport på listen og derefter klikke på <strong>Flyt op</strong> eller <strong>Flyt ned</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Se også
--------

[Økonomirapportering](financial-reporting-intro.md)




