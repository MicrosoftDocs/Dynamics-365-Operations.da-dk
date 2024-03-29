---
title: Oprette en arbejdstidskalender
description: Definer en arbejdstidskalender, feriedage og ikke-arbejdstider i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dac3ad583be9e4cbd6eacbc6d228819bd298628b
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323538"
---
# <a name="create-a-working-time-calendar"></a>Oprette en arbejdstidskalender


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I en arbejdstidskalender i Dynamics 365 Human Resources vises de dage og timer, hvor medarbejdere arbejder i organisationen. Når en medarbejder sender en anmodning om fritid, behøver de ikke at bekymre sig om helligdage og lukketider.

Hvis du vil strømline anmodninger om fritid, skal du konfigurere disse elementer for organisationen:

- Arbejdstidskalender
- Helligdage og lukninger
- Fritid

Du kan tilføje de sidste to elementer, mens du konfigurerer en arbejdstidskalender. Du kan også konfigurere eller opdatere dem separat.

## <a name="set-up-a-working-time-calendar"></a>Konfigurere en arbejdstidskalender

Konfigurer mindst én arbejdstidskalender, der viser arbejdsdagene og -timerne. Hvis du har adresser i flere lande og områder, kan det være en god ide at oprette en arbejdstidskalender for hvert område.

1. Vælg **Kalendere** på siden **Organisationsadministration**.

2. Vælg **Ny**, og angiv et navn og en beskrivelse for din nye kalender.

3. Under **Oprettelsesindstillinger** kan du vælge arbejdsdage for din organisation og angive arbejdstider. 
   - Hvis du vil tilføje en helligdag eller en lukning, skal du vælge knappen **Tilføj** ud for **Helligdage og lukninger**.
   - Hvis du vil tilføje ikke-arbejdstider, f.eks. frokostpauser, skal du vælge **Tilføj** under **Ikke-arbejdstid** og angive navnet og tidsintervallet.

4. Under **Dage** skal du vælge **Generér** for at generere dagene i kalenderen. Angiv datointervallet for kalenderen, og vælg derefter **Generér dage**.

5. Hvis du vil tilføje arbejdsplaner, skal du vælge **Tilføj** under **Arbejdsplan** og derefter angive tidspunkterne for hver enkelt arbejdsplan.

## <a name="configure-holidays-and-closures"></a>Konfigurere helligdage og lukninger

Du kan tilføje eller ændre helligdage og lukninger separat fra en arbejdstidskalender.

1. Vælg **Helligdage og lukninger** på siden **Organisationsadministration**.

2. Vælg **Ny**, og angiv et navn og en dato for helligdagen eller lukningen.

## <a name="configure-non-work-time"></a>Konfigurere fritid

Du kan tilføje eller ændre fritid separat fra en arbejdstidskalender.

1. Vælg **Fritid** på siden **Organisationsadministration**.

2. Vælg **Ny**, og angiv navnet og tidsintervallet for fritiden.

Hvis du har aktiveret prøvefunktionen til korrektion af helligdage i orlov og fravær, bruger Human Resources helligdage og lukningsdatoer til at bestemme det antal dage, der skal reguleres for medarbejdere, der er tilmeldt i kalenderen.

## <a name="see-also"></a>Se også

- [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)
- [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
