---
title: Administrere e-handelsbrugere og -roller
description: Denne artikel beskriver, hvordan du giver brugere adgang til oprettelsesmiljøet for dit Microsoft Dynamics 365 Commerce-websted.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 180fc5c0a9c9e247d5bd6ec7f469f313463526df
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279496"
---
# <a name="manage-e-commerce-users-and-roles"></a>Administrere e-handelsbrugere og -roller


[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du giver brugere adgang til oprettelsesmiljøet for dit Microsoft Dynamics 365 Commerce-websted.

Som en hjælp til at styre brugeradgang og tildele brugerrettigheder til at udføre bestemte opgaver, bruger miljøet til webstedsoprettelse sikkerhedsgrupper, som du opretter i Microsoft Azure Active Directory (Azure AD). Du skal først tildele en ny eller eksisterende sikkerhedsgruppe fra Azure AD til hver rolle i oprettelsesmiljøet. Derefter kan du tildele eller tilbagekalde individuelle brugeres rettigheder ved enten at føje disse brugere til en relevant sikkerhedsgruppe eller ved at fjerne dem fra en sikkerhedsgruppe.

## <a name="overview-of-roles-in-the-authoring-environment"></a>Oversigt over roller i oprettelsesmiljøet

Dynamics 365 for Commerce-oprettelsesmiljøet understøtter følgende roller.

| Rolle                 | Beskrivelse |
|----------------------|-------------|
| Systemadministrator | Brugere, der har denne rolle, har alle rettigheder til alle værktøjer og til alle vurderinger og anmeldelser. De kan også oprette websteder. |
| Administrator   | Brugere, der har denne rolle, har alle rettigheder til alle værktøjer og RnR i en bestemt webstedsstruktur. |
| Webproducent         | Brugere, der har denne rolle, kan oprette sider, fragmenter og skabeloner, overføre og administrere aktiver og forbedre produkter og kategorier. |
| Læser               | Brugere, der har denne rolle, kan få vist sider, skabeloner, aktiver, fragmenter, layout og indstillinger, men kan muligvis ikke foretage ændringer. |
| RnR-redaktør        | Brugere, der har denne rolle, kan moderere produktanmeldelser. |

## <a name="system-administrator-role"></a>Systemadministratorrolle

Når du klargør Dynamics 365 Commerce i Microsoft Dynamics Lifecycle Services-miljøet (LCS), bliver du bedt om at angive en sikkerhedsgruppe for rollen **Systemadministrator**. Denne rolle anvendes derefter automatisk på alle de websteder, du opretter i det miljø, du konfigurerer. Sikkerhedsgruppen for denne rolle kan kun opdateres i LCS. På siden **Webstedsadministration** for alle websteder vises den som skrivebeskyttet og er kun til orientering.

## <a name="administrator-role"></a>Administratorrolle

Når du opretter et nyt websted i Commerce, bliver du bedt om at angive en sikkerhedsgruppe for **Administrator**-rollen. Se tabellen tidligere i denne artikel for at få en oversigt over de rettigheder, som denne rolle giver.

## <a name="add-or-update-security-groups"></a>Tilføje eller opdatere sikkerhedsgrupper

Når webstedet er oprettet, er det kun brugere, der er i sikkerhedsgrupper, som er tilknyttet rollerne **Systemadministrator** og **Administrator**, der har adgang til oprettelsesmiljøet for det pågældende websted. Hvis du vil tildele brugere rollerne **Webproducent**, **RnR-redaktør** og **Læser**, skal du tildele sikkerhedsgrupper til disse roller. Hvis du vil føje en sikkerhedsgruppe til en rolle eller opdatere en sikkerhedsgruppe, der aktuelt er tildelt en rolle, skal du følge disse trin.

1. Gå til det websted, du vil opdatere.
1. Åbn siden **Sikkerhed** i **Administration af websted**.
1. Vælg den rolle, der skal redigeres.
1. Føj sikkerhedsgrupper til roller, eller fjern sikkerhedsgrupper fra roller.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)

[Overvejelser om optimering af søgeprogram (SEO) for webstedet](search-engine-optimization-considerations.md)

[Administrere sikkerhedspolitik for indhold (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
