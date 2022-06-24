---
title: Flytte NF-e XML-filer som vedhæftede filer
description: Denne artikel forklarer, hvordan du flytter NF-e XML-filer fra Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management-databasen og gør dem tilgængelige som vedhæftede filer i stedet.
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ce9061896759efeb8e8960e84656d5fc1f0616ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877891"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>Flytte NF-e XML-filer som vedhæftede filer

[!include [banner](../includes/banner.md)] 


Når der udstedes elektroniske regnskabsdokumenter (NF-e), oprettes og lagres XML-filer i Microsoft Dynamics 365 Finance- og Dynamics 365 Supply Chain Management-databaserne. I den brasilianske lokalisering kan du bruge funktionen **NF-e XML flytning som vedhæftet fil** for at frigøre databaseplads, som disse XML-filer optager.

Inden for et bestemt datointerval og regnskabsområde flytter funktionen NF-e XML-filerne fra din Finance- eller Supply Chain Management-database til Blob-lageret fra dit Azure-abonnement. Denne bevægelse gør, at filerne kun er tilgængelige som vedhæftede filer. Når XML-filerne er flyttet til Blob-lageret, slettes de oprindelige filer fra Finance- eller Supply Chain Management-databasen. Det databaseområde, disse filer brugte, frigives derfor.

Hvis du vil aktivere funktionen **NF-e XML flytning som vedhæftet fil**, skal du følge disse trin.

1. Åbn arbejdsområdet **Funktionsstyring** i Finance eller Supply Chain Management.
2. Søg efter og vælg funktionen **NF-e XML flytning som vedhæftet fil** under fanen **Alle**.
3. Vælg **Aktiver nu**.

Følg disse trin for at flytte NF-e XML-filer som vedhæftede filer.

1. Gå til **Debitor** \> **Regnskabsdokumenter** \> **Elektroniske regnskabsdokumenter** \> **Flyt NF-e XML-filer som vedhæftede filer**.
2. Vælg start- og slutdatoerne i felterne **Fra dato** og **Til dato**.
3. Vælg en værdi i feltet **Skattekontor-id**.
4. Vælg **OK**.

> [!IMPORTANT]
> Processen kan ikke fortrydes. Når du har flyttet NF-e XML-filerne, kan brugerne kun få dem vist ved at vælge **Vedhæftede filer** øverst på siden **Regnskabsdokument**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
