---
title: "Produktsøgning og kundesøgning i POS"
description: "Dette emne indeholder en oversigt over de forbedringer, der er foretaget i produkt- og kundesøgefunktionen i Dynamics 365 for Retail."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 08/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 5f6f9a02b20549a75941d367c1b46e3439360078
ms.contentlocale: da-dk
ms.lasthandoff: 01/19/2018

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a>Oversigt over produkt- og kundesøgning i POS

[!include[banner](includes/banner.md)]

Modern Point of Sale (MPOS) og Cloud Point of Sale (CPOS) indeholder brugervenlige søgefunktioner, der giver butiksmedarbejdere mulighed for hurtigt at søge efter produkter og kunder. Søgelinjen vises altid øverst i MPOS og CPOS, så medarbejderne hurtigt kan finde produkter og kunder.

Medarbejdere kan søge efter produkter i det sortiment og de kataloger, der er tilknyttet den aktuelle butik og i det sortiment og de kataloger, der er knyttet til alle de andre butikker i virksomheden. Derfor kan kasserere sælge og returnere produkter, der ikke er i butikkens sortiment. På samme måde kan medarbejdere søge efter kunder, der er knyttet til den aktuelle butik eller alle de andre butikker i virksomheden. Medarbejdere kan desuden søge efter kunder, der er knyttet til en anden virksomhed i den overordnede organisation.

## <a name="product-search"></a>Produktsøgning 

Som standard udføres en søgning efter produkt på butikkens sortiment. Denne type søgning kaldes en *søgning efter lokalt produkt*. Men medarbejdere kan nemt skifte til ethvert katalog, der er tilknyttet den aktuelle butik, eller de kan søge i en anden butik. Denne type søgning kaldes en *ekstern produktsøgning*. Hvis du vil ændre kataloget, skal du vælge knappen **Kategorier** til venstre på siden. Øverst i ruden, der vises, skal du vælge knappen **Skift katalog** og derefter vælge et af de tilgængelige kataloger for at gennemse det. Systemet søger i det valgte katalog efter produkter.

På siden **Skift katalog** kan medarbejdere nemt vælge alle butikker, eller de kan søge efter produkter på tværs af alle butikker.

![Ændre kataloget](./media/Changecatalog.png "Ændre kataloget")
 
En lokal produktsøgning søger i følgende produktegenskaber:

- Produktnummer
- Produktnavn
- Betegnelse
- Dimensioner
- Stregkode
- Søgenavn

### <a name="enhancements-to-local-product-searches"></a>Forbedringer af lokale produktsøgninger

Oplevelsen for lokale produktsøgninger er blevet gjort mere brugervenlig. Der er blevet foretaget følgende forbedringen:

- Rullemenuer for produkt og kunde er føjet til søgelinjen, så medarbejderne kan vælge enten **Produkt** eller **Kunde**, før de søger. Som standard er **Produkt** markeret, som vist i nedenstående illustration.
- Til søgninger med flere nøgleord (dvs. til søgninger, der bruger søgeord), kan detailhandlerne konfigurere, om søgeresultaterne omfatter resultater, der passer til et af søgeordene, eller kun de resultater, der svarer til alle søgeord. Denne indstilling findes i POS-funktionalitetsprofilen under en ny gruppe med navnet **Produktsøgning**. Standardindstillingen er **Match et hvilket som helst søgeord**. Denne indstilling er også den anbefalede indstilling. Når indstillingen **Match et hvilket som helst søgeord** bruges, returneres alle de produkter, der matcher et eller flere søgeord helt eller delvist, som resultater, og resultaterne sorteres automatisk i stigende rækkefølge efter produkter, der matcher flest nøgleord (helt eller delvist).

    Indstillingen **Match alle søgeord** returnerer kun produkter, der matcher alle søgeordene (helt eller delvist). Denne indstilling er nyttig, når produktnavnene er lange, og medarbejdere kun vil se begrænsede produkter i søgeresultaterne. Denne type søgning har dog to begrænsninger:

    - Søgningen foretages på de enkelte produktegenskaber. F.eks. returneres kun produkter, der har alle de søgte nøgleord i mindst én produktegenskab.
    - Der søges ikke i dimensioner.

- Detailhandlere kan nu konfigurere produktsøgning til at vise søgeforslag, mens brugerne skriver produktnavne. En ny indstilling for denne funktion findes i POS-funktionalitetsprofilen under en ny gruppe med navnet **Produktsøgning**. Indstillingen hedder **Vis søgeforslag, mens du skriver**. Denne funktion kan hjælpe medarbejderne med hurtigt at finde det produkt, de søger efter, da de ikke behøver at skrive hele navnet manuelt.
- Produktsøgningsalgoritmen søger nu også efter de søgte udtryk i egenskaben **Søgenavn** for produktet.

![Produktforslag](./media/Productsuggestions.png "Produktforslag")

## <a name="customer-search"></a>Kundesøgning

Kundesøgning bruges til at finde kunder til forskellige formål. F.eks. ønsker kasserere eventuelt at få vist en kundes ønskeliste eller købshistorik eller at føje kunden til en transaktion. I forbindelse med søgninger med flere nøgleord returnerer kundesøgningsalgoritmen alle kunder, der svarer til et hvilket som helst af de søgte nøgleord. Men de kunder, der matcher de fleste nøgleord vises øverst i resultaterne. Denne funktionsmåde svarer til den måde, andre søgeprogrammer vsier resultater på. Først vises de resultater, der matcher de fleste søgte termer, og derefter vises de resultater, der delvist matcher søgeordene. Denne funktionsmåde gør det lettere for kasserere i situationer, hvor de anvender flere nøgleord til deres søgning, men et af nøgleordene har en forkert stavemåde.

Som standard udføres en kundesøgning på de kundeadressekartoteker, der er knyttet til butikken. Denne type søgning kaldes en *søgning efter lokal kunde*. Men medarbejdere kan også søge efter kunder globalt. De kan med andre ord søge på tværs af virksomhedens butikker og andre juridiske enheder. Denne type søgning kaldes en *ekstern kundesøgning*.

For at søge globalt kan medarbejderne vælge knappen **Filtrer resultater** i bunden af siden og derefter vælge indstillingen **Søg i alle butikker**, som vist i følgende illustration. I dette tilfælde returneres ikke kun kunder. Alle former for parter, der er en del af enhvert adressekartotek i hovedkontoret, returneres også. Disse parter omfatte medarbejdere, leverandører, kontaktpersoner og konkurrenter.

> [!NOTE]
> Der skal angives mindst fire tegn for at en ekstern kundesøgning returnerer resultater.

I en ekstern kundesøgning vises kunde-id ikke for debitorer fra de andre juridiske enheder, da der ikke er oprettet noget kunde-id for disse parter i det aktuelle regnskab. Men hvis en medarbejder åbner siden med oplysninger for kunden, opretter systemet automatisk et kunde-id for parten og knytter også butikkens kundeadressekartoteker til kunden. Kunden vil derfor være synlig i lokale butikssøgninger, der udføres senere.

![Global kundesøgning](./media/Globalcustomersearch.png "Global kundesøgning")

### <a name="enhancements-to-local-customer-searches"></a>Forbedringer af lokale kundesøgninger

Lokal kundesøgninger hjælpe medarbejderne med hurtigt at finde kunder ved hjælp af telefonnummeret. Medarbejderne behøver ikke at skrive eventuelle specialtegn, der er føjet til en kundes telefonnummer. f.eks. mellemrum, bindestreger eller kantede parenteser. Selvom kasserere kan gemme telefonnumre i et vilkårligt format (de kan f.eks. indeholde parenteser, bindestreger, symboler osv.), kan de søge efter kunder ved at skrive et delvis telefonnummer. Hvis en kasserer medtager specialtegn, når han eller hun angiver et telefonnummer, kan andre kasserere finde kunden ved at skrive de tal, der vises efter de særlige tegn. Hvis en kundes telefonnummer f.eks. blev angivet som **123-456-7890**, kan en kasserer søge efter debitoren ved at skrive **123**, **456**, **7890** eller **1234567890** eller ved delvist at angive de første par tal af telefonnummeret.

