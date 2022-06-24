---
title: Disponeringsindstillinger
description: Denne artikel indeholder oplysninger om de indstillinger for disponering, som behovsplanlægningen bruger til at beregne varebehov.
author: t-benebo
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1218c447a18f79f9a44bfa413a0414d6926d7499
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871943"
---
# <a name="coverage-settings"></a>Disponeringsindstillinger

[!include [banner](../includes/banner.md)]

Ved behovsplanlægning anvendes disponeringsindstillinger til at beregne varebehov.

Du kan angive disponeringsindstillinger på flere måder:

- Angiv disponeringsindstillinger for en disponeringsgruppe.

    Du kan oprette en disponeringsgruppe, der indeholder alle produkter, der er knyttet til disponeringsgruppen. Du kan oprette en disponeringsgruppe ved at gå til **Varedisponering &gt; Konfiguration &gt; Disponering &gt; Disponeringsgrupper**. Du kan sammenkæde en disponeringsgruppe til et produkt. Hvis sammenkædningen er specifik for et websted, et lagersted eller en produktdimension, skal du bruge feltet **Disponeringsgruppe** på siden **Varedisponering**. Hvis sammenkædningen er generisk, uanset produktdimensionerne, skal du bruge feltet **Disponeringsgruppe** på oversigtspanelet **Plan** på siden **Produktdetaljer**. Hvis du som standard ikke knytter en disponeringsgruppe til et produkt, bruger den overordnede planlægning den standarddisponeringsgruppe, der er angivet på siden **Varedisponeringsparametre**.

- Angiv disponeringsindstillinger for et produkt.

    Du kan oprette disponeringsindstillinger for et bestemt produkt. Gå til **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg produktet, og vælg derefter **Varedisponering** i gruppen **Disponering** under fanen **Plan** i handlingsruden for at åbne siden **Varedisponering**. Hvis produktet allerede er knyttet til en dispositionsgruppe, kan du tilsidesætte indstillingerne for dispositionsgruppen ved hjælp af feltet **Tilsidesæt**. Disponeringsindstillinger på siden **Varedisponering** har fortrinsret over indstillingerne på siden **Dækningsgruppe**.

- Angiv disponeringsindstillinger for et produkt ved hjælp af en guide.

    Guiden hjælper dig trin for trin gennem opsætningen af de primære varedisponeringsparametre. På siden **Varedisponering** skal du i handlingsruden klikke på **Guide** for at åbne **Varedisponeringsguide**.

- Angiv disponeringsindstillinger for en dimensionsgruppe.

    Gå til **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg linket feltet **Lagringsdimensionsgruppe** i sektionen **Administration** i oversigtspanelet **Generelt** på siden **Frigivne produktdetaljer**. På siden **Lagringsdimensionsgrupper** skal du markere afkrydsningsfeltet **Disponer pr. dimension** for at oprette dispositionsindstillinger for en dimension i lagringsdimensionsgruppen. Feltet **Disponer pr. dimension** skal være markeret for alle produktdimensioner, f.eks. konfiguration, farve, størrelse, typografi.


## <a name="coverage-codes"></a>Disponeringskoder

Varedisponering kan konfigureres til at bruge forskellige genopfyldningsmetoder. Genopfyldningsmetoderne eller metoderne til angivelse partistørrelse er de teknikker, der bruges af systemet til at bestemme batchstørrelsen for købte eller fremstillede varer. 

Hver genbestillingsmetode tildeles en af følgende disponeringskoder:

- **Manuel** – Metoden til angivelse af partistørrelse, hvor systemet ikke foreslår købte, overflytninger eller produktionsordrer for varen. Planlæggeren for varen vil være ansvarlig for oprettelsen af de nødvendige ordrer til genopfyldning af varen.
- **Pr. behov** – Metoden til angivelse af partistørrelse, hvor systemet opretter en planlagt indkøbs-, overførsels- eller produktionsordre pr. behov for varen. Dette bruges generelt til dyre varer med forbigående behov.  
- **Pr. periode** - Metoden til angivelse af partistørrelse, som kombinerer alle behov for en periode til én ordre for varen. Ordren planlægges for den første dag i perioden, og dens antal vil opfylde nettobehovet i den oprettede periode. Perioden starter med det første behov for varen og dækker den definerede varighed i tiden. Den næste periode vil starte med de næste behov for varen.
- **Min./Maks.** - Metoden til angivelse af partistørrelse, som indeholder genopfyldningen af lageret op til et bestemt niveau, når den forventede beholdning er lavere end en tærskel. Genopfyldningsantallet vil være forskellen mellem maksimumniveauet og det forventede disponible lagerniveau.


## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over behovsplaner](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]