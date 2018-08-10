---
title: Intern fakturering
description: Denne artikel indeholder oplysninger og eksempler om intern fakturering for projekter i Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3d4354316d0c37c6556c0ec3d27a3c62c5afb7b0
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="intercompany-invoicing"></a>Intern fakturering

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger og eksempler om intern fakturering for projekter i Microsoft Dynamics 365 for Finance and Operations.

Din organisation kan have flere divisioner, datterselskaber og andre juridiske enheder, der overfører produkter og tjenester til hinanden i forbindelse med projekter. Den juridiske enhed, der leverer servicer eller produkter, kaldes den *juridiske udlånsenhed*, og den juridiske enhed, der modtager servicen eller produktet, kaldes den *juridiske låneenhed*. 

Følgende illustration viser et typisk scenarie, hvor to juridiske enheder, SI FR (den juridiske låneenhed) og SI USA (den juridiske udlånsenhed), deler ressourcer for at levere et projekt for debitor A. I dette scenarie er SI FR hyret til at levere arbejdet til kunde A. 

[![Eksempel på intern fakturering](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Målet er at gøre omkostningsstyring, indtægtsføring, skatter og afregningspris for interne projektposteringer mere fleksible og effektive. Desuden findes der følgende muligheder:

-   Oprette debitorfakturaer mod et projekt i en juridisk låneenhed ved hjælp af interne timesedler, udgifter og kreditorfakturaer i en juridisk udlånsenhed.
-   Understøtte momsberegninger og indirekte omkostninger.
-   Udsætte indtægtsføring i en juridisk udlånsenhed, og når en juridisk låneenhed skal foretage indtægtsføring af omkostningen.
-   Periodisere indtægt for igangværende arbejde (IGVA) i den juridiske udlånsenhed.
-   Angive afregningspriser, der kan være baseret på forskellige prismodeller. Her er nogle eksempler:
    -   **Antal** – Det beløb, du angiver i feltet **Prissætning** er de faktiske omkostninger pr. antal eller enhed.
    -   **Gebyrbeløb** – Pris/omkostning pr. postering plus det tillægsbeløb, du har angivet i feltet **Prissætning**.
    -   **Gebyrprocent** – Afregningsprisen er pris/omkostning pr. transaktion ganget med den gebyrprocent, du angiver i feltet **Prissætning**.
    -   **Procent af salgspris** – Procentdelen af salgsprisen, der overføres til den juridiske udlånsenhed.
    -   **Beløb under salgspris** – Det beløb, som den juridiske låneenhed indeholder tilbage fra salgspriserne, inden de overfører til den juridiske udlånsenhed.
    -   **Dækningsgrad** – Det tal, du angiver i feltet **Prissætning**, er den dækningsgrad, der er udtrykt som en procentdel af salgsprisen.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Eksempel 1: Konfigurere parametre for intern fakturering
I dette eksempel er USSI er en juridisk udlånsenhed, og dens ressourcer rapporterer tid i forhold til den juridiske låneenhed, FRSI, der ejer kontrakten med slutkunden. Timer og udgifter, som USSI-medarbejdere rapporter, kan indgå i projektfakturaen, som FRSI genererer. Desuden er der en tredje kilde til posteringer, der kan stammer fra den juridiske udlånsenhed (i dette eksempel USSI), når den leverer delte leverandørservices til datterselskaber (f.eks. FRSI) og derefter overfører disse omkostninger til projekter inden for disse datterselskaber. Alle tilsvarende fakturadokumenter og momsberegninger udføres af Finance and Operations. 

I dette eksempel skal FRSI være en debitor i den juridiske enhed for USSI, og USSI skal være kreditor i den juridiske FRSI-enhed. Du kan derefter oprette en intern relation mellem de to juridiske enheder. Følgende procedure viser, hvordan du konfigurerer parametre, så begge juridiske enheder kan deltage i intern fakturering.

1. Opret FRSI som debitor i den juridiske USSI-enhed, og opret USSI som kreditor i den juridiske enhed for FRSI. Der er tre indgangspunkter for de trin, der kræves til denne opgave.

   | Trin |                                                       Indgangspunkt                                                        |                                                                                                                                                                                               Betegnelse                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | I USSI skal du klikke på <strong>Debitor</strong> &gt; <strong>Kunder</strong> &gt; <strong>Alle kunder</strong>. |                                                                                                                                                                  Opret en ny kundepost for FRSI, og vælg debitorgruppen.                                                                                                                                                                  |
   |  B   |    I FRSI skal du klikke på <strong>Kreditor</strong> &gt; <strong>Kreditorer</strong> &gt; <strong>Alle kreditorer</strong>.     |                                                                                                                                                                    Opret en ny kreditorpost for USSI, og vælg kreditorgruppen.                                                                                                                                                                    |
   |  K   |                                  I FRSI skal du åbne den kreditorpost, du netop har oprettet.                                  | I handlingsruden under fanen <strong>Generelt</strong> i gruppen <strong>Konfigurer</strong> skal du klikke på <strong>Internt</strong>. På siden <strong>Intern</strong> under fanen <strong>Handelsforhold</strong> skal du indstille skyderen <strong>Aktiv</strong> til <strong>Ja</strong>. I feltet <strong>Kundens firma</strong> skal du vælge den debitorpost, som du oprettede i trin A. |


2. Klik på **Projektstyring og regnskab** &gt; **Konfiguration** &gt; **Parametre for projektstyring og regnskab**, og klik derefter på fanen **Intern**. Hvordan du skal konfigurere parametrene afhænger af, om du er den juridiske låneenhed eller den juridiske udlånsenhed.
   -   Hvis du er den juridiske låneenhed, skal du vælge den indkøbskategori, der skal bruges til at sammenholde de kreditorfakturaer, der genereres automatisk.
   -   Hvis du den juridiske udlånsenhed, skal du for hver låneenhed vælge en standardprojektkategori for hver posteringstype. Projektkategorier bruges til momskonfiguration, når den fakturerede kategori i interne transaktioner kun findes i den juridiske låneenhed. Du kan vælge at periodisere omsætningen for de interne transaktioner. Denne periodiseringen udføres, når posteringerne bogføres, og den tilbageføres derefter, når den interne faktura bogføres.

3. Klik på **Projektstyring og regnskab** &gt; **Konfiguration** &gt; **Priser** &gt; **Overfør pris**.
4. Vælg en valuta, transaktionstype og afregningsprismodel. Den valuta, der bruges på fakturaen, er den valuta, der er konfigureret i kundeposten for den juridiske låneenhed i den juridiske udlånsenhed. Valutaen bruges til at afstemme poster i afregningspristabellen.
5. Klik på **Finans** &gt; **Opsætning af bogføring** &gt; **Mellemregning**, og opret en relation til USSI og FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Eksempel 2: Oprette og bogføre en intern timeseddel
USSI, den juridiske udlånsenhed, skal oprette og bogføre timesedlen til et projekt fra FRSI, den juridiske låneenhed. Der er to indgangspunkter for de trin, der kræves til denne opgave.

| Trin | Indgangspunkt                                                                       | Betegnelse                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektstyring og regnskab** &gt; **Timesedler** &gt; **Alle timesedler** | Opret en ny timeseddel. På timeseddellinjen i feltet **Juridisk enhed** skal du vælge **FRSI**. Vælg projektet i FRSI i feltet **Projekt-id**. Angiv arbejdstimer for hver dag i ugen. |
| B    | Siden **Timeseddel**                                                                | Når arbejdsprocessen kører, skal du sende timesedlen og notere bilagsnummeret.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Eksempel 3: Oprette og bogføre en intern kreditorfaktura
USSI, den juridiske udlånsenhed, skal oprette og bogføre den interne kreditorfaktura til et projekt fra FRSI, den juridiske låneenhed. Denne kreditorfaktura repræsenterer udliciteret arbejdskraft og udgifter, der blev udført af leverandører, som betales af USSI. Der er to indgangspunkter for de trin, der kræves til denne opgave.

| Trin | Indgangspunkt                                                                                      | Betegnelse                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Kreditor** &gt; **Fakturaer** &gt; **Åbne kreditorfakturaer** &gt; **Ny kreditorfaktura** | Opret en ny kreditorfaktura, og angiv de servicer, der er købt på vegne af FRSI-projektet.                                                                                                                                                                                  |
| B    | Siden **Kreditorfaktura**                                                                      | Angiv linjer, der repræsenterer de outsourcede servicer på vegne af FRSI. I oversigtspanelet **Linjedetaljer** under fanen **Projekt** for fakturalinjen skal du i feltet **Projektfirma** angive **FRSI**. Angiv projektet og tilsvarende oplysninger. Bogfør derefter kreditorfakturaen. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Eksempel 4: Oprette og bogføre den interne kreditorfaktura
USSI, den juridiske udlånsenhed, skal oprette og bogføre den interne faktura. Der er to indgangspunkter for de trin, der kræves til denne opgave.

| Trin | Indgangspunkt                                                                                             | Betegnelse                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektstyring og regnskab** &gt; **Projektfakturaer** &gt; **Intern salgsordrefaktura**.  | Klik på **Ny** at åbne siden **Opret intern faktura**.                                                                                  |
| B    | **Projektstyring og regnskab** &gt; **Projektfakturaer** &gt; **Interne salgsordrefakturaer** | På siden **Opret intern faktura** skal du angive den juridiske enhed, angive den postering, der skal indgå, og derefter klikke på **Søg**. |
| K    | **Projektstyring og regnskab** &gt; **Projektfakturaer** &gt; **Interne salgsordrefakturaer** | Vælg posteringerne, der skal faktureres, eller klik på **Vælg alle** for at fakturere alle posteringerne på listen, og klik derefter på **OK**.                  |
| D    | Siden **Intern faktura**                                                                       | Det interne debitorfakturaforslag vises.                                                                                             |
| E    | Siden **Intern faktura**                                                                       | Klik på **Bogfør**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Eksempel 5: Bogføre kreditorfakturaen og fakturere debitoren
Når den juridisk udlånsenhed, USSI, bogfører den intern debitorfaktura, oprettes en tilsvarende ventende kreditorfaktura i den juridiske låneenhed, FRSI. Når denne kreditorfaktura bogføres, fakturaer FRSI også projektets debitor for de timer, USSI har angivet. Der er tre indgangspunkter for de trin, der kræves til denne opgave.

| Trin | Indgangspunkt                                                                                        | Betegnelse                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Kreditor** &gt; **Fakturaer** &gt; **Ventende kreditorfakturaer**                            | Gennemgå faktura for at kontrollere, at værdierne i timesedlen er inkluderet, og bogfør derefter kreditorfakturaen.                  |
| B    | **Projektstyring og regnskab** &gt; **Projektfakturaer** &gt; **Projektfakturaforslag** | Opret en ny projektfaktura til projektet, og kontrollér, at de timeposteringer, der er bogført, vises.            |
| K    | Siden **Projektfaktura**                                                                       | Vælg projektfakturaen, og klik derefter på **Vis detaljer** for at gennemgå omkostnings- og salgsbeløb. Bogfør derefter fakturaen. |


Yderligere oplysninger finder du i [Konfigurere intern projektfakturering](tasks/configure-intercompany-project-invoicing.md).



