---
title: Konfigurere BOPIS i et Dynamics 365 Commerce-sandkassemiljø
description: Denne artikel forklarer, hvordan du konfigurerer køb online, afhent i butikken (BOPIS) i et Microsoft Dynamics 365 Commerce-sandkassemiljø, efter at det er blevet klargjort.
author: BrianShook
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 16cea7beb6ca05b5e96a9713b1217b414e27d56e
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013156"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-sandbox-environment"></a>Konfigurere BOPIS i et Dynamics 365 Commerce-sandkassemiljø

[!include [banner](includes/banner.md)]

Denne artikel forklarer, hvordan du konfigurerer køb online, afhent i butikken (BOPIS) i et Microsoft Dynamics 365 Commerce-sandkassemiljø, efter at miljøet er blevet klargjort.

## <a name="prerequisite"></a>Forudsætning

Fuldfør kun procedurerne i denne artikel, efter dit Commerce-sandkassemiljø er klargjort og konfigureret. Oplysninger om, hvordan du klargør og konfigurerer dit miljø, finder du under [Klargøre et Dynamics 365 Commerce-sandkassemiljø](provisioning-guide.md) og [Konfigurere et Dynamics 365 Commerce-sandkassemiljø](./cpe-post-provisioning.md).

Når Commerce-miljøet er blevet klargjort og konfigureret fra ende til anden, kan du bruge denne artikel til at aktivere BOPIS-scenarier.

## <a name="configure-the-pos"></a>Konfigurere POS

### <a name="configure-modern-pos"></a>Konfigurere Modern POS

BOPIS-scenarier, der involverer en kreditkortbetaling, kræver en hardwarestation. Hardwarestationen er indbygget i Modern POS til Windows og Android-klienter. Hvis du bruger Cloud POS eller Modern POS til iOS, skal POS-klienten kombineres med en delt hardwarestation. Denne artikel forklarer, hvordan du kan konfigurere BOPIS til Windows- og Android-klienter. Du kan finde oplysninger om, hvordan du konfigurerer en delt hardwarestationen, under [Konfigurere og installere Retail-hardwarestation](./retail-hardware-station-configuration-installation.md).

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> Kasseapparater**.
2. Vælg kasseapparatet **SANFRAN-5**, og vælg derefter **Rediger**.
3. Rediger værdien i feltet **Hardwareprofil** fra **HW002** til **HW001**, og vælg derefter **Gem**.
4. Gå til **Retail og Commerce \> Retail og CommerceIT \> Distributionsplan** for at synkronisere ændringerne.
5. Vælg distributionsplanen **1090**, og vælg derefter **Kør nu** i handlingsruden.
6. Vælg **Ja** og derefter **OK** for at starte datasynkroniseringen. 

### <a name="install-modern-pos"></a>Installere Modern POS

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> Enheder**.
2. Vælg enheden **SANFRANCIS-5**.
3. I handlingsruden skal du vælge **Download** og derefter vælge **Konfigurationsfil**.
4. Vælg **Download**, og vælg derefter **Retail Modern POS**. 
5. Når overførslen af filen **ModernPOSSetup.exe** er fuldført, skal du vælge **Åbn fil**.

    ![Åbn fil.](./dev-itpro/media/PAYMENTS/openfile.png)

6. Vælg **Næste** for at gennemgå installationsprocessen. Vælg **Luk**, når installationen er fuldført.

### <a name="activate-modern-pos"></a>Aktivere Modern POS

1. Vælg knappen **Start** på skrivebordet i Windows, og angiv **Retail Modern POS**.
2. Vælg **Retail Modern POS**-programmet for at starte aktivering.
3. Vælg **Næste**. Felterne **Serverens URL-adresse**, **Enheds-id** og **Kassenummer** skal forudindstilles ved hjælp af oplysningerne fra den konfigurationsfil, du har downloadet i den foregående procedure.
4. Vælg **Aktivér**.
5. Der vises en godkendelsesdialogboks. Vælg den konto, der bruger den mailadresse, der tidligere er knyttet til arbejderen **000713 - Andrew Collette**.

    > [!NOTE]
    > Hvis du endnu ikke har knyttet en arbejder til din identitet, lykkes aktiveringen ikke. I dette tilfælde skal du følge trinnene i afsnittet "Knytte en arbejder til din identitet" under artiklen [Konfigurere et Dynamics 365 Commerce-sandkassemiljø](cpe-post-provisioning.md#associate-a-worker-with-your-identity).
    
6. Når du bliver bedt om at lade din organisation administrere enheden, skal du vælge **Kun denne app**.
7. Vælg **Kom i gang**, når aktiveringen er fuldført.

### <a name="enable-bopis-in-modern-pos"></a>Aktivere BOPIS i Modern POS

1. Log på Modern POS med **000713** som operatør-id og **123** som adgangskode.
2. Mens videoen med gennemgang af introduktion afspilles, skal du markere de to afkrydsningsfelter i nederste venstre hjørne af dialogboksen og derefter lukke dialogboksen.
3. Hvis du ikke bliver bedt om at lukke skiftet, skal du rulle til højre på **velkomstsiden**, vælge **Luk skifte** og derefter logge på POS igen.
4. Når du er logget på, skal du vælge **Udfør handling uden om kasseskuffe**, når du bliver bedt om det.
5. Rul til højre på **velkomstsiden**, og vælg handlingen **Vælg hardwarestation**.
6. Vælg **Administrer**, angiv indstillingen **Brug hardwarestation** til **Slået til**, og vælg derefter **OK**.
7. Log af POS, og log derefter på igen.
8. Når du er logget på, skal du vælge **Åbn et nyt skifte** og derefter vælge **Kasseskuffe**.

## <a name="complete-a-bopis-scenario"></a>Fuldføre et BOPIS-scenarie

### <a name="create-a-storefront-order-for-in-store-pickup"></a>Oprette en butiksordre til afhentning i butikken

1. Gå til den URL-adresse, du har angivet i afsnittet [Initialisere e-handel](./provisioning-guide.md#initialize-e-commerce) under konfigurationen af miljøet.
2. Vælg en vare, og vælg **Føj til indkøbsvogn**.
3. Vælg **Afhent** for den ordrelinje, du lige har tilføjet, på siden med indkøbsposen.
4. Skriv **San Francisco** i dialogboksen **Vælg en butik**, og vælg derefter knappen **Søg**.
5. Find San Francisco-butikken på listen med resultater, og vælg **Afhent her**.
6. Vælg **Betal som gæst** på siden med indkøbsposen. 

    > [!NOTE]
    > Hvis du vil fortsætte med betaling, skal du acceptere cookie-beskeden. Denne meddelelse vises som et banner øverst på betalingssiden.

7. Angiv følgende oplysninger for kreditkortets betalingsmetode:

    - **Kortindehaverens navn:** Angiv et navn.
    - **Kortnummer:** Angiv **4111-1111-1111-1111**.
    - **Udløbsdato:** Angiv **20-10**.
    - **Værdi for kontrolnummer på kreditkort (CVV):** Angiv **737**.

    > [!IMPORTANT]
    > Forsøg aldrig under nogen omstændigheder at bruge faktiske kreditkortoplysninger på testwebstedet.

8. Fortsæt med betaling ved at angive detaljer om faktureringsadressen, og vælg derefter **Gem og fortsæt**.
9. Vælg **Betaling ved kassen**, når ordren er klar til at blive afgivet.

### <a name="synchronize-online-orders-to-the-back-office"></a>Synkronisere onlineordrer til administrationen

Du kan finde oplysninger om, hvordan du synkroniserer onlineordrer, under [Bogføre onlinesalg og -betalinger](./tasks/posting-online-sales-payments.md).

### <a name="pick-up-an-order-in-the-store"></a>Afhente en ordre i butikken

1. Log på POS'et.
2. På **velkomstsiden** skal du vælge **Ordreopfyldning**
3. Vælg linjen fra den ordre, der blev afgivet online, på listen over varer til afhentning.
4. Når ordrelinjen er valgt, skal du vælge **Afhent**.

    Linjevaren føjes til transaktionsskærmbilledet, og **$0,00** vises som den skyldige saldo.

5. Vælg forfaldne saldo på **0,00**, eller vælg en betalingsmåde for at afslutte transaktionen.

## <a name="troubleshooting"></a>Fejlfinding

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>Onlineordrer, der hentes i POS, har en forfaldssaldo på nul.

Når der hentes en ordre for en butiksafhentning, og den forfaldne saldo ikke er 0 (nul), skal du sørge for, at Modern POS bruges, og at hardwarestationen er aktiv. Hvis der bruges Cloud POS eller Modern POS til iOS, skal du kontrollere, at en delt hardwarestation er aktiv. En form for aktiv hardwarestation kræves for at hente betalinger, der er foretaget online.

### <a name="general-issues-with-payment-capture"></a>Generelle problemer med betalingsregistrering

Ved alle generelle problemer skal du altid konsultere hændelseslogfilerne for hardwarestationen Modern POS eller Internet Information Services (IIS) som første trin. Du kan finde disse logfiler under følgende noder i hændelseslogfilen for Windows:

- Logfiler for programmer og tjenester \> Microsoft \> Dynamics \> Commerce-ModernPOS
- Logfiler for programmer og tjenester \> Microsoft \> Dynamics \> Commerce-Hardware Station

## <a name="additional-resources"></a>Yderligere ressourcer

[Klargøre et Dynamics 365 Commerce-sandkassemiljø](provisioning-guide.md)

[Konfigurere valgfrie funktioner for et Dynamics 365 Commerce-sandkassemiljø](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-websted](https://aka.ms/Dynamics365CommerceWebsite)

[Adyen-betalingsconnector](./dev-itpro/adyen-connector.md?tabs=8-1-3)

[Gemme onlinebetalingsmidler med Adyen-connector](./dev-itpro/adyen-connector-listpi.md)

[Oversigt over omni-kanalbetalinger](./omni-channel-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
