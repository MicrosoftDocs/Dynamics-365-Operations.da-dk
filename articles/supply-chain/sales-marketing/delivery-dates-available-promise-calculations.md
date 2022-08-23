---
title: Ordretilsagn
description: Denne artikel indeholder oplysninger om ordretilsagn. Ordretilsagn hjælper med at love pålidelige leveringsdatoer til dine kunder og giver dig fleksibilitet, så du kan opfylde disse datoer.
author: Henrikan
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates, SalesCarrier
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c835e25348b937c1dd68d8fa45b0264bd6815c23
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228260"
---
# <a name="order-promising"></a>Ordretilsagn

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om ordretilsagn. Ordretilsagn hjælper med at love pålidelige leveringsdatoer til dine kunder og giver dig fleksibilitet, så du kan opfylde disse datoer.

Ordretilsagn beregner tidligste afsendelses- og modtagelsesdatoer og er baseret på kontrolmetoden for leveringsdato og transportdage. Du kan vælge mellem følgende kontrolmetoder for leveringsdato:

- **Salgsleveringstid** – Salgsleveringstid er tiden mellem oprettelse af salgsordren og forsendelse af varerne. Beregningen af leveringsdatoen er baseret på antal dage og tager ikke hensyn til varernes tilgængelighed, kendte behov eller planlagte leveringer.
- **DTT (disponibel til tilsagn)** – DTT er antallet af en vare, der er tilgængelig og kan være lovet til en kunde på en bestemt dato. DTT-beregningen omfatter leveringstider, der ikke er bindende, planlagte tilgange og afgange.
- **DTT + Afgangsmargen**– Afsendelsesdatoen er lig med DTT-datoen plus varens afgangsmargen. Afgangsmargenen er den tid, der kræves for at klargøre varerne til afsendelse.
- **LE (leveringsevne)**– Tilgængelighed beregnes via udfoldning. Hvis du bruger Planlægningsoptimering, er det ikke tilladt at bruge *LE*-leveringsdatokontrolmetoden, og hvis den er valgt, opstår der en fejl, når beregningen køres. Du kan finde flere oplysninger om opsætning og brug af LE under [Beregne leveringsdatoer for salgsordrer med LE](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).
- **LE til planlægningsoptimering** – Brug den LE-beregning, der er leveret af Planlægningsoptimering. Denne indstilling har ingen virkning, hvis du bruger det indbyggede varedisponeringsprogram. Du kan finde flere oplysninger om opsætning og brug af LE under [Beregne leveringsdatoer for salgsordrer med LE](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

> [!NOTE]
> Når en salgsordre opdateres, opdateres oplysningerne om ordretilsagn kun, hvis den eksisterende dato for ordretilsagn ikke kan opfyldes, som vist i følgende eksempler:
>
> - **Eksempel 1**: Den aktuelle dato for ordretilsagn er 20. juli, men på grund af forøget antal vil du ikke være i stand til at levere før 25. juli. Da den aktuelle dato ikke længere kan opfyldes, udløses ordretilsagn.
> - **Eksempel 2**: Den aktuelle dato for ordretilsagn er 20. juli, men på grund af nedsat antal er det nu muligt at levere den 15. juli. Da den aktuelle dato stadig kan opfyldes, udløses der ikke ordretilsagn, og 20. juli forbliver datoen for ordretilsagn.

## <a name="atp-calculations"></a>DTT-beregninger

DTT-antallet beregnes ved hjælp af metoden "kumulativ fremtidig DTT". Den største fordel ved denne metode til beregning af DTT er, at det kan håndtere de tilfælde, hvor summen af afgange mellem tilgange er mere end sidste tilgang (for eksempel når et antal fra en tidligere tilgang skal bruges til at imødekomme et behov). Metoden til beregning af "kumulativ fremtidig DTT" omfatter alle afgange, indtil det kumulative antal, der skal modtages, overstiger det kumulative antal af afgange. Derfor evaluerer DTT-beregningsmetoden, om nogle af antallet fra en tidligere periode kan bruges i en senere periode.

DTT-antallet er den ikke-allokerede lagersaldo i den første periode. Den beregnes typisk for de enkelte perioder, hvor der er planlagt en tilgang. DTT-perioden beregnes i dage, og dags dato beregnes som den første dato for DTT-antallet. I første periode indeholder DTT den disponible lagerbeholdning minus kundeordrer, der er forfaldne eller overskredet.

DTT beregnes ved hjælp af følgende formel:

DTT = DTT for den forrige periode + tilgange i indeværende periode - afgange i indeværende periode – Nettoafgangsantallet for alle fremtidige perioder indtil den periode, hvor summen af tilgange for alle fremtidige perioder til og med den fremtidige periode er større end summen af afgange til og med den fremtidige periode.

Bemærk, at beregningen af DTT ikke indeholder oplysninger omkring udløbsdatoen og ud over den DTT-horisont, som systemet forventer, når et antal kan loves.

Når der ikke er flere afgange eller tilgange, der skal tages i betragtning, er DTT-antallet for følgende datoer det samme som det senest beregnede DTT-antal.

Hvis ikke alle de dimensioner, der bruges for en vare, er angivet, når DTT-kontrollen udføres, kan de måske stadig blive angivet på afgangen og tilgangen. I dette tilfælde skal tilgangene og afgangene i DTT-beregningen samles i de eksisterende dimensioner for at reducere antallet af tilgangs- og afgangslinjer, der bruges i DTT-beregningen.

DTT-antallet, der vises, er altid større end eller lig med 0 (nul). Hvis beregningen returnerer et negativt DTT-antal (hvis f.eks. det antal, der tidligere er lovet, overstiger det antal, der er tilgængeligt), angives antallet automatisk til 0.

### <a name="example"></a>Eksempel

Feltet **Tidshorisont for DTT-behov bagud** styrer, hvor langt tilbage i tiden der skal søges efter forsinkede behovsordrer eller lagerafgange. Feltet **Tidshorisont for DTT-forsyning bagud** styrer, hvor langt tilbage i tiden der skal søges efter forsinkede forsyningsordrer eller lagertilgange. Hvis ordrer, der f.eks. er forsinket med kun syv dage, skal tages i betragtning i DTT-beregningen, skal begge felter angives til **7**.

Felterne **Modretningstid for DTT-forsinket behov** og **Modretningstid for DTT-forsinket forsyning** styrer, hvornår forsinket behov eller forsyning behandles i DTT-beregningen. Hvis f.eks. den forsinkede forsyning og det forsinkede behov skal tages i betragtning i DTT-beregningen i overmorgen, skal begge felter angives til **2**. En værdi af **2** betyder, at antallet af en vare på en forsinket indkøbsordre, der skal overvejes i DTT-beregningen, vises som tilgængelige to dage efter den aktuelle dato.

I følgende eksempel er **7** angivet i felterne **Tidshorisont for DTT-behov bagud** og **Tidshorisont for DTT-forsyning bagud**, og **1** er angivet i felterne **Modretningstid for DTT-forsinket behov** og **Modretningstid for DTT-forsinket forsyning**.

En indkøbsordre på 200 stk. af et produkt, der skulle være modtaget for tre dage siden, er ikke modtaget endnu. Derfor er en salgsordrelinje på 75 stk. af samme produkt, der skulle være leveret i går, ikke leveret.

En kunde ringer og ønsker at bestille 150 stk. af samme produkt. Når du kontrollerer tilgængeligheden af produktet, opdager du, at en anden indkøbsordre på 100 stk. af produktet leveres 10 dage senere.

Du opretter en salgsordrelinje for produktet og angiver **150** for antallet.

Da metoden for kontrol af leveringsdato er DTT, beregnes DTT-dataene for at finde den tidligst mulige afsendelsesdato. Baseret på indstillingerne bliver den forsinkede indkøbsordre og salgsordre behandlet, og det resulterende DTT-antal for den aktuelle dato er 0. I morgen, når den forsinkede indkøbsordre forventes at blive modtaget, beregnes DTT-antallet som mere end 0 (i dette tilfælde beregnes det som 125). Men 10 dage fra nu, hvor den ekstra indkøbsordre for 100 styk forventes at blive modtaget, vil DTT-antallet være mere end 150.

Derfor bliver afsendelsesdatoen indstillet til 10 dage fra nu, baseret på DTT-beregningen. Du fortæller derfor kunden, at det ønskede antal kan leveres om 10 dage.

## <a name="ctp-calculations"></a>CTP-beregninger

MED LE-funktionen kan du give kunder realistiske datoer for, hvornår du kan love bestemte varer. For hver salgslinje kan du angive en dato, der tager højde for eksisterende lagerbeholdning, produktionskapacitet og transporttider.

LE udvider DTT-funktionaliteten ved at tage kapacitetsoplysninger med i betragtning. Mens DTT kun tager højde for materialetilgængelighed og forudsætter ressourcer med ubegrænset kapacitet, tager LE højde for tilgængeligheden af både materialer og kapacitet. Det giver derfor et mere realistisk billede af, om efterspørgslen kan opfyldes inden for en given tidsramme.

LE fungerer lidt anderledes baseret på den brugte varedisponering (Planlægningsoptimering eller det indbyggede program). LE til Planlægningsoptimering understøtter i øjeblikket kun et undersæt af LE-scenarier, der understøttes af det indbyggede program.

Du kan finde flere oplysninger om opsætning og brug af LE for hvert program under [Beregne leveringsdatoer for salgsordrer med LE](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
