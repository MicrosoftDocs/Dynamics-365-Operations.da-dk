---
title: Forsendelse af småpakker
description: Dette emne indeholder oplysninger om funktionen til forsendelse af småpakker (SPS). Denne funktion sætter Microsoft Dynamics 365 Supply Chain Management i stand til at sende oplysninger om en pakket container til fragtmanden og derefter modtage en forsendelseslabel, forsendelsessats og sporingsnummeret fra fragtmanden.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: e4682674e6f61b9b75276df57afa522b29b5f052fd8a4c450c7fcfbe79654f90
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780452"
---
# <a name="small-parcel-shipping"></a>Forsendelse af småpakker

[!include [banner](../../includes/banner.md)]

Funktionen til forsendelse af småpakker (SPS) giver Microsoft Dynamics 365 Supply Chain Management mulighed for at kommunikere direkte med fragtmænd ved at give en struktur til kommunikation via fragtmands-API'er. Denne funktionalitet er nyttig, når du sender individuelle salgsordrer via kommercielle fragtmænd i stedet for at bruge containerforsendelse eller LTL (Less than Load)-forsendelse.

SPS-funktionen interagerer med fragtmanden via et dedikeret *satsprogram*. Din organisation skal udvikle dette satsprogram i samarbejde med din fragtmand eller fragtmandens hubtjeneste. Satsprogrammet sætter Supply Chain Management i stand til at sende oplysninger om en pakket container til fragtmanden og derefter modtage en forsendelseslabel, forsendelsessats og sporingsnummeret fra fragtmanden.

Den forsendelsessats, der returneres, føjes til den tilknyttede salgsordre som et tillægsgebyr. Den forsendelsesetiket, der returneres, kan derefter automatisk udskrives ved hjælp af en ZPL-printer (Zebra Programming Language) og anvendes på forsendelsen. Fragtmanden vil scanne denne forsendelsesetiket ved afhentning af pakkerne på lagerstedet.

## <a name="prepare-your-system-to-support-sps"></a>Forberede systemet til at understøtte SPS

Før du kan begynde at bruge SPS-funktionalitet, skal du aktivere SPS-funktionen i Funktionsstyring, tilføje satsprogrammet og konfigurere modulerne **Transportstyring** og **Lokationsstyring** for at understøtte funktionen.

### <a name="turn-on-the-sps-feature"></a>Slå SPS-funktionen til

Før du kan bruge SPS-funktionen, skal den være slået til i dit system. Administratorer kan bruge arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Module** *Transportstyring*
- **Funktionsnavn:** *Forsendelse af småpakker*

### <a name="deploy-and-set-up-rate-engines"></a>Implementere og konfigurere satsprogrammer

Supply Chain Management inkluderer ikke nogen satsprogrammer. Du skal anskaffe eller oprette de satsprogrammer, du har brug for, og derefter føje dem til systemet. Microsoft stiller dog et demosatsprogram til rådighed, som du kan bruge til test.

#### <a name="download-and-deploy-the-demo-rate-engine"></a>Downloade og installere demosatsprogrammet

Følg disse trin for at hente demosatsprogrammet.

1. På GitHub kan du downloade [DLL-værten (dynamic-link library) til demosatsprogrammet](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).
1. På din Supply Chain Management-server skal du gemme DLL'en i mappen **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.

#### <a name="create-and-deploy-functional-rate-engines"></a>Oprette og implementere funktionelle satsprogrammer

Du kan finde flere oplysninger om oprettelse og implementering af funktionelle satsprogrammer, så de kan bruges i en produktion eller et testmiljø, under følgende emner:

- [Oprette et nyt transportstyringsprogram](../transportation/create-new-transportation-management-engine.md)
- [Konfigurere transportstyringsprogrammer](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

Yderligere oplysninger om, hvordan du opretter et SPS-satsprogram, finder du i følgende blogindlæg: [Forsendelse af småpakker: Sådan udnytter du funktionen til forsendelse af småpakker i Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a>Konfigurere et satsprogram i Supply Chain Management

Når du har oprettet og implementeret et satsprogram til SPS, skal du følge disse trin for at konfigurere det.

1. Gå til **Transportstyring \> Opsætning \> Programmer \> Satsprogram**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.
1. Angiv følgende felter i den nye række:

    - **Vurderingsprogram** – Angiv et entydigt navn til satsprogrammet. Hvis du bruger demosatsprogrammet, skal du angive *Demosatsprogram*.
    - **Navn** – Angiv en kort beskrivelse af satsprogrammet. Hvis du bruger demosatsprogrammet, skal du angive *Demosatsprogram*.
    - **Vurderingsmetadata-id** – Vælg det grundlag, der skal bruges til at beregne din sats. Din sats kan f.eks. beregnes ud fra afstand. Hvis du bruger demosatsprogrammet, kan du lade dette felt stå tomt.
    - **Programsamling** – Angiv filnavnet på den DLL-pakke, du har implementeret. Hvis du bruger demosatsprogrammet, skal du angive *TMSSmallParcelShippingEngine.dll*.
    - **Programklasse** – Angiv det klassenavn, der blev oprettet for dit satsprogram. Hvis du bruger demosatsprogrammet, skal du angive *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.

## <a name="example-scenario"></a>Eksempelscenario

I dette eksempelscenarie vises, hvordan du konfigurerer og bruger SPS, når du har forberedt systemet som beskrevet tidligere i dette emne. I dette scenarie bruges det tidligere nævnte demosatsprogram.

### <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Hvis du vil arbejde gennem dette scenarie ved hjælp af de demoposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

### <a name="set-up-the-scenario"></a>Konfigurere scenariet

I dette eksempelscenarie skal du have en demofragtmand, fragtmandsgruppe, pakkepolitik og pakkeprofil. I følgende underafsnit forklares, hvordan du kan forberede de poster, der kræves til scenariet. I et produktionsscenarie ligner opsætningsprocessen typisk den proces, der er beskrevet her. Du skal dog angive forskellige værdier.

#### <a name="set-up-carriers"></a>Konfigurere fragtmænd

Følg disse trin for at konfigurere en fragtmand.

1. Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Fragtmænd**.
1. Vælg **Ny** i handlingsruden for at tilføje en fragtmand.
1. Angiv følgende værdier på hoveddelen:

    - **Fragtmand:** *Demofragtmand*
    - **Navn:** *Demofragtmand*
    - **Tilstand:** *Fragt*

1. I oversigtspanelet **Oversigt** kan du angive følgende værdier:

    - **Aktivere fragtmand:** *Ja*
    - **Aktivere fragtmandsvurdering:** *Ja*

1. Gå til oversigtspanelet **Tjenester**, og vælg **Ny** for at føje en tjeneste til gitteret.
1. Angiv følgende værdier for den nye tjeneste:

    - **Fragttjeneste:** *Demofragtmandstjeneste*
    - **Navn:** *Demofragtmandstjeneste*
    - **Transportmetode:** *Fragt*

    Angiv tilfældige værdier for alle de andre felter efter behov. (Når du gemmer den nye fragtmandspost, oprettes der en ny leveringsmåde, og Feltet **Leveringsmåde** angives automatisk).

1. I oversigtspanelet **Vurderingsprofiler** skal du vælge **Ny** for at føje en vurderingsprofil til gitteret.
1. Angiv følgende værdier for den nye profil:

    - **Vurderingsprofil:** *Demofragtmandstjeneste*
    - **Navn:** *Demofragtmandstjeneste*
    - **Satsprogram:** *Demosatsprogram*

    Angiv tilfældige værdier for alle de andre felter efter behov.

1. Vælg **Gem** i handlingsruden.

Du kan finde flere oplysninger om at konfigurere fragtmænd under [Konfigurere fragtmænd](../transportation/tasks/set-up-shipping-carriers.md).

#### <a name="set-up-carrier-service-accounts"></a>Konfigurere fragttjenestekonti

Følg disse trin for at konfigurere en fragttjenestekonto.

1. Gå til **Transportstyring \> Opsætning \> Klassificering \> Fragttjenestekonto**.
1. Gå til handlingsruden, og vælg **Ny** for at tilføje en fragttjenestekonto.
1. Angiv følgende værdier for den nye konto:

    - **Fragtmand:** *Demofragtmand*
    - **Fragttjeneste:** *Demofragtmandstjeneste*
    - **Debitorkontonummer for fragtmand:** Det debitorkontonummer for fragtmanden, der bruges til at kontrollere og godkende forbindelsen til fragtmanden. Din fragtmand angiver denne værdi. Hvis du bruger demotjenesten, kan du angive en tilfældig værdi.
    - **Lokation:** *6*
    - **Lagersted:** *62*

    > [!NOTE]
    > Ofte er værdien **Debitorkontonummer for fragtmand** den eneste værdi, der kræves for at godkende forbindelsen. Men hvis fragtmanden kræver yderligere godkendelsesparametre, skal din organisation tilpasse denne side for at tilføje ekstra felter efter behov.

#### <a name="set-up-a-container-packing-policy"></a>Konfigurere en politik for containerpakning

Følg disse trin for at konfigurere en politik for containerpakning:

1. Hvis du ikke allerede har konfigureret en ZPL-printerdefinition, skal du bruge programmet Dokumentets ruteplanlægningsagent til at konfigurere den. Yderligere oplysninger finder du i [Oversigt over udskrivning af dokumenter](../../fin-ops-core/dev-itpro/analytics/print-documents.md) og relaterede emner.
1. Gå til **Lokationsstyring \> Konfiguration \> Containere \> Politikker for containerpakning**.
1. Gå til handlingsruden, og vælg **Ny** for at tilføje en politik for containerpakning.
1. Angiv følgende værdier på hoveddelen for den nye politik:

    - **Politik for containerpakning:** *Politik for demopakning*
    - **Beskrivelse:** En beskrivelse af politikken

1. I oversigtspanelet **Oversigt** kan du angive følgende værdier:

    - **Lagersted:** *62*
    - **Standardlokation til endelig forsendelse:** *Baydoor*
    - **Vægtenhed:** *KG*
    - **Politik for containerlukning:** *Automatisk frigivelse*
    - **Politik for containerfrigivelse:** *Gør disponibel ved endelig afsendelseslokation*

1. I oversigtspanelet **Containermanifest** skal du angive følgende værdier:

    - **Automatisk manifest ved containerlukning:** *Ja*
    - **Manifestkrav til container:** *Transportstyring*
    - **Udskriv containerindhold:** *Nej*

1. I oversigtspanelet **Udskrivning af fragtetiket** skal du angive følgende værdier:

    - **Udskriv forsendelsesetiket til containere:** *Altid*
    - **Printernavn:** Navnet på den ZPL-printer, der skal udskrive forsendelsesetiketter

#### <a name="set-up-a-packing-profile"></a>Konfigurere en pakningsprofil

Følg disse trin for at konfigurere en pakningsprofil.

1. Gå til **Lokationsstyring \> Konfiguration \> Pakning \> Pakningsprofiler**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en pakningsprofil til gitteret.
1. Angiv følgende værdier for den nye profil:

    - **Pakkeprofil-id:** *Demopakningsprofil*
    - **Beskrivelse:** En beskrivelse af profilen
    - **Politik for containerpakning:** *Politik for demopakning*
    - **Container-id-tilstand:** *Auto*
    - **Containertype:** *SmallBox*

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a>Konfigurere en debitor til at bruge SPS-fragtmanden

Følg disse trin for at konfigurere en kunde, så denne kan bruge den fragtmand, du har oprettet.

1. Gå til **Debitor \> Debitorer \> Alle debitorer**.
1. Find og vælg debitor *US-027* i gitteret.
1. Vælg **Debitorkonti for fragtmand** i gruppen **Konfiguration** på fanen **Generelt** i handlingsruden.
1. Vælg **Ny** på siden **Debitorkonti for fragtmand** i handlingsruden for at føje en konto til gitteret.
1. Angiv følgende værdier for den nye konto:

    - **Fragtmand:** *Demofragtmand*
    - **Debitorkontonummer for fragtmand:** *12345* (værdien er ikke vigtig for dette scenarie, men der vil blive henvist til den i næste afsnit).

### <a name="go-through-the-example-scenario"></a>Gennemgå eksempelscenariet

Når du har konfigureret alle eksempeldataene som beskrevet i forrige afsnit, er du klar til at gennemgå eksempelscenariet.

#### <a name="create-a-sales-order-and-process-the-work"></a>Oprette en salgsordre og behandle arbejdet

Følg disse trin for at oprette en salgsordre.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** for at oprette en ny salgsordre.
1. Gå til dialogboksen **Opret salgsordre**, og angiv **US-027** i feltet *Debitorkonto*.
1. Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.
1. Den nye indkøbsordre åbnes. I oversigtspanelet **Salgsordrehoved** skal du angive feltet **Debitorkontonummer for fragtmand** til den værdi, du valgte for denne debitor tidligere (*12345*).
1. Tilføj en salgslinje i sektionen **Salgsordrelinjer**, og angiv følgende værdier for den:

    - **Varenummer:** *A0002*
    - **Antal:** *1*
    - **Lokation:** *6*
    - **Lagersted:** *62*

1. Skift til **overskriftsvisningen**.
1. I oversigtspanelet **Levering** kan du angive følgende værdier:

    - **Fragtmand:** *Demofragtmand*
    - **Fragttjeneste:** *Demofragtmandstjeneste*

1. Skift tilbage til visningen **Linjer**. Hvis du bliver bedt om at opdatere leveringsmåden for salgslinjerne, skal du vælge **Ja**.
1. I sektionen **Salgsordrelinjer** skal du vælge den ordrelinje, du konfigurerede tidligere, og derefter vælge **Lager \> Reservation**.
1. På siden **Reservation** skal du vælge **Reserver parti** for at reservere det fulde antal på valgte linje på lagerstedet.
1. Luk siden **Reservation** for at vende tilbage til salgsordren.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

    Der oprettes arbejde for at flytte varer fra pluklokationen til pakkestationen.

1. I sektionen **Salgsordrelinjer** skal du vælge **Lagersted \> Forsendelsesoplysninger**.
1. Notér forsendelses-id'et på siden **Forsendelsesoplysninger**. Du skal bruge det, når du pakker forsendelsen på pakkestationen.
1. Luk siden **Forsendelsesoplysninger** for at vende tilbage til salgsordren.
1. Notér salgsordrenummeret, og gå derefter til **Lokationsstyring \> Arbejde \> Alt arbejde**.
1. Brug salgsordrenummeret til at finde og vælge det arbejde, der er oprettet for ordren.
1. I handlingsruden skal du på fanen **Arbejde** vælge **Fuldfør arbejde**.
1. Vælg et bruger-id i feltet **Bruger-id** på siden **Færdiggørelse af arbejde**. Vælg derefter **Valider arbejde** i handlingsruden.
1. Hvis arbejdet består valideringen du vælge **Fuldfør arbejde** i handlingsruden.

    Arbejdet er markeret som fuldført for at simulere bevægelsen af varer til pakkestationen.

#### <a name="pack-the-shipment"></a>Pakke forsendelsen

Følg disse trin for at pakke forsendelsen.

1. Gå til **Lokationsstyring \> Konfiguration \> Arbejder**, og kontrollér, at din brugerkonto er knyttet til en arbejderkonto til lokationsstyring.
1. Gå til **Lokationsstyring \> Pluk og containerisering \> Pakke**.
1. Angiv følgende værdier i dialogboksen **Vælg pakkestation**:

    - **Lokation:** *6*
    - **Lagersted:** *62*
    - **Lokation:** *Pakke*
    - **Pakkeprofil-id:** *Demopakningsprofil*

1. Vælg **OK**.
1. Siden **Pakke** vises. I et produktionsscenarie scanner en arbejder en nummerplade eller et forsendelses-id. I dette scenarie skal du dog åbne siden **Alle forsendelser** og slå forsendelsesnummeret op for den forsendelse, du netop har oprettet. Angiv derefter denne værdi i feltet **Nummerplade eller forsendelse** på siden **Pakke**. Du kan alternativt angive det forsendelses-id, du har noteret tidligere.
1. Gå til handlingsruden, og vælg **Ny container**.
1. I den dialogboks, der vises, vises detaljer om den nye container. Behold standardværdierne, og vælg derefter **OK**.
1. På siden **Pakke** skal du i handlingsruden **Varepakning** i feltet **Identifikator** vælge *A0002* for at pakke denne vare. Varen føjes til containeren.
1. Vælg **Containere til forsendelse** i handlingsruden.

    Siden **Containere til forsendelse**, der vises, indeholder en række for den container, du netop har oprettet. Feltet **Containermanifest-id** i denne række er dog tomt i øjeblikket, da du endnu ikke har modtaget forsendelsesetiketten og sporingsnummeret fra fragtmanden.

1. Gå til handlingsruden, og vælg **Luk container**.
1. I dialogboksen **Luk container** skal du angive feltet **Bruttovægt** til *1 kg* og derefter vælge **OK**.

    Forsendelsesetiketten skal nu udskrives på den ZPL-printer, du valgte tidligere. Den skulle ligne følgende eksempel:

    ![Eksempel på forsendelsesetiket.](media/sps-label-example.png "Eksempel på forsendelsesetiket")

1. Bemærk, at værdierne **Containermanifest-id** og **Samlet fragt** er tilføjet som modtaget fra fragtmanden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]