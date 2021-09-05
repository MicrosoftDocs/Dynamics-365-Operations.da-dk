---
title: Konfigurere Azure Active Directory-godkendelse for POS-login
description: Dette emne forklarer, hvordan du kan konfigurere Azure Active Directory som godkendelsesmetode i POS i Microsoft Dynamics 365 Commerce.
author: boycezhu
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 9dfb0389b0ca4b2cf75ccc70f35824674e618055
ms.sourcegitcommit: dca3279a8b7cd5d0bcd4e4a3aa9938b337aa8849
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/19/2021
ms.locfileid: "7402145"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a>Konfigurere Azure Active Directory-godkendelse for POS-login

[!include [banner](includes/banner.md)]

Dette emne forklarer, hvordan du kan konfigurere Azure Active Directory (Azure AD) som godkendelsesmetode i POS i Microsoft Dynamics 365 Commerce.

Detailhandlere, der bruger Dynamics 365 Commerce sammen med andre Microsoft-skytjenester, f.eks. Microsoft Azure, Microsoft 365 og Microsoft Teams, vil typisk bruge Azure AD til centraliseret administration af brugerlegitimationsoplysningerne for at opnå en sikker og problemfri logonoplevelse på tværs af programmer. Hvis du vil bruge Azure AD-godkendelse til Commerce POS, skal du først konfigurere Azure AD som godkendelsesmetoden i Commerce-hovedkvarteret.

## <a name="configure-pos-authentication-method"></a>Konfigurere POS-godkendelsesmetode

Benyt denne fremgangsmåde for at konfigurere POS-godkendelsesmetoden i Commerce-hovedkvarteret.
    
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**, og vælg den funktionalitetsprofil, du vil ændre.
1. Vælg en ønsket godkendelsesmetode på rullelisten **Logongodkendelsesmetode** i sektionen **POS-marbejderlogon** i oversigtspanelet **Funktioner**.

    Der er tre indstillinger for **Logon-godkendelsesmetode**:
    
    - **Personale-id og adgangskode** – Denne standardindstilling kræver, at POS-brugere angiver et personale-id og en adgangskode for at logge på POS og få adgang til funktionaliteten til ledertilsidesættelse.
    - **Azure AD uden enkeltlogon** – Denne indstilling kræver, at POS-brugere bruger Azure AD-legitimationsoplysninger til at logge på POS og få adgang til funktionaliteten til ledertilsidesættelse. Når POS-klienten opdateres eller åbnes igen, skal POS-brugeren angive Azure AD-legitimationsoplysninger for at logge på igen.
    - **Azure AD med enkeltlogon** – Når denne indstilling er valgt, kan POS-brugere logge på Cloud POS (CPOS) ved hjælp af aktive Azure AD-legitimationsoplysninger, der bruges af andre webapplikationer i samme webbrowser, eller logge på Modern POS (MPOS) ved hjælp af Azure AD-legitimationsoplysninger, der er logget på Windows. Begge metoder gør det muligt at logge på uden at skulle angive Azure AD-legitimationsoplysninger på skærmen for POS-logon. Adgangen til funktionaliteten for POS-ledertilsidesættelse kræver dog stadig logon med Azure AD-legitimationsoplysninger.

1. Gå til **Retail og Commerce > Retail og Commerce IT > Distributionsplan**, og kør jobbet **1070 (Kanalkonfiguration)** for at synkronisere funktionalitetens seneste profilindstillinger til POS-klienter.

> [!NOTE]
> - Indstillingen for godkendelsesmetoden **Azure AD uden enkeltlogon** erstatter indstillingen **Azure Active Directory** i Commerce version 10.0.18 og tidligere.
> - Azure AD-godkendelse kræver en aktiv internetforbindelse og vil ikke fungere, når POS er offline.

## <a name="associate-azure-ad-accounts-with-pos-users"></a>Knytte Azure AD-konti til POS-brugere

Hvis du vil bruge Azure AD som POS-godkendelsesmetode, skal du knytte Azure AD-konti til POS-brugere i Commerce-hovedkvarteret. 

Hvis du vil knytte Azure AD-konti til POS-brugere i Commerce-hovedkvarteret, skal du benytte denne fremgangsmåde.
    
1. Gå til **Retail og Commerce > Medarbejdere > Arbejdere**, og åbn en arbejderpost.
1. Vælg fanen **Commerce** i handlingsruden, og vælg derefter **Tilknyt eksisterende identitet** under **Ekstern identitet**. 
1. Vælg **Søg ved hjælp af email** i dialogboksen **Brug eksisterende ekstern identitet**, indtast en Azure AD-emailadresse, og vælg derefter **Søg**.
1. Vælg den Azure AD-konto, der returneres, og vælg derefter **OK**.

Efter konfigurationsmetoden ovenfor, skal du udfylde felterne **Alias**, **UPN** og **Eksternt under-id** under fanen **Commerce** på siden med detaljer om arbejderen.

Du skal køre jobbet **1060 (personale)** i **Retail og Commerce > Retail og Commerce IT > Distributionsplan** for at synkronisere den seneste POS-bruger og Azure AD-kontodata til kanalen.

> [!NOTE]
> Efter du har opdateret arbejderoplysninger som f.eks. adgangskode, POS-tilladelse, tilknyttet Azure AD-konto eller medarbejderadressekartotek i Commerce-hovedkvarteret, anbefales det som bedste praksis at køre jobbet **1060 (personale)** for at synkronisere de seneste arbejderoplysninger med kanalen. POS-klienten kan derefter hente de korrekte data til brugergodkendelse og godkendelseskontroller.

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a>Låse kasseapparat for POS og logge af med Azure AD-godkendelse

Følgende sker, når POS er konfigureret til at bruge Azure AD-godkendelsesmetoden:

- Funktionen **Lås kasseapparat** er ikke tilgængelig i POS-applikationen. 
- Funktionen **Lås automatisk** fungerer på samme måde som funktionen **Log af automatisk**.
- Hvis POS-brugeren vælger **Log af**, vil brugeren blive bedt om at logge på med Azure AD-legitimationsoplysninger, næste gang POS starter, uanset om enkeltlogon er aktiveret.

## <a name="manager-override-functionality-with-azure-ad-authentication"></a>Funktionaliteten til ledertilsidesættelse med Azure AD-godkendelse

Når POS er konfigureret til at bruge Azure AD-godkendelse, åbner funktionaliteten til ledertilsidesættelse en dialogboks, hvor brugeren bliver bedt om at angive lederens Azure AD-legitimationsoplysninger. Når lederens logon er godkendt, fjernes lederens Azure AD-legitimationsoplysninger, og den forrige brugers Azure AD-legitimationsoplysninger anvendes til efterfølgende POS-handlinger.

> [!NOTE]
> - I Commerce-versionerne 10.0.18 og tidligere understøtter lederens tilsidesættelsesfunktion ikke Azure AD. Der kræves en medarbejders id og adgangskode, selvom POS er konfigureret som Azure AD-godkendelsesmetode.
> - Når du bruger CPOS med Safari-webbrowseren på en Apple iOS-enhed, skal du først deaktivere **Bloker popup-vinduer** i Safari-indstillingerne for funktionaliteten til ledertilsidesættelse, før du kan arbejde med Azure AD-godkendelse. 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a>Bedste sikkerhedspraksis for Azure AD-baseret POS-godkendelse på delte enheder

Mange detailhandlende konfigurerer deres detailbutiksmiljø på en måde, så flere brugere har brug for at få adgang til POS-applikationen fra en delt fysisk enhed. I denne sammenhæng giver enkeltlogon en praktisk og problemfri godkendelsesoplevelse, kan den også oprette et sikkerhedshul, hvor den aktuelle POS-bruger muligvis ikke kan se, at en anden brugers legitimationsoplysninger anvendes til at udføre transaktioner eller handlinger i POS. Før du konfigurerer POS til at bruge Azure AD-godkendelsesmetoden, anbefales det at gennemse sikkerhedspolitikken og logonindstillingerne for den delte enhed for at bestemme, hvilken indstilling der er bedst egnet.

- Hvis der bruges en delt konto i dit detailmiljø (f.eks. en lokal konto) til logon på en fysisk enhed, anbefales det, at du bruger indstillingen **Azure AD uden enkeltlogon**. Dette sikrer, at den enkelte POS-bruger udtrykkeligt angiver Azure AD-legitimationsoplysninger for at logge på POS.
- Hvis detailmiljøet kræver, at medarbejdere bruger deres egne Azure AD-konti til at logge på POS og dets fysiske hostingenhed, anbefales det, at du bruger indstillingen **Azure AD med med enkeltlogon**.

## <a name="additional-resources"></a>Yderligere ressourcer

[ Konfigurere en arbejder](tasks/worker.md)

[Oprette en detailfunktionalitetsprofil](retail-functionality-profile.md)


[Konfigurere udvidet logonfunktionalitet for MPOS og Cloud POS](extended-logon.md)

[Bedste sikkerhedspraksis for Cloud POS i delte miljøer](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
