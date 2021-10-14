---
title: Nulstil Dataverse-synkronisering
description: Dette emne beskriver, hvordan der foretages fejlfinding af poster, som ikke synkroniseres korrekt mellem Microsoft Dynamics 365 Human Resources og HCM (Human capital management) Fælles løsning i Microsoft Dataverse.
author: jaredha
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-27
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d88f538fbf22313feaca6771b7cb1757a3c3fbad
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559634"
---
# <a name="reset-dataverse-synchronization"></a>Nulstil Dataverse-synkronisering

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Emne

Poster synkroniseres ikke mellem Microsoft Dynamics 365 Human Resources og enhederne i HCM (Human Capital Management) Under Fælles løsning i Microsoft Dataverse. Du kan få flere oplysninger om synkronisering ved at gå til [Konfigurer Dataverse-integration](hr-admin-integration-common-data-service.md). Der kan opstå fejl under den korrekte synkronisering, når **Dataverse-integrationens forsøg på at udføre** eller **Dataverse-integrationen af manglende synkroniseringsbatchjob** til anmodninger bliver sat i forbindelse med **udførelse**.

## <a name="resolution"></a>Løsning

Der kan opstå fejl under den korrekte synkronisering, når **Dataverse-integrationens forsøg** på at udføre eller **Dataverse-integrationen af manglende synkroniseringsbatchjob** til anmodninger bliver sat i forbindelse med **Udførelse** eller **Annullering**, kan du nulstille status. Dette kan du gøre ved at annullere batchjobbet ved at følge retningslinjerne for Nulstil [batchjob, der sidder fast](hr-admin-troubleshooting-batch-execution.md). Når du har annulleret batch-jobbet, kan du nulstille batchjobbet ved at indstille det til **Venter**-status. Batchjobbet køres derefter i forbindelse med den næste planlagte kørselstid.

1. Hvis du ikke allerede har gjort det, skal du aktivere funktionen til **udvidet batchafbrydelse** i **funktionsstyring**.
   1. Gå til siden **Funktionsstyring** (**Systemadministration** > **Oversigt** > **Funktionsstyring**).
   2. Vælg fanen **Alle**.
   3. Marker kolonnen **Funktionsnavn**, og filtrer efter **Udvidet batchafbrydelse**.
   4. Vælg handlingen **Aktiver**, hvis den ikke allerede er aktiveret.

2. Sluk Dataverse-integration.
   1. Gå til **Microsoft Dataverse-integrationssiden** (**Systemadministration** gå til **Links** > **Integrationer** > **Dataverse-konfiguration**).
   2. Angiv indstillingen **Aktivér Dataverse-integration** til **Nej**.

3. Annuller batch-jobbet **Forsøg Dataverse-integration igen**.
   1. Gå til siden **Batch-jobs** (**Systemadministration** gå til **Links** > **Batch-jobs** > **Batch-jobs**).
   2. Filtrer kolonnen **Jobbeskrivelse** efter **integration**.
   3. Vælg batch-jobbet **Forsøg Dataverse-integration igen**.
   4. Vælg **Batchjob**, **Gennemtving annullering** på handlingsbåndet, og vælg derefter **Ja**, der skal bekræftes.

   > [!NOTE]
   > Afhængigt af, hvornår integrationen blev aktiveret første gang, kan batchjobbet forsøge at genaktivere **Common Data Service-integrationsbeskrivelse**. Vælg dette batchjob, hvis det er angivet, i stedet for batchjobbet **Dataverse-genintegrere**.

4. Slet alle Dataverse-integrationsbatchjob.
   1. På siden **Batchjob** skal du vælge synkronisering af manglende **Dataverse-integrationsanmodning**, **Dataverse-genintegration** og første synkronisering af **Dataverse-integration** for batchjob.
   2. Vælg **Skift status** på handlingsbåndet. 
   3. Vælg **Tilbagehold**, og vælg derefter **OK**.
   4. Vælg **Slet-handling**, og vælg derefter **Ja** for at bekræfte handlingen.

5. Aktivere Dataverse-integrationsbatchjobbene.
   1. Gå til **Microsoft Dataverse-integrationssiden** (**Systemadministration** > **Links** > **Integration** > **Dataverse-konfiguration**).
   2. Angiv indstillingen **Aktivér Dataverse-integration** til **Ja**.

6. Gå til siden **Batchjob**, og bekræft, at du har oprettet **Dataverse-integrationsforsøg igen** og **Dataverse-integration mistet anmodning af synkronisering** batch-jobs.

Når batchjobbene er genoprettet, kan du nu overvåge **Dataverse-integrationsforsøg igen**-batch-job for at se, hvor lang tid det tager at udføre jobbet. Du kan derefter kontrollere, at posterne synkroniseres korrekt til HCM Common-løsningen i Microsoft Dataverse.

## <a name="see-also"></a>Se også

[Konfigurere Dataverse-integration](hr-admin-integration-common-data-service.md)<br>
[Nulstille fastsiddende batchjob](hr-admin-troubleshooting-batch-execution.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
