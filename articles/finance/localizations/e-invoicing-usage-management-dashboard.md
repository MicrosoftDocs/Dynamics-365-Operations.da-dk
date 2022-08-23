---
title: Dashboardet Brugsstyring
description: Denne artikel forklarer, hvordan du bruger dashboardet Brugsstyring til at overvåge brugen af tjenesten Elektronisk fakturering og altid overholder angivne standarder.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 74f3d88faf192474c177da971a9f7bb0e58e1279
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272203"
---
# <a name="usage-management-dashboard"></a>Dashboardet Brugsstyring

[!include [banner](../includes/banner.md)]

Dashboardet **Brugsstyring** hjælper dig med at overvåge brugen af den elektroniske faktureringsservice og hjælper derfor din organisation med at overholde månedlig brug. Overholdelse bestemmes ved at beregne afsendelsesvolumen og sammenligne den med den anskaffede volumen for afsendelser for at identificere eventuelle afvigelser mellem den anskaffede volumen og den anvendte volumen.

Dashboardet indeholder følgende indikatorer:

- En omkostningsindikator, som du kan bruge til at overvåge forbruget med henblik på licensoverholdelse:

    - Forbrug pr. måned (eksport)

- Tre driftsmæssige indikatorer, som du kan bruge til at spore brugen af tjenesten til elektronisk fakturering til administrationsformål:

    - Brug af funktion
    - Brug efter miljø
    - Forbrug pr. måned (import)

## <a name="measurement-scope"></a>Omfang af mål

- Måleenhed: 

    Dashboardet **Brugsstyring** tæller afsendelsen af forretningsdokumenter og importerede elektroniske fakturaer.

- Organisation: 

    Optælling opsummeres ud fra organisationens lejer-id, uanset antallet af forekomster af Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management eller antallet af juridiske enheder, hvor tjenesten til elektronisk fakturering er aktiveret.


## <a name="indicator-usage-per-month-export"></a>Indikator: Brug pr. måned (eksport)

Denne indikator indeholder oplysninger om de elektroniske fakturaer, som din organisation udsteder i løbet af en defineret periode.

### <a name="scope"></a>Område
- Antallet af forretningsdokumenter, der afsendes fra Finance og Supply Chain Management til tjenesten for elektronisk fakturering, uanset antallet af linjer i forretningsdokumenterne.
- Antallet af afsendte forretningsdokumenter, der er blevet korrekt behandlet af den elektroniske faktureringsservice. Et dokument anses for at være behandlet korrekt, når flowet af handlinger, der er defineret i funktionsopsætningen, er fuldført.

> [!NOTE]
> Når en elektronisk faktura sendes til en ekstern webtjeneste, er optællingen uafhængig af resultaterne af behandling af webtjenesten (accepterede, afviste eller skemavalideringsfejl). Hvis webtjenesten har modtaget og besvaret anmodningen fra den elektroniske faktureringstjeneste, betragtes afsendelsen som en gyldig optælling.

- **Undtagelse:** Forretningsdokumenter tælles ikke med, hvis de sendes fra Finance og Supply Chain Management til den elektroniske faktureringsservice, f.eks. i de scenarier, hvor samme forretningsdokument skal sendes igen for at ændre status for den elektroniske faktura. Udstedelsen af en brasiliansk elektronisk faktura (regnskabsdokumentet) er f.eks. gyldig, mens annulleringsanmodningen for den ikke er medregnet.


### <a name="calculation"></a>Udregning

Saldoberegningen foretages på følgende måde:

Saldo = Gratis + Købt – Brugt

Placering:

- Gratis:
  
    En gratis volumen af forretningsdokumenter, som kunden kan sende pr. måned. Den indeholder en pakke med 100 forretningsdokumenter, der kan sendes til den elektroniske faktureringsservice. Den gratis volumen er ikke akkumuleret, og eventuel resterende saldo overføres ikke til næste periode.
  
- Købt:
  
    En pakke med 1.000 forretningsdokumenter, der kan sendes til den elektroniske faktureringsservice. Denne pakke skal anskaffes af din organisation på månedsbasis. Den købte volumen er ikke akkumuleret, og eventuel resterende saldo overføres ikke til næste periode.
  
- Brugt: 

    Antallet af afsendte forretningsdokumenter til den elektroniske faktureringsservice i henhold til definerede kriterier.
   
> [!IMPORTANT]
> Hvis din organisation planlægger at overskride den månedlige mængde på 100 gratis afsendelser, skal du købe den maksimale mængde for at sikre, at du overholder Microsofts licenspolitik for tjenesten til elektronisk fakturering.
>
> I øjeblikket skal købt volumen angives manuelt i overensstemmelse med anskaffelsesdatoen som flere pakker på 1.000 afsendelser.

## <a name="indicator-usage-by-feature"></a>Indikator: Anvendelse efter funktion

Denne indikator viser brugen af funktioner for elektronisk fakturering til udstedelse af elektroniske fakturaer i en defineret periode.

- Udregning:
  
    Brugt = Antal gange hver enkelt funktion til elektronisk fakturering er blevet brugt under afsendelse af forretningsdokumenter til den elektroniske faktureringsservice.

## <a name="indicator-usage-by-environment"></a>Indikator: Anvendelse efter miljø

Denne indikator viser brugen af servicemiljøer for elektronisk fakturering i en defineret periode.

- Udregning:
    
    Brugt = Antal gange hvert enkelt tjenestemiljø til elektronisk fakturering er blevet brugt under afsendelse af forretningsdokumenter til den elektroniske faktureringsservice.

## <a name="indicator-usage-per-month-import"></a>Indikator: Brug pr. måned (import)

Denne indikator viser omfanget af import af elektroniske fakturaer fra tjenesten Elektronisk fakturering til Finance og Supply Chain Management i en defineret periode.

- Område:

    Elektroniske fakturaer, der importeres til Finance og Supply Chain Management, uanset antallet af linjer, som disse elektroniske fakturaer indeholder.

- Udregning:

    Modtaget = Antal importerede elektroniske fakturaer til Finance og Supply Chain Management.

## <a name="functions"></a>Funktioner
### <a name="purchase"></a>Indkøb

Under fanen **Brug pr. måned (eksport)** skal du vælge **Indkøb** for manuelt at registrere beløbet af anskaffede afsendelser.

Vælg **Ny** for en bestemt dato, og angiv det antal **Pakker**, der er anskaffet på den pågældende dato.

**Antal** beregnes på følgende måde:

Antal = Pakker * 1,000

Det beregnede **Antal** afspejles i det **Købte** fra indikatoren **Forbrug pr. måned (eksport)**.

### <a name="update"></a>Vedligeholdelse

Vælg **Opdater** i handlingsruden for at opdatere beregningen og opdatere de data, der vises på siden og i diagrammet.

### <a name="reset-history-data"></a>Nulstil historikdata

Vælg **Nulstil historikdata** i handlingsruden for at opdatere den database, som indikatorerne beregnes fra.




> [!NOTE]
> Dashboardet **Brugsstyring** viser ikke pengebeløb. I stedet viser det kun volumen af optalte afsendelser og importerede dokumenter.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
