---
title: Nulstille kvitteringsnumre
description: Denne artikel beskriver, hvordan du nulstiller de kvitteringsnumre, der bruges til forskellige handlinger på den ønskede dato (f.eks. regnskabsåret eller kalenderåret).
author: ShalabhjainMSFT
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Application update 10.0.9
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, Commerce
ms.search.form: ''
ms.openlocfilehash: 3034a1b8f1a9f304b8d8803a7f906418321d81d9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272735"
---
# <a name="reset-receipt-numbers"></a>Nulstille kvitteringsnumre 

[!include [banner](includes/banner.md)]

> [!NOTE]
> Vi kræver, at du vælger egenskaben **Uafhængig sekvens** for alle kvitteringstyperne i funktionalitetsprofilen, før du bruger denne funktion. Desuden skal systemets tidszone for den enhed, hvor POS bruges, svare til butikkens tidszone. På grund af disse begrænsninger anbefales det, at du ikke bruger denne funktion i produktion, mens vi arbejder på at løse problemerne i en fremtidig version. 

Detailhandlere genererer kvitteringsnumre for forskellige handlinger i butikken, f.eks. kontanttransaktioner, returtransaktioner, kundeordrer, tilbud og betalinger. Selvom detailhandlere definerer deres egne kvitteringsformater, har visse lande eller områder forordninger, der har lagt begrænsninger på disse kvitteringsformater. Disse regler kan f.eks. begrænse antallet af tegn i kvitteringen, kræve fortløbende kvitteringsnumre, begrænse nogle specialtegn eller kræve nulstilling af kvitteringsnumrene i begyndelsen af året. Microsoft Dynamics 365 Commerce gør det nemmere at administrere kvitteringsnumre for at hjælpe forhandlerne med at overholde lovpligtige krav. Denne artikel forklarer, hvordan du kan bruge funktionerne til nulstilling af kvitteringsnumre.

I Commerce kan kvitteringsformater være alfanumeriske. Du kan indsætte både statisk indhold og dynamisk indhold i dem. Statisk indhold omfatter alfabetiske tegn, tal og specialtegn. Dynamisk indhold omfatter et eller flere tegn, der repræsenterer oplysninger som butiksnummer, terminalnummer, dato, måned, år og nummerserier, der øges automatisk. Formaterne defineres i sektionen **Kvitteringsnummerering** i funktionalitetsprofilen. I følgende tabel beskrives de tegn, der repræsenterer det dynamiske indhold.

| Tegn | Beskrivelse |
|------------|-------------|
| S          | Tegnet **S** bruges til butiksnummeret. Hvis f.eks. en butik er nummereret HOUSTON1, viser formatet **SSS** "ON1" i kvitteringen. Formatet **SSSSS** viser "STON1" i kvitteringen. |
| T          | Tegnet **T** bruges til terminalnummeret. Hvis f.eks. en terminal er nummereret 0001, viser formatet **TTTT** "0001" i kvitteringen. |
| C          | Tegnet **C** bruges til medarbejders id-nummer. Hvis en medarbejder f.eks. har ID 000160, viser formatet **CCCC** "0160" på kvitteringen. |
| ddd        | Tegnene **ddd** svarer til årets dag fra 1 til 366. F.eks. vil 15. januar med formatet **ddd** vise "015" i kvitteringen. |
| MM         | Tegnene **MM** bruges til den tocifrede måned. F.eks. vil januar med formatet **MM** vise "01" i kvitteringen. |
| DD         | Tegnene **DD** bruges til den tocifrede dag i måneden. F.eks. vil 15. januar med formatet **DD** vise "15" i kvitteringen. |
| YY         | Tegnene **YY** bruges til det tocifrede årstal. I en måned i år 2020 viser formatet **YY** f.eks. "20" på kvitteringen. |
| \#         | Et nummertegn (**\#**) bruges til fortløbende nummerering. F.eks. vil viser formatet **####** "0001," "0002," "0003" osv. i kvitteringen. |

Du kan nulstille den fortløbende nummerering af kvitteringen på en bestemt dato. Derefter nulstiller systemet kvitteringsnummerserien til 1 for den første transaktion, der finder sted efter kl. 12:00 midnat på den valgte nulstillingsdato. Du kan også angive, om nulstillingen kun skal foretages én gang, eller om den skal gentages hvert år. Hvis der er angivet årlig gentagelse, sker nulstillingen automatisk hvert år, indtil forhandleren vælger at stoppe den. 

Udfør følgende trin for at aktivere nulstilling.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**.
1. Vælg **Nulstil dato for nulstilling af nummer** i oversigtspanelet **Kvitteringsnummerering**.
1. Vælg en fremtidig dato, hvor nulstillingen skal finde sted, i feltet **Nulstillingsdato** i dialogboksen.
1. I feltet **Nulstil kvittering-type** skal du vælge **Kun engangs** eller **Årligt**.
1. Vælg **OK**.

![Vælge en nulstillingsdato for kvittering.](media/Enable_receipt_reset.png "Vælge en nulstillingsdato for kvittering")

Når du har valgt en dato, vises den i kolonnen **Næste dato for nulstilling af kvitteringsnummer**. Nulstillingsdatoen gælder for alle kvitteringstransaktionstyper. Derfor nulstilles kvitteringsnummerserien for alle kvitteringstyper.

Når nulstillingsdatoen er kommet, nulstilles kvitteringsnummeret for den første transaktion af hver type. I funktionalitetsprofilen flyttes nulstillingsdatoen desuden fra kolonnen **Næste dato for nulstilling af kvitteringsnummer** til **Nuværende dato for nulstilling af kvitteringsnummer**. Denne ændring angiver, at hvis der ikke bruges en kasse på nulstillingsdatoen, vil kvitteringsnummeret blive nulstillet, næste gang kasseapparatet *er* i brug. F.eks. skal du 3. december 2019 vælge **1. januar 2020** som nulstillingsdato. Den 1. januar, når kasseapparatet foretager den første transaktion, nulstilles kvitteringsnummeret. Ét kasseapparat bruges dog ikke i hele december og januar, men begynder derefter at blive brugt i februar. Da der i dette tilfælde er defineret en nulstillingshandling, nulstilles kvitteringsnummeret for den pågældende kasse, når kassen foretager den første transaktion i februar.

Du kan bruge funktionen **Ryd nulstillingsdato** til at rydde fremtidige nulstillingsdatoer. Men hvis nulstillingsdatoen er i fortiden, kan den ikke fortrydes. Derfor vil nulstillingen blive foretaget for alle kasseapparater, hvor der endnu ikke er foretaget nulstilling.

> [!NOTE]
> Afhængigt af, hvilken nulstillingsdato du har valgt og kvitteringsformatet, kan du have dublerede kvitteringsnumre. Selvom POS-systemet kan håndtere disse situationer, øger de den tid, der kræves for at behandle returneringer, da salgsmedarbejderne skal vælge blandt de dublerede kvitteringer. Andre komplikationer, der er relateret til dataoprydning, kan forekomme, hvis de dublerede kvitteringer ikke var en planlagt konsekvens. Det anbefales derfor, at du bruger dynamiske datotegn (f.eks **ddd**, **MM**, **DD** og **YY**) for at forhindre dublerede kvitteringsnumre efter nulstilling.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
