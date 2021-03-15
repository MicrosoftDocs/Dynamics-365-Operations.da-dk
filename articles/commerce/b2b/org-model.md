---
title: Oprette organisationsmodelhierarkier for B2B-organisationer
description: Dette emne indeholder en beskrivelse af, hvordan du kan oprette organisationsmodelhierarkier for business-to-business (B2B-organisationer).
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 450efd595a1cc1b72b2e62afbdd4518bcca59cb0
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035885"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a>Oprette organisationsmodelhierarkier for B2B-organisationer

[!include [banner](../../includes/banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du kan oprette organisationsmodelhierarkier for business-to-business (B2B-organisationer) i Microsoft Dynamics 365 Commerce.

I Commerce Headquarters repræsenteres organisationer af forretningspartnerlande af debitor- og debitorhierarkienheder. Forretningspartnerorganisationen og dens brugere er repræsenteret som kunder, og der bruges debitorhierarkier til at knytte disse kunder til hinanden.

Når en forretningspartneranmodning om at deltage i et B2B-e-handelswebsted godkendes, udføres følgende handlinger:

- Der oprettes to nye kundeposter i systemet: en kundepost af typen **Organisation** for partnerorganisationen for forretningspartneren og en kundepost af typen **Person** for anmoderen (dvs. den forretningspartnerbruger, der indsendte anmodningen).
- Der oprettes en ny debitorhierarkipost under **Debitor \> Debitorhierarki**. Denne post har følgende overskriftsegenskaber:

    - **Debitorhierarki-id** – et entydigt id for debitorhierarkiet. Dette id bruger den nummerserie, der er defineret i Delte parametre for Commerce i Commerce Headquarters.
    - **Navn** – Forretningspartnerens organisationsnavn, som det er angivet i anmodningen om onboarding.
    - **Formål** – Denne egenskab er angivet til den foruddefinerede værdi **B2B-organisation**.
    - **Organisation** – Forretningspartnerens debitor-id.

Her er detaljer om debitorhierarkiposten:

- Debitorposten for anmoderen er knyttet til debitorhierarkiet.
- Administratorrollen er tilknyttet anmoderen.

Når administratoren tilføjer flere brugere, føjes til forretningspartnerorganisationen på et B2B-websted, oprettes der en ny kundepost for hver bruger i Commerce Headquarters. Denne kundepost føjes også til den relevante kundehierarkipost for forretningspartneren og har rollen som "bruger".

> [!NOTE]
> I de fleste tilfælde skal de tilsvarende egenskabsværdier for alle debitorposter i et hierarki være ens. Da alle forretningspartnerbrugere f.eks. skal få ens priser for produkter, skal deres prisgruppe og tilknyttede konfigurationer stemmer overens. Systemet gennemtvinger dog ikke denne konsistens. De relevante brugere i handelshovedkvarteret er derfor ansvarlige for at sikre, at egenskabsværdierne og -konfigurationerne er ens for alle debitorer i et bestemt hierarki.

Brugere i Commerce Headquarters kan se på egenskabsværdierne for alle debitorposter i hierarkiet ved siden af hinanden. Vælg de relevante egenskaber for debitorposten ved at vælge fanenavnene i rullemenuen. Brugerne kan få vist og redigere egenskabsværdierne fra denne visning. Du kan også anvende alle værdierne fra administratorkundeposten på alle brugerkundeposter ved at vælge Tilsidesæt i oplysningerne **Tilsidesæt** i oplysningerne om debitorhierarkiet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere et B2B-e-handelswebsted](set-up-b2b-site.md)

[Administrere forretningspartnerbrugere på B2B-e-handelswebsteder](manage-b2b-users.md)

[Konfigurere betalingsmåden for debitorkonti for B2B-e-handelswebsteder](payment-method.md)

[Angive produktantalsgrænser for B2B-e-handelswebsteder](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]