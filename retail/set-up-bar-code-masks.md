---
title: "Opsætning af stregkodemasker"
description: "Dette emne beskriver, hvordan du konfigurerer stregkodemasketegn, stregkodemasker, og hvordan du kan tildele stregkode masker på stregkoder."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fe598799d52cacd84da775ac7ace8cf9a30ae5fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bar-code-masks"></a>Opsætning af stregkodemasker

Dette emne beskriver, hvordan du konfigurerer stregkodemasketegn, stregkodemasker, og hvordan du kan tildele stregkode masker på stregkoder.

<a name="set-up-bar-code-mask-characters"></a>Opsætning af stregkodemasketegn
-------------------------------

Stregkodemasker bruges til at oprette stregkoder og til hurtigt at identificere stregkoder, der er scannet til salgsstedet (POS). Masker består af tegn, der fungerer som pladsholdere, som angiver formatet for stregkoder, der oprettes. Hvis du vil konfigurere en stregkodemaske, skal du konfigurere stregkodemasketegn. Gå til **detail- og commerce**&gt;**Lagerstyring**&gt;**stregkoder og etiketter**&gt;**maskere tegn**. Klik på **ny** til at oprette stregkodemasketegn. Masketegn kan oprettes for at angive følgende data i stregkoden.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Field**            | **Description**                                                                                                 |
| **Product**          | Pladsholder for produkt-ID.                                                                                     |
| **Any number**       | Bruges til at angive et tal, der er hårdt kodet i stregkoder.                                                  |
| **Check digit**      | Betyder, at formatet stregkode i en stregkodemaske bruger et kontrolciffer for at bekræfte gyldigheden af en stregkode. |
| **Size digit**       | Angiver størrelse på en stregkode, der er oprettet for en produktvariant, der omfatter størrelse.                                 |
| **Color digit**      | Angiver farven på en stregkode, der er oprettet for en produktvariant, som omfatter farve.                               |
| **Style digit**      | Angiver formatet i en stregkode, der er oprettet for en produktvariant, der indeholder en typografi.                             |
| **EAN license code** | Pladsholder for EAN-licensen er udstedt for EAN-licenskoder.                                                       |
| **Pris**            | Angiver pris pris integrerede stregkoder.                                                                   |
| **Quantity**         | Angiver antallet i antal tilfældige vægt integreret stregkoder.                                                |
| **Employee**         | Angiver stregkode målgruppe for medarbejder id-nummer, der bruges til at logge på stregkode POS.                                  |
| **Customer**         | Angiver ID'ET kundesegment.                                                                                  |
| **Indtastning af data**       | *Endnu ikke implementeret.*                                                                                          |
| **Discount code**    | Angiver en rabatkode til en stregkode, der bruges til at tilføje en rabat til et punkt af salgstransaktion             |
| **Gavekort**        | Angiver en gavekortnummer, når de udsteder eller betale med gavekort.                                               |
| **Loyalty card**     | Tilføjer en fordelskunde i transaktionen, og kan bruges ved betaling af loyalitet.                             |

## <a name="define-bar-code-masks"></a>Definere stregkodemasker
Når stregkodemasketegn er angivet for de nødvendige stregkodemasker, gå til **detail- og commerce**&gt;**Lagerstyring**&gt;**stregkoder og etiketter**&gt;**opsætning af maske i stregkode**. På denne side kan du definere stregkodemasker, der bruger de tidligere angivne tegn. Disse stregkode masker, der skal bruges ved oprettelse af stregkoder og vil også hjælpe med at identificere stregkoder, der er scannet ved POS.

1.  Klik på **ny** til at oprette en ny stregkodemasken.
2.  Angiv værdier i den **maske-ID** og **beskrivelse** felter, og vælg derefter en stregkodemasketypen i **Type** felt.
3.  I den **generelle** skal du vælge en værdi i den **standard stregkode** felt og derefter angive præfikset stregkode, hvis den er påkrævet.
4.  I den **stregkode maske målgruppe** skal du føje stregkode segmenter, der skal bruges i stregkoden skal oprettes.

Som et eksempel, hvis du vil oprette en stregkodemaske med maske-ID 'Produkt', gøre du følgende:

1.  Opret en ny stregkodemaske og vælg typen 'Produkt'.
2.  Vælg en stregkode som standard, for eksempel 'kode 39'.
3.  Angiv et præfiks, der skal bruges til nemt at identificere stregkoden. For eksempel '22.'
4.  Tilføje en maske målgruppe. «Produkt» maske målgruppen vil være markeret.
5.  Give en længde for målgruppen produkt, for eksempel '10'. Længden skal svare til længden af et produkt-ID, der normalt bruges i butikken. Masken, der vises som et eksempel på den **generelle** afsnit **maske**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Tildele stregkoder stregkodemasker
Stregkodemasker skal tildeles stregkoder, før de kan bruges. Fortsætter det foregående eksempel, at stregkodemasken tildeles en stregkode, skal du gøre følgende:

1.  Gå til **virksomhedsadministration**&gt;**Setup**&gt;**stregkoder**. Klik på **ny** til at oprette en ny stregkode.
2.  Angiv værdier i den **stregkode****setup** og ** opsætning ** felter.
3.  I den **generelle** i sektionen på **stregkodetype** skal du vælge 'Kode 39'. I den **maske****ID** skal du vælge 'Produkt' masken har oprettet tidligere.
4.  Under **størrelse**, Angiv '12'.
5.  Click **Save**.

Stregkodemasken kan nu bruges til at oprette stregkoder for produkter. Ovenfor er eksempler på, hvordan du opretter stregkodemasker for produkter, men de også illustrere, hvordan du opretter stregkodemasker for alle typer andre understøttede stregkode. Stregkodemasker, former og længder bør justeres til brug i dit miljø.


