---
title: Færdigmelde til en ikke-id-styret lokation (program, maj 2016)
description: Denne opgavevejledning viser et eksempel på færdigmedling til en lokation, der ikke er id-kontrolleret.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f891b2e3b20993a08138dfac1aed4f4bab33c6b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576706"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>Færdigmelde til en ikke-id-styret lokation (program, maj 2016)

[!include [banner](../../includes/banner.md)]

Denne opgavevejledning viser et eksempel på færdigmedling til en lokation, der ikke er id-kontrolleret. En relevant arbejdspolitik er en forudsætning for denne opgave. En tidligere opgavevejledning viste konfigurationen af arbejdspolitikken. Denne opgavevejledning kræver Dynamics AX-program 7.0.1 eller nyere.




## <a name="set-up-an-output-location"></a>Konfigurere en outputlokation
1. Gå til Virksomhedsadministration > Ressourcer > Ressourcegrupper.
2. Vælg ressourcegruppen '5102' på listen.
3. Klik på Rediger.
4. Indtast '51' i feltet Lagersted for udlagring.
5. Indtast '001' i feltet Udlagringslokation.
    * Lokationen 001 er ikke en id-kontrolleret lokation. Du kan kun konfigurere en outputplacering uden id-kontrol, hvis der findes en gyldig arbejdspolitik for lokationen.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>Oprette en produktionsordre og rapportere den som færdig
1. Luk siden.
2. Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.
3. Klik på Ny produktionsordre.
4. Indtast 'L0101' i feltet Varenummer.
5. Klik på Opret.
6. Klik på Produktionsordre i handlingsruden.
7. Klik på Forkalkulation.
8. Klik på OK.
9. Klik på Start.
10. Klik på fanen Generelt.
11. Vælg "Aldrig" i feltet Automatisk styklisteforbrug.
12. Klik på OK.
13. Klik på Færdigmeld.
14. Klik på fanen Generelt.
15. Vælg Ja i feltet Accepter fejl.
16. Klik på OK.
17. Klik på Lagersted i handlingsruden.
18. Klik på Arbejdsdetaljer.
    * Når produktionsordren er færdigmeldt, oprettes der intet arbejde for læg-på-lager. Dette skyldes, at der er defineret en arbejdspolitik, som forhindrer, at der genereres arbejde, når produktet L0101 rapporteres som færdigt på lokation 001.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]