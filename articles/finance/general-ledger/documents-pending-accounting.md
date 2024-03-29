---
title: Dokumenter, der afventer regnskab
description: I denne artikel beskrives, hvordan du bruger funktionerne på siden Dokumenter, der afventer regnskab.
author: ryanCCarlson2
ms.date: 09/02/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: f37d46659b2fc5bf9933719811a7b90cc4e80f52
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709243"
---
# <a name="documents-pending-accounting"></a>Dokumenter, der afventer regnskab

[!include [banner](../includes/banner.md)]

I denne artikel beskrives, hvordan du bruger funktionerne på siden **Dokumenter, der afventer regnskab**.

I Microsoft Dynamics 365 Finance 10.0.30 er funktionen **Forbedret ydeevne for regnskabsstruktur for kildedokument** tilgængelig. Denne funktion forbedrer bogføringsprocesserne for dokumentbogføring af kildedokumenter startende med bogføringsprocessen for fritekstfakturaer.

Når denne funktion er aktiveret, bogføres reskontrodokumentet separat i forhold til processen til regnskabsgenerering eller processen *journalisering*, der opretter den komplette regnskabsdetalje, der overføres til finans. I bogføringsprocessen til fritekstfakturaer registreres debitorfakturaen f.eks. i modulet **Debitor**, før hele regnskabet genereres. Denne udvidede ydeevnefunktion gør det muligt at registrere debitorfakturaer hurtigere, mens generering af regnskaber forsinkes.

Følgende knapper er tilgængelige på siden **Dokumenter, der afventer regnskab**.

- **Generer regnskab** – Send et dokument, der i øjeblikket afventer oprettelse af en konto til journalisering.
- **Vis distributioner** – Få vist regnskabsfordelingerne for et valgt dokument på listen.
- **Vis fejllog** – Få vist eventuelle oplysninger om fejlmeddelelser, der findes for et dokument, hvor regnskabstilstanden angiver fejl. Du kan få vist de samme detaljer om fejlmeddelelsen ved at vælge linket **Fejllog** på dokumentlinjen.

Generering af regnskaber sker via en baggrundsproces for procesautomatisering, der kaldes **Regnskabsstrukturprocessor**. Du kan finde yderligere oplysninger om opsætning og konfiguration af alle automatiserede processer i [Procesautomatisering](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
