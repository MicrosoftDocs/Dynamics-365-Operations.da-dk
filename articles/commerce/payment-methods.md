---
title: Betalingsmetoder
description: De enkelte betalingstyper, som en detailhandlende accepterer, skal konfigureres, når systemet konfigureres. I denne artikel beskrives de betalingstyper, som du kan konfigurere, og processen for konfigurationen af dem..
author: BrianShook
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.industry: Retail
ms.search.form: RetailTenderTypeTable
ms.openlocfilehash: d16cdf237042471d367adb7081bf34e9c8a9460f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272816"
---
# <a name="payment-methods"></a>Betalingsmetoder

[!include [banner](includes/banner.md)]

De enkelte betalingstyper, som en detailhandlende accepterer, skal konfigureres, når systemet konfigureres. I denne artikel beskrives de betalingstyper, som du kan konfigurere, og processen for konfigurationen af dem..

Detailhandlende kan acceptere forskellige former for betalinger for de produkter og tjenester, de sælger. Selvom kontant er den mest almindelige form for betaling, kan detailhandlende også modtage betaling i form af checks, kort, kuponer osv. De enkelte betalingstyper, som den detailhandlende accepterer, skal konfigureres i Dynamics 365 Commerce, når systemet konfigureres. På følgende liste beskrives de enkelte betalingstyper, der kan konfigureres:

- **Kontant** - Penge i en valutas fysiske form, dvs. sedler og mønter. Denne valuta kan enten være firmaets valuta eller butikkens lokale valuta.
- **Check** – Et omsætningspapir, der angiver betaling af et bestemt beløb i en bestemt valuta, og at det skal trækkes hos en bestemt bank. En check er som regel enten gyldig på ubestemt tid eller i seks måneder efter udstedelsesdatoen, medmindre en anden gyldighedsperiode er angivet. Denne periode varierer, afhængigt af den bank hvorfra checken trækkes. Der findes forskellige typer check, f.eks. ordrecheck, bankcheck, ihændehavercheck og crossede check. Du kan konfigurere checks som betalingsmetode for de enkelte butikker. Checks kan accepteres i den valuta, der enten er defineret på regnskabsniveau eller butiksniveau. Du skal konfigurere checks som betalingsmetode, før du kan acceptere en check som betaling i en butik.
- **Valuta** - Den primære betalingsform bortset fra firmaets standardvaluta. Mønter og sedler er begge valutaformer. Valutabetalingsmetoden repræsenterer alle valutaer, der bruges. Før du kan bruge denne betalingsmetode, skal du konfigurere valutaer og angive oplysninger om kurssatser.
- **Kort** – Alle typer kort, der anvendes, f.eks. debetkort eller kreditkort. Det anbefales, at du konfigurerer én kortbetalingsmetode på organisationsniveau, der repræsenterer alle slags kort. Derefter kan der på butiksniveau konfigureres en betalingsmetode for hvert kort eller sæt af kort, som behandles ved hjælp af de samme indstillinger. Du skal konfigurere de producentkort, der er tilgængelige på markedet, f.eks. debetkort og kreditkort, før du kan acceptere kortene som betaling i en butik.
- **Kreditnota** – Kreditnotaer, der udstedes eller indløses ved kassen. Kreditnotaen kan være en kredit- eller returnota, der udstedes i forhold til retursalg. Hvis kreditnotaer kun indløses delvist, udsteder programmet en ny kreditnota for restbeløbet. Den nye kreditnota får et nyt nummer. En kreditnota kan kun bruges én gang, og i systemet holdes der styr på alle de numre, der er anvendt. Posten kan ses på siden **Kreditnotatabel**. En kunde kan ikke indløse mere end den værdi, der er angivet på kreditnotaen.
- **Gavekort** - Gavekort, der udstedes og indløses ved POS. Der tillades ikke overbetaling i forbindelse med gavekort. Alle gavekort skal have tilknytninger af kortnummer. 
- **Debitorkonto** – Betalinger kan tilskrives en debitorkonto ved kasseapparatet på salgstidspunktet. Du kan også bruge denne betalingsmetode til at indsamle salgsoplysninger eller kundespecifikke rabatter, når kunden foretager en betaling ved hjælp af en anden betalingsmetode. I dette tilfælde skal du definere kundespecifikke oplysninger.
- **Fordelskundepoint** – de point, som kunder akkumulere gennem loyalitetsprogrammer. Hvis du opretter loyalitetsprogrammer, kan kunderne få point og indløse dem på forskellige måder. I nogle loyalitetsprogrammer kan kunder f.eks. indløse fordelskundepoint i form af en rabat eller endda bruge dem som en form for betaling.

Hvis du vil konfigurere betalingsmetoder, skal du udføre følgende opgaver.

1. Konfigurer betalingsmåder for en organisation. Opret de betalingsmetoder, der accepteres af hele organisationen.
2. Oprettelse af korttyper og kortnumre i hele organisationen. Hvis der skal accepteres kredit- eller debetkort, skal du oprette én betalingsmetode for kort og derefter oprette korttyper og kortnumre, der gælder for hele organisationen.
3. Konfigurer betalingsmetode for butikken. Tilknyt betalingsmetoder til de enkelte butikker, og angiv derefter butiksspecifikke indstillinger for de enkelte betalingsmetoder.
4. Konfigurer betalingsmetoder for butikker. For alle kortbetalingsmetoder, som butikken accepterer, skal du udføre kortopsætningen.

## <a name="handle-change-tendering-for-payment-methods"></a>Håndtere betalingsmetoder til betalingsmiddel for byttepenge

Nogle betalingsmetoder understøtter ikke direkte betalingsmiddel for byttepenge, hvis kunderne skal have penge tilbage i forbindelse med POS-transaktioner. Det er kun betalingsmetoderne **Kontant** og **Valuta**, der kan bruges som betalingsmiddel for byttepenge. 

Til at håndtere sager, hvor betalingsmiddel for byttepenge er påkrævet under en transaktion, men betalingsmetoden ikke understøtter den, kan du definere et **Betalingsmiddel for byttepenge** som betalingsmetode. Når du konfigurerer butiksbetalingsmetoder for butikken, skal du vælge den betalingsmetode, der skal bruges. Angiv derefter en betalingsmetode som betalingsmiddel for byttepenge i feltet **Betalingsmiddel for byttepenge** i sektionen **Byttepenge**. Du kan f.eks. angive **1** for at angive, at kontanter kan bruges som betalingsmiddel for byttepenge.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
