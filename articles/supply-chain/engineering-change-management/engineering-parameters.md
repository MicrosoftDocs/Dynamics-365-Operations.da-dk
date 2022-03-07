---
title: Parametre for styring af teknisk ændring
description: I dette emne beskrives det, hvordan du konfigurerer teknisk ændringsstyring for Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d5cf6826aa44e27fae989c73d87d2d3687e0cd0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262279"
---
# <a name="engineering-change-management-parameters"></a>Parametre for styring af teknisk ændring

[!include [banner](../includes/banner.md)]

Siden **Parametre for styring af teknisk ændring** indeholder de opsætningsparametre, der ændrer den standardfunktionsmåde, der er relateret til processerne for frigivelse af produktstruktur og styring af tekniske ændringer.

## <a name="open-the-engineering-change-management-parameters-page"></a>Åbn siden Parametre for styring af tekniske ændringer

Hvis du vil åbne siden **Parametre for styring af tekniske ændringer**, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Parametre for styring af tekniske ændringer**. Du kan derefter angive felterne som beskrevet i de øvrige afsnit i dette emne.

## <a name="release-control-tab"></a>Fanen Frigiv styring

I følgende tabel beskrives de felter, der er tilgængelige under fanen **Frigiv styring** på siden **Parametre for styring af tekniske ændringer**. Disse felter har indflydelse på frigivelsesprocessen for produktstrukturen.

| Felt | Beskrivelse |
|---|---|
| Varenummerregel | Vælg, hvordan varenummeret skal defineres, når produktet frigives til en juridisk enhed. Vælg *Teknisk produktnummer*, hvis produktnummeret i den modtagende juridiske enhed skal svare til produktnummeret i den tekniske virksomhed. Vælg *Lokal varenummerserie*, hvis produktet skal tage det næste nummer i nummerserien for produktnumre i den modtagende juridiske enhed. |
| Regel for styklistenavn | Vælg, hvordan navnet på styklisten skal defineres, når produktet modtages (frigives) i en juridisk enhed. Vælg enten *Teknisk navn* eller *Modtaget varenummer*. |
| Regel for rutenavn | Vælg, hvordan rutenavnet skal defineres, når produktruten modtages (frigives) i en juridisk enhed. Vælg enten *Teknisk navn* eller *Modtaget varenummer*. |
| Kør styklistekontrol | Vælg, om der skal køres en styklistekontrol, når produktet modtages (frigives) i en juridisk enhed. |
| Frigivelsesfunktionalitet for inaktive styklister | Vælg, om et produkt kan frigives, hvis det har en inaktiv stykliste. Vælg *Acceptér*, *Kun advarsel* eller *Ikke tilladt*. |
| Frigivelsesfunktionalitet for inaktive ruter | Vælg, om et produkt kan frigives, hvis det har en inaktiv rute. Vælg *Acceptér*, *Kun advarsel* eller *Ikke tilladt*.|
| Produktgodkendelse | Vælg, om der kræves et ekstra trin til godkendelse, før produktet kan frigives i den juridiske enhed. Vælg *Manuel* for at tilføje accepttrinnet. I dette tilfælde vil siden **Åbne produktfrigivelser** vise produkterne. Vælg *Automatisk* for at få vist produktet direkte på siden **Frigivne produkter** i den juridiske destinationsenhed, umiddelbart efter at produktet er frigivet sammen med produktstrukturen for frigivelsen. |

## <a name="engineering-change-management-tab"></a>Fanen Teknisk ændringsstyring

I følgende tabel beskrives de felter, der er tilgængelige under fanen **Teknisk ændringsstyring** på siden **Parametre for styring af tekniske ændringer**. Disse indstillinger påvirker processen til styring af tekniske ændringer.

| Felt | Beskrivelse |
|---|---|
| Kategori | Den standardkategori, der vil blive brugt, når der oprettes en anmodning om en teknisk ændring. |
| Prioritet | Den standardprioritet, der vil blive brugt, når der oprettes en anmodning om en teknisk ændring. |
| Regel for alvorsgrad | Vælg, hvordan graden af en teknisk ændringsordre skal fastlægges. Vælg *Manuel*, hvis brugeren forventes at angive en værdi i feltet **Alvorsgrad**. Vælg *Beregn* for at få systemet til at beregne værdien af feltet **Alvorsgrad**, når du vælger **Beregn alvorsgrad** i handlingsruden i den tekniske ændringsordre. I dette tilfælde vil systemet bruge de alvorlighedsregler, der er defineret på siden **Regelsæt for alvorsgrad**. Vælg *Beregn automatisk*, hvis værdien i feltet **Alvorsgrad** automatisk skal beregnes og udfyldes i overensstemmelse med regelsæt for alvorsgrad. |
| Frigiv påvirkede produkter igen | Dette felt kan anvendes ved ny frigivelse af produkter via en teknisk ændringsordre. Du kan vælge, om alle produkter eller kun de berørte produkter skal foreslås, i dialogboksen **Frigivelser**. |
| Styklisteniveauer, der skal frigives | Dybden af det styklisteniveau, der skal frigives. Hvis styklisten har flere niveauer (dvs. hvis den er dybere) end den værdi, der er angivet her, vil kun de niveauer, der ligger højere gennem den angivne værdi, blive frigivet. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]