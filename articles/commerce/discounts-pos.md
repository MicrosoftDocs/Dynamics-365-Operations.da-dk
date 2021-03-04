---
title: Få vist rabatter i POS
description: I dette emne forklares det, hvordan Microsoft Dynamics 365 Commerce hjælper salgsforbindelser med at få mere at vide om kampagner, og hvordan de kan bruges til at krydssælge og videresælge bevægelser.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 07/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-Commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail, Commerce
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.openlocfilehash: 7531e250580019a1e9892d22fc7761770227c61f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411084"
---
# <a name="show-discounts-in-pos"></a>Få vist rabatter i POS

[!include [banner](includes/banner.md)]

Kampagner spiller en vigtig rolle i at motivere kunder, der træffer beslutninger om indkøb. Ferier kan f.eks. producere det højeste antal salg for detailhandlere, da hele detailmarkedet er overfyldt med lokkende kampagner og rabatter. Hvis butiksmedarbejderne kender til og forstår de tilgængelige kampagner, kan de nemt udnytte disse kampagner for at kunne krydssælge og videresælge varer. I dette emne forklares det, hvordan Microsoft Dynamics 365 Commerce hjælper salgsforbindelser med at få mere at vide om kampagner, og hvordan de kan bruges til at krydssælge og videresælge bevægelser.

## <a name="learn-about-store-discounts"></a>Få mere at vide om butiksrabatter

Commerce indeholder en handling med navnet "Få vist alle rabatter". Denne handling viser alle de rabatter, der i øjeblikket kører i en butik. Handlingen "Få vist alle rabatter" kan knyttes til en knap i POS, og denne knap kan føjes til **Velkomst**- eller **Transaktion**-siden. I følgende illustration vises et eksempel på siden **Alle rabatter**, når den er åben.

![Siden Alle rabatter](./media/View_all_discounts.png "Siden Alle rabatter")

Systemet søger efter alle de rabatter, der svarer til en eller flere af følgende betingelser, for at vise rabatter:

- Prisgruppen for rabatten svarer til butikkens prisgruppe.
- Prisgruppen for rabatten er knyttet til et tilhørsforholds- eller fordelskundeprogram.
- Prisgruppen for rabatten er tilknyttet et katalog, der er tilknyttet butikken.

På siden **Alle rabatter** vises kun nogle rabatkuponbaserede rabatter, fordi detailhandlerne typisk opretter tusindvis af kuponer og tilsvarende rabatter for særlige kunder, og denne side er ikke beregnet til at vise kundespecifikke rabatter. Kuponbaserede rabatter vises kun, hvis indstillingen **Anvend uden en kuponkode** er aktiveret i hver kuponoverskrift. I dette tilfælde kan kasserere anvende kuponen uden at skulle angive eller scanne en kupon- eller stregkode.

Når indstillingen **Anvend uden en kuponkode** er aktiveret, bliver der forskellige scenarier tilgængelige. Kasserere kan f.eks. give kunder flere rabatter til kundeberoligelsesformål eller pga. produktfejl. Udskrevne kupon- eller stregkoder behøver ikke at blive fordelt til kasserere. Kasserere kan i stedet vælge knappen **Anvend kupon**. Rabatten anvendes derefter automatisk på transaktionen. Hvis der findes flere rabatkuponer for en kuponoverskrift, vælger systemet automatisk den første aktive kupon på transaktionen.

På siden **Alle rabatter** kan salgsmedarbejderen også søge efter rabatter efter nøgleord. Nøgleordssøgningen søger i de felter, der indeholder rabatnavnet og -beskrivelsen. Salgsmedarbejdere kan også filtrere rabatter ud fra, om en rabat skal bruge en rabatkuponkode.

## <a name="cross-sell-and-upsell-by-using-discounts"></a>Krydssælg og videresælg ved hjælp af rabatter

Samkøbsrabatter, f.eks. mængderabatter, mix og match-rabatter og grænserabatter, er en god måde at motivere kunderne til at købe flere produkter på for at opnå større rabatter. Derfor kan de også øge størrelsen på kundens indkøbsvogn og detailhandlers indtægt. Disse rabatter kan offentliggøres på e-handelswebsteder, på sociale medier og på bannere i butikken.

Selv når alle disse metoder til offentligheden anvendes, kan kunderne imidlertid miste muligheden for at udnytte kampagnerne. Detailhandlere kan føje knappen for handlingen **"Få vist tilgængelige rabatter"** til knaplinjen på siden **Transaktion** for at gøre det let for salgsmedarbejderne at finde ud af, hvilke kampagner der gælder for en bestemt linje eller endda for hele kurven. Derfor kan en salgsmedarbejder vælge en transaktionslinje og derefter vælge knappen for at få vist alle de rabatter, der er tilgængelige for den valgte linje. Salgsmedarbejderen kan også vælge en anden fane for at få vist rabatter, der gælder for hele transaktionen. Det er vigtigt at bemærke, at **Få vist tilgængelige rabatter** ikke viser de rabatter, der allerede er anvendt på salgslinjen, fordi rabatoplysningerne allerede er vist på salgslinjen. Formålet med dette scenario er kun at vise de rabatter, der endnu ikke er anvendt. Undtagelsen til dette er de rabatter, der anvendes på basis af en kupon, der er markeret som "Anvend uden en kuponkode". Det gør det nemt for salgsmedarbejderen at fjerne den kupon, de har anvendt.

Siden **Alle rabatter** viser kun rabatter, der ikke konkurrerer med nogen af de anvendte rabatter. Denne funktionsmåde sikrer, at en salgsmedarbejder informerer kunden om en rabat, og kunden udfører den påkrævede handling (f.eks. hvis kunden køber én mere vare for at opnå en rabat på 10 %), anvendes rabatten på transaktionen. De kuponbaserede rabatter vises kun, når indstillingen **Anvend uden en kuponkode** er slået til.

I et simpelt scenarie hvor alle rabatter har samme prioritet, er rabattens sammensatte tilstand **Sammensat**, og rabattens sammensatte kontrol er angivet til **Bedste pris og sammensæt inden for prioritet, aldrig sammensat på tværs af prioriteter**, viser siden **Alle rabatter** alle tilgængelige rabatter for et produkt, da alle rabatter er sammensatte og ikke konkurrerer med hinanden.

I følgende illustrationer vises den logik, som bestemmer, hvilke rabatter der vises i avancerede scenarier, f.eks. et scenarie, hvor rabattens sammensatte tilstand er **Bedste pris** eller **Eksklusiv**, og der bruges to eller flere prioriteter. I disse scenarier påvirkes de rabatter, der vises, yderligere afhængigt af, om rabattens sammensatte kontrol er angivet til **Bedste pris og sammensat inden for prioriteten, aldrig sammensat på tværs af prioriteter** eller **Kun bedste pris inden for prioriteten, altid sammensat på tværs af prioritet**.

I følgende illustration vises den logik, der bruges, når rabattens sammensatte kontrol er angivet til **Bedste pris og sammensat inden for prioritet, aldrig sammensat på tværs af prioriteter**.

![Logik for bedste pris og sammensat inden for prioriteten, aldrig sammensat på tværs af prioriteter](./media/Model_1.png "Logik for bedste pris og sammensat inden for prioriteten, aldrig sammensat på tværs af prioriteter").

I følgende illustration vises den logik, der bruges, når rabattens sammensatte kontrol er angivet til **Kun bedste pris indenfor prioritet, altid sammensat på tværs af prioriteter**.

![Logik for bedste pris kun inden for prioritet, altid sammensat på tværs af prioritet](./media/Model_2.png "Logik for bedste pris kun inden for prioritet, altid sammensat på tværs af prioritet").


[!INCLUDE[footer-include](../includes/footer-banner.md)]