---
title: Registrere og bogføre en fremdateret check for en kreditor
description: Du kan registrere detaljerne omkring en fremdateret check, før du udsteder checken til en leverandør ved brug af kladdebilaget.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 312f7c58352e3cb86c22f8c34b1b6c11456c0083
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779416"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a>Registrere og bogføre en fremdateret check for en kreditor

[!include [banner](../../includes/banner.md)]

Du kan registrere detaljerne omkring en fremdateret check, før du udsteder checken til en leverandør ved brug af kladdebilaget. Du kan også bogføre den fremdaterede check og generere økonomiske bevægelser. Inden du registrerer og bogfører en fremdateret check fra en kunde, skal du udføre følgende opgave: 

Konfigurer fremdaterede checks på siden **Kontant- og bankstyring**. 

Rollen for denne opgaveguide er Kasserer. Denne opgave bruger demofirmaet USMF.

1. Gå til **Kreditor > Betalinger > Betalingskladde**.
2. Klik på **Ny**.
3. I feltet **Navn** angives 'VendPay'.
4. Klik på **Linjer**.
5. I feltet **Konto** skal du angive de ønskede værdier.
6. Markér den valgte række på listen.
7. Angiv et tal i feltet **Debet**.
8. Klik på rullelisten i feltet **Betalingsmåde** for at åbne opslaget.
    * Vælg betalingsmåden for den fremdaterede check  
9. Find og vælg den ønskede post på listen.
10. Klik op linket i den valgte række på listen.
11. Klik på fanen **Fremdaterede checks**.
12. Skriv en værdi i feltet **Checknummer**.
    * Angiv eller ret nummeret på den fremdaterede check.  
13. Skriv en værdi i feltet **Navn på udstedende bank**.
    * Angiv bankoplysninger om den udstedende bank.  
14. Klik på fanen **Liste**.
15. Klik på **Bogfør**.
16. Luk siden.
17. Klik på fanen Fremdaterede checks.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
