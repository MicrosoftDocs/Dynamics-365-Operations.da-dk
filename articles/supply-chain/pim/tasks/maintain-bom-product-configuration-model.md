---
title: Vedligeholde styklisten for en produktkonfigurationsmodel
description: Kørsel af denne procedure kræver en eksisterende model til produktkonfiguration.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd78b06f10d0c9b1df57dacdd824b06ebe414b3b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577282"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Vedligeholde styklisten for en produktkonfigurationsmodel

[!include [banner](../../includes/banner.md)]

Kørsel af denne procedure kræver en eksisterende model til produktkonfiguration. Højttaler af topkvalitet-modellen i demofirmaet USMF bruges til at oprette denne procedure.

## <a name="add-a-bom-line"></a>Tilføj en styklistelinje

1. Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.
1. Find og vælg den ønskede post på listen.
    * Vælg Højttaler af topkvalitet for denne procedure.  
1. Vælg linket i den valgte række på listen.
1. Udvid sektionen **Styklistelinjer**.
1. Vælg **Tilføj**.
1. Skriv en værdi i feltet **Navn**.
1. Indtast en værdi i feltet **Beskrivelse**.
1. Vælg **Gem**.

## <a name="add-bom-line-details"></a>Tilføj Linjedetaljer i stykliste

1. Vælg **Oplysninger om styklistelinjer**.
2. Indtast eller vælg en værdi i feltet **Varenummer**.
    * Du kan f.eks. vælge elementet M0055.  
    * For hver stykliste linjeegenskab kan du vælge, om den har en fast værdi eller er knyttet til en attribut.  
3. Marker afkrydsningsfeltet **Indstil**.
4. Vælg *Ja* i feltet **Beregning**.
    * Når du indstiller egenskaben **Beregning** til *Ja*, sikrer du, at styklistelinjen medtages i omkostningsberegninger.  
5. Vælg fanen **Opsætning**.
6. Marker afkrydsningsfeltet **Indstil**.
7. Angiv et tal i feltet **Antal**.
    * Antalsfeltet bestemmer, hvor meget af elementet, der skal medtages i styklisten. Dette kunne være en oplagt kandidat til en attributtilknytning.  
8. Vælg fanen **Dimension**.
    * Kontroller, hvis nogen af produktdimensionerne er aktive og derfor skal have en værdi eller en attribut tildelt.  
9. Vælg **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]