---
title: Konfigurere politikker for lagerstedsarbejde (program, maj 2016)
description: Lagerstedsprocesser omfatter ikke altid lagerstedsarbejde.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 23ad33a2f070a33e4e658870561406c4604f4dce
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847057"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a>Konfigurere politikker for lagerstedsarbejde (program, maj 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Lagerstedsprocesser omfatter ikke altid lagerstedsarbejde. Ved at definere en arbejdspolitik kan du forhindre oprettelse af arbejde med pluk af råmaterialer og placering af færdigvarer på lager for en række produkter på bestemte lokationer. USMF-demodatafirmaet blev brugt til at oprette denne registrering. Denne opgavevejledning kræver Dynamics AX-program 7.0.1 eller nyere.

1. Gå til Lagerstyring > Konfiguration > Arbejde > Arbejdspolitikker.
2. Klik på Ny.
3. Skriv 'Ikke læg-på-lager-arbejde' i navnefeltet Arbejdspolitik.
4. Klik på Gem.
5. Klik på Tilføj.
6. Markér den valgte række på listen.
7. Vælg 'Færdige varer lægges på lager' i feltet Arbejdsordretype.
8. Klik på Tilføj.
9. Markér den valgte række på listen.
10. Vælg 'Samprodukter eller biprodukter, der er lagt på lager' i feltet Arbejdsordretype.
11. Udvid sektionen Lagerlokationer.
12. Klik på Tilføj.
13. Markér den valgte række på listen.
14. Indtast '51' på lagerstedslisten.
15. Indtast eller vælg '001' i feltet Lokation.
16. Udvid afsnittet Produkter.
17. Vælg 'Valgt' i feltet Produktvalg.
18. Klik på Tilføj.
19. Markér den valgte række på listen.
20. Indtast eller vælg 'L0101' i feltet Varenummer.
21. Klik på Gem.

