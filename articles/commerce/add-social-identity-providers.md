---
title: Tilføj sociale identitetsudbydere
description: Denne artikel beskriver, hvordan du tilføjer leverandører af social identitet i Microsoft Azure-portalen.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785222"
---
# <a name="add-social-identity-providers"></a>Tilføj sociale identitetsudbydere

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du tilføjer leverandører af social identitet i Microsoft Azure-portalen.

Sociale identitetsudbydere giver brugerne mulighed for at bruge deres sociale konti til godkendelse. Tilføjelse af godkendelse af sociale identitetsudbydere er valgfri i Dynamics 365 Commerce. 

Hvis godkendelse af sociale identitetsudbydere ikke tilføjes, vil Azure Active Directory (Azure AD) B2C-standardprofilerne være hovedprofilerne til din brugerbase. Brugerne vælger deres eget brugernavn (deres foretrukne mailadresse) og angiver en adgangskode. Azure AD B2C vil godkende brugere direkte. 

Hvis godkendelse af sociale identitetsudbydere er tilføjet, og en bruger vælger en af de tilbudte sociale identitetsudbydere, oprettes der stadig en enhed i Azure AD B2C-lejeren. Azure AD B2C godkender derefter brugerens legitimationsoplysninger via den sociale identitetsudbyder.

> [!NOTE]
> Identitetsudbyderens login opretter en post i B2C-lejeren, men i et andet format end lokale konti, da det kalder den eksterne sociale identitetsudbyders reference for godkendelse. Brugeren kan bruge den samme mailadresse på tværs af sociale identitetsudbydere, hvilket betyder, at det brugernavn, der bruges til godkendelse af mailadressen, ikke er entydigt for lejeren. Azure AD B2C vil kun gennemtvinge, at brugere har en entydig mailadresse på lokale B2C-konti.

Før du kan tilføje en social identitetsudbyder til godkendelse, skal du gå til portalen for identitetsudbyderen og konfigurere et identitetsudbyderprogram som angivet i dokumentationen til Azure AD B2C. Der findes en liste over links til dokumentationen nedenfor.

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Enkelt lejer)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft-konto](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Tilføje og konfigurere en sociale identitetsudbyder

> [!NOTE]
> Det er valgfrit at tilføje leverandører af social identitet, når du konfigurerer en B2C-lejer Microsoft Dynamics 365 Commerce.

Udfør følgende trin for at tilføje og konfigurere en social identitetsudbyder.  

1. Naviger til **Identitetsudbydere** i Azure-portalen.
1. Vælg **Tilføj**. Skærmbilledet **Tilføj identitetsudbyder** vises.
1. Angiv det navn, der skal vises for brugere på din logonskærm, under **Navn**.
1. Vælg en identitetsudbyder på listen under **Type identitetsudbyder**.
1. Vælg **OK**.
1. Vælg **Konfigurer denne identitetsudbyder** for at få adgang til skærmbilledet **Konfigurer den sociale identitetsudbyder** .
1. Angiv det klient-id, der er hentet fra installationsprogrammet til identitetsudbyderen, under **Klient-id**.
1. Angiv den klienthemmelighed, der er hentet fra installationsprogrammet til identitetsudbyderen, under **Klienthemmelighed**.
1. Knyt brugerflow til tilmeldings- og logonpolitikker:
1. Gå til **Azure AD B2C – Brugerstrømme (politikker) \> {din tilmeldings- og logon-politik} \> Identitetsudbydere**.
1. Hvis du vil knytte brugerflowet til logon-/tilmeldingspolitikken, skal du vælge hver af de identitetsudbydere, du har konfigureret til din konto. Hvis du vil teste disse flows, skal du vælge **Kør brugerstrøm** for hver identitetsudbyder. Login-siden vises på en ny fane, og der vises et valgfelt til den nye identitetsudbyder.

I følgende billede vises eksempler på skærmbillederne **Tilføj identitetsudbyder** og **Konfigurerer sociale identitetsudbydere** i Azure AD B2C.

![Føje en social identitetsudbyder til dit program.](./media/B2CImage_14.png)

I følgende billede vises et eksempel på, hvordan du kan vælge identitetsudbydere på siden Azure AD B2C **Identitetsudbydere**.

![Vælg alle de sociale identitetsudbydere, der skal aktiveres for din politik.](./media/B2CImage_16.png)

I følgende billede vises et eksempel på en standardlogin-skærm, hvor der vises en knap til login på en social identitetsudbyder.

> [!NOTE]
> Hvis du benytter de brugerdefinerede sider, der er indbygget Commerce, til dine brugerflow, skal knapperne for leverandører af social identitet tilføjes ved hjælp af funktionerne til udvidelse af Commerce-modulbiblioteket. Når du konfigurerer dine programmer med en bestemt social identitetsudbyder, skal der i URL-adresser eller konfigurationsstrenge i nogle tilfælde skelnes mellem små og store bogstaver. Yderligere oplysninger finder du i din sociale identitetsudbyders forbindelsesinstruktioner.
 
![Eksempel på standardlogin-skærm med knap til login til social identitetsudbyder.](./media/B2CImage_17.png)

## <a name="next-steps"></a>Næste trin

Hvis du vil fortsætte med at konfigurere en B2C-lejer i Commerce, [skal du fortsætte til Update Commerce Headquarters med de nye Azure AD B2C-oplysninger](update-hq-aad-b2c-info.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere en B2C-lejer i Commerce](set-up-b2c-tenant.md)

[Oprette eller sammenkæde med en eksisterende Azure AD B2C-lejer i Azure-portalen](create-link-aad-b2c-tenant.md)

[Opret B2C-programmet](create-b2c-app.md)

[Oprette politikker for brugerstrøm](create-user-flow-policies.md)

[Opdater Commerce Headquarters med de nye Azure AD B2C-oplysninger](update-hq-aad-b2c-info.md)

[Konfigurere din B2C-lejer i Commerce-webstedsgeneratoren](config-b2c-tenant-site-builder.md)

[Flere B2C-oplysninger](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
