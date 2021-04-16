---
title: Refusionsbetalingsmetoder i callcentre
description: Dette emne forklarer, hvordan refusion af betalinger genereres via callcentre, når der oprettes returneringer, eller når ordrer eller ordrelinjer annulleres.
author: hhainesms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e3837ccebca0e6644ac5ded98344a5135cfb5d7a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799583"
---
# <a name="refund-payment-processing-in-call-centers"></a>Refusionsbetalingsmetoder i callcentre

Dette emne forklarer, hvordan refusion af betalinger genereres via callcentre, når der oprettes returneringer, eller når ordrer eller ordrelinjer annulleres.

En bruger, der opretter en returordre for en kunde som callcenter-bruger i Microsoft Dynamics 365 Commerce, bruger siden **Returordre** til at oprette den første godkendelse af returneringsmateriale (RMA). RMA definerer de produkter, kunden ønsker at returnere eller udveksle, og det opretter en tilknyttet retursalgsordre, der har ordretypen **Returordre**. Denne tilknyttede returordre bruges til at spore bogføringen af den returnerede lagerbeholdning og eventuelle kreditnotaer eller betalingsrefusioner, der er bogført.

Hvis indstillingen **Aktiver ordrefærdiggørelse** er angivet til **Ja** til opkaldscenterkanalen, skal den callcenter-bruger, der opretter RMA,køre behandling af ordre fuldførelse ved at vælge **Fuldført** på siden **Returordre**. Funktionen **Fuldfør** indeholder en beregnet returoversigt, der viser det skyldige refunderingsbeløb. Når den er konfigureret korrekt, oprettes der desuden systematisk en betalingslinje til refundering af den returnerede ordre.

Logikken i callcenter bestemmer betalingsmetoden for betalingslinjen for refusionen baseret på den betalingsmåde, der er brugt til den oprindelige ordre. Hvis den returordre, der er oprettet, ikke er knyttet til en oprindelig ordre, anvendes en standardbetalingsmåde, der er taget fra en systemparameter.

## <a name="how-a-call-center-determines-which-payment-method-to-apply-to-a-return-order"></a>Hvordan en callcenter afgør, hvilken betalingsmåde der skal anvendes til en returordre

Callcenter bruger betalingsmåden for den oprindelige ordre til at bestemme den betalingsmåde, der skal anvendes for en returordre. Nedenfor kan du se, hvordan denne proces fungerer for følgende oprindelige betalingsmetoder:

- **Normal** (kontant) eller **Check** – Når en returordre, der oprettes, refererer til en oprindelig ordre, der er betalt med brug af den normale (kontante) eller checkbetalingstype, refererer programmet til opkaldscenter til konfigurationer på siden **Refunderingsmetoder for callcenter**. På denne side kan organisationer definere i ordrevalutaen, hvordan refusioner udstedes til kunder for ordrer, der oprindeligt blev betalt ved hjælp af den normale betalingstype eller checkbetalingstypen. På siden **Refunderingsmetoder for callcenter** kan organisationer også vælge, om der skal sendes en systemgenereret refusionscheck til kunden, eller om der skal oprettes en debitorkontokreditering i forhold til den interne debitorkontosaldo. I disse scenarier refererer callcenter-logikken til returordren og bruger derefter værdien for **Detail-betalingsmåden** for den pågældende valuta til at oprette en betalingslinje til refundering på retursalgsordren. Senere sammenkædes en debitorbetalingskladde, der bruger den tilknyttede AR-betalingsmåde, med valutaen.

    I følgende illustration vises konfigurationen for et scenario, hvor en kunde returnerer produkter fra en salgsordre, der er knyttet til valutaen USD, og som oprindeligt blev betalt ved hjælp af den normale betalingstype eller checkbetalingstypen. I dette scenario vil der blive udstedt en refusion til kunden via en systemgenereret refusionskontrol. **REF-CHK** AR-betalingsmåden er konfigureret som en betalingstype til refunderingskontrol.

    ![Konfiguration af refunderingsmetoder for callcenter for normale betalinger og kontrol af oprindelige betalinger](media/callcenterrefundmethods.png)

- **Kreditkort** – Når en returordre, der oprettes, refererer til en oprindelig ordre, der blev betalt med kreditkort, anvender callcenter-logikken for refunderingsbetalinger samme oprindelige kreditkort på returordren.
- **Fordelskundekort** – Når en returordre, der oprettes, refererer til en oprindelig ordre, der blev betalt med fordelskundekort, anvender callcenter-logikken for refunderingsbetalinger til samme fordelskundekort på returordren.
- **Gavekort** (internt) – Når en returordre, der oprettes, refererer til en oprindelig ordre, der er betalt med et gavekort, der er udstedt fra Dynamics 365 Commerce (intern gavekortfunktionalitet), anvender callcenter-funktionen til refundering af betalinger refusionen til det samme oprindelige gavekortnummer.
- **Gavekort** (eksternt) – Når en returordre, der oprettes, refererer til en oprindelig ordre, der er betalt med et eksternt gavekort fra en ekstern tredjepart, anvender callcenter-logikken for refundering af betalinger den standardbetalingsmetode for returnering, der er defineret under fanen **RMA/Returnering**  på siden **Callcenter-parametre**.

Hvis den oprindelige ordrebetalingstype af en eller anden grund er ukendt, eller hvis der er brugt flere betalingsmåder til betaling for den oprindelige ordre, anvender callcenter-logikken den standardbetalingsmåde for returnering, der er defineret under fanen **RMA/Return** på siden **Callcenter-parametre**.

I følgende illustration vises feltet **Betalingsmåde** under fanen **RMA/Return** på siden **Callcenter-parametre**.

![Feltet Betalingsmåde under fanen RMA/Return på siden Callcenter-parametre.](media/callcenterrefundparameters.png)

> [!NOTE]
> De regler for refundering, der er beskrevet tidligere, gælder også for ordrer eller ordrelinjer, som en callcenter-bruger annullerer i Commerce Headquarters. Hvis annulleringen af en ordre eller bestemte ordrelinjer medfører overbetaling, anvendes samme regler til at generere betalingslinjer for refusion.

En returordre gennemgår typisk en standardproces, hvor der modtages (eller kasseres), bogføres en følgeseddel mod returordren, og der køres derefter en fakturabogføringsproces for retursalgsordren. Retursalgsordren sammenkædes og genereres systematisk som del af oprettelsen af returordren. I typiske tilfælde udstedes betalingsrefusioner ikke til kunder, før fakturaen for retursalgsordren bogføres.

### <a name="what-happens-when-an-invoice-is-posted-on-a-return-sales-order"></a>Hvad der sker, når en faktura bogføres på en retursalgsordre

Følgende scenarie beskriver, hvad der sker, når en faktura bogføres på en retursalgsordre:

- Hvis refunderingsbetalingen på returordren er for et kreditkort, aktiveres der en ekstra logik, når fakturaen bogføres. Denne logik kræver, at betalingsprocessoren refunderer betalingen til kundens kreditkort. Der oprettes også et bilag for refundering af debitorbetaling, som systematisk bogføres på kundens konto. Denne betalingskladde udlignes mod kreditnotabilaget for returordren.
- Hvis den refusionsbetaling, der skal udstedes, er for checkbetalingstypen, oprettes der et debitorbetalingsbilag, der bruger AR-betalingsmåden, som skal bogføres eller udskrives manuelt, før betalingsbilaget kan bogføres mod debitorkontoen. For at behandle refusionschecken kan brugere enten bruge siden **Debitorbetalingskladde** i Debitor eller den særlige side til **behandling af refundering** i Retail og Commerce.
- Hvis den refusionsbetaling, der skal udstedes, er for betalingstypen intern gavekort eller fordelskundekort, når returordren faktureres, oprettes og bogføres refunderingsbetalingsbilaget mod debitorkontoen. Ved dette faktureringstrin føjes refusionsbeløbet også tilbage til kundens internt sporede saldo for gavekort eller fordelskundepoint.
- Hvis en betalingsmåde, der bruger funktionen **Debitor** (f.eks. en debitorkonto), er knyttet til retursalgsordren, ignoreres valideringerne af kreditmaksimum, når betalingen behandles. Der oprettes eller bogføres ikke et betalingsbilag i denne sammenhæng. Når der bruges en debitorbetalingstype på en returordre, fungerer det kreditnotabilag, som fakturabogføringsprocessen opretter, som kundens kreditbilag og angiver en refusion til debitors AR-saldo.

## <a name="advance-credit"></a>Fremskynd kredit

Når en bruger behandler returordrer som en callcenter-bruger i et callcenter, hvor indstillingen **Aktiver ordrefærdiggørelse** er angivet til **Ja**, kan der indtræffe en undtagelse til den tidligere beskrevne proces for bogføring af refundering af refusion, hvis den callcenter-bruger, der opretter returordren, angiver kreditindstillingen **Forskud** til **Ja** under fanen **RMA/Returnering** på siden **Callcenter-parametre**. I dette tilfælde finder betalingsrefusionen sted, umiddelbart efter at returordren er blevet sendt med funktionen **Send** på oversigtssiden **Retur**. Systemet opretter med det samme et debitorbetalingsbilag for returværdien, selvom selve retursalgsordren endnu ikke er faktureret. Denne indfaldsvinkel kan bruges i situationer, hvor en organisation skal udstede refusioner til kunder på forhånd på grund af problemer med kundeservice, og organisationen ønsker ikke at kræve, at returneret lager modtages, før refusionerne udstedes.

## <a name="replacement-orders"></a>Erstatningsordrer

Når der udstedes en returordre, kan funktionen **Erstatningsordre** bruges til at generere en ny salgsordre for kunden. Denne indfaldsvinkel kan bruges i udvekslingsscenarier. Med funktionen **Erstatningsordre** oprettes endnu en salgsordre for de nye varer, der skal sendes, men der oprettes et krydsreferencelink under fanen **RMA/Return**  på siden **Callcenter-parametre**, der sammenkæder erstatningsordren, RMA og den returnerede salgsordre.

Når betalinger til en erstatningsordre behandles, har organisationer to muligheder:

- Refunder kunden for returordren på baggrund af den oprindelige betalingsmåde og opkræv derefter en separat betaling for erstatningsordren. Der kræves ingen yderligere konfiguration for at bruge denne indstilling.
- Indstil til **Anvend kredit** til **Ja** på fanen **RMA/Return** på siden **Callcenter-parametre**. I dette tilfælde anvendes en kundebetalingsmetode systematisk på både returordren og erstatningsordren. Denne indstilling kan hjælpe med at forhindre, at der udstedes nogen ekstern refundering. Det hjælper også med at forhindre enhver betalingsbehandling af transaktionen. Det kan være nyttigt i situationer, hvor en lige udveksling behandles, og organisationen foretrækker at bruge det kreditbilag, der oprettes, når returordren faktureres, til at betale for den faktura, der genereres af erstatningsordren. Når indstillingen **Anvend kredit** er angivet til **Ja**, skal organisationen udligne kreditnotaen manuelt mod fakturaen for erstatningsordren, når begge disse regnskabsdokumenter er genereret.

Indstillingen **Ja** til indstillingen **Anvend kredit** gælder kun, når returordren knyttes til en erstatningsordre. I dette tilfælde defineres den debitorbetalingsmåde, der bruges til systematisk betaling for returneringen og valutakursen ved feltet **Anvend betalingsmåde for kredit** under fanen **RMA/Retur** for siden **Callcenter-parametre**. I dette felt kan der vælges en betalingstype til funktionen **Debitor**.

> [!NOTE]
> I forbindelse med en returordre, der ikke har nogen tilknyttet erstatningsordre, påvirker indstillingen **Ja** for indstillingen **Anvend kredit** ikke betalingslogikken for returordren, da denne indstilling kun gælder for erstatningsordrer.

![Anvend feltet kreditbetalingsmetode under fanen RMA/Return på siden Callcenterparametre.](media/callcenterrefundparameters1.png)

> [!IMPORTANT]
> Hvis brugere, der opretter en plan for erstatningsordrer for at bruge indstillingen **Anvend kredit**, skal de ikke køre funktionen **Afsluttet** på returordren, før de angiver indstillingen **Anvend kredit** til **Ja**. Når funktionen **Fuldført** er udført, beregnes og anvendes refusionsbetalingen på retursalgsordren. Hvis du forsøger at angive indstillingen **Anvend kredit** til **Ja**, efter at en refusionsbetaling allerede er beregnet og anvendt, udløser det ikke en genberegning af refusionsbetalingen, og den betalingsmåde, der er valgt i feltet **Anvend betalingsmåde for kredit**, anvendes ikke. Hvis indstillingen **Anvend kredit** skal bruges i denne sammenhæng, skal brugeren slette erstatningsordren og RMA og derefter starte forfra og oprette en ny RMA. Denne gang skal brugeren sikre sig, at indstillingen **Anvend kredit** er angivet til **Ja**, før funktionen **Fuldført** køres.

## <a name="payment-overrides-for-call-center-returns"></a>Betalingsændring for callcenter-returneringer

Selvom det systematisk er callcenter-logikken, der bestemmer refunderingsmetoden på den måde, der er beskrevet tidligere i dette emne, vil brugerne måske nogle gange ønske at tilsidesætte disse betalinger. En bruger kan f.eks. redigere eller fjerne eksisterende betalingslinjer til refundering og anvende nye betalingslinjer. Systemberegnerede refusionsbetalinger kan kun ændres af brugere, som har de korrekte tilladelser til ændring. Disse tilladelser kan konfigureres på siden **Tilsidesæt tilladelser** i Retail og Commerce. Hvis du vil udføre en tilsidesættelse af refusionsbetaling, skal brugeren være knyttet til en sikkerhedsrolle, hvor indstillingen **Tillad alternativ betaling** er angivet til **Ja** på siden **Tilsidesæt tilladelser**.

![Tillad alternativ betalingsmåde på siden Tilsidesæt tilladelser](media/overridepermissions.png)

Alternativt kan en organisation angive indstillingen **Tillad betalingsændring** til **Ja** under fanen **RMA/Retur** på siden **Callcenter-parametre**. I dette tilfælde skal der vælges en kode til tilsidesættelse af sikkerhed i feltet **Kode til tilsidesættelse af sikkerhed**. Koden for sikkerhedsændring er en alfanumerisk kode, der skal administreres eksternt, da brugerne ikke kan se den i Commerce Headquarters, når den er angivet. Koden til sikkerhedsændring bør kun kendes af nogle få nøgler og betroede personer i en organisation. Når indstillingen **Tillad betalingstilsidesættelse** er angivet til **Ja**, hvis brugere, der ikke har de korrekte rolletilladelser, forsøger at ændre betalingsmåden for en returordre, har de mulighed for at angive sikkerhedsændringskoden. Hvis de ikke ved det, eller hvis en leder eller tilsynsførende ikke kan angive det på siden for dem, kan de ikke tilsidesætte betalingsmåden for returnering.

> [!NOTE]
> Hvis koden for sikkerhedsændringen går tabt eller glemtes, skal organisationen nulstille den ved at definere en ny **kode for sikkerhedsændring** i feltet Sikkerhedsændringskode under fanen **RMA/Return** for siden **Callcenter-parametre**.

![Parametre til betalingstilsidesættelse under fanen RMA/Return på siden Callcenter-parametre.](media/overridepaymentparameter.png)

> [!IMPORTANT]
> Før organisationer forsøger at tilsidesætte refusionsbetalinger, der bruger kreditkortbetalingstyper, skal de kontrollere, at deres kreditkortprocessor tillader returneringer, der ikke er sammenkædet. Mange processorer kræver, at refusioner bogføres tilbage på det oprindelige kort. Et forsøg på at udstede en refusion til et kort, der ikke tidligere er blevet indfanget, kan medføre, at der bogføres fejl med processoren.

## <a name="additional-resources"></a>Yderligere ressourcer

[Betalingsmetoder i callcentre](work-with-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]