---
title: Konfigurere produktfiltre til lagerstedstransaktioner
description: Dette emne beskriver, hvordan du konfigurerer produktfiltre og filtrerer koder for at kategorisere lagervarer på et lagersted. Du kan også bruge filtre til at angive, hvilke kunder der kan bestille en bestemt vare, og angive de varer, der kan købes hos en bestemt leverandør.
author: Mirzaab
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 922ff818e069f41c139cc00db9161dc6e113888b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973729"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a>Konfigurere produktfiltre til lagerstedstransaktioner

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer produktfiltre og filtrerer koder for at kategorisere lagervarer på et lagersted. Du kan også bruge filtre til at angive, hvilke kunder der kan bestille en bestemt vare, og angive de varer, der kan købes hos en bestemt leverandør.

Du kan desuden konfigurere og bruge produktfiltre til automatisk at organisere lagervarer i et lagersted og kombinere filtrerede elementer i filtergrupper. Du kan bruge filtre til at anbrunge varer i kategorier til håndterings-, indkøbs- og salgsprocesser. Det kan være en god ide at gruppere varer eller adskille dem fra hinanden, når den måde, de håndteres på, er baseret på vægt eller håndteringsbegrænsninger. Du kan også angive, hvilke kunder eller leverandører en vare kan købes hos eller sælges til.

## <a name="prerequisites"></a>Forudsætninger

Følgende tabel viser de forudsætninger, der skal være på plads, før du starter.

| Forudsætning | Instruktioner |
|---|---|
| Før du begynder at konfigurere produkter på siden **Frigivne produktdetaljer**, skal du aktivere lagerstedsbehandling for produktets lagringsdimensionsgruppe. | Gå til **Administration af produktoplysninger \> Opsætning \> Dimension og variantgrupper \> Lagringsdimensionsgrupper**, og vælg eller opret en lagringsdimensionsgruppe, hvor indstillingen **Brug lokationsstyringsprocesser** er angivet til *Ja*. |
| Hvis du vil bruge debitorfiltre og/eller kreditorfiltre, skal du aktivere brugen af dem i parametrene for lokationsstyring. | Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**. Angiv indstillingen **Aktivér debitorfiltre** og/eller **Aktivér kreditorfiltre** til **Ja** under fanen *Produktfiltre*. |

## <a name="set-up-product-filters"></a>Konfigurere produktfiltre

Produktfiltre indeholder op til 10 egenskaber for **filtertitlen**, som er fasttekstværdier. Disse fasttekstværdier kan vælges, når du opretter et produktfilter. Fasttekstværdierne *Kode 1* til og med *Kode 10* er systemdefinerede og repræsenterer en bestemt egenskab eller attribut for en vare. *Kode 1* kan f.eks. repræsentere varer, der har en klassifikation af farligt materiale. *Kode 2* kan repræsentere varer, som kun leverandører kan købe. Produktfiltre definerer derefter den specifikke **Filterkode**-værdi, der er knyttet til en værdi for **Filtertitel**.

1. Gå til **Lokationsstyring \> Konfiguration \> Produktfiltre \> Produktfiltre**.
1. Gå til handlingsruden, og vælg **Ny** for at føje et produktfilter til gitteret.
1. Vælg en værdi i feltet **Filtertitel**.
1. Angiv en værdi i feltet **Filterkode**.

    ![Konfigurere et produktfilter](media/Product_Filters10.png "Konfigurere et produktfilter")

1. Angiv et navn til koden i feltet **Beskrivelse**. *Kode 2* kan f.eks. repræsentere leverandører. Du kan derefter oprette et produktfilter for en bestemt leverandør eller gruppe af leverandører. Du kan finde flere oplysninger i afsnittet [Konfigurere leverandørfilterkoder](#vendor-product-filters) nedenfor i dette emne.

    ![Konfigurere produktfiltre](media/Product_Filters.png "Konfigurere produktfiltre")

## <a name="set-up-product-filter-groups"></a>Konfigurere produktfiltergrupper

Du kan bruge filtergrupper til at gruppere filterkoder. Dette er nyttigt, når en gruppe bruges i en forespørgsel i en lokationsvejledning, og du vil søge efter en gruppe i stedet for til en serie af koder. Hver filtergruppe er knyttet til en varegruppe.

> [!IMPORTANT]
> Ikke alle produktfiltergrupper er tilgængelige for filterkoder, der er højere end *Kode 4* (det vil sige *Kode 5* til og med *Kode 10*). Selvom alle produktfilterkoder f.eks. vil blive tilføjet, vil gruppering af filterkoder ikke blive opdateret for frigivne produkter. Denne funktionalitet opdateres muligvis i senere versioner.

Følg disse trin for at konfigurere filtergrupper.

1. Gå til **Lokationsstyring \> Konfiguration \> Produktfiltre \> Produktfiltergrupper**.
1. Gå til handlingsruden, og vælg **Ny**.
1. I felterne **Gruppe 1** og **Gruppe 2** skal du angive de navne, der skal bruges til at kategorisere varer.
1. I oversigtspanelet **Detaljer** skal du vælge **Ny** for at tilføje en linje.
1. Angiv start- og slutdatoer for filtergruppen i felterne **Startdato/-tidspunkt** og **Slutdato/-tidspunkt**.
1. Vælg den varegruppe, som produktfilteret skal gælde for, i feltet **Varegruppe**.
1. Vælg de filterkoder, der skal medtages i gruppen, i felterne **Kode 1** til og med **Kode 10**.

    ![Varegruppe](media/ProdFilterGroup.png "Varegruppe")

> [!NOTE]
> Hvis du modtager en fejlmeddelelse, når du lukker siden, mangler der muligvis en kodeopsætning. På siden **Varegrupper** kan du gøre koderne obligatoriske for en varegruppe ved at markere afkrydsningsfelterne **Tildel filterkode 1 til varegruppe**, **Tildel filterkode 2 til varegruppe** osv.

## <a name="set-up-filter-codes-on-item-groups"></a>Konfigurere filterkoder på varegrupper

Ved at oprette filterkoder på en varegruppe kan du oprette de koder, der er nødvendige for produkter, som er tilknyttet varegruppen.

Hvis du vil konfigurere filterkoder på varegrupper, skal du følge disse trin.

1. Gå til **Lagerstyring \> Opsætning \> Lager \> Varegrupper**.
1. Vælg **Ny** i handlingsruden for at oprette en varegruppe.
1. Angiv et navn i feltet **Varegruppe**.
1. Angiv en beskrivelse i feltet **Navn**.
1. I oversigtspanelet **Lagersted** skal du markere de relevante afkrydsningsfelter i sektionen **Filter påkrævet** for de filterkoder, der skal angives for produkter, der er knyttet til varegruppen.

    Hvis du vil opdatere et frigivet produkt, skal du åbne siden **Oplysninger om frigivne produkter** og derefter vælge **Rediger** i handlingsruden. De filtre, der er knyttet til koder, bliver derefter tilgængelige i oversigtspanelet **Lagersted**.

    ![Varegrupper](media/ItemGroup10.png "Varegrupper")

1. Markér afkrydsningsfelterne for de filtre, der skal matche for den filtergruppe, der skal være standardfiltergruppe for en vare, i sektionen **Varegruppefilter**.

    Hvis f.eks. **Brug filterkode 1** og **Brug filterkode 2** er markeret, skal både filterkode 1 og filterkode 2 for varen svare til opsætningen af filtergruppen for varegruppen, før filtergruppen kan vælges. Når du opretter en ny vare, er den valgte filtergruppe standardfiltergruppen i felterne **Gruppe 1** og **Gruppe 2** i oversigtspanelet **Lagersted** på siden **Oplysninger om frigivne produkter**.

> [!IMPORTANT]
> Produktfilterkoder er kun aktiveret for varer, der bruger avanceret lokationsstyring.

## <a name="specify-filter-codes-for-released-products"></a>Angive filterkoder for frigivne produkter

Følg disse trin for at angive filterkoder for frigivne produkter. Du kan f.eks. bruge filterkoder til at gruppere skadelige produkter, som bestemte leverandører køber.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg **Ny** i handlingsruden for at oprette et produkt.
1. I dialogboksen **Nyt frigivet produkt** skal du angive de data, der skal bruges til at oprette grundlaget for et nyt produkt, og derefter vælge **OK**.

    Produktfilterkoder aktiveres ikke, medmindre den varegruppe, der er knyttet til produktet, er konfigureret til filterkoder.

    Du kan finde flere oplysninger i [Oprette et nyt produkt](../pim/tasks/create-new-product.md).

1. I sektionen **Produktfilterkoder** i oversigtspanelet **Lagersted** skal du vælge filterkoder for **Kode 1** til og med **Kode 10**-felter efter behov for at angive filterkoder for produktet.

## <a name="set-up-generally-available-items"></a>Konfigurere generelt disponible varer

Du kan gøre bestemte lagervarer tilgængelige kun for kunder eller kun for leverandører eller for både kunder og leverandører.

> [!NOTE]
> Kunde- og leverandørfiltre gælder ikke for nogen vare, der er oprettet som generelt disponibel.

Benyt følgende fremgangsmåde for at konfigurere generelt disponible varer.

1. Gå til **Lokationsstyring \> Konfiguration \> Produktfiltre \> Generelt disponible produkter**.
1. Vælg **Ny** i handlingsruden for at oprette en post.
1. Vælg **Debitor**, *Kreditor* eller *Alle* i feltet *Debitor eller kreditor* for at gøre varerne tilgængelige for kunder, leverandører eller begge.
1. Angiv den dato og det klokkeslæt, hvor varen bliver tilgængelig, i feltet **Startdato/-tidspunkt**.
1. I feltet **Varegruppe** skal du vælge en varegruppe.
1. I felterne **Kode 1** til og med **Kode 10** skal du vælge filterkoder for at begrænse, hvilke varer der er generelt disponible.

    Når du vælger en varegruppe, angiver du, at denne varegruppe er generelt disponible. Ved at vælge filterkoder i disse felter begrænser du, hvilke varer der er disponible.

## <a name="set-up-customer-product-filters"></a>Konfigurere debitorproduktfiltre

Du kan bruge denne valgfrie fremgangsmåde til at angive varer, der skal være tilgængelige for en debitor foruden de varer, der er disponible via filteropsætningen på siden **Generelt disponible varer**. Du kan oprette flere filtre for en enkelt debitor.

Benyt følgende fremgangsmåde for at konfigurere debitorfilterkoder.

1. Gå til **Salg og marketing \> Kunder \> Alle kunder**.
1. Vælg en kunde.
1. Gå til handlingsruden, og vælg **Produktfiltre** i gruppen **Opsætning** under fanen **Kunde**.
1. På siden **Produktfilterkoder** skal du vælge **Ny** i handlingsruden.
1. Angiv start- og slutdatoer for varegruppen i felterne **Startdato/-tidspunkt** og **Slutdato/-tidspunkt**.
1. I feltet **Varegruppe** skal du vælge en varegruppe.
1. Vælg de filterkoder, der skal bruges som kriterier, i felterne **Kode 1** til og med **Kode 10**, for at begrænse de varer, der er tilgængelige for kunder i den valgte varegruppe. Du skal angive et valg for hver filterkode, der er konfigureret for varegruppen.

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a>Konfigurere kreditorproduktfiltre

Du kan bruge denne valgfrie fremgangsmåde til at angive varer, der skal være tilgængelige for en kreditor foruden de varer, der er disponible via filteropsætningen på siden **Generelt disponible varer**. Du kan oprette flere filtre for en enkelt kreditor.

Benyt følgende fremgangsmåde for at konfigurere kreditorfilterkoder.

1. Gå til **Indkøb og forsyning \> Kreditorer \> Alle kreditorer**.
1. Vælg en kreditor.
1. Gå til handlingsruden, og vælg **Produktfiltre** i gruppen **Opsætning** under fanen **Kreditor**.
1. På siden **Filterkoder** skal du vælge **Ny** i handlingsruden.
1. Angiv start- og slutdatoer for varegruppen i felterne **Startdato/-tidspunkt** og **Slutdato/-tidspunkt**.
1. I feltet **Varegruppe** skal du vælge en varegruppe.
1. Vælg de filterkoder, der skal bruges som kriterier, i felterne **Kode 1** til og med **Kode 10**, for at begrænse de varer, der er tilgængelige for leverandører i den valgte varegruppe. Du skal angive et valg for hver filterkode, der er konfigureret for varegruppen.

> [!NOTE]
> Opsætningen af kreditorproduktfiltre gælder for frigivne produkter, hvor processer til lokationsstyring er aktiveret for den tilknyttede lagringsdimensionsgruppe. Filterkoderne bruges til at bestemme, om systemet tillader brugere at købe en bestemt vare hos en bestemt leverandør, når de opretter indkøbsordrelinjer. Microsoft Dynamics 365 Supply Chain Management har to metoder til håndtering af kreditorgodkendelse. Hvis der findes en eller flere frigivne produkter, hvor feltet **Godkendt kontrolmetode for kreditorer** er angivet til *Kun advarsel* eller *Ikke tilladt*, kan begge metoder til kreditorgodkendelse være aktiveret for disse varer. Denne situation kan forårsage problemer, når brugerne opretter indkøbsordrelinjer.

## <a name="see-also"></a>Se også

[Yderligere oplysninger finder du i blogindlægget om WMS-Warehouse-filterkoder](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]