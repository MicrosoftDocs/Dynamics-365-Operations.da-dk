---
title: Arbejdsgang for udgift
description: Dette emne forklarer, hvordan du kan bruge arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til at konfigurere en revisionsproces for udgiftsrapporter i Udgiftsstyring.
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d60d2f462a1fd27d4655e68aab7f96fb28a34b77
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="expense-workflow"></a>Arbejdsgang for udgift

[!include[banner](../includes/banner.md)]

Du kan bruge arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til at konfigurere en revisionsproces for udgiftsrapporter i Udgiftsstyring. Du kan angive en arbejdsgang, der bruger følgende kriterier til at bestemme, hvem der skal godkende udgiftsrapporter:

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

