---
title: Arbejdsområde for styring af anlægsaktiver
description: Denne artikel indeholder oplysninger om arbejdsområdet Styring af anlægsaktiv. Dette arbejdsområde viser oplysninger, der er tilknyttet de anlægsaktiver, der er angivet i systemet. Det omfatter en oversigtsvisning og en analysevisning.
author: moaamer
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetWorkspace
audience: Application User
ms.reviewer: kfend
ms.assetid: ''
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 95b45a91cd201a6d3a4817c315053e98a7693e05
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894049"
---
# <a name="fixed-asset-management-workspace"></a>Arbejdsområde for styring af anlægsaktiver

[!include [banner](../includes/banner.md)]

Arbejdsområdet **Styring af anlægsaktiv** viser oplysninger, der er tilknyttet de anlægsaktiver, der er angivet i systemet. Arbejdsområdet indeholder en oversigtsvisning og analysevisning. Fanen **Mit arbejde** viser en oversigtsfelter, oplysninger om anlægsaktiver og relaterede oplysninger om anlægsaktiver i det aktuelle firma. Du kan også føje analyser til afsnittet med Power BI-analyser direkte i arbejdsområdet. Fanen **Analyser – alle firmaer** bruger funktioner i Microsoft Power BI til at vise grafik, der vedrører anlægsaktiver i alle firmaer.

## <a name="my-work"></a>Mit arbejde

### <a name="summary"></a>Resume

Felterne i afsnittet **Oversigt** giver et overblik over dine anlægsaktiver. Oplysningerne omfatter statistik om aktiver, der endnu ikke er købt, aktiver, som er anskaffet i indeværende år og aktiver, der er blevet kasseret i indeværende år. Afsnittet **Oversigt** har også hurtig navigation til listesiden **Anlægsaktiver**, batchafskrivningsforslag og anlægsaktivkladde.

### <a name="find-fixed-assets"></a>Find anlægsaktiver

I afsnittet **Find anlægsaktiver** kan du hurtigt søge efter aktiver ved at angive nummeret på anlægsaktivet, gruppe, navn, sted eller den person, der er ansvarlig. Alle aktiver, der opfylder søgekriterierne, vises på listen.

På listen kan du få vist følgende sider:

 - Siden **Oplysninger** for anlægsaktivet.
 - Siden **Bøger** for alle bøger, der er knyttet til anlægsaktivet
 - Siden **Vurderinger af anlægsaktiver**

### <a name="valuations"></a>Vurderinger

På siden **Vurderinger af anlægsaktiver** kan du få vist de vigtigste oplysninger om et anlægsaktiv og også detaljerne for alle de bøger, der er knyttet til anlægsaktivet. Indstillingen **Saldi** øverst til venstre på siden viser den gældende vurdering for hver bog, der er knyttet til anlægsaktivet. Du kan rulle tilbage fra værdierne for at se de detaljerede posteringer, der udgør oversigtsværdien. Indstillingen **Profil** øverst til venstre på siden viser afskrivningsplanen for hver bog, der er knyttet til anlægsaktivet.

Du kan få adgang til siden **Vurderinger af anlægsaktiver** fra arbejdsområdet **Styring af anlægsaktiv** eller listesiden **Anlægsaktiv**.

### <a name="related-information"></a>Relaterede oplysninger

Du kan gå direkte til siden **Opsætning af bøger**, siden **Forespørgsel om anlægsaktivposteringer** og flere rapporter ved hjælp af linkene i afsnittet **Relaterede oplysninger** i arbejdsområdet.

### <a name="analytics--all-companies"></a>Analyse – alle firmaer

Siden **Analyser** indeholder vigtige oplysninger om anlægsaktiver i alle juridiske enheder i systemet. Adgang til denne fane styres af sikkerhedsrettighederne Vis analyse af anlægsaktiver for alle firmaer.

Følgende tabel viser de visualiseringer, der er tilgængelig på hver rapportside.

| Rapportside            | Visualisering        |
|------------------------|----------------------|
| Vurderinger af anlægsaktiver | Samlet bogført nettoværdi |
| Vurderinger af anlægsaktiver | Bogført nettoværdi pr. anlægsaktivgruppe |
| Vurderinger af anlægsaktiver | Anskaffelsesværdier |
| Vurderinger af anlægsaktiver | Kassationsværdier |
| Vurderinger af anlægsaktiver | Anlægsaktivoplysninger |
| Vurderingstilknytninger        | Samlet bogført nettoværdi |
| Vurderingstilknytninger        | Anlægsaktivplaceringer |
| Vurderingstilknytninger        | Anlægsaktivoplysninger |

For at få vist analyser med data skal du først opdatere den samlede måling af AssetTransactionMeasure på siden **Enhedslager**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
