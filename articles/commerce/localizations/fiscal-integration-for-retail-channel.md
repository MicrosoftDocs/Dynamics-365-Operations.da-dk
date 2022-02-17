---
title: Oversigt over regnskabsintegration for Commerce-kanaler
description: Dette emne indeholder en oversigt over de regnskabsintegrationsfunktioner, der findes i Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 01/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 82913eaca1d56a5b0609480d8825717278eca132
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077186"
---
# <a name="overview-of-fiscal-integration-for-commerce-channels"></a>Oversigt over regnskabsintegration for Commerce-kanaler

[!include [banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Dette emne indeholder en oversigt over de regnskabsintegrationsfunktioner, der findes i Dynamics 365 Commerce. 

Regnskabsintegration omfatter integration med forskellige regnskabsenheder og -tjenester, der muliggør regnskabsregistrering af salg i overensstemmelse med lokal regnskabslovgivning, som har til formål at forhindre momssvindel i detailbranchen. Her er nogle typiske scenarier, som kan adresseres ved hjælp af regnskabsintegrationen:

- Registrere et salg på en regnskabsenhed, der er knyttet til POS, f.eks. en bonprinter, og udskrive en regnskabskvittering til kunden.
- Sende oplysninger, der er relateret til salg og returvarer, som er behandlet i Retail POS, sikkert til en ekstern webtjeneste, der styres af skattemyndighederne.
- Hjælpe med at sikre, at salgstransaktionsdata ikke kan ændres, ved hjælp af digitale signaturer.

Regnskabsintegrationsfunktionen er en struktur, der indeholder en almindelig løsning til yderligere udvikling og tilpasning af integrationen mellem Retail POS og regnskabsenheder og -tjenester. Funktionen indeholder også eksempler på regnskabsintegration, der understøtter grundlæggende scenarier for bestemte lande eller områder, og som kan bruges sammen med bestemte regnskabsenheder eller -tjenester. Et eksempel på regnskabsintegration består af flere udvidelser af Commerce-komponenter og er medtaget i SDK'et (Software Development Kit). Du kan finde flere oplysninger om regnskabsintegrationseksempler i [Eksempler på regnskabsintegration i Commerce SDK](#fiscal-integration-samples-in-the-commerce-sdk). Du kan finde oplysninger om, hvordan du installerer og bruger Commerce SDK'et, i [Arkitektur for udviklingsværktøjskasse (SDK) til Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md).

For at understøtte andre scenarier, der ikke understøttes af et regnskabsintegrationseksempel, for at integrere Retail POS med andre regnskabsenheder eller -tjenester eller for at opfylde kravene i andre lande eller områder, skal du enten udvide et eksisterende regnskabsintegrationseksempel eller oprette et nyt eksempel ved hjælp af et eksisterende eksempel.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Regnskabsregistreringsprocessen og eksempler på regnskabsintegration for regnskabsenheder og -tjenester

En regnskabsregistreringsproces i Retail POS kan bestå af et eller flere trin. Hvert trin omfatter regnskabsregistrering af bestemte transaktioner eller -hændelser i én regnskabsenhed eller -tjeneste. Følgende løsningskomponenter deltager i regnskabsregistreringen i en regnskabsenhed eller -tjeneste:

- **Udbyder af regnskabsdokument** – Denne komponent serialiserer transaktions-/hændelsesdata i det format, der også bruges til interaktion med regnskabsenheden eller -tjenesten, analyserer svar fra regnskabsenheden eller -tjenesten og lagrer svarene i kanaldatabasen. Filtypenavnet definerer også bestemte transaktioner og hændelser, der skal registreres.
- **Regnskabsconnector** – Denne komponent initialiserer kommunikationen med regnskabsenheden eller -tjenesten, sender anmodninger eller direkte kommandoer til regnskabsenheden eller -tjenesten ud fra transaktions-/hændelsesdata, der er hentet fra regnskabsdokument, og modtager svar fra regnskabsenheden eller -tjenesten

Et eksempel på regnskabsintegration kan indeholde Commerce Runtime (CRT), hardwarestation og POS-udvidelser for en udbyder af regnskabsdokumenter og en regnskabsconnector. Det indeholder også følgende komponentkonfigurationer:

- **Konfiguration af udbydere af regnskabsdokumenter** – Denne konfiguration definerer en outputmetode til og et format for regnskabsdokumenter. Den indeholder også en datatilknytning til moms og betalingsmetoder for at gøre data fra Retail POS kompatible med de værdier, der er foruddefineret i regnskabsenhedens eller -tjenestens firmware.
- **Konfiguration af regnskabsconnectoren** – Denne konfiguration definerer den fysiske kommunikation med den ønskede regnskabsenhed eller -tjeneste.

En regnskabsregistreringsproces for et bestemt POS-kasseapparat er defineret af en tilsvarende indstilling i POS-funktionalitetsprofilen. Du kan finde flere oplysninger om, hvordan du kan konfigurere en regnskabsregistreringsproces, overføre konfigurationer for regnskabsdokumentudbyderen og regnskabsconnectoren og ændre deres konfigurationsparametre, under [Konfigurere en regnskabsregistreringsproces](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Følgende typiske regnskabsregistreringsflow starter med en hændelse i POS (f.eks. færdiggørelse af en salgstransaktion) og implementerer en foruddefineret trinsekvens, der omfatter andre Commerce-komponenter (f.eks. CRT og Hardwarestation).

1. POS anmoder om et regnskabsdokument fra regnskabsintegrationsstrukturen (FIF).
1. FIF bestemmer, om den aktuelle hændelse kræver regnskabsregistrering.
1. FIF identificerer baseret på indstillingerne for regnskabsregistreringsprocessen en regnskabsconnector og en tilsvarende regnskabsdokumentudbyder, der skal bruges til regnskabsregistreringen.
1. FIF kører regnskabsdokumentudbyderen, der genererer et regnskabsdokument (f.eks. et XML-dokument), der repræsenterer detailtransaktionen eller -hændelsen.
1. FIF returnerer det genererede regnskabsdokument til POS.
1. POS anmoder om, at FIF sender regnskabsdokumentet til regnskabsenheden eller regnskabstjenesten.
1. FIF kører regnskabsconnectoren, der behandler regnskabsdokumentet og sender det til regnskabsenheden eller -tjenesten.
1. FIF returnerer regnskabssvaret (dvs. svaret fra regnskabsenheden eller -tjenesten) til POS.
1. POS analyserer regnskabssvaret for at afgøre, om regnskabsregistreringen blev udført korrekt. Efter behov anmoder POS om, at FIF håndterer eventuelle fejl, der er opstået. 
1. POS anmoder om FIF-processen og gemmer regnskabssvaret.
1. Regnskabsdokumentudbyderen behandler regnskabssvaret. Som en del af denne behandling fortolker udbyderen af regnskabsdokumentet svaret og udtrækker udvidede data fra det.
1. FIF gemmer svaret og de udvidede data i kanaldatabasen.
1. Efter behov udskriver POS en kvittering via en almindelig kvitteringsprinter, som er tilsluttet Hardwarestation. Kvitteringen kan indeholde påkrævede data fra regnskabssvaret.
 
Følgende eksempler viser udførelsesflow for regnskabsregistrering for typiske enheder eller tjenester.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Regnskabsregistrering sker via en enhed, der er tilsluttet hardwarestationen

Denne konfiguration bruges, når en fysisk regnskabsenhed som f.eks. en regnskabsprinter er tilsluttet hardwarestationen. Den gælder også, når kommunikationen med en regnskabsenhed eller -tjeneste sker via software, der er installeret på hardwarestationen. I dette tilfælde findes regnskabsdokumentudbyderen på CRT, og regnskabsconnectoren er placeret på Hardwarestation.

![Regnskabsregistrering sker via en enhed, der er tilsluttet hardwarestationen.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Regnskabsregistrering sker via en ekstern tjeneste

Denne konfiguration bruges, når regnskabsregistrering foretages via en ekstern tjeneste, f.eks. en webtjeneste, der betjenes af skattemyndighederne. I dette tilfælde findes både regnskabsdokumentudbyderen og regnskabsconnectoren på CRT.

![Regnskabsregistrering sker via en ekstern tjeneste.](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Regnskabsregistrering foretages internt i CRT

Denne konfiguration bruges, når der ikke kræves nogen ekstern regnskabsenhed eller -tjeneste til regnskabsregistrering. Den bruges f.eks., når regnskabsregistrering sker via digital signering af salgstransaktioner. I dette tilfælde findes både regnskabsdokumentudbyderen og regnskabsconnectoren på CRT.

![Regnskabsregistrering foretages internt i CRT.](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Regnskabsregistrering sker via en enhed eller tjeneste i det lokale netværk

Denne konfiguration bruges, når der findes en fysisk regnskabsenhed eller regnskabstjeneste i butikkens lokale netværk, og den indeholder en HTTPS-API (Application Programming Interface). I dette tilfælde findes regnskabsdokumentudbyderen på CRT, og regnskabsconnectoren er placeret på POS.

![Regnskabsregistrering sker via en enhed eller tjeneste i det lokale netværk.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Fejlhåndtering

Regnskabsintegrationen struktur indeholder følgende indstillinger til håndtering af fejl under regnskabsregistreringen:

- **Prøv igen** – Operatører kan bruge denne indstilling, så fejlen kan rettes hurtigt og regnskabsregistreringen kan køre igen. Denne indstilling kan f.eks. bruges, når regnskabsenheden ikke er tilsluttet, bonprinteren mangler papir, eller der er papirstop i bonprinteren.
- **Annuller** – Med denne indstilling kan operatører udskyde regnskabsregistreringen af den aktuelle transaktion eller hændelse, hvis noget mislykkes. Når registreringen udsættes, kan operatøren fortsat arbejde på POS og kan udføre alle handlinger, som regnskabsregistreringen ikke indgår i. Når en hændelse, der kræver brug af regnskabsregistreringen, indtræffer i POS (f.eks. når en ny transaktion åbnes), åbnes dialogboksen til håndtering af fejlen automatisk med besked til operatøren om, at den tidligere transaktion ikke blev registreret korrekt, og at fejlhåndteringsindstillingerne skal angives.
- **Spring over** – Operatører kan bruge denne indstilling, når regnskabsregistreringen kan udelades under bestemte betingelser og normal drift kan fortsættes på POS. F.eks. kan denne indstilling bruges, når en salgstransaktion, som regnskabsregistreringen mislykkedes for, kan registreres i en særlig papirkladde.
- **Markér som registreret** – Operatører kan bruge denne indstilling, når transaktionen er blevet registreret i regnskabsenheden (f.eks. når en regnskabskvittering et blevet udskrevet), men der opstod en fejl, da regnskabssvaret blev gemt i kanaldatabasen.
- **Udskyd** – Operatørerne kan bruge denne indstilling, når transaktionen ikke er registreret, fordi registreringstjenesten ikke var tilgængelig. 

> [!NOTE]
> Indstillingerne **Spring over**, **Markér som registreret** og **Udskyd** skal aktiveres i regnskabsregistreringsprocessen, før de bruges. Desuden skal operatørerne have tildelt tilsvarende rettigheder.

Indstillingerne **Spring over**, **Markér som registreret** og **Udskyd** gør det muligt for infokoder at hente nogle specifikke oplysninger om fejlen, f.eks. årsagen til fejlen eller en begrundelse for at springe regnskabsregistreringen over eller markere transaktionen som registreret. Du kan finde flere oplysninger om, hvordan du konfigurerer fejlhåndteringsparametre, i [Angive indstillinger for fejlhåndtering](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Valgfri regnskabsregistrering

Regnskabsregistrering kan være obligatorisk for visse operationer, men valgfri for andre. Regnskabsregistreringen af almindelige salg og returneringer kan eksempelvis være obligatorisk, mens regnskabsregistreringen af operationer, der er relateret til kunders indbetalinger, kan være valgfri. I dette tilfælde bør manglende regnskabsregistrering af et salg blokere for fremtidige salg, mens manglende regnskabsregistrering af en kundeindbetaling ikke bør blokere fremtidige salg. For at kunne skelne mellem obligatoriske og valgfrie operationer anbefaler vi, at du behandler dem via forskellige dokumentudbydere, og at du i processen for regnskabsregistrering fastsætter separate fremgangsmåder for de pågældende udbydere. Parametret **Fortsæt ved fejl** bør være aktiveret for enhver fremgangsmåde, der er relateret til valgfri regnskabsregistrering. Du kan finde flere oplysninger om, hvordan du konfigurerer fejlhåndteringsparametre, i [Angive indstillinger for fejlhåndtering](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Manuel kørsel igen af regnskabsregistrering

Såfremt regnskabsregistreringen af en transaktion eller hændelse er blevet udsat som følge af en fejl (eksempelvis hvis operatøren har valgt **Annuller** i dialogboksen til fejlhåndtering), kan du manuelt køre regnskabsregistreringen igen ved at anvende en tilsvarende operation. Du kan finde flere oplysninger under [Aktiver manuel udførelse af udsatte regnskabsregistreringer](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="postpone-option"></a>Indstillingen Udskyd

Du kan bruge indstillingen **Udskyd** til at fortsætte processen med regnskabsregistrering, hvis det aktuelle trin mislykkes. Den kan bruges, når der er en indstilling til sikkerhedskopiering af regnskabsregistrering.

### <a name="fiscal-registration-health-check"></a>Sundhedskontrol af regnskabsregistreringen

Proceduren for sundhedskontrol af regnskabsregistreringer verificerer regnskabsenhedens eller -tjenestens tilgængelighed, når visse hændelser finder sted. Såfremt regnskabsregistreringen ikke kan fuldførelse på nuværende tidspunkt, bliver operatøren adviseret herom på forhånd.

POS kører sundhedskontrollen, når følgende hændelser finder sted:

- Der åbnes en ny transaktion.
- En suspenderet transaktion kaldes tilbage.
- En salgs- eller returtransaktion færdiggøres.

Hvis sundhedskontrollen er mangelfuld, viser POS dialogboksen for sundhedskontrollen. Den pågældende dialogboks indeholder følgende knapper:

- **OK** – Denne knap tillader operatøren at se bort fra en fejl i sundhedskontrollen og fortsætte med at behandle operationen. Operatører kan alene vælge denne knap, såfremt rettigheden **Tillad, at springe sundhedskontrolfejl over** er aktiveret for dem.
- **Annuller** – Hvis operatøren vælger denne knap, annullerer POS den seneste handling (der tilføjes eksempelvis ikke et element til en ny transaktion).

> [!NOTE]
> Sundhedskontrollen køres udelukkende, hvis den nuværende operation kræver regnskabsregistrering, og parameteren **Fortsæt ved fejl** er deaktiveret for det aktuelle trin i regnskabsregistreringsprocessen. Du kan finde flere oplysninger under [Angiv indstillinger for fejlhåndtering](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Lagring af regnskabssvar i regnskabstransaktion

Når regnskabsregistrering af en transaktion eller en hændelse er foretaget, oprettes en regnskabstransaktion i kanaldatabasen og knyttes til den oprindelige transaktion eller hændelse. På samme måde, hvis indstillingen **Spring over** eller **Markér som registreret** er valgt for en mislykket regnskabsregistrering, gemmes disse oplysninger i en regnskabstransaktion. En regnskabstransaktion indeholder regnskabssvaret fra regnskabsenheden eller -tjenesten. Hvis regnskabsregistreringsprocessen består af flere trin, oprettes der en regnskabstransaktion for hvert trin i processen, der resulterede i en fuldført eller mislykket regnskabsregistrering.

Regnskabstransaktionerne overføres til Headquarters af *P-job*, sammen med transaktioner. I oversigtspanelet **Regnskabstransaktioner** på siden **Transaktioner i butik** kan du se de regnskabstransaktioner, der er knyttet til detailtransaktioner.

En regnskabstransaktion indeholder følgende oplysninger:

- Detaljer om regnskabsregistreringsprocessen (proces, connectorgruppe, connector osv.). Serienummeret for regnskabsenheden gemmes også i feltet **Kassenummer**, hvis disse oplysninger er inkluderet i regnskabssvaret.
- Status for regnskabsregistreringen: **Fuldført** for fuldført registrering, **Sprunget over**, hvis operatøren har valgt indstillingen **Spring over** for en mislykket registrering, **Markeret som registreret**, hvis operatøren har valgt indstillingen **Markér som registreret** eller indstillingen **Udskudt**, hvis operatøren har valgt indstillingen **Udskyd**.
- Infokodetransaktioner, der er relateret til en valgt regnskabstransaktion. Hvis du vil se infokodetransaktioner, skal du i oversigtspanelet **Regnskabstransaktioner** vælge en regnskabstransaktion, der har statussen **Sprunget over**, **Markeret som registreret** eller **Udskudt**, og derefter vælge **Infokodetransaktioner**.

Hvis du vælger **Udvidede data**, kan du også få vist visse egenskaber for regnskabstransaktionen. Listen over egenskaber, der kan vises, gælder specifikt for funktionen til regnskabsregistrering, som har genereret regnskabsposteringen. Du kan f.eks. få vist den digitale signatur, løbenummer, certifikataftryk, id for hash-algoritmer og andre egenskaber for regnskabsposteringer for den digitale signeringsfunktionalitet for Frankrig.

## <a name="fiscal-texts-for-discounts"></a>Regnskabstekster for rabatter

Nogle lande eller områder har særlige krav om yderligere tekster, der skal udskrives på regnskabskvitteringer, når der anvendes forskellige rabatter. Med regnskabsintegrationsfunktionen kan du oprette en særlig tekst for en rabat, der udskrives efter en rabatlinje på en regnskabskvittering. For manuelle rabatter kan du konfigurere en regnskabstekst for den infokode, der er angivet som **Produktrabat**-infokoden i POS-funktionalitetsprofilen. Du kan finde flere oplysninger om, hvordan du opretter regnskabstekster for rabatter, i [Oprette regnskabstekster for rabatter](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Udskrivning af X- og Z-regnskabsrapporter

Funktionen til regnskabsintegration understøtter generering af kasseoptællingsopgørelser, der er specifikke for den integrerede regnskabsenhed eller -tjeneste:

- Nye knapper, der kører tilsvarende operationer, skal føjes til POS-skærmlayoutet. Du kan finde flere oplysninger i [Konfigurere X/Z-regnskabsrapporter fra POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- I regnskabsintegrationseksemplet skal disse operationer sammenholdes med de tilsvarende handlinger for regnskabsenheden.

## <a name="fiscal-integration-samples-in-the-commerce-sdk"></a>Eksempler på regnskabsintegration i Commerce SDK

Følgende regnskabsintegrationseksempler er aktuelt tilgængelige i Commerce SDK:

- [Eksempel på integration af bonprinter for Italien](./emea-ita-fpi-sample.md)
- [Eksempel på integration af bonprinter i Polen](./emea-pol-fpi-sample.md)
- [Eksempel på integration af regnskabsregistreringstjeneste for Østrig](./emea-aut-fi-sample.md)
- [Eksempel på integration af regnskabsregistreringstjeneste i Tjekkiet](./emea-cze-fi-sample.md)
- [Eksempel på integration med kontrolenhed for Sverige](./emea-swe-fi-sample.md)
- [Eksempel på integration af regnskabsregistreringsservice i Tyskland](./emea-deu-fi-sample.md)
- [Eksempel på integration af bonprinter i Rusland](./rus-fpi-sample.md)

Følgende funktionalitet til regnskabsintegration implementeres også ved hjælp af strukturen for regnskabsintegration, men den er tilgængelig fra feltet og er ikke inkluderet i Commerce SDK:

- [Regnskabsregistrering for Brasilien](./latam-bra-commerce-localization.md#fiscal-registration-for-brazil)
- [Digital signatur for Frankrig](./emea-fra-cash-registers.md)

Følgende regnskabsintegrationsfunktionalitet er også tilgængelig i Commerce SDK, men den kan i øjeblikket ikke udnytte strukturen for regnskabsintegration. Overførsel af denne funktion til regnskabsintegrationsstrukturen er planlagt til senere opdateringer.

- [Digital signatur for Norge](./emea-nor-cash-registers.md)

Følgende ældre finansintegrationsfunktionalitet, der er tilgængelig i Commerce SDK, anvender ikke strukturen for finansintegration og vil blive udfaset i senere opdateringer:

- [Eksempel på integration med kontrolenhed for Sverige (forældet)](./retail-sdk-control-unit-sample.md)
- [Digital signatur for Frankrig (ældre)](./emea-fra-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
