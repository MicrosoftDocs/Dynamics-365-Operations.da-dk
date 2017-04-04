---
title: Betalingsmetoder
description: "Hver betalingstype, der accepterer en detailhandler, der skal være konfigureret i Retail og handel i Microsoft Dynamics 365 for operationer, når systemet er konfigureret. I denne artikel beskrives de betalingstyper, som du kan konfigurere, og processen for konfigurationen af dem.."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: MargoC
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b887fc5d03ea8982515e92725ce98cc416e56f9e
ms.openlocfilehash: 011beec07bf1ab858892ab1c374f1acf3839e877
ms.lasthandoff: 03/31/2017


---

# <a name="payment-methods"></a>Betalingsmetoder

Hver betalingstype, der accepterer en detailhandler, der skal være konfigureret i Retail og handel i Microsoft Dynamics 365 for operationer, når systemet er konfigureret. I denne artikel beskrives de betalingstyper, som du kan konfigurere, og processen for konfigurationen af dem..

Detailhandlende kan acceptere forskellige former for betalinger for de produkter og tjenester, de sælger. Selvom kontant er den mest almindelige form for betaling, kan detailhandlende også modtage betaling i form af checks, kort, kuponer osv. Hver betalingstype, der accepterer formidleren skal være konfigureret i Dynamics 365 for operationer - Retail, når systemet er sat op. På følgende liste beskrives hver betalingstype, der kan konfigureres i Dynamics 365 for operationer – Retail:

-   **Kontant** - Penge i en valutas fysiske form, dvs. sedler og mønter. Denne valuta kan enten være firmaets valuta eller butikkens lokale valuta.
-   **Check** – Et omsætningspapir, der angiver betaling af et bestemt beløb i en bestemt valuta, og at det skal trækkes hos en bestemt bank. En check er som regel enten gyldig på ubestemt tid eller i seks måneder efter udstedelsesdatoen, medmindre en anden gyldighedsperiode er angivet. Denne periode varierer, afhængigt af den bank hvorfra checken trækkes. Der findes forskellige typer check, f.eks. ordrecheck, bankcheck, ihændehavercheck og crossede check. Du kan konfigurere checks som betalingsmetode for de enkelte butikker. Checks kan accepteres i den valuta, der enten er defineret på regnskabsniveau eller butiksniveau. Du skal konfigurere checks som betalingsmetode, før du kan acceptere en check som betaling i en butik.
-   **Valuta** - Den primære betalingsform bortset fra firmaets standardvaluta. Mønter og sedler er begge valutaformer. Valutabetalingsmetoden repræsenterer alle valutaer, der bruges i Detail og handel. Før du kan bruge denne betalingsmetode, skal du konfigurere valutaer og angive oplysninger om forretningens kurssatser.
-   **Kort** – alle typer kort, der anvendes i Detail og handel, f.eks. debetkort eller kreditkort. Det anbefales, at du konfigurerer én kortbetalingsmetode på organisationsniveau, der repræsenterer alle slags kort. Derefter kan der på butiksniveau konfigureres en betalingsmetode for hvert kort eller sæt af kort, som behandles ved hjælp af de samme indstillinger. Du skal konfigurere de producentkort, der er tilgængelige på markedet, f.eks. debetkort og kreditkort, før du kan acceptere kortene som betaling i en butik.
-   **Kreditnota** – Kreditnotaer, der udstedes eller indløses ved kassen. Kreditnotaen kan være en kredit- eller returnota, der udstedes i forhold til retursalg. Hvis kreditnotaer kun indløses delvist, udsteder programmet en ny kreditnota for restbeløbet. Den nye kreditnota får et nyt nummer. En kreditnota kan kun bruges én gang, og i systemet holdes der styr på alle de numre, der er anvendt. Posten kan ses på siden **Kreditnotatabel**. En kunde kan ikke indløse mere end den værdi, der er angivet på kreditnotaen.
-   **Gavekort** - Gavekort, der udstedes og indløses ved POS. Der tillades ikke overbetaling i forbindelse med gavekort.
-   **Debitorkonto** – Betalinger kan tilskrives en debitorkonto ved kasseapparatet på salgstidspunktet. Du kan også bruge denne betalingsmetode til at indsamle salgsoplysninger eller kundespecifikke rabatter, når kunden foretager en betaling ved hjælp af en anden betalingsmetode. I dette tilfælde skal du definere kundespecifikke oplysninger.
-   **Fordelskundepoint** – de point, som kunder akkumulere gennem loyalitetsprogrammer. Hvis du opretter loyalitetsprogrammer, kan kunderne få point og indløse dem på forskellige måder. I nogle loyalitetsprogrammer kan kunder f.eks. indløse fordelskundepoint i form af en rabat eller endda bruge dem som en form for betaling.

Hvis du vil konfigurere betalingsmetoder i Detail og handel, skal du udføre følgende opgaver.

1.  Konfigurer betalingsmåder for en organisation. Opret de betalingsmetoder, der accepteres af hele organisationen.
2.  Oprette globale korttyper og kortnumre. Hvis der accepteres kredit- eller debetkort, skal du oprette en betalingsmetode for kort og derefter oprette globale korttyper og kortnumre.
3.  Oprette betalingsmetode til butik. Tilknyt betalingsmetoder til hver butik, og angiv derefter de butiksspecifikke indstillinger for hver betalingsform.
4.  Opsætning af kortbetalingsmetoder for butikker. For alle kortbetalingsmetoder, butikken accepterer, at fuldføre opsætning af kortet.



