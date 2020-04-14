---
title: Arbejdsgang for udgiftsstyring
description: Dette emne forklarer, hvordan du kan bruge arbejdsgangssystemet i Microsoft Dynamics 365 Finance til at konfigurere en revisionsproces for udgiftsrapporter i Udgiftsstyring.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153965"
---
# <a name="expense-management-workflow"></a>Arbejdsgang for udgiftsstyring

[!include [banner](../includes/banner.md)]

Du kan bruge arbejdsgangssystemet til at oprette en revisionsproces for udgiftsrapporter i Udgiftsstyring. Du kan angive en arbejdsgang, der bruger følgende kriterier til at bestemme, hvem der skal godkende udgiftsrapporter:

- Medarbejderens rapporteringshierarki og foruddefinerede godkendelsesbegrænsninger
- Godkendelse med flere niveauer, der understøtter midlertidige godkendere og en endelig godkender
- Økonomiske dimensioner og projektansvar
- Tildeling til bestemte brugere eller brugergrupper

Der kan oprettes godkendelse af arbejdsgangen for udgiftsrapporter, rejserekvisitioner, kontante forskud og refusion af moms.

**Eksempel**

Nedenstående proces er et eksempel på udgiftsstyringsarbejdsgangen for en udgiftsrapport.

1. En medarbejder opretter og gemmer en udgiftsrapport.
2. Medarbejderen sender udgiftsrapporten til godkendelse. Godkenderen identificeres ud fra de regler, der blev defineret, da arbejdsprocessen blev konfigureret.
3. Godkenderen modtager en meddelelse om, at en udgiftsrapport er klar til godkendelse. Godkenderen gennemser udgiftsrapporten og kontrollerer, at følgende betingelser er opfyldt:

    - Udgifterne overtræder ikke nogen udgiftspolitikker. Hvis en udgift overtræder en politik, kontrollerer godkenderen, at udgiftsrapporten omfatter en gyldig forretningsberettigelse.
    - Der er knyttet elektroniske kvitteringer til udgiftsrapporten.

4. Godkenderen godkender udgiftsrapporten.
5. Udgiftsrapporten tildeles kreditorkoordinatoren for bogføring.
6. Et af følgende trin opstår, afhængigt af om der er konfigureret automatisk bogføring:

    - Hvis der er konfigureret automatisk bogføring, behandles udgiftsrapporten til betaling, og udgiftsrapportens status opdateres.
    - Hvis der ikke er konfigureret automatisk bogføring, kontrollerer kreditorkoordinatoren, at alle originale kvitteringer er indsendt, og at kvitteringerne svarer til udgifterne i udgiftsrapporten. Alle momskoder, der er angivet på udgiftsrapporten, skal også kontrolleres som korrekte.

Når opfyldelsen af disse krav er kontrolleret, kan du bogføre udgiftsrapporten.

Når udgiftsrapporten er bogført, godkendes betaling for udgiftsrapporten, og medarbejderen bliver refunderet.
