---
title: Salg og marketing
description: "Du kan bruge Salg og marketing til at finde, gemme og bruge forskellige typer data i salgsprocessen. Disse data omfatter det oprindelige salgsinitiativ, fremtidig opfølgning og yderligere salg."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 92303
ms.assetid: 65ca9992-bbfa-4224-bf0e-067a25c7e6a4
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: da48a9eef118a7a369343c986e4b67f53266f7e1
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="sales-and-marketing"></a>Salg og marketing

[!include [banner](../includes/banner.md)]

Du kan bruge Salg og marketing til at finde, gemme og bruge forskellige typer data i salgsprocessen. Disse data omfatter det oprindelige salgsinitiativ, fremtidig opfølgning og yderligere salg.

<a name="marketing"></a>Marketing
---------

Du bruger marketingkampagner og -aktiviteter til at finde og opbygge relationer med potentielle kunder, så indledende interaktioner kan udvikle til salgsrelationer. I følgende procesflow vises forretningsprocesserne for marketing. [![Forretningsproces for marketing](./media/marketing01.jpg)](./media/marketing01.jpg)

### <a name="relationships"></a>Relationer

I modulet Salg og marketing kan de første interaktioner, du har med potentielle kunder, forekomme i forskellige situationer. Du kan for eksempel finde en potentiel kunde, mens du deltager i en messe, eller du har måske et kundeemner, efter at din virksomhed har kørt en masseforsendelseskampagne. Det er meget vigtigt, at du forstår forløbet af en parts enhed, før denne part bliver kunde. Følgende grafik viser flowet af enhedsrelationer, når en potentiel kunde bliver en faktisk kunde. [![SalesandMarketing01](./media/salesandmarketing01.jpg)](./media/salesandmarketing01.jpg)

### <a name="campaigns"></a>Kampagner

En kampagne henvender sig til kontaktpersoner for kundeemner, potentielle kunder, salgsmuligheder og kunder, der er blevet valgt til at deltage i kampagnen. Du kan oprette flere typer kampagner som f.eks. telemarketing-, post- og mailkampagner, for at maksimere dit kundepotentiale i Microsoft Dynamics 365 for Finance and Operations. Efterhånden som din kampagnen skrider frem, og du får positive tilbagemeldinger, kan du begynde salgsprocessen med de modtagere, der har reageret positivt på kampagnen.

## <a name="sales"></a>Salg
Du kan bruge salgsfunktionen til at oprette tilbud og foretage mersalg og krydssalg til nye og eksisterende kunder, oprette salgsordrer og oprette salgsfakturaer til kunder. I følgende procesflow vises forretningsprocesserne for salg. [![Forretningsproces for salg](./media/sales01.jpg)](./media/sales01.jpg)

### <a name="sales-quotations"></a>Salgstilbud

Du kan oprette salgstilbud for at give kunder et tilbud om varer eller ydelser, som du kan levere. En kunde kan anmode om et tilbud, eller du kan oprette et tilbud som svar på en anmodning fra en potentiel eller eksisterende kunde. Når kunden godkender salgstilbuddet, kan du konvertere det til en salgsordre.

### <a name="up-sellcross-sell"></a>Mersalg/tillægssalg

Mersalg og krydssalg er teknikker til salg af produkter, når der registreres en ordre for en kunde. Ved mersalg foreslås et andet produkt i stedet for det aktuelle produkt. Ved krydssalg foreslås et produkt i tillæg til det aktuelle produkt. Når du konfigurerer produktlister, kan du oprette særlige regler for at angive, hvornår et produkt skal foreslås som et krydssalgs- eller mersalgsprodukt.

### <a name="sales-orders"></a>Salgsordrer

Når du opretter en ny salgsordre, skal du vælge, hvilken ordretype der skal oprettes. Du har fem muligheder. **Bemærk:** Når du har oprettet en salgsordre, kan en hvilken som helst ordretype ændres, undtagen typen **Varebehov**, hvis salgsordren har status **Leveret**.

| Salgsordretype  | Beskrivelse                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Journal           | Brug denne type som udkast til en salgsordre. Denne type har ingen effekt på lagermængderne og genererer ingen vareposteringer.                                                                                                                                                                    |
| Abonnement      | Brug denne type ved tilbagevendende ordrer. Når ordren er faktureret, indstilles ordrestatus automatisk til en åben ordre. Det leverede antal, der er faktureret, og de resterende antal opdateres. Du kan ikke bruge denne salgsordretype, hvis du bruger funktionen Lagerstedsstyring. |
| Salgsordre       | Brug denne type, når en kunde har afgivet eller bekræftet en ordre.                                                                                                                                                                                                                                        |
| Returordre    | Brug denne type, når en debitor returnerer en vare. Der tildeles automatisk et RMA-nummer (returvarenummer).                                                                                                                                                                                            |
| Varebehov | Denne type oprettes automatisk, når du foretager et varesalg via et projekt.                                                                                                                                                                                                                       |

### <a name="sales-agreements"></a>Salgsaftaler

En salgsaftale er en kontrakt, der forpligtiger kunden til at købe et produkt med et bestemt antal eller for et bestemt beløb over en periode mod at få særlige priser og rabatter. Priserne og rabatterne i salgsaftalen gå forud for de eventuelle priser og rabatter, der er angivet i de eventuelle samhandelsaftaler, der findes. En salgsaftale er gyldig i en defineret periode. Den ønskede afsendelsesdato, der er angivet for et salg på siden **Salgsordre**, skal være i den periode, der er gyldig. Som standard er en salgsaftale på hold. Du kan kun foretage bestillinger fra en salgsaftale, når den er indstillet til **Gyldig**.

### <a name="backorders"></a>Restordrer

Når du angiver og validerer ordrer, kan det være nødvendigt at administrere restordrer og undtagelser, før salget kan gennemføres. Restordrer er enten indkøbsordrer, der endnu ikke er leveret fra en leverandør, eller salgsordrer, der endnu ikke er leveret til en kunde. Det er vigtigt, at du følger op på restordrer. Hvis produkter f.eks. er forsinket fra en leverandør, skal du måske ændre datoen for levering til en kunde og derefter underrette kunden om forsinkelsen. Du kan få vist restordrer efter vare, debitor eller kreditor.

#### <a name="viewing-backorders-by-item"></a>Visning af restordrer efter vare

Når du får vist restordrer efter vare, kan du følge op på det forventede fremtidige flow for posteringer for en specifik vare. Du kan f.eks. udføre kontrollere følgende oplysninger:

-   Antallet af ordrer, der er afgivet for en vare
-   Om der stadig mangler leverancer af varen fra leverandører til kunder
-   Om der skal bestilles flere varer, så du kan levere alle salgsordrer i tide

Når du udfører denne kontrol, kan du besvare anmodninger fra kunder om tidspunktet for levering af varer. Derudover kan du prioritere salgsrestordrerne og senere dele de varer, der findes i lagerbeholdningen, ud på ordrerne.

#### <a name="viewing-backorders-by-customer"></a>Visning af restordrer efter debitorer

Når du får vist restordrer efter kunde, kan du se status for kundens resterende ordrer. Dette er nyttigt, når du skal reagere på kunder, der venter på varer, der er blevet forsinket.

#### <a name="viewing-backorders-by-vendor"></a>Visning af restordrer efter kreditor

Når du får vist restordrer efter leverandør, kan du følge op på manglende leveringer og forventede leveringsdatoer. Denne kontrol gør det også nemmere for dig at prioritere restordrerne, når der ankommer produkter fra leverandører, og salgsordrerne skal plukkes til levering.

### <a name="invoices"></a>Fakturaer

Du kan oprette tre typer af fakturaer under salgsprocessen:

-   Debitorfaktura
-   Fritekstfaktura
-   Proformafaktura

#### <a name="customer-invoice"></a>Debitorfaktura

En debitorfaktura er en regning, som en organisation giver en kunde i forbindelse med et salg. Du kan oprette denne type debitorfaktura på basis af en salgsordre, som omfatter et salgsordrehoved og en eller flere linjer for varer eller ydelser. Debitorfakturaen afslutter salgsordre-, følgeseddel- og salgsfakturacyklussen.  

Du kan bogføre og udskrive en enkelt debitorfaktura på basis af enten en salgsordre eller følgeseddel og dato. Du kan også bogføre og udskrive flere debitorfakturaer sammen på basis af følgesedler og datoer. Når du bogfører en enkelt debitorfaktura ved hjælp af salgsordren, opdateres antallet i **Fakturarestmængde** for de enkelte varer med det samlede fakturerede antal fra den valgte salgsordre.  

Hvis både antallet i **Fakturarestmængde** og antallet i **Levér rest** for alle varer i salgsordren er 0 (nul), ændres salgsordrens status til **Faktureret**. Hvis antallet i et af felterne ikke er 0, ændres salgsordrens status ikke, og du kan angive flere fakturaer. Hvis du vil bogføre og udskrive en eller flere debitorfakturaer baseret på følgesedler, skal du forinden have bogført mindst én følgeseddel for hver salgsordre. Debitorfakturaen er baseret på følgesedlerne og afspejler de antal, der er angivet.  

Du kan oprette en debitorfaktura, der er baseret på de linjeelementer på følgesedlen, som er afsendt til dato, selvom alle varerne i en bestemt salgsordre endnu ikke er afsendt. Det kan du f.eks. gøre, hvis din juridiske enhed udsteder én faktura pr. debitor pr. måned til dækning af alle de leverancer, du sender i den pågældende måned. Hver følgeseddel repræsenterer en dellevering eller en komplet levering af varerne i salgsordren.  

Når du bogfører fakturaen, opdateres antallet **Fakturarestmængde** for hver vare med det samlede beløb for de leverede antal fra de valgte følgesedler. Hvis antallet i **Fakturarestmængde** og antallet i **Levér rest** for alle varer i salgsordren er 0 (nul), ændres salgsordrens status til **Faktureret**. Hvis antallet ikke er 0, ændres salgsordrens status ikke, og du kan angive flere fakturaer. Lagerposteringer opdateres med fakturanummeret, og status i salgsordrelinjen på ændres til **Faktureret**.

#### <a name="free-text-invoice"></a>Fritekstfaktura

En fritekstfaktura er en faktura, der ikke er tilknyttet en salgsordre. Den indeholder ordrelinjer, der omfatter finanskonti, fritekstbeskrivelser og et salgsbeløb. Du kan ikke angive et varenummer på denne type faktura. Du skal angive de relevante momsoplysninger. En hovedkonto for salget angives på hver fakturalinje. Debitorsaldoen bogføres på samlekontoen fra den posteringsprofil, der bruges til fritekstfakturaen.

#### <a name="pro-forma-invoice"></a>Proformafaktura

En proformafaktura er en faktura, der udarbejdes som et estimat over det faktiske fakturabeløb, før fakturaen bogføres. Du kan udskrive en proformafaktura til enten en debitorfaktura eller en fritekstfaktura.




