---
title: Administrere B2B-forretningspartnere ved hjælp af kundehierarkier
description: Denne artikel beskriver, hvordan du bruger kundehierarkier til at administrere forretningspartnere for Microsoft Dynamics 365 Commerce business-to-business (B2B)-e-handelswebsteder.
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ddd02045b5df3ce20160a4feaa23339475823d3d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864975"
---
# <a name="manage-b2b-business-partners-using-customer-hierarchies"></a>Administrere B2B-forretningspartnere ved hjælp af kundehierarkier

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du bruger kundehierarkier til at administrere forretningspartnere for Microsoft Dynamics 365 Commerce business-to-business (B2B)-e-handelswebsteder.

I Commerce Headquarters bruges en *kundehierarkienhed* til at repræsentere de forretningspartnerorganisationer, der skal bruge dit B2B-e-handelswebsted. Før du kan begynde at bruge kundehierarkier til at administrere forretningspartnere, skal du aktivere funktionerne for B2B-e-handel i Commerce Headquarters og derefter definere en nummerserie til kundehierarkiet.

## <a name="enable-the-b2b-e-commerce-feature-in-commerce-headquarters"></a>Aktivere funktionen til B2B-e-handel i Commerce Headquarters

Hvis du vil bruge egenskaberne for B2B-e-handel, skal du først aktivere funktionen **Aktivér brugen af eCommerce-egenskaber** i Commerce Headquarters.

1. Gå til **Arbejdsområder \> Funktionsstyring**.
1. Brug filterfeltet til at søge efter **Modul: Retail og Commerce** under fanen **Alle** .
1. Find og vælg funktionen **Aktivér brugen af B2B-eCommerce-egenskaber**, og vælg derefter **Aktivér nu** nederst til højre.

## <a name="define-a-number-sequence-for-the-customer-hierarchy"></a>Definere en nummerserie til kundehierarkiet

Talserier bruges til generering af læselige, entydige identifikatorer for masterdataposter og transaktionsposter, der kræver identifikatorer. Du skal definere en nummerserie, der skal bruges til at generere id'et for kundehierarkiet. Du kan finde flere oplysninger om nummerserier i [Oversigt over nummerserier](/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Følg disse trin for at definere en nummerserie for kundehierarkiet i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Headquarters-opsætning \> Nummerserier \> Nummerserier**.
1. Opret en ny nummerserie, eller vælg en eksisterende nummerserie for at genbruge den.
1. Gå til **Retail og Commerce \> Konfiguration af Headquarters \> Parametre \> Delte Commerce-parametre**.
1. Under fanen **Nummerserier** skal du føje den nummerserie, du oprettede eller har valgt tidligere, til referencen for **Kundehierarki-id**.

![Nummerserie, der er føjet til referencen for kundehierarki-id'et.](../media/NumberSequenceCustHierarchy.png)

## <a name="how-the-approval-process-works"></a>Sådan fungerer godkendelsesprocessen

Når en forretningspartner anmoder om at deltage i et B2B-e-handelswebsted, gemmer systemet anmodningen som et *kundeemne*. En person i Commerce Headquarters som f.eks. en detaildriftschef kan godkende eller afvise partneranmodninger. Du kan finde flere oplysninger om, hvordan du administrerer forretningspartneranmodninger og godkendelse af kundeemner, i [Administrere forretningspartnerbrugere på B2B-e-handelswebsteder](manage-b2b-users.md).

Når et kundeemne er godkendt, opretter systemet to nye kundeposter:

- En kundepost af typen **Organisation** repræsenterer den organisation, der anmoder om at blive forretningspartner.
- En kundepost af typen **Person** repræsenterer den person, der har sendt anmodningen.

Desuden oprettes der en ny post for kundehierarki i **Retail og Commerce \> Kunder \> Kundehierarkier**. Denne kundehierarkipost har følgende overskriftsegenskaber:

- **Kundehierarki-id** – Det entydige id for kundehierarkiet. Dette id bruger den nummerserie, du har defineret i Delte parametre for Commerce.
- **Navn** – Forretningspartnerens organisationsnavn, som det er angivet i anmodningen om onboarding. Dette felt kan redigeres.
- **Formål** – Denne egenskab er angivet til den foruddefinerede værdi **B2B-organisation**.
- **Organisation** – Forretningspartnerorganisationens kunde-id.

Den person, der har sendt anmodningen om onboarding, tilføjes i oversigtspanelet **Hierarki**, og rollen **Administrator** er tildelt til dem. Når administratoren tilføjer flere brugere, føjes til forretningspartnerorganisationen på et B2B-websted, oprettes der en ny kundepost for hver bruger. Denne kundepost føjes også til den relevante kundehierarkipost for forretningspartneren og har fået tildelt rollen som **Bruger**.

### <a name="examples"></a>Eksempler

En person, der hedder Sam J. sender en anmodning om onboarding på vegne af Microsoft-organisationen. Når anmodningen er godkendt, oprettes der to nye kundekonti: en af typen **Person** for Sam J. og en af **Organisation**-typen for Microsoft.

Som eksemplet i følgende illustration viser, oprettes der også en ny post for kundehierarkiet. Denne post har samme navn som organisationen (**Microsoft**), og rollen **Administrator** er tildelt Sam J. Som administrator føjer Sam J. alle andre Microsoft-brugere på B2B-webstedet til dette hierarki og tildeler **Bruger** til dem. I dette eksempel er Sush R. blevet tilføjet som bruger.

![Eksempel på et kundehierarkipost.](../media/CustomerHierarchy2.png)

Når du skal afgøre, om en kunde er knyttet til et kundehierarki, skal du åbne kundeposten. Som eksemplet i følgende illustration viser feltet **Kundehierarki-id** i sektionen **B2B** i oversigtspanelet **Detail**, om kunden er en del af et kundehierarki, og indstillingen **B2B-administrator** angiver, om kunden er administrator af dette hierarki.

![Eksempel på sektionen B2B i oversigtspanelet Detail for en kundepost, hvor kunden er tilknyttet et hierarki og angivet som administrator.](../media/CustomerHierarchyMapping2.png)

I de fleste tilfælde skal egenskabsværdierne for alle kundeposter i et hierarki være ens. Da alle forretningspartnerbrugere f.eks. skal få ens priser for produkter, skal deres prisgruppe og tilknyttede konfigurationer stemmer overens. Systemet gennemtvinger dog ikke denne konsistens. De relevante brugere i handelshovedkvarteret er derfor ansvarlige for at sikre, at egenskabsværdierne og -konfigurationerne er ens for alle debitorer i et bestemt hierarki.

Brugere i Commerce Headquarters kan inspicere egenskabsværdierne for alle kundeposter i hierarkiet ved siden af hinanden. Som eksemplet i følgende illustration viser, kan du bruge indstillingen **Generelt** på rullelisten i oversigtspanelet **Hierarki** og derefter vælge et afsnit i kundeposten for at se de relaterede egenskaber. Brugerne kan redigere egenskabsværdierne direkte i denne visning. Hvis du vil kopiere alle værdierne fra en administratorkundepost til alle brugere, skal du vælge **Tilsidesæt** i oversigtspanelet **Hierarki**.

![Eksempel på en kundehierarkipost med knappen Tilsidesæt og indstillingen på rullelisten.](../media/HierarchyDetails2.png)

[!include [footer-include](../../includes/footer-banner.md)]
