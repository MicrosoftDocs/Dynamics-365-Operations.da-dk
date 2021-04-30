---
title: Installere og tilslutte mobilappen Lokationsstyring
description: Dette emne forklarer, hvordan du installerer mobilappen Lokationsstyring og konfigurerer den til at oprette forbindelse til dit Microsoft Dynamics 365 Supply Chain Management-miljø.
author: MarkusFogelberg
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f46c5d4ec78a1e5ed708687e8da6eb379697d5f4
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908946"
---
# <a name="install-and-connect-the-warehouse-management-mobile-app"></a>Installere og tilslutte mobilappen Lokationsstyring

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Dette emne beskriver, hvordan du konfigurerer den nye mobilapp Lokationsstyring. Hvis du søger efter oplysninger om, hvordan du konfigurerer den gamle lagerstedsapp (nu frarådet), skal du se [Installere og tilslutte lagerstedsappen](../../supply-chain/warehousing/install-configure-warehousing-app.md).

Dette emne forklarer, hvordan du downloader og installerer mobilappen Lokationsstyring på dine mobilenheder og konfigurerer den til at oprette forbindelse til dit Supply Chain Management-miljø. Du kan konfigurere hver enkelt enhed manuelt, eller du kan importere forbindelsesindstillinger gennem en fil eller ved at scanne en QR-kode.

## <a name="system-requirements"></a>Systemkrav

mobilappen Lokationsstyring er tilgængelig på både Windows- og Google Android-operativsystemer. Når du vil bruge appen, skal du have et af følgende understøttede operativsystemer installeret på dine mobilenheder:

- Windows 10 (Universal Windows Platform \[UWP\]) October 2018 Update 1809 (build 10.0.17763) eller senere
- Android 4.4 eller senere

## <a name="turn-on-the-feature"></a>Slå funktionen til

Før du kan bruge appen, skal en relateret funktion være slået til i dit system. Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Brugerindstillinger, ikoner og trintitler til den nye lagerstedsapp*

## <a name="get-the-warehouse-management-mobile-app"></a>Hent mobilappen Lokationsstyring

Ved mindre udrulninger vil du måske installere appen fra den relevante store på hver enkelt enhed og derefter konfigurere forbindelsen til de miljøer, du bruger, manuelt.

Til større udrulning kan du automatisere udrulning og/eller konfiguration af appen, hvilket kan være mere praktisk, hvis du administrerer mange enheder. Du kan f.eks. bruge en løsning til administration af mobilenheder og administration af mobilapps som f.eks. [Microsoft Intune](/mem/intune/fundamentals/what-is-intune). Du kan få oplysninger om, hvordan du bruger Intune til at tilføje applikationer, i [Tilføj apps til Microsoft Intune](/mem/intune/apps/apps-add).

### <a name="install-the-app-from-an-app-store"></a>Installere appen fra en appbutik

Det er lettest at installere appen på en enkelt enhed ved at installere den fra en appbutik, som altid har den nyeste og mest tilgængelige version. Microsoft Intune kan også hente apps fra appbutikkerne. Brug et af følgende links til at installere appen fra en appbutik:

- **Windows (UWP):** [Lokationsstyring på Microsoft Store](https://www.microsoft.com/store/apps/9pd35cdqcmg3)

- **Android:** [Lokationsstyring på Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)

### <a name="download-the-app-from-microsoft-app-center"></a>Downloade appen fra Microsoft App Center

Som et alternativ til at installere fra en appbutik kan du i stedet hente appen fra Microsoft App Center. App Center indeholder installerbare pakker, som du kan indlæse. Ud over den aktuelle version giver App Center dig også mulighed for at hente tidligere versioner og eventuelt forhåndsversioner med kommende funktioner, som du kan prøve af. Hvis du vil hente aktuelle, tidligere eller forhåndsversioner af mobilappen Lokationsstyring fra Microsoft App Center, skal du bruge følgende links:

- **Windows (UWP):** [Lokationsstyring (Windows)](https://go.microsoft.com/fwlink/?linkid=2154406)  
    Du kan finde oplysninger om, hvordan du installerer en hentet pakke på en Windows-enhed og derefter konfigurerer de nødvendige certifikater, under [Installere en build fra App Center](/appcenter/distribution/installation).

- **Android:** [Lokationsstyring (Android)](https://go.microsoft.com/fwlink/?linkid=2154613)  
    Hvis du henter en forhåndsversion, skal du følge nogle få ekstra trin for at installere den. Yderligere oplysninger finder du i [Teste Android-apps](/appcenter/distribution/testers/testing-android).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Oprette en webtjenesteapplikation i Azure Active Directory

For at aktivere mobilappen Lokationsstyring til at kommunikere med en bestemt Supply Chain Management-server skal du registrere en webtjenesteapplikation til Supply Chain Management-lejeren i Azure Active Directory (Azure AD). Følgende procedurer viser en måde at fuldføre denne opgave på. Få detaljerede oplysninger og alternativer ved at se linkene, når proceduren er udført.

1. Åbn en webbrowser, og gå til [https://portal.azure.com](https://portal.azure.com/).
1. Angiv brugernavnet og adgangskoden for den bruger, der har adgang til Azure-abonnementet.
1. Vælg **Azure Active Directory** i venstre navigationsrude på Azure-portalen.

    ![Azure Active Directory](media/app-connect-azure-aad.png "Azure Active Directory")

1. Kontrollér, at du arbejder med den forekomst af Azure AD, der bruges af Supply Chain Management.
1. Vælg **Appregistreringer** på listen **Administrer**.

    ![Appregistreringer](media/app-connect-azure-register.png "Appregistreringer")

1. På værktøjslinjen skal du vælge **Ny registrering** for at åbne guiden **Registrer et program**.
1. Angiv et navn til applikationen, og vælg indstillingen **Kun konti i denne organisations bibliotek**, og vælg derefter **Registrer**.

    ![Registrer en applikationsguide](media/app-connect-azure-register-wizard.png "Registrere en applikationsguide.").

1. Den nye appregistrering åbnes. Notér værdien i feltet **Applikations-id (klient)**, da du skal bruge den senere. Dette id henvises til senere i dette emne som *klient-id'et*.

    ![Program-id (klient)](media/app-connect-azure-app-id.png "Program-id (klient)")

1. Gå til listen **Administrer**, og vælg **Certifikat og hemmeligheder**. Vælg derefter en af følgende knapper, afhængigt af hvordan du vil konfigurere appen til godkendelse. (Få flere oplysninger i afsnittet [Godkende ved at bruge et certifikat eller klienthemmelighed](#authenticate) senere i dette emne.)

    - **Upload certifikat** – upload et certifikat, der skal bruges som en hemmelighed. Vi anbefaler denne fremgangsmåde, fordi den er mere sikker og også kan automatiseres mere fuldstændigt. Hvis du kører mobilappen Lokationsstyring på Windows-enheder, skal du notere dig, hvilken **aftryksværdi** der vises, når du har uploadet certifikatet. Du skal bruge denne værdi, når du konfigurerer certifikatet på Windows-enheder.
    - **Ny klienthemmelighed** – opret en nøgle ved at angive en nøglebeskrivelse og en varighed i sektionen **Adgangskoder**, og vælg derefter **Tilføj**. Tag en kopi af nøglen, og opbevar den sikkert.

    ![Certifikat og hemmeligheder](media/app-connect-azure-authentication.png "Certifikat og hemmeligheder")

Få flere oplysninger om, hvordan du konfigurerer webtjenesteapplikationer i Azure AD, i følgende ressourcer:

- Du kan finde instruktioner, der viser, hvordan du bruger Windows PowerShell til at konfigurere webtjenesteapplikationer i Azure AD, i [Sådan bruger du Azure PowerShell til at oprette en tjenesteprincipal med et certifikat](/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Få flere oplysninger om, hvordan du opretter en webtjenesteapplikation manuelt i Azure AD, i følgende emner:

    - [Hurtig start: Registrer et program med platformen Microsoft-identitet](/azure/active-directory/develop/quickstart-register-app)
    - [Sådan bruges portalen til at oprette en Azure AD-applikation og tjenesteportal, der kan få adgang til ressourcer](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Opret og konfigurer en brugerkonto i Supply Chain Management

Benyt følgende fremgangsmåde, hvis du vil give mulighed for, at Supply Chain Management kan bruge din Azure AD-applikation.

1. Opret en bruger, der svarer til brugerlegitimationsoplysningerne til mobilappen Lokationsstyring:

    1. I Supply Chain Management skal du gå til **Systemadministration \> Brugere \> Brugere**.
    1. Opret en bruger.
    1. Tildele brugeren af lagerstedsmobilenheden.

    ![Tildele brugeren af lagerstedsmobilenheden](media/app-connect-app-users.png "Tildele brugeren af lagerstedsmobilenheden")

1. Knyt din Azure AD-applikation til brugeren af mobilappen Lokationsstyring:

    1. Gå til **SSystemadministration \> Opsætning \> Azure Active Directory-applikationer**.
    1. Oprette en linje.
    1. Angiv det klient-id, du har noteret i forrige afsnit, giv det et navn, og vælg den bruger, du netop har oprettet. Det anbefales, at du mærker alle dine enheder. Hvis en enhed derefter går tabt, kan du så nemt fjerne adgangen til Supply Chain Management fra denne side.

    ![Azure Active Directory-applikationer](media/app-connect-aad-apps.png "Azure Active Directory-applikationer")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Godkende ved hjælp af et certifikat eller en klienthemmelighed

Godkendelse med Azure AD giver en sikker metode til at forbinde en mobilenhed med Supply Chain Management. Du kan godkende enten ved at bruge en klienthemmelighed eller et certifikat. Hvis du vil importere forbindelsesindstillinger, anbefales det, at du bruger et certifikat i stedet for en klienthemmelighed. Da klienthemmeligheden altid skal lagres på en sikker måde, kan du ikke importere den fra en fil med forbindelsesindstillinger eller en QR-kode, som beskrevet senere i dette emne.

Certifikater kan bruges som hemmeligheder for at bevise applikationens identitet, når der anmodes om et token. Den offentlige del af certifikatet overføres til appregistreringen på Azure-portalen, hvorimod hele certifikatet skal installeres på hver enkelt enhed, hvor mobilappen Lokationsstyring er installeret. Din organisation er ansvarlig for at administrere certifikatet i form af rotation osv. Du kan bruge selvsignerede certifikater, men du bør altid bruge certifikater, der ikke kan eksporteres.

Du skal gøre certifikatet lokalt tilgængeligt på hver enhed, hvor du kører mobilappen Lokationsstyring. Du kan finde oplysninger om, hvordan du administrerer certifikater til Intune-styrede enheder, hvis du bruger Intune, under [Bruge certifikater til godkendelse i Microsoft Intune](/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Konfigurere applikationen ved at importere forbindelsesindstillinger

Hvis du vil gøre det nemmere at vedligeholde og implementere applikationen på mange mobilenheder, kan du importere forbindelsesindstillingerne i stedet for at angive dem manuelt på hver enhed. Dette afsnit forklarer, hvordan du kan oprette og importere indstillingerne.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Oprette en fil med forbindelsesindstillinger eller QR-kode

Du kan importere forbindelsesindstillinger fra enten en fil eller en QR-kode. Ved begge fremgangsmåder gælder det, at du først skal oprette en indstillingsfil, der bruger JSON-format og -syntaks (JavaScript Object Notation). Filen skal indeholde en forbindelsesliste, der indeholder de enkelte forbindelser, der skal tilføjes. I følgende tabel opsummeres de parametre, du skal angive i filen med forbindelsesindstillinger.

| Parameter | Beskrivende tekst |
|---|---|
| ConnectionName | Angiv navnet på forbindelsesindstillingen. Beskrivelsen må højst være på 20 tegn. Da denne værdi er et entydigt id for en forbindelsesindstilling, skal du sørge for, at den er entydig på listen. Hvis der allerede findes en forbindelse med samme navn på enheden, vil den blive tilsidesat af indstillingerne fra den importerede fil. |
| ActiveDirectoryClientAppId | Angiv det klient-id, du har noteret, mens du var i opsætningen af Azure AD i afsnittet [Oprette en webtjenesteapplikation i Azure Active Directory](#create-service). |
| ActiveDirectoryResource | Angiv rod-URL-adressen for Supply Chain Management. |
| ActiveDirectoryTenant | Angiv den Azure AD-lejer, som du bruger sammen med Supply Chain Management-serveren. Denne værdi har formatet `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Her er et eksempel: `https://login.windows.net/contosooperations.onmicrosoft.com`. |
| Regnskab | Angiv den juridiske enhed i Supply Chain Management, som applikationen skal oprette forbindelse til. |
| ConnectionType | (Valgfri) Angiv, om forbindelsesindstillingen skal bruge et certifikat eller en klienthemmelighed til at oprette forbindelse til et miljø. De gyldige værdier er *"certificate"* og *"clientsecret"*. Standardværdien er *"certificate"*.<p>**Bemærk!** Klienthemmeligheder kan ikke importeres.</p> |
| IsEditable | (Valgfrit) Angiv, om appen skal kunne redigere forbindelsesindstillingen. Gyldige værdier er *"true"* og *"false"*. Standardværdien er *"true"*. |
| IsDefault | (Valgfrit) Angiv, om forbindelsen er standardforbindelsen. En forbindelse, der er angivet som standardforbindelse, vælges automatisk på forhånd, når appen åbnes. Kun én forbindelse kan angives som standardforbindelsen. Gyldige værdier er *"true"* og *"false"*. Standardværdien er *"false"*. |
| CertificateThumbprint | (Valgfrit) I forbindelse med Windows-enheder kan du angive certifikataftrykket for forbindelsen. For Android-enheder kan app-brugeren vælge certifikatet, første gang en forbindelse bruges. |

I følgende eksempel vises en gyldig fil med indstillinger for forbindelser, der indeholder to forbindelser. Som du kan se, er forbindelseslisten (kaldet *"ConnectionList"* i filen) et objekt, der indeholder en matrix, der gemmer hver enkelt forbindelse som et objekt. Hvert objekt skal stå i klammeparenteser ({}) og være adskilt af kommaer, og matrixen skal være omsluttet af kantede parenteser (\[\]).

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

Du kan enten gemme oplysningerne som en JSON-fil eller generere en QR-kode med det samme indhold. Hvis du gemmer oplysningerne som en fil, anbefales det, at du gemmer den ved hjælp af standardnavnet, *connections.json*, især hvis du vil gemme den på standardplaceringen på de enkelte mobilenheder.

### <a name="save-the-connection-settings-file-on-each-device"></a>Gem filen med forbindelsesindstillinger på hver enkelt enhed

Du vil typisk bruge et værktøj til enhedshåndtering eller script til at distribuere filerne med forbindelsesindstillinger til hver af de enheder, du administrerer. Hvis du bruger standardnavnet og -placeringen, når du gemmer filen med forbindelsesindstillinger på hver enkelt enhed, importerer mobilappen Lokationsstyring den automatisk, selv når den køres første gang, efter at appen er installeret. Hvis du bruger et brugerdefineret navn eller en brugerdefineret placering til filen, skal app-brugeren angive værdierne under den første kørsel. Appen vil dog fortsat bruge det angivne navn og den specificerede placering bagefter.

Hver gang appen startes, genindlæser den forbindelsesindstillingerne fra den tidligere placering for at finde ud af, om der er foretaget ændringer. Appen opdaterer kun forbindelser, der har samme navn som forbindelserne i filen med forbindelsesindstillinger. Brugeroprettede forbindelser, der bruger andre navne, opdateres ikke.

Du kan ikke fjerne en forbindelse ved hjælp af filen med forbindelsesindstillinger.

Som nævnt tidligere er standardfilnavnet *connections.json*. Standardplaceringen for filer afhænger af, om du bruger en Windows-enhed eller en Android-enhed:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.WarehouseManagement\files`

Stierne oprettes som regel automatisk efter den første kørsel af appen. Du kan dog oprette dem manuelt, hvis du skal overføre filen med forbindelsesindstillinger til enheden, før du installerer.

> [!NOTE]
> Hvis appen fjernes, fjernes standardstien og dens indhold.

### <a name="import-the-connection-settings"></a>Importere forbindelsesindstillingerne

Benyt følgende fremgangsmåde til at importere forbindelsesindstillinger fra en fil eller en QR-kode.

1. Start mobilappen Lokationsstyring på din mobilenhed. Første gang du starter appen, vises en velkomstmeddelelse. Vælg **Vælg en forbindelse**.

    ![Velkomstmeddelelse](media/app-configure-welcome-screen.png "Velkomstmeddelelse")

1. Hvis du importerer forbindelsesindstillingerne fra en fil, og standardnavnet og -placeringen blev brugt, da filen blev gemt, har appen muligvis allerede fundet filen. I dette tilfælde skal du gå videre til trin 4. Ellers skal du vælge **Konfigurer forbindelse** og derefter fortsætte til trin 3.

    ![Konfigurer forbindelse](media/app-configure-set-up-connection.png "Konfigurer forbindelse")

1. I dialogboksen **Opsætning af forbindelse** skal du vælge **Tilføj fra fil** eller **Tilføj fra QR-kode**, afhængigt af hvordan du vil importere indstillingerne:

    - Hvis du importerer forbindelsesindstillingerne fra en fil, skal du vælge **Tilføj fra fil**, gennemse den lokale enhed for filen og vælge den. Hvis du vælger en brugerdefineret placering, gemmer appen den og bruger den automatisk næste gang.
    - Hvis du vil importere forbindelsesindstillingerne ved at scanne en QR-kode, skal du vælge **Tilføj fra QR-kode**. Appen beder dig om tilladelse til at bruge enhedens kamera. Når du har givet dig tilladelse, startes kameraet, så du kan bruge det til scanning. Afhængigt af kvaliteten af enhedens kamera og QR-kodens kompleksitet, kan det være vanskeligt at få en korrekt scanning. Hvis det er tilfældet, skal du forsøge at reducere QR-kodens kompleksitet ved kun at oprette én forbindelse pr. QR-kode. (I øjeblikket kan du kun bruge enhedens kamera til at scanne QR-koden).

    ![Menuen Forbindelsesopsætning](media/app-configure-connection-setup-flyout.png "Menuen Forbindelsesopsætning")

1. Når forbindelsesindstillingerne er indlæst, vises den valgte forbindelse.

    ![Forbindelsesindstillinger er indlæst](media/app-configure-select-connection.png "Forbindelsesindstillinger er indlæst")

1. Hvis du bruger en Android-enhed og bruger et certifikat til godkendelse, beder enheden dig om at vælge certifikatet.

    ![Vælg certifikatbeskeden på en Android-enhed](media/app-configure-select-certificate.png "Vælg certifikatbeskeden på en Android-enhed")

1. Appen opretter forbindelse til din Supply Chain Management-server og viser logonsiden.

    ![Logonside](media/app-configure-sign-in-page.png "Logonside")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Konfigurere applikationen manuelt

Hvis du ikke har en fil eller QR-kode, kan du konfigurere manuelt på enheden, så den opretter forbindelse til Supply Chain Management-serveren via Azure AD-applikationen.

1. Start mobilappen Lokationsstyring på din mobilenhed.
1. Hvis appen startes i **Demotilstand**, skal du vælge **Forbindelsesindstillinger**. Hvis siden **Log på** vises, når appen startes, skal du vælge **Skift forbindelse**.
1. Vælg **Konfigurer forbindelse**.

    ![Konfigurer forbindelse](media/app-configure-set-up-connection.png "Konfigurer forbindelse")

1. Vælg **Input manuelt**.

    ![Menuen Forbindelsesopsætning](media/app-configure-connection-setup-flyout.png "Menuen Forbindelsesopsætning")

    Siden **Ny forbindelse** vises med de indstillinger, der kræves for at angive forbindelsesoplysningerne manuelt.

    ![Manuelle forbindelsesfelter](media/app-configure-input-manually.png "Manuelle forbindelsesfelter")

1. Angiv følgende oplysninger:

    - **Brug klienthemmelighed** – angiv denne indstilling til _Ja_ for at bruge en klienthemmelighed til godkendelse med Supply Chain Management. Angiv den til _Nej_ for at bruge et certifikat til godkendelse. (Du kan finde flere oplysninger i [Oprette en webtjenesteapplikation i afsnittet Azure Active Directory](#create-service) tidligere i dette emne).
    - **Forbindelsesnavn** – angiv et navn til den nye forbindelse. Dette navn vises i feltet **Vælg forbindelse**, næste gang du åbner forbindelsesindstillingerne. Det navn, du angiver her, skal være entydigt. (Med andre ord skal det være forskelligt fra alle andre forbindelsesnavne, der er gemt på enheden, hvis der er gemt andre forbindelsesnavne dér).
    - **Active Directory-klient-id** – angiv det klient-id, du har noteret, mens du var i opsætningen af Azure AD i [Oprette en webtjenesteapplikation i afsnittet Azure Active Directory](#create-service).
    - **Active Directory-klienthemmelighed** – dette felt er kun tilgængeligt, hvis indstillingen **Brug klienthemmelig** er angivet til _Ja_. Angiv den klienthemmelighed, du har noteret, mens du var i opsætningen af Azure AD i afsnittet [Oprette en webtjenesteapplikation i Azure Active Directory](#create-service).
    - **Active Directory-certifikataftryk** – dette felt er kun tilgængeligt for Windows-enheder, og kun, når indstillingen **Brug klienthemmelig** er angivet til _Nej_. Angiv det certifikataftryk, du har noteret, mens du var i opsætningen af Azure AD i afsnittet [Oprette en webtjenesteapplikation i Azure Active Directory](#create-service).
    - **Active Directory-ressource** – angiv rod-URL-adressen for Supply Chain Management.

        > [!IMPORTANT]
        > Undlad at afslutte denne værdi med en skråstreg (/).

    - **Active Directory-lejer** – angiv den Azure AD-lejer, du bruger til Supply Chain Management-serveren. Denne værdi har formatet `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Her er et eksempel: `https://login.windows.net/contosooperations.onmicrosoft.com`.

        > [!IMPORTANT]
        > Undlad at afslutte denne værdi med en skråstreg (/).

    - **Firma** – angiv den juridiske enhed (virksomhed) i Supply Chain Management, som applikationen skal oprette forbindelse til.

1. Vælg knappen **Gem** i øverste højre hjørne af siden.
1. Hvis du bruger en Android-enhed og bruger et certifikat til godkendelse, beder enheden dig om at vælge certifikatet.
1. Appen opretter forbindelse til din Supply Chain Management-server og viser logonsiden.

## <a name="remove-access-for-a-device"></a>Fjerne adgang til en enhed

Hvis en enhed er mistet eller beskadiget, skal du fjerne adgangen til Supply Chain Management for den. De følgende trin beskriver den anbefalede proces til at fjerne adgangen.

1. Gå til **SSystemadministration \> Opsætning \> Azure Active Directory-applikationer**.
1. Slet den linje, der svarer til den enhed, du vil fjerne adgangen til. Notér det klient-id, der bruges til enheden, da du får brug for det senere.

    Hvis du kun har registreret ét klient-id, og flere enheder bruger samme klient-id, skal du pushe nye forbindelsesindstillinger til disse enheder. Ellers vil de miste adgang.

1. Log på Azure-portalen på [https://portal.azure.com](https://portal.azure.com/).
1. Vælg **Active Directory** i den venstre navigationsrude, og sørg for, at du er i den rigtige mappe.
1. På listen **Administrer** skal du vælge **Appregistreringer** og derefter vælge den applikation, du vil konfigurere. Siden **Indstillinger** vises og angiver konfigurationsoplysninger.
1. Kontroller, at klient-id'et for applikationen svarer til det klient-id, du har noteret dig i trin 2.
1. Vælg **Slet** på værktøjslinjen.
1. Vælg **Ja** i den bekræftelsesmeddelelsesboks, der vises.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]