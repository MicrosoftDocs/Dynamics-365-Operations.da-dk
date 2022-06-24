---
title: Forkert feltværdi i TaxTrans
description: Denne artikel indeholder oplysninger om fejlfinding af forkerte feltværdier i TaxTrans.
author: EricWangChen
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6e7329ffdc04207116c92cb42e02750b176713fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899808"
---
# <a name="incorrect-field-value-in-taxtrans"></a>Forkert feltværdi i TaxTrans

[!include [banner](../includes/banner.md)]

Hvis en feltværdi i **TaxTrans** ikke er korrekt, kan du bruge oplysningerne i denne artikel til at løse problemet.

## <a name="overview-of-values"></a>Oversigt over værdier
Følgende liste viser, hvordan **TaxTrans**, **TaxUncommitted** og **TmpTaxWorkTrans** er tilsvarende datasæt, men fungerer forskelligt.

  - **TaxTrans** er det endelige resultat af den bogførte momspostering i databasen.
  - **TaxUncommitted** er det midlertidige beregnede momsresultat, der bevares i databasen (hvis det er relevant), og som bruges senere i bogføringen.
  - **TmpTaxWorkTrans** er det midlertidige beregnede momsresultat i tabellen i hukommelsen (tabeltype = InMemory).

Hvis du finder rodårsagen til en forkert **TaxTrans**-kolonne, har du også fundet rodårsagen til en forkert kolonne for **TaxUncommitted** eller **TmpTaxWorkTrans**. Det skyldes, at de tre kolonner kopieres mellem hinanden.

Ved momsberegning genereres **TmpTaxWorkTrans** typisk, og derefter genereres **TaxUncommitted**, hvis det er relevant. Ved momsbogføring genereres **TaxTrans**.


## <a name="add-breakpoints"></a>Tilføje pausepunkter
Hvis du vil tilføje pausepunkter, skal du benytte følgende fremgangsmdåe: 

1. Tilføj udvidelser og pausepunkter i *indsert()* og *update()* i udvidelserne som vist nedenfor.

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmpTaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. Du kan også tilføje pausepunkter direkte, når **TaxUncommitted** ikke er medtaget.

     - *TaxTrans.insert()*, *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>Genskabe og løse fejl

Når pausepunkterne er angivet, vises alle ændringer af dataene under fejlfinding. Hvis du vil finde rodårsagen til en forkert kolonne for **TaxTrans**, **TaxUncommitted** eller **TmpTaxWorkTrans**, skal du gennemse og notere følgende punkter ned:

- Det sidste pausepunkt, hvor kolonnen var korrekt.
- Det første pausepunkt, hvor kolonnen var korrekt.
- Hvad der er sket mellem disse to punkter.

## <a name="determine-whether-customization-exists"></a>Afgøre, om der findes tilpasninger
Hvis du har udført trinnene i de forrige afsnit, men ikke har kunnet løse problemet, skal du afgøre, om der er foretaget tilpasninger. Hvis der ikke er foretaget tilpasninger, skal du kontakte Microsoft Support for at få hjælp.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

