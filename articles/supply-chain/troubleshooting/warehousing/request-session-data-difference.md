---
title: Uventet difference mellem anmodnings- og sessionsdata under test
description: Der forekommer en uventet difference mellem anmodnings- og sessionsdata i valideringsresultaterne for opgaver i lagerstedsappen.
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456934"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>Uventet difference mellem anmodnings- og sessionsdata under test

Fejlkode: WarehouseMobileDeviceRequestInputValidationError

## <a name="symptoms"></a>Symptomer

Når du bruger [valideringsstruktur til opgaver i lagerstedsappen](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat), returnerer valideringen følgende fejlmeddelelse:

> Uventet difference mellem anmodnings- og sessionsdata. XML-protokol for lagersteders mobilenheder overtrædes. REQUEST_XML_TAMPERING

## <a name="cause"></a>Årsag

Fejlen opstår, når outputtet for det sidste trin, der blev kørt korrekt i testkørslen, ikke svarer til det registrerede input til næste trin. Denne situation kan opstå, fordi valideringen af opgaven ikke bruger output af et tidligere trin som input til et efterfølgende trin. Den bruger i stedet registreret XML som input for hvert trin.

I de fleste tilfælde opstår fejlen, når du kører en opgave igen, men testen kræver visse poster, der er blevet ændret eller fjernet af en tidligere kørsel af samme opgave.

## <a name="resolution"></a>Løsning

Valideringstestkørslen af opgaven i lagerstedsappen er ikke en redundant operation, men ændrer de underliggende data. Derfor skal du muligvis nulstille de relevante data, før du kører en opgave igen.

1. Gennemse XML-outputtet for det sidste testtrin, der lykkedes, for at finde ud af, hvor testkørslen var kommet til.
1. Kontrollér testen, og sørg for, at alle nødvendige salgsordrer, flytteordrer, arbejdshoveder og andre poster stadig er til stede og i den forventede tilstand.
1. Genopret eller rediger de manglende eller ændrede poster. Du kan også oprette en ny testopsætning og designe testen, så der bruges gyldige eksisterende poster.
