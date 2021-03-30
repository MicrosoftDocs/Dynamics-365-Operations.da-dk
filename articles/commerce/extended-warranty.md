---
title: Oprette og konfigurere udvidede garantier
description: Dette emne omhandler udvidede garantier og beskriver, hvordan du kan oprette og konfigurere dem i Microsoft Dynamics 365 Commerce.
author: sijoshi
manager: annbe
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: sijoshi
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2457f2cf1d6bfb228aae63a0aebaca0d159b7323
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209071"
---
# <a name="create-and-configure-extended-warranties"></a>Oprette og konfigurere udvidede garantier

[!include [banner](includes/banner.md)]

Dette emne omhandler udvidede garantier og beskriver, hvordan du kan oprette og konfigurere dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Kunderne vælger i stigende grad udvidet support og services, når de køber produkter, især forbrugsvarer, der sælges til et Premium-prispoint, f.eks. telefoner og computere. Ved at tilbyde udvidede garantier for køb kan forhandlere hjælpe med at opbygge kundeloyalitet. Udvidede garantier giver kunderne besked om, hvor de kan få service og support. Derfor kan de have tillid til, at deres problemer håndteres effektivt.

Udvidede garantier kan sælges til kunder i en detailkanal under det indledende produktkøb. De kan også sælges i en begrænset periode efter det indledende køb.

### <a name="warranty-item-setup"></a>Opsætning af garantivare

Dynamics 365 Commerce har funktionalitet, der giver dig mulighed for at oprette en garantivare og angive attributter for den. Disse attributter omfatter tilknytningen mellem et produkt og en garantivare, prisen på garantien og garantiens varighed. Når en garantivare er konfigureret og frigivet til organisationsenheden, kan en forhandler sælge garantier ved hjælp af Modern POS (MPOS), onlinebutikker og andre detailkanaler.

### <a name="warranty-item-sales"></a>Salg af garantivare

Udvidede garantier sælges i en detailkanal under det indledende produktkøb. De kan også sælges i en begrænset periode efter det indledende køb.

På POS bliver salgsmedarbejdere bedt om at tilføje en udvidet garanti, når der føjes et relateret produkt til en kundes indkøbsvogn. Derfor vises der en salgsmulighed for mersalg og tillægsslag for salgsmedarbejdere som en del af salgsflowet.

Kunder kan også vende tilbage senere og købe en udvidet garanti for et produkt, som de tidligere har købt. I disse tilfælde kan en salgsmedarbejder slå den oprindelige transaktion op og sælge kunden den relaterede udvidede garantivare.

### <a name="warranty-terminology"></a>Garantiterminologi

I følgende tabel defineres nogle garantirelaterede udtryk.

| Periode | Beskrivende tekst |
|------------------------------|--------------|
| Udvidet garanti/garanti | En *udvidet garanti* henviser til en serviceaftale eller kontrakt, der giver en længere garanti for kunderne. Den udvidede garanti omfatter den supplerende service, der erstatter eller reparerer varer i løbet af den udvidede garantis dækningsperiode. |
| Producentens garanti | En *producents garanti* (ofte kaldet en *begrænset garanti*) er den garanti, som kunder modtager, når de køber et produkt. Her er nogle af funktionerne i en producents garanti:<ul><li>Garantiomkostningerne er inkluderet i produktets kostpris. Kunderne behøver ikke betale noget ekstra beløb for en producents garanti.</li><li>Afhængigt af produktkategorien varer en producentgaranti som regel 30 dage, seks måneder eller et år. (For det meste forbrugerelektronik vil garantien vare ét år).</li><li>Garantien omfatter defekter, der skyldes mekaniske eller elektriske fejl. Dækningen er begrænset, og den omfatter ikke utilsigtet beskadigelse af det købte produkt. Kunder, der ønsker at beskytte de produkter, de køber, mod typiske skader, bør investere i en udvidet garanti. Udvidede garantier varer to til ti år, afhængigt af produktkategorien. De har også større dækning og dækker typiske uheld, f.eks. tab, spildt væske og pletter.</li></ul> |
| Garantielement | En *garantivare* er en udvidet garantivare, der sælges for en berettiget vare. Et eksempel er en toårs beskyttelsesplan for bærbare computere. |
| Garantiberettiget vare | En *garantiberettiget vare* er et serienummereret produkt, som en garanti sælges til. En bærbar computer er f.eks. en garantiberettiget vare, som to års og tre års udvidede garantier sælges til. |
| Garantigruppe | En *garantigruppe* er en relation mellem garantivarer og garantiberettigede varer. POS bruger garantigrupper til at bestemme, hvilke garantivarer salgsmedarbejdere skal bedes om at tilføje, når en berettiget vare føjes til en kundes indkøbsvogn. |
| Garantipolice | En *garantipolice* er en enhed, der oprettes i Commerce, når der sælges en garantipolice. En garantipolice omfatter oplysninger som start- og slutdatoer for den købte garantivare, vilkår og betingelser samt serienummeret på det garantiberettigede produkt. Garantipolicenumre kan deles med kunder, så de har en reference til den udvidede garantivare, som de har købt. |

## <a name="create-a-warranty-item"></a>Oprette en garantivare

Hvis du vil oprette en garantivare i Commerce, skal du følge disse trin.

1. Gå til **Detail og handel \> Produkter og kategorier \> Produkter**.
1. Vælg **Ny** for at oprette en ny garantivare.
1. Vælg **Service** i feltet **Produkttype** i dialogboksen **Nyt produkt**.
1. Vælg **Produkt** i feltet **Produktundertype**.
1. Vælg **Service** i feltet **Produktservicetype**.
1. Indtast produktnavnet i feltet **Produktnavn**.
1. Vælg en værdi på rullelisten i feltet **Detailkategori**, og vælg derefter **OK**.
1. Angiv produktnummeret i feltet **Produktnummer**.
1. Vælg **OK**.
1. Angiv felterne **Tidsenhed** og **Tidsrum** i oversigtspanelet **Garanti** på siden **Produktdetaljer**.

    | Feltnavn | Værdi | Beskrivende tekst |
    |------------|-------|-------------|
    | Tidsenhed | **Dag(e)**, **Uge(r)**, **Måned(er)** eller **År** | I dette felt angives den tidsenhed, der bruges til garantien. |
    | Tidsrum | En positiv heltalsværdi | I dette felt angives varigheden af garantien i den valgte tidsenhed. |

    Hvis der f.eks. er en garanti på to år, skal du angive feltet **Tidsenhed** til **År** og feltet **Tidsrum** til **2**. Du kan også vælge at angive feltet **Tidsenhed** til **Måned(er)** og feltet **Tidsrum** længde til **24**, som vist i følgende illustration.

    ![Siden Produktdetaljer for en garantivare](./media/ew-time-properties.png)

1. Vælg **Gem** for at gemme garantivaren.
1. Frigiv garantiproduktet til firmaet, så det kan sælges. Du kan finde flere oplysninger under [Konfigurere detailprodukter](set-up-retail-products.md).
1. I oversigtspanelet **Garanti** på siden **Frigivne produktdetaljer** skal du angive felterne **Prisinterval**, **Nedre grænse** og **Øvre grænse**.

    | Feltnavn | Værdi | Beskrivende tekst |
    |------------|-------|-------------|
    | Basis for prisinterval | **Ingen**, **Basispris** eller **Salgspris** | <ul><li>**Ingen** – Værdierne for **Nedre grænse** og **Øvre grænse** er ikke tilgængelige for prisintervallet.</li><li>**Basispris** – En bestemt garanti vil være gældende, hvis basisprisen (dvs. prisen uden rabatter) for den garantiberettigede vare befinder sig mellem den **Nedre grænse** og den **Øvre grænse**, der er angivet her, baseret på prisen på den berettigede vare.</li><li>**Salgspris** – Denne værdi er reserveret til fremtidig brug.</li></ul> |
    | Nedre grænse, Øvre grænse | En positiv heltalsværdi | Disse felter definerer de øvre og nedre prisgrænser for den garantiberettigede vare, og hvordan den aktuelle garantivare gælder for den berettigede vare. Disse grænser kan være baseret på den berettigede vares basispris (kaldes også producentens foreslåede detailpris \[MSRP\]). Hvis feltet **Prisinterval** er angivet til **Basispris**, vil kun en berettiget vare (produkt), der har en basispris mellem den **Nedre grænse** og den **Øvre grænse**, udløse en prompt for at tilføje garantivaren ved POS. |

    I følgende illustration vises feltet **Prisinterval** angivet til **Basispris**, feltet **Nedre grænse** er angivet til $500, og feltet **Øvre grænse** er angivet til $1000.
    
    ![Siden Frigivne produktdetaljer for en garantivare](./media/ew-release-product-details.png)

1. Send garantivaren til den kanal, hvor den sælges. Du kan finde flere oplysninger under [Konfigurere udvalg](set-up-assortments.md).

### <a name="example"></a>Eksempel

En bærbar computer (produkt) har som garantiberettiget vare en basispris på $999, og der er to bærbare garantivarer:

- Garantien\_1 har en nedre grænse på $500 og en øvre grænse på $1.000, og **Prisintervallet** er angivet til **Basispris**.
- Garantien\_2 har en nedre grænse på $1.001 og en øvre grænse på $2.000, og **Prisintervallet** er angivet til **Basispris**.

I dette tilfælde vises en meddelelse om, at der skal tilføjes Garanti\_1 ved POS, når den bærbare computer med garantiberettigelse lægges i en kundes kurv, da prisen på den bærbare computer er mellem de nedre og øvre grænser for Garanti\_1.

> [!NOTE]
> Hvis du f.eks. vil have vist prompter for både Garanti\_1 og Garanti\_2, uanset prisen på den berettigede vare, skal du angive feltet **Prisinterval** til **Ingen**.

## <a name="configure-channel-specific-settings"></a>Konfigurere kanalspecifikke indstillinger

Du kan bruge kanalspecifikke indstillinger til at angive, om en prompt for tilføjelse af en garantivare skal vises ved POS, når en berettiget vare føjes til en kundes indkøbsvogn.

Hvis du vil konfigurere kanalspecifikke indstillinger i Commerce, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Produkter og kategorier \> Garanti \> Garantiindstillinger**.
1. På fanen **Kanalspecifik** skal du i kolonnen **Spørg efter garanti** for kanalen følge et af disse trin:

    - Markér afkrydsningsfeltet, hvis en prompt for garantivaren skal vises ved POS, når den garantiberettigede vare føjes til indkøbsvognen.
    - Fjern markeringen af afkrydsningsfeltet, hvis ingen prompt for garantivaren skal vises ved POS, når den garantiberettigede vare føjes til indkøbsvognen.

1. Kør jobbet **1070** for at synkronisere dataene til kanalen.

## <a name="configure-a-number-sequence-for-warranty-policies"></a>Konfigurere en nummerserie for garantipolicer

Hver garantipolice identificeres entydigt af et garantipolicenummer, der genereres af en nummerserie. Du kan finde flere oplysninger om nummerserier i [Oversigt over nummerserier](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Udfør følgende trin for at konfigurere en nummerserie for garantipolicer i Commerce.

1. Gå til **Retail og Commerce \> Produkter og kategorier \> Garanti \> Garantiindstillinger**.
1. Angiv eller vælg en værdi i feltet **Nummerseriekode** i rækken for referencen **Garantipolice** under fanen **Nummerserier**.

## <a name="set-up-a-warranty-group"></a>Konfigurere en garantigruppe

En garantigruppe er en relation mellem garantivarer og garantiberettigede varer. POS bruger garantigrupper til at bestemme, hvilke garantivarer salgsmedarbejdere skal bedes om at tilføje, når en berettiget vare føjes til en kundes indkøbsvogn.

Gør følgende for at konfigurere en garantigruppe i Commerce.

1. Gå til **Retail og Commerce \> Produkter og kategorier \> Garanti \> Garantigrupper**.
1. Vælg **Ny** for at oprette en ny garantigruppe.
1. Indtast et navn til den nye gruppe i feltet **Navn**.
1. Indtast en beskrivelse af gruppen i feltet **Beskrivelse** i oversigtspanelet **Generelt**.
1. Vælg **Tilføj linje** i oversigtspanelet **Garanti produkter** for at tilføje en garantivare.
1. I feltet **Visningsrækkefølge** skal du angive et nummer for at rangere garantigruppen ved POS. POS vil vise garantivarer i stigende rækkefølge ved garantiprompten.
1. Vælg **Tilføj linje** i oversigtspanelet **Garantiberettigede produkter** for at tilføje garantiberettigede produkter.
1. Hvis garantivaren gælder for en hel kategori af berettigede varer (produkter), skal du vælge kategorien i feltet **Kategori**. Hvis garantivaren gælder for en bestemt berettiget vare (produkt), skal du vælge produktet i feltet **Produkt**.
1. Vælg **Tilføj linje** i oversigtspanelet **Gældende kanaler** for at tilføje den kanal, hvor du vil sælge garantivaren.
1. Vælg **Gem** for at gemme konfigurationen.
1. Vælg **Publicer** for at publicere garantigruppen.
1. Kør jobbet **1040** for at synkronisere dataene til kanalen.

## <a name="sell-warranty-items-at-the-pos"></a>Sælge garantivarer ved POS

Med to POS-operationer kan salgsmedarbejdere sælge garantivarer under arbejdsgangen for kundekøb:

- **Tilføj garanti** – Denne operation udløser en prompt, der viser de relevante garantier for en berettiget vare, der er valgt i indkøbsvognen.
- **Føj garanti til eksisterende transaktion** – Denne operation giver salgsmedarbejdere mulighed for at sælge garantier for de berettigede varer, der tidligere er blevet solgt. Salgsmedarbejdere kan finde den oprindelige transaktion for en berettiget vare ved at angive transaktionens kvitteringsnummer.

I følgende illustration vises et eksempel på en side i en POS-klient med en prompt om at tilføje en garantivare for det aktuelle køb af en berettiget vare.

![Eksempel på en prompt om at tilføje en garantivare for det aktuelle indkøb](./media/ew-sell-warranty.png)

I følgende illustration vises et eksempel på funktionen til tilføjelse af en garantivare for en berettiget vare, der tidligere er blevet solgt.

![Eksempel på funktionen til tilføjelse af en garantivare for en tidligere solgt berettiget vare](./media/ew-add-warranty-existing.png)

## <a name="process-warranty-transactions"></a>Behandl garantitransaktioner

Når garantierne sælges i kontanttransaktioner, efter transaktioner er bogført i Commerce Headquarters, kan Commerce-brugere køre jobbet til **behandling af garantitransaktioner** for at behandle garantitransaktionerne og oprette garantipolicer.

Hvis du vil behandle garantitransaktioner i Commerce Headquarters, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Produkter og kategorier \> Garanti \> Behandling af garantitransaktioner**.
1. Vælg en værdi i feltet **Organisationshierarki** i dialogboksen **Vælg organisationsnoder**.
1. På listen **Tilgængelige organisationsnoder** skal du vælge enten en enkelt butik eller, hvis du vil oprette batchjobbet for en gruppe butikker, en node.
1. Vælg knappen Højre pil for at tilføje dit valg på listen **Valgte organisationsnoder**.
1. Vælg fanen **Kør i baggrunden**.
1. Angiv indstillingen **Batchbehandling** til **Ja**, og vælg derefter **Gentagelse**.
1. Vælg eller angiv en startdato for gentagelsen i feltet **Startdato** i dialogboksen **Definer gentagelse**.
1. Vælg eller angiv et starttidspunkt for gentagelsen i feltet **Starttidspunkt**.
1. Udfør ét af følgende trin:

    - Vælg indstillingen **Ingen slutdato**, hvis gentagelsen aldrig skal afsluttes.
    - Vælg indstillingen **Afslut efter**, hvis gentagelsen skal slutte efter et bestemt antal kørsler. Hvis du har valgt denne indstilling, skal du angive antallet af kørsler.
    - Vælg indstillingen **Afslut den**, hvis gentagelsen skal afsluttes på en bestemt dato. Hvis du har valgt denne indstilling, skal du vælge eller angive datoen.

1. Vælg **OK**.
1. Vælg **OK**.

## <a name="warranty-policies"></a>Garantipolicer

Når der sælges en udvidet garanti, oprettes der automatisk en garantipoliceenhed. Garantipolicenumre kan deles med kunder, så de har en reference til den udvidede garantivare, som de har købt. Egenskaberne for garantipolicer omfatter den gældende start- og udløbsdato for garantien, vilkår og betingelser samt serienummeret på den berettigede vare, som garantien blev solgt til.

> [!NOTE]
> Egenskaber for garantipolice oprettes automatisk, når der oprettes garantipoliceobjekter. I øjeblikket kan de ikke konfigureres eller redigeres manuelt.

I følgende tabel beskrives egenskaber for garantipolice og deres værdier. I Commerce Headquarters hedder databasetabellen WARRANTYPOLICY.

| Egenskabsbetegnelse | Værdi | Beskrivende tekst |
|---------------|-------|-------------|
| PolicyNumber | En tegnstreng (højst 20 tegn) | Garantipolicenummeret |
| WarrantiedItemId | En tegnstreng (højst 20 tegn) | Id'et for den garantiberettigede vare |
| WarrantiedInventoryLotId | En tegnstreng (højst 20 tegn) | Lagerparti-id'et for den garantiberettigede vare |
| WarrantiedSerialNumber | En tegnstreng (højst 20 tegn) | Serienummeret på den garantiberettigede vare |
| WarrantiedFulfilledDate | En dato | Indfrielsesdatoen for den garantiberettigede vare |
| WarrantyItemId | En tegnstreng (højst 20 tegn) | Id'et for garantivaren |
| WarrantyInventoryLotId | En tegnstreng (højst 20 tegn) | Lagerparti-id'et for garantivaren |
| WarrantySalesDate | En dato | Salgsdatoen for garantivaren |
| WarrantyEffectiveDate | En dato | Ikrafttrædelsesdatoen for garantipolicen |
| WarrantyExpirationDate | En dato | Udløbsdatoen for garantipolicen |
| CustAccount | En tegnstreng (højst 20 tegn) | Kundens kontonummer |
| Status | **Oprettet**, **Afvist**, **Gyldig** eller **Udløbet** | Status for garantipolicen |
| Bemærkninger | En tegnstreng (højst 255 tegn) | Bemærkninger om garantipolicen, f.eks. vilkår og betingelser |

## <a name="frequently-asked-questions-faq"></a>Ofte stillede spørgsmål

**Hvorfor kan jeg ikke se en garantiprompt ved POS?**

Kontrollér, at garantivaren er udvalgt til kanalen. Kontrollér også, at garantigruppen er konfigureret, så den omfatter den relevante kanal.

**Hvorfor kan jeg ikke se nogen posteringslinjevarer, når jeg forsøger at føje en garanti til en eksisterende transaktion og angive kundens ordrekvitteringsnummer?**

Kvitteringer kan kun findes, hvis der køres et pull-job (P-job) for at uploade kvitteringerne til Commerce Headquarters. Hvis du vil køre P-job, skal du gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**, vælge job **P-0001** og derefter vælge **Kør nu**.

**Hvorfor gælder garantifunktionen kun for serienummerede produkter?**

En garanti er en service, der er beregnet til et specifikt, entydigt produkt. I Dynamics 365 kan et produkt kun identificeres entydigt af et serienummer.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere detailprodukter](set-up-retail-products.md)

[Konfigurere udvalg](set-up-assortments.md)

[Oversigt over nummerserier](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]