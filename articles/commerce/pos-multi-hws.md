---
title: Dedikerede betalingsterminaler og anmodninger om printer og kasseskuffe
description: Dette emne indeholder oplysninger om muligheden for at have en dedikeret betalingsterminal og brugeranmodning om at vælge en pengeskuffe og en kvitteringsprinter.
author: rubendel
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 848e83505e9e20111c2809000dcf19f352142de4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223017"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a>Dedikerede betalingsterminaler og anmodninger om printer og kasseskuffe

[!include [banner](includes/banner.md)]

Dette emne indeholder oplysninger om muligheden for at have en dedikeret betalingsterminal og brugeranmodning om at vælge en pengeskuffe og en kvitteringsprinter.

## <a name="overview"></a>Overblik

Moderne detailhandlere søger efter måder at strømline betalingsoplevelsen i butikken. De seneste tendenser mod papirløs betaling ved hjælp af elektroniske løsninger er ikke blot med til at gøre indkøbsoplevelsen mere glidende, men reducerer også behovet for at have et fuldt sortiment af eksterne enheder til rådighed for hver butiksmedarbejder.

Microsoft Dynamics 365 Commerce understøtter disse tendenser ved at muliggøre et scenarie, hvor en POS-enhed får tildelt sin egen helt særlige betalingsterminal, men uden at have egen kvitteringsprinter eller pengeskuffe. Når medarbejderne skal udskrive en kvittering eller tage imod betaling i kontanter, bliver de bedt om at vælge en hardwarestation, hvor disse enheder er konfigureret.

## <a name="key-terms"></a>Vigtige termer

| Periode | Beskrivende tekst |
|---|---|
| Registrere | Den enhed, der bruges til at konfigurere en forekomst af et POS-kasseapparat. |
| Enhed | En repræsentation af den fysiske forekomst af et POS-kasseapparat og Modern POS-programmet, der er tildelt til det. |
| Dedikeret hardwarestation | Hardwarestationens forretningslogik, der er indbygget i Modern POS til Windows- og Modern POS til Android-programmer. |
| d/k-port (drawer kick) | En traditionel metode for tilslutning af en pengeskuffe til en kvitteringsprinter. |
| Eksterne netværksenheder | Indbygget understøttelse af netværksaktiverede betalingsterminaler, kvitteringsprintere og pengeskuffer. |

## <a name="supported-pos-clients-and-devices"></a>Understøttede POS-klienter og enheder

Den funktionalitet, der beskrives i dette emne, understøttes af Modern POS til Windows- og Modern PSO til Android-POS-klienterne.

Denne funktionalitet understøtter netværksaktiverede betalingsterminaler og kvitteringsprintere. Du kan understøtte pengeskuffen ved at slutte den til den netværksaktiverede kvitteringsprinter via d/k-porten.

Out-of-box-understøttelse af denne funktion findes i [Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3). Andre betalingsforbindelser kan dog understøttes via SDK (Commerce Software Development Kit) til betalinger. Understøttede kvitteringsprintere omfatter netværksaktiverede kvitteringsprintere fra Star Micronics og Epson.

Hvis du vil konfigurere Star Micronics-kvitteringsprintere, skal du bruge Star Micronics Printer Utility til at konfigurere enheden, så den kan bruges over netværket. Dette hjælpeværktøj angiver også enhedens IP-adresse.

Hvis du vil konfigurere Epson-kvitteringsprintere, skal du bruge Epson ePOS-Print-værktøjet til at konfigurere enheden, så den kan bruge netværksprotokoller.

Du kan finde flere oplysninger om, hvordan du konfigurerer eksterne netværksenheder, i [Oversigt over understøttelse af eksterne netværksenheder](https://go.microsoft.com/fwlink/?linkid=2129965).

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a>Konfigurere en dedikeret betalingsterminal og anmodning om en printer og kasseskuffe

### <a name="set-up-hardware-profiles"></a>Opsætning af hardwareprofiler

Du skal have to typer hardwareprofil. Den første tildeles kasseapparatet. Den anden tildeles en hardwarestation på butiksniveau og bruges til logisk at gruppere netværkskvitteringsprintere og -pengeskuffer.

#### <a name="set-up-a-hardware-profile-for-the-register"></a>Konfigurere en hardwareprofil til kasseapparatet

Udfør følgende trin for at konfigurere den hardwareprofil, der er tildelt kasseapparatet.

1. I Dynamics 365 Commerce skal du søge efter **Hardwareprofil**.
2. Vælg **Ny**.
3. Tildel et hardwareprofilnummer, og indtast derefter en beskrivelse. Denne hardwareprofil vil blive knyttet til selve kasseapparatet. Derfor er en beskrivelse, f.eks. **Dedikeret med fallback**, tilstrækkelig.
4. Konfigurer følgende enhedstyper i oversigtspanelerne for de forskellige enhedstyper.

    | Enhed | Type | Enhedens navn | Flere oplysninger |
    |---|---|---|---|
    | Printer | Reserve | *Alle* | Der skelnes mellem store og små bogstaver i enhedsnavnet. **Id'et for kvitteringsprofilen** skal være det samme som det **Kvitteringsprofil-id**, som er knyttet til den netværksprinter, der er konfigureret i den hardwareprofil, der er tildelt hardwarestationen på kanalniveau. |
    | Pengeskuffe | Reserve | *Alle* | Der skelnes mellem store og små bogstaver i enhedsnavnet. Angiv indstillingen **Brug af delt skift** til **Ja**. |
    | Autorisationskodetjeneste | Adyen | Ikke relevant | Du kan finde oplysninger om, hvordan du konfigurerer out-of-box Adyen-betalingsconnectoren i [Dynamics 365-betalingsconnector til Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3). Andre betalingsconnectorer kan understøttes via [Commerce Software Development Kit (SDK) til betalinger](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/end-to-end-payment-extension). |
    | Pinkodetastatur | Netværk | **MicrosoftAdyenDeviceV001** | Ingen. |

5. I Dynamics 365 Commerce skal du søge efter **Kasseapparater**.
6. Vælg et kasseapparat ved at vælge kassenummeret og derefter **Rediger**.
7. Tildel den hardwareprofil, du netop har oprettet, til det kasseapparat, der skal bruge en dedikeret betalingsterminal. Den enhed, der er knyttet til dette kasseapparat, skal enten bruge Modern POS til Windows-programmet eller Modern POS til Android-programmet.
8. Vælg **Gem**.
9. I handlingsruden skal du på fanen **Kasseapparater** vælge **Konfigurer IP-adresser**.
10. I oversigtspanelet **Pinkodetastatur** skal du angive IP-adressen for betalingsterminalen. Yderligere oplysninger om, hvordan du får IP-adressen på betalingsterminalen ved hjælp af Adyen-forbindelsen, finder du i [Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3).
11. Vælg **Gem**.

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a>Konfigurere en hardwareprofil for kvitteringsprinteren og kasseskuffen

Hvis du vil konfigurere den hardwareprofil, der bruges til at gruppere netværkskvitteringsprinteren og -kasseskuffen, skal du følge disse trin.

1. I Dynamics 365 Commerce skal du søge efter **Hardwareprofil**.
2. Vælg **Ny**.
3. Tildel et hardwareprofilnummer, og indtast derefter en beskrivelse. Denne hardwareprofil vil blive brugt til at gruppere kvitteringsprinteren og kasseskuffen. Derfor er en beskrivelse, f.eks. **Netværksprinter og kasseskuffe**, tilstrækkelig.
4. Konfigurer følgende enhedstyper i oversigtspanelerne for de forskellige enhedstyper.

    | Enhed | Type | Beskrivende tekst | Flere oplysninger |
    |---|---|---|---|
    | Printer | Netværk | **Epson** eller **Star** | Der skelnes mellem store og små bogstaver i enhedsnavnet. **Id'et for kvitteringsprofilen** skal være det samme som det **Kvitteringsprofil-id**, der er knyttet til den printer, der er konfigureret i den hardwareprofil, der er tildelt kasseapparatet. |
    | Pengeskuffe | Netværk | **Epson** eller **Star** | Der skelnes mellem store og små bogstaver i enhedsnavnet. angiv indstillingen **Brug af delt skift** til **Ja**. |

5. Vælg **Gem**.

### <a name="set-up-hardware-stations"></a>Oprette hardwarestationer

Du skal have to hardwarestationer. Den første bliver knyttet til kasseapparatet. Den anden vælges, som det kræves, når der skal udskrives en kvittering, eller der skal åbnes en kasseskuffe.

#### <a name="register-a-hardware-station"></a>Registrere en hardwarestation

1. I Dynamics 365 Commerce skal du søge efter **Alle butikker**.
2. Vælg en butik ved at vælge dens **Detailkanal-id** og derefter **Rediger**.
3. Vælg **Tilføj** i oversigtspanelet **Hardwarestationer**.
4. Angiv feltet **Hardwarestationstype** til **Dedikeret**.
5. Angiv en beskrivelse, men undlad at angive andre værdier for denne hardwarestation. Denne hardwarestation bruges hele tiden til kasseapparatet. 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a>Konfigurere en hardwarestation til kvitteringsprinteren og kasseskuffen

1. I Dynamics 365 Commerce skal du søge efter **Alle butikker**.
2. Vælg en butik ved at vælge dens **Detailkanal-id** og derefter **Rediger**.
3. Vælg **Tilføj** i oversigtspanelet **Hardwarestationer**.
4. Angiv feltet **Hardwarestationstype** til **Dedikeret**.
5. Angiv en beskrivelse. Denne hardwarestation vil blive brugt til kvitteringsprinteren og kasseskuffen.
6. I feltet **Hardwareprofil** skal du vælge den hardwareprofil, du tidligere har oprettet til kvitteringsprinteren og kasseskuffen.
7. Vælg **Gem**.
8. Mens hardwarestationen til kvitteringsprinteren og kasseskuffen stadigvæk er valgt, skal du vælge **Konfigurer IP-adresser**.
9. Få printerens IP-adresse, og angiv den som IP-adressen for både kvitteringsprinteren og pengeskuffen.
10. Vælg **Gem**
11. Søg efter **Distributionsplaner**.
12. Vælg distributionsplan **1090** og derefter **Kør nu**.
13. Vælg distributionsplan **1070** og derefter **Kør nu**.

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a>Konfigurer systemet til at anmode om kvitteringsprinter og kasseskuffe efter behov

1. Luk det aktuelle skift i en understøttet POS-klient, hvis et skift er åbent.
2. Log på, og vælg derefter **Skuffehandlinger uden for pengeskuffe**.
3. Brug handlingen **Administrer hardwarestationer** til at aktivere en hardwarestation.
4. Vælg den hardwarestation, du har oprettet til kasseapparatet, for at gøre den aktiv.
5. Log af POS, log derefter på igen og åbn et skift.

Den betalingsterminal, der er tildelt hardwareprofilen, vil nu altid være aktiv, og du vil blive spurgt, om der kræves en kvitteringsprinter eller kasseskuffe.

Mange handlende, der har anmodet om denne funktion, er interesseret i at få mindre affald ved at sende e-mailkvitteringer og opfordre til elektronisk betalinger. Afhængigt af POS-konfigurationen bliver butiksmedarbejderne bedt om kun at vælge en kvitteringsprinter eller en kasseskuffe, når en kunde ønsker en fysisk kvittering eller at betale med kontanter.

Butiksmedarbejderne bliver bedt om kun at vælge en hardwarestation én gang pr. transaktion, medmindre der skal udskrives en kvittering, og der betales med kontanter, men den hardwareprofil, der oprindeligt blev valgt, omfatter ikke begge enheder. I dette tilfælde vil butiksmedarbejderen blive bedt om at vælge en hardwarestation, der kan bruges til at gennemføre transaktionen.

## <a name="related-articles"></a>Relaterede artikler

- [Konfigurere POS Hybrid-appen på Android og iOS](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp)
- [Dynamics 365-betalingsconnector til Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)
- [Oversigt over understøttelse af eksterne netværksenheder](https://go.microsoft.com/fwlink/?linkid=2129965)


[!INCLUDE[footer-include](../includes/footer-banner.md)]