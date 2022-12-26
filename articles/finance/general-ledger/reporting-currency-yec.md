---
title: Rapporteringsvalutaen balancerer ikke, når årsafslutningen køres
description: I denne artikel forklares det, hvordan rapporteringsvalutaen kan være saldoafvisende, når årsafslutning køres.
author: kweekley
ms.date: 12/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 31f79791330e076d4fbd7b604ba9f9c6cd9b9195
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850256"
---
# <a name="reporting-currency-out-of-balance-when-the-year-end-close-is-run"></a>Rapporteringsvalutaen balancerer ikke, når årsafslutningen køres

Når du aktiverer funktionen **Opmærksomhed mellem finansudligning og årsafslutning** (funktionen **Opmærksomhed**), medtages finansposteringer, der er udlignet, ikke længere i startsaldoen for det næste regnskabsår, når afslutningen af finansåret afsluttes. Udelukkelsen af finansposteringer, der er udlignet, kan give udfordringer for kunderne ved årsafslutningen, hvis Finans er defineret som en rapporteringsvaluta.

Finansudligning udføres kun for regnskabsvalutaen. Når finansposteringerne er udlignet, sikrer valideringen kun regnskabsvalutaens debetbeløb svarende til regnskabsvalutakreditterne. Beløbene i rapporteringsvalutaen for disse finansposteringer valideres ikke og debiteringer udlignes måske ikke krediteringer. Derudover beregner og bogføres der ikke automatisk vinding/tab i rapporteringsvalutaen.

På grund af disse begrænsninger skal der findes en postering for vinding/tab i rapporteringsvalutaen ved udførelse af finansudligninger. Hvis vinding/tab ikke indgår i finansudligning, vil lukningen ved årsafslutning resultere i en meddelelse om saldoafvigelse.

I følgende eksempel gennemgås de trin, der skal bruges til at løse dette problem, før lukningen af året køres.

## <a name="example-setup"></a>Eksempel på opsætning

Du kan konfigurere dette eksempel ved at aktivere funktionen **Opmærksomhed** og konfigurere hovedkonto 110180 til finansudligning. I følgende illustration vises de finansposteringer, der blev bogført i den juridiske enhed DEMF. Regnskabsvalutaen til DEMF er amerikanske dollar (USD), og rapporteringsvalutaen er euro (EUR).

![Bogførte finansposteringer i rapporteringsvalutaen.](./media/reporting-currency-1.png)

På siden **Finansudligninger** vises finansposteringerne for hovedkonto 110180. Vælg og hold (eller højreklik på) gitterhovedet, og vælg derefter **Indsæt kolonner**. Tilføj **beløbet i kolonnen til rapporteringsvaluta** , så alle beløb for transaktionsvaluta, regnskabsvaluta og rapporteringsvaluta vises.

![Beløb i kolonnen med rapporteringsvaluta, der er føjet til siden Finansudligninger.](./media/Ledger-settlement2.png)

De første to finansposteringer for 100,00 EUR udlignes som én gruppe, og de næste to finansposteringer for 200,00 EUR udlignes som en anden gruppe. (De to posteringer har forskellige udlignings-d'er). Denne konfiguration viser, at organisationer har flere grupper finansposteringer, der udlignes på forskellige tidspunkter og har forskellige udligningsdatoer. Når udligningen er udført, vises følgende oplysninger på siden **Finansudligninger**, når den er filtreret til at vise posteringer, der har status **udlignet**.

![Udlignede posteringer på siden Finansudligninger.](./media/Settled-trans-filtered3.png)

Vælg og hold (eller højreklikke) i kolonnen **Beløb** i transaktionsvaluta på siden **Finansudligninger**, og vælg derefter at lave en **total for denne kolonne**. Gentag dette trin for **Beløb i rapporteringsvalutakolonner**. Regnskabsvalutaen skal have en difference på 0 (nul), før der kan foretages udligning. Men udligningsbeløbet for rapporteringsvalutaen valideres ikke. I følgende illustration vises en difference på -27,79 USD for rapporteringsvalutaen.

![Difference i rapporteringsvaluta.](./media/Difference4.png)

## <a name="year-end-close"></a>Årsafslutning

Hvis årsslutningen nu køres for 2022, afsluttes processen med en fejl, der ikke balancerer. Denne fejl er direkte forårsaget af, at rapporteringsvalutaen ikke har et finansudligningersbeløb, der netto er 0 (nul).

![Fejlmeddelelse, der angiver, at finansudligninger ikke er 0 (nul).](./media/YEC5.png)

## <a name="posting-reporting-currency-gainloss"></a>Postering af gevinst/tab i rapporteringsvaluta

For at årsafslutregningen skal lykkes, skal differencen i rapporteringsvalutabeløbet gøres regnskabet for det, typisk som en vinding eller et tab, og være medtaget i finansudligingen. Vinding/tab for rapporteringsvalutaen kan bogføres på flere måder:

- Hvis hovedkontoen er kreditor eller debitor, genererer debitorudligning /kreditorudligning af disse dokumenter den nødvendige gevinst/tab. Den pågældende regnskabspost skal medtages i finansudligningen, når de tilsvarende finansposteringer fra fakturaen, betalinger, kreditnotaer osv. udlignes.
- Hvis hovedkontoen ikke er en kreditorkonto eller debitorkonto, skal vinding/tab angives manuelt. Når vinding/tab bogføres, bestemmes detaljeringsniveauet for regnskabsposten af din organisation.
- Identificer det vinding/tab-beløb, der skal bogføres, for hver hovedkonto.

Som beskrevet tidligere kan denne postering udføres på siden **Finansudligninger**.

1. Filtrer til det datointerval, du vil bogføre vinding/tab for. Hvis du planlægger at bogføre et tab/vinding pr. måned, skal du filtrere efter hver måned. Hvis du planlægger at bogføre et tab/vinding pr. regnskabsår, skal du filtrere efter hele året.
2. Filtrer på hovedkontoen.
3. Filtrer efter status, så der kun vises **udlignede** posteringer.
4. Tilføj en total i kolonnen **Beløb i rapporteringsvaluta**.
5. Hvis du vil bogføre vinding/tab på et mere detaljeret niveau, kan du udføre yderligere filtrering af udlignings-id'et, økonomiske dimensioner osv. Det samlede beløb for kolonnen **Beløb i rapporteringsvaluta** repræsenterer det beløb, som vinding/tab vil blive bogført for.
6. Gå til **Finans \> Kladdeposteringer \> Reguleringskladder for rapporteringsvaluta**.
7. Angiv transaktionen for gevinst/tab. Kladden bogfører kun en regulering i rapporteringsvalutaen. De posteringsvaluta- og regnskabsvalutabeløb, der bogføres, er altid 0 (nul). Hvis kladden ikke er blevet brugt tidligere, skal du muligvis oprette et kladdenavn med kladdetypen **Rapportering af valutaregulering ved kladdenavne** i **Finans \> Kladdeopsætning \> Finanskladder.**
8. Denne justering bogføres ikke, hvis hovedkontoen ikke tillader manuel indtastning. Du skal muligvis midlertidigt deaktivere parameteren **Tillad ikke manuel indtastning** på **hovedkontosiden**.

![Manuel indtastning på siden Kladdebilag.](./media/Manual-entry6.png)

Når du har bogført reguleringskladden, skal du vende tilbage til siden **Finansudligninger** og vælge den hovedkonto, du har bogført vind/tab for. Reguleringen af vinding/tab skal medtages i en finansudligning. Da beløbet i rapporteringsvalutaen ikke behøver at være netto til 0 (nul), kan du udligne tidligere posteringer og derefter udligne dem igen, men denne gang skal du medtage vindingen/tabet. Hvor præcis du vil være for bogføringen af vinding/tab og udligning af denne vinding/tab i finansudligninger, er op til din organisation.

I følgende illustration vises det, at posteringerne for 200 EUR ikke er blevet afmærket og derefter markeret til udligning igen. Denne gang inkluderer de reguleringen af vinding/tab.

![Regulering af vinding/tab på siden Finansudligninger.](./media/gain-loss7.png)

Når posteringerne er udlignet, skal du ændre **statusfilteret** , så siden viser **udlignede** posteringer. Totalen for kolonnen **Beløb i rapporteringsvaluta** er nu 0 (nul). Årsslut lukningen kan nu køres uden problemer.

![Gennemført årsafslutning.](./media/Zero-settled8.png)
