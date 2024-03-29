---
title: Behandle tilmeldingsberettigelse
description: I denne artikel beskrives, hvordan du kan køre processen til berettigelse af tilmelding.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bd05585f691a4c6aa55a7aec7ceaaf0273f0abcb
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323475"
---
# <a name="process-enrollment-eligibility"></a>Behandle tilmeldingsberettigelse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I denne artikel beskrives, hvordan du kan køre processen til berettigelse af tilmelding.

1. Vælg **Behandling af berettigelse til tilmelding** under **Behandling** i arbejdsområdet **Frynsegodeadministration**.

2. Angiv værdier for følgende felter i dialogboksen **Kør behandling af berettigelse til frynsegodetilmelding**:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Tilmeldingsperiode** | Den tilmeldingsperiode, der skal behandles berettigelse til tilmelding for. |
   | **Juridisk enhed** | Den juridiske enhed, der skal behandles berettigelse til tilmelding for. |
   | **Arbejdstråd** | Den arbejder, der skal behandles berettigelse til tilmelding for. Hvis du ikke udfylder dette felt, behandles berettigelsen til tilmelding for alle arbejdere. |
   | **Frynsegodeplan** | Den frynsegodeplan, der skal behandles berettigelse til tilmelding for.

3. Hvis du vil køre processen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:

   1. Angiv oplysninger om processen.

   2. Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.

   3. Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.

   4. Vælg **OK**. Processen køres med de parametre, du angiver.

4. Vælg **OK**.

## <a name="view-process-results"></a>Vis procesresultater

I denne artikel beskrives, hvordan du få vist resultater af berettigelsesprocessen.

1.  Vælg **Procesresultater** under **Behandling** i arbejdsområdet **Administration af frynsegoder**.

2.  Følgende felter er angivet på siden **Procesresultater**:

   | Felt | Betegnelse |
   | --- | --- |
   | **Proces-id** | Det entydige id for kombinationen af Arbejder, Juridisk enhed og Proceskørsel. |
   | **Procestype** | Det identificerer den proces, der blev kørt. Eksempel: Tilmelding. |
   | **Registreringstidspunkt** | Det tidspunkt, hvor berettigelsesprocessen blev kørt. |
   | **Juridisk enhed** | Den juridiske enhed, der er angivet under tilmeldingsprocessen. |
   | **Arbejdstråd** | Den arbejder, der blev behandlet. |
   | **Plan | Den frynsegodeplan, som tilmeldingen blev forsøgt for. |
   | **Berettigelsesregel** | Den berettigelsesregel, der blev behandlet. Hvis der blev fundet en fejl, før berettigelsen blev kørt, vil dette felt være tomt. Eksempel: Hvis der ikke er defineret kompensation for en arbejder, vil berettigelsesprocessen ikke blive kørt, og dette felt vil være tomt. |
   | **Resultatstatus** | Det vil være Berettiget eller Ikke-berettiget. Resultatstatussen vil være Ikke-berettiget, hvis arbejderen ikke opfylder kriterierne for berettigelsesreglen, hvis arbejderen mangler påkrævede oplysninger som f.eks. en betalingsfrekvens eller fast løn, eller hvis der mangler oplysninger i frynsegodeplanen, der forhindrer, at arbejdere kan tilmeldes. |
   | **Resultatmeddelelse** | Angiver, hvorfor en arbejder ikke er berettiget til en frynsegodeplan, eller hvis berettigelsesreglen er overført. |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
