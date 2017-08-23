--- 
title: "Bekræfte salgsordrer"
description: "Denne fremgangsmåde viser, hvordan du bekræfter salgsordrer."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
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
ms.openlocfilehash: b0853e6a326a90b022bedc3b898d6c1b218c5fa2
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="confirm-sales-orders"></a>Bekræfte salgsordrer

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du bekræfter salgsordrer. Du får vist, hvordan du bekræfter en enkelt ordre, og hvordan du bekræfter flere ordrer på én gang. Disse opgaver udføres normalt af en salgsordrebehandler. Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data. Kontrollér, at der er flere åbne salgsordrer for samme debitor, før du starter. Hvis du bruger USMF, kan du bruge debitor US-027.


## <a name="confirm-a-single-sales-order"></a>Bekræft en enkelt salgsordre
1. Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.
2. På listen skal du finde og vælge den ordre, du vil bekræfte.
3. Klik på linket på salgsordrenummeret for at åbne den valgte ordre.
4. Klik på Sælg i handlingsruden.
5. Klik på Bekræft salgsordre.
6. Udvid eller skjul sektionen Parametre.
    * Sørg for, at feltet Bogføring ja er aktivt.  
7. Sæt indstillingen Udskrivning af bekræftelse til Ja.
    * Feltet Kontrollér kreditmaks angiver den metode, der bruges til at beregne en kundes resterende kredit. Koden kopieres som standard fra siden konti Debitorparametre. Hvis du vil springe kontrollen af kreditmaksimum over, når du bekræfter en bestemt salgsordre, kan du indstille Kontrollér kreditmaks. til Ingen. Du skal dog være opmærksom på, at selv hvis dette felt er indstillet til Ingen, bliver Kontrollér kreditmaks. stadig udført, hvis indstillingen Tvungen kreditmaks er valgt i kundens masterdata.  
8. Klik på OK.
9. Klik på Ja.
10. Luk siden.
11. Klik på Indstillinger i handlingsruden.
12. Klik på Skift visning.
13. Klik på Overskriftsvisning.
    * Når en ordre er bekræftet, angives dokumentets status til Bekræftelse.  
14. Klik på Sælg i handlingsruden.
15. Klik på Salgsordrebekræftelse.
16. Luk siden.

## <a name="confirm-multiple-sales-orders-at-once"></a>Bekræft flere salgsordrer på samme tid
1. Gå til Salg og marketing > Salgsordrer > Ordrebekræftelse > Bekræft salgsordre.
2. Klik på Vælg.
3. På listen under fanen Interval skal du finde og vælge den post, der henviser til Debitorkontofeltet.
4. Klik på rullelisten i feltet Kriterier for at åbne opslaget.
5. På listen skal du finde og vælge den debitorkonto med flere ordrer, du vil massebekræfte.
    * Hvis du bruger USMF, kan du vælge kontoen US-027.  
6. Klik på OK.
    * Fanen Oversigt viser en liste over de ordrer, der opfylder søgekriterierne. Disse medtages i bekræftelsen.  
    * Feltet Samleopdatering angiver parameteren, som flere ordrer skal opsummeres i, et enkelt bekræftelsesdokument. Indstillingen kopieres som standard fra indstillingen for standardværdier for samleopdatering på siden Debitorparametre.  
7. Vælg "Ordre" i Samleopdatering for felt.
    * Minimumsparametrene, der er påkrævet til at oprette samleopdateringer, er Fakturakonto og Valuta. Det betyder, at samleopdateringer, der har forskellige fakturakonti og forskellige valutaer, ikke er tilladt. Yderligere parametre kan konfigureres på siden Samleopdateringsparametre, der er tilgængelig fra siden Debitorparametre.  
8. Klik på rullelisten i feltet Salgsordrer for at åbne opslaget.
9. Vælg det ordrenummer, der skal udgøre salgsordren, på listen.
10. Klik på Arranger.
11. Klik på OK.
12. Klik på OK.


