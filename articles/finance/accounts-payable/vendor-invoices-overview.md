---
title: Oversigt over kreditorfakturaer
description: Dette emne indeholder generelle oplysninger om kreditorfakturaer.
author: abruer
manager: AnnBe
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0299eb3470f500bf469c3367f1c426715067a5dc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993310"
---
# <a name="vendor-invoices-overview"></a>Oversigt over kreditorfakturaer

[!include [banner](../includes/banner.md)]

Dette emne indeholder generelle oplysninger om kreditorfakturaer. Kreditorfakturaer er anmodninger om modtaget betaling for produkter og tjenester. Kreditorfakturaer kan repræsentere en regning for løbende ydelser, eller de kan være baseret på indkøbsordrer for specifikke varer og tjenester.

## <a name="vendor-invoices"></a>Kreditorfakturaer

En kreditorfaktura fra en indkøbsordre er produceret, når produkter eller tjenesteydelser modtages i henhold til en indkøbsordre, der blev afgivet med en leverandør. Kreditorfakturaen indeholder et hoved og en eller flere linjer til varer eller tjenester. En kreditorfaktura afslutter cyklussen fra indkøbsordre til produktkvittering til kreditorfaktura.

Selvom nogle kreditorfakturaer er knyttet til en indkøbsordre, kan kreditorfakturaer også indeholde linjer, der ikke svarer til indkøbsordrelinjer. Du kan også oprette kreditorfakturaer, der ikke er knyttet til nogen indkøbsordrer. Disse kreditorfakturaer kan repræsentere igangværende servicer, f.eks. en forsyningsfaktura. Du behøver ikke at referere til en indkøbsordre, når du tilføjer en igangværende service.

Der er flere måder at angive en kreditorfaktura på:

- I kreditorindgangsbogen kan du hurtigt indtaste fakturaer, der ikke refererer til en indkøbsordre, så du kan periodisere udgiften. Ved hjælp af kreditorfakturagodkendelseskladden kan du vælge disse fakturaer og bogføre dem på kreditorsaldoen for at tilbageføre periodiseringen.
- Med kreditorfakturajournalen kan du hurtigt indtaste fakturaer, der ikke refererer til en indkøbsordre i et enkelt trin.
- Sammen med kreditorfakturapuljen kan du med kreditorindgangsbogen hurtigt indtaste fakturaer for at periodisere udgiften. Du kan åbne tilknyttede indkøbsordrer senere for at bogføre fakturaen mod udgiftskontoen.
- Med siderne **Åbne kreditorfakturaer** og **Afventende kreditorfakturaer** kan du oprette kreditorfakturaer fra bekræftede indkøbsordrer.

Den følgende diskussion indeholder flere oplysninger om, hvordan du kan bruge siden **Åbne kreditorfakturaer** eller **Afventende kreditorfakturaer** til at oprette en kreditorfaktura fra en indkøbsordre.

## <a name="understanding-invoice-line-quantities"></a>Sådan skal du forstå fakturalinjeantal

Når du åbner en kreditorfaktura fra en relateret indkøbsordre, opretter systemet fakturalinjer fra indkøbsordren. Systemet, der tager mængderne som standard fra produktkvitteringen. Du kan dog bruge en eller flere af følgende standardfunktionsmåder:

- **Modtagelse nu-antal** – Brug denne indstilling til delleverancer. Systemet indstiller standardværdien i feltet **Antal** stammer fra det antal, der er angivet i feltet **Modtag nu** på indkøbsordren.
- **Bestilt antal** – Brug denne indstilling til fuldførte forsendelser. Systemet indstiller standardværdien i feltet **Antal** stammer fra det antal, der er angivet i feltet **Bestilt** på indkøbsordren.
- **Registreret antal** – Brug denne indstilling, hvis varen kræver registrering, som angivet på siden **Varemodelgrupper**. Standardværdien i feltet **Antal** er det fysisk opdaterede antal, der er registreret.
- **Antal produktkvitteringer** – Brug denne indstilling, hvis der allerede er modtaget en produktkvittering for ordren. Systemet tager standardværdien i feltet **Antal** stammer fra det samlede antal tilgængelige produktkvitteringer.
- **Registreret antal og tjenester** – Brug denne indstilling, hvis der er registreret antal i modtagelseskladder for lagerførte varer eller ikke-lagerførte varer. Denne indstilling omfatter også tjenester, uanset om de er registreret.

Hvis din juridiske enhed bruger sammenholdelse af kreditorfakturaer, kan du se resultaterne af den mængde, der passer i kolonnen **Antal afstemte produktkvitteringer**. Du kan også bruge knappen **Detaljer om sammenholdelse** under fanen **Gennemgang** i handlingsruden for at få vist resultaterne af den tilsvarende mængde.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Tilføje en linje, der ikke var på indkøbsordren

Du kan tilføje en linje, der ikke var på indkøbsordren, til kreditorfakturaen. Du skal vælge et varenummer eller en indkøbskategori. Du kan derefter tilføje mængder, priser og beløb på linjen. Linjen medtages kun i sammenholdelsespolitikker for fakturatotaler.

## <a name="submitting-a-vendor-invoice-for-review"></a>Sende en kreditorfaktura til gennemsyn

Din organisation bruger måske arbejdsgange til at administrere gennemsynsprocessen for kreditorfakturaer. Gennemsyn via arbejdsgang kan være påkrævet for fakturahovedet, fakturalinjen eller begge dele. Arbejdsgangskontrolelementerne gælder for hovedet eller linjen, afhængigt af hvor fokus er, når du vælger kontrolelementet. I stedet for knappen **Bogfør** får du vist knappen **Send**, som du kan bruge til at sende kreditorfakturaen gennem evalueringsprocessen.

### <a name="preventing-invoice-from-being-submitted-to-workflow"></a>Forhindre faktura i at blive sendt til arbejdsgang 

Du kan bruge følgende forskellige metoder til at forhindre, at der sendes en faktura til en arbejdsgang.

- **Fakturatotalen og den registrerede total er forskellige.** Den person, der har sendt fakturaen, modtager en påmindelse om, at totalerne ikke er ens. Påmindelsen giver mulighed for at rette saldi, inden fakturaen sendes til arbejdsgangen igen. Denne funktion er tilgængelig, hvis parameteren **Forbyd afsendelse til arbejdsgang, når fakturatotalen og den registrerede slutsaldo ikke er ens** på siden **Funktionsstyring** er slået til. 

- **Fakturaen indeholder ikke-allokerede gebyrer.** Den person, der sendte fakturaen, vil modtage en påmindelse om, at fakturaen har ikke-allokerede gebyrer, så fakturaen kan rettes, før den sendes til arbejdsgangen. Denne funktion er tilgængelig, hvis parameteren **Forbyd afsendelse til arbejdsgang, når der er ikke-allokerede gebyrer på en kreditorfaktura** på siden **Funktionsstyring** er slået til.

- **Faktura indeholder samme fakturanummer som en anden bogført faktura.** Den person, der sendte fakturaen, vil modtage en påmindelse om, at der findes en faktura med et duplikeret fakturanummer, så den kan rettes, før den sendes til arbejdsgangen. Denne påmindelse vises, når kreditorparameteren med navnet **Tjek det anvendte fakturanummer** er indstillet til **Afvis dublet**. Denne funktion er tilgængelig, hvis parameteren **Forbyd afsendelse til arbejdsgang, når fakturanummeret allerede findes på en bogført faktura, og dit system ikke er konfigureret til at acceptere for identiske fakturanumre** på siden **Funktionsstyring** er slået til.  

## <a name="matching-vendor-invoices-to-product-receipts"></a>Sammenholde kreditorfakturaer med produktkvitteringer

Du kan angive og gemme oplysninger om kreditorfakturaer, og du kan sammenholde fakturalinjer med produktkvitteringslinjer. Du kan også sammenholde delmængder for en linje.

Du kan oprette en kreditorfaktura, der er baseret på de linjeelementer i produktkvitteringen, som er modtaget til og med dags dato, selvom alle varerne i en bestemt indkøbsordre endnu ikke er modtaget. Du kan f.eks. bruge denne indstilling, hvis en kreditor sender én faktura pr. måned, som skal dække alle de leverancer, der er sendt i den pågældende måned. Hver produktkvittering repræsenterer en dellevering eller en komplet levering af varerne i indkøbsordren.

Når en faktura er i arbejdsgangen, kan godkenderen opdatere fakturaantal, så de svarer til værdien i feltet **Antal til modtagelse af produktkvittering**. Dette gør det ved at vælge funktionen **Opdater fakturaantal for at af svare til produktkvitteringer i arbejdsflow** i arbejdsområdet **Funktionsstyring** og vælge **Aktivér**. Hvis en godkender i arbejdsflowet har fjernet alle forekomster fra alle produktkvitteringerne fra fakturalinjen, slettes fakturalinjen. Når denne funktion ikke er aktiveret, opdateres fakturaantal ikke for fakturaer i arbejdsflowet.

Når du bogfører fakturaen, opdateres antallet for **Fakturarestmængde** for de enkelte varer med de samlede modtagne antal fra de valgte produktkvitteringer. Hvis både antallet **Fakturarestmængde** og antallet **Levér rest** for alle varer i indkøbsordren er 0 (nul), ændres indkøbsordrens status til **Faktureret**. Hvis antallet for **Fakturarestmængde** ikke er 0 (nul), forbliver status for indkøbsordren uændret, og der kan bogføres ekstra fakturaer for den.

Denne indstilling antager, at der er bogført mindst én produktkvittering for indkøbsordren. Kreditorfakturaen er baseret på disse produktkvitteringer og afspejler antallene i dem. De økonomiske oplysninger til fakturaen er baseret på de oplysninger, der angives, når du bogfører fakturaen.

Du kan finde flere oplysninger under [Registrere kreditorfaktura og sammenligne med modtaget antal](../accounts-payable/tasks/record-vendor-invoice-match-against-received-quantity.md).

## <a name="configure-an-automated-task-for-vendor-invoice-workflow-to-post-the-vendor-invoice-using-a-batch-job"></a>Konfigurere en automatisk opgave for arbejdsgangen for kreditorfakturaer til bogføring af kreditorfakturaen ved hjælp af et batchjob

Du kan føje en automatisk bogføringsopgave til arbejdsgangen for kreditorfakturaer, så fakturaer behandles i et batch. Når fakturaer bogføres i en batch, kan processen fortsætte uden at vente på, at bogføringen er færdig, hvilket forbedrer den overordnede ydeevne for alle opgaver, der er sendt til arbejdsgangen.

Hvis du vil bogføre en kreditorfaktura i en batch, skal du slå parameteren **Batchbogføring af kreditorfaktura** til på siden **Funktionsstyring**. Arbejdsgange for kreditorfakturaer konfigureres ved at gå til **Kreditor > Opsætning > Kreditorarbejdsgange**.

Du kan få vist opgaven **Bogfør kreditorfakturaen ved hjælp af en batch** i arbejdsgangseditoren, uanset om den funktionsparameteren **Batchbogføring af kreditorfaktura** er aktiveret. Når funktionsparameteren ikke er aktiveret, behandles en faktura, der indeholder **Bogfør kreditorfakturaen ved hjælp af en batchopgave**, ikke i arbejdsgangen, før parameteren er aktiveret. Opgaven **Bogfør kreditorfakturaen ved hjælp af en batch** må ikke bruges i den samme arbejdsgang som den automatiserede opgave **Bogfør kreditorfakturaer** . Desuden skal opgaven **Bogfør kreditorfakturaen ved hjælp af en batch** være det sidste element i konfigurationen af arbejdsgangen.

Du kan angive det antal fakturaer, der skal medtages i batchen, og det antal timer, du vil vente, før du omplanlægger en batch, ved at gå til **Kreditor > Opsætning > Kreditorparametre > Faktura > Fakturaarbejdsgang**. 

## <a name="working-with-multiple-invoices"></a>Arbejde med flere fakturaer

Du kan arbejde med flere fakturaer samtidig og bogføre dem alle på én gang. Hvis du skal oprette flere fakturaer, skal du bruge siden **Afventende kreditorfakturaer**. Hvis du skal bogføre og udskrive flere kreditorfakturaer, skal du bruge fakturagodkendelseskladde. Hvis du bruger fakturagodkendelseskladden, skal mindst én produktkvittering bogføres for indkøbsordren, og der skal bogføres en faktura for indkøbsordren i en indgangsbog. De økonomiske oplysninger for fakturaen stammer fra den faktura, der blev bogført i indgangsbogen.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Gendanne kreditorfakturaer, der er i brug

Når en kreditorfaktura anvendes, kan den ikke redigeres af en anden bruger. Fakturaens tilstand kan dog til tider indikere, at fakturaen er i brug, selv om den ikke redigeres på daværende tidspunkt. Programmet er f.eks. stoppet med at svare, mens en faktura blev redigeret, eller en bruger har måske utilsigtet ladet fakturaen stå åben i programmet.

Du kan anvende siden **Gendan kreditorfakturaer** til at gendanne eller frigive kreditorfakturaer, der er blevet benyttet i mere end fire timer, så de kan redigeres. Du kan åbne denne side fra navigationen **Periodiske opgaver** eller en flise i arbejdsområdet **Indtastning af kreditorfaktura**. Når en faktura er blevet gendannet, vil det være muligt at redigere den fra siden **Kreditorfakturaer**.

Du kan alene tilgå siden **Gendan kreditorfakturaer**, hvis du har fået tildelt sikkerhedsadgangspligterne og -rettighederne for **Gendan kreditorfakturaer i brug**. Derudover skal parametret **Tillad gendannelse af kreditorfaktura** på siden **Kreditorparametre** være slået til.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Nulstille arbejdsgangsstatus for kreditorfakturaer fra Uoprettelig til Kladder

En arbejdsgangsforekomst, der er stoppet på grund af en uoprettelig fejl, har arbejdsgangsstatussen **Uoprettelig**. Når status for en arbejdsgang for en kreditorfaktura er **Uoprettelig**, kan du nulstille den til **Kladde** ved at vælge **Tilbagekald**. Du kan derefter redigere kreditorfakturaen. Denne funktion er tilgængelig, hvis parameteren **Nulstil kladdestatus for leverandørfakturaer fra uoprettelig til kladder** på siden **Administration af funktioner** er aktiveret.

Du kan bruge siden **Arbejdsgangshistorik** for at nulstille arbejdsgangsstatussen til **Kladde**. Du kan åbne denne side fra **Kreditorfaktura**  eller fra navigationen **Almindelig > Forespørgsler > Arbejdsgang**. Hvis du vil nulstille arbejdsgangsstatussen til **Kladde**, skal du vælge **Tilbagekald**. Du kan også nulstille arbejdsgangsstatussen til kladde ved at vælge handlingen **Tilbagekald** på siden **Kreditorfaktura** eller **Afventende kreditorfakturaer**. Når arbejdsgangsstatus er nulstillet til **Kladde**, bliver den tilgængelig for redigering på siden **Kreditorfaktura**.

## <a name="viewing-the-invoice-total-on-the-pending-vendor-invoices-page"></a>Se fakturatotalen på siden Ventende kreditorfakturaer.
Du kan få vist fakturatotalen på siden **Ventende kreditorfakturaer** ved at aktivere parameteren **Vis fakturatotal på ventende kreditorfakturaer** på siden **kreditorparametre**. 



## <a name="additional-resources"></a>Yderligere ressourcer

- [Konfigurer politikker for kreditorfakturaer](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Vigtigste fakturadata i kreditorsystem, der bruger kreditorfaktura](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Indtaste fakturadata under kreditorer ved hjælp af en godkendelseskladde](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Indtaste fakturadata i kreditorsystemet ved hjælp af en fakturapulje](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Registrere en kreditorfaktura i fakturakladden](tasks/record-vendor-invoice-invoice-journal.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]