---
title: Sikkerhedsdiagnosticering for opgaveregistreringer
description: Denne artikel giver oplysninger om, hvordan du kan analysere og administrere krav til sikkerhedstilladelser på basis af en opgaveregistrering.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.search.form: ''
ms.openlocfilehash: e564a0499cb1a5dc00fc027c20a027f9b454600c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272514"
---
# <a name="security-diagnostics-for-task-recordings"></a>Sikkerhedsdiagnosticering for opgaveregistreringer

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Før du begynder

Denne artikel giver oplysninger om, hvordan du kan analysere og administrere krav til sikkerhedstilladelser på basis af en opgaveregistrering. Før du fuldfører trinnene i denne artikel, skal du have en opgaveregistrering for den forretningsproces, der skal analyseres. Du kan registrere en forretningsproces ved at se [Ressourcer for Arbejdsrutineoptager](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Administrere sikkerhed for en opgaveregistrering

1. Gå til **Systemadministration** > **Sikkerhed** > **Sikkerhedsdiagnosticering for opgaveregistrering**.
2. Åbn opgaveregistreringen fra dens placering. Vælg **Åbn fra denne pc** eller **Åbn fra Lifecycle Services**, og vælg derefter **Luk**.
3. Derved åbnes siden **Detaljer om sikkerhedsmenupunkter**, der viser de sikkerhedsobjekter, der kræves til processen.

 > [!NOTE]
 > Menupunkterne **Handling** og **Output** er ikke medtaget på listen.

4. Vælg en bruger i feltet **Bruger-id**. Hvis brugeren ikke har rettigheder til visse menupunkter, opdateres feltet **Manglende tilladelser** til **Ja**.
  
  ![Siden Detaljer om sikkerhedsmenupunkter.](../media/Security-Menu-Item-Details.png)

5. Vælg **Tilføj reference** for at få vist en liste over sikkerhedsobjekterne, herunder roller, pligter og rettigheder, der giver den manglende tilladelse.
6. Vælg et sikkerhedsobjekt på listen:

    - Hvis **Rolle** er valgt, skal du vælge **Føj rolle til bruger**. Derved åbnes siden **Tildel brugere roller**. Du kan finde flere oplysninger på siden [Tildele brugere til sikkerhedsroller](assign-users-security-roles.md).
    - Hvis **Pligt** er valgt, skal du vælge **Føj pligt til rolle**, vælge de roller, som pligten skal føjes til, og derefter vælge **OK**.
    - Hvis **Rettighed** er valgt, skal du vælge **Føj rettighed til pligter**, vælge de roller, som pligten skal føjes til, og derefter vælge **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
