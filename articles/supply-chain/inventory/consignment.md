---
title: Konfigurere konsignation
description: Dette emne forklarer, hvordan du bruger indgående processer for konsignationslager.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchTablePart, PurchVendorPortalConfirmedOrders, DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c36426e854453cd3c5ce5aca8398183fde1d75a2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823499"
---
# <a name="set-up-consignment"></a>Konfigurere konsignation

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du bruger indgående processer for konsignationslager.

Konsignationslager er lager, der ejes af en leverandør, men lagret på dit sted. Når du er klar til at forbruge eller bruge af lageret, overtager du ejerskabet af lageret. Dette emne indeholder oplysninger om, hvordan du får fysisk leverandørejet lager uden at oprette finanstransaktioner, hvordan du starter en produktionsproces, hvor leverandørejet lager kan reserveres fysisk. Og hvordan du ændrer ejerskab af råvarer for at kunne behandle forbrug som en del af behandlingen af produktionsordrer. Der er også nogle oplysninger om, hvordan leverandørerne kan overvåge forbruget af deres lager ved hjælp af grænsefladen for leverandørsamarbejde. 

## <a name="overview-of-the-consignment-process"></a>Oversigt over konsignationsprocessen
I dette eksempelscenario har firmaet USMF en konsignationsaftale med leverandør US-104 for råvaren M9211CI.

1.  En genbestillingsordre på konsignation oprettes manuelt af en person i USMF, der er baseret på den forventede efterspørgsel. Ordren er oprettet for leverandør US-104, og der tilføjes en linje for vare MS9211CI.
2.  Leverandøren bliver informeret om forventet levering. Dette kan ske på en af tre måder:
    -   En ansat hos USMF sender ordreoplysninger til leverandøren.
    -   Leverandøren kan overvåge den forventede disponible lagerbeholdning ved hjælp af grænsefladen for leverandørsamarbejde.
    -   En ansat hos USMF filtrerer dataene på siden **Disponibel lagerbeholdning** for at få vist posterne for leverandør US-104, hvis modtagestatus er **Bestilt**, og sender derefter oplysningerne til leverandøren.
3.  Lageret leveres fra US-104 til USMF.
4.  Når materialet ankommer til USMF, opdateres genbestillingsordren for konsignation med en produktkvittering. Det er kun fysiske mængder af det lager, der ejes af leverandøren, som registreres. Der oprettes ingen finanstransaktioner, fordi lageret ejes stadig af leverandøren.
5.  Leverandøren overvåger opdateringer til den fysisk disponible lagerbeholdning ved hjælp af siden **Disponibelt konsignationslager**.
6.  Nu, hvor det fysiske lager er disponibelt, reserveres det lager, der ejes af leverandøren, i produktionsprocessen, og starter produktionsordren til færdige varer, der forbruger råvare M9211CI.
7.  Ejeren af reserverede råvarer, der skal forbruges i produktionen i dag, er ændret fra US-104 til USMF. Dette gøres ved hjælp af et lagerejerskabs ændringskladde. Denne proces opretter indkøbsordrer, hvor feltet **Oprindelse** er angivet til **Konsignation**.
8.  Leverandøren overvåger forbrug (ændring af ejerskabet) på siden **Produkter, der er modtaget fra konsignationslager** og udsteder en faktura, der er baseret på aftaler mellem de to selskaber.
9.  Produktionsprocessen forbruger råvarer via en plukliste til produktion. Fysisk reservation opdateres automatisk for at afspejle, at den disponible lagerbeholdning er ejet af USMF.
10. Fakturaen fra US-104 behandles mod de indkøbsordrer, der blev genereret automatisk , da ændringsjournalen for lagerets ejerskab blev behandlet. Der foretages betaling til kreditor US-104 for det lager, der blev forbrugt.

USMF udfører yderligere periodiske processer:

-   Fysisk flytning af leverandørejet lager mellem forskellige lagersteder behandles ved hjælp af en overførselskladde.
-   Fysisk disponibel lagerbeholdning opdateres ved hjælp af kladden **Vareoptælling**. Optælling kan også bruges af leverandøren til at opdatere den disponible lagerbeholdning, hvis de har tilladelse til at gøre dette.

Kreditoren, US-104, kan overvåge opdateringer ved hjælp af siden **Disponibelt konsignationslager**.

## <a name="consignment-replenishment-orders"></a>Genopfyldningsordrer til konsignation
En genopfyldningsordre for konsignation er et dokument, der bruges til at anmode om og holde styr på lagerantal af produkter, som en leverandør har til hensigt at levere inden for et bestemt datointerval ved at oprette bestilte lagertransaktioner. Dette vil normalt baseres på budgettet og faktisk efterspørgsel på specifikke produkter. Det lager, der skal modtages mod genopfyldningsordre til konsignation, forbliver i ejerskabet af leverandøren. Det er kun besiddelse af produkter i forbindelse med fysisk opdatering, der registreres, og derfor bliver ingen opdateringer af finanstransaktion udført. 

Dimensionen **Ejer** bruges til at adskille oplysninger om, hvilket lager der ejes af leverandøren, og som ejes af den modtagende juridiske enhed. Genopfyldningens ordrelinjer til konsignation har en **Åben ordre**-status, så længe det fulde antal på linjerne ikke er modtaget eller annulleret. Når det fulde antal er modtaget eller annulleret, ændres status til **Fuldført**. Den fysisk disponible lagerbeholdning, der er tilknyttet en genopfyldningsordre til konsignation, kan registreres ved hjælp af en registreringsproces samt en opdateringsproces for produktkvittering. Registrering kan foretages som en del af varemodtagelsesprocessen eller ved manuelt at opdatere ordrelinjerne. Når opdateringsprocessen for produktkvittering bruges, oprettes der en post i produktkvitteringskladden, som kan bruges til at bekræfte modtagelsen af varerne for leverandørerne.

[![consignment-replenishment-order](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Ændringskladde for beholdningsejerskab
Processen, der ændrer ejeren af lageret fra leverandøren til den modtagende juridiske enhed, udføres via en ændringskladde for lagerejerskab. Der oprettes ingen lagertransaktioner for kladden. Det er kun lagertransaktioner, der vedrører en bogført kladde, der oprettes. Når kladden er bogført:

-   Det lager, der ejes af leverandøren, udstedes ved hjælp af en **Ændring af ejerskab**-reference med en **Solgt**-status.
-   Den disponible lagerbeholdning modtages af den juridiske enhed, der forbruger den, ved hjælp af en produktkvitteringsopdatering af lagertransaktionen på indkøbsordren. Dette angiver status for ordren til **Modtaget**. Indkøbsordrer, der bruges til konsignation, har feltet **Oprindelse** indstillet til **Konsignation**.

Det er ikke muligt at opdatere antal på indkøbsordrelinjer til konsignation, når ordren er blevet oprettet.

[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Leverandørsamarbejde i konsignationsprocesser
Leverandørsamarbejde-grænsefladen har tre sider, der er relateret til den indgående konsignationsproces:

-   **Indkøbsordrer**, **der forbruger konsignationslager** - Viser detaljerede indkøbsordreoplysningerne, der vedrører ejerskabsændringen fra konsignationsprocessen.
-   **Produkter, der er modtaget fra konsignationslager** - Viser oplysninger om varer og mængder, der får produktkvitteringer opdateret under ejerskabets ændringsproces.
-   **Disponibelt konsignationslager** – Viser oplysninger om de konsignationsvarer, som de forventes at levere, og varerne, der allerede er fysisk disponible på kundens adresse.

## <a name="inventory-owners"></a>Lagerejere
For at registrere fysisk indgående konsignationslager skal du definere en leverandørejer. Dette gøres på siden **Lagerejer**. Når du vælger en **kreditorkonto**, oprettes standardværdier for felterne **Navn** og **Ejer**. Værdien i feltet **Ejer** vil være synlig for leverandøren, så kan du ændre den, hvis dine kontonavne for kreditorer ikke er let for eksterne personer at genkende. Det er muligt at redigere feltet **Ejer**, men kun indtil tidspunktet, når du gemmer posten **Lagerejer**. Feltet **Navn** udfyldes med navnet på den part, der er tilknyttet kreditorkontoen, og dette kan ikke ændres.

[![lagerejere](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Sporingsdimensionsgruppe
Varer, der skal bruges i konsignationsprocesser, skal være tilknyttet en **sporingsdimensionsgruppe**, hvor dimensionen **Ejer** er sat til **Aktiv**. Ejerdimensionen har altid **Fysisk lager** og **Økonomisk lager** som valgte indstillinger. **Disponer pr. dimension** er aldrig markeret.

[![sporingsdimensionsgruppe](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Ændringskladde for beholdningsejerskab
Kladden **Ændring af beholdningsejerskab** bruges til at registrere overdragelse af ejendomsretten til konsignationslager fra leverandøren til den juridiske enhed, der bruger den. Det skal være identificeret med et lagerkladdenavn som enhver lagerkladde. Disse navne oprettes på siden **Lagerkladdenavne**, og **Kladdetype** skal være indstillet til **Ændring af ejerskab**.

[![ændringskladde for beholdningsejerskab](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Leverandørsamarbejde i konsignationsprocesser
Hvis dine kreditorer bruger leverandørsamarbejde som interface, kan de bruge dette til at overvåge forbruget af lageret på dit sted. Yderligere oplysninger om opsætning af leverandører til at anvende leverandørsamarbejde findes i [Sikkerhed for bruger af leverandørportal](../procurement/configure-security-vendor-portal-users.md).







[!INCLUDE[footer-include](../../includes/footer-banner.md)]