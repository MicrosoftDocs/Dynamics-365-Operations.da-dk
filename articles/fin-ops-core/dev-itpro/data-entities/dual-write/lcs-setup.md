---
title: Installation med to skrivninger fra Lifecycle Services
description: I dette emne beskrives, hvordan du kan oprette en forbindelse med to skrivninger mellem et nyt Finance and Operations-miljø og et nyt Common Data Service-miljø fra Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c78752aa1544b12f61071fa06617af4ac2809233
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172986"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Installation med to skrivninger fra Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

I dette emne beskrives, hvordan du kan oprette en forbindelse med to skrivninger mellem et nyt Finance and Operations-miljø og et nyt Common Data Service-miljø fra Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Forudsætninger

Du skal være administrator for at kunne konfigurere en forbindelse med to skrivninger.

+ Du skal have adgang lejeren.
+ Du skal være administrator i Finance and Operations-miljøer og Common Data Service-miljøer.

## <a name="set-up-a-dual-write-connection"></a>Oprette en forbindelse med to skrivninger

Følg disse trin for at oprette forbindelsen med to skrivninger.

1. Gå til dit projekt i LCS.
2. Vælg **Konfigurer** for at installere et nyt miljø.
3. Vælg versionen. 
4. Vælg topologien. Hvis der kun er én tilgængelig topologi, vælges den automatisk.
5. Afslut de første trin i guiden **Installationsindstillinger**.
6. Udfør ét af følgende trin på fanen **Common Data Service**:

    - Hvis der allerede er klargjort et Common Data Service-miljø til din lejer, kan du vælge det.

        1. Angiv indstillingen **Konfigurer Common Data Service** til **Ja**.
        2. Vælg det miljø, der skal integreres med dine Finance and Operations-data, i feltet **Tilgængelige miljøer**. Listen omfatter alle de miljøer, hvor du har administratorrettigheder.
        3. Markér afkrydsningsfeltet **Acceptér** for at angive, at du accepterer vilkårene og betingelserne.

        ![Common Data Service-fanen, når et Common Data Service-miljø allerede er klargjort til din lejer](../dual-write/media/lcs_setup_1.png)

    - Hvis din lejer ikke allerede har et Common Data Service-miljø, vil der blive klargjort et nyt miljø.

        1. Angiv indstillingen **Konfigurer Common Data Service** til **Ja**.
        2. Angiv et navn for Common Data Service-miljøet.
        3. Vælg det område, som miljøet skal installeres i.
        4. Vælg standardsprog og valuta for miljøet.

            > [!NOTE]
            > Du kan ikke ændre sproget og valutaen senere.

        5. Markér afkrydsningsfeltet **Acceptér** for at angive, at du accepterer vilkårene og betingelserne.

        ![Common Data Service-fanen, når din lejer ikke allerede har et Common Data Service-miljø](../dual-write/media/lcs_setup_2.png)

7. Afslut de resterende trin i guiden **Installationsindstillinger**.
8. Når miljøet har status **Installeret**, skal du åbne siden med miljødetaljer. Afsnittet med **Common Data Service-miljøoplysninger** viser navnene på Finance and Operations-miljøet og det sammenkædede Common Data Service-miljø.

    ![Afsnittet med Common Data Service-miljøoplysninger](../dual-write/media/lcs_setup_3.png)

9. En administrator af Finance and Operations-miljøet skal logge på LCS og vælge **Link til CDS for Apps** for at fuldføre sammenkædningen. På siden med miljødetaljer vises administratorens kontaktoplysninger.

    Når sammenkædningen er fuldført, opdateres status til **Miljøsammenkædning er fuldført**.

10. Hvis du vil åbne arbejdsområdet **Dataintegration** i Finance and Operations-miljøet og styre, hvilke skabeloner der findes, skal du vælge **Link til CDS For Apps**.

    ![Knappen Link til CDS for Apps i området med Common Data Service-miljøoplysninger](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Du kan ikke fjerne sammenkædningen mellem miljøer ved hjælp af LCS. Hvis du vil fjerne sammenkædningen mellem et miljø, skal du åbne arbejdsområdet **Dataintegration** i Finance and Operations-miljøet og derefter vælge **Fjern sammenkædning**.
