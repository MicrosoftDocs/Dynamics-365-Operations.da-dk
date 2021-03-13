---
title: Registrere salgskommissioner
description: I dette emne beskrives, hvordan salgsprovisioner beregnes og registreres.
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4334fcd996f32b00bb399d3df5c43eb6bf50ab28
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010691"
---
# <a name="register-sales-commissions"></a>Registrere salgskommissioner

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan salgsprovisioner beregnes og registreres. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data. Før du starter denne vejledning, skal du køre vejledningen "Konfigurer regler for salgsprovision" for at sikre, at du har den nødvendige provisionsberegningsopsætning.

Notér de kunde- og varenumre, du har valgt til provisionsprocessen, og brug dem, når du bliver bedt om at oprette en salgsordre i denne vejledning.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Fakturere en salgsordre, der kvalificerer en sælger til en provision
1. Gå til **Moduler > Salg og marketing > Salgsordrer > Alle salgsordrer** i navigationsruden.
2. Vælg **Ny**.
3. Vælg den ønskede post på rullemenuen i feltet **Debitorkonto**.
4. Vælg **OK**.
5. Vælg **Indstillinger** i handlingsruden.
6. Vælg **Skift visning**.
7. Vælg **Overskriftsvisning**.
8. Udvid sektionen **Konfiguration**.

    - Værdien i feltet **Salgsgruppe** repræsenterer en gruppe med en eller flere tilknyttede sælgere. Personerne i gruppen er dem, der modtager provision, når ordren faktureres i henhold til foruddefinerede satser og fordeling.   
    - Værdien kopieres fra kundekortet, men du kan ændre den, hvis du ønsker.  
    - Gruppen Salg kopieres også til salgsordrelinjen. Du kan ændre den, så den er anderledes end den i hovedet og/eller mellem linjerne.  
    - Værdien i feltet **Provisionsgruppe** repræsenterer en gruppe, du har oprettet for en eller flere kunder med det formål at spore provisioner.   
    - Værdien kopieres fra kundekortet, men du kan ændre den, hvis du ønsker.   

9. Vælg **Indstillinger** i handlingsruden.
10. Vælg **Skift visning**.
11. Vælg **Linjevisning**
12. Vælg den vare, du har konfigureret til provisioner, i rullemenuen i feltet **Varenummer**. 
13. Angiv et tal i feltet **Antal**. Bemærk linjens nettobeløb. Det repræsenterer salgsindtægter, som i dette eksempel danner grundlag for provisionsberegningen.  
14. Vælg **Gem**.
15. Vælg **Faktura** i handlingsruden.
16. Vælg **Faktura**.
17. Udvid sektionen **Parametre**.
18. Vælg **Alle**" i feltet **Antal**.
19. Vælg **Ja** i feltet **Bogføring**.
20. Vælg **OK**, og vælg derefter **OK** i den næste rude. Det kan tage omkring et minut at bogføre transaktionen. Vent på, at behandlingen fuldføres, og luk ikke siden.  

## <a name="review-the-registered-sales-commissions"></a>Gennemse de registrerede salgsprovisioner
1. I handlingsruden skal du vælge **Faktura** og derefter vælge **Faktura** igen.
2. I handlingsruden skal du vælge **Faktura** og derefter vælge **Provisionsposter**.

    - Fanen **Oversigt** viser linjer, der repræsenterer provisionsbeløb, der skal betales til sælgere, der er knyttet til fakturerede salgsordrer. Lad os se nærmere på det.  
    - Hvis du har brugt guiden "Konfigurer regler for salgsprovision" til at konfigurere gruppen **Provisionssalg**, er der to sælgere, som skal modtage en salgsprovision, og provisionen deles ligeligt mellem dem.  
    - I dette eksempel beregnes det samlede provisionsbeløb som en procentdel af salgsindtægterne (nettobeløbet på ordrelinjen).  
3. Luk siden.
4. Vælg **Bilag**. Du kan gennemgå bilagsposteringer for provisionsbeløb, der er bogført til de foruddefinerede provisionsudgifts- og -kreditorkonti.  

