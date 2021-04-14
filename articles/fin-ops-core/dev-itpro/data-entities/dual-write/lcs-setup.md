---
title: Konfiguration af dobbeltskrivning fra Lifecycle Services
description: Dette emne beskriver, hvordan du konfigurerer en forbindelse med dobbeltskrivning fra Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e51b4ef1e309e5f89dc82a3776b88c505dc6593d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748535"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Konfiguration af dobbeltskrivning fra Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives, hvordan du kan oprette en forbindelse med to skrivninger mellem et nyt Finance and Operations-miljø og et nyt Dataverse-miljø fra Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Forudsætninger

Du skal være administrator for at kunne konfigurere en forbindelse med to skrivninger.

+ Du skal have adgang lejeren.
+ Du skal være administrator i Finance and Operations-miljøer og Dataverse-miljøer.

## <a name="set-up-a-dual-write-connection"></a>Oprette en forbindelse med to skrivninger

Følg disse trin for at oprette forbindelsen med to skrivninger.

1. Gå til dit projekt i LCS.
2. Vælg **Konfigurer** for at installere et nyt miljø.
3. Vælg versionen. 
4. Vælg topologien. Hvis der kun er én tilgængelig topologi, vælges den automatisk.
5. Afslut de første trin i guiden **Installationsindstillinger**.
6. Udfør ét af følgende trin på fanen **Dataverse**:

    - Hvis der allerede er klargjort et Dataverse-miljø til din lejer, kan du vælge det.

        1. Angiv indstillingen **Konfigurer Dataverse** til **Ja**.
        2. Vælg det miljø, der skal integreres med dine Finance and Operations-data, i kolonnen **Tilgængelige miljøer**. Listen omfatter alle de miljøer, hvor du har administratorrettigheder.
        3. Markér afkrydsningsfeltet **Acceptér** for at angive, at du accepterer vilkårene og betingelserne.

        ![Dataverse-fanen, når et Dataverse-miljø allerede er klargjort til din lejer](../dual-write/media/lcs_setup_1.png)

    - Hvis din lejer ikke allerede har et Dataverse-miljø, vil der blive klargjort et nyt miljø.

        1. Angiv indstillingen **Konfigurer Dataverse** til **Ja**.
        2. Angiv et navn for Dataverse-miljøet.
        3. Vælg det område, som miljøet skal installeres i.
        4. Vælg standardsprog og valuta for miljøet.

            > [!NOTE]
            > Du kan ikke ændre sproget og valutaen senere.

        5. Markér afkrydsningsfeltet **Acceptér** for at angive, at du accepterer vilkårene og betingelserne.

        ![Dataverse-fanen, når din lejer ikke allerede har et Dataverse-miljø](../dual-write/media/lcs_setup_2.png)

7. Afslut de resterende trin i guiden **Installationsindstillinger**.
8. Når miljøet har status **Installeret**, skal du åbne siden med miljødetaljer. Afsnittet med **Power Platform Integration** viser navnene på Finance and Operations-miljøet og det sammenkædede Dataverse-miljø.

    ![Afsnittet Power Platform Integration](../dual-write/media/lcs_setup_3.png)

9. En administrator af Finance and Operations-miljøet skal logge på LCS og vælge **Link til CDS for Apps** for at fuldføre sammenkædningen. På siden med miljødetaljer vises administratorens kontaktoplysninger.

    Når sammenkædningen er fuldført, opdateres status til **Miljøsammenkædning er fuldført**.

10. Hvis du vil åbne arbejdsområdet **Dataintegration** i Finance and Operations-miljøet og styre, hvilke skabeloner der findes, skal du vælge **Link til CDS For Apps**.

    ![Knappen Link til CDS for Apps i afsnittet Power Platform Integration](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Du kan ikke fjerne sammenkædningen mellem miljøer ved hjælp af LCS. Hvis du vil fjerne sammenkædningen mellem et miljø, skal du åbne arbejdsområdet **Dataintegration** i Finance and Operations-miljøet og derefter vælge **Fjern sammenkædning**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]