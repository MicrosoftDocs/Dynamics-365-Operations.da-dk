---
title: Definere kontinuitetstidsplaner
description: Denne artikel gennemgår oprettelse af et kontinuitetsprogram (kaldes også tilbagevendende ordrer).
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: faa55c844c8ee8742fbb0868b55a520cec6686aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885078"
---
# <a name="define-continuity-schedules"></a>Definere kontinuitetstidsplaner

[!include [banner](../includes/banner.md)]

Denne artikel gennemgår oprettelse af et kontinuitetsprogram (kaldes også tilbagevendende ordrer). Denne artikel bruger USRT-firmaets demodata.


## <a name="create-continuity-program"></a>Oprette kontinuitetsprogram
1. Gå til Retail og Commerce > Kontiniutet > Kontinuitetsprogrammer.
2. Klik på Ny.
3. I feltet Tidsplans-id skal du angive id'et for kontinuitetstidsplanen.
4. I feltet Ordrestart skal du vælge 'Første hændelse'.
    * Hvis en kunde afgiver en ny ordre for kontinuitetsprogrammet, er der to muligheder for produktlevering: 1. Første hændelse: det første produkt i kontinuitetsprogrammet afsendes.  2 Den aktuelle hændelse: Det aktuelle produkt afsendes. F.eks.: Tre måneder inde i programmet modtager kunden det tredje i programmet.  
5. Vælg 'Ja' for at bede om ordrens startdato.
6. Klik på Tilføj linje.
7. Angiv varenummeret for første produkt ('0013') i feltet Varenummer.
8. Skriv 'CP'.
9. Angiv den dato, hvor det første produkt kan bestilles.
10. Klik på Tilføj linje.
11. I feltet Varenummer skal du skrive "0014".
12. Fjern værdien, så feltet er tomt, i feltet Datointervalkode.
    * Fjern datointervallet for denne procedure. Du skal angive datoen som trinvis fra startdatoen for første vare.  
13. Her kan du angive intervallet for afsendelse af produkterne. Skriv '30'.
    * For et månedligt program skal du angive 30 dage for intervallet.  
14. Klik på Tilføj linje.
15. I feltet Varenummer skal du skrive "0015".
16. Skriv 'Slut'.
17. Klik på Gem.

## <a name="assign-to-continuity-item"></a>Tildele til kontinuitetsvare
1. Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.
2. Vælg vare '0016'.
    * I denne procedure skal du vælge varenummer 0016. Normalt har du oprettet et frigivet produkt, hvor der anvendes en yderligere forretningslogik for kontinuitet, når det placeres i en salgsordre i callcenter.  
3. Klik op linket i den valgte række på listen.
4. Klik på Rediger.
5. Udvis eller skjul sektionen Sælg.
6. Her kan du angive kontinuitetsprogrammet, som denne vare repræsenterer. Skriv det tidsplans-id, du har oprettet tidligere.
    * Når varen sælges i et callcenter, anvendes yderligere forretningslogik fra det valgte kontinuitetsprogram.  
7. Klik på Gem.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]