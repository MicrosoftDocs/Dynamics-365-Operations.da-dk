---
title: Sikkerhedsdiagnosticering for opgaveregistreringer
description: Dette emne giver oplysninger om, hvordan du kan analysere og administrere krav til sikkerhedstilladelser på basis af en opgaveregistrering.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 88eb90b35f1a9754cc4daa01d8f40cdf712db4f8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679784"
---
# <a name="security-diagnostics-for-task-recordings"></a>Sikkerhedsdiagnosticering for opgaveregistreringer

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Før du begynder

Dette emne giver oplysninger om, hvordan du kan analysere og administrere krav til sikkerhedstilladelser på basis af en opgaveregistrering. Før du fuldfører trinnene i dette emne, skal du have en opgaveregistrering for den forretningsproces, der skal analyseres. Du kan registrere en forretningsproces ved at se [Ressourcer for Arbejdsrutineoptager](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Administrere sikkerhed for en opgaveregistrering

1. Gå til **Systemadministration** > **Sikkerhed** > **Sikkerhedsdiagnosticering for opgaveregistrering**.
2. Åbn opgaveregistreringen fra dens placering. Vælg **Åbn fra denne pc** eller **Åbn fra Lifecycle Services**, og vælg derefter **Luk**.
3. Derved åbnes siden **Detaljer om sikkerhedsmenupunkter**, der viser de sikkerhedsobjekter, der kræves til processen.

 > [!NOTE]
 > Menupunkterne **Handling** og **Output** er ikke medtaget på listen.

4. Vælg en bruger i feltet **Bruger-id**. Hvis brugeren ikke har rettigheder til visse menupunkter, opdateres feltet **Manglende tilladelser** til **Ja**.
  
  ![Siden Detaljer om sikkerhedsmenupunkter](../media/Security-Menu-Item-Details.png)

5. Vælg **Tilføj reference** for at få vist en liste over sikkerhedsobjekterne, herunder roller, pligter og rettigheder, der giver den manglende tilladelse.
6. Vælg et sikkerhedsobjekt på listen:

    - Hvis **Rolle** er valgt, skal du vælge **Føj rolle til bruger**. Derved åbnes siden **Tildel brugere roller**. Du kan finde flere oplysninger på siden [Tildele brugere til sikkerhedsroller](assign-users-security-roles.md).
    - Hvis **Pligt** er valgt, skal du vælge **Føj pligt til rolle**, vælge de roller, som pligten skal føjes til, og derefter vælge **OK**.
    - Hvis **Rettighed** er valgt, skal du vælge **Føj rettighed til pligter**, vælge de roller, som pligten skal føjes til, og derefter vælge **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]