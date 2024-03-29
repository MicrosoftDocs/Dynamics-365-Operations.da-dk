---
title: Antal bøger pr. kladde
description: Denne artikel beskriver forholdet mellem kladder og anlægsaktivbøger, når du opretter et anlægsaktivanskaffelse eller et afskrivningsforslag via et batchjob. Du kan definere det maksimale antal kartoteker, der er inkluderet for hver anskaffelse, og til afskrivning.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2dbd50963cf13f00e09b82e884cd8ebc0b67d424
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883323"
---
# <a name="number-of-books-per-journal"></a>Antal bøger pr. kladde

[!include [banner](../includes/banner.md)]

Denne artikel beskriver forholdet mellem kladder og anlægsaktivbøger, når du opretter et anlægsaktivanskaffelse eller et afskrivningsforslag via et batchjob. Du kan definere det maksimale antal kartoteker, der er inkluderet for hver enkelt anskaffelse og for afskrivning ved hjælp af felterne i **Antal kartoteker pr. kladde** under fanen **Generelt** på siden **Parametre til anlægsaktiver** (**Anlægsaktiver \> Konfiguration \> Struktur for anlægsaktiver**). Du kan bruge disse felter til at fordele antallet af anlægskartoteker pr. anskaffelseskladde og en afskrivningskladde.

I forbindelse med et anskaffelsesforslag er standardværdien mindst 10.000 bøger. I forbindelse med et afskrivningsforslag er standardværdien mindst 2.000 kartoteker.

Hvis der f. eks. er 4.000 anlægsaktiver, og der er knyttet to kartoteker til hvert enkelt anlægsaktiv, bogføres det ene kartotek i det aktuelle lag, og det andet kartotek bogføres på momslaget. Hvis du anskaffer 4.000 anlægsaktiver via batchafvikling, vil det batchjob, der opretter en anskaffelseskladde for anlægsaktiver, indeholde 4.000 anlægskartoteker.

> [!NOTE]
> Den kladde, der er oprettet, vil fortsat blive brugt, indtil kørslen er fuldført.
>
> De afledte kartoteker indgår ikke i det maksimale antal kartoteker pr. kladde.

Du kan bruge batchafvikling til at køre afskrivning for det samme sæt anskaffede aktiver. Et batchjob opretter f. eks. to afskrivningskladder, der hver består af 2.000 anlægskartoteker. Den første kladde vil indeholde de kartoteker, der er knyttet til anlægsaktiverne med numrene 1 til 2.000. Den anden kladde vil indeholde de kartoteker, der er knyttet til anlægsaktiverne med numrene 2.001 til 4.000.

Batchafviklingsjobbet udelader lukkede kartoteker. I et batchjob til afskrivning lukkes f. eks. 10 af de første 2.000 kartoteker. Den første kladde vil således indeholde de kartoteker, der er knyttet til anlægsaktiverne med numrene 1 til 2.011. Den anden kladde vil indeholde de kartoteker, der er knyttet til anlægsaktiverne med numrene 2,012 til 4.000.

> [!NOTE]
> Hvis du har anlægsaktiv-id'er med forskellige separatorer (som f.eks. – eller /), og du opretter anlægsaktivposteringer i batchjob, skal du køre et separat batchjob for hver type separator. Systemet kan ikke behandle forskellige separatorer i det samme batchjob.

Grænsen for antallet af kartoteker anvendes, hvis der ikke findes identiske anlægs-id'er i samme kladde. Men hvis aktiv-id'et er det samme som det bogførte ID, kan antallet af kartoteker pr. kladde overskrides for at beholde aktiv-id'et i samme kladde.

Der er f. eks. 5.001 anlægsaktiv-id'er, der knyttes tre kartoteker til hvert anlægsaktiv-ID, og hver enkelt anlægs model bogføres på samme posteringslag. Du kører afskrivning for tre på hinanden følgende måneder uden opsummering.  Afskrivningskladden oprettes via et batchjob, og der oprettes syv kladder med 667 anlægsaktiv-id'er og tre kartoteker for hvert anlægsaktiv-ID. Resultatet vil være 2.001 kartoteker. I tre måneder vil der derfor være 6.003 kladdelinjer til at vedligeholde samme anlægs-id'er i samme kladde. Der oprettes også én kladde med 332 anlægsaktiv-id'er og tre kartoteker for hvert anlægsaktiv-ID. Inden for tre måneder vil der være 2.988 linjer.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
