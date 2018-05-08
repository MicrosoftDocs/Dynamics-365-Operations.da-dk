--- 
title: "Oprette en gentagen indkøbsordre"
description: "Denne fremgangsmåde viser, hvordan du opretter en ny indkøbsordre (IO) ved at kopiere linjer fra et tidligere indkøbsordredokument til en ny indkøbsordre eller en eksisterende indkøbsordre."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 257582d889ff55753f9bdbd234f0540503d20f27
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-repeat-purchase-order"></a>Oprette en gentagen indkøbsordre

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du opretter en ny indkøbsordre (IO) ved at kopiere linjer fra et tidligere indkøbsordredokument til en ny indkøbsordre eller en eksisterende indkøbsordre. Du kan oprette tilbagevendende ordrer på to måder. Du kan bruge de tilgængelige handlinger på dokumentniveau fra handlingsruden, eller du kan bruge linjedetaljehandlinger. Handlingerne på dokumentniveau er primært beregnet til at oprette en ny købsordre ved at tilføje linjer og headeroplysninger fra en anden ordre, mens linjedetaljehandlingen især er beregnet til at føje linjer til en eksisterende ordre. Eksemplet i denne vejledning kan bruges i demodatafirmaet USMF. Denne opgave foretages typisk af en indkøber.


## <a name="create-a-new-repeat-purchase-order"></a>Opret en ny gentagende indkøbsordre
1. Gå til Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer.
    * Først skal vi prøve at kopiere oplysninger til en ny ordre.  
2. Klik på Ny.
3. Skriv "US-101" i feltet Kreditorkonto.
4. Klik på OK.
5. Klik på Indkøbsordre i handlingsruden.
6. Klik på Fra alt.
    * Det er den side, hvorfra du kan kopiere fra eksisterende ordrer til din ordre. Der er forskellige indstillinger for, hvordan linjerne kopieres, og forskellige former for dokumenter, der kan kopieres fra. Vi ser først på muligheder for, hvordan linjer kopieres.   
7. Udvid sektionen Parametre.
    * Feltet Antalsfaktor er nyttig, hvis du skal bruge et antal, der er anderledes end det, der er i den ordre, du kopierer fra. Hvis du f.eks. vil bestille to gange det antal, der er på de linjer, du kopierer fra, skal du skrive '2' i dette felt, og derefter tilføjer systemet linjer, hvor det oprindelige antal er blevet fordoblet.  
    * Feltet Vend fortegn understøtter også ændring af det bestilte antal ved at ændre fortegn for antallet af ordrelinjer, der er tilføjet. Dette kan være nyttigt, hvis du vil tilbageføre en postering ved at oprette ordrelinjer, der negere transaktionen. Denne indstilling vælges automatisk, når siden åbnes fra handlingen Opret kreditnota.  
    * Med indstillingen Kopiér gebyrer kan du kopiere gebyrer til din nye ordre fra det dokument, du kopierer ordrelinjerne fra.  
    * Indstillingen Genberegn priser bruger de aktuelle priser og rabatter i stedet for at kopiere dem fra det dokument, du kopierer andre oplysninger fra.  
    * Indstillingen Kopiér præcis opretter en nøjagtig kopi af værdierne i alle felter i ordredokumentets header og linjer. Hvis denne indstilling ikke er markeret, bruges standardværdierne for mange af de felter, der vedrører leverandøren og produkterne, som når du opretter den nye ordre manuelt. For eksempel hvis den ordre, du kopierer fra, havde tilsidesat standardfakturakontoen for leverandøren, ville den samme fakturakonto være blevet kopieret til din ordre. Hvis du ikke har markeret feltet Kopiér præcis, ville standardfakturakontoen for leverandøren blive brugt på din ordre i stedet.  
    * Indstillingen Slet købslinjer sletter alle indkøbsordrelinjer, der allerede findes på den indkøbsordre, du kopierer til, før du anvender de nye linjer. Brug denne indstilling med omhu, da det sletter alle eksisterende linjer uden yderligere varsel.  
    * Hvis du bruger indstillingen Kopiér ordrehoved, behøver du ikke manuelt at oprette headeroplysningerne på din nye ordre. Bemærk, at denne indstilling resulterer i standardværdier, der bruges til felter, som er knyttet til kreditoren. Hvis det dokument, du kopierer fra, har ikke-standardværdier, du vil kopiere, skal du også bruge indstillingen Kopiér præcis.  
8. Skjul sektionen Parametre.
    * Der er forskellige dokumentkilder, som du kan kopiere fra, og de har hver især et separat afsnit på denne side. I afsnittet Indkøbsordrer kan du f.eks. kopiere fra eksisterende indkøbsordrer.  
9. Klik på linjen for den indkøbsordre, der har id'et 00015. 
10. Vælg linjen ved at markere dette afkrydsningsfelt.
11. Fjern markeringen i afkrydsningsfeltet for linjen, så den ikke kopieres til din ordre.
    * Nu er der valgt 4 linjer, som skal kopieres til indkøbsordren. Det er også muligt at vælge flere indkøbsordrelinjer fra andre indkøbsordrer og kopiere dem til din ordre. Du kan også tilføje linjer fra andre typer købsdokumenter. I de næste par trin gennemgås de forskellige muligheder.  
12. Skjul sektionen Indkøbsordrer.
13. Udvid afsnittet Bekræftelse.
    * Her kan du vælge indkøbsordrebekræftelser, der skal kopieres fra. Indkøbsordrebekræftelser identificeres med det tilknyttede indkøbskladde-id eller indkøbsordre-id.  
14. Skjul sektionen Bekræftelse.
15. Udvid afsnittet Produktkvitteringer.
    * Her kan du vælge produktkvitteringskladder, der skal kopieres fra. Produktkvitteringskladder identificeres ved produktkvitteringsbilaget eller indkøbsordre-id.   
16. Skjul afsnittet Produktkvitteringer.
17. Udvid afsnittet Fakturaer.
    * Her kan du vælge leverandørfakturaer, der skal kopieres fra. Fakturaerne identificeres ved fakturabilaget eller indkøbsordre-id.   
18. Skjul afsnittet Fakturaer.
19. Udvid sektionen Valgte linjer eller overskrifter, der skal kopieres.
    * Denne visning indeholder en oversigt over alle dokumenter og linjer, der er valgt til at blive kopieret til din ordre.   
20. Skjul sektionen Valgte linjer eller overskrifter, der skal kopieres.
21. Klik på OK.
    * De 4 linjer, du har valgt, er kopieret til din nye indkøbsordre.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopiér linjer til en eksisterende indkøbsordre
    * I stedet for at kopiere en hel ordre er det mere almindeligt at oprette en ny indkøbsordre og udfylde oplysninger på indkøbsordrehovedet og derefter kopiere de enkelte linjer fra eksisterende ordrer.  
1. Klik på Indkøbsordrelinje.
2. Klik på Fra alt.
    * Den side, der åbnes, er identisk med den, der vises før, men forskellige indstillinger er valgt, når den åbnes fra ordrelinjevisningen. Lad os se nærmere på parametrene.   
3. Udvid sektionen Parametre.
    * Indstillingen Slet indkøbslinjer er ikke valgt. Det betyder, at du kan kopiere nye linjer til ordren uden at fjerne eksisterende linjer.   
    * Indstillingen Kopier ordrehoved er heller ikke markeret, da vi kun føjer ekstra linjer til ordren.   
4. Skjul sektionen Parametre.
    * I dette eksempel kopierer vi linjer fra en eksisterende indkøbsordre.   
5. Klik på linjen for den indkøbsordre, der har id'et 00034. 
6. Vælg linjen ved at markere dette afkrydsningsfelt.
    * Bemærk, at den ene ordrelinje, der er på denne indkøbsordre, også er markeret.  
7. Klik på OK.
    * Den ekstra ordrelinje er blevet føjet til din indkøbsordre.  


