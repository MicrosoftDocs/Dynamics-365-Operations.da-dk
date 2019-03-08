---
title: Oprette en købsaftale
description: Denne procedure føres du gennem oprettelsen af en købsaftale.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b317f0a0fc8f198bad9501f325557ac2a4796989
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "338607"
---
# <a name="create-a-purchase-agreement"></a>Oprette en købsaftale

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure føres du gennem oprettelsen af en købsaftale. Dette vil normalt ske ved en indkøbschef. Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data. Du skal have oprettet købsaftaleklassifikationer, før du starter. Når du har oprettet en aftale, du kan bruge den, når du opretter en Indkøbsordre, og denne handling kopierer køb aftale betingelserne til hovedet og linjer i ordren, der berøres af aftalen.


## <a name="create-a-new-purchase-agreement"></a>Opret en ny købsaftale
1. Gå til Indkøb og forsyning > Købsaftaler > Købsaftaler.
2. Klik på Ny.
3. Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Klik på rullelisten i feltet Købsaftaleklassifikation for at åbne opslaget.
7. Find og vælg den ønskede post på listen.
8. Klik op linket i den valgte række på listen.
9. Udvid sektionen Generelt.
10. Indtast en dato i feltet Udløbsdato.
    * Denne udløbsdato er standard for alle tilsagnslinjer og bestemmer, hvor længe hvert specifikt tilsagn er gyldigt.  
11. Indtast et navn for købsaftalen i feltet Dokumenttitel.
    * Lad feltet Standardtilsagn være angivet til Bundet produktantal (eller ændr det, hvis det er ikke er angivet til dette).  
    * Værdien for standardtilsagnet angiver dine indstillinger på aftalelinjerne. Hvis du har brug for en ny tilsagnstype, når du opretter aftalelinjer, skal du ændre standardtilsagnet i overskriften.  Der er 4 typer tilsagn: Bundet produktantal – for en bestemt mængde af et produkt, Værditilsagn om produkt – for et bestemt valutabeløb af et produkt, Værditilsagn om produktkategori – for et bestemt valutabeløb i en indkøbskategori, hvor beløbet kan være for en katalogvare eller en vare uden for kataloget, Værditilsagn – for et bestemt valutabeløb, som kan opfyldes ved et produkt eller en indkøbskategori.  
12. Klik på OK.

## <a name="add-a-commitment"></a>Tilføj et tilsagn
1. Klik på Tilføj linje.
2. Markér den valgte række på listen.
3. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
4. Vælg det produkt, du vil føje et tilsagn til.
5. Klik op linket i den valgte række på listen.
6. Angiv et tal i feltet Antal.
    * Dette er den samlede mængde, som du har aftalt at købe fra din kreditor.  
7. Angiv et tal i feltet Enhedspris.
8. Vis eller skjul sektionen Linjedetaljer.
9. Sæt indstillingen Maks. gennemtvinges til Ja.
    * Maksimale gennemtvinges indstilling begrænser brugen af forpligtelsen. Du kan kun købe op til det antal, der er angivet i feltet Antal for linjen.  
10. Skjul sektionen Linjedetaljer.

## <a name="add-header-conditions"></a>Tilføj hovedbetingelser
1. Klik på Indstillinger i handlingsruden.
2. Klik på Skift visning.
3. Klik på Overskriftsvisning.
4. Udvid afsnittet Betingelser.
5. Klik på rullelisten i feltet Betalingsmåde for at åbne opslaget.
    * Betalingsbetingelserne fra kreditorkontoen vises her som standard.       
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Klik på rullelisten i feltet Leveringsmåde for at åbne opslaget.
9. Klik op linket i den valgte række på listen.
10. Klik på rullelisten i feltet Leveringsbetingelse for at åbne opslaget.
11. Klik op linket i den valgte række på listen.

## <a name="confirm-and-activate-the-agreement"></a>Bekræft og aktivér aftalen
1. Klik på Købsaftale i handlingsruden.
2. Klik på Bekræftelse.
    * Angiv indstillingen Markér aftale som gældende til Ja.  
3. Klik på OK.
4. Klik på Købsaftale i handlingsruden.
5. Klik på Bekræftelser af købsaftale.
    * Med indstillingen Vis/udskriv kan du oprette et dokument for købsaftalen, som du kan udskrive eller sende til kreditoren. Hvis du opdaterer aftalen senere og bekræfter den igen, vises begge versioner her.  
6. Luk siden.

