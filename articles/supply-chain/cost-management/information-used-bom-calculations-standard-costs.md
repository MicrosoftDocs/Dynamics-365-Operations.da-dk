---
title: Oplysninger, der bruges i styklistekalkulationer med standardomkostninger
description: Styklisteberegninger anvender data fra flere kilder ved beregning af standardomkostningerne for en produceret vare. Blandt kilderne er oplysninger om varer, styklisteruter, beregningsformler for indirekte omkostninger og efterkalkulationsversionen.
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcGroup, BOMCalcTable, ProdParmBOMCalc
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 65571
ms.assetid: ca17e6dd-b16a-4bbc-8682-b16345ab9906
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ec6ffe41d6dae10693b1a1ebd6e5012c32bc2e6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "333754"
---
# <a name="information-used-in-bom-calculations-with-standard-costs"></a>Oplysninger, der bruges i styklistekalkulationer med standardomkostninger

[!include [banner](../includes/banner.md)]

Styklisteberegninger anvender data fra flere kilder ved beregning af standardomkostningerne for en produceret vare. Blandt kilderne er oplysninger om varer, styklisteruter, beregningsformler for indirekte omkostninger og efterkalkulationsversionen.

Der bruges blandt andet følgende oplysninger om købsvaren i en standardstyklistekalkulation:
-   Omkostninger − Omkostningerne for en købt vare vedligeholdes som områdespecifikke omkostningsposter i en efterkalkulationsversion for standardomkostninger. Hver omkostningspost har en ikrafttrædelsesdato, og datoen for styklisteberegningen bestemmer, hvilken omkostningspost der skal bruges. En styklisteberegning med en af fremtidig beregningsdato kan f.eks. bruge en omkostningspost med en ventende status og en fremtidig ikrafttrædelsesdato.
-   Kostprisgruppe – Kostprisgrupper, der knyttes til en købsvare, udgør grundlaget for segmentering af omkostninger i de beregnede kostpriser for en produceret vare.
-   Advarselsbetingelser, der er integreret i varens styklisteberegningsgruppe, gør det muligt for styklisteberegningen at identificere potentielle problemer. Det kan være, når den købte vare har nulomkostninger, et antal på nul i en stykliste eller en forældet omkostningspost. Du kan tilsidesætte disse gældende advarselssituationer, når du starter en styklisteberegning.

Der bruges blandt andet følgende oplysninger om den producerede vare i en standardstyklistekalkulation:
-   Standardordreantal for lager – Varens standardordreantal for lager fungerer som standardpartistørrelsen til amortisering af konstante omkostninger i en styklisteberegning. Beregningspartistørrelsen afspejler også multiplen for ordreantallet, hvis den er angivet.
-   Advarselsbetingelser, der er integreret i varens styklisteberegningsgruppe, gør det muligt for styklisteberegningen at identificere potentielle problemer. Et eksempel kunne være, at den fremstillede vare ikke har en stykliste eller en rute. Du kan tilsidesætte disse gældende advarselssituationer, når du starter en styklisteberegning.

Der bruges blandt andent følgende styklisteoplysninger i en styklisteberegning for standardomkostninger:
-   Styklisteversion – Den styklisteversion, der er knyttet til den producerede vare, har Gælder fra- og Gælder til-datoer og en status for Godkendt og Aktiv. Styklisteversionen kan gælde for hele firmaet eller være lokationsspecifik, og den kan også konfigureres til at afspejle pausepunkter for antal.
-   Antal for styklistelinjeelement − En komponent har typisk et variabelt behovsantal, men det kan være en konstant. Komponentantallet udtrykkes typisk ved fremstilling af én overordnet vare, men de kan være angivet pr. 100 eller pr. 1000 for at imødegå problemer med decimalnøjagtighed. Komponentantallet kan også beregnes på basis af målinger.
-   Spil for tyklistelinjeelement − En komponent kan have et variabelt eller et konstant antal for planlagt spild.
-   Gyldighedsdatoer for styklistelinjelement – En komponent kan Gyldig fra- og Gyldig til-datoer.
-   Produktionstype for styklistelinjeelement – Kostprislotstørrelsen til amortisering af konstante omkostninger vil afspejle antallet for styklisteberegningen og udfoldningstilstanden Fremstil til ordrer, da styklisteberegningen antager, at den fremstillede komponent vil blive produceret i det nøjagtige antal og ikke i standardordreantallet.
-   Understykliste for en fremstillet komponent – En fremstillet komponent kan konfigureres til at have en angivet styklisteversion, som vil blive brugt i en styklisteberegning i stedet for varens aktuelt aktive styklisteversion.
-   Underrute for en fremstillet komponent – En fremstillet komponent kan konfigureres til at have en angivet ruteversion, som vil blive brugt i en styklisteberegning i stedet for varens aktuelt aktive ruteversion.
-   Operationsnummer og virkningen af spildprocenter for operationer – Operationsnummeret knytter en komponent til en bestemt operation, og operationer kan have en spildprocent. Tilknytningen betyder, at styklisteberegninger kan medtage spildprocenter og akkumulerede spildprocenter på tværs af flere operationer i beregningen af behovsantal for komponenten.
-   Ignorer styklistelinjeelementet i omkostningsberegnininger – I forbindelse med styklisteberegninger kan en komponent igoreres.

De operationsressourceoplysninger, der bruges i en styklisteberegning for en standardkostpris, omfatter:
-   Timeomkostninger – De timeomkostninger, der er knyttet til en operationsressource, udtrykkes som omkostningsarter, der tilknyttes opstillingstid og procestid. Disse omkostningsarter skal angives for ressourcegrupper og operationsressourcer. Det timeomkostninger, der er forbundet med en omkostningsart, kan være lokationsspecifikke eller gælde for hele firmaet.
-   Enhedsomkostninger – I nogle produktionsmiljøer tildeles ressourceomkostninger pr. outputenhed, hvilket ville være angivet som en anden omkostningsart for antal. De antalsrelaterede omkostninger kan f.eks. afspejle styksatserne for arbejdsløn, eller en malingsproducent kan tildele ressourceomkostninger pr. liter af produktoutput.
-   Overstyring af ressourceoplysninger på ruteoperationer – Ressourceoplysningerne om omkostningsarter vil blive nedarvet af operationer, hvor disse oplysninger kan blive tilsidesat. Styklisteberegninger vil bruge de oplysninger om omkostningsart, der er angivet på ruteoperationerne.
-   Kostprisgruppe for en omkostningsart – En kostprisgrupper, der knyttes til en omkostningsart, udgør segmenteringen af omkostninger i de beregnede kostpriser for en produceret vare. Der kan f.eks. bruges en anden kostprisgruppe til at segmentere den beregnede omkostning, der er tilknyttet maskiner og arbejdsløn eller opstilling og procestid.

Der bruges blandt andet følgende ruteoplysninger ved en styklisteberegning for en standardkostpris:
-   Ruteversion – Den ruteversion, der er knyttet til den producerede vare, har Gælder fra- og Gælder til-datoer og en status for Godkendt og Aktiv. Ruteversionen skal være lokationsspecifik, og den kan også konfigureres til at afspejle pausepunkter for antal.
-   Ruteoperationstid – Der kan angives tider for procestid og opstillingstid. Timetallet udtrykkes typisk ved fremstilling af én overordnet vare, men de kan være angivet pr. 100 eller pr. 1000 for at imødegå problemer med decimalnøjagtighed.
-   Ruteoperationstid for sekundære ressourcer – En sekundær ressource (identificeres ved sekundær prioritet) har samme operationsnummer som den primære ressource, og den har samme ruteoperationstid. En operation kan f.eks. kræve en maskine som primær ressource og arbejdsløn og værktøj som sekundære ressourcer.
-   Spildprocent for ruteoperation – Styklisteberegninger medregner spildprocenter og akkumulerede spildprocenter på tværs af flere operationer. Dette gælder for den tid, der kræves for ruteoperationer, og den tid der kræves for komponenter, der er tilknyttet operationsnumre.
-   Omkostningsarter for en ruteoperation − Operationsressourceoplysninger om omkostningsarter nedarves af operationer, når disse oplysninger kan tilsidesættes. Styklisteberegninger vil bruge de oplysninger om omkostningsart, der er angivet på ruteoperationerne.

Der bruges blandt andet følgende oplysninger om indirekte produktionsomkostninger ved en styklisteberegning for en standardkostpris:
-   Tillæg – En beregningsformel for tillæg afspejler en procent af værdien, f.eks. 100 procent, som knyttes til en bestem kostprisgruppe, f.eks. arbejdsløn.
-   SAts – En beregningsformel for en sats afspejler et beløb pr. enhed, f.eks. kr. 10,00 pr. time, som knyttes til en bestem kostprisgruppe, f.eks. arbejdsløn.
-   Timebaserede vs. materialebaserede indirekte omkostninger − De indirekte produktionsomkostninger kan knyttes til ruteoperationer eller materialekomponenter.

Der bruges blandt andet følgende oplysninger om efterkalkulationsversioner ved en styklisteberegning for en standardkostpris:
-   Efterkalkulationstype – Efterkalkulationsversionen skal indeholde standardkostpriser. Der kan gælde flere begrænsninger for styklisteberegninger, der benytter standardomkostninger. Disse begrænsninger angiver f.eks., at der skal medtages tillæg i enhedsomkostningerne, og at udfoldningstilstanden for styklistebereginger skal være Et enkelt niveau.
-   Tilladt reserveprincip − Efterkalkulationsversionen kan tillade brugen af et reserveprincip, f.eks. brug en bestemt efterkalkulation eller de aktive omkostningsposter. Det tilladte reserveprincip gælder typisk for en efterkalkulationsversion, der repræsenterer de trinvise opdateringer i en tilgang for omkostningsopdateringer.
-   Blokeringsflag for ventende omkostninger – Der kan bruges et blokeringsflag for at forhindre styklisteberegning af ventende omkostninger for producerede varer.
-   Angive fra-dato − Den angivne fra-dato vil fungere som standardberegningsdato for alle styklisteberegnminger, hvor efterkalkulationsversionen bruges.
-   Angivet lokation – En angiven lokation vil begrænse styklisteberegningerne til en enkelt lokation.
-   Indholdet af efterkalkulationen skal indeholde omkostninger – Indholdet skal indeholde omkostninger. Det kan vælges, at det kan indeholde salgspriser med henblik på beregning af vejledende salgspriser for producerede varer.

Flere informationskilder kan angives, når du starter en styklistekalkulation. Dette omfatter webstedet, beregningsdatoen og efterkalkulationsversionen.





