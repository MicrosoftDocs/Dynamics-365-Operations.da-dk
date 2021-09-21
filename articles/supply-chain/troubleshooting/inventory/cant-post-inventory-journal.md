---
title: Arbejdsgang for lagerkladder fuldføres aldrig, og kladden kan ikke behandles
description: Når du har sendt en arbejdsgang for lagerkladdegodkendelse, stopper arbejdsgangsbehandlingen med at svare, og du kan ikke redigere eller behandle kladderne.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9430068f9c2d92c894817db04143297de6c6aa6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475866"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Arbejdsgang for lagerkladder fuldføres aldrig, og kladden kan ikke behandles

## <a name="symptoms"></a>Symptomer

Når du har sendt en arbejdsgang for lagerkladdegodkendelse, stopper arbejdsgangsbehandlingen med at svare, og du kan ikke redigere eller behandle kladderne.

## <a name="resolution"></a>Løsning

Der er flere årsager til, at arbejdsgangsbehandlingen muligvis ikke fuldføres. Kontrollér, om der er følgende problemer:

- Gå til **Lagerstyring &gt; Konfiguration &gt; Arbejdsgange for lagerstyring**, og gennemse konfigurationen af den berørte arbejdsgang. Du kan finde flere oplysninger i [Arbejdsgange for godkendelse af lagerkladde](/dynamics365/supply-chain/inventory/inventory-journal-workflow.md).
- Der kan opstå en undtagelse eller fejl i arbejdsgangen. Gennemse historikken for arbejdselementet for den berørte arbejdsgang for at se, om den omfatter en applikationsfejl, der afslutter arbejdsgangen.
- Lagerkladden kan kun opdateres eller redigeres, hvis den er godkendt. Hvis tilbagekaldelse er aktiv, kan du prøve at tilbagekalde kladden. Afviklingen af arbejdsgangsbatchjobbet kan være suspenderet af flere årsager. Nogle af disse årsager kan være forårsaget af problemer i arbejdsgangsstrukturen.
