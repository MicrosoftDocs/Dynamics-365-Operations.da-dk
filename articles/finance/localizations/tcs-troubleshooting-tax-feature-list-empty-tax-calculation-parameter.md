---
title: Tom momsfunktionsliste i momsberegningsparametre
description: Dette emne forklarer, hvordan du foretager fejlfinding af et problem, hvor listen over momsfunktioner på siden Parametre for momsberegning er tom.
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: ef8158c2ada18e7d132eebbedef559b3f80ab19f
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612283"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>Tom momsfunktionsliste i momsberegningsparametre

[!include [banner](../includes/banner.md)]


## <a name="symptom"></a>Symptom

Du har udgivet en funktion i RCS (Regulatory Configuration Service), så du kan bruge den i Microsoft Dynamics 365 Finance. Mn når du åbner Finance og går til **Moms** \> **Konfiguration** \> **Momskonfiguration** \> **Parametre for momsberegning** og vælger en værdi i feltet **Navn på funktionsopsætning**, så er listen over værdier tom.

## <a name="reason"></a>Årsag

Dette problem opstår normalt, fordi Finance-miljøet og RCS-miljøet ikke er under den samme lejer.

### <a name="rcs-tenant"></a>RCS-lejer

Følg disse trin for at finde id'et for din RCS-lejer.

1. Kopiér hele RCS-URL-adressen. URL-adressen kan f. eks være `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`.
2. Åbn et InPrivate-browservindue, indsæt RCS-URL-adressen på adresselinjen, og vælg derefter **Enter**. Du dirigeres til logonsiden, hvor du kan finde RCS-lejer-id'et. Hvis URL-adressen for logonsiden f.eks. er `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d`, er lejer-id'et de oplysninger, der vises efter `https://login.microsoftonline.com/` eller **d335a570-a05b-4bc5-8eb3-c42c65f9560d**.

### <a name="finance-environment-tenant-id"></a>Lejer-id for dit Finance-miljø

Hvis du vil finde lejer-id'et for dit Finance-miljø, skal du følge de trin, du har fulgt for at finde RCS-lejeren. Kopiér og indsæt dog hele URL-adressen til dit Finance-miljø i stedet for den fulde RCS-URL-adresse.

## <a name="resolution"></a>Løsning

Hvis de to lejer-id'er er forskellige, opstår der et problem, som beskrives i dette emne. Hvis de er ens, er der et ikke-relateret problem. I dette tilfælde anbefales du at kontakte Microsoft Support.

### <a name="solution-1"></a>Løsning 1

Log på RCS-miljøet hos den samme lejer, som Finance-miljøet er logget på. Opret og publicer derefter momsfunktionen.

### <a name="solution-2"></a>Løsning 2

Del momsfunktionen med Finance-lejeren i RCS.

1. Gå i RCS til **Globaliseringsfunktioner** \> **Momsberegning**.
2. Vælg den funktion, du vil dele, og vælg derefter **Del med** under fanen **Organisationer**.
3. Angiv et navn i feltet **Organisationens domænenavn**. Angiv f.eks. **contoso.onmicrosoft.com**.
4. Vælg **Del**.

![Dialogboksen Del med ekstern organisation.](media/ShareTaxFeature.png)
