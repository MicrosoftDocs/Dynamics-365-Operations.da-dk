---
title: Oprette nye brugere
description: Brugerne er interne medarbejdere i din organisation, eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 480d181e8abb3af5a7406efd13c8bd9961a7490a
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595380"
---
# <a name="create-new-users"></a>Oprette nye brugere

[!include [banner](../../includes/banner.md)]

Før du kan få adgang til Finance and Operations-apps, skal du først føjes til siden **Brugere** (**Systemadministration \> Brugere \> Brugere**). Brugere omfatter interne medarbejdere i din organisation eller eksterne kunder og leverandører. Brugere kan importeres eller tilføjes manuelt. Alle brugere skal have korrekt licens for at få kompatibel brug.

Du kan finde flere oplysninger om, hvordan du køber og får licens til Finance and Operations-apps, i [licensvejledningen til Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).

## <a name="assign-a-license-to-a-user"></a>Tildele en bruger licens
Systemadministratorer kan [tildele licenser til brugere](/office365/admin/subscriptions-and-billing/assign-licenses-to-users) i [Microsoft 365 Administration](/office365/admin/admin-overview/about-the-admin-center).

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>Tilføje en ekstern bruger i Azure AD og tildele en licens 
Eksterne brugere skal være repræsenteret i dit lejerbibliotek (Azure Active Directory (Azure AD)), så de kan tildeles licenser. Disse eksterne brugere skal føjes til lejeren i Azure AD som gæstebrugere og derefter tildeles de relevante licenser. Et krav til Finance and Operations-apps er, at gæstebrugerens firma skal bruge Azure AD. Du kan finde flere oplysninger under [Tilføje Azure Active Directory B2B-samarbejdsbrugere i Azure-portalen](/azure/active-directory/b2b/add-users-administrator).

## <a name="import-new-users-from-azure-ad"></a>Importere nye brugere fra Azure AD 
1. Gå til **Systemadministration** \> **Bruger** \> **Brugere**.
2. Vælg **Importer brugere** i handlingsruden.
3. Vælg de brugere, der skal importeres. Listen indeholder Azure AD-brugere, der aktuelt ikke er brugere i dette miljø.
4. Vælg **Importer brugere**.
5. Vælg **Luk**.

> [!NOTE]
> Værdien af feltet **Firma** angives på basis af det aktuelle sessionsfirma for administratoren. Efter importen skal du tildele roller og organisationer efter behov. Du kan finde flere oplysninger under [Tildele brugere til sikkerhedsroller](assign-users-security-roles.md). Det kan også være nødvendigt at knytte brugeren til en **Person** og opdatere brugerindstillinger som f.eks. sprog.

## <a name="manually-add-a-new-user"></a>Tilføje en ny bruger manuelt
1. Gå til **Systemadministration** \> **Brugere** \> **Brugere**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Angiv et entydigt id for brugeren i feltet **Bruger-id**.   
4. Angiv brugerens navn i feltet **Brugernavn**.  
5. I feltet **Udbyder**:
 - Brug standardværdien til interne brugere. Din Azure AD-lejer har f.eks. præfikset https://sts.windows.net/.  
 - For ikke-Azure AD-brugere, f.eks. Service-2-Service-konti, skal du angive en grundlæggende tekstværdi. For eksempel Ikke relevant. Denne værdi hjælper med at undgå forkerte godkendelseskald, der kan resultere i fejl, hvis der bruges en gyldig værdi for identitetsudbyderen.  
 - For eksterne brugere eller gæstebrugere skal du tilføje deres Azure AD-lejernavn efter https://sts.windows.net/.
6. I feltet **Mail** skal du angive brugerens fulde mail/hovednavn.  
7. Vælg standardstartfirmaet for brugeren i feltet **Firma**. 
8. Vælg **Gem**.

Værdierne for Identitetsudbyder og Telemetri-id opdateres baseret på et [Microsoft-grafkald](/graph/overview), når brugerposten gemmes. Telemetri-id'et er baseret på brugerens objekt-id/sikkerheds-id (SID) i Azure AD.

> [!NOTE]
> Når du har tilføjet en bruger, skal du tildele roller og organisationer efter behov. Du kan finde flere oplysninger under [Tildele brugere til sikkerhedsroller](assign-users-security-roles.md). Det kan også være nødvendigt at knytte brugeren til en **Person** og opdatere **Brugerindstillinger** som f.eks. sprog.

## <a name="change-a-user-id"></a>Ændre et bruger-id
Hvis du vil ændre et bruger-id, skal du omdøbe nøglen i databasen. Når du ændrer et bruger-id ved hjælp af denne procedure, ændres alle relaterede brugerindstillinger, så de bruger det nye bruger-id. Brugsoplysningerne i tabellen **SysLastValue** opdateres f.eks. til at referere til det nye bruger-id.

> [!NOTE]
> Bruger-id'et er primærnøglen i tabellen med brugeroplysninger. Det kan tage et stykke tid at omdøbe primærnøglen for eksisterende brugere, da alle referencer til nøglen også opdateres i databasen. 

1. Gå til **Systemadministration \> Brugere \> Brugere**.
2. Vælg en bruger på listen, og vælg **Indstillinger\> Postoplysninger**.
3. Vælg **Omdøb**.
4. Angiv en ny og entydig værdi af bruger-id, og vælg derefter **OK**. 
5. Vælg **Ja** for at bekræfte.

## <a name="additional-resources"></a>Yderligere ressourcer

Du kan finde flere indstillinger til implementering af B2B-brugere i [Eksportere B2B-brugere til Azure AD](../implement-b2b.md).

Du kan finde oplysninger om forudkonfigurerede systemkonti i [Forudkonfigurerede systemkonti](../pre-configured-system-accounts.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]