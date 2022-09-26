---
title: Brugerdefinerede certifikatprofiler til detailbutikker
description: Denne artikel indeholder en oversigt over de certifikatprofiler, der findes i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: v-chgriffin
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: 5baf043a43210d819b605546089e981c86922ca9
ms.sourcegitcommit: 4f28f262cfb8f047cb5c0070261aa0748835e74b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/21/2022
ms.locfileid: "9558431"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Brugerdefinerede certifikatprofiler til detailbutikker

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over de certifikatprofiler, der findes i Microsoft Dynamics 365 Commerce. Denne funktion udvider funktionen [Administrer hemmeligheder for detailkanaler](../dev-itpro/manage-secrets.md) ved at tilføje understøttelse af lokale certifikater.

Når POS kører i offline tilstand, kan det ikke få adgang til de certifikater, der er gemt i Microsoft Azure Key Vault. Det lokale certifikat skal bruges i stedet. Følgende funktioner understøttes:

- Bruge lokale certifikater i Key Vault-reservescenarier
- Bruge lokale certifikater uden en Key Vault (f.eks. en installation i det lokale miljø)
- Gradvis opdatering af certifikater, hvor nogle butikker og terminaler bruger en ny version af certifikatet, mens andre butikker og terminaler fortsætter med at bruge den tidligere version

Med funktionerne til certifikatprofiler kan du angive et standardcertifikat og angive den rækkefølge, certifikater i den samme certifikatprofil skal søges i. Denne funktionalitet giver også en lignende opsætningstilgang til lokale certifikater og Key Vault-certifikater. Du kan tilføje firmaspecifikke indstillinger for certifikater, men det entydige id på tværs af firmaer for hvert certifikat kan bruges i Commerce-kanalerne.

### <a name="scenarios"></a>Scenarier

Funktionen til certifikatprofiler understøtter følgende scenarier i Commerce-kanalerne:

- Brug et lokalt certifikat i Key Vault-reservescenarier. Her er nogle eksempler på disse reservescenarier:

    - Key Vault-lageret er ikke tilgængeligt.
    - Der blev ikke fundet et certifikat i Key Vault-lageret.
    - POS kører i offline tilstand.

- Brug lokale certifikater uden at gemme dem i Key Vault (f.eks. en installation i det lokale miljø).
- Udfør en gradvis opdatering af certifikater, hvor en ny version af certifikatet kun bruges i butikker eller på terminaler, hvor den nye version allerede er tilgængelig.
- Brug samme certifikat i flere firmaer.

## <a name="set-up-certificate-profiles"></a>Konfigurere certifikatprofiler

Følgende procedure forklarer, hvordan du konfigurerer certifikatprofiler.

### <a name="set-up-key-vault"></a>Konfigurere Key Vault

Følgende trin skal udføres, før du kan bruge et digitalt certifikat, der er gemt i Key Vault.

1. Opret en Key Vault-lagerkonto. Det anbefales, at du implementerer lagerkontoen i samme geografiske område som Commerce Scale Unit.
1. Upload det digitale certifikat til Key Vault-lagerkontoen.
1. Tillad, at AOS-programmet (Application Object Server) må læse hemmeligheder fra Key Vault-lagerkontoen.

Du kan finde flere oplysninger om, hvordan du arbejder med Key Vault, i [Kom i gang med Azure Key Vault](/azure/key-vault/key-vault-get-started).

### <a name="set-up-system-parameters"></a>Angiv systemparametre

Før du konfigurerer certifikatprofiler i Commerce-kanalerne, skal du tillade, at Commerce bruger begge de certifikater, der er lagret i Key Vault og certifikatprofiler.

Gør følgende for at konfigurere systemparametre i Commerce headquarters.

1. På siden **Systemparametre** skal du angive indstillingen **Brug avanceret certifikatlager** til **Ja**.
1. I arbejdsområdet **Styring af funktioner** skal du aktivere funktionen **Brugerdefinerede certifikatprofiler for detailbutikker**.

### <a name="set-up-key-vault-parameters"></a>Konfigurer Key Vault-parametre

På siden **Key Vault-parametre** skal du angive følgende parametre for at få adgang til Key Vault-lageret:

- **Navn** og **Beskrivelse** – Navnet på og beskrivelsen af Key Vault-lagerkontoen.
- **URL-adresse til Key Vault** – URL-adressen til Key Vault-lagerkontoen.
- **Key Vault-klient** – Det interaktive klient-id for det Azure Active Directory-program (Azure AD), der er tilknyttet et Key Vault-lagerkontoen til godkendelsesformål. Denne klient skal have adgang til at læse hemmeligheder fra lagerkontoen.
- **Nøgle-Vault hemmelig nøgle** – En nøgle, der er tilknyttet det Azure AD-program, som bruges til godkendelse i Key Vault-lagerkontoen.
- **Navn**, **Beskrivelse** og **Hemmelig reference** – Navnet på, beskrivelsen af og den hemmelige reference til certifikatet.

Du kan finde flere oplysninger i [Konfigurere Azure Key Vault-klienten](../../finance/localizations/setting-up-azure-key-vault-client.md).

### <a name="configure-a-certificate-profile"></a>Konfigurere en certifikatprofil

Følg disse trin for at konfigurere en certikatprofil i Commerce headquarters.

1. Gå til **Systemadministration \> Opsætning \> Certifikatprofiler**.
1. Vælg **Ny** i handlingsruden for at oprette en post.
1. Angiv værdier i felterne **Certifikatprofil**, **Navn** og **Beskrivelse**.

    > [!NOTE]
    > Certifikatprofilen er et entydigt id for et certifikat på tværs af alle firmaer og Commerce-komponenter.

1. I oversigtspanelet **Juridiske enheder** skal du vælge **Tilføj** for at tilføje en linje.
1. Under **Juridisk enhed** skal du vælge den juridiske enhed (firma), som den aktuelle certifikatprofil skal bruges til.

    Hvis certifikatprofilen skal bruges til flere juridiske enheder, skal du gentage trin 4 og 5 for at tilføje en linje for hver ekstra juridiske enhed.

1. Vælg **Indstillinger** for at åbne siden **Indstillinger for certifikatprofil**, hvor du kan angive firmaspecifikke indstillinger for certifikatprofilen. Angiv, hvilke certifikater der kan bruges, når den aktuelle certifikatprofil kaldes i Commerce-kanalerne. Tilføj lige så mange certifikater, som du har brug for, og angiv prioriteter for dem. Hvis et certifikat med højere prioritet ikke er tilgængeligt, bruges det næste certifikat på baggrund af prioritet. Du kan finde flere oplysninger i afsnittet [Arbejdsgang: søge efter certifikater i Commerce Runtime](#workflow-searching-certificates-in-the-commerce-runtime).

    > [!NOTE]
    > Feltet **Prioritet** angives automatisk. Værdien **1** repræsenterer den højeste prioritet. Når en ny linje tilføjes på siden **Indstillinger for certifikatprofil**, angives prioriteten til et tal, der er ét tal højere end prioriteten for den foregående linje. Hvis du vil ændre prioriteten for en bestemt linje, skal du markere linjen og derefter vælge enten **Flyt op** for at øge prioriteten eller **Flyt ned** for at mindske prioriteten.

1. Når du føjer en ny linje til siden **Indstillinger for certifikatprofil**, skal du angive følgende felter:

    - **Lokationstype** – Vælg den lokation, hvor certifikatet er gemt. Dette felt har to mulige værdier: **Lokalt certifikat** og **Key Vault**.
    - **Key Vault-certifikat** – Dette felt er obligatorisk, hvis du angiver feltet **Lokationstype** til **Key Vault**. Brug det til at angive en Key Vault-certifikathemmelighed.
    - **Butiksnavn** – Dette felt er valgfrit og er kun tilgængeligt, hvis du angiver feltet **Lokationstype** til **Lokalt certifikat**. Brug det til at angive et standardbutiksnavn, der skal bruges til søgning efter lokale certifikater.
    - **Butiksplacering** – Dette felt er valgfrit og er kun tilgængeligt, hvis du angiver feltet **Lokationstype** til **Lokalt certifikat**. Brug det til at angive en standardbutiksplacering, der skal bruges til søgning efter lokale certifikater.

        > [!NOTE]
        > Standardbutiksnavnet og butiksplaceringen tilføjes for at forenkle processen med søgning efter lokale certifikater i Commerce Runtime. X509StoreProvider har en liste over mapper, hvor certifikater gemmes. Hvis standardbutiksnavnet og standardbutiksplaceringen ikke er angivet, forsøger X509StoreProvider at finde et certifikat i de andre mapper på listen. Du kan finde flere oplysninger om tilgængelige værdier for butiksnavnet og butiksplaceringen i [StoreName Enum](/dotnet/api/system.security.cryptography.x509certificates.storename) og [StoreLocation Enum](//dotnet/api/system.security.cryptography.x509certificates.storelocation).

    - **Aftryk** – Dette felt er obligatorisk og er kun tilgængeligt, hvis du angiver feltet **Lokationstype** til **Lokalt certifikat**. Brug det til at angive certifikataftrykket.

        > [!IMPORTANT]
        > Du skal sikre, at den bruger, der kører det program, som skal bruge det lokale certifikat (f.eks. Moderne POS i offlinetilstand) som minimum har skrivebeskyttet adgang til certifikatets private nøgle.

    - **Kommentarer** – Dette felt er valgfrit, og brugerne kan skrive bemærkninger.

## <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Arbejdsgang: søge efter certifikater i Commerce Runtime

Her er den grundlæggende arbejdsgang, der bruges til at søge efter et certifikat, når en certifikatprofil kaldes i Commerce Runtime.

1. Systemet identificerer, om certifikatprofilen har firmaspecifikke indstillinger for den aktuelle juridiske enhed.
1. Systemet forsøger at finde certifikatet ved hjælp af værdierne på siden **Indstillinger for certifikatprofil** for den linje, hvor feltet **Prioritet** er angivet til **1**.

    - Hvis feltet **Lokationstype** er angivet til **Key Vault**, bruges værdien af feltet **Key Vault-certifikathemmelighed** til at søge efter certifikatet på siden **Key Vault-parametre**. Der søges efter certifikatet i Key Vault-lageret.
    - Hvis feltet **Lokationstype** er angivet til **Lokalt certifikat**, søger X509StoreProvider først efter certifikatet ved hjælp af standardbutiksnavnet og butiksplaceringen, hvis disse parametre er angivet. Den søger derefter i alle andre mapper på listen over mapper.

1. Hvis certifikatet ikke bliver fundet, gentages processen for den linje, hvor **Prioritet**-feltet er angivet til **2** osv.

> [!NOTE]
> Hvis certifikatprofilen ikke har nogen indstillinger for den aktuelle juridiske enhed, eller hvis certifikatsøgningen mislykkes for alle linjer på siden **Indstillinger for certifikatprofil**, findes certifikatet ikke.

### <a name="caching-the-results-of-certificate-searches"></a>Cachelagre resultaterne af certifikatsøgninger

Resultaterne af certifikatsøgninger cachelagres. Standardudløbsdatoen for en cache er én time. Denne tid kan dog tilpasses og angives til en maksimumværdi på 24 timer.

## <a name="gradual-update"></a>Gradvis opdatering

Hvis der introduceres en ny version af certifikatet, men det ikke kan opdateres i alle lagre på samme tid, kan du bruge certifikatprofilerne til at opdatere certifikatet gradvist.

1. Find en certifikatprofil og den linje, der skal opdateres, og vælg derefter **Indstillinger**.
1. Tilføj en linje, og angiv indstillinger, der er relateret til den seneste version af certifikatet.
1. Forøg **Prioritet**-værdien for den nye linje. Brug knappen **Flyt op** til at flytte linjen, så den ligger over linjen for den forrige version af det samme certifikat.
> [!NOTE]
> I Commerce Runtime vil den nye version af certifikatet blive kaldt først. Hvis certifikatet endnu ikke er opdateret i en bestemt butik eller på en bestemt terminal, vil den tidligere version blive kaldt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
