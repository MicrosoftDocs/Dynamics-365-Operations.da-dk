---
title: Konfigurere en SharePoint-forbindelse
description: Dette emne forklarer, hvordan du konfigurerer en forbindelse, så elektronisk fakturering kan få adgang til et Microsoft SharePoint-websted.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6b9fffc1f3525e69792517dd1c6ebdcfbe5a74d2
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371533"
---
# <a name="configure-a-sharepoint-connection"></a>Konfigurere en SharePoint-forbindelse

[!include [banner](../includes/banner.md)]

Tjenesten Elektronisk fakturering kan læse filer fra Microsoft SharePoint-mapper og overføre filer til SharePoint. For at sikre, at elektronisk fakturering kan få adgang til et bestemt SharePoint-websted, skal du angive legitimationsoplysningerne for webstedet til tjenesten for elektronisk fakturering. Du skal desuden sikre dig, at legitimationsoplysningerne er sikkert gemt, og angiv dem ikke direkte. Du kan i stedet gemme dem i en Azure Key Vault og angive en Azure Key Vault-hemmelighed.

## <a name="grant-access-to-a-sharepoint-folder"></a>Give adgang til en SharePoint-mappe

1. Opret en appregistrering i lejeren, hvor RCS (Regulatory Configuration Service) er installeret.

    1. Log på [Azure-portalen](https://portal.azure.com/).
    2. Gå til **Appregistreringer**.
    3. Vælg **Ny registrering**.
    4. Angiv et navn, f.eks. **SharePoint -app til elektronisk fakturering**, og fuldfør registreringen
    5. Vælg den nye appregistrering.
    6. Aktivér indstillingen **Tillad offentlige klientflow** under fanen **Godkendelse**.
    4. Under fanen **Certifikater og hemmeligheder** skal du vælge **Ny klienthemmelighed** for at oprette en klienthemmelighed.
    5. Kopiér værdien af den hemmelighed, der blev oprettet.

    Følg disse retningslinjer:

    - Brug ikke samme appregistrering til forskellige tjenester.
    - Følg [anbefalingerne til adgangskodepolitikken](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide).
    - Konfigurer rotation af adgangskoder. Under rotation skal du oprette en ny klienthemmelighed til appregistreringen, opdatere Key Vault og derefter slette den gamle hemmelighed.

2. Gem værdierne for **Appregistreringshemmelighed** og **Program-id (klient)** som to nye hemmeligheder i Key Vault i opsætningen af dit miljø til elektronisk fakturering.
3. Tilføj de hemmeligheder, du har oprettet, i Key Vault-parametrene i konfigurationen af dit elektroniske faktureringsmiljø i RCS.
4. Giv i Azure-portalen adgang til SharePoint. Dette trin skal fuldføres af lejeradministratoren.

    1. Vælg den appregistrering, du oprettede.
    2. Vælg **Tilføj en rettighed** under **API-rettigheder**.
    3. Vælg **Microsoft Graph (programrettigheder)** \> **Sites.Selected**.
    4. Vælg **Giv administratorsamtykke til \<user&nbsp;name\>**.
    5. Gennemgå feltet **Status** for at sikre, at der er tildelt rettigheder.

        ![Rettigheder tildelt under fanen API-tilladelser.](media/configured-permissions.jpg)

    6. Åbn [Graph-tester – Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer), og log på.
    7. I ruden til venstre under fanen **Eksempelforespørgsler** skal du under **SharePoint-websteder** du vælge **hent SharePoint-websted ud fra den relative sti til webstedet**.
    8. Angiv parametrene for **\{host-name\}** og **\{server-relative-path\}**. Angiv f.eks. `<domain>.sharepoint.com` som **\{host-name\}** og `sites/<siteName>` som **\{server-relative-path\}**.

        > [!NOTE]
        > Lad parameteren **\{server-relative-path\}** være tom for standardwebstedet.

    9. Vælg **Kør forespørgsel**, og gem resultatet.
    10. Konfigurer følgende forespørgsel.

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        I denne forespørgsel er **\{site-id\}** værdien af **id**-noden fra det forrige svar på forespørgslen.

        Her er anmodningsteksten.

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        I dette anmodningstekst er **\{app-id\}** værdien af **Program-id (klient)**, og **\{app-name\}** er værdien af **Applikationsnavn**.

        ![POST-forespørgsel.](media/app-id-query.jpg)

    11. Under fanen **Rediger tilladelser** skal du vælge **Åbn rettighedspanel** og derefter vælge **Websteder** \> **Sites.FullControl.All** \> **Samtykke**.
    12. Vælg **Kør forespørgsel**.

Tjenesten Elektronisk fakturering har nu adgang til dit SharePoint-websted.
