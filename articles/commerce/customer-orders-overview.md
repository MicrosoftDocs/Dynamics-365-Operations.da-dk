---
title: Kundeordrer i POS
description: Dette emne indeholder oplysninger om kundeordrer i POS. Kundeordrer kaldes også specialordrer. Emnet indeholder en beskrivelse af relaterede parametre og transaktionsflow.
author: josaw1
ms.date: 08/02/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom:
- "260594"
- intro-internal
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9ebdad47d761f775cf26666dc3e2736818fb4832
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982812"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Kundeordrer i POS

[!include [banner](includes/banner.md)]

Dette emne indeholder oplysninger om, hvordan du kan oprette og styre kundeordrer i appen POS. Kundeordrer kan bruges til at registrere salg, hvor kunder ønsker at afhente produkter på en senere dato, afhente produkter fra en anden adresse eller få varer leveret til dem. 

Med et hav af tilgængelige kanaler i handelsverdenen giver mange detailhandlere mulighed for kundeordrer eller specialordrer for at opfylde forskellige produkt- og opfyldelseskrav. Her er nogle typiske scenarier:

- En kunde ønsker, at produkter skal leveres til en bestemt adresse på en bestemt dato.
- En kunde ønsker at afhente varer fra en butik eller et sted, der er forskelligt fra butikken eller det sted, hvor kunden købte varerne.
- En kunde på en butiks adresse ønsker at bestille produkter i dag og afhente dem fra samme butiksadresse på en senere dato.

Detailhandlere kan bruge kundeordrer til at minimere manglende salg, som ellers kan skyldes, at en vare midlertidigt ikke kan leveres, da varerne kan leveres eller afhentes på et andet tidspunkt eller sted.

## <a name="set-up-customer-orders"></a>Konfigurere kundeordrer
Før du forsøger at bruge kundeordrefunktionaliteten i POS, skal du sørge for at fuldføre alle nødvendige konfigurationer i Commerce Headquarters.

### <a name="configure-modes-of-delivery"></a>Konfigurere leveringsmetoder

Hvis du vil bruge kundeordrer, skal du konfigurere leveringsmåder, som butikskanalen kan bruge. Du skal definere mindst én leveringsmåde, der kan bruges, når der sendes ordrelinjer til en kunde fra en butik. Du skal også definere mindst én levering gennem afhentning, der kan bruges, når der afhentes ordrelinjer fra butikken. Leveringsmåder defineres på siden **Leveringsmåder** i Commerce Headquarters. Du kan finde flere oplysninger om, hvordan du kan konfigurere leveringsmåden for Commerce-kanaler, under [Definere leveringsmåder](./configure-call-center-delivery.md#define-delivery-modes).

![Siden Leveringsmåder.](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Konfigurere opfyldelsesgrupper

Nogle butikker eller lagersteder kan muligvis ikke opfylde kundeordrer. Ved at konfigurere opfyldelsesgrupper kan en organisation angive, hvilke butikker og lagersteder der vises som muligheder for brugere, der opretter kundeordrer i POS. Opfyldelsesgrupper konfigureres på siden **Opfyldelsesgrupper**. Organisationer kan oprette lige så mange opfyldelsesgrupper, som de har brug for. Når der er defineret en opfyldelsesgruppe, skal den knyttes til en butik ved hjælp af **Gruppetildeling for opfyldelse** fra fanen **Opsætning** i handlingsruden på siden **Butikker**.

I Commerce version 10.0.12 og nyere kan organisationer definere, om lagerstedet eller de kombinationer af lagersted og butik, der er defineret i opfyldelsesgrupper, kan bruges til forsendelse, til afhentning eller til både forsendelse og afhentning. Dette giver ekstra fleksibilitet til at virksomheden kan bestemme, hvilke lagersteder der kan vælges, når der oprettes en kundeordre for varer, der skal afsendes, vs. hvilke butikker der kan vælges, når der oprettes en kundeordre for varer, der skal afhentes. Hvis du vil bruge disse konfigurationsindstillinger, skal du aktivere funktionen **Mulighed for at angive steder som "Forsendelse" eller "Afhentning" er aktiveret i opfyldelsesgruppe**. Hvis et lagersted, der er knyttet til en opfyldelsesgruppe, ikke er en butik, kan det kun konfigureres som et afsendelsessted. Det kan ikke bruges, når der er konfigureret ordrer til afhentning i POS.

![Sidan Opfyldelsesgrupper.](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Konfigurere kanalindstillinger

Når du arbejder med kundeordrer i POS, skal du overveje nogle af indstillingerne for butikskanalen. Disse indstillinger findes på siden **Butikker** i Commerce Headquarters.

- **Lagersted** – Dette felt angiver det lagersted, der skal bruges, når lagerbeholdningen falder for cash and carry og kundeafhentningsordrer, der er bundet til denne butik. Som en bedste praksis opfordrer vi til brug af entydige lagersteder for hver butikskanal for at forhindre konflikter mellem forretningslogik på tværs af butikker.
- **Forsendelseslagersted** – Dette felt angiver det lagersted, der skal bruges, når lagerbeholdningen falder for kundeordrer, der skal afsendes fra den valgte butik. Hvis funktionen **Mulighed for at angive lokationer som "Forsendelse" eller "Afhentning" er aktiveret i Opfyldningsgruppe**, er aktiveret i dit miljø, kan POS-brugere vælge et bestemt lagersted, der skal afsendes fra i POS, i stedet for at vælge en butik, der skal afsendes fra. Når denne funktion er aktiveret, anvendes afsendelseslagerstedet derfor ikke længere, da brugeren skal plukke det specifikke lagersted for at afsende ordren fra det tidspunkt, hvor ordren oprettes.
- **Gruppetildeling for opfyldelse** – Vælg denne knap (under fanen **Konfigurer** i handlingsruden) for at knytte de opfyldelsesgrupper, der refereres til, til at vise indstillinger for afhentningssteder eller forsendelsesoprindelse, når der oprettes kundeordrer i POS.
- **Brug destinationsbaseret moms** – Denne indstilling angiver, om forsendelsesadressen bruges til at bestemme, hvilken momsgruppe der anvendes på de ordrelinjer, der leveres til kundens adresse.
- **Brug kundebaseret moms** – Denne indstilling angiver, om den momsgruppe, der er defineret for kundens leveringsadresse, skal bruges til af lægge moms til kundeordrer, der oprettes i POS ved forsendelse til kundens hjem.

![Konfiguration af butikskanal på siden Butikker.](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Konfigurere kundeordreparametre

Før du forsøger at oprette kundeordrer i POS, skal du konfigurere de relevante parametre i Commerce Headquarters. Disse parametre findes under fanen **Kundeordrer** på siden **Commerce-parametre**.

- **Standardordretype** – Du kan angive den ordretype, der som standard tildeles kundeordrer, der er oprettet i POS. Disse kundeordrer kan enten være salgsordrer eller tilbudsordrer. Uanset standardordretypen kan brugerne stadig oprette både salgsordrer og kundeordrer fra POS.
- **Standard indbetalingsprocent** – Angiv den procentdel af det samlede ordrebeløb, som kunden skal betale som et depositum, før en ordre kan bekræftes. Afhængigt af deres rettigheder kan butiksansatte tilsidesætte beløbet ved at bruge handlingen **Tilsidesæt depositum** i POS, hvis denne operation er konfigureret til transaktionens skærmlayout.
- **Levering gennem afhentning** – Angiv den leveringsmåde, der skal anvendes på salgsordrelinjer, der er konfigureret til afhentning i POS.
- **Udførelsesleveringsmåde** – Angiv den leveringsmåde, der skal anvendes på salgsordrelinjer, der betragtes som udførelsesordrelinjer, når der oprettes en blandet indkøbsvogn, hvor nogle linjer skal afhentes eller afsendes, og andre linjer udføres med det samme af kunden.
- **Annulleringsgebyrprocent** – Hvis et gebyr skal anvendes, når en kundeordre annulleres, skal du angive beløbet på dette gebyr.
- **Annulleringsgebyrkode** – Angiv den debitorgebyrkode, der skal bruges, når et annulleringsgebyr anvendes på annullerede kundeordrer via POS. Gebyrkoden definerer den økonomiske bogføringslogik for annulleringsgebyret.
- **Forsendelsesgebyrkode** – Hvis indstillingen **Brug avancerede automatiske gebyr** er angivet til **Ja**, har denne parameter ingen virkning. Hvis denne indstilling er angivet til **Nej**, vil brugerne blive bedt om manuelt at angive et forsendelsesgebyr, når de opretter kundeordrer i POS. Brug denne parameter til at tilknytte en debitorgebyrkode, der skal anvendes på ordrer, når brugerne angiver et forsendelsesgebyr. Gebyrkoden definerer den økonomiske bogføringslogik for forsendelsesgebyret.
- **Brug avancerede automatiske gebyrer** – Angiv denne indstilling til **Ja** for at bruge systemberegnede automatiske gebyrer, når der oprettes kundeordrer i POS. Disse automatiske gebyrer kan bruges til at beregne forsendelsesgebyrer eller andre ordre- eller varespecifikke gebyrer. Du kan få flere oplysninger om, hvordan du konfigurerer og bruger avancerede automatiske gebyrer, i [Avancerede automatiske gebyrer for omni-kanal](./omni-auto-charges.md).

![Fanen Kundeordrer på siden Commerce-parametre.](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Opdatere transaktionsskærmlayout i POS

Sørg for, at POS-[skærmlayoutet](./pos-screen-layouts.md) er konfigureret til at understøtte oprettelse og styring af kundeordrer, og at alle nødvendige POS-operationer er konfigureret. Her er nogle af de POS-handlinger, der anbefales til at understøtte oprettelse og styring af kundeordrer korrekt:
- **Send alle produkter** – Denne operation bruges til at angive, at alle linjer i transaktionskurven skal leveres til en destination.
- **Send valgte produkter** – Denne operation bruges til at angive, at de valgte linjer i transaktionskurven skal leveres til en destination.
- **Afhent alle produkter** – Denne operation bruges til at angive, at alle linjer i transaktionskurven skal afhentes fra den valgte butiksadresse.
- **Afhent valgte produkter** – Denne operation bruges til at angive, at de valgte linjer i transaktionskurven skal afhentes fra den valgte butiksadresse.
- **Udfør alle produkter** – Denne operation bruges til at angive, at alle linjer i transaktionskurven skal udføres. Hvis denne operation bruges i POS, vil kundeordren blive konverteret til en kontant og afhentet-transaktion.
- **Udfør valgte produkter** – Denne operation bruges til at angive, at de valgte linjer i transaktionskurven udføres af kunden på købstidspunktet. Denne handling er kun nyttig i et scenarie for [hybrid ordre](./hybrid-customer-orders.md).
- **Tilbagekald ordre** – Denne handling bruges til at søge efter og hente kundeordrer, så POS-brugere kan redigere, annullere eller udføre opfyldelsesrelaterede operationer på dem efter behov.
- **Skift leveringsmåde** – Denne handling kan bruges til hurtigt at ændre leveringsmåden for linjer, der allerede er konfigureret til forsendelse, uden at kræve, at brugerne går gennem flowet "Send alle produkter" eller "Send valgte produkter" igen.
- **Tilsidesæt depositum** – Denne operation kan bruges til at ændre det depositumbeløb, som kunden vil betale for den valgte kundeordre.

![Operationer på POS-transaktionsskærmen.](media/customer-order-screen-layout.png)

## <a name="work-with-customer-orders-in-pos"></a>Arbejde med kundeordrer i POS

> [!NOTE]
> Funktionaliteten til indtægtsføring understøttes i øjeblikket ikke til brug i Handelskanaler (e-handel, POS, call center). Varer, der er konfigureret med indtægtsføring, bør ikke føjes til ordrer, der er oprettet i handelskanaler. 

### <a name="create-a-customer-order-for-products-that-will-be-shipped-to-the-customer"></a>Oprette en kundeordre for produkter, der skal sendes til kunden

1. Føj en kunde til transaktionen på POS-transaktionsskærmen.
2. Føj produkter til indkøbsvognen.
3. Vælg **Send valgte** eller **Send alle** for at sende produkterne til en adresse på kundekontoen.
4. Vælg muligheden for at oprette en kundeordre.
5. Bekræft eller rediger "levér fra"-adressen, bekræft eller ret leveringsadressen, og vælg en forsendelsesmåde.
6. Angiv kundens ønskede ordreforsendelsesdato.
7. Brug betalingsfunktionerne til at betale for beregnede beløb, der er forfaldne, eller brug handlingen **Tilsidesæt depositum** til at ændre de forfaldne beløb, og anvend derefter betaling.
8. Hvis hele ordretotalen ikke er betalt, skal du angive et kreditkort, der skal registreres for den saldo, der er forfalden på ordren, når den faktureres.

### <a name="create-a-customer-order-for-products-that-the-customer-will-pick-up"></a>Oprette en kundeordre for produkter, der skal afhentes af kunden

1. Føj en kunde til transaktionen på POS-transaktionsskærmen.
2. Føj produkter til indkøbsvognen.
3. Vælg **Hent valgte** eller **Hent alle** for at starte konfigurationen af ordreafhentning.
4. Vælg den butiksadresse, hvor kunden afhenter de valgte produkter.
5. Vælg en dato for afhentning af varen.
6. Brug betalingsfunktionerne til at betale for beregnede beløb, der er forfaldne, eller brug handlingen **Tilsidesæt depositum** til at ændre de forfaldne beløb, og anvend derefter betaling.
7. Hvis hele ordretotalen ikke er betalt, skal du vælge, om kunden skal betale på et senere tidspunkt (ved afhentning), eller om et kreditkort skal anføres nu og derefter bruges og registreres på afhentningstidspunktet.

### <a name="edit-an-existing-customer-order"></a>Rediger en eksisterende kundeordre

Detailordrer, der er oprettet i enten online- eller butikskanalen, kan tilbagekaldes og redigeres via POS efter behov.

> [!IMPORTANT]
> Ikke alle detailordrer kan redigeres via kasseprogrammet. Ordrer, der oprettes i en callcenter-kanal, kan ikke redigeres via POS, hvis indstillingen [Aktivér ordrefuldførelse](./set-up-order-processing-options.md#enable-order-completion) er slået til for callcenter-kanalen. For at sikre korrekt betalingsbehandling skal ordrer, der kommer fra en callcenter-kanal, og som bruger funktionen Aktivér ordrefuldførelse, skal redigeres via callcenter-programmet i Commerce Headquarters.

> [!NOTE]
> Det anbefales, at du ikke redigerer ordrer og tilbud i POS, som er oprettet af en bruger, som ikke er på callcenter, i Commerce Headquarters. Disse ordrer og tilbud bruger ikke Commerce-prissætningsprogrammet, så hvis de redigeres i POS, vil Commerce-prissætningsprogrammet ændre deres pris.


I version 10.0.17 og senere kan brugere redigere berettigede ordrer via kasseansøgningen, selvom ordren er delvist opfyldt. Ordrer, der er fuldt faktureret, kan dog ikke redigeres via POS. Hvis du vil aktivere denne funktion og give yderligere feedback, skal du aktivere funktionen **Rediger delvist opfyldte ordrer i POS** i arbejdsområdet **Funktionsstyring**. Hvis denne funktion ikke er aktiveret, eller hvis du bruger version 10.0.16 eller tidligere, kan brugerne kun redigere kundeordrer i POS, hvis ordren er helt åben. Hvis funktionen er aktiveret, kan du desuden begrænse de butikker, der kan redigere delvist opfyldte ordrer. Indstillingen for deaktivering af denne egenskab for bestemte butikker kan konfigureres via **funktionalitetsprofilen** i oversigtspanelet **Generelt**.


1. Vælg **Tilbagekald ordre**.
2. Brug **Søg** til at angive filtre for at finde ordren, og vælg derefter **Anvend**.
3. Vælg ordren på resultatlisten, og vælg derefter **Rediger**. Hvis knappen **Rediger** ikke er tilgængelig, er ordren i en tilstand, hvor den ikke kan redigeres.
4. Fra transaktionskurven kan du foretage ændringer i kundeordren efter behov. Visse ændringer kan være forbudt under redigering.
5. Fuldfør redigeringsprocessen ved at vælge en betalingshandling.
6. Hvis du vil afslutte redigeringsprocessen uden at gemme ændringer, kan du bruge handlingen **Afvis transaktion**.

#### <a name="pricing-impact-when-orders-are-edited"></a>Prissætningsvirkning, når ordrer redigeres

Når ordrer afgives i POS eller på et Commerce-e-handelswebsted, forpligter kunder sig til et beløb. Dette beløb omfatter en pris, og det kan også omfatte en rabat. En kunde, der afgiver en ordre og derefter kontakter callcenteret for at ændre ordren (f.eks. for at tilføje en vare), har særlige forventninger til anvendelsen af rabatter. Selvom kampagnerne på de eksisterende ordrelinjer er udløbet, forventer kunden, at de rabatter, der oprindeligt blev anvendt på disse linjer, forbliver gældende. Men hvis ingen rabat var gældende, da ordren oprindeligt blev afgivet, men en rabat siden da er trådt i kraft, forventer kunden, at den nye rabat anvendes på den ændrede ordre. Ellers kan kunden blot annullere den eksisterende ordre og derefter oprette en ny ordre, hvor den nye rabat anvendes. Som det fremgår af dette scenario, skal de priser og rabatter, som kunder har forpligtiget sig til, bevares. Brugerne af POS og callcenter skal samtidig have fleksibiliteten til at genberegne priser og rabatter for salgsordrelinjer efter behov.

Når ordrer tilbagekaldes og redigeres i POS, betragtes priserne og rabatterne på de eksisterende ordrelinjer som "låst". Det betyder, at de ikke ændres, selvom nogle af ordrelinjerne annulleres eller ændres, eller der tilføjes nye ordrelinjer. For at ændre priserne og rabatterne for eksisterende salgslinjer skal POS-brugeren vælge **Genberegn**. Prislåsen fjernes derefter fra de eksisterende ordrelinjer. Men før Commerce version 10.0.21 blev frigivet, var denne egenskab ikke tilgængelig i callcenteret. Hvis ordrelinjerne ændredes, blev priser og rabatter i stedet genberegnet.

I Commerce version 10.0.21 findes der en ny funktion med navnet **Undgå utilsigtet prisberegning for handelsordrer** i arbejdsområdet til **Funktionsstyring**. Denne funktion er som standard slået til. Når den er slået til, er der en ny **Pris låst** tilgængelig for alle e-handelsordrer. Når ordreregistreringen er fuldført for ordrer, der er afgivet fra en kanal, aktiveres denne egenskab automatisk (så afkrydsningsfeltet er markeret) for alle ordrelinjerne. Commerce-prissætningsprogrammet udelukker derefter disse ordrelinjer fra alle pris- og rabatberegninger. Hvis ordren redigeres, vil ordrelinjerne derfor som standard blive udeladt fra pris- og rabatberegningen. Callcenter-brugere kan dog deaktivere egenskaben (fjerne markeringen i afkrydsningsfeltet) for enhver ordrelinje og derefter vælge **Genberegn** for at medtage de eksisterende ordrelinjer i prisberegningerne.

Selvom de anvender en manuel rabat på en eksisterende salgslinje, skal callcenter-brugere deaktivere egenskaben **Pris låst** for salgslinjen, før de anvender den manuelle rabat.

Callcenter-brugere kan også deaktivere egenskaben **Pris låst** for ordrelinjer samlet ved at vælge **Fjern prislås** i gruppen **Beregn** under fanen **Sælg** i handlingsruden på **Salgsordre**-siden. I dette tilfælde fjernes prislåsen fra alle ordrelinjer med undtagelse af linjer, der ikke kan redigeres (med andre ord linjer, der har status som **Delvist faktureret** eller **Faktureret**). Når ændringerne af ordren er fuldført og afsendt, anvendes prislåsen derefter på alle ordrelinjerne igen.

> [!IMPORTANT]
> Når funktionen **Undgå utilsigtet prisberegning for handelsordrer** er slået til, ignoreres opsætningen af evaluering af samhandelsaftale i prissætningsarbejdsgangene. Med andre ord vises sektionen **Prisrelateret** ikke i dialogboksene til evaluering af samhandelsaftale. Denne funktionsmåde forekommer, fordi både konfigurationen af evalueringsfunktionen for samhandelsaftale og funktionen til prislås har et lignende formål: at forhindre utilsigtede prisændringer. Brugeroplevelsen til evaluering af samhandelsaftale er dog ikke velegnet til store ordrer, hvor brugerne skal vælge en eller flere ordrelinjer til ny prissætning.

> [!NOTE]
> **Pris låst**-egenskaben kan kun deaktiveres for en eller flere valgte linjer, når modulet **Callcenter** bruges. POS-funktionsmåden forbliver uændret. Det vil sige, at POS-brugeren ikke kan låse priser op for udvalgte ordrelinjer. De kan dog vælge **Genberegn** for at fjerne prislåsen fra alle eksisterende ordrelinjer.

### <a name="cancel-a-customer-order"></a>Annullere en kundeordre

1. Vælg **Tilbagekald ordre**.
2. Brug **Søg** til at angive filtre for at finde ordren, og vælg derefter **Anvend**.
3. Vælg ordren på resultatlisten, og vælg derefter **Annuller**. Hvis knappen **Annuller** ikke er tilgængelig, er ordren i en tilstand, hvor den ikke længere kan annulleres.
4. Hvis annulleringsgebyrer er konfigureret, skal du bekræfte dem. Du kan justere annulleringsgebyrerne, før du bekræfter dem, efter behov. 
5. Udfyld annulleringsprocessen ved at vælge en betalingshandling i transaktionskurven. Hvis depositum, der er betalt, overstiger annulleringsgebyret, kan refusionsbetalinger forfalde.
6. Hvis du vil afslutte annulleringsprocessen uden at gemme ændringer, kan du bruge handlingen **Afvis transaktion**.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>Afslutte forsendelse eller afhentning af kundeordre fra POS

Når en ordre er oprettet, vil varerne blive afhentet af kunden fra en butiksadresse eller afsendt, afhængigt af ordrens konfiguration. Du kan finde flere oplysninger om denne proces i dokumentationen til [opfyldelse af butiksordrer](./order-fulfillment-overview.md).

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynkront transaktionsflow for kundeordrer

Kundeordrer kan oprettes i POS i enten synkron eller asynkron tilstand. Hvis du bemærker problemer med ydeevnen eller brugerforsinkelser, når du opretter kundeordrer i POS, bør du overveje at aktivere oprettelse af asynkron ordre.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Aktivere kundeordrer, der skal oprettes i asynkron tilstand

1. I Commerce Headquarters skal du på siden **Funktionalitetsprofiler** vælge den funktionalitetsprofil, der svarer til den butik, du vil konfigurere.
2. I oversigtspanelet **Generelt** skal du vælge **Ja** for **Opret kundeordre i asynkron tilstand**.

Når indstillingen **Opret kundeordre i asynkron tilstand** er indstillet til **Ja**, oprettes kundeordrer altid i asynkron tilstand, også selvom Retail Transaction Service (RTS) er tilgængelig. Hvis du vælger **Nej** for denne indstilling, oprettes kundeordrer altid i synkron tilstand ved hjælp af RTS. Når der oprettes kundeordrer i asynkron tilstand, udtrækkes de og oprettes som detailtransaktioner i Commerce Headquarters fra Commerce Pull-job (P). De tilsvarende salgsordrer oprettes for detailtransaktioner, når **Synkroniser ordrer** køres enten manuelt eller via en batchproces.

## <a name="additional-resources"></a>Yderligere ressourcer

[Hybride kundeordrer](hybrid-customer-orders.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
