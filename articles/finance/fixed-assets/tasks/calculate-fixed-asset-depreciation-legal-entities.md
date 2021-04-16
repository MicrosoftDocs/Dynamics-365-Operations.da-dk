---
title: Beregne afskrivning af anlægsaktiver på tværs af juridiske enheder
description: Afskrivning af anlægsaktiver kan køres på tværs af juridiske enheder i et enkelt trin.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85a1e71967fb126be29a76a8a29ea5e4ae2b2199
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818458"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Beregne afskrivning af anlægsaktiver på tværs af juridiske enheder

[!include [banner](../../includes/banner.md)]

Afskrivning af anlægsaktiver kan køres på tværs af juridiske enheder i et enkelt trin. Denne fremgangsmåde viser, hvordan du konfigurerer og kører processen for flere juridiske enheder. Den bruger rollen Revisor og demodata for den juridiske enhed USMF.


## <a name="set-up-cross-company-depreciation-run-journals"></a>Konfigurer kladder for kørsel af afskrivning på tværs af virksomheden
1. Gå til Anlægsaktiver > Opsætning > Anlægsaktivparametre.
2. Udvid sektionen Forslag til anlægsaktiver.
3. Klik på Tilføj.
4. I feltet Posteringslag skal du angive eller vælge en værdi.
5. Indtast eller vælg en værdi i feltet Kladdenavn.
    * Gentag kladdeopsætningen på siden med parametre for anlægsaktiver i hver juridisk enhed.  

## <a name="depreciation-run"></a>Afskrivning
1. Gå til Anlægsaktiver > Kladdeposteringer > Opret afskrivningsforslag.
2. I feltet Posteringslag skal du angive eller vælge en værdi.
    * Kladdenavnet dannes som standard fra parametrene for anlægsaktivet. Det kan ændres her for den aktuelle juridiske enhed.  
3. Indtast en dato i feltet Til dato.
    * Vælg de juridiske enheder, der skal medtages i afskrivningskørslen.  
    * Kun juridiske enheder med kladder, der er angivet for anlægsaktivforslag på siden med parametre for anlægsaktiver, vises på listen.  
4. Vælg Ja i feltet Bogfør kladder.
    * Filtreringsfelterne omfatter alle anlægsaktiver, grupper og bøger for de juridiske enheder, der er valgt for denne kørsel af afskrivning.  
    * Indstillingen for batchbehandling er aktiveret som standard. Når denne indstilling er aktiveret, kører oprettelse og bogføring af afskrivningskladden i baggrunden.  
5. Klik på Opret kladde.
6. Gå til Anlægsaktiver > Kladdepostering > Anlægsaktivkladde.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]