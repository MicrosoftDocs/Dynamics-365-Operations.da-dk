---
title: Oprette avancerede regler for kladder
description: Denne procedure indeholder en trinvis gennemgang, hvordan du opretter avancerede regler for kladder.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd753d521dc4ad4c1e46bf51d9c1e4aa0ba02721
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832796"
---
# <a name="create-advanced-rules-for-journals"></a>Oprette avancerede regler for kladder

[!include [banner](../../includes/banner.md)]

Denne procedure indeholder en trinvis gennemgang, hvordan du opretter avancerede regler for kladder. Dette omfatter opsætning af kladdekontrol og brugerbogføringsbegrænsninger. Proceduren bruger USMF-demodatafirmaet.


## <a name="set-up-journal-control"></a>Opsæt kladdekontrol.
1. Gå i **Navigationsrude** til **Moduler > Finans > Konfiguration af kladde > Kladdenavne**.
2. Find og vælg den ønskede post på listen.
3. I **Handlingsruden** skal du klikke på **Kladdekontrol**.
4. Klik på **Tilføj** i oversigtspanelet **Hvilke kontotyper kan posteres?**.
5. Klik på rullelisten i feltet **Regnskaber** for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Klik på **Tilføj** i oversigtspanelet **Hvilke segmentværdier er gyldige denne kladde?**.
9. Klik på rullelisten i feltet **Kontostruktur** for at åbne opslaget.
10. Find og vælg den ønskede post på listen.
11. Klik op linket i den valgte række på listen.
12. Klik på rullelisten i feltet **Segment** for at åbne opslaget.
13. Klik op linket i den valgte række på listen.
14. Klik på rullelisten i feltet **Fra-værdi** for at åbne opslaget.
15. Find og vælg den ønskede post på listen.
16. Klik op linket i den valgte række på listen.
17. Klik på rullelisten i feltet **Til-værdi** for at åbne opslaget.
18. Find og vælg den ønskede post på listen.
19. Klik op linket i den valgte række på listen.

## <a name="set-up-posting-restrictions"></a>Angive bogføringsbegrænsninger
1. Luk siden.
2. Klik på **Bogføringsbegrænsninger**.
3. Vælg 'Pr. brugergruppe' i **Hvordan vil du indstille bogføringsbegrænsninger?**.
4. Markér 'den gruppe, du vil tillade bogføring af dette kladdenavn' i træet.
5. Klik på **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]