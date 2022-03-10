---
title: Brugerdefinerede certifikatprofiler til detailbutikker
description: I dette emne kan du finde en oversigt over, hvordan certifikater bruges i detailbutikker.
author: josaw
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9cb82a6d6336bb69fe818fb33e04ad621382b383055b24a4e79eee5ddff217ac
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719924"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Brugerdefinerede certifikatprofiler til detailbutikker

[!include [banner](../includes/banner.md)]


## <a name="overview"></a>Overblik

Dette emne indeholder en oversigt over de certifikatprofiler, der findes i Microsoft Dynamics 365 Commerce. Denne funktion udvider funktionen [Administrer hemmeligheder for detailkanaler](../dev-itpro/manage-secrets.md) ved at tilføje understøttelse af lokale certifikater.

Når POS kører i offline tilstand, kan det ikke få adgang til de certifikater, der er gemt i key vault. Det lokale certifikat skal bruges i stedet. Følgende funktioner understøttes:

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

Følgende procedure forklarer, hvordan du konfigurerer certifikatprofiler. Før du brugercertifikatprofiler i Commerce-kanaler, skal du udføre disse trin for at konfigurere indstillingerne.

1. I arbejdsområdet **Styring af funktioner** skal du aktivere funktionen **Brugerdefinerede certifikatprofiler for detailbutikker**.
2. Gå til **Systemadministration \> Opsætning \> Certifikatprofiler**.
3. Opret en post, og angiv felterne **Certifikatprofil**, **Navn** og **Beskrivelse** for den.

    > [!NOTE]
    > Certifikatprofilen er et entydigt id for et certifikat på tværs af alle firmaer og Commerce-komponenter.

3. Under fanen **Juridiske enheder** kan du tilføje en linje og vælge den juridiske enhed (firma), som den aktuelle certifikatprofil skal bruges til. Hvis certifikatprofilen skal bruges til flere juridiske enheder, skal du gentage dette trin for at tilføje en linje for hver ekstra juridiske enhed.
4. Vælg **Indstillinger** for at åbne siden **Indstillinger for certifikatprofil**, hvor du kan angive firmaspecifikke indstillinger for certifikatprofilen.

### <a name="certificate-profile-settings"></a>Certifikatprofilindstillinger

Når du vælger **Indstillinger** for certifikatprofillinjer, vises siden **Indstillinger for certifikatprofil**. På denne side kan du angive, hvilke certifikater der kan bruges, når den aktuelle certifikatprofil kaldes i Commerce-kanalerne. Du kan også angive den rækkefølge, som certifikater skal gennemsøges i.

> [!NOTE]
> Feltet **Prioritet** angives automatisk. Værdien **1** repræsenterer den højeste prioritet. Når en ny linje tilføjes på siden **Indstillinger for certifikatprofil**, angives prioriteten til et tal, der er ét tal højere end prioriteten for den foregående linje. Hvis du vil ændre prioriteten for en bestemt linje, skal du markere linjen og derefter vælge enten **Flyt op** for at øge prioriteten eller **Flyt ned** for at mindske prioriteten.

Når du føjer en ny linje til siden **Indstillinger for certifikatprofil**, skal du angive følgende felter:

- **Lokationstype** – Vælg den lokation, hvor certifikatet er gemt. Dette felt har to mulige værdier: **Lokalt certifikat** og **Key Vault**.
- **Key Vault-certifikat** – Dette felt er obligatorisk, hvis du angiver feltet **Lokationstype** til **Key Vault**. Brug det til at angive en Key Vault-certifikathemmelighed.

    > [!NOTE]
    > Før du bruger et Key Vault-certifikat i certifikatprofiler, skal du sørge for at overføre et certifikat til Key Vault-lageret og følge instruktionerne i [Konfigurere Azure Key Vault-klienten](../../finance/localizations/setting-up-azure-key-vault-client.md).

- **Butiksnavn** – Dette felt er valgfrit og er kun tilgængeligt, hvis du angiver feltet **Lokationstype** til **Lokalt certifikat**. Brug det til at angive et standardbutiksnavn, der skal bruges til søgning efter lokale certifikater.
- **Butiksplacering** – Dette felt er valgfrit og er kun tilgængeligt, hvis du angiver feltet **Lokationstype** til **Lokalt certifikat**. Brug det til at angive en standardbutiksplacering, der skal bruges til søgning efter lokale certifikater.

    > [!NOTE]
    > Standardbutiksnavnet og butiksplaceringen tilføjes for at forenkle processen med søgning efter lokale certifikater i Commerce Runtime. X509StoreProvider har en liste over mapper, hvor certifikater gemmes. Hvis standardbutiksnavnet og standardbutiksplaceringen ikke er angivet, forsøger X509StoreProvider at finde et certifikat i de andre mapper på listen.

- **Aftryk** – Dette felt er obligatorisk og er kun tilgængeligt, hvis du angiver feltet **Lokationstype** til **Lokalt certifikat**. Brug det til at angive certifikataftrykket.
- **Kommentarer** – Dette felt er valgfrit, og brugerne kan skrive bemærkninger.

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Arbejdsgang: søge efter certifikater i Commerce Runtime

Her er den grundlæggende arbejdsgang, der bruges til at søge efter et certifikat, når en certifikatprofil kaldes i Commerce Runtime.

1. Systemet identificerer, om certifikatprofilen har firmaspecifikke indstillinger for den aktuelle juridiske enhed.
1. Systemet forsøger at finde certifikatet ved hjælp af værdierne på siden **Indstillinger for certifikatprofil** for den linje, hvor feltet **Prioritet** er angivet til **1**.

    - Hvis feltet **Lokationstype** er angivet til **Key Vault**, bruges værdien af feltet **Key Vault-certifikathemmelighed** til at søge efter certifikatet på siden **Key Vault-parametre**. Der søges efter certifikatet i Key Vault-lageret.
    - Hvis feltet **Lokationstype** er angivet til **Lokalt certifikat**, søger X509StoreProvider først efter certifikatet ved hjælp af standardbutiksnavnet og butiksplaceringen, hvis disse parametre er angivet. Den søger derefter i alle andre mapper på listen over mapper.

1. Hvis certifikatet ikke bliver fundet, gentages processen for den linje, hvor **Prioritet**-feltet er angivet til **2** osv.

> [!NOTE]
> Hvis certifikatprofilen ikke har nogen indstillinger for den aktuelle juridiske enhed, eller hvis certifikatsøgningen mislykkes for alle linjer på siden **Indstillinger for certifikatprofil**, findes certifikatet ikke.

#### <a name="caching-the-results-of-certificate-searches"></a>Cachelagre resultaterne af certifikatsøgninger

Resultaterne af certifikatsøgninger cachelagres. Standardudløbsdatoen for en cache er én time. Denne tid kan dog tilpasses og angives til en maksimumværdi på 24 timer.

### <a name="gradual-update"></a>Gradvis opdatering

Hvis der introduceres en ny version af certifikatet, men det ikke kan opdateres i alle lagre på samme tid, kan du bruge certifikatprofilerne til at opdatere certifikatet gradvist.

1. Find en certifikatprofil og den linje, der skal opdateres, og vælg derefter **Indstillinger**.
1. Tilføj en linje, og angiv indstillinger, der er relateret til den seneste version af certifikatet.
1. Forøg **Prioritet**-værdien for den nye linje. Brug knappen **Flyt op** til at flytte linjen, så den ligger over linjen for den forrige version af det samme certifikat.

> [!NOTE]
> I Commerce Runtime vil den nye version af certifikatet blive kaldt først. Hvis certifikatet endnu ikke er opdateret i en bestemt butik eller på en bestemt terminal, vil den tidligere version blive kaldt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]