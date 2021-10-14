---
title: Forsendelseskonsolideringspolitikker
description: Dette emne giver en oversigt over den funktionalitet, der giver en fleksibel konfiguration af politikker for forsendelseskonsolidering.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationError, WHSShipConsolidationSetShipment, WHSShipConsolidationPolicySelect, WHSShipPlanningListPage, TMSCarrierGroup, WHSShipConsolidationTemplate, WHSShipConsolidationTemplateApply, WHSShipConsolidationTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 11ee4beefed02425d4650de3e896e608d3d00ef5
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577954"
---
# <a name="shipment-consolidation-policies"></a>Forsendelseskonsolideringspolitikker

[!include [banner](../includes/banner.md)]

Processen til forsendelseskonsolidering, der bruger politikker for forsendelseskonsolidering, giver mulighed for automatiseret forsendelseskonsolidering og manuel frigivelse til lageret. Den automatiserede konsolidering, der var tilgængelig, før denne funktion blev introduceret, havde faste felter og var baseret på feltet **Konsolider forsendelse ved udlevering til lagersted**, der var angivet for et lagersted.

Der bruges politikker for forsendelseskonsolidering til følgende funktioner:

- Det automatiserede batchjob for frigivelse til lager
- Kommandoen **Frigiv til lager** i en salgsordre eller en flytteordre
- Den dedikerede side **Frigiv til lagersted**
- Kommandoen **Frigiv til lagersted** på siden **Panelet Lastplanlægning**
- Den manuelle konsolidering af forsendelser på siderne **Konsolider forsendelser** og **Panelet Forsendelseskonsoliderings**

Før der blev introduceret politikker for forsendelseskonsolidering, var konsolideringsfunktionen en indstilling på lagerstedsniveau. Alle ordrer for alle debitorer fra et enkelt lagersted blev behandlet, som om de havde samme konsolideringskrav. Politikker for forsendelseskonsolidering tilføjer understøttelse af scenarier, hvor forskellige organisationer har forskellige krav til forsendelseskonsolidering.

Forespørgsler bruges til at identificere den politik for forsendelseskonsolidering, der gælder, og derefter bestemmer et redigerbart sæt felter, hvordan lastlinjerne grupperes på forsendelsesniveau. (Dette mønster ligner det mønster, som bølgeskabeloner følger). Derudover er indstillingen **Konsolider med eksisterende forsendelser** føjet til hver politik. Når denne indstilling er aktiveret, finder proceduren *Frigiv til lagersted* forsendelser til konsolidering ved at søge blandt eksisterende forsendelser, der er blevet oprettet på baggrund af samme konsolideringspolitik. I dette tilfælde vil systemet vælge en eksisterende forsendelse eller last i stedet for at oprette en ny. Systemet vil dog kun konsolidere med eksisterende forsendelser, der har statussen *Åben*. Forsendelser, der tilhører en bølgefrigivelse med statussen *Frigivet* eller højere, betragtes ikke som mål for konsolideringen.

Når politikkerne for forsendelseskonsolidering er gjort tilgængelige, skjules indstillingen **Konsolider forsendelse ved frigivelse til lagersted**, der tidligere var tilgængelig på siden **Lagersted**. For at hjælpe dig med at overføre til den nye funktion til konsolidering af forsendelser opretter en funktion på siden **Politikker for forsendelseskonsolidering** en standardpolitik, der automatisk medtager den gamle indstilling for eksisterende lagersteder. Når standardpolitikken er oprettet, tages der ikke længere højde for indstillingen **Konsolider forsendelse ved frigivelse til lagersted** på konfigurationssiden **Lagersteder**.

Du kan bruge siden **Frigiv til lager** til manuelt at tilsidesætte den relevante konsolideringspolitik på samme måde, som du kan tilsidesætte opfyldningspolitikker.

Du kan bruge kommandoen **Frigiv \> Frigiv til lagersted** på siden **Panelet Lastplanlægning** til at oprette udgående laster, der er baseret på salgsordre- og flytteordrelinjer, før du foretager frigivelsen til lagerstedet. Disse laster bruger samme konsolideringslogik, som blev introduceret sammen med konsolideringen af forsendelsespolitikker.

Du kan bruge siden **Panelet Forsendelseskonsolidering** til at konsolidere eksisterende forsendelser, der endnu ikke er bekræftet, men som allerede er frigivet til lagerstedet. Denne funktionalitet understøtter scenarier, hvor den automatiserede udgivelsesproces, der har sin egen forsendelseskonsolidering, køres flere gange om dagen, men potentielle yderligere konsolideringer skal angives manuelt, før forsendelsen til fragtmænd fuldføres under bekræftelsesprocessen. Denne funktionalitet giver dig mulighed for at konsolidere udgående forsendelser, der er oprettet fra salgsordre- eller flytteordrelinjer på et hvilket som helst tidspunkt, efter at forsendelserne frigives til lagerstedet, men før de bekræftes.

Siden **Panelet Siden Forsendelseskonsolidering** fungerer ligesom panelet for lastopbygning, hvor du kan vurdere flere forsendelser samtidigt og tildele en ikke-konsolideret ordre til en bestemt forsendelse. Du kan anvende skabeloner til forsendelseskonsolidering for at vurdere foreslåede konsolideringer flere gange og bekræfte dem. Nogle regler implementeres for at forhindre uautoriseret konsolidering og advare dig om eventuelle fejl.

## <a name="overview-of-new-functionality"></a>Oversigt over nye funktioner

I dette afsnit beskrives de sider, kommandoer og funktioner, der ændres eller tilføjes, når du aktiverer og bruger funktionen *Politikker for forsendelseskonsolidering*.

### <a name="shipment-consolidation-policies-page"></a>Siden Politikker for forsendelseskonsolidering

Politikker differentieres via typen af arbejdsordre. Typen **Salgsordrer** repræsenterer forsendelser af typen _Salesordre_, og **Flytteordrer** repræsenterer forsendelser af typen  _Flytteafgang_.

Enhver politik for forsendelseskonsolidering har en forespørgsel, der definerer, hvornår den anvendes, og et sekvensnummer, der bestemmer udførelsesrækkefølgen. Konsolidering anvendes for hver entydig kombination af de valgte felter. En yderligere parameter, der angives, bruges til konsolidering med eksisterende (åbne) forsendelser. Politikkerne evalueres og anvendes, hver gang der oprettes en ny forsendelse (før bølgebehandling).

Hvis en politik mangler obligatoriske felter, eller hvis den omfatter forbudte felter, er politikken markeret som ikke gyldig i sektionen **Valgt**. Listerne over obligatoriske og forbudte felter er faste og kan udvides.

Følgende liste viser de obligatoriske felter. Da forsendelser altid opdeles ud fra disse felter, kan du ikke gruppere flere forsendelser, der har forskellige værdier for disse felter.

- For salgsordrer:

    - **Kontonummer:** _WHSShipmentTable.AccountNum_
    - **Leveringsmodtager:** _WHSShipmentTable.DeliveryName_
    - **Postadresse (RecId):** _WHSShipmentTable.DeliveryPostalAddress_
    - **Lagersted:** _WHSShipmentTable.InventLocationId_

- For flytteordrer:

    - **Fra lagersted:** _InventTransferTable.InventLocationIdFrom_
    - **Til lagersted:** _InventTransferTable.InventLocationIdTo_

Følgende felter er ikke tilgængelige for alle dokumenttyper. Disse felter er ikke synlige i brugergrænsefladen (UI), og de kan ikke bruges til konsolidering.

- **Forsendelses-id:** _WHSShipmentTable.ShipmentId_
- **Status:** _WHSShipmentTable.ShipmentStatus_
- **Politik for forsendelseskonsolidering:** _WHSShipmentTable.ShipConsolidationPolicyName_
- **Arbejdstransaktionstype:** _WHSShipmentTable.WorkTransType_
- **Bølge-id:** _WHSShipmentTable.WaveId_
- **Last-id:** _WHSShipmentTable.LoadId_
- **Forsendelses-id:** _WHSLoadLine.ShipmentId_
- **Last-id:** _WHSLoadLine.LoadId_

Når du opretter en politik, bruges sættet med obligatoriske felter som standard som konsolideringsfelterne. Du kan dog redigere listen ved hjælp af venstre- og højre pileknapper. (Processen minder om processen til valg af metoder i bølgeskabeloner).

De værdier, som brugerne vælger for disse felter, bruges til alle nyoprettede forsendelser, eller de føjes til eksisterende forsendelser under konsolideringen med disse forsendelser. Hvis to forsendelser har samme værdi for et felt, der er valgt til konsolidering af disse forsendelser, konsolideres forsendelserne. Det samme princip gælder for alle de efterfølgende konsolideringsfelter, der er valgt. Hvis værdierne er forskellige, kasseres den anden forsendelse, og der vælges en ny forsendelse. Den automatiserede konsolideringsproces består i at oprette alle entydige kombinationer af værdier for felterne til forsendelseskonsolidering og derefter tildele en forsendelse til den relevante kombination.

Felter, der ikke er valgt, ignoreres under konsolideringsprocessen. Hvis to forsendelser har forskellige værdier for et felt, der ikke er markeret, ryddes feltet (dvs. det er angivet som tomt). Hvis begge forsendelser har samme værdi for et felt, der ikke er valgt, udfyldes feltet.

Listen over konsolideringsfelter (dvs. felter, der fjernes, hvis de har forskellige værdier) er faste. Listen indeholder alle de felter, der er initialiseret fra en salgsordre- eller flytteordrelinje, når der oprettes en ny forsendelse. Det vil med andre ord sige, at hvis et felt ikke er initialiseret fra en salgsordre- eller flytteordrelinje, ignoreres det, når der føjes nye data til en eksisterende forsendelse.

### <a name="release-to-warehouse-page"></a>Siden Frigiv til lager

- Et nyt felt i det nederste gitter viser, hvilken konsolideringspolitik der blev anvendt.
- Med en ny knap kan du manuelt vælge og/eller tilsidesætte konsolideringspolitikken.

### <a name="release-to-warehouse-command-on-the-load-planning-workbench-page"></a>Kommandoen Frigiv til lagersted på siden Panelet Lastplanlægning

- Logikken blev justeret, så den bruger anvendte konsolideringspolitikker.
- Forsendelser konsolideres nu kun inden for en enkelt last.

### <a name="consolidate-shipments-page"></a>Siden Konsolider forsendelser

- Søgningen efter lignende forsendelser (dvs. kandidater til konsolidering) blev ændret, så den bruger de felter, der er valgt i politikken for forsendelseskonsolidering.
- Felter, der har forskellige værdier i forskellige forsendelser, angives nu som tomme. (Tidligere blev værdierne fra den valgte "basis"-forsendelse anvendt.)

### <a name="shipment-consolidation-workbench-page"></a>Siden for panelet Forsendelseskonsolidering

- Nye funktioner replikerer processen med manuel konsolidering på en større skala.
- Du kan nu åbne denne side fra menuen **Frigiv til lagersted** i modulet **Lagerstedsstyring**.
- Algoritmen analyserer eksisterende forsendelser, der endnu ikke er afsendt. Derefter foreslår den en konsolidering, baseret på felter, der er valgt i konsolideringspolitikkerne.

## <a name="comparison-of-functionality"></a>Sammenligning af funktioner

Følgende tabel viser en oversigt over, hvordan forsendelseskonsolidering fungerer, når du ikke bruger politikker for forsendelseskonsolidering, og når du bruger dem.

| Uden politikker for forsendelseskonsolidering | Med politikker for forsendelseskonsolidering |
|---|----|
| Ikke relevant | Salgs- eller flytteforsendelser, der er valgt til konsolidering, skal have samme konsolideringspolitik som den forsendelse, der oprettes, eller de skal knyttes til en åben forsendelse (når indstillingen **Konsolider med eksisterende forsendelser** er aktiveret). |
| Proceduren *Frigiv til lager* søger ikke mellem eksisterende forsendelser for at finde en forsendelse til konsolidering. Det er kun forsendelser, der oprettes af en aktuel forekomst af proceduren *Frigiv til lager*, der bruges til at finde en forsendelse til konsolidering. | Hvis indstillingen **Konsolider med eksisterende forsendelser** er aktiveret for en konsolideringspolitik, der bruges i øjeblikket, søger proceduren *Frigiv til lagersted* mellem eksisterende forsendelser, der er oprettet på basis af samme konsolideringspolitik, for at finde en forsendelse til konsolidering. Hvis du derfor har to politikker, vil en forsendelse, der oprettes på basis af politik 2, aldrig blive konsolideret med en forsendelse, der er oprettet på basis af politik 1. |
| Ikke relevant | Hvis en liste over felter til konsolideringspolitik er tom, eller hvis der ikke kan findes en politik, oprettes der en ny forsendelse for hver salgsordre- eller flytteordrelinje. |
| Følgende konsolideringsfelt definerer den entydige kombination af værdier, der bruges til at konsolidere forsendelser for en *flyttelinje*. (De øvrige felter ignoreres.)<ul><li>Ordrenummer (OrderNum)</li></ul> | Følgende konsolideringsfelter definerer den entydige kombination af værdier, der bruges til at konsolidere forsendelser for en *flyttelinje*. (De øvrige felter ignoreres.)<ul><li>Ordrenummer (OrderNum)</li><li>Leveringsmodtager (DeliveryName)</li><li>Postadresse (DeliveryPostalAddress)</li><li>ISO-landekode (CountryRegionISOCode)</li><li>Adresse (Address)</li><li>Lokation (InventSiteId)</li><li>Lagersted (InventLocationId)</li><li>Fragtmand (CarrierCode)</li><li>Fragttjeneste (CarrierServiceCode)</li><li>Leveringsmåde (ModeCode)</li><li>Fragtgruppe (CarrierGroupCode)</li><li>Leveringsbetingelser (DlvTermId)</li></ul>Disse felter er de eneste felter, der er tilgængelige og initialiseret, når der oprettes en ny forsendelse. |
| Følgende konsolideringsfelter definerer den entydige kombination af værdier, der bruges til at konsolidere forsendelser for en *salgslinje*. (De øvrige felter ignoreres.)<ul><li>Ordrenummer (OrderNum)</li><li>Kundereference (CustomerRef)</li><li>Debitorrekvisition (CustomerReq)</li><li>Leveringsbetingelser (DlvTermId)</li></ul> | Følgende konsolideringsfelter definerer den entydige kombination af værdier, der bruges til at konsolidere forsendelser for en *salgslinje*. (De øvrige felter ignoreres.)<ul><li>Ordrenummer (OrderNum)</li><li>Kontonummer (AccountNum)</li><li>Leveringsmodtager (DeliveryName)</li><li>Postadresse (DeliveryPostalAddress)</li><li>ISO-landekode (CountryRegionISOCode)</li><li>Adresse (Address)</li><li>Lokation (InventSiteId)</li><li>Lagersted (InventLocationId)</li><li>Fragtmand (CarrierCode)</li><li>Fragttjeneste (CarrierServiceCode)</li><li>Leveringsmåde (ModeCode)</li><li>Fragtgruppe (CarrierGroupCode)</li><li>Mægler-id (BrokerCode)</li><li>Retning (LoadDirection)</li><li>Leveringsbetingelser (DlvTermId)</li><li>Kundereference (CustomerRef)</li><li>Debitorrekvisition (CustomerReq)</li></ul>Disse felter er de eneste felter, der er tilgængelige og initialiseret, når der oprettes en ny forsendelse. |
| Ikke relevant | Følgende konsolideringsfelter er obligatoriske for en *salgslinje* og kan ikke fjernes:<ul><li>Kontonummer (AccountNum)</li><li>Leveringsmodtager (DeliveryName)</li><li>Postadresse (DeliveryPostalAddress)</li><li>Lagersted (InventLocationId)</li></ul>Disse felter tildeles som standard, når der oprettes en ny politik. De kan ikke fjernes. |
| Proceduren *Frigivelse af laster til lagersted* på siden **Panelet Lastplanlægning** bruger sin egen separate kode til at oprette forsendelser og bølger. | Politikker for forsendelseskonsolidering anvendes til at bestemme, hvilke felter der skal evalueres med henblik på konsolidering. Forsendelser konsolideres kun inden for en enkelt last. |
| Du kan vælge **Konsolider leverancer** manuelt på siden **Alle forsendelser** og derefter vælge en "destinationsbasisforsendelse". Filteret vil foreslå alle eksisterende forsendelser, der har tilsvarende værdier for flere nøglefelter. | Du kan vælge **Konsolider leverancer** manuelt på siden **Alle forsendelser** og derefter vælge en "destinationsbasisforsendelse". Systemet vil foreslå andre eksisterende forsendelser ved at sammenligne værdierne i flere nøglefelter, der er konfigureret til de relevante regler for forsendelseskonsolidering. |
| Du kan kun bruge kommandoen **Konsolider forsendelser** på siden **Alle forsendelser** til en enkelt forsendelse. | Siden **Panelet Forsendelseskonsolidering** hjælper dig med at finde et sæt forsendelser, der endnu ikke er i en afsendt tilstand. Disse afsendelser analyseres på basis af flere nøglefelter, der er konfigureret i dine regler for forsendelseskonsolidering. Alle forsendelser, hvor værdierne i disse felter foreslås til konsolidering.<p>Du kan vedligeholde konsolideringen manuelt ved at fjerne forsendelser fra foreslåede konsolideringer og/eller ved at føje forsendelser til dem. Der kan forekomme flere typer af fejl, men du kan tilsidesætte nogle af dem.</p> |
| **Designbemærkning:** Proceduren *Frigiv automatisk salgsordre til lagersted* opdeler salgslinjer i grupper. Hver gruppe har sin egen entydige værdi **ReleaseToWarehouseId** og behandles separat af proceduren *Frigive til lagersted*. Denne procedure opretter nyt arbejde uanset opsætningen af arbejdspause. | **Designbemærkning** Proceduren *Frigiv automatisk salgsordrer til lagersted* tildeler den samme **ReleaseToWarehouseId** til alle salgslinjer, der behandles. Alle salgslinjer behandles samtidigt af proceduren *Frigiv til lagersted*. For at sikre den tidligere funktionalitet skal du konfigurere arbejdsskift pr. forsendelses-id. |

## <a name="additional-resources"></a>Yderligere ressourcer

- [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]