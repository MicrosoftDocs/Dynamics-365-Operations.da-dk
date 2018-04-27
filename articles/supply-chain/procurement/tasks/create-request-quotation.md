--- 
title: Oprette en tilbudsanmodning
description: Denne procedure viser dig, hvordan du skal oprette en tilbudsanmodning.
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 331f516f3483acd79be4ef7b95b53adcfbef1ae2
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-request-for-quotation"></a>Oprette en tilbudsanmodning

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser dig, hvordan du skal oprette en tilbudsanmodning. Dette vil normalt ske via en indkøbsagent. Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data. Du skal have oprettet anmodningstyper, før du begynder. Når du har fuldført denne opgave, og du har oprettet og sendt en tilbudsanmodning, kan du derefter angive svarene pr. kreditor, sammenligne dem og tildele kontrakter.


## <a name="prepare-a-new-rfq"></a>Forberede en ny tilbudsanmodning
1. Gå til Indkøb og forsyning > Tilbudsanmodninger > Alle tilbudsanmodninger.
2. Klik på Ny.
    * Følgende indkøbstyper er tilgængelige: Indkøbsordre (dette er standard): et dokument, der bekræfter tilbuddet om at købe produkter eller accepten af et tilbud om at sælge produkter mod betaling. Indkøbsrekvisition: denne type vælges automatisk, hvis du opretter en tilbudsanmodning direkte fra en indkøbsrekvisition. Hvis du vælger denne indstilling manuelt, vises der en fejlmeddelelse. Købsaftale: en aftale om at købe et bestemt antal eller en bestemt værdi af et produkt over tid. Hvis du vælger denne indstilling, skal du vælge det datointerval, der gælder for købsaftalen.  
3. Skriv en værdi i feltet Dokumenttitel.
4. Indtast eller vælg en værdi i feltet Anmodningstype.
    * Hvis en scoremetode er knyttet til anmodningstypen, bruges den som standardscoremetode til den tilbudsanmodning, du opretter. Det er muligt at ændre scoremetoden på et senere tidspunkt.  
    * Angiv en dato i feltet Leveringsdato.  
    * Vælg den dato, hvor varerne ønskes modtaget.  
    * Angiv dato og klokkeslæt i feltet Udløbsdato og -klokkeslæt.  
    * Angiv datoen og klokkeslættet, hvor kreditorerne skal svare på tilbudsanmodningen.  
5. Indtast eller vælg en værdi i feltet Lagersted.
    * Leveringsadressen er som standard lagerstedets adresse.  
6. Klik på OK.

## <a name="add-lines"></a>Tilføjelse af linjer
    * Når du har angivet de grundlæggende oplysninger om din tilbudsanmodning, kan du angive de varer eller tjenesteydelser, som du vil have leverandørerne til at byde på. Vare er standardlinjetypen.   
1. Indtast eller vælg en værdi i feltet Varenummer.
    * Hvis du bruger USMF, kan du vælge T0020.  
2. Angiv et tal i feltet Antal.
3. Klik på Tilføj linje.
4. Vælg Kategori i feltet Linjetype.
    * Du kan bruge linjetypen Kategori til at oprette tilbudsanmodninger for ikke-lagerførte varer eller tjenesteydelser. Derefter skal du vælge typen varer eller tjenesteydelser fra et hierarki af indkøbskategorier.  
5. Indtast eller vælg en værdi i feltet Indkøbskategori.
6. Skriv en værdi i feltet Produktnavn.
7. Angiv et tal i feltet Antal.
8. Indtast eller vælg en værdi i feltet Enhed.

## <a name="add-vendors"></a>Tilføj kreditorer
1. Klik på Overskrift for at skifte fra visningen Linjer til Overskrift. 
2. Vis sektionen Kreditor.
3. Klik på Tilføj kreditorer automatisk.
    * Du kan tilføje leverandører automatisk til tilbudsanmodningen, baseret på indkøbskategorien for de ønskede varer. Du kan tilføje kreditorer manuelt, hvis der ikke er nogen kreditorer, der er godkendt til de kategorier, der er inkluderet i linjerne.  
4. Klik på Tilføj.
5. Indtast eller vælg en værdi i feltet Kreditorkonto.
6. Klik på Tilføj.
7. Indtast eller vælg en værdi i feltet Kreditorkonto.
    * Når du har valgt en kreditor, er status Oprettet. Det betyder, at leverandøroplysningerne er gemt i tilbudsanmodningen, men du har ikke sendt tilbudsanmodningen til leverandøren. Du kan føje en leverandør til en tilbudsanmodning uanset leverandørens status.  

## <a name="send-the-rfq-to-vendors"></a>Send tilbudsanmodningen til kreditorer
1. Klik på Send.
    * Markér de kreditorer på listen, som skal have tilbudsanmodningen, på siden Sender tilbudsanmodning.  
2. Klik på Udskriv.
    * I denne dialogboks kan du udskrive tilbudsanmodningen. Hvis du vælger at udskrive et svarark, er indholdet af dette defineret i parametrene for Indkøb og forsyning. Hvis du vil vælge, hvordan du vil udskrive svarark, når du har åbnet dialogboksen Udskriv, skal du klikke på Avancerede udskriftsindstillinger. Der udskrives én tilbudsanmodning for hver kreditor, der indeholder de linjer, der har statussen Oprettet eller Sendt. Annullerede linjer og linjer med registrerede svar udskrives ikke.   
3. Klik på Annuller.
4. Klik på OK.
5. Luk siden.
6. Luk siden.

## <a name="view-the-rfq-journal"></a>Få vist tilbudsanmodningskladden
1. Gå til Indkøb og forsyning > Tilbudsanmodninger > Opfølgning på tilbudsanmodninger > Journaler til tilbudsanmodning.
2. Klik på Vis/udskriv.
3. Klik på Oprindelig visning.
4. Luk siden.
5. Luk siden.


