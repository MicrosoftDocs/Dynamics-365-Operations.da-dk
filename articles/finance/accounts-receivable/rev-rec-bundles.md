---
title: Indtægtsføring i bundter
description: Denne artikel beskriver den bundtfunktionalitet, der er inkluderet i indtægtsføringsfunktionaliteten i Debitor. Et bundt omfatter en overordnet vare og flere komponentvarer.
author: kweekley
ms.date: 01/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 478fdfc69514fba829deb63b4e2904ff3fe1e199
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876290"
---
# <a name="revenue-recognition-bundles"></a>Indtægtsføring i bundter

[!include [banner](../includes/banner.md)]

Denne artikel beskriver den bundtfunktionalitet, der er inkluderet i indtægtsføringsfunktionaliteten i Debitor. Et bundt omfatter en overordnet vare og flere komponentvarer. Den overordnede vare angives på en salgsordre, så ordreindtastningen bliver mere effektiv. Men det udfoldes derefter i komponentvarer. Interne dokumenter, f.eks. følgesedlen, viser en oversigt over komponentvarer. Eksterne dokumenter viser dog kun den overordnede vare.

> [!NOTE]
> Microsoft Dynamics 365 Commerce-kanaler, f.eks. online, POS (POS) og callcentre understøtter ikke indtægtsføring (herunder bundtfunktionaliteten). Det omfatter også løsningen Kundeemne til kontantløsningen til Dynamics 365 Supply Chain Management og Dynamics 365 Sales. Varer, der er konfigureret til at bruge indtægtsføring, bør ikke føjes til ordrer eller transaktioner, der er oprettet i handelskanaler eller i Kundeemne til kontantløsningen.

Hvis du vil konfigurere bundter, skal du angive konfigurationsnøgler til indtægtsføring. Du kan dog bruge bundter, selvom indtægtsføring ikke er konfigureret. Tilsvarende kan du bruge indtægtsføring, selvom der ikke er konfigureret bundter. Hvis der er konfigureret indtægtsføring, bestemmer indgående varer indtægtsprisen og den omsætningsplan, der bruges til indtægtsføring eller udskydelser, når en salgsordre faktureres.

Denne konfiguration for bundter anvender stykliste-funktionen (BOM). Du kan finde flere oplysninger om, hvordan du konfigurerer et bundtelement, i [konfigurationen af indtægtsføring](revenue-recognition-setup.md). Hvis den overordnede vare er markeret som et bundt, behandles den anderledes end andre styklistevarer (BOM). Her er en liste over forskellene:

- Bundter skal udfoldes via salgsordrebekræftelse ved at vælge **Bekræft salgsordre** under fanen **Sælg** i handlingsruden på salgsordresiden. Varer i bundter må aldrig udfoldes ved at vælge **Styklistelinje** under **Udfold** i menuen **Salgsordrelinje** i oversigtspanelet **Salgsordrelinjer**. Ellers behandles varen som en stykliste og ikke som et bundt.
- En salgsordre, der indeholder en bundtvare, skal bekræftes, før følgesedlen eller fakturaen oprettes.
- Når et bundt udfoldes via en salgsordrebekræftelse, annulleres den overordnede vare, og dets enhedspris og rabatter fordeles på de indgående varer i bundtet.
- Summen af indgående varer skal altid være lig med prisen på den overordnede vare. Derfor er der begrænsninger på de felter, der kan opdateres eller ændres for indgående varer. Enhedsprisen kan f.eks. ikke ændres manuelt. Den kan heller ikke ændres indirekte ved at få en ny prisaftale til at træde i kraft. Lagerdimensioner kan ikke ændres på indgående varer for at forhindre en ny prisaftale.
- Når der udskrives et eksternt dokument, som f.eks. salgsordrebekræftelsen eller fakturaen, udskrives den overordnede vare, og ikke komponentvarerne.

## <a name="bundles-on-sales-orders"></a>Bundter på salgsordrer

USMF-demofirmaet indeholder følgende bundtopsætning. Bemærk, at alle indstillinger for indtægtsføring, f.eks. opsætning af omsætningsplaner, er fjernet fra de varer, der er medtaget i dette scenario.

**Overordnet vare:** Computerbundt

- **Indgående vare:** Et antal på 1 af vare 1000
- **Indgående vare:** Et antal på 1 af vare S0021
- **Indgående vare:** Et antal på 1 af varesupport

*Basissalgsprisen* for komponentvarer er en væsentlig del af konfigurationen af komponenterne. Basissalgsprisen defineres i **Sælg**-oversigtspanelet for en vare. Den bruges til at beregne fordelingsfaktoren, når den overordnede vares enhedspris fordeles på komponentvarerne. Salgspriserne i samhandelsaftalen bruges aldrig til dette formål.

Der er defineret følgende basissalgspriser for komponentvarer:

- **1000:** $1.900,00
- **S0021:** $150,00
- **Support:** $500,00

Der er angivet en salgsordre for debitor US-004, Cave Wholesales. Den eneste linje, der angives, er for bundtelementet Bærbar computer. Standardenhedsprisen for den overordnede linje kan tages fra flere steder, f.eks. samhandelsaftalen eller basissalgsprisen. I dette eksempel var DKK 2.300 manuelt angivet som enhedspris.

[![Bundtvare til bærbar computer på en salgsordre.](./media/bundle-01.png)](./media/bundle-01.png)

Da salgsordren indeholder et bundt, skal det bekræftes. Bekræftelsesdialogboksen viser bundtets komponenter.

[![Dialogboksen Bekræft salgsordre, der viser komponentvarerne.](./media/bundle-02.png)](./media/bundle-02.png)

Den udskrevne bekræftelsesrapport viser dog kun den overordnede vare i bundtet, da den pågældende rapport er det eksterne dokument for kunden.

[![Bekræftelsesrapport, der kun viser den overordnede vare.](./media/bundle-03.png)](./media/bundle-03.png)

Når salgsordren er bekræftet, vises den overordnede vare stadig på salgsordren, men dens status er ændret til **Annulleret**. Derudover spores nettobeløbet i feltet **Bundtede nettobeløb**. Dette beløb skal bruges til at udskrive fakturaen, fordi fakturaen viser den overordnede vare og ikke komponentvarerne.

Summen af komponentvarerne skal være lig med **nettobeløbsværdien for bundtet** for den overordnede vare, da denne værdi er det beløb, kunden får vist på den udskrevne faktura. Hvis du vil sikre, at fakturaen svarer til de beløb, der er bogført i finansmodulet, begrænses redigeringen af komponentvarerne. Lokationen og lagerstedet kan f.eks. ikke ændres, da disse ændringer kan udløse en prisændring baseret på en samhandelsaftale.

Enhedsprisen fra linjen for den overordnede vare fordeles til komponenterne på følgende måde:

**Samlede basissalgspriser fra komponenter:** $1.900 + $500 + $150 = $2.550

- **Komponent 1:** $2.300 × (1.900 ÷ 2.550) = $1.713,73
- **Komponent 2:** $2.300 × (500 ÷ 2.550) = $450,98
- **Komponent 3:** $2.300 × (150 ÷ 2.550) = $135,29

Summen af komponenterne skal være lig $2.300, og det betyder (1.713,73 kr. + $450,98 + $135,29 = $2.300).

Hvis ændringer er nødvendige for alle komponentvarer, kan den overordnede vare fjernes. I dette tilfælde fjernes komponentvarerne også. Derefter kan den overordnede vare tilføjes igen, og de nødvendige ændringer kan fuldføres, før salgsordren bekræftes.

[![Bundtvare, der inkluderer ændringer af komponentvarer.](./media/bundle-04.png)](./media/bundle-04.png)

Når salgsordren plukkes og pakkes, indeholder dokumenterne kun komponenterne i bundtet. Følgesedlen og fakturaen skal omfatte et komplet bundt. Ellers kan de ikke bogføres. I dialogboksen vises f.eks. tre komponentvarer. Hvis du prøver at slette en af dem, modtager du en fejlmeddelelse, der viser, at alle produkter i bundtet skal afsendes, før de kan faktureres.

Et bundt skal afsendes og faktureres som et komplet bundt. Hvis du f.eks. ændrer antallet for vare 1000 til 4, men lader antallet af de andre indgående varer være 5, kan følgesedlen og fakturaen ikke bogføres.

En delmængde kan kun afsendes og faktureres, hvis antallet reduceres for alle komponenter i bundtet. Der angives f.eks. et antal på 5 af bundtelementet Bærbar computer på en salgsordre. Når salgsordren er bekræftet, vises de tre komponentvarer på salgsordren, og antallet af hver er 5. Antallet angives som standard til 5 for hver komponent under afsendelse og fakturering. Du kan dog justere antallet til 3 for alle tre komponentvarer. I dette tilfælde afsendes og faktureres tre fulde bundter. De resterende to bundtvarer (et antal på 2 af hver af de tre komponentvarer) kan afsendes og faktureres senere.

Det sidste trin er at fakturere salgsordren. Under faktureringen vises komponentvarerne i fakturadialogboksen.

[![Dialogboksen Faktura, der viser komponentvarerne.](./media/bundle-06.png)](./media/bundle-06.png)

Den udskrevne faktura viser dog kun den overordnede vare.
 
[![Den udskrevne faktura, der kun viser den overordnede vare.](./media/bundle-07.png)](./media/bundle-07.png)

Den fakturakladde, der oprettes, efter bogføringen er indtraf, omfatter ikke den overordnede vare fra bundtet, da den pågældende vare har status af **Annulleret**.

[![Fakturakladde, der ikke inkluderer den overordnede vare.](./media/bundle-08.png)](./media/bundle-08.png)

Det er vigtigt, at fakturakladden ikke medtager den overordnede vare fra bundtet, da alle processer, der udføres, efter at fakturaen er bogført, er baseret på denne fakturajournal. Hvis du f.eks. opretter en kreditnota fra fanen **Sælg** i handlingsruden, omfatter den kreditnota, der oprettes, de indgående varer, men ikke den overordnede vare.

[![Kreditnota, der viser komponentvarerne, men ikke den overordnede vare.](./media/bundle-09.png)](./media/bundle-09.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
