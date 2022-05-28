---
title: Tilpasse momskonfigurationer til masterdataopslag
description: Dette emne forklarer, hvordan du kan tilpasse momskonfigurationer for at udvide funktionen til masterdataopslag.
author: kai-cloud
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 69541316ad4c6c4bb404ea142844ce596b5502b9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689122"
---
# <a name="customize-tax-configurations-for-master-data-lookup"></a>Tilpasse momskonfigurationer til masterdataopslag

[!include [banner](../includes/banner.md)]

Følg trinnene i dette emne for at tilpasse momskonfigurationer for at udvide funktionen til masterdataopslag.

## <a name="import-a-tax-configuration-provided-by-microsoft"></a>Importere en momskonfiguration fra Microsoft

1. I Regulatory Configuration Service (RCS) skal du i arbejdsområdet **Elektronisk rapportering** vælge **Microsoft** som konfigurationsudbyder.
2. Vælg **Lagre**.
3. Vælg **Global**, og vælg derefter **Åbn**.
4. Vælg en momskonfiguration, f.eks. **Konfiguration af momsberegning**, og vælg derefter en version under fanen **Versioner**.
5. Vælg **Importér**.

> [!NOTE]
> Som standard importeres Dataverse-modeltilknytningen. Hvis du modtager advarselsmeddelelser under konfigurationsimportprocessen, skal du aktivere de virtuelle enheder i Dataverse. Du kan finde flere oplysninger i [Aktivere virtuelle Dataverse-enheder](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="create-a-customized-data-model-configuration"></a>Oprette en brugerdefineret datamodelkonfiguration

1. Vælg **Momskonfigurationer** i arbejdsområdet **Elektronisk rapportering**, og vælg derefter den datamodelkonfiguration, der skal udvides. Vælg f.eks. **Datamodel til momsberegning**.
2. Vælg **Opret konfiguration**.
3. Vælg **Momspligtig dokumentmodel, der er afledt af Navn: Datamodel til momsberegning, Microsoft**.
4. Angiv **Datamodel for tilpasning** i feltet **Navn**.
5. Vælg **Opret konfiguration**.

## <a name="create-customized-reference-models"></a>Oprette tilpassede referencemodeller

1. Vælg **Datamodel for tilpasning** på siden **Momskonfigurationer**, og vælg derefter **Designer**.
2. Vælg ellipseknappen (**...**), og vælg derefter visningen **Referencemodul**.

    [![Referencemodel.](./media/pic2.png)](./media/pic2.png)

3. Opret den tilpassede referencemodel. Den tilpassede model er en rodmodel. Den tilpassede enhed er en postliste. Det brugerdefinerede felt er et strengfelt, du skal bruge i opslaget. Hvis det er nødvendigt, kan du tilføje felter.
4. Vælg ellipseknappen (**...**), og vælg derefter visningen **Momspligtigt dokument**.
5. Vælg den attribut, der skal knyttes til den tilpassede referencemodel. Vælg f.eks. **Brugerdefineret attribut**, og benyt derefter følgende fremgangsmåde:

    1. Vælg **Vælg referencemodel**.
    2. Vælg **Tilpasset model**, og vælg derefter **OK**. Referencemodelnavnet opdateres til værdien i feltet **Naturlig nøgle**.

        [![Dialogboksen Vælg referencemodel.](./media/pic5.png)](./media/pic5.png)

    3. Vælg **Gem**, og vælg derefter **Fuldfør**.

## <a name="create-a-customized-model-mapping-configuration"></a>Oprette en brugerdefineret modeltilknytningskonfiguration

1. Vælg **Momskonfigurationer** i arbejdsområdet **Elektronisk rapportering**, og vælg derefter konfigurationen **Dataverse-modeltilknytning**.
2. Vælg **Nej** i feltet **Standard for modeltilknytning**.
3. Vælg **Opret konfiguration**.
4. Vælg **Momspligtig dokumentmodeltilknytning, der er afledt af Navn: Dataverse-modeltilknytning, Microsoft**.
5. Angiv **Tilknytning af tilpasningsmodel** i feltet **Navn**.
6. Vælg datamodellen **Datamodel for tilpasning** i feltet **Målmodel**.
7. Vælg **Opret konfiguration**.

    [![Dialogboks til rulleliste Opret konfiguration.](./media/pic6.png)](./media/pic6.png)

8. Vælg **Tilknytning af tilpasningsmodel**, og angiv feltet **Tilknyttet program** til den forbindelse, der blev oprettet i trin 8 i [Konfigurere et miljø til opslag efter masterdata](tax-service-set-up-environment-master-data-lookup.md).
9. Vælg **Ja** i feltet **Standard for modeltilknytning**.

## <a name="create-customized-model-mappings"></a>Oprette tilpassede modeltilknytninger

1. Vælg **Tilknytning af tilpasningsmodel** på siden **Momskonfigurationer**.
2. Vælg **Designer**, og vælg derefter **Tilpasningsmodel**.

    [![Tilpasningsmodel.](./media/pic8.png)](./media/pic8.png)

## <a name="map-a-model-mapping-to-a-dataverse-entity"></a>Knytte en modeltilknytning til en Dataverse-enhed

1. Vælg **Tilpasningsmodel** på siden **Modeltilknytningsdesigner**, og vælg derefter **Designer**.
2. Brug træet **Datakildetyper** til at vælge **Dataverse-tabel**.
3. Vælg **Tilføj rod** under fanen **Datakilder**.
4. I feltet **Navn** skal du angive **Tilpasset Dataverse**.
5. Vælg en enhed i det andet **Navn**-felt.
6. Vælg **OK**.

    [![Dialogboksen Egenskaber for datakilden 'Tabel'.](./media/pic9.png)](./media/pic9.png)

7. Vælg **Tilpasset Dataverse** og **Tilpasset enhed**, og vælg derefter **Bind**.

    [![Tilpasset Dataverse og tilpasset enhedsbinding.](./media/pic10.png)](./media/pic10.png)

8. Vælg et felt under **Tilpasset Dataverse** og **Tilpasset enhed**, og vælg derefter **Bind**.

    [![Tilpasset Dataverse og tilpasset feltbinding.](./media/pic11.png)](./media/pic11.png)

9. Vælg **Gem**, og vælg derefter **Fuldfør**.

## <a name="create-a-customized-tax-configuration"></a>Oprette en brugerdefineret momskonfiguration

1. Vælg **Momskonfigurationer** i arbejdsområdet **Elektronisk rapportering**, og vælg derefter **Konfiguration af momsberegning**.
2. Vælg **Opret konfiguration**.
3. Vælg **Konfiguration af momstjeneste, der er afledt af Navn: Konfiguration af momsberegning, Microsoft**.
4. Angiv **Konfiguration af tilpasning** i feltet **Navn**.
5. Vælg **Opret konfiguration**.
6. Vælg **Konfiguration af tilpasning**, og vælg derefter **Designer**.
7. Vælg **Datamodel for tilpasning** i feltet **Datamodel**.
8. Vælg den tilsvarende version af datamodellen i feltet **Datamodelversion**.

    [![Sektionen Egenskaber.](./media/pic13.png)](./media/pic13.png)

9. Vælg **Fuldfør**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
