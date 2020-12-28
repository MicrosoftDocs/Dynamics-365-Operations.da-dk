---
title: Sende ordrer som direkte leveringer
description: Dette emne beskriver, hvordan du opretter en direkte levering for en salgsordre.
author: omulvad
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart, PurchEditLines, PurchTable, PurchTableReferences, MCRDropShipWorkbench, SalesShippingLine
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31cb26479ccb74dfb58fd5590cd60d7b7c64c292
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425043"
---
# <a name="ship-orders-as-direct-deliveries"></a>Sende ordrer som direkte leveringer

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du opretter en direkte levering for en salgsordre. Du bruger direkte levering, når du vil levere varer til kunden direkte fra leverandøren, i stedet for at sende dem til dit eget lager først. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data. For at fuldføre den anden underopgave "Oprette direkte leveringer fra panelet" skal du sikre dig, at der for den vare, du vælger på salgsordren, er angivet en standardleverandør i oversigtspanelet Køb i Frigivne produktmaster.

## <a name="set-an-individual-order-for-direct-delivery"></a>Angive en enkelt ordre til direkte levering
1. Gå til **Navigationsrude > Moduler > Debitor > Ordrer > Alle salgsordrer**.
2. Vælg **Ny**.
3. Indtast eller vælg en værdi i feltet **Kundekonto** og vælg **OK**.
4. Angiv eller vælg værdier i felterne **Varenummer** og **Sted**, og vælg dernæst **Gem**.
5. Derefter skal du vælge **Direkte levering** under fanen **Salgsordre** i Handlingsruden. Siden Opret levering indeholder alle åbne salgsordrelinjer som kopieret fra salgsordren. Du kan gennemse ordredetaljerne, og hvis det er nødvendigt, kan du ændre oplysninger som f.eks. købsmængde og prisvilkår, før du opretter en direkte levering.  
6. Vælg **Ja** i feltet **Medtag alle**.
    - Hvis du vil generere en direkte levering for kun et undersæt af salgsordrelinjerne, skal du vælge disse individuelt.  
    - Feltet **Kreditorkonto** er muligvis allerede udfyldt med et leverandørnummer. Hvis standardkreditoren er konfigureret til produktet (på den tilknyttede varedisponering), kopieres denne kreditor til linjen. Ellers skal du angive en kreditor manuelt. I dette eksempel skal vi vælge en ny kreditor i det næste trin, selvom der allerede er angivet en.   
7. Indtast eller vælg en værdi i feltet **Leverandørkonto** og vælg **OK**. Meddelelsen fortæller dig, at indkøbsordren er blevet oprettet.   
8. Vis eller skjul sektionen **Linjedetaljer**.
9. Vælg fanen **Levering**, og bekræft, at feltet **Direkte levering** er angivet til **Ja**.
10. Vælg **Generelt** i handlingsruden.
11. Vælg **Relaterede ordrer**.
12. Vælg linket i feltet **Indkøbsordre**.
13. Udvid sektionen **Linjedetaljer**, og vælg fanen **Adresse**.
    - Leveringsadressen for denne indkøbsordrelinje er kundens leveringsadresse og ikke virksomhedens adresse.  
    - Hvis du ændrer leveringsadressen på salgsordrelinjen eller på den oprindelige salgsordrelinje, vil leveringsadressen på den tilsvarende ordrelinjen automatisk blive opdateret.  
14. Vælg fanen **Levering**.
    - Ligesom salgsordrelinjen er linjetypen for den tilknyttede indkøbsordre også indstillet til Direkte levering.  
    - Leveringsdato for indkøbsordrelinjen og Bekræftet leveringsdato er indstillet til henholdsvis Ønsket modtagelsesdato og Bekræftet modtagelsesdato på den oprindelige salgsordrelinje.   
    - Hvis du opdaterer nogen af disse datoer på købslinjen eller salgslinjen, opdateres datoer på tilsvarende ordren automatisk.     
    - Den indkøbsordre, der er indstillet til direkte levering af varer til debitoren er knyttet til den oprindelige salgsordre ved hjælp af en særlig tilknytning. Denne tilknytning pålægger reglen, at opdatering af følgesedlen for salgsordren ikke kan foretages fra salgsordren selv og skal ske ved hjælp af indkøbsordren. Dog foretages kundefakturering fra salgsordren.  
15. Klik på **Køb** i handlingsruden.
16. Vælg **Bekræftelse**.
17. Vælg **OK**.
18. Vælg **Modtag** i handlingsruden.
19. Vælg **Produktkvittering**.
20. Skriv en værdi i feltet **Produktkvittering**.
21. Vælg **OK**.
22. Vælg **Generelt** i handlingsruden.
23. Vælg **Relaterede ordrer**, og fremhæv den ønskede post.
    - Når indkøbsordren er blevet opdateret som modtaget, eller med andre ord, når leverandøren har leveret varerne til kundens adresse, opdateres status for den oprindelige salgsordre automatisk til Leveret.  
    - Salgsordren kan nu faktureres.    
24. Vælg **OK**.
25. Luk siden.
26. Vælg **OK**. Luk siderne og gå tilbage til startsiden.

## <a name="create-direct-deliveries-from-the-workbench"></a>Oprette direkte leveringer fra panelet
1. Gå til **Navigation > Moduler > Debitor > Ordrer > Alle salgsordrer**.
2. Vælg **Ny**.
3. Indtast eller vælg en værdi i feltet **Kundekonto** og vælg **OK**.
4. Indtast eller vælg en værdi i felterne **Varenummer** og **sted**.
5. Udvid sektionen **Linjedetaljer**, og vælg dernæst fanen **Levering**. I stedet for at oprette en direkte levering som en del af salgsordrebehandling som i den forrige procedure, kan du vælge at udlevere denne opgave til en indkøbsmedarbejder. Hvis du vil medtage salgsordrelinjen i den direkte leveringsproces, skal du markere linjen for direkte levering.  
6. Vælg **Ja** i feltet **Direkte levering**.
    - Hvis varen er allerede indstillet til direkte levering som standard, indstilles feltet automatisk til Ja ved ordrelinjeposteringen. Du kan angive en vare til direkte levering på masteren for Frigivet produkt ved at indstille Direkte levering til Ja og vælge et standardlagersted for direkte levering.  
    - Fordi indkøbsordren endnu ikke er oprettet, er status for den direkte levering indstillet til "Skal leveres direkte".   
7. Vælg **Gem**.
8. Luk siderne, indtil du når tilbage til startsiden.
9. Angiv søgekriteriet `Direct delivery` i søgelinjen.
    - Siden Direkte levering fungerer som et panel, der giver indkøberen en oversigt over alle salgsordrelinjer, der skal leveres direkte, og den gør det muligt at oprette de respektive indkøbsordrer. Desuden kan han eller hun se de åbne direkte leveringsordrer og de bekræftede ordrer under fanen Bekræftelse og Levering.  
    - Når du har oprettet en ordre med direkte levering, flyttes den automatisk til fanen Bekræftelse. Du kan vælge at bekræfte ordren direkte fra denne side. Når købet er bekræftet, flyttes det automatisk til fanen Levering, hvorfra du kan registrere modtagelsen.  

