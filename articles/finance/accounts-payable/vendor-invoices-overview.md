---
title: Oversigt over kreditorfakturaer
description: Dette emne indeholder generelle oplysninger om kreditorfakturaer. Kreditorfakturaer er anmodninger om betaling for produkter og tjenester, der er modtaget. Kreditorfakturaer kan repræsentere en regning for løbende ydelser, eller de kan være baseret på indkøbsordrer for specifikke varer og tjenester.
author: abruer
manager: AnnBe
ms.date: 07/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 616d3f5560d18c7fdd8a092c3fbca0fde44be069
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570419"
---
# <a name="vendor-invoices-overview"></a>Oversigt over kreditorfakturaer

[!include [banner](../includes/banner.md)]

Dette emne indeholder generelle oplysninger om kreditorfakturaer. Kreditorfakturaer er anmodninger om betaling for produkter og tjenester, der er modtaget. Kreditorfakturaer kan repræsentere en regning for løbende ydelser, eller de kan være baseret på indkøbsordrer for specifikke varer og tjenester.

## <a name="vendor-invoices"></a>Kreditorfakturaer

En kreditorfaktura fra en indkøbsordre er en faktura, der er produceret, når produkter eller tjenesteydelser modtages i henhold til en indkøbsordre, der blev afgivet med en leverandør. Kreditorfakturaen indeholder et hoved og en eller flere linjer til varer eller tjenester. En kreditorfaktura afslutter cyklussen fra indkøbsordre til produktkvittering til kreditorfaktura.

Selvom nogle kreditorfakturaer er knyttet til en indkøbsordre, kan kreditorfakturaer også indeholde linjer, der ikke svarer til indkøbsordrelinjer. Du kan også oprette kreditorfakturaer, der ikke er knyttet til nogen indkøbsordrer. Disse kreditorfakturaer kan repræsentere løbende tjenester som et værktøj til regning, og du behøver ikke at henvise til en indkøbsordre, når du tilføjer dem.

Der er flere måder at angive en kreditorfaktura på:

- I kreditorindgangsbogen kan du hurtigt indtaste fakturaer, der ikke refererer til en indkøbsordre, så du kan periodisere udgiften. Ved hjælp af kreditorfakturagodkendelseskladden kan du vælge disse fakturaer og bogføre dem på kreditorsaldoen for at tilbageføre periodiseringen.
- Med kreditorfakturajournalen kan du hurtigt indtaste fakturaer, der ikke refererer til en indkøbsordre i et enkelt trin.
- Sammen med kreditorfakturapuljen kan du med kreditorindgangsbogen hurtigt indtaste fakturaer for at periodisere udgiften. Du kan åbne tilknyttede indkøbsordrer senere for at bogføre fakturaen mod udgiftskontoen.
- Med siderne **Åbne kreditorfakturaer** og **Afventende kreditorfakturaer** kan du oprette kreditorfakturaer fra bekræftede indkøbsordrer.

Den følgende diskussion indeholder flere oplysninger om, hvordan du kan bruge siden **Åbne kreditorfakturaer** eller **Afventende kreditorfakturaer** til at oprette en kreditorfaktura fra en indkøbsordre.

## <a name="understanding-invoice-line-quantities"></a>Sådan skal du forstå fakturalinjeantal

Når du åbner en kreditorfaktura fra en relateret indkøbsordre, oprettes der fakturalinjer fra indkøbsordren. Mængderne tages som standard fra antallet på produktkvitteringen. Du kan dog bruge en eller flere af følgende standardfunktionsmåder:

- **Modtagelse nu-antal** – Brug denne indstilling til delleverancer. Standardværdien i feltet **Antal** stammer fra det antal, der er angivet i feltet **Modtag nu** på indkøbsordren.
- **Bestilt antal** – Brug denne indstilling til fuldførte forsendelser. Standardværdien i feltet **Antal** stammer fra det antal, der er angivet i feltet **Bestilt** på indkøbsordren.
- **Registreret antal** – Brug denne indstilling, hvis varen kræver registrering, som angivet på siden **Varemodelgrupper**. Standardværdien i feltet **Antal** er det fysisk opdaterede antal, der er registreret.
- **Antal produktkvitteringer** – Brug denne indstilling, hvis der allerede er modtaget en produktkvittering for ordren. Standardværdien i feltet **Antal** stammer fra det samlede antal tilgængelige produktkvitteringer.
- **Registreret antal og tjenester** – Brug denne indstilling, hvis der er registreret antal i modtagelseskladder for lagerførte varer eller ikke-lagerførte varer. Denne indstilling omfatter også tjenester, uanset om de er registreret.

Hvis din juridiske enhed bruger sammenholdelse af kreditorfakturaer, kan du se resultaterne af den mængde, der passer i kolonnen **Antal afstemte produktkvitteringer**. Du kan også bruge knappen **Detaljer om sammenholdelse** under fanen **Gennemgang** i handlingsruden for at få vist resultaterne af den tilsvarende mængde.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Tilføje en linje, der ikke var på indkøbsordren

Du kan tilføje en linje, der ikke var på indkøbsordren, til kreditorfakturaen. Du skal vælge et varenummer eller en indkøbskategori. Du kan derefter tilføje mængder, priser og beløb på linjen. Linjen medtages kun i sammenholdelsespolitikker for fakturatotaler.

## <a name="submitting-a-vendor-invoice-for-review"></a>Sende en kreditorfaktura til gennemsyn

Din organisation bruger måske arbejdsgange til at administrere gennemsynsprocessen for kreditorfakturaer. Gennemsyn via arbejdsgang kan være påkrævet for fakturahovedet, fakturalinjen eller begge dele. Arbejdsgangskontrolelementerne gælder for hovedet eller linjen, afhængigt af hvor fokus er, når du vælger kontrolelementet. I stedet for knappen **Indlæg** får du vist knappen **Send**, som du kan bruge til at sende kreditorfakturaen gennem evalueringsprocessen.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Sammenholde kreditorfakturaer med produktkvitteringer

Du kan angive og gemme oplysninger om kreditorfakturaer, og du kan sammenholde fakturalinjer med produktkvitteringslinjer. Du kan også sammenholde delmængder for en linje.

Du kan oprette en kreditorfaktura, der er baseret på de linjeelementer i produktkvitteringen, som er modtaget til og med dags dato, selvom alle varerne i en bestemt indkøbsordre endnu ikke er modtaget. Du kan f.eks. bruge denne indstilling, hvis en kreditor sender én faktura pr. måned, som skal dække alle de leverancer, der er sendt i den pågældende måned. Hver produktkvittering repræsenterer en dellevering eller en komplet levering af varerne i indkøbsordren.

Når du bogfører fakturaen, opdateres antallet for **Fakturarestmængde** for de enkelte varer med de samlede modtagne antal fra de valgte produktkvitteringer. Hvis både antallet **Fakturarestmængde** og antallet **Levér rest** for alle varer i indkøbsordren er 0 (nul), ændres indkøbsordrens status til **Faktureret**. Hvis antallet for **Fakturarestmængde** ikke er 0 (nul), forbliver status for indkøbsordren uændret, og der kan bogføres ekstra fakturaer for den.

Denne indstilling antager, at der er bogført mindst én produktkvittering for indkøbsordren. Kreditorfakturaen er baseret på disse produktkvitteringer og afspejler antallene i dem. De økonomiske oplysninger til fakturaen er baseret på de oplysninger, der angives, når du bogfører fakturaen.

Du kan finde flere oplysninger under [Registrere kreditorfaktura og sammenligne med modtaget antal](../accounts-receivable/tasks/record-vendor-invoice-match-against-received-quantity.md).

## <a name="working-with-multiple-invoices"></a>Arbejde med flere fakturaer

Du kan arbejde med flere fakturaer samtidig og bogføre dem alle på én gang. Hvis du skal oprette flere fakturaer, skal du bruge siden **Afventende kreditorfakturaer**. Hvis du skal bogføre og udskrive flere kreditorfakturaer, skal du bruge fakturagodkendelseskladde. Hvis du bruger fakturagodkendelseskladden, skal mindst én produktkvittering bogføres for indkøbsordren, og der skal bogføres en faktura for indkøbsordren i en indgangsbog. De økonomiske oplysninger for fakturaen stammer fra den faktura, der blev bogført i indgangsbogen.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Gendanne kreditorfakturaer, der er i brug

Når en kreditorfaktura anvendes, kan den ikke redigeres af en anden bruger. Fakturaens tilstand kan dog til tider indikere, at fakturaen er i brug, selv om den ikke redigeres på daværende tidspunkt. Programmet er f.eks. stoppet med at svare, mens en faktura blev redigeret, eller en bruger har måske utilsigtet ladet fakturaen stå åben i programmet.

Du kan anvende siden **Gendan kreditorfakturaer** til at gendanne eller frigive kreditorfakturaer, der er blevet benyttet i mere end fire timer, så de kan redigeres. Du kan åbne denne side fra navigationen **Periodiske opgaver** eller en flise i arbejdsområdet **Indtastning af kreditorfaktura**. Når en faktura er blevet gendannet, vil det være muligt at redigere den fra siden **Kreditorfakturaer**.

Du kan alene tilgå siden **Gendan kreditorfakturaer**, hvis du har fået tildelt sikkerhedsadgangspligterne og -rettighederne for **Gendan kreditorfakturaer i brug**. Derudover skal parametret **Tillad gendannelse af kreditorfaktura** på siden **Kreditorparametre** være slået til.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Nulstille arbejdsgangsstatus for kreditorfakturaer fra Uoprettelig til Kladder

En arbejdsgangsforekomst, der er stoppet på grund af en uoprettelig fejl, har arbejdsgangsstatussen **Uoprettelig**. Når status for en arbejdsgang for en kreditorfaktura er **Uoprettelig**, kan du nulstille den til **Kladde** ved at vælge **Tilbagekald**. Du kan derefter redigere kreditorfakturaen. Denne funktion er tilgængelig, hvis parameteren **Nulstil kladdestatus for arbejdsgang for kreditorfakturaer** på siden **Administration af funktioner** er aktiveret.

Du kan bruge siden **Arbejdsgangshistorik** for at nulstille arbejdsgangsstatussen til **Kladde**. Du kan åbne denne side fra **Kreditorfaktura**  eller fra navigationen **Almindelig > Forespørgsler > Arbejdsgang**. Hvis du vil nulstille arbejdsgangsstatussen til **Kladde**, skal du vælge **Tilbagekald**. Du kan også nulstille arbejdsgangsstatussen til kladde ved at vælge handlingen **Tilbagekald** på siden **Kreditorfaktura** eller **Afventende kreditorfakturaer**. Når arbejdsgangsstatus er nulstillet til **Kladde**, bliver den tilgængelig for redigering på siden **Kreditorfaktura**.



## <a name="additional-resources"></a>Yderligere ressourcer

- [Konfigurere politikker for kreditorfakturaer](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Indtaste fakturadata under kreditorer ved hjælp af en kreditorfaktura](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Indtaste fakturadata under kreditorer ved hjælp af en godkendelseskladde](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Indtaste fakturadata i kreditorsystemet ved hjælp af en fakturapulje](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Registrere en kreditorfaktura i fakturakladden](tasks/record-vendor-invoice-invoice-journal.md)
