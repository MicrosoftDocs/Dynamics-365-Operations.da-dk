---
title: Automatisk frigivelse af forsendelse til cross-docking
description: I dette emne beskrives en strategi for cross-docking, hvor du kan frigive en behovsordre automatisk til lagerstedet, når den produktionsordre, der leverer behovsantallet, færdigmeldes, så antallet flyttes direkte fra udlagringslokationen for produktionen til forsendelsesområdet.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: b86fe2f3ea4321dbe598233018934187ba0d713a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424427"
---
# <a name="auto-release-shipment-for-cross-docking"></a>Automatisk frigivelse af forsendelse til cross-docking

[!include [banner](../includes/banner.md)]

I dette emne beskrives en strategi for cross-docking, hvor du kan frigive en behovsordre automatisk til lagerstedet, når den produktionsordre, der leverer behovsantallet, færdigmeldes. På denne måde flyttes det antal, der kræves til opfyldelse af behovsordren, direkte fra udlagringslokationen for produktionen til forsendelsesområdet.

Cross-docking er en lagerekspeditionsproces, hvor det antal, der kræves for at opfylde en udgående ordre, sendes til ordrens forsendelsesområde eller stadieinddelte område fra den lokation, hvor den indgående ordre blev modtaget. (Den indgående ordre kan være en indkøbsordre, en flytteordre eller en produktionsordre). Den avancerede funktion til cross-docking understøtter alle forsynings- og behovsordrer, og den kræver, at det udgående behov frigives, før muligheden for cross-docking er identificeret. Den automatiske forsendelsesfunktion har følgende karakteristika:

- Den understøtter kun produktionsordrer som forsyning og kun salgsordrer og flytteordrer efter behov.
- Cross-docking-handlingen kan startes, selvom behovsordren ikke blev frigivet til lagerstedet, før leveringskvitteringen blev registreret (dvs. før produktionen blev færdigmeldt).

Denne cross-docking-funktion har to fordele:

- Lagerstedsoperationerne kan springe det trin over, der lægger antal færdigvarer i det generelle lagerområde, hvis disse antal kun skal plukkes igen for at opfylde den udgående ordre. I stedet kan antallet flyttes én gang fra outputlokationen til en pakke-/afsendelseslokation. På denne måde er funktionaliteten med til at minimere det antal gange, som lagerbeholdningen håndteres, og som i sidste ende bidrager til maksimering af tid og plads i lagerstedets produktion.
- Lagerstedsoperationerne kan udsætte frigivelsen af salgsordrer og flytteordrer til lagerstedet, indtil afgang af færdigvarer for den tilknyttede produktionsordre færdigmeldes. Denne fordel kan være særligt relevant i Fremstil til ordre-produktionsmiljøer, hvor produktionstiden har tendens til at være længere end gennemløbstiderne i Fremstil til lager-miljøer.

## <a name="prerequisites"></a>Forudsætninger

| Forudsætning | Beskrivelse |
|---|---|
| Element | Varen skal være aktiveret for lagerprocesser for lagersted.<p>**Bemærk:** Varer med fastvægt kan ikke inkluderes i cross-docking-processer.</p> |
| Lagersted | Lagerstedet skal være aktiveret for lagerprocesser for lagersted. |
| Skabeloner for cross-docking | Der skal defineres mindst én cross-docking-skabelon, der bruger **Ved leveringskvittering** som frigivelsespolitik for behov på et givet lagersted. |
| Arbejdsklasse | Der skal oprettes et arbejds klasse-ID til cross-docking for arbejdsordretypen **Cross-docking**. |
| Arbejdsskabeloner | Arbejdsskabeloner for arbejdsordretypen **Cross-docking** skal bruges til at oprette pluk og læg på lager-arbejde for cross-docking. |
| Lokationsvejledninger | Lokationsvejledninger for arbejdsordretypen **Cross-docking** skal bruges til at styre læg på lager-arbejdet på de lokationer, hvor salgsordreantal skal pakkes og leveres. |
| Afmærkning mellem en behovsordre og en produktionsordre | Lagersystemet kan udløse automatisk frigivelse af forsendelse af den udgående ordre og oprette cross-docking-arbejde ud fra outputlokationen i færdigmeldingshandlingen, hvis salgsordrer og flytteordrer er reserveret og afmærket til en produktionsordre. |

## <a name="example-cross-docking-flow"></a>Eksempel på cross-docking-flow

Et typisk cross-docking-flow består af følgende hovedtrin.

1. En modtager af en salgsordre opretter en salgsordre for et Fremstil til ordre-produkt. Det ønskede antal er typisk ikke på lager og skal først produceres.
2. Modtageren af salgsordren opretter en produktionsordre direkte fra salgsordrelinjen. På denne måde reserverer og afmærker salgsordrens modtager antallet af salgsordrer i forhold til produktionsordreantallet. 

    Alternativt angiver en produktionsplanlægger, at afmærkningen skal opdateres, når ordreforslagene autoriseres.

3. Produktionsordren gennemgår følgende trin:

    1. En produktionsplanlægger beregner og frigiver produktionsordren. (Forkalkulation omfatter reservation af råmateriale, og frigivelsen omfatter frigivelsen til et lagersted).
    2. En lagermedarbejder starter og fuldfører plukning af råmaterialer fra lagerlokationen til produktionens indlagringslokation i henhold til produktionens pluk-arbejde.
    3. En produktionsoperatør starter produktionsordren.
    4. I den sidste operation bruger en maskinoperatør mobilenheden til at færdigmelde produktionsordren.

4. Systemet bruger opsætningen til at identificere cross-docking-hændelsen for de to sammenkædede ordrer og fuldfører derefter disse opgaver:

    1. Frigiv automatisk den tilknyttede salgsordre til et lagersted for at oprette en forsendelse.
    2. Opret automatisk et cross-docking-arbejde, der har instruktioner om at plukke de færdige varer fra outputlokationen og flytte dem til den udgående lokation, som cross-docking-lokationsvejledningen har tildelt salgsordren.
    3. Bed en maskinoperatør om at fuldføre cross-docking-arbejdet, umiddelbart efter at produktionsordren er færdigmeldt.

5. Når cross-docking-arbejdet er fuldført, og antallet er læsset på køretøjet, bekræfter en planlægger på et udgående lagersted salgsforsendelsen.

## <a name="example-scenario"></a>Eksempelscenario

I dette scenario skal du have installeret demodata, og du skal bruge demodatafirmaet **USMF**.

### <a name="set-up-cross-docking-that-uses-the-auto-release-shipment-feature"></a>Konfigurere cross-docking, hvor funktionen til automatisk frigivelse af forsendelse bruges

#### <a name="cross-docking-template"></a>Cross-docking-skabelon

1. Gå til **Lagerstedsstyring** \> **Opsætning** \> **Arbejde** \> **Skabeloner for cross-docking**.
2. Vælg **Ny**.
3. Angiv **1** i feltet **Løbenummer**.
4. Angiv et navn i feltet **Cross-docking-skabelon-id ID**, f.eks. **XDock\_færdigmeldt**.
5. Vælg **Ved leveringskvittering** i feltet **Frigivelsespolitik for behov**.
6. Angiv nummeret på det lagersted, hvor du vil konfigurere den cross-docking-processen, i feltet **Lagersted**. I dette eksempel skal du vælge **51**.

    > [!NOTE]
    > Så snart du vælger **Ved leveringskvittering** som politik for behovsfrigivelse for skabelonen, vil alle andre felter på siden ikke være tilgængelige. Du kan heller ikke definere forsyningskilder. Dette funktionsmåde opstår, fordi cross-docking, der bruger funktionen til automatisk frigivelse af forsendelse, kun understøtter produktionsordrer som forsyningskilder, og det kræver, at der findes en afmærkning mellem salgsordrer og produktionsordrer. Hvis du vælger **Før leveringskvittering** som frigivelsespolitik for behov, er felterne under fanerne **Planlægning** og **Forsyningskilder** tilgængelige og kan redigeres.

#### <a name="work-classes"></a>Arbejdsklasser

1. Gå til **Lagerstyring** \> **Opsætning** \> **Arbejde** \> **Arbejdsklasser**.
2. Vælg **Ny**.
3. Angiv et navn i feltet **Arbejdsklasse-id**, f.eks. **CrossDock**.
4. I feltet **Arbejdsordretype** skal du vælge **Cross-docking**.

Du kan angive en eller flere gyldige lokationstyper for at begrænse de typer lokationer, hvor cross-docking-færdigvarer kan lægges.

#### <a name="work-templates"></a>Arbejdsskabeloner

1. Gå til **Lagerstedsstyring** \> **Opsætning** \> **Arbejde** \> **Arbejdsskabeloner**.
2. I feltet **Arbejdsordretype** skal du vælge **Cross-docking**.
3. Vælg **Ny**.
4. Angiv **1** i feltet **Løbenummer**.
5. Angiv et navn i feltet **Arbejdsskabelon**, f.eks. **CrossDock\_51**.
6. Vælg **Gem**.
7. Vælg **Nye** i sektionen **Arbejdsskabelondetaljer**.
8. For den nye linje skal du i feltet **Arbejdstype** vælge **Pluk**. Vælg **CrossDock** i feltet **Arbejdsklasse-id**.
9. Vælg **Ny**.
10. For den nye linje skal du i feltet **Arbejdstype** vælge **Læg på lager**. Vælg **CrossDock** i feltet **Arbejdsklasse-id**.

#### <a name="location-directives"></a>Lokationsvejledninger

En læg på lager-standard proces for færdigvarer kræver, at der er en **Læg på lager**-vejledning til flytning af plukkede produktionsantal til en almindelig lagerplads. På samme måde skal du konfigurere en **Læg på lager**-lokationsvejledning til cross-docking for at give arbejdet besked på at lægge det færdige antal på en angivet udgående lokation, der servicerer forsendelsen af den tilknyttede salgsordre.

I forbindelse med cross-docking, ligesom ved almindelig læg-på-lager af færdigvarer, behøver du ikke at oprette en lokationsvejledning for plukarbejdet, da outputlokationen er givet. Desuden forventes det, at denne outputlokation er konfigureret enten som standardoutputlokation i en af de ressourcerelaterede poster (dvs. ressourcen, ressourcegrupperelationen eller ressourcegruppen) eller som standardproduktionslokation for færdigvarer til en lagersted.

1. Gå til **Lagerstedsstyring** \> **Opsætning** \> **Lokationsvejledninger**.
2. I feltet **Arbejdsordretype** skal du vælge **Cross-docking**.
3. Vælg **Ny**.
4. Angiv **1** i feltet **Løbenummer**.
5. Angiv et navn i feltet **Navn**, f.eks. **Baydoor**.
6. Vælg **Læg på lager** i feltet **Arbejdstype**.
7. Vælg **5** i feltet **Sted**.
8. Vælg **51** i feltet **Lagersted**.
9. Gå til oversigtspanelet **Linjer**, og vælg **Ny**.
10. Angiv det maksimale antal i intervallet, f.eks. **1000000**, i feltet **Antal til**.
11. Vælg **Gem**.
12. Vælg **Ny** i oversigtspanelet **Handlinger for lokationsvejledninger**.
13. Angiv et navn i feltet **Navn**, f.eks. **Baydoor**.
14. Vælg **Gem**.
15. Du kan bruge standardforespørgselsfunktionen til at begrænse læg på lager-lokationer til en eller flere bestemte lokationer. Vælg **Rediger forespørgsel**, og vælg **51** som kriterium for feltet **Lagersted** i tabellen **Lokationer**.

### <a name="cross-dock-finished-goods-to-the-outbound-location"></a>Cross-docking af færdigvarer til den udgående lokation

Udfør følgende trin for at foretage cross-docking af antal færdigvarer til den udgående lokation for de tilknyttede salgsordre.

1. Gå til **Salg og marketing** \> **Salgsordrer** \> **Alle salgsordrer**.
2. Vælg **Ny**.
3. For salgsordrehovedet skal du vælge debitorkonto **US-001** og et lagersted, der er angivet til cross-docking, og som bruger funktionen til automatisk frigivelse af forsendelser.
4. Tilføj en linje for et færdigt produkt, og angiv **10** som antal.
5. I sektionen **Salgsordrelinjer** skal du vælge **Produkt og forsyning** \> **Produktionsordre**.
6. Gennemse standardværdierne i dialogboksen **Opret produktionsordre**, og vælg derefter **Opret**. Der oprettes en ny produktionsordre, som knyttes til salgsordren (dvs. den er reserveret og afmærket).
7. Valgfrit: Ret værdien i feltet **Antal**, så den er højere end den værdi, der kræves for at opfylde salgsordren. Når produktionsantallet er færdigmeldt, opretter systemet cross-docking-arbejde for det afmærkede antal og læg på lager-arbejde for det resterende antal i henhold til den almindelige procedure for håndtering af færdigvarernes læg på lager.

    Som tidligere nævnt skal der være en afmærkning mellem salgsordren og produktionsordren. Ellers vil cross-docking ikke fungere. Der kan oprettes en afmærkning på flere måder:

    - Systemet kan automatisk oprette afmærkningen i følgende situationer:

        - Produktionsordren oprettes manuelt direkte fra salgsordrelinjen (se trin 6).
        - Produktionsordreforslag autoriseres, og feltet **Opdater afmærkninger** er angivet til **Standard.**

    - Brugeren kan oprette afmærkningen manuelt ved at åbne siden **Afmærkning** fra behovsordrelinjen.

    > [!NOTE]
    > En afmærkning kan ikke oprettes manuelt for varer, der er konfigureret til at bruge lagermodeller, der er standard eller har vægtede gennemsnit.

8. På siden **Produktionsordre** i handlingsruden skal du vælge fanen **Produktionsordre**, og i gruppen **Proces** skal du vælge **Estimat** og derefter vælge **OK**. Ordren forkalkuleres, og råvareantallet er reserveret til produktionen.
9. Under fanen **Produktionsordre** i handlingsruden skal du vælge gruppen **Proces**, vælge **Frigiv** og derefter vælge **OK**. Der oprettes lagerpluk for råvarerne.
10. Åbn og gennemse arbejdet. Vælg **Arbejdsdetaljer** i gruppen **Generelt** under fanen **Lagersted** i handlingsruden. Notér dig arbejds-id'et.
11. Log på lagerstedsappen for at køre arbejde på lagersted 51.
12. Gå til **Produktion** \> **Produktionspluk**.
13. Angiv arbejds-id'et for at starte og fuldføre råvarepluk. 

    Når arbejdet er færdigmeldt, er antallet af råvarer tilgængeligt på produktionens indlagringslokation (**005** i USMF demodata), og kørslen af produktionsordren kan starte.

14. På siden **Produktionsordre** i handlingsruden skal du vælge fanen **Produktionsordre**, og i gruppen **Proces** skal du vælge **Start** og derefter vælge **OK**.
15. Gå i appen til **Produktion** \> **Færdigmeld og læg på lager**.
16. Angiv nummeret på produktionsordren og andre obligatoriske oplysninger i feltet **Prod-id**, og vælg **derefter OK**.

Bemærk, at der sker følgende:

- Frigivelsen til et lagersted udløses for den tilknyttede salgsordre.
- På baggrund af frigivelsen oprettes forsendelses- og cross-docking-arbejde. Dette arbejde giver lageroperatøren besked på at plukke det antal, der kræves for at opfylde salgsordrelinjen, og lægge det på den udgående lokation, der er angivet i lokationsvejledningen til cross-docking.
- Hvis produktionsordreantallet er større end det antal, der kræves af salgsordren, oprettes der et almindeligt læg på lager-arbejde. Dette arbejde giver lageroperatøren besked på at plukke antallet af færdigvarer, der er tilbage efter cross-docking, og flytte dem til almindelig opbevaring i overensstemmelse med lokationsvejledningen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]