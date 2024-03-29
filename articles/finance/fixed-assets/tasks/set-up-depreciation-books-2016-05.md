---
title: 'Konfigurere afskrivningsmodeller '
description: Denne procedure gennemgår processen med at oprette en ny afskrivningsmodel og knytte den til en anlægsaktivgruppe.
author: moaamer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a4713d949fe119cde1b1187a7c485d291281a8f
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725646"
---
# <a name="set-up-depreciation-books"></a>Konfigurere afskrivningsmodeller  

[!include [banner](../../includes/banner.md)]

Denne procedure gennemgår processen med at oprette en ny afskrivningsmodel og knytte den til en anlægsaktivgruppe. 

## <a name="create-a-depreciation-book"></a>Opret en afskrivningsmodel
1. Gå til Anlægsaktiver > Opsætning > Afskrivningsmodeller.
2. Klik på Ny.
3. Skriv en værdi i feltet Afskrivningsmodel.
4. Skriv en værdi i feltet Beskrivelse.
5. Markér eller fjern markeringen af afkrydsningsfeltet Beregn afskrivning.
6. Klik på rullelisten i feltet Afskrivningsprofil for at åbne opslaget.
7. Find og vælg den ønskede afskrivningsprofil på listen.
8. Klik op linket i den valgte række på listen.
9. Klik på rullelisten i feltet Alternativ afskrivningsprofil for at åbne opslaget.
10. Vælg den ønskede afskrivningsprofil på listen.
11. Klik op linket i den valgte række på listen.
    * Afskrivningsprofilen Ekstraordinær bruges som yderligere afskrivningsmetode for et aktiv under usædvanlige omstændigheder. Du kan f.eks. bruge dette til at registrere afskrivning, der sker som følge af en naturkatastrofe.  
12. Markér eller fjern markeringen af afkrydsningsfeltet Opret reguleringer af afskrivning med basisreguleringer.
13. Klik på rullelisten i feltet Kalender for at åbne opslaget.
14. Klik op linket i den valgte række på listen.

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>Knyt afskrivningsmodellen til en anlægsaktivgruppe
1. Klik på Anlægsaktivgrupper.
2. Klik på rullelisten i feltet Anlægsaktivgruppe for at åbne opslaget.
3. Find og vælg den ønskede post på listen.
4. Klik op linket i den valgte række på listen.
5. Vælg en indstilling i feltet Afskrivningsprincip.
6. Angiv et tal i feltet Levetid.
    * Bemærk, at værdien i Afskrivningsperioder beregnes efter angivelse af levetid.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
