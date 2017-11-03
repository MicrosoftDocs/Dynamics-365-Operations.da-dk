---
title: "Opsætning af stregkodemasker"
description: Dette emne beskriver, hvordan du konfigurerer stregkodemasketegn, stregkodemasker, og hvordan du kan tildele stregkodemasker til stregkoder.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 671155cbf76c1570374a1602cd6590117cffa28e
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-bar-code-masks"></a>Opsætning af stregkodemasker

[!include[banner](includes/banner.md)]


Dette emne beskriver, hvordan du konfigurerer stregkodemasketegn, stregkodemasker, og hvordan du kan tildele stregkodemasker til stregkoder.

<a name="set-up-bar-code-mask-characters"></a>Opsætning af stregkodemasketegn
-------------------------------

Stregkodemasker bruges til at oprette stregkoder og til hurtigt at identificere stregkoder, der er scannet ind i POS-enheden. Masker består af tegn, der fungerer som pladsholdere, som angiver formatet for de stregkoder, der oprettes. Hvis du vil konfigurere en stregkodemaske, skal du konfigurere stregkodemasketegn. Gå til **Detail** &gt; **Lagerstyring** &gt; **Stregkoder og labels** &gt; **Masketegn**. Klik på **Ny** for at oprette stregkodemasketegn. Masketegn kan oprettes for at angive følgende stregkodedata.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Felt**            | **Beskrivelse**                                                                                                 |
| **Produkt**          | Pladsholder for produkt-id.                                                                                     |
| **Vilkårligt tal**       | Bruges til at angive et tal, der er hard-coded i stregkoder.                                                  |
| **Kontrolciffer**      | Angiver, at stregkodeformatet i en stregkodemaske bruger et kontrolciffer for at bekræfte gyldigheden af en stregkode. |
| **Størrelse - ciffer**       | Angiver størrelse i en stregkode, der er oprettet for en produktvariant, der omfatter størrelse.                                 |
| **Farve - ciffer**      | Angiver farve i en stregkode, der er oprettet for en produktvariant, der omfatter farve.                               |
| **Type - ciffer**      | Angiver type i en stregkode, der er oprettet for en produktvariant, der omfatter type.                             |
| **EAN-licenskode** | Pladsholder for EAN-licensen er udstedt for EAN-licenskoder.                                                       |
| **Pris**            | Angiver pris for stregkoder med integreret pris.                                                                   |
| **Antal**         | Angiver antal i stregkoder med integreret antal/tilfældig vægt.                                                |
| **Medarbejder**         | Angiver stregkodesegment for medarbejder id-nummer, der bruges til at logge på med stregkode på POS-enheden.                                  |
| **Kunde**         | Angiver kunde-id-segment.                                                                                  |
| **Datapost**       | *Ikke implementeret endnu.*                                                                                          |
| **Rabatkode**    | *Afskrives* pr. Dynamics 365 for Retail 2017-forårsversion. Tidligere. Angiver en rabatkode til en stregkode, der bruges til at føje en rabat til en POS-transaktion.                                                                   |
| **Kuponkode**      | Angiver kuponkode for en stregkode, der bruges til at føje rabat til en detailordre. Dette har erstattet rabatkoden.     |
| **Gavekort**        | Angiver en gavekortnummer, når der udstedes eller betales med gavekort.                                               |
| **Fordelskundekort**     | Tilføjer en fordelskunde i transaktionen, og kan bruges ved betaling af loyalitet.                             |

## <a name="define-bar-code-masks"></a>Definer stregkodemasker
Når stregkodemasketegn er angivet for de nødvendige stregkodemasker, skal du gå til **Detail** &gt; **Lagerstyring** &gt; **Stregkoder og labels** &gt; **Opsætning af stregkodemaske**. På denne side kan du definere stregkodemasker, der bruger de tidligere angivne tegn. Disse stregkodemasker, der skal bruges ved oprettelse af stregkoder og vil også hjælpe med til at identificere stregkoder, der er scannet ved POS-enheden.

1.  Klik på **Ny** for at oprette en ny stregkodemaske.
2.  Angiv værdier i felterne **Maske-id** og **Beskrivelse**, og vælg derefter en stregkodemasketypen i feltet **Type**.
3.  I afsnittet **Generelt** skal du vælge en værdi i feltet **Stregkodestandard** og derefter angive præfikset stregkode, hvis det er påkrævet.
4.  I afsnittet **Stregkodemaskesegment** skal du tilføje stregkodesegmenter, der skal bruges i den stregkode, der skal oprettes.

Hvis du f.eks. vil oprette en stregkodemaske med maske-id'et 'Produkt', skal du gøre følgende:

1.  Opret en ny stregkodemaske, og vælg typen 'Produkt'.
2.  Vælg en stregkodestandard, f.eks. 'Code 39'.
3.  Angiv et præfiks, der skal bruges til nemt at identificere stregkoden. F.eks. '22'.
4.  Tilføj et maskesegment. Maskesegmentet 'Produkt' vælges.
5.  Angiv en længde for produktsegmentet, f.eks. '10'. Længden skal svare til længden af et produkt-ID, der normalt bruges i butikken. Masken vises som et eksempel i afsnittet **Generelt** under **Maske**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Tildel stregkodemasker til stregkoder
Stregkodemasker skal tildeles stregkoder, før de kan bruges. Hvis vi fortsætter med det foregående eksempel, skal du gøre følgende for at tildele stregkodemasken til en stregkode:

1.  Gå til **Virksomhedsadministration** &gt; **Opsætning** &gt; **Stregkoder**. Klik på **Ny** for at oprette en ny stregkode.
2.  Angiv værdier i felterne **Stregkode** **Opsætning** og **Opsætning**.
3.  I afsnittet **Generelt** i feltet **Stregkodetype** skal du vælge 'Kode 39'. I feltet **Maske-****id** skal du vælge masken 'Produkt', der er oprettet tidligere.
4.  Under **Størrelse** skal du angive '12'.
5.  Klik på **Gem**.

Stregkodemasken kan nu bruges til at oprette stregkoder for produkter. Ovenstående trin er eksempler på, hvordan du opretter stregkodemasker for produkter, men de illustrerer også, hvordan du opretter stregkodemasker for alle andre typer understøttede stregkoder. Stregkodemasker, typer og længder bør justeres til brug i dit specifikke miljø.




