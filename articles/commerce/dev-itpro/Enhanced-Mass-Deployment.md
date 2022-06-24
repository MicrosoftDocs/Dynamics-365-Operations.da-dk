---
title: Masseinstallation af forseglede Commerce-selvbetjeningskomponenter
description: Denne artikel indeholder en forklaring på, hvordan du kan bruge strukturen til installation af selvbetjeningskomponenter til uovervåget installation og tjenesteudrulninger.
author: jashanno
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: a679d78db3ad5bd9cccbd4ab6a7026bd07890f55
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898573"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>Masseinstallation af forseglede Commerce-selvbetjeningskomponenter

[!include [banner](../includes/banner.md)]

Denne artikel gælder for den lukkede struktur, komponentinstallationer, der frigives hver måned, med start i version 10.0.18, og som gøres tilgængelige i det delte aktivbibliotek i Microsoft Dynamics Lifecycle Services (LCS). Bemærk, at de første adskillige versioner af disse nye installationsprogrammer er angivet som **(forhåndsversion)**. Det eneste formål med denne betegnelse er dog at skelne mellem de nye installationsprogrammer, mens Microsoft beslutter, om der er andre funktionskrav til at bruge dem. Det betyder ikke, at installationsprogrammerne ikke er gyldige til produktion. Baseret på frigivelsen af disse nye installationsprogrammer planlægger Microsoft at udfase de gamle (ældre) installationsprogrammer i eller omkring oktober 2023. 

Denne artikel forklarer, hvordan du bruger de nye installationsprogrammer til at udføre uovervåget installation og servicering af opdateringer via kommandolinjeargumenter. Med disse argumenter kan du udføre masseinstallationer på flere forskellige måder.

> [!NOTE]
> De nye forseglede selvbetjeningsinstallationsprogrammer bliver ikke tilgængelige i hovedkontoret og kan kun hentes via LCS.

## <a name="delimiters-for-mass-deployment"></a>Separatorer for masseudrulning

Følgende tabel viser de afgrænsningstegn, der kan bruges i udførelse af kommandolinjen.


| Separator                 | Beskrivende tekst |
|---------------------------|-------------|
| --AadTokenIssuerPrefix | Præfikset for Microsoft Azure Active Directory-tokenudstederen (Azure AD). |
| --AsyncClientAadClientId | Det Azure AD-klient-id, som Async Client skal bruge under kommunikation med hovedkontoret. |
| --AsyncClientAppInsightsInstrumentationKey | Instrumenteringsnøgle for Async Client AppInsights. |
| --AsyncClientCertFullPath | Den fuldt formaterede URN-sti, der bruger aftrykket som søgemetrikværdi for Async Client Identity-certifikatplaceringen, der skal bruges til godkendelse i Azure AD til kommunikation med hovedkontoret. F.eks. er `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` en korrekt formateret URN. Værdien **\<MyThumbprint\>** erstattes med det certifikataftryk, der skal bruges. Du må ikke bruge denne parameter sammen med parameteren **-AsyncClientCertThumbprint**. |
| --AsyncClientCertThumbprint | Aftrykket af Async Client Identity-certifikatet, der skal bruges til godkendelse hos Azure AD til kommunikation med hovedkontoret. Dette aftryk bruges til at søge i placeringen af og navnet på **LocalMachine/Min butik** for at finde det rette certifikat, der skal bruges. Du må ikke bruge denne parameter sammen med parameteren **-AsyncClientCertFullPath**. |
| --ClientAppInsightsInstrumentationKey | Instrumenteringsnøgle for Client AppInsights. |
| --CloudPosAppInsightsInstrumentationKey | Instrumenteringsnøgle for Cloud POS AppInsights. |
| --Config | Den konfigurationsfil, der skal bruges under installationen. **Contoso.CommerceScaleUnit.xml** er et eksempel på et filnavn. |
| --CposAadClientId | Det Azure AD-klient-id, som Cloud POS skal bruge under enhedsaktivering. Denne parameter er ikke påkrævet i forbindelse med udrulninger i det lokale miljø. |
| --Device | Enheds-id'et, som det vises på siden **Enheder** i hovedkontoret. |
| --EnvironmentId | Miljø-id'et. |
| --HardwareStationAppInsightsInstrumentationKey | Instrumenteringsnøgle for Hardware Station AppInsights. |
| --Install | En parameter, der angiver, om den komponent, som dette installationsprogram leverer, skal installeres. Denne parameter er ikke påkrævet. |
| --InstallOffline | I forbindelse med Modern POS angiver denne parameter, at offlinedatabasen også skal installeres og konfigureres. Brug også parameteren **-SQLServerName**. Ellers forsøger installationsprogrammet at finde en standardforekomst, der opfylder forudsætningerne. |
| --Port | Den port, der skal knyttes til og bruges af den virtuelle mappe i Retail Server. Standardporten, 443, bruges, hvis der ikke angives en port. |
| --Register | Kasseapparat-id'et, som det vises på siden **Kasseapparater** i hovedkontoret. |
| --RetailServerAadClientId | Det Azure AD-klient-id, som Retail Server skal bruge under kommunikation med hovedkontoret. |
| --RetailServerAadResourceId | Det ressource-id for Retail Server-appen Azure AD, der skal bruges under enhedsaktivering. Denne parameter er ikke påkrævet i forbindelse med udrulninger i det lokale miljø. |
| --RetailServerCertFullPath | Den fuldt formaterede URN-sti, der bruger aftrykket som søgemetrikværdi for Retail Server Identity-certifikatplaceringen, der skal bruges til godkendelse i Azure AD til kommunikation med hovedkontoret. F.eks. er `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` et korrekt formateret URN, hvor værdien **\<MyThumbprint\>** erstattes af det certifikataftryk, der skal bruges. Du må ikke bruge denne parameter sammen med parameteren **-RetailServerCertThumbprint**. |
| --RetailServerCertThumbprint | Aftrykket af Retail Server Identity-certifikatet, der skal bruges til godkendelse hos Azure AD til kommunikation med hovedkontoret. Dette aftryk bruges til at søge i placeringen af og navnet på **LocalMachine/Min butik** for at finde det rette certifikat, der skal bruges. Du må ikke bruge denne parameter sammen med parameteren **-RetailServerCertFullPath**. |
| --RetailServerURL | URL-adressen på den Retail Server, som installationsprogrammet skal bruge. (Denne URL-adresse kaldes også Commerce Scale Unit \[CSU\] URL). I forbindelse med Modern POS bruges denne værdi under enhedsaktivering. |
| --SkipAadCredentialsCheck| En switch, der angiver, om kontrol af Azure AD-legitimationsoplysninger skal springes over. Standardværdien er **falsk**. |
| --SkipCertCheck | En switch, der angiver, om kontrol af certifikatforudsætninger skal springes over. Standardværdien er **falsk**. |
| --SkipIisCheck | En switch, der angiver, om kontrol af IIS-forudsætninger (Internet Information Services) skal springes over. Standardværdien er **falsk**. |
| --SkipNetFrameworkCheck | En switch, der angiver, om kontrol af .NET Framework-forudsætninger skal springes over. Standardværdien er **falsk**. |
| --SkipScaleUnitHealthcheck | En switch, der angiver, om tilstandskontrol på installerede komponenter skal springes over. Standardværdien er **falsk**. |
| --SkipSChannelCheck | En switch, der angiver, om kontrol af sikker kanal-forudsætninger skal springes over. Standardværdien er **falsk**. |
| --SkipSqlFullTextCheck | En switch, der angiver, om validering af den forudsætning for SQL Server, der kræver fuldtekstsøgning, skal springes over. Standardværdien er **falsk**. |
| --SkipSqlServerCheck | En switch, der angiver, om kontrol af SQL Server-forudsætning skal springes over. Standardværdien er **falsk**. |
| --SqlServerName | SQL Server-navnet. Hvis navnet ikke er angivet, forsøger installationsprogrammet at finde standardforekomsten. |
| --SslcertFullPath | Den fuldt formaterede URN-sti, der bruger aftrykket som søgemetrik for den certifikatplacering, der skal bruges til at kryptere HTTP-trafik til skalaenheden. F.eks. er `store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>` et korrekt formateret URN, hvor værdien **\<MyThumbprint\>** erstattes af det certifikataftryk, der skal bruges. Du må ikke bruge denne parameter sammen med parameteren **-SslCertThumbprint**. |
| --SslCertThumbprint | Aftrykket af det certifikat, der skal bruges til at kryptere HTTP-trafik til skalaenheden. Dette aftryk bruges til at søge i placeringen af og navnet på **LocalMachine/Min butik** for at finde det rette certifikat, der skal bruges. Du må ikke bruge denne parameter sammen med parameteren **-SslCertFullPath**. |
| --StoreSystemAosUrl | Hovedkontorets URL-adresse (AOS) |
| --StoreSystemChannelDatabaseId | Id'et for kanaldatabasen (navn). |
| --TenantId | Azure AD-lejer-id. |
| --TransactionServiceAzureAuthority | Transaction Service Azure AD-myndigheden. |
| --TransactionServiceAzureResource | Transaction Service Azure AD-ressourcen. |
| --TrustSqlServerCertificate | En switch, der angiver, om der skal være tillid til Server-certifikatet, mens der oprettes forbindelse til SQL Server. Med henblik på at undgå sikkerhedsrisici bør produktionsinstallationer aldrig her angive en **sand** værdi. Standardværdien er **falsk**. |
| --Verbosity | Det logføringsniveau, der anmodes om under installationen. Normalt bør denne værdi ikke bruges. |
| --WindowsPhoneAppInsightsInstrumentationKey | Instrumenteringsnøgle for Hardware Station AppInsights. |

## <a name="general-overview"></a>Generel oversigt

Den nye struktur for installationsprogrammer til selvbetjening har forskellige funktioner og forbedringer. Den nye struktur genererer i øjeblikket kun installationsprogrammer til Modern POS, hardwarestation og CSU (selvhostet). Det er vigtigt at forstå den grundlæggende brug af kommandolinjer til forseglede installationsprogrammer, som skal ligne dem, der bruges i følgende eksempel. 
 
```Console
<Component Installer Name>.exe install --<Parameter Name> "<Parameter Information>"
```

Installationsprogrammet kræver parameteren **install** (eller **uninstall** for at fjerne installationen) og eventuelle parametre, der er specifikke for den pågældende installation. **Parameternavn** skal indeholde eventuelle parametre, der skal bruges, f.eks. til kasseapparat, CSU-URL-adresse eller certifikatoplysninger. **Parameteroplysninger** skal omfatte eventuelle yderligere oplysninger om parametrene.

Den forseglede struktur er oprettet for at tage hensyn til følgende ændringer:
- **Forseglet** – Den nye installationsstruktur adskiller helt installationsprogrammer for Microsoft-distribuerede basiskomponenter fra de udvidelsesbaserede tilpasninger. Tilpasningerne installeres senere, men vil derefter være frie i forhold til opdateringer (så opdateringer kun tillades for Microsoft-basiskomponenten, kun for tilpasningerne eller for begge).
- **GUI-less** – Der findes ikke længere en brugergrænseflade (UI). I stedet er der en fuldstændig kommandolinjebaseret eksekverbar linje for hver installationsprogramkomponent. Denne ændring er en af flere centrale ændringer eller funktioner, der bruges til at fokusere på den nye installationsstruktur til brug sammen med masseudrulninger.
- **Dybere logføring** – Udvidede installationslogfiler giver mulighed for bedre validering af fuldførelse eller fejl under installationen, de trin, der blev udført, og eventuelle advarsler eller fejl, der er genereret.
- **Oprydning** – I den nye struktur arbejder komponentinstallationerne hårdere på at vedligeholde oprydningen af installationsmapper ved at fjerne det fulde indhold i komponentmappen, før de installerer de nyere komponenter. Denne oprydning sikrer, at der ikke er nogen restfiler, der kan forårsage problemer og forhindre korrekt installation.

Tre komponenter er ikke blevet overflyttet til den nye struktur: virtuel simulator til eksterne enheder, Async Server Connector Service (bruges til Understøttelse af Dynamics AX 2012 R3) og Real-time Service Replacement (bruges til AX 2012 R3-understøttelse).

> [!NOTE]
> Installationsprogrammer gemmes lokalt og bevares.  Det er vigtigt med tiden at administrere eller slette de opbevarede installationsprogrammer, så de ikke spilder diskplads. Det anbefales, at det aktuelle installationsprogram til basiskomponenterne og eventuelle udvidelsesinstallationer til de seneste versioner beholdes til gendannelse i forbindelse med nødsituationer.

## <a name="migration"></a>Overførsel

Migrering fra de gamle selvbetjeningskomponenter for installationsprogrammer til den nye installationsstruktur kræver afinstallation af de gamle komponenter.

- **Modern POS** – Den nye installationsstruktur har medført, at programmet modtager et nyt signatur-id for programmet. Derfor kræves der fuld afinstallation af gamle komponenter, før den nye struktur for Modern POS-komponent installeres. Pga. kravet om fuldstændig afinstallation skal enhedsaktivering foretages igen. (Denne enhedsgenaktivering er et engangskrav, forudsat at afinstallationen ikke finder sted igen).
- **Hardwarestation** – Som et IIS-websted kræver den nye installationsstruktur, at basismappestrukturen ændres. Derfor kræves der fuld afinstallation af gamle komponenter, før den nye struktur for hardwarestationens komponent installeres.
- **CSU (Commerce Scale Unit, selvhostet)** – Som en serie af IIS-websteder kræver den nye installationsstruktur, at basismappestrukturen ændres.  Derfor kræves der fuld afinstallation af gamle komponenter, før den nye struktur for CSU (selvhostet)-komponent installeres.

## <a name="modern-pos"></a>Moderne POS

### <a name="before-you-begin"></a>Før du begynder

Det er vigtigt, at du fjerner den gamle selvbetjeningskomponent til Modern POS. Du kan finde flere oplysninger i migreringstrin tidligere i denne artikel.

### <a name="examples-of-silent-deployment"></a>Eksempler på uovervåget installation

Dette afsnit indeholder eksempler på kommandoer, der bruges til at installere Modern POS.

#### <a name="silently-install-modern-pos"></a>Installere Modern POS uovervåget

Følgende kommando installerer (eller opdaterer) Modern POS uovervåget. Den har den standardkommandostruktur, der bruges til uovervåget service af komponenter, der er installeret i øjeblikket. Strukturen bruger de grundlæggende værdier fra **&lt;InstallerName&gt;.exe**.

Følgende grundlæggende kommando viser de tilgængelige muligheder, hvis der anmodes om en installation. Det anbefales kraftigt, at denne kommando bruges, når installationsprogrammet testes eller bruges første gang.

```Console
CommerceModernPOS.exe --help install
```

> [!NOTE]
> En konfigurationsfil er ikke påkrævet for Modern POS. Installationsprogrammet har nu parametre (vist tidligere i denne artikel) for de forskellige værdier, der bruges under enhedsaktivering.

Følgende kommando angiver alle de parametre, der skal bruges under enhedsaktivering, efter at programmet Modern POS er installeret. I dette eksempel bruges kasseapparatet **Houston-3**, som er en almindeligt anvendt værdi i Dynamics 365 Commerce-demodata.

```Console
CommerceModernPOS.exe install --Register "Houston-3" --Device "Houston-3" --RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

Følgende kommando angiver de parametre, der skal bruges til at installere og konfigurere offlinedatabasen. SQL Server angives sammen med den konfigurationsfil, der skal bruges.

```Console
CommerceModernPOS.exe install --InstallOffline --SQLServerName "SQLExpress" --Config "ModernPOS.Houston-3.xml"
```

Du kan mikse og matche disse begreber for at opnå de ønskede installationsresultater.

## <a name="hardware-station"></a>Hardwarestation

### <a name="before-you-begin"></a>Før du begynder

Det er vigtigt, at du fjerner den gamle selvbetjeningskomponent til hardwarestationen. Du kan finde flere oplysninger i migreringstrin tidligere i denne artikel. Der er ikke længere et værktøj til forhandleres kontooplysninger. Oplysningerne om forhandlerens konto installeres i stedet, når en POS-terminal parres med hardwarestationen. Det anbefales kraftigt at køre følgende kommando, når installationsprogrammet testes første gang:

```Console
CommerceHardwareStation.exe --help install
```

### <a name="examples-of-silent-deployment"></a>Eksempler på uovervåget installation

Dette afsnit indeholder eksempler på kommandoer, der bruges til at installere hardwarestation.

#### <a name="silently-install-hardware-station"></a>Installere hardwarestation uovervåget

Følgende kommando installerer (eller opdaterer) hardwarestation uovervåget. Den har den standardkommandostruktur, der bruges til at servicere komponenter, der er installeret i øjeblikket. Strukturen bruger de grundlæggende værdier fra **&lt;InstallerName&gt;.exe**.

Følgende grundlæggende kommando kører installationsprogrammets eksekverbare fil.

```Console
HardwareStation.exe install --Port 443 --StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" --StoreSystemChannelDatabaseID "Houston" --SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> En konfigurationsfil er ikke påkrævet for hardwarestation. Installationsprogrammet har nu parametre (vist tidligere i denne artikel) for de forskellige værdier, der er påkrævet.

Følgende kommando angiver alle de parametre, der kræves for at springe de nødvendige kontroller over under en standardinstallation. 

> [!NOTE]
> Det frarådes at springe kontroller over, hvis der ikke er foretaget grundige test i forvejen eller i udviklingssituationer.

```Console
HardwareStation.exe install --SkipFirewallUpdate --SkipOPOSCheck --SkipVersionCheck --SkipURLCheck --Config "HardwareStation.Houston.xml"
```

Det er almindelig praksis at mikse og matche disse begreber for at opnå de ønskede installationsresultater.

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (selvhostet)

Det anbefales kraftigt at køre følgende kommando, når installationsprogrammet testes første gang:

```Console
CommerceStoreScaleUnitSetup.exe --help install
```

### <a name="before-you-begin"></a>Før du begynder

Det er vigtigt, at du fjerner den gamle selvbetjeningskomponent til CSU (selvhostet). Du kan finde flere oplysninger i migreringstrin tidligere i denne artikel.

### <a name="examples-of-silent-deployment"></a>Eksempler på uovervåget installation

Dette afsnit indeholder eksempler på kommandoer, der bruges til at installere CSU (selvhostet).

#### <a name="silently-install-csu-self-hosted"></a>Uovervåget installation af CSU (selvhostet)

Følgende kommando installerer (eller opdaterer) CSU (selvhostet) uovervåget. Den har den standardkommandostruktur, der bruges til uovervåget service af komponenter, der er installeret i øjeblikket. Strukturen bruger de grundlæggende værdier fra **&lt;InstallerName&gt;.exe**.

Sammenlignet med de andre selvbetjeningsinstallationer er CSU (Commerce Scale Unit) mere kompliceret og kræver mange flere oplysninger. Følgende kommando er den minimumkommando (med parametre), der skal bruges til at køre installationsprogrammets eksekverbare fil, når der ikke findes en konfigurationsfil.

```Console
CommerceScaleUnit.exe install --port 446 --SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate --Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> Der kræves stadig en konfigurationsfil til CSU (selvhostet).

Følgende kommando er en mere grundig kommando, der kører installationsprogrammets eksekverbare fil med visse alternative parametre.

```Console
CommerceScaleUnit.exe install --Port 446 --SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate --Verbosity 0 --Config "Contoso.StoreSystemSetup.xml"
```

Følgende kommando angiver de parametre, der kræves for at springe de forudsættende kontroller over under en standardinstallation. 

> [!NOTE]
> Det frarådes at springe kontroller over, hvis der ikke er foretaget grundige test i forvejen eller i udviklingssituationer.


```Console
CommerceScaleUnit.exe installer --skipscaleunithealthcheck --skipcertcheck --skipaadcredentialscheck --skipschannelcheck --skipiischeck --skipnetcorebundlecheck --skipsqlservercheck --skipnetframeworkcheck --skipversioncheck --skipurlcheck --Config "Contoso.StoreSystemSetup.xml" --SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate
```

Du kan mikse og matche disse begreber for at opnå de ønskede installationsresultater.

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
