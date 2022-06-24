---
title: Administrere leasingaftaler via struktur for leasingimport
description: Denne artikel forklarer, hvordan du kan bruge leasingimportstrukturen til at justere flere leasingaftaler på én gang.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseImportHeader
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8cf81ccf61e62ac49e6cb90d13ca5fe50147cc76
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894958"
---
# <a name="manage-leases-through-the-lease-import-framework"></a>Administrere leasingaftaler via struktur for leasingimport

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du kan bruge leasingimportstrukturen til at justere flere leasingaftaler i et trin. Når du bruger denne facilitet, kan du spare tid, og du kan også sikre dig mere præcise justeringer ved at reducere risikoen for menneskelige fejl. Desuden kan denne egenskab oprette forbindelse mellem Microsoft Dynamics 365 Finance og eksterne dataenheder for at overføre data effektivt.

Følgende dataenheder kan bruges til at integrere aktivleasing med eksterne systemer:

- Midlertidig lagring af leasing
- Midlertidig lagring af betalingskontrakt
- Midlertidig lagring af kontrakt til senere opfyldelse

Du kan bruge importprocessen til at justere en leasingaftale, opdatere ikke-økonomiske oplysninger eller tilføje nye leasingaftaler. Du kan få vist og redigere leasingdata, før du importerer dem.

Systemet kan køre følgende tre processer via leasingimportpakken.

| Procestype  | Betegnelse |
|---------------|-------------|
| Tilføj post    | Overførte leasingaftaler med denne procestype opretter en leasingaftale i systemet. Betalingsplanen skal bekræftes manuelt, og den oprindelige genkendelseskladdepostering skal bogføres manuelt efter overflytningen. |
| Opdater post | Overførte leasingaftaler med denne procestype for opdatering af feltværdier for en leasingaftale, der allerede findes i systemet. Kun de felter, der er blevet valgt på siden **Opdater feltvalg**, opdateres. Det anbefales, at du vælger ikke-økonomiske felter på siden **Valg af opdateringsfelter**, da denne procestype ikke justerer leasingaftalen. |
| Reguler post | Overførte leasingaftaler med denne procestype justerer leasingaftalen. Denne justering medfører en finansiel leasingændring af leasingaftalen. Når leasingaftalen er behandlet, opretter systemet en ny betalingsplan ved hjælp af de nye data fra leasingimportpakken. Systemet bekræfter ikke betalingsplanen eller bogfører reguleringskladdeposten. |

Når oplysningerne er overført via arbejdsområdet **Datastyring**, skal du åbne siden **Importer sidehoved** (**Aktivleasing \> Struktur for leasingimport \> Importoverskrift**). På denne side vises en liste over alle import af de tre dataenheder, der blev angivet tidligere.

Hvis du vil have vist de midlertidige leasingdata, før behandlingen køres, skal du vælge **Midlertidige data**.

Med sammenligningsfunktionen kan du sammenligne en post, der er ved at blive importeret, med den tilsvarende post, der allerede findes i systemet. Hvis du vil sammenligne en individuel leasingpost, skal du vælge en leasingaftale og derefter vælge **Sammenlign**. Du skal udføre dette trin for at generere en rapport **Forskelle**, før du overfører leasingposterne. Sammenligningsfunktionaliteten sammenligner værdierne i de midlertidige data med de værdier for leasingaftaler, der aktuelt findes i systemet.

> [!NOTE]
> Sammenligningsfunktionaliteten virker ikke for leasinger, der har procestypen **Tilføj post**, da der ikke er noget at sammenligne med den pågældende leasingaftale.
>
> Hvis du vil sammenligne flere leasinger samtidig, skal du gå til **Aktivleasing \> Struktur af leasingimport \> Periodisk** og vælge **Sammenlign**.

For de enkelte objekter kan du få vist forskellene mellem det, der aktuelt findes i systemet, og hvad der er i de midlertidige tabeller. For de enkelte objekter i de midlertidige tabeller skal du vælge **Se forskelle**. Den dialogboks, der vises, viser den aktuelle værdi og den foreslåede midlertidige værdi.

Du kan også opdatere den midlertidige værdi ved at ændre den i kolonnen **Ny værdi** og derefter vælge **Opdater midlertidig**.

Du kan validere leasingaftaler for at sikre, at posterne kan bringes ind i systemet, uden at der indføres fejl. Før en leasingpost overføres, kører systemet flere valideringer for at sikre, at posten importeres korrekt. Hvis du vil validere en individuel leasingaftale, skal du vælge **Valider**.

> [!NOTE]
> Hvis du vil validere flere leasinger samtidig, skal du gå til **Aktivleasing \> Struktur af leasingimport \> Periodisk** og vælge **Valider**.

Hvis du vil behandle en individuel leasing, skal du vælge **Overfør leasingposter** på siden **Importer sidehoved**. Når en leasingaftale overføres, udfører systemet den handling, der er angivet i feltet **Procestype**.

> [!NOTE]
> Hvis du vil overføre flere leasinger samtidig, skal du gå til **Aktivleasing \> Struktur af leasingimport \> Periodisk** og vælge **Overfør**.

Når leasingaftalerne sammenlignes, kan du køre en rapport for at få vist forskellene for hver leasingaftale, der er medtaget i import-id. Hvis du vil køre rapporten for én leasingaftale, skal du vælge den pågældende leasingaftale i de midlertidige data og derefter vælge **Sammenlign, og vis rapport \> Rapport med forskelle**.

> [!NOTE]
> Hvis du vil sammenligne flere leasinger samtidig, skal du gå til **Aktivleasing \> Struktur af leasingimport \> Periodisk** og vælge **Sammenlign**. 

## <a name="set-up-update-fields"></a>Konfigurer opdateringsfelter

Hvis du bruger struktur til leasingimport til at opdatere leasingaftaler, og procestypen er **Opdater post**, kan du vælge at opdatere bestemte felter.

1. Gå til **Aktivleasing \> Struktur af importstruktur \> Opsætning \> Opdater feltvalg**.
2. På den side, der vises, skal du vælge de felter, der skal opdateres, og derefter vælge den grønne pil for at flytte dem til listen **Valgte felter**. Det er kun felter på listen **Valgte felter**, der kan opdateres ved hjælp af leasingimportpakken.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
