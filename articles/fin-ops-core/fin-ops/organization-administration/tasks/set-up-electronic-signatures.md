---
title: Opsætning af elektroniske signaturer
description: Brug denne procedure til at konfigurere elektroniske signaturer.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 314f48fcac32793c96466ee807d5685e596193b1
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796652"
---
# <a name="set-up-electronic-signatures"></a>Opsætning af elektroniske signaturer

[!include [banner](../../includes/banner.md)]

Brug denne procedure til at konfigurere elektroniske signaturer. En elektronisk signatur bekræfter identiteten på en person, som skal starte eller godkende en computerproces. Det demodatafirma, der bruges til at oprette denne procedure, er DAT.


## <a name="enable-the-electronic-signature-configuration-key"></a>Aktiver konfigurationsnøglen for elektronisk signatur
1. Gå til Systemadministration > Opsætning > Licenskonfiguration.
2. Udvid "Administration" i træet.
    * Kontroller, at afkrydsningsfeltet Elektronisk signatur markeret.  
    * Hvis afkrydsningsfeltet Elektronisk signatur ikke er markeret, skal du aktivere vedligeholdelsestilstand. Vedligeholdelsestilstand kan aktiveres i dette miljø ved at køre et vedligeholdelsesjob fra Lifecycle Services eller lokalt ved hjælp af værktøjet Deployment.Setup.  
3. Luk siden.

## <a name="set-up-electronic-signature-parameters"></a>Konfigurere parametre for elektronisk signatur
1. Gå til Virksomhedsadministration > Opsætning > Elektronisk signatur > Parametre for elektronisk signatur.
2. Klik på Rediger.
3. Skriv en værdi i feltet Meddelelse.
    * Indtast den besked, som underskrivere vil få, når der kræves en signatur. Du kan indtaste en hvilken som helst tekst. Typisk fortæller denne tekst brugeren, hvad det at signere et dokument elektronisk betyder.  
    * Hvis du vil indtaste beskedteksten på flere sprog, skal du klikke på knappen Oversættelser.  
4. Klik på Gem.
5. Luk siden.

## <a name="set-up-reason-codes-for-electronic-signatures"></a>Konfigurere årsagskoder for elektroniske signaturer
1. Gå til Virksomhedsadministration > Opsætning > Elektronisk signatur > Årsagskoder for elektronisk signatur.
2. Klik på Ny.
    * Du skal angive årsagskoder, før du bruger elektroniske signaturer. Der kræves en gyldig årsagskode, når du signerer et dokument.     En underskriver vælger en årsagskode, som angiver formålet med en elektronisk signatur. En årsagskode kan f.eks. bruges til at angive juridisk godkendelse.  
3. Skriv en værdi i feltet Årsagskode.
4. Skriv en værdi i feltet Beskrivelse.
    * Angiv flere årsagskoder, hvis det er nødvendigt.  
5. Klik på Gem.
6. Luk siden.

## <a name="require-electronic-signatures-for-existing-processes"></a>Krav om elektroniske signaturer for eksisterende processer
1. Gå til Virksomhedsadministration > Opsætning > Elektronisk signatur > Elektronisk signatur-krav.
2. Find og vælg den ønskede post på listen.
    * Vælg en proces, der kræver elektroniske signaturer.  
3. Marker eller fjern markeringen i afkrydsningsfeltet Signatur er påkrævet efter behov.
    * Gentag disse trin for hver proces, der kræver elektroniske signaturer.  
4. Klik på Gem.

## <a name="create-a-custom-requirement-for-electronic-signatures"></a>Opret et brugerdefineret krav om elektroniske signaturer
1. Klik på Ny.
2. Marker eller fjern markeringen i afkrydsningsfeltet Signatur er påkrævet efter behov.
3. I feltet Navn skal du angive et navn til den proces, der kræver elektroniske signaturer.
4. Klik på rullelisten i feltet Tabelnavn for at åbne opslaget.
5. På listen skal du finde og vælge den tabel, hvor de data, der skal signeres, er gemt.
6. Klik op linket i den valgte række på listen.
7. Klik på rullelisten i feltet Feltnavn for at åbne opslaget.
8. På listen skal du finde og vælge det felt i tabellen, som du vil overvåge.
9. Klik op linket i den valgte række på listen.
    * Angiv, hvornår der kræves en signatur.     Vælg Altid, hvis en signature kræves, når dataene i feltet ændres.     Vælg Kun, hvis der kun kræves en signatur under visse omstændigheder. Hvis du vælger Kun, skal du også vælge en af følgende indstillinger: Når der indsættes en post, Når en post opdateres eller Når en post slettes.  
10. Klik på Gem.
11. Luk siden.

