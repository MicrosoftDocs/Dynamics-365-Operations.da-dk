---
title: Installere og tilslutte lagerstedsapp
description: Dette emne forklarer, hvordan du installerer lagerstedsappen på de mobile enheder og konfigurerer den til at oprette forbindelse til dit Microsoft Dynamics 365 Supply Chain Management-miljø. Du kan konfigurere hver enkelt enhed manuelt, eller du kan importere forbindelsesindstillinger gennem en fil eller ved at scanne en QR-kode.
author: MarkusFogelberg
ms.date: 05/25/2020
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
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: aeb9675477e728c28c38b1ef43fa6055acd23360
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909373"
---
# <a name="install-and-connect-the-warehouse-app"></a>Installere og tilslutte lagerstedsapp

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Dette emne beskriver, hvordan du konfigurerer den gamle lagerstedsapp (som nu er frarådet). Hvis du leder efter oplysninger om, hvordan du konfigurerer den nye mobilapp Lokationsstyring, skal du se [Installere og forbinde mobilappen Lokationsstyring](install-configure-warehouse-management-app.md).

> [!NOTE]
> Dette emne beskriver, hvordan du konfigurerer lagerstedsappen for skyinstallationer. Hvis du søger efter oplysninger om, hvordan du konfigurerer lagerstedsappen for installationer i det lokale miljø, skal du se [Lagersted for installationer i det lokale miljø](../../fin-ops-core/dev-itpro/deployment/warehousing-for-on-premise-deployments.md).

Lagerstedsappen er tilgængelig i Google Play Butik og Microsoft Store. Den udbydes som en enkeltstående komponent. Derfor skal du overføre den på hver enkelt enhed og derefter konfigurere den til at oprette forbindelse til dit Microsoft Dynamics 365 Supply Chain Management-miljø.

Dette emne forklarer, hvordan du installerer lagerstedsappen på de mobile enheder og konfigurerer den til at oprette forbindelse til dit Supply Chain Management-miljø. Du kan konfigurere hver enkelt enhed manuelt, eller du kan importere forbindelsesindstillinger gennem en fil eller ved at scanne en QR-kode.

## <a name="system-requirements"></a>Systemkrav

Lagerstedsappen er tilgængelig på både Windows- og Android-operativsystemer. Hvis du vil bruge den seneste version af appen, skal du have et af følgende understøttede operativsystemer installeret på dine mobilenheder:

- Windows 10 (Universal Windows Platform \[UWP\]) Fall Creators Update 1709 (build 10.0.16299) eller senere
- Android 4.4 eller senere

> [!NOTE]
> Hvis du skal understøtte ældre Windows-enheder, der ikke kan køre den nyeste version af Windows, kan du stadig hente version 1.6.3.0 af lagerstedsappen i Microsoft Store. Denne version kører på Windows 10 (UWP) November Update 1511 (build 10.0.10586) eller senere. Bemærk dog, at denne version af lagerstedsappen ikke understøtter masseimplementering af forbindelsesindstillinger. Du skal derfor [manuelt konfigurere forbindelsen](#config-manually) for de enkelte enheder, der kører denne version af appen.

## <a name="get-the-warehouse-app"></a>Hente lagerstedsappen

Brug et af følgende links til at hente appen:

- **Windows (UWP):** [Dynamics 365 for Finance and Operations – lager på Microsoft Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
- **Android:** [Warehousing - Dynamics 365 on Google Play Butik](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

Ved mindre installationer vil du måske installere appen fra den relevante store på hver enkelt enhed og derefter konfigurere forbindelsen til de miljøer, du bruger, manuelt. Men i version 1.7.0.0 og nyere af lagerstedsappen kan du også automatisere appimplementering og/eller -konfiguration. Det kan være en fordel at bruge denne fremgangsmåde, hvis du administrerer mange enheder, og du bruger en løsning til administration af mobilenheder og løsningen til styring af mobilapplikationer såsom [Microsoft Intune](/mem/intune/fundamentals/what-is-intune). Du kan få oplysninger om, hvordan du bruger Intune til at tilføje applikationer, i [Tilføj apps til Microsoft Intune](/mem/intune/apps/apps-add).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Oprette en webtjenesteapplikation i Azure Active Directory

For at aktivere lagerstedsappen til at kommunikere med en bestemt Supply Chain Management-server skal du registrere en webtjenesteapplikation til Supply Chain Management-lejeren i Azure Active Directory (Azure AD). Følgende procedurer viser en måde at fuldføre denne opgave på. Få detaljerede oplysninger og alternativer ved at se linkene, når proceduren er udført.

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

    - **Upload certifikat** – upload et certifikat, der skal bruges som en hemmelighed. Vi anbefaler denne fremgangsmåde, fordi den er mere sikker og også kan automatiseres mere fuldstændigt. Hvis du kører lagerstedsappen på Windows-enheder, skal du notere dig, hvilken **aftryksværdi** der vises, når du har uploadet certifikatet. Du skal bruge denne værdi, når du konfigurerer certifikatet på Windows-enheder.
    - **Ny klienthemmelighed** – opret en nøgle ved at angive en nøglebeskrivelse og en varighed i sektionen **Adgangskoder**, og vælg derefter **Tilføj**. Tag en kopi af nøglen, og opbevar den sikkert.

    ![Certifikat og hemmeligheder](media/app-connect-azure-authentication.png "Certifikat og hemmeligheder")

Få flere oplysninger om, hvordan du konfigurerer webtjenesteapplikationer i Azure AD, i følgende ressourcer:

- Du kan finde instruktioner, der viser, hvordan du bruger Windows PowerShell til at konfigurere webtjenesteapplikationer i Azure AD, i [Sådan bruger du Azure PowerShell til at oprette en tjenesteprincipal med et certifikat](/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Få flere oplysninger om, hvordan du opretter en webtjenesteapplikation manuelt i Azure AD, i følgende emner:

    - [Hurtig start: Registrer et program med platformen Microsoft-identitet](/azure/active-directory/develop/quickstart-register-app)
    - [Sådan bruges portalen til at oprette en Azure AD-applikation og tjenesteportal, der kan få adgang til ressourcer](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Opret og konfigurer en brugerkonto i Supply Chain Management

Benyt følgende fremgangsmåde, hvis du vil give mulighed for, at Supply Chain Management kan bruge din Azure AD-applikation.

1. Opret en bruger, der svarer til brugerlegitimationsoplysningerne til lagerstedsappen:

    1. I Supply Chain Management skal du gå til **Systemadministration \> Brugere \> Brugere**.
    1. Opret en bruger.
    1. Tildele brugeren af lagerstedsmobilenheden.

    ![Tildele brugeren af lagerstedsmobilenheden](media/app-connect-app-users.png "Tildele brugeren af lagerstedsmobilenheden")

1. Knyt din Azure AD-applikation til brugeren af lagerstedsappen:

    1. Gå til **SSystemadministration \> Opsætning \> Azure Active Directory-applikationer**.
    1. Oprette en linje.
    1. Angiv det klient-id, du har noteret i forrige afsnit, giv det et navn, og vælg den bruger, du netop har oprettet. Det anbefales, at du mærker alle dine enheder. Hvis de derefter går tabt, kan du så nemt fjerne deres adgang til Supply Chain Management fra denne side.

    ![Azure Active Directory-applikationer](media/app-connect-aad-apps.png "Azure Active Directory-applikationer")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Godkende ved hjælp af et certifikat eller en klienthemmelighed

Godkendelse med Azure AD giver en sikker metode til at forbinde en mobilenhed med Supply Chain Management. Du kan godkende enten ved at bruge en klienthemmelighed eller et certifikat. Hvis du vil importere forbindelsesindstillinger, anbefales det, at du bruger et certifikat i stedet for en klienthemmelighed. Da klienthemmeligheden altid skal lagres på en sikker måde, kan du ikke importere den fra en fil med forbindelsesindstillinger eller en QR-kode, som beskrevet senere i dette emne.

Certifikater kan bruges som hemmeligheder for at bevise applikationens identitet, når der anmodes om et token. Den offentlige del af certifikatet overføres til appregistreringen på Azure-portalen, hvorimod hele certifikatet skal installeres på hver enkelt enhed, hvor lagerstedsappen er installeret. Din organisation er ansvarlig for at administrere certifikatet i form af rotation osv. Du kan bruge selvsignerede certifikater, men du bør altid bruge certifikater, der ikke kan eksporteres.

Du skal gøre certifikatet lokalt tilgængeligt på hver enhed, hvor du kører lagerstedsappen. Du kan finde oplysninger om, hvordan du administrerer certifikater til Intune-styrede enheder, hvis du bruger Intune, under [Bruge certifikater til godkendelse i Microsoft Intune](/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Konfigurere applikationen ved at importere forbindelsesindstillinger

Hvis du vil gøre det nemmere at vedligeholde og implementere applikationen på mange mobilenheder, kan du importere forbindelsesindstillingerne i stedet for at angive dem manuelt på hver enhed. Dette afsnit forklarer, hvordan du kan oprette og importere indstillingerne.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Oprette en fil med forbindelsesindstillinger eller QR-kode

Du kan importere forbindelsesindstillinger fra enten en fil eller en QR-kode. Ved begge fremgangsmåder gælder det, at du først skal oprette en indstillingsfil, der bruger JSON-format og -syntaks (JavaScript Object Notation). Filen skal indeholde en forbindelsesliste, der indeholder de enkelte forbindelser, der skal tilføjes. I følgende tabel opsummeres de parametre, du skal angive i filen med forbindelsesindstillinger.

| Parameter | Beskrivende tekst |
| --- | --- |
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

Du vil typisk bruge et værktøj til enhedshåndtering eller script til at distribuere filerne med forbindelsesindstillinger til hver af de enheder, du administrerer. Hvis du bruger standardnavnet og -placeringen, når du gemmer filen med forbindelsesindstillinger på hver enkelt enhed, importeres den pågældende app automatisk, selv når den køres første gang, efter at appen er installeret. Hvis du bruger et brugerdefineret navn eller en brugerdefineret placering til filen, skal app-brugeren angive værdierne under den første kørsel. Appen vil dog fortsat bruge det angivne navn og den specificerede placering bagefter.

Hver gang appen startes, genindlæser den forbindelsesindstillingerne fra den tidligere placering for at finde ud af, om der er foretaget ændringer. Appen opdaterer kun forbindelser, der har samme navn som forbindelserne i filen med forbindelsesindstillinger. Brugeroprettede forbindelser, der bruger andre navne, opdateres ikke.

Du kan ikke fjerne en forbindelse ved hjælp af filen med forbindelsesindstillinger.

Som nævnt tidligere er standardfilnavnet *connections.json*. Standardplaceringen for filer afhænger af, om du bruger en Windows-enhed eller en Android-enhed:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.Dynamics365forOperations-Warehousing_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.Dynamics365forOperationsWarehousing\files`

Stierne oprettes som regel automatisk efter den første kørsel af appen. Du kan dog oprette dem manuelt, hvis du skal overføre filen med forbindelsesindstillinger til enheden, før du installerer.

> [!NOTE]
> Hvis appen fjernes, fjernes standardstien og dens indhold.

### <a name="import-the-connection-settings"></a>Importere forbindelsesindstillingerne

Benyt følgende fremgangsmåde til at importere forbindelsesindstillinger fra en fil eller en QR-kode.

1. Åbn lagerstedsappen på din mobilenhed.
1. Gå til **Forbindelsesindstillinger**.
1. Angiv indstillingen **Brug demotilstand** til _Nej_.

    ![Brug af indstillingen for demotilstand](media/app-connect-app-demo-mode.png "Brug af indstillingen for demotilstand")

1. Vælg **Vælg fil** eller **Scan QR-kode**, afhængigt af hvordan du vil importere indstillingerne:

    - Hvis du importerer forbindelsesindstillingerne fra en fil, har appen muligvis allerede fundet filen, hvis standardnavnet og standardplaceringen blev brugt, da den blev gemt. Ellers skal du vælge **Vælg fil**, gå til filen på den lokale enhed og vælge den. Hvis du vælger en brugerdefineret placering, gemmer appen den og bruger den automatisk næste gang.
    - Hvis du vil importere forbindelsesindstillingerne ved at scanne en QR-kode, skal du vælge **Scan QR-kode**. Appen beder dig om tilladelse til at bruge enhedens kamera. Når du har givet dig tilladelse, startes kameraet, så du kan bruge det til scanning. Afhængigt af kvaliteten af enhedens kamera og QR-kodens kompleksitet, kan det være vanskeligt at få en korrekt scanning. Hvis det er tilfældet, skal du forsøge at reducere QR-kodens kompleksitet ved kun at oprette én forbindelse pr. QR-kode. (I øjeblikket kan du kun bruge enhedens kamera til at scanne QR-koden).

    ![Importere forbindelsesindstillinger](media/app-connect-app-select-file.png "Importere forbindelsesindstillinger")

1. Når forbindelsesindstillingerne er indlæst, skal du vælge knappen **Tilbage** (venstre pil) i øverste venstre hjørne af siden.

    ![Forbindelsesindstillinger er indlæst](media/app-connect-app-settings-loaded.png "Forbindelsesindstillinger er indlæst")

1. Hvis du bruger en Android-enhed og bruger et certifikat til godkendelse, beder enheden dig om at vælge certifikatet.

    ![Vælg certifikatbeskeden på Android-enhed](media/app-connect-app-choose-cert.png "Vælge certifikatbeskeden på Android-enhed")

1. Appen opretter forbindelse til din Supply Chain Management-server og viser logonsiden.

    ![Logonside](media/app-connect-sign-in.png "Logonside")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Konfigurere applikationen manuelt

Du kan konfigurere manuelt på enheden, så den opretter forbindelse til Supply Chain Management-serveren via Azure AD-applikationen.

1. Åbn lagerstedsappen på din mobilenhed.
1. Gå til **Forbindelsesindstillinger**.
1. Angiv indstillingen **Brug demotilstand** til _Nej_.

    ![Demotilstand er slået fra](media/app-connect-app-select-file.png "Demotilstand er slået fra")

1. Tryk i feltet **Vælg forbindelse** for at udvide de indstillinger, der kræves for at angive forbindelsesoplysningerne manuelt.

    ![Manuelle forbindelsesfelter](media/app-connect-manual-connect.png "Manuelle forbindelsesfelter")

1. Angiv følgende oplysninger:

    - **Brug klienthemmelighed** – angiv denne indstilling til _Ja_ for at bruge en klienthemmelighed til godkendelse med Supply Chain Management. Angiv den til _Nej_ for at bruge et certifikat til godkendelse. (Få flere oplysninger i [Oprette en webtjenesteapplikation i Azure Active Directory](#create-service).)
    - **Forbindelsesnavn** – angiv et navn til den nye forbindelse. Dette navn vises i feltet **Vælg forbindelse**, næste gang du åbner forbindelsesindstillingerne. Det navn, du angiver her, skal være entydigt. (Med andre ord skal det være forskelligt fra alle andre forbindelsesnavne, der er gemt på enheden, hvis der er gemt andre forbindelsesnavne dér).
    - **Active Directory-klient-id** – angiv det klient-id, du har noteret, mens du var i opsætningen af Azure AD i [Oprette en webtjenesteapplikation i afsnittet Azure Active Directory](#create-service).
    - **Active Directory-klienthemmelighed** – dette felt er kun tilgængeligt, hvis indstillingen **Brug klienthemmelig** er angivet til _Ja_. Angiv den klienthemmelighed, du har noteret, mens du var i opsætningen af Azure AD i afsnittet [Oprette en webtjenesteapplikation i Azure Active Directory](#create-service).
    - **Active Directory-certifikataftryk** – dette felt er kun tilgængeligt for Windows-enheder, når indstillingen **Brug klienthemmelig** er angivet til _Nej_. Angiv det certifikataftryk, du har noteret, mens du var i opsætningen af Azure AD i afsnittet [Oprette en webtjenesteapplikation i Azure Active Directory](#create-service).
    - **Active Directory-ressource** – angiv rod-URL-adressen for Supply Chain Management.

        > [!NOTE]
        > Undlad at afslutte denne værdi med en skråstreg (/).

    - **Active Directory-lejer** – angiv den Azure AD-lejer, du bruger til Supply Chain Management-serveren. Denne værdi har formatet `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Her er et eksempel: `https://login.windows.net/contosooperations.onmicrosoft.com`.

        > [!NOTE]
        > Undlad at afslutte denne værdi med en skråstreg (/).

    - **Firma** - angiv den juridiske enhed i Supply Chain Management, som applikationen skal oprette forbindelse til.

1. Vælg knappen **Gem** i øverste højre hjørne af siden.
1. Hvis du bruger en Android-enhed og bruger et certifikat til godkendelse, beder enheden dig om at vælge certifikatet.
1. Appen opretter forbindelse til din Supply Chain Management-server og viser logonsiden.

## <a name="remove-access-for-a-device"></a>Fjerne adgang til en enhed

I tilfælde af en mistet eller beskadiget enhed skal du fjerne adgangen til Supply Chain Management for enheden. De følgende trin beskriver den anbefalede proces til at fjerne adgangen.

1. Gå til **SSystemadministration \> Opsætning \> Azure Active Directory-applikationer**.
1. Slet den linje, der svarer til den enhed, du vil fjerne adgangen til. Noter det klient-id, der bruges til den fjernede enhed, da du får brug for det senere.

    Hvis du kun har registreret ét klient-id, og flere enheder bruger samme klient-id, skal du pushe nye forbindelsesindstillinger til disse enheder. Ellers vil de miste adgang.

1. Log på Azure-portalen på [https://portal.azure.com](https://portal.azure.com/).
1. Vælg **Active Directory** i den venstre navigationsrude, og sørg for, at du er i den rigtige mappe.
1. På listen **Administrer** skal du vælge **Appregistreringer** og derefter vælge den applikation, du vil konfigurere. Siden **Indstillinger** vises og angiver konfigurationsoplysninger.
1. Kontroller, at klient-id'et for applikationen svarer til det klient-id, du har noteret dig i trin 2.
1. Vælg **Slet** på værktøjslinjen.
1. Vælg **Ja** i den bekræftelsesmeddelelsesboks, der vises.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]