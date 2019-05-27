---
title: Oversigt over positive betalinger
description: Denne artikel indeholder oplysninger om positiv betaling, som bruges til at generere en elektronisk liste over checks, der kan indløses i en bank.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 51603df2847f4c21910a718186accca27e30ca67
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1512303"
---
# <a name="positive-pay-overview"></a>Oversigt over positive betalinger

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om positiv betaling, som bruges til at generere en elektronisk liste over checks, der kan indløses i en bank. 

Positiv betaling bruges til at generere en elektronisk liste over checks, der kan indløses i en bank. Positive betalingsfiler kan hjælpe banker med at forebygge checkbedrageri. Du konfigurerer en positiv betaling til at generere en elektronisk liste over checks, hver gang checks udskrives. Når checken derefter skal indløses hos banken, sammenligner banken checken med den liste over checks, du tidligere har fremsendt. Hvis checken svarer til en check på listen, indløser banken den. Hvis checken ikke stemmer overens med en check på listen, beholder banken den til gennemsyn.

Positiv betaling er også kendt som SafePay. 

Filer til positiv betaling kan indeholde følsomme oplysninger om beløbsmodtagere og checkbeløb. Sørg derfor for, at du bruger passende de sikringsforanstaltninger fra det tidspunkt, hvor filerne genereres, indtil de modtages af banken. Filer til positive betalinger overføres i henhold til overførselsinstruktionerne for webbrowseren. 

Filer til positiv betaling oprettes ved hjælp af dataenheder. Før du genererer en fil til positiv betaling, skal du angive transformationsformaterne for den XML-filer, der oversætter dataene til et format, som banken kan anvende. 

For hver bankkonto, du vil generere oplysninger om positiv betaling for, skal du tildele formatet for positiv betaling. Når du har genereret betalinger, kan du oprette en fil til positiv betaling for en enkelt juridisk enhed og en enkelt bankkonto. Du kan også samtidig generere filer til positiv betaling for flere juridiske enheder og bankkonti. 

Når de checks, der er angivet i en fil til positiv betaling, er betalt, modtager du et bekræftelsesnummer fra din bank. Derefter kan du bekræfte filen til positiv betaling i Microsoft Dynamics 365 for Finance and Operations. 

Hvis du vil ændre en fil til positiv betaling, kan du tilbagekalde den. For hver check i filen til positiv betaling, nulstilles derefter det felt, der angiver, om checken er inkluderet i en fil til positiv betaling.

Yderligere oplysninger finder du i afsnittet [Konfigurer og generer filer til positive betalinger](set-up-generate-positive-pay-files.md).



