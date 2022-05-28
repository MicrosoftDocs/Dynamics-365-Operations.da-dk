---
title: Signere MPOS med et kodesigneringscertifikat
description: Dette emne indeholder en forklaring på, hvordan du signerer MPOS med et kodesigneringscertifikat.
author: mugunthanm
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 28021
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.openlocfilehash: e45961cf1ddb385d914b700d03bc95d07de47b68
ms.sourcegitcommit: d70f66a98eff0a2836e3033351b482466bd9c290
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2022
ms.locfileid: "8741539"
---
# <a name="sign-mpos-appx-with-a-code-signing-certificate"></a>Signere MPOS appx med kodesigneringscertifikat

[!include [banner](../includes/banner.md)]

Hvis du vil installere MPOS (Modern POS), skal du signere MPOS-appen med et kodesigneringscertifikat fra en betroet udbyder og installere det samme certifikat på alle de maskiner, hvor MPOS er installeret under den aktuelle brugers betroede rodmappe.

Hvis du vil signere MPOS-appen med et certifikat, skal du bruge en af disse indstillinger i **Retail SDK\\Build-værktøj\\Customization.settings**-filen:

- Tilføj delen Sikker filopgave i Azure DevOps-opbygningstrin, og upload certifikatet for at sikre filopgaven. Brug stivariablen til det sikre filopgaveoutput som parameter i filen Customization.settings.

    > [!NOTE]
    > Opgaven Sikker fil understøtter ikke et certifikat, der er beskyttet med adgangskode. Du skal fjerne adgangskoden, før du overfører denne opgave. Da certifikatet overføres til den sikre filsystemopgave i Azure, kan du kun fjerne adgangskoden for dette trin. Du bør dog diskutere fjernelse af adgangskoden med sikkerhedseksperterne for at finde ud af, om dette er den korrekte handling for dit projekt. Fjern ikke certifikatadgangskoden for andre scenarier.
- Brug et certifikat, der findes i filsystemet. Det kan du gøre ved at hente eller generere et certifikat og anbringe det i det filsystem, hvor buildet kører. Den Microsoft-hostede agent eller build-bruger skal have adgang til denne sti og fil.
- Brug aftryk til at slå op i certifikatet i butikken og logge på med det pågældende certifikat.

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>Bruge en sikker filopgave til signering af Universal Windows Platform-appen

> [!NOTE]
> Du kan også bruge Azure Key Vault til at gemme certifikatet og bruge Azure-værktøjet til at signere .appx-filen til Modern POS og selvbetjeningsinstallationerne. Du kan finde eksempel-pipeline-scripts og flere oplysninger i [Konfigurere en build-pipeline i Azure DevOps til at generere Retail-selvbetjeningspakker](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages).

Brug af opgaven Sikker fil er den anbefalede metode til signering af UWP-appen (Universal Windows Platform). Du kan finde flere oplysninger om pakkesignering under [Konfigurere pakkesignering](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing). Denne proces er vist i følgende billede.

![Signeringsflow for MPOS-app.](media/POSSigningFlow.png)

> [!NOTE]
> I øjeblikket understøtter OOB-pakningen kun signering af appx-filen, men de forskellige selvbetjeningsinstallationer som f.eks. MPOIS, RSSU og HWS signeres ikke af denne proces. Du skal signere den manuelt ved hjælp af SignTool eller andre signeringsværktøjer. Det certifikat, der bruges til signering af appx-filen, skal være installeret i den maskine, hvor Modern POS er installeret.

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>Trin til at konfigurere certifikatet til signering i Azure Pipelines

### <a name="certificate-in-the-file-systemsecure-location"></a>Certifikat i filsystemet/sikker placering

Download [opgaven DownloadFile](/visualstudio/msbuild/downloadfile-task), og tilføj den som det første trin i build-processen. Fordelen ved at bruge opgaven Sikker fil er, at filen er krypteret og placeret på disken under build, uanset om build-pipelinen lykkes, mislykkes eller annulleres. Filen slettes fra overførselsplaceringen, når build-processen er fuldført.

1. Download og tilføj opgaven Sikker fil som det første trin i Azure-build-pipelinen. Du kan hente opgaven Sikker fil fra [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile).
2. Overfør certifikatet til opgaven Sikker fil, og angiv referencenavnet under Outputvariabler, som vist på følgende billede.
    > [!div class="mx-imgBorder"]
    > ![Opgaven Sikker fil.](media/SecureFile.png)
3. Opret en ny variabel i Azure Pipelines ved at vælge **Ny variabel** under fanen **Variabler**.
4. Angiv et navn til variablen i værdifeltet, f.eks. **MySigningCert**.
5. Gem variablen.
6. Åbn filen **Customization.settings** fra **RetailSDK\\BuildTools**, og opdater **ModernPOSPackageCertificateKeyFile** med det variabelnavn, der er oprettet i pipelinen (trin 3). F.eks.:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    Dette trin skal angives, hvis certifikatet ikke er beskyttet med adgangskode. Hvis certifikatet er beskyttet med adgangskode, skal du fortsætte med følgende trin.
 
7. Tilføj en ny variabel med sikker tekst under fanen **Variabler** for pipelinen. Angiv navnet **MySigningCert.secret**, og angiv værdien for adgangskoden til certifikatet. Vælg låseikonet for at sikre variablen.
8. Føj en **Powershell-script**-opgave til pipelinen (efter Download sikker fil og før build-trinnet). Angiv det **Viste** navn, og angiv Typen som **Inline**. Kopiér og indsæt følgende i scriptsektionen.

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

9. Åbn filen **Customization.settings** fra **RetailSDK\\BuildTools**, og opdater **ModernPOSPackageCertificateThumbprint** med værdien af certifikataftrykket.

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
Yderligere oplysninger om, hvordan du henter aftryk for et certifikat, finder du i [Hent et certifikats aftryk](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint). 

 
## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>Hente eller generere et certifikat til manuel signering af MPOS-appen ved hjælp af msbuild i SDK

Hvis et hentet eller genereret certifikat bruges til at signere MPOS-appen, skal du opdatere **ModernPOSPackageCertificateKeyFile**-noden i filen **BuildTools\\Customization.settings** til at pege på pfx-filplaceringen (**$(SdkReferencesPath)\\appxsignkey.pfx**). F.eks.:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

I dette tilfælde er navnet på certifikatfilen **appxsignkey.pfx**, som findes i mappen **Retail SDK\\Reference**.

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>Bruge aftryk til at signere MPOS-appen

Hvis du bruger aftryk til at signere MPOS-appen, skal du installere certifikatet lokalt. Brug aftryksværdien i noden **ModernPOSPackageCertificateThumbprint** i filen **BuildTools\\Customization.settings**.

Denne indstilling vil fungere, hvis build-brugeren er en lokal bruger. Men hvis du bruger Azure DevOps-agenterne til at generere buildet, har agenten muligvis ikke adgangstilladelse til certifikatbutikken for at bruge certifikatet til signering, eller også har build-maskinen ikke certifikatet installeret. I dette tilfælde er løsningen at ændre build-brugeren til den lokale bruger og installere certifikatet i feltet. Men denne indstilling vil ikke fungere, hvis du ikke har administratoradgang til feltet.

> [!NOTE]
> Hvis .pfx-filen eller opgaveindstillingen Sikker fil bruges til at signere appen, skal du lade noden **ModernPOSPackageCertificateThumbprint** være tom i **Customization.settings**. Hvis aftryksindstillingen bruges, skal du lade **ModernPOSPackageCertificateKeyFile** være tom. Hvis begge værdier opdateres, mislykkes build'et.

### <a name="certification-renewal"></a>Fernyelse af certificering

### <a name="renew-a-certificate-from-trusted-ca"></a>Forny et certifikat fra et betroet CA

Kontakt din certificeringsmyndighed (CA) for processen til fornyelse af certifikatet. Der kræves ingen handling på MPOS-siden for et certifikat, der er tillid til.

### <a name="renew-a-self-signed-certificate"></a>Forny et selvsigneret certifikat

Du må ikke bruge det eksempelcertifikat, der er tilgængeligt i Retail SDK til produktion. Det kan alene anvendes til udvikling. Eksempelcertifikatet for Contoso kan ikke fornys, og det eksempelcertifikat, der er inkluderet i Retail SDK version 10.0.16 eller tidligere, udløb den 31. december 2020. Hvis dette certifikat, eller et selvsigneret certifikat, er blevet brugt til at signere en tilpasset Modern POS, er der stor risiko for, at Modern POS ikke vil fungere korrekt efter denne dato.
 
### <a name="impact"></a>Effekt
 
Hvis ovenstående gælder for dig, vil det problem, du kommer til at opleve, være, at installationsprogrammet ikke kan køre efter 31. december 2020. Afhængigt af de anvendte it-politikker for virksomheden kan Modern POS muligvis ikke fungere. Det er vigtigt, at du tester dette ved at ændre datoen midlertidigt til en fremtidig dato for at fastlægge påvirkningen i din organisation.
 
### <a name="steps-to-determine-the-issue"></a>Trin til bestemmelse af problemet
 
1.  Brug Windows-indstillinger til at ændre computerens or til en dato og et klokkeslæt i år 2021.
2.  Kontrollér, at Modern POS kan åbnes, at der kan logges på, og at en transaktion kan fuldføres.
3.  Kontrollér, at installationsprogrammet til selvbetjening af Modern POS kan køres, og at installationen i så tilfælde kan fuldføres.
4.  Nulstil Windows-uret til korrekt dato og klokkeslæt.
 
Hvis du kan udføre alle disse trin uden problemer, kan du operere med det aktuelle certifikat efter end 31. december 2020.  
 
### <a name="steps-going-forward"></a>Næste trin 

Det anbefales kraftigt, at du fornyer det tidligere brugte certifikat. Det anbefales på det kraftigste, at du anskaffer et nyt certifikat. Det kan du gøre ved at udføre en af følgende opgaver:
 
- **Foretrukket** – Hent et kodesigneringscertifikat fra et betroet nøglecenter (CA).

- **Ikke foretrukket** – Generér et selvsigneret kodesigneringscertifikat, der skal bruges. Dette bruges typisk kun til udviklingsformål inden for et domæne og anbefales ikke til produktion. 

- **Tilgængelig som en midlertidig løsning** – Brug det fornyede Contoso-kodesigneringscertifikat. Det bruges typisk til testformål, så det frarådes at implementere det i produktionen.
 
Derefter skal du generere en ny brugerdefineret pakke til Moder POS, som er signeret med brug af dette certifikat, som er hentet fra en af handlingerne ovenfor. Udfør et af følgende trin, alt efter certifikatet:
 
- Hvis du bruger et nyt certifikat, der er tillid til (eller et nyt selvsigneret certifikat), skal du installere et nyt certifikat på alle enheder. Når dette er gjort, skal du tage den nyoprettede Modern POS-pakke (installer), afinstallere det eksisterende program og derefter geninstallere den nye Modern POS-pakke. Du skal udføre en enhedsaktivering af Modern POS på alle enheder.

- Hvis du anvender det fornyede Contoso-certifikat, skal du installere det nye certifikat på alle enheder og installere Modern POS-pakken (installer). Det er ikke et krav at afinstallere, men du skal geninstallere på enheden. Bemærk, at det ikke er nødvendigt at aktivere enheden for Modern POS. Denne mulighed er en midlertidig løsning. Brug denne mulighed til at undgå genaktivering og løsning af problemet, før du får et nyt betroet certifikat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
