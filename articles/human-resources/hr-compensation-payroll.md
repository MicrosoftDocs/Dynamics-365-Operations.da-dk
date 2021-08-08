---
title: Klar til at betale
description: I dette emne vises det, hvordan du markerer en medarbejder som klar til betaling i Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/13/2020
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
ms.openlocfilehash: f9aa9e60b51b1801c07981ad120cb77f65fee286
ms.sourcegitcommit: baad2723291774f610324a8054fc14abf3287fe1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/14/2021
ms.locfileid: "6560097"
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

1. Åbn **Kompensationsstyring**. Der er to felter i arbejdsområdet 
    - **Medarbejdere, der er klar til at betale**
    - **Medarbejdere, der ikke er klar til betaling**
    ![Arbejdsområdet for kompensationsstyring.](./media/hr-ready-to-pay-1-workspace.png)

2. Vælg feltet **Medarbejdere, der ikke er klar til betaling**.

3. Vælg de medarbejdere, der skal valideres. Vælg **Valider** under fanen **Løn** i gruppen **Klar til betaling**.
    ![Validere medarbejdere.](./media/hr-ready-to-pay-2-validate.png)

4. Hvis du vil gennemse resultaterne, skal du vælge **Resultater** under fanen **Løn** i gruppen **Klar til betaling**.

## <a name="validation"></a>Validering

Før en medarbejder markeres som klar til betaling, foretages der en grundlæggende validering af, om profilen er komplet.

![Valider resultaterne.](./media/hr-ready-to-pay-3-results.png)

Følgende tabel indeholder flere oplysninger om de enkelte valideringer, der er udført. 

| Validering | Detaljer |
| --- | --- |
| Parameter for adresseformål | Validerer, om parameteren **Brug formål med lønadresser** er aktiveret. |
| Lønadresse | Validerer, om arbejderprofilen har mindst én adresse med formålet "Bopælsplacering for løn" eller "Arbejdsplacering for løn", og der kun er én adresse pr. formål. |
| Ansættelse | Kontrollér, om arbejderen har mindst én ansættelse (nuværende, tidligere eller fremtidig). |
| Identifikationsnummer | Validerer, om parameteren "Brug identifikationstyper i lønbehandling" er angivet til Ja, og hvis den identifikationstype, der er angivet i parameteren, er angivet i arbejderprofilen. |
| For- og efternavn | Kontrollerer, om arbejderprofilen er gyldig, og kontrollerer, om felterne **Navn** og **Efternavn** er udfyldt.|
| Position | Kontrollér, om arbejderen har en tildelt stilling. |
| Fødselsdato | Kontrollerer, om arbejderprofilen er gyldig, og om feltet **Fødselsdag** er udfyldt. |
| Kompensation | Kontrollér, om arbejderen er tilmeldt en fast kompensationsplan. |

Hvis en af disse valideringer mislykkes, kan du ikke markere medarbejderen som klar til betaling.

Hvis feltet **Klar til betaling** er angivet til **Nej**, betyder det, at du skal udføre en handling for at sikre, at arbejderprofilen er komplet. Dette stopper ikke de data, der vises i en dataenhed. 

## <a name="known-issues"></a>Kendte problemer

- Du skal deaktivere funktionen **Strømlinet medarbejderangivelse** i funktionsstyring. Felterne i arbejdsområdet for kompensationsstyring fungerer ikke korrekt, hvis du bruger denne funktion.
- I arbejderformularen er fanen **Løn**, **Klar til betaling** tilgængelig for alle brugerroller. 

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
