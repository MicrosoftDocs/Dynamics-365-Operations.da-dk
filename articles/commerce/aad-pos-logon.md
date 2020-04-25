---
title: Aktivér Azure Active Directory-godkendelse til POS-login
description: I dette emne beskrives, hvordan du kan konfigurere logonprocessen for Microsoft Dynamics 365 Commerce POS, så den bruger Azure Active Directory-godkendelse.
author: boycezhu
manager: annbe
ms.date: 03/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: dfc49585434383385b6b993893d93b95ef888384
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248934"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>Aktivér Azure Active Directory-godkendelse til POS-login
[!include [banner](includes/banner.md)]


Mange af de kunder, der bruger Microsoft Dynamics 365 Commerce, bruger også andre Microsoft skytjenester, og de bruger muligvis Azure Active Directory (Azure AD) til at administrere brugerlegitimationsoplysninger til disse tjenester. I disse tilfælde kan kunderne vælge at bruge den samme Azure AD-konto på tværs af programmer. I dette emne beskrives, hvordan du kan konfigurere POS-logonoplevelsen til at bruge Azure AD-godkendelse.

## <a name="configure-azure-ad-authentication"></a>Konfigurere Azure AD-godkendelse

Hvis du vil gøre Azure AD tilgængelig som godkendelsesmetode for POS-login i en butik, skal du konfigurere indstillingerne for butikkens funktionalitetsprofil og derefter anvende denne indstilling på POS-klienter.

Gør følgende for at konfigurere en ny funktionalitetsprofil.

1. Gå til **Retail og Commerce** \> **Konfiguration af kanal** \> **POS-opsætning** \> **POS-profiler** \> **Funktionalitetsprofiler**.
1. Vælg den funktionalitetsprofil, du vil ændre.
1. I oversigtspanelet **Funktioner** i sektionen **POS-medarbejderlogon** skal du ændre værdien i feltet **Logongodkendelse** fra **Personale-id og adgangskode** til **Azure Active Directory**.

Som standard bruger alle funktionalitetsprofiler **Personale-id og adgangskode** som POS-godkendelsesmetode. Du skal derfor ændre værdien i feltet **Logongodkendelsesmetode**, hvis du vil bruge Azure AD. Alle de detailbutikker, der er kædet sammen med den valgte funktionalitetsprofil, påvirkes af ændringen.

Udfør følgende trin for at anvende indstillingerne til POS-klienter.

1. Gå til **Retail og Commerce** \> **Retail og Commerce IT** \> **Distributionsplan**.
1. Kør distributionstidsplanen **1070** (**Kannalkonfiguration**).

> [!NOTE]
> Azure AD-godkendelse kræver en internetforbindelse. Det fungerer ikke, når POS er i offline-tilstand.

## <a name="associate-an-azure-ad-account-with-a-worker"></a>Knytte en Azure AD-konto til en arbejder

Før en butiksmedarbejder kan bruge en Azure AD-konto til at logge på POS-programmet, skal Azure AD-kontoen knyttes til den pågældende medarbejder.

Hvis du vil knytte en Azure AD-konto til en arbejder, skal du følge disse trin.

1. Gå til **Retail og Commerce** \> **Medarbejdere** \> **Arbejdere**.
1. Åbn siden med detaljer til en arbejder.
1. Vælg **Tilknyt eksisterende identitet** i handlingsruden på fanen **Commerce** i gruppen **Eksternt identitet**.
1. Vælg **Søg ved hjælp af mail** i dialogboksen **Brug eksisterende ekstern identitet**, indtast en Azure AD-mailadresse, og vælg derefter **Søg**.
1. Vælg den Azure AD-konto, der returneres, og vælg derefter **OK**.

Felterne **Alias**, **UPN** og **Eksternt under-id** under fanen **Commerce** på siden med detaljer om arbejderen udfyldes.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere udvidet logonfunktionalitet for MPOS og Cloud POS](extended-logon.md)

[Oprette en detailfunktionalitetsprofil](retail-functionality-profile.md)

[ Konfigurere en arbejder](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
