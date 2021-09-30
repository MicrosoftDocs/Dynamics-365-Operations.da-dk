---
title: Klar til at betale
description: I dette emne vises det, hvordan du markerer en medarbejder som klar til betaling i Dynamics 365 Human Resources.
author: marcelbf
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 80bba5446eb7a87d96a7da4ae856cb5ca114ce52
ms.sourcegitcommit: 24e20b3b96834b23311f1bf5dbab28baf3323728
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2021
ms.locfileid: "7483776"
---
# <a name="ready-to-pay"></a>Klar til at betale

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

> [!NOTE]
> Hvis du vil markere en medarbejder som klar til betaling, skal du først aktivere funktionen **(Forhåndsversion) lønintegration** i funktionsstyring. Du kan finde flere oplysninger om aktivering af prøveversionsfunktioner i [Administrere funktioner](hr-admin-manage-features.md).

Denne funktion gør det muligt for personalemedarbejderne at forstå, hvilke medarbejdere der er klar til lønbehandling, og hvilke der kræver handling, før de kan forbruges af en anden lønudbyder.

## <a name="mark-employee-as-ready-to-pay"></a>Markere medarbejder som klar til betaling

Indsamling og validering af medarbejderoplysninger kan være tidskrævende og fejlbehæftede. Ved at give personalemedarbejdere mulighed for at gennemse og nemt opdatere medarbejderoplysninger, kan Dynamics 365 Human Resources reducere tidsforbruget til klargøring af lønudbetalingen.

Sådan markeres en medarbejder som klar til betaling:

1. Åbn **Kompensationsstyring**. Der er to felter i arbejdsområdet: 
    - **Medarbejdere, der er klar til at betale**
    - **Medarbejdere, der ikke er klar til betaling**
    ![Arbejdsområdet for kompensationsstyring.](./media/hr-ready-to-pay-1-workspace.png)

2. Vælg feltet **Medarbejdere, der ikke er klar til betaling**.

3. Vælg de medarbejdere, der skal valideres. Vælg **Valider** under fanen **Løn** i gruppen **Klar til betaling**.
    ![Validere medarbejdere.](./media/hr-ready-to-pay-2-validate.png)

4. Hvis du vil gennemse resultaterne, skal du vælge **Resultater** under fanen **Løn** i gruppen **Klar til betaling**.

## <a name="validation"></a>Validering

Før en medarbejder markeres som klar til betaling, foretages der en validering af, om medarbejderprofilen er komplet.

![Valider resultaterne.](./media/hr-ready-to-pay-3-results.png)

| Validering | Detaljer |
| --- | --- |
| **Parameter for adresseformål** | Bekræfter, at parameteren **Brug formål med lønadresser** er valgt. |
| **Lønadresse** | Bekræfter, at arbejderprofilen har mindst én adresse med formålet **Bopælsplacering for løn** eller **Arbejdsplacering for løn**, og der kun er én adresse pr. formål. |
| **Ansættelse** | Bekræfter, at arbejderen har mindst én ansættelse (nuværende, tidligere eller fremtidig). |
| **Identifikationsnummer** | Bekræfter, at feltet **Brug identifikationstyper i lønbehandling** er angivet til **Ja** på siden **Human Resources-parametre**, og om den identifikationstype, der er angivet i parameteren, er udfyldt i arbejderprofilen. |
| **For- og efternavn** | Bekræfter, at felterne **Navn** og **Efternavn** er udfyldt.|
| **Stilling** | Bekræfter, at en stilling er tildelt arbejderen. |
| **Fødselsdato** | Bekræfter, at feltet **Fødselsdag** er udfyldt. |
| **Kompensation** | Bekræfter, at arbejderen er tilmeldt en fast kompensationsplan. |

Hvis en af disse valideringer mislykkes, kan du ikke markere medarbejderen som klar til betaling.

Hvis feltet **Klar til betaling** er angivet til **Nej**, betyder det, at du skal udføre en handling for at sikre, at arbejderprofilen er komplet. Dette stopper ikke de data, der vises i en dataenhed. 

## <a name="known-issues"></a>Kendte problemer

- Du skal deaktivere funktionen **Strømlinet medarbejderangivelse** i funktionsstyring. Felterne i arbejdsområdet for kompensationsstyring fungerer ikke korrekt, hvis du bruger denne funktion.
- Under fanen **Løn** på siden **Arbejder** er gruppen **Klar til betaling** tilgængelig for alle brugerroller. 

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
