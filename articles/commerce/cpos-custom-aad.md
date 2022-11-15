---
title: Konfigurere CPOS til en brugerdefineret Azure AD-app
description: Denne artikel forklarer, hvordan du konfigurerer CPOS (Cloud POS) til en brugerdefineret Azure Active Directory-app (Azure AD).
author: boycez
ms.date: 11/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 5e4ff797410e1e94869cc37684e7622ec0d97842
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746254"
---
# <a name="configure-cpos-to-use-a-custom-azure-ad-app"></a>Konfigurere CPOS til en brugerdefineret Azure AD-app

[!include [banner](includes/banner.md)]

CPOS (Cloud POS) peger i Microsoft Dynamics 365 Commerce som standard på en registreret Microsoft-førstepartsapp i Azure Active Directory (Azure AD). Du kan derfor bruge CPOS uden at skulle foretage nogen ændringer i Azure AD. Det kan dog være en god ide at pege din forekomst af CPOS til en brugerdefineret Azure AD-app, som du styrer. Denne artikel forklarer, hvordan du konfigurerer CPOS til en brugerdefineret Azure AD-app.

## <a name="set-up-a-custom-retail-server-app-in-azure-ad"></a>Konfigurere en brugerdefineret Retail Server-app i Azure AD

Hvis du vil oprette og konfigurere en brugerdefineret Retail Server-app i Azure AD, skal du følge disse trin.

1. Log på [Azure Active Directory Administration](https://aad.portal.azure.com) med den relevante Azure AD-brugerkonto. Brugerkontoen behøver ikke at have administratorrettigheder.
1. Vælg **Azure Active Directory**.
1. Vælg **Appregistreringer**, og vælg derefter **Ny registrering** for at åbne dialogboksen **Registrer et program**.
1. Angiv følgende felter:

    - **Navn** – Angiv et brugerdefineret navn til appen. Du kan f.eks. angive **Brugerdefineret Retail Server**.
    - **Understøttede kontotyper** – Vælg standardindstillingen, **Konti kun i denne organisationsmappe (kun Microsoft - enkelt lejer)**.
    - **Omdirigerings-URI** – Dette felt er valgfrit. Lad feltet stå tomt.
    - **Tjenestetræ-id** – Dette felt er valgfrit. Lad feltet stå tomt.
    
1. Vælg **Registrer**. Konfigurationssiden for den nyregistrerede app vises.
1. I afsnittet **Oversigt \> Essentials** skal du vælge **Tilføj en URI for applikations-id** og derefter vælge **Indstil** ud for **URI for applikations-id**. Notér dig den foreslåede værdi, og vælg derefter **Gem** for at acceptere denne værdi. 
1. Vælg **Tilføj et område**, og angiv derefter følgende felter:

    - **Områdenavn** – Angiv et brugerdefineret navn til området. Du kan f.eks. skrive **Gammel.Adgang.Fuld**.
    - **Hvem kan give samtykke** – Angiv, om både administratorer og brugere eller kun administratorer kan give deres samtykke baseret på din organisations sikkerhedspolitikker.
    - **Vist navn for administratorsamtykke** – Angiv et vist navn. Du kan f.eks. angive **Adgang til Retail Server**.
    - **Beskrivelse af administratorsamtykke** – Indtast en beskrivelse. Du kan f.eks. angive **Giv adgang til Retail Server-API'er**.

1. Vælg **Tilføj område** for at fuldføre oprettelsen af området.

## <a name="set-up-a-custom-cpos-app-in-azure-ad"></a>Konfigurere en brugerdefineret CPOS-app i Azure AD

> [!IMPORTANT]
> Hvis du opgraderer en eksisterende brugerdefineret CPOS Azure AD-app, der blev oprettet før Commerce version 10.0.21, skal du følge trinnene i [Opgradere en eksisterende brugerdefineret CPOS Azure AD-app , der er oprettet før Commerce version 10.0.21](#upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021).

Hvis du vil oprette og konfigurere en brugerdefineret CPOS-app i Azure AD, skal du følge disse trin.

1. Log på [Azure Active Directory Administration](https://aad.portal.azure.com) med den relevante Azure AD-brugerkonto. Brugerkontoen behøver ikke at have administratorrettigheder.
1. Vælg **Azure Active Directory**.
1. Vælg **Appregistreringer**, og vælg derefter **Ny registrering** for at åbne dialogboksen **Registrer et program**.
1. Angiv følgende felter:

    - **Navn** – Angiv et navn til appen. Angiv f.eks. **Egen Cloud POS**.
    - **Understøttede kontotyper** – Vælg standardindstillingen, **Konti kun i denne organisationsmappe (kun Microsoft - enkelt lejer)**.
    - **Omdirigerings-URI** – Vælg **Enkeltsidet ansøgning (SPA)** på rullelisten, og angiv derefter din CPOS-URI.
    - **Tjenestetræ-id** – Dette felt er valgfrit. Lad feltet stå tomt.

1. Vælg **Registrer**. Konfigurationssiden for den nyregistrerede app vises.
1. Angiv parametrene **oauth2AllowIdTokenImplicitFlow** og **oauth2AllowImplicitFlow** til **true** i afsnittet **Manifest**, og vælg derefter **Gem**.
1. I afsnittet **Tokenkonfiguration** skal du benytte følgende fremgangsmåde for at tilføje to krav:

    1. Vælg **Tilføj valgfrit krav**. Indstil feltet **Tokentype** til **id**, og vælg derefter kravet **sid**. Vælg **Tilføj**.
    1. Vælg **Tilføj valgfrit krav**. Indstil feltet **Tokentype** til **Adgang**, og vælg derefter kravet **sid**. Vælg **Tilføj**.

1. Vælg **Tilføj en rettighed** under **API-rettigheder**.
1. Under fanen **API'er, som min organisation bruger**, skal du søge efter den Retail Server-app, du har oprettet i afsnittet [Konfigurere en brugerdefineret Retail Server-app i Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad). Vælg derefter **Tilføj tilladelser**.
1. I afsnittet **Oversigt** skal du notere værdien i feltet **Program-id (klient-id)**.

### <a name="upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021"></a>Opgradere en eksisterende brugerdefineret CPOS Azure AD-app, der er oprettet før Commerce version 10.0.21

Følg disse trin for at opgradere en eksisterende brugerdefineret CPOS Azure AD-app, der er oprettet før Commerce version 10.0.21. 

1. Åbn din brugerdefinerede CPOS Azure AD-app i Azure-portalen.
1. Vælg fanen **Godkendelse**.
1. Kopiér og gem den oprindelige omdirigerings-URI fra **Web**-typen til brug senere, og slet den derefter.
1. Vælg **Tilføj en platform**, og vælg derefter **Enkeltsidet ansøgning (SPA)**.
1. Tilføj den oprindelige webomdirigerings-URI, der er kopieret ovenfor, til SPA-platformen.
1. I afsnittet **Tokenkonfiguration** skal du benytte følgende fremgangsmåde for at tilføje to krav:
    1. Vælg **Tilføj valgfrit krav**. Indstil feltet **Tokentype** til **id**, og vælg derefter kravet **sid**. Vælg **Tilføj**.
    1. Vælg **Tilføj valgfrit krav**. Indstil feltet **Tokentype** til **Adgang**, og vælg derefter kravet **sid**. Vælg **Tilføj**.

## <a name="update-the-cpos-configuration-file"></a>Opdatere CPOS-konfigurationsfilen

Åbn CPOS config.json-filen, og foretag følgende opdateringer i den.

1. Erstat nøgleværdien **AADClientId** med værdien for **Applikations-id' (klient)** til den brugerdefinerede CPOS-app, som du oprettede i afsnittet [Konfigurere en brugerdefineret CPOS-app i Azure AD](#set-up-a-custom-cpos-app-in-azure-ad).
1. Erstat nøgleværdien **AADRetailServerResourceId** med værdien for **Applikations-id-URI** til den brugerdefinerede Retail Server-app, som du oprettede i afsnittet [Konfigurere en brugerdefineret Retail Server-app i Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad).

CPOS bruger begge parametre, når der sendes anmodninger til Azure AD om at anskaffe et sikkerhedstoken.

## <a name="update-identity-providers-settings-in-commerce-headquarters"></a>Opdatere indstillinger for identitetsudbydere i Commerce headquarters

Nu skal du opdatere indstillinger for identitetsudbydere i Commerce headquarters.

1. I Commerce headquarters skal du åbne siden **Delte parametre til handel**.
1. Under fanen **Identitetsudbydere** skal du i afsnittet **Identitetsudbydere** vælge den række, hvor feltet **Type** er angivet til **Azure Active Directory**, og **Udsteder**-feltet peger på din Azure AD-lejer. Denne indstilling angiver, at du vil arbejde med underordnede gitre, der indeholder de data, der er relateret til den identitetsudbyder, der svarer til din Azure AD-lejer.
1. Vælg **Tilføj** i sektionen **Afhængige parter** for at tilføje en række.
1. Angiv følgende felter:

    - **ClientId** – Angiv værdien for **Applikations-id (klient)** til den brugerdefinerede CPOS-app, som du oprettede i afsnittet [Konfigurere en brugerdefineret CPOS-app i Azure AD](#set-up-a-custom-cpos-app-in-azure-ad).
    - **Type** – Vælg **Offentlig**.
    - **UserType** – Vælg **Arbejder**.

1. Vælg den række, du har tilføjet. Afsnittet **Serverressource-id'er** under sektionen **Afhængige parter** viser de Retail Server-app-id'er, der kan åbnes af den app, du har valgt i gitteret **Afhængige parter**.
1. Vælg **Tilføj** i sektionen **Serverressource-id'er** for at tilføje en række.
1. Indtast værdien for **Applikations-id-URI** i feltet **Serverressource-id** til den brugerdefinerede Retail Server-app, som du oprettede i afsnittet [Konfigurere en brugerdefineret Retail Server-app i Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad).

    > [!IMPORTANT]
    > Der bruges store og små bogstaver i alle de felter, der nævnes i de foregående trin. De værdier, du angiver, skal svare præcist til de værdier, der er konfigureret i Azure AD-administrationen.

1. Gå derefter til **Detail- og handels-it \> Distributionsplan**, og kør job **1110** (**Global konfiguration**).

Du kan nu aktivere CPOS-enheder ved hjælp af din egen Azure AD-app.

## <a name="additional-resources"></a>Yderligere ressourcer

[Aktivering af POS-enhed](dev-itpro/retail-device-activation.md)

[Administrere aktiveringskonti og validere enheder](set-up-activation-accounts-validate-devices-hq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
