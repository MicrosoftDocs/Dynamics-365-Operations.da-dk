--- 
title: Sende ordrer som direkte leveringer
description: Denne procedure viser, hvordan du opretter en direkte levering for en salgsordre.
author: omulvad
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d98e288a157183fbf4d7c032d86bb4a65166e297
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="ship-orders-as-direct-deliveries"></a>Sende ordrer som direkte leveringer

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en direkte levering for en salgsordre. Du bruger direkte levering, når du vil levere varer til kunden direkte fra leverandøren, i stedet for at sende dem til dit eget lager først. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data. For at fuldføre den anden underopgave "Oprette direkte leveringer fra panelet" skal du sikre dig, at der for den vare, du vælger på salgsordren, er angivet en standardleverandør i oversigtspanelet Køb i Frigivne produktmaster.


## <a name="set-an-individual-order-for-direct-delivery"></a>Angive en enkelt ordre til direkte levering
1. Gå til Alle salgsordrer.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Kundekonto.
    * Hvis du bruger USMF, kan du vælge kontoen US-001.  
4. Klik på OK.
5. Indtast eller vælg en værdi i feltet Varenummer.
    * Hvis du bruger USMF, kan du vælge element T0020.  
6. Klik på Gem.
7. Klik på Salgsordre i handlingsruden.
8. Klik på Direkte levering.
    * Siden Opret levering indeholder alle åbne salgsordrelinjer som kopieret fra salgsordren. Du kan gennemse ordredetaljerne, og hvis det er nødvendigt, kan du ændre oplysninger som f.eks. købsmængde og prisvilkår, før du opretter en direkte levering.  
9. Vælg Ja i feltet Medtag alle.
    * Hvis du vil generere en direkte levering for kun et undersæt af salgsordrelinjerne, skal du vælge disse individuelt.  
    * Feltet Kreditorkonto er muligvis allerede udfyldt med et leverandørnummer. Hvis standardkreditoren er konfigureret til produktet (på den tilknyttede varedisponering), kopieres denne kreditor til linjen. Ellers skal du angive en kreditor manuelt. I dette eksempel skal vi vælge en ny kreditor i det næste trin, selvom der allerede er angivet en.   
10. Indtast eller vælg en værdi i feltet Kreditorkonto.
    * Hvis du bruger USMF, kan du vælge kontoen 1001.  
11. Klik på OK.
    * Meddelelsen fortæller dig, at indkøbsordren er blevet oprettet.   
12. Vis eller skjul sektionen Linjedetaljer.
13. Klik på fanen Levering.
    * Feltet Direkte levering er nu indstillet til Ja.  
    * Status for direkte levering viser den indkøbsordre, der er oprettet.   
14. Klik på Generelt i handlingsruden.
15. Klik på Relaterede ordrer.
16. Klik for at følge linket i feltet Indkøbsordre.
17. Vis eller skjul sektionen Linjedetaljer.
18. Klik på fanen Adresse.
    * Bemærk, at leveringsadressen for denne indkøbsordrelinje er kundens leveringsadresse og ikke virksomhedens adresse.  
    * Hvis du ændrer leveringsadressen på salgsordrelinjen eller på den oprindelige salgsordrelinje, vil leveringsadressen på den tilsvarende ordrelinjen automatisk blive opdateret.  
19. Klik på fanen Levering.
    * Ligesom salgsordrelinjen er linjetypen for den tilknyttede indkøbsordre også indstillet til Direkte levering.  
    * Leveringsdato for indkøbsordrelinjen og Bekræftet leveringsdato er indstillet til henholdsvis Ønsket modtagelsesdato og Bekræftet modtagelsesdato på den oprindelige salgsordrelinje.   
    * Hvis du opdaterer nogen af disse datoer på købslinjen eller salgslinjen, opdateres datoer på tilsvarende ordren automatisk.     
    * Den indkøbsordre, der er indstillet til direkte levering af varer til debitoren er knyttet til den oprindelige salgsordre ved hjælp af en særlig tilknytning. Denne tilknytning pålægger reglen, at opdatering af følgesedlen for salgsordren ikke kan foretages fra salgsordren selv og skal ske ved hjælp af indkøbsordren. Dog foretages kundefakturering fra salgsordren.  
20. Klik på Køb i handlingsruden.
21. Klik på Bekræftelse.
22. Klik på OK.
23. Klik på Modtag i handlingsruden.
24. Klik på Produktkvittering.
25. Skriv en værdi i feltet Produktkvittering.
26. Klik på OK.
27. Klik på Generelt i handlingsruden.
28. Klik på Relaterede ordrer.
29. Markér den valgte række på listen.
    * Når indkøbsordren er blevet opdateret som modtaget, eller med andre ord, når leverandøren har leveret varerne til kundens adresse, opdateres status for den oprindelige salgsordre automatisk til Leveret.  
    * Salgsordren kan nu faktureres.    
30. Klik på OK.
31. Luk siden.
32. Klik på OK.

## <a name="create-direct-deliveries-from-the-workbench"></a>Oprette direkte leveringer fra panelet
1. Luk siden.
2. Luk siden.
3. Gå til Alle salgsordrer.
4. Klik på Ny.
5. Indtast eller vælg en værdi i feltet Kundekonto.
6. Klik på OK.
7. Indtast eller vælg en værdi i feltet Varenummer.
8. Vis eller skjul sektionen Linjedetaljer.
9. Klik på fanen Levering.
    * I stedet for at oprette en direkte levering som en del af salgsordrebehandling som i den forrige procedure, kan du vælge at udlevere denne opgave til en indkøbsmedarbejder. Hvis du vil medtage salgsordrelinjen i den direkte leveringsproces, skal du markere linjen for direkte levering.  
10. Vælg Ja i feltet Direkte levering.
    *   Hvis varen er allerede indstillet til direkte levering som standard, indstilles feltet automatisk til Ja ved ordrelinjeposteringen. Du kan angive en vare til direkte levering på masteren for Frigivet produkt ved at indstille Direkte levering til Ja og vælge et standardlagersted for direkte levering.  
    * Fordi indkøbsordren endnu ikke er oprettet, er Status for direkte levering indstillet til Til direkte levering.   
11. Luk siden.
12. Luk siden.
13. Gå til Direkte levering.
    * Siden Direkte levering fungerer som et panel, der giver indkøberen en oversigt over alle salgsordrelinjer, der skal leveres direkte, og den gør det muligt at oprette de respektive indkøbsordrer. Desuden kan han eller hun se de åbne direkte leveringsordrer og de bekræftede ordrer under fanen Bekræftelse og Levering.   
14. Klik på Opret direkte levering.
15. Klik på fanen Bekræftelse.
    * Når du har oprettet en direkte leveringsordre, flyttes den automatisk til fanen Bekræftelse. Du kan vælge at bekræfte ordren direkte fra denne side. Når købet er bekræftet, flyttes det automatisk til fanen Levering, hvorfra du kan registrere modtagelsen.  


