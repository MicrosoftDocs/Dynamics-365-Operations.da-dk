---
title: EUR-00011 Generere EU-listesystemrapporten
description: Denne procedure fører dig gennem oprettelse af EU-salgslisterapporten.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ce3fa3eaae48499e58228d9d6dbf7ce7e97d2bd8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821827"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a>EUR-00011 Generere EU-listesystemrapporten

[!include [banner](../../includes/banner.md)]

Denne procedure fører dig gennem oprettelse af EU-salgslisterapporten. Dette omfatter overførsel af samhandelstransaktioner inden for Fællesskabet til EU-listesystemet og procestiden for rapporten. Denne procedure omfatter også oprettelse af en EU-samhandelstransaktion til demonstrationsformål. Du kan finde flere oplysninger om rapportering i EU-listesystemet, herunder de nødvendige forudsætninger, i Hjælp.

Denne procedure gælder for alle europæiske lande/områder. Proceduren er oprettet i demodatafirmaet DEMF, og dermed bruges Tyskland som et eksempel på indenlandsk land/område. Proceduren bruger også Portugal som et eksempel EU-land/område. Før du kan fuldføre denne procedure, skal du konfigurere rapportering i EU-listesystem.

Denne procedure er kun beregnet til bogholdere.


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a>Oprette en EU-salgstransaktion til demonstrationsformål
1. Gå til Debitor > Ordrer > Alle salgsordrer.
2. Klik på Ny.
3. Skriv "PRT-001" i feltet Kundekonto.
4. Klik på OK.
5. Skriv 'D0001' i feltet Varenummer.
6. Vis eller skjul sektionen Linjedetaljer.
7. Klik på fanen Opsætning.
8. Skriv Fuld i feltet Varemomsgruppe.
9. Klik på Tilføj linje.
10. Skriv 'D0003' i feltet Varenummer.
11. Skriv Rød i feltet Varemomsgruppe.
12. Klik på Gem.
13. Klik på Faktura i handlingsruden.
14. Klik på Faktura.
15. Udvid sektionen Parametre.
16. Vælg "Alle" i feltet Antal.
17. Udvid sektionen Konfiguration.
18. I feltet Fakturadato skal du indstille datoen til "01-11-2016".
19. Klik på OK.
20. Klik på OK.

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a>Overføre EU-samhandelstransaktioner til EU-listesystemet
1. Gå til Skat > Erklæringer > Udenrigshandel > EU-listesystemet.
2. Klik på Overførsel.
3. Vælg Ja i feltet Vare for at overføre vareposteringer.
4. Vælg Ja i feltet Ydelse for at overføre ydelsesposteringer.
    * Du kan også angive ekstra filtre på samhandelstransaktioner inden for Fællesskabet, du vil overføre.  
5. Klik på Overførsel.
    * Kontroller, at salgstransaktionen inden for Fællesskabet er blevet overført til EU-listesystemet.  

## <a name="generate-the-eu-sales-list-report"></a>Generere rapport for EU-listesystem
1. Klik på Rapportering.
2. I feltet Rapporteringsperiode skal du vælge Månedlig.
3. I feltet Fra dato skal du indstille datoen til "01-01-2016".
4. Vælg Ja i feltet Generer fil.
5. Vælg Ja i feltet Generer rapport.
6. Skriv "EUSalesList" i feltet Filnavn.
7. Skriv "EUSalesList" i feltet Rapportfilnavn.
8. Skriv "123" i feltet Registrerings-id for EU-listesystem.
    * Dette felt er kun tilgængeligt for Tyskland.  
    * Du kan også angive ekstra filtre på EU-samhandelstransaktioner, som du vil medtage i rapporten.  
9. Klik på OK.
    * Kontroller, at der vises pop op-vinduer, for at bekræfte, at filen og kontrolrapporten, bliver hentet.  

## <a name="mark-eu-sales-list-lines-as-reported"></a>Marker linjerne for EU-listesystemet som rapporteret
1. Klik på Marker.
2. Klik på Marker som rapporteret.
3. Vælg rækken for feltet Fakturadato på listen.
4. Skriv "01/01/2016..01/31/2016" i feltet Kriterier.
5. Vælg rækken for feltet Rapporteringsstatus på listen.
6. Vælg Medtages i feltet Kriterier.
    * Du kan også angive ekstra filtre på samhandelstransaktioner inden for Fællesskabet, som du vil markere som Rapporteret.  
7. Klik på OK.
8. Vælg Rapporteret i feltet Valg.

## <a name="mark-eu-sales-list-lines-as-closed"></a>Marker linjerne for EU-listesystemet som lukket
1. Klik på Marker.
2. Klik på Marker som lukket.
3. Markér rækken for feltet Fakturadato på listen.
4. Skriv "01/01/2016..01/31/2016" i feltet Kriterier.
5. Markér rækken for feltet Rapporteringsstatus på listen.
6. Vælg Rapporteret i feltet 'Kriterier'.
    * Du kan også angive ekstra filtre på samhandelstransaktioner inden for Fællesskabet, som du vil markere som Rapporteret.  
7. Klik på OK.
8. Vælg Lukket i feltet Valg.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]