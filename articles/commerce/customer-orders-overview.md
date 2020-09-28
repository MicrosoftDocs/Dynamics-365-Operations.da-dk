---
title: Kundeordrer i POS
description: Dette emne indeholder oplysninger om kundeordrer i POS. Kundeordrer kaldes også specialordrer. Emnet indeholder en beskrivelse af relaterede parametre og transaktionsflow.
author: josaw1
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9e5770de82638e6cef6d4c1dffd1dc85549fb11f
ms.sourcegitcommit: 30e4dc0a45f7de5f0a7178b1e88f7c3d61a7395e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/03/2020
ms.locfileid: "3763695"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Kundeordrer i POS

[!include [banner](includes/banner.md)]

Dette emne indeholder oplysninger om, hvordan du kan oprette og styre kundeordrer i POS. Kundeordrer kan bruges til at registrere salg, hvor kunder ønsker at afhente produkter på en senere dato, afhente produkter fra en anden adresse eller få varer leveret til dem. 

Med et hav af tilgængelige kanaler i handelsverdenen giver mange detailhandlere mulighed for kundeordrer eller specialordrer for at opfylde forskellige produkt- og opfyldelseskrav. Her er nogle typiske scenarier:

- En kunde ønsker, at produkter skal leveres til en bestemt adresse på en bestemt dato.
- En kunde ønsker at afhente varer fra en butik eller et sted, der er forskelligt fra butikken eller det sted, hvor kunden købte varerne.
- En kunde på en butiks adresse ønsker at bestille produkter i dag og afhente dem fra samme butiksadresse på en senere dato.

Detailhandlere kan bruge kundeordrer til at minimere manglende salg, som ellers kan skyldes, at en vare midlertidigt ikke kan leveres, da varerne kan leveres eller afhentes på et andet tidspunkt eller sted.

## <a name="set-up-customer-orders"></a>Konfigurere kundeordrer
Før du forsøger at bruge kundeordrefunktionaliteten i POS, skal du sørge for at fuldføre alle nødvendige konfigurationer i Commerce Headquarters.

### <a name="configure-modes-of-delivery"></a>Konfigurere leveringsmetoder

Hvis du vil bruge kundeordrer, skal du konfigurere leveringsmåder, som butikskanalen kan bruge. Du skal definere mindst én leveringsmåde, der kan bruges, når der sendes ordrelinjer til en kunde fra en butik. Du skal også definere mindst én levering gennem afhentning, der kan bruges, når der afhentes ordrelinjer fra butikken. Leveringsmåder defineres på siden **Leveringsmåder** i Commerce Headquarters. Du kan finde flere oplysninger om, hvordan du kan konfigurere leveringsmåden for Commerce-kanaler, under [Definere leveringsmåder](https://docs.microsoft.com/dynamics365/commerce/configure-call-center-delivery#define-delivery-modes).

![Siden Leveringsmåder](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Konfigurere opfyldelsesgrupper

Nogle butikker eller lagersteder kan muligvis ikke opfylde kundeordrer. Ved at konfigurere opfyldelsesgrupper kan en organisation angive, hvilke butikker og lagersteder der vises som muligheder for brugere, der opretter kundeordrer i POS. Opfyldelsesgrupper konfigureres på siden **Opfyldelsesgrupper**. Organisationer kan oprette lige så mange opfyldelsesgrupper, som de har brug for. Når der er defineret en opfyldelsesgruppe, er den knyttet til en butik ved hjælp af en knap under fanen **Opsætning** i handlingsruden på siden **Butikker**.

I Commerce version 10.0.12 og nyere kan organisationer definere, om lagerstedet eller de kombinationer af lagersted/butik, der er defineret i opfyldelsesgrupper, kan bruges til forsendelse, til afhentning eller til både forsendelse og afhentning. Butikken har derfor en ekstra fleksibilitet til at styre de lagersteds- og butiksindstillinger, der vises for brugere, som opretter en ordre for afhentning, i forhold til en forsendelsesordre. Hvis du vil udnytte disse konfigurationsindstillinger, skal du aktivere funktionen **Mulighed for at angive steder som "Forsendelse" eller "Afhentning" er aktiveret i opfyldelsesgruppe**. Hvis et lagersted, der er knyttet til en opfyldelsesgruppe, ikke er en butik, kan det kun konfigureres som et afsendelsessted. Det kan ikke bruges, når der er konfigureret ordrer til afhentning i POS.

![Sidan Opfyldelsesgrupper](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Konfigurere kanalindstillinger

Når du arbejder med kundeordrer i POS, skal du overveje nogle af indstillingerne for butikskanalen. Disse indstillinger findes på siden **Butikker** i Commerce Headquarters.

- **Lagersted** – I dette felt angives det lagersted, der skal bruges til at opfylde ordrer, der er konfigureret til forsendelse fra butikken.
- **Gruppetildeling for opfyldelse** – Vælg denne knap (under fanen **Konfigurer** i handlingsruden) for at knytte de opfyldelsesgrupper, der refereres til, til at vise indstillinger for afhentningssteder eller forsendelsesoprindelse, når der oprettes kundeordrer i POS.
- **Brug destinationsbaseret moms** – Denne indstilling angiver, om forsendelsesadressen bruges til at bestemme, hvilken momsgruppe der anvendes på de ordrelinjer, der leveres til kundens adresse.
- **Brug kundebaseret moms** – Denne indstilling angiver, om den momsgruppe, der er defineret for kundens leveringsadresse, skal bruges til af lægge moms til kundeordrer, der oprettes i POS ved forsendelse til kundens hjem.

![Konfiguration af butikskanal på siden Butikker](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Konfigurere kundeordreparametre

Før du forsøger at oprette kundeordrer i POS, skal du konfigurere de relevante parametre i Commerce Headquarters. Disse parametre findes under fanen **Kundeordrer** på siden **Commerce-parametre**.

- **Standardordretype** – Du kan angive den ordretype, der som standard tildeles kundeordrer, der er oprettet i POS. Disse kundeordrer kan enten være salgsordrer eller tilbudsordrer. Uanset standardordretypen kan brugerne stadig oprette både salgsordrer og kundeordrer fra POS.
- **Standard indbetalingsprocent** – Angiv den procentdel af det samlede ordrebeløb, som kunden skal betale som et depositum, før en ordre kan bekræftes. Afhængigt af deres rettigheder kan butiksansatte tilsidesætte beløbet ved at bruge handlingen **Tilsidesæt depositum** i POS, hvis denne operation er konfigureret til transaktionens skærmlayout.
- **Levering gennem afhentning** – Angiv den leveringsmåde, der skal anvendes på salgsordrelinjer, der er konfigureret til afhentning i POS.
- **Udførelsesleveringsmåde** – Angiv den leveringsmåde, der skal anvendes på salgsordrelinjer, der betragtes som udførelsesordrelinjer, når der oprettes en blandet indkøbsvogn, hvor nogle linjer skal afhentes eller afsendes, og andre linjer udføres med det samme af kunden.
- **Annulleringsgebyrprocent** – Hvis et gebyr skal anvendes, når en kundeordre annulleres, skal du angive beløbet på dette gebyr.
- **Annulleringsgebyrkode** – Angiv den debitorgebyrkode, der skal bruges, når et annulleringsgebyr anvendes på annullerede kundeordrer via POS. Gebyrkoden definerer den økonomiske bogføringslogik for annulleringsgebyret.
- **Forsendelsesgebyrkode** – Hvis indstillingen **Brug avancerede automatiske gebyr** er angivet til **Ja**, har denne parameter ingen virkning. Hvis denne indstilling er angivet til **Nej**, vil brugerne blive bedt om manuelt at angive et forsendelsesgebyr, når de opretter kundeordrer i POS. Brug denne parameter til at tilknytte en debitorgebyrkode, der skal anvendes på ordrer, når brugerne angiver et forsendelsesgebyr. Gebyrkoden definerer den økonomiske bogføringslogik for forsendelsesgebyret.
- **Brug avancerede automatiske gebyrer** – Angiv denne indstilling til **Ja** for at bruge systemberegnede automatiske gebyrer, når der oprettes kundeordrer i POS. Disse automatiske gebyrer kan bruges til at beregne forsendelsesgebyrer eller andre ordre- eller varespecifikke gebyrer. Du kan få flere oplysninger om, hvordan du konfigurerer og bruger avancerede automatiske gebyrer, i [Avancerede automatiske gebyrer for omni-kanal](https://docs.microsoft.com/dynamics365/commerce/omni-auto-charges).

![Fanen Kundeordrer på siden Commerce-parametre](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Opdatere transaktionsskærmlayout i POS

Sørg for, at POS-[skærmlayoutet](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts) er konfigureret til at understøtte oprettelse og styring af kundeordrer, og at alle nødvendige POS-operationer er konfigureret. Her er nogle af de POS-handlinger, der anbefales til at understøtte oprettelse og styring af kundeordrer korrekt:
- **Send alle produkter** – Denne operation bruges til at angive, at alle linjer i transaktionskurven skal leveres til en destination.
- **Send valgte produkter** – Denne operation bruges til at angive, at de valgte linjer i transaktionskurven skal leveres til en destination.
- **Afhent alle produkter** – Denne operation bruges til at angive, at alle linjer i transaktionskurven skal afhentes fra den valgte butiksadresse.
- **Afhent valgte produkter** – Denne operation bruges til at angive, at de valgte linjer i transaktionskurven skal afhentes fra den valgte butiksadresse.
- **Udfør alle produkter** – Denne operation bruges til at angive, at alle linjer i transaktionskurven skal udføres. Hvis denne operation bruges i POS, vil kundeordren blive konverteret til en kontant og afhentet-transaktion.
- **Udfør valgte produkter** – Denne operation bruges til at angive, at de valgte linjer i transaktionskurven udføres af kunden på købstidspunktet. Denne handling er kun nyttig i et scenarie for [hybrid ordre](https://docs.microsoft.com/dynamics365/commerce/hybrid-customer-orders).
- **Tilbagekald ordre** – Denne handling bruges til at søge efter og hente kundeordrer, så POS-brugere kan redigere, annullere eller udføre opfyldelsesrelaterede operationer på dem efter behov.
- **Skift leveringsmåde** – Denne handling kan bruges til hurtigt at ændre leveringsmåden for linjer, der allerede er konfigureret til forsendelse, uden at kræve, at brugerne går gennem flowet "Send alle produkter" eller "Send valgte produkter" igen.
- **Tilsidesæt depositum** – Denne operation kan bruges til at ændre det depositumbeløb, som kunden vil betale for den valgte kundeordre.

![Operationer på POS-transaktionsskærmen](media/customer-order-screen-layout.png)

## <a name="working-with-customer-orders-in-pos"></a>Arbejde med kundeordrer i POS

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
5. Vælg en afhentningsdato.
6. Brug betalingsfunktionerne til at betale for beregnede beløb, der er forfaldne, eller brug handlingen **Tilsidesæt depositum** til at ændre de forfaldne beløb, og anvend derefter betaling.
7. Hvis hele ordretotalen ikke er betalt, skal du vælge, om kunden skal betale på et senere tidspunkt (ved afhentning), eller om et kreditkort skal anføres nu og derefter bruges og registreres på afhentningstidspunktet.

### <a name="edit-an-existing-customer-order"></a>Rediger en eksisterende kundeordre

Detailordrer, der er oprettet i enten online- eller butikskanalen, kan tilbagekaldes og redigeres via POS efter behov.

> [!IMPORTANT]
> Ordrer, der oprettes i en callcenter-kanal, kan ikke redigeres via POS, hvis indstillingen [Aktivér ordrefuldførelse](https://docs.microsoft.com/dynamics365/commerce/set-up-order-processing-options#enable-order-completion) er slået til for callcenter-kanalen. For at sikre korrekt betalingsbehandling skal ordrer, der kommer fra en callcenter-kanal, og som bruger funktionen Aktivér ordrefuldførelse, skal redigeres via callcenter-programmet i Commerce Headquarters.

I Commerce version 10.0.13 og tidligere kan brugere kun redigere understøttede kundeordrer via POS, hvis ordrerne er fuldt åbne. Hvis der allerede er behandlet nogle linjer i en ordre til opfyldelse (pluk, pakke osv.), bliver ordren låst for redigering i POS.

> [!NOTE]
> I Commerce version 10.0.14 kan en funktion, der er frigivet i [offentlig prøveversion](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms), lade POS-brugere redigere kundeordrer via POS, selvom en del af ordren allerede er opfyldt. Ordrer, der er fuldt faktureret, kan dog ikke redigeres via POS. Hvis du vil teste denne prøveversionsfunktion og give yderligere feedback, skal du aktivere funktionen **(Prøveversion) Rediger delvist opfyldte ordrer i POS** i arbejdsområdet **Funktionsstyring**. Kundeordrer, der kommer fra en callcenter-kanal, og som bruger funktionen Aktivér ordrefuldførelse, kan ikke redigeres, selv når denne funktion er aktiveret.

1. Vælg **Tilbagekald ordre**.
2. Brug **Søg** til at angive filtre for at finde ordren, og vælg derefter **Anvend**.
3. Vælg ordren på resultatlisten, og vælg derefter **Rediger**. Hvis knappen **Rediger** ikke er tilgængelig, er ordren i en tilstand, hvor den ikke kan redigeres.
4. Fra transaktionskurven kan du foretage ændringer i kundeordren efter behov. Visse ændringer kan være forbudt under redigering.
5. Fuldfør redigeringsprocessen ved at vælge en betalingshandling.
6. Hvis du vil afslutte redigeringsprocessen uden at gemme ændringer, kan du bruge handlingen **Afvis transaktion**.



### <a name="cancel-a-customer-order"></a>Annullere en kundeordre

1. Vælg **Tilbagekald ordre**.
2. Brug **Søg** til at angive filtre for at finde ordren, og vælg derefter **Anvend**.
3. Vælg ordren på resultatlisten, og vælg derefter **Annuller**. Hvis knappen **Annuller** ikke er tilgængelig, er ordren i en tilstand, hvor den ikke længere kan annulleres.
4. Hvis annulleringsgebyrer er konfigureret, skal du bekræfte dem. Du kan justere annulleringsgebyrerne, før du bekræfter dem, efter behov. 
5. Udfyld annulleringsprocessen ved at vælge en betalingshandling i transaktionskurven. Hvis depositum, der er betalt, overstiger annulleringsgebyret, kan refusionsbetalinger forfalde.
6. Hvis du vil afslutte annulleringsprocessen uden at gemme ændringer, kan du bruge handlingen **Afvis transaktion**.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>Afslutte forsendelse eller afhentning af kundeordre fra POS

Når en ordre er oprettet, vil varerne blive afhentet af kunden fra en butiksadresse eller afsendt, afhængigt af ordrens konfiguration. Du kan finde flere oplysninger om denne proces i dokumentationen til [opfyldelse af butiksordrer](https://docs.microsoft.com/dynamics365/commerce/order-fulfillment-overview).

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynkront transaktionsflow for kundeordrer

Kundeordrer kan oprettes i POS i enten synkron eller asynkron tilstand. Hvis du bemærker problemer med ydeevnen eller brugerforsinkelser, når du opretter kundeordrer i POS, bør du overveje at aktivere oprettelse af asynkron ordre.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Aktivere kundeordrer, der skal oprettes i asynkron tilstand

1. I Commerce Headquarters skal du på siden **Funktionalitetsprofiler** vælge den funktionalitetsprofil, der svarer til den butik, du vil konfigurere.
2. I oversigtspanelet **Generelt** skal du vælge **Ja** for **Opret kundeordre i asynkron tilstand**.

Når indstillingen **Opret kundeordre i asynkron tilstand** er indstillet til **Ja**, oprettes kundeordrer altid i asynkron tilstand, også selvom Retail Transaction Service (RTS) er tilgængelig. Hvis du vælger **Nej** for denne indstilling, oprettes kundeordrer altid i synkron tilstand ved hjælp af RTS. Når der oprettes kundeordrer i asynkron tilstand, udtrækkes de og oprettes som detailtransaktioner i Commerce Headquarters fra Commerce Pull-job (P). De tilsvarende salgsordrer oprettes for detailtransaktioner, når **Synkroniser ordrer** køres enten manuelt eller via en batchproces.

## <a name="additional-resources"></a>Yderligere ressourcer

[Hybride kundeordrer](hybrid-customer-orders.md)
