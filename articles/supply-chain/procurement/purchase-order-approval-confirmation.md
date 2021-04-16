---
title: Godkende og bekræfte indkøbsordrer
description: I dette emne beskrives de statusser, som en indkøbsordre gennemgår, når det er blevet oprettet, og effekten af at aktivere ændringsstyring på PO'er.
author: kamaybac
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchOrderInReview, PurchOrderApproved, PurchOrderInDraft, PurchOrderAssignedToMe, VendPurchOrderJournalListPage, PurchTableWorkflowDropDialog, VendPurchOrderJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.search.industry: ''
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95f1f6971e645a0aae8679c94a4bbd4cba946dc3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825416"
---
# <a name="approve-and-confirm-purchase-orders"></a>Godkende og bekræfte indkøbsordrer

[!include [banner](../includes/banner.md)]

I dette emne beskrives de statusser, som en indkøbsordre (IO) gennemgår, når det er blevet oprettet, og effekten af at aktivere ændringsstyring på IO'er.

Når en købsordre (IO) er blevet oprettet, skal den evt. gennemgå en godkendelsesproces. Når leverandøren har accepteret ordren, indstilles indkøbsordrens status til **Bekræftet**.

## <a name="approval-of-purchase-orders"></a>Godkendelse af indkøbsordrer
IO'er, der ikke bruger ændringsstyring, har status som **Godkendt**, så snart de er oprettet, mens IO'er, der bruger ændringsstyring, får status som **Kladde**, når de oprettes. En indkøbsordre, der er oprettet ved autorisation af et ordreforslag fra varedisponering, får altid status **Godkendt**, uanset indstillingerne for ændringsstyring. En IO opretter kun lagertransaktioner, når den har nået status **Godkendt**. Derfor vises dette lager ikke som tilgængeligt for reservation eller mærkning, før ordren accepteres.

Du aktiverer ændringsstyring for IO'er ved at angive indstillingen **Aktivér ændringsstyring** på siden **Indkøbs- og forsyningsparametre**. Når ændringsstyring er aktiveret, skal IO'er gennemgå et godkendelsesforløb, når de er færdige. Supply Chain Management er en editor til arbejdsgangsprocesser, hvor du kan definere en arbejdsgang til at repræsentere godkendelsesprocessen. Denne arbejdsgang kan omfatte regler for automatisk godkendelse, regler, som bestemmer, hvem der bliver tildelt til at godkende bestemte IO'er og regler for eskalering af en arbejdsgang, der har afventet godkendelse i lang tid. Du kan aktivere ændringsstyringsprocessen for alle kreditorer eller for bestemte kreditorer. Du kan også konfigurere processen, så den kan tilsidesættes for enkelte IO'er.

Når ændringsstyring er aktiveret, går IO'er gennem seks godkendelsesstatusser, fra **Udkast** til **Færdiggjort**. Når en ordre er blevet godkendt, skal brugere, der vil ændre den, bruge handlingen **Anmod om ændring**.

| Godkendelsesstatus | Beskrivelse                                                                      | Anmod om ændring er aktiveret |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Kladde           | Indkøbsordren er en kladde og endnu ikke sendt til godkendelse i arbejdsgangen for indkøbsordren.     | Nr.                        |
| Til gennemsyn       | Indkøbsordren er sendt til godkendelse i arbejdsgangen for indkøbsordren. Der afventes godkendelse       | Nej                        |
| Afvist        | Indkøbsordren blev afvist under godkendelsesprocessen.                                 | Nej                        |
| Godkendt        | Indkøbsordren blev godkendt.                                                             | Ja                       |
| Bekræftet       | Indkøbsordren blev bekræftet. En indkøbsordre kan ikke bekræftes, før den er godkendt.        | Ja                       |
| Færdiggjort       | Indkøbsordren blev færdiggjort. Den er nu økonomisk lukket og kan ikke længere ændres. | Nr.                        |

## <a name="confirming-purchase-orders"></a>Bekræftelse af indkøbsordrer
IO'er, der har godkendelsesstatus **Godkendt**, kan gennemgå flere trin, før de bliver bekræftet. For eksempel skal du muligvis sende en forespørgsel om indkøb til leverandøren for at få oplysninger om priser, rabatter eller leveringsdatoer. Skal du det, kan du give indkøbsordren statussen **Til eksternt gennemsyn** ved hjælp af handlingen **Købsforespørgsel**.

Kreditorer, der er konfigureret til at bruge kreditorportalen, kan gennemse ordrer på portalen, og godkende eller afvise dem. Under denne revisionsproces har indkøbsordren statussen **Til eksternt gennemsyn**. Kreditorportalen kan konfigureres, så en bekræftelse fra kreditoren automatisk bekræfter ordren i Supply Chain Management. Du kan også manuelt bekræfte en indkøbsordre, når du har modtaget bekræftelse fra leverandøren. Hvis en leverandør afviser en IO, modtages afvisningen samt årsagen til afvisningen og forslag til ændringer. I dette tilfælde forbliver status for indkøbsordren **Til eksternt gennemsyn**.

Der er også mulighed for at generere en proforma bekræftelse for en ordre, før den faktiske bekræftelse er blevet behandlet. Denne indstilling opretter kun en rapport, som du kan dele med leverandøren. Der oprettes ikke nogen kladdeoplysninger.

Når leverandøren har accepteret ordren, er næste trin at registrere IO'en som bindende. Du kan udføre dette trin, ved hjælp af handlingen **Bekræftelse** eller handlingen **Bekræft**. Begge disse handlinger indstiller godkendelsesstatus for ordren til **Bekræftet**. Bekræftelse af ordre starter to yderligere processer:

-   Der oprettes en kladde for at gemme en nøjagtig kopi af det, der blev bekræftet i systemet. Nogle gange skal ordrer ændres, og flere kladder oprettes, når den opdaterede ordre er bekræftet. I disse kladder kan du få vist en oversigt over de forskellige versioner af ordren, som blev bekræftet.
-   Regnskabsfordelinger oprettes, og der udføres evt. ordrekontrol og budgetkontrol, hvis denne funktion er aktiveret. Hvis en af kontrollerne mislykkes, vises en fejlmeddelelse, der angiver, at der skal udføres ændringer af indkøbsordren, før den kan bekræftes igen.

En kreditor kan anmode om en form for sikkerhed for, at der ydes betaling for et køb. Der findes forskellige metoder til at give denne garanti i kreditorprocesser. For eksempel reserverer handlingen **Forudbetaling** midler til indkøbsordren, og denne forudbetaling registreres på indkøbsordren.

## <a name="changing-purchase-orders"></a>Ændring af indkøbsordrer
I nogle situationer kan det være nødvendigt at ændre en indkøbsordre, når den har fået godkendelsesstatussen **Godkendt** eller **Bekræftet**.

Hvis indkøbsordren blev oprettet ved hjælp af en ændringsstyringsproces, kan du foretage ændringer ved at tilbagekalde ordren eller, hvis ordren er allerede blevet godkendt, ved hjælp af handlingen **Anmod om ændring**. I så fald ændres godkendelsesstatussen tilbage til **Udkast**, og du kan derefter ændre ordren. Når du er færdig med at foretage ændringer, kan det være nødvendigt at sende IO'en til fornyet godkendelse. Du kan konfigurere de ændringstyper, som kræver fornyet godkendelse, ved hjælp af en **Gengodkendelsesregel for indkøbsordrer**-politikregel på siden **Indkøbspolitikker**.

Hvis en del af det bestilte antal for en indkøbsordrelinje er leveret, kan du ikke ændre det bestilte antal, når indkøbsordren er i tilstanden **Kladde**. Du kan imidlertid ændre antallet for **Levér rest** på linjen for den indkøbsordre, der er i tilstanden **Kladde**.

Når en ordre er bekræftet, kan du ikke længere slette den. Du kan dog annullere den samlede mængde eller et eventuelt restantal på en ordre, forudsat at mængden eller antallet endnu ikke er modtaget eller faktureret. Du kan derefter bruge handlingen **Færdiggør** for at forhindre yderligere behandling. 


## <a name="canceling-purchase-orders"></a>Annullering af indkøbsordrer

En indkøbsordre kan annulleres ved hjælp af handlingen **Annuller** i hovedet.

Hvis antallet er delvist registreret, modtaget eller faktureret, kan du kun annullere det resterende antal, der ikke er registreret, modtaget eller faktureret. Ordreantallet reduceres derefter tilsvarende. Når antallet på linjen opdateres, opdateres linjestatus også. Det oprindelige antal på linjen er f.eks. 5, og der modtages et antal på 3. I dette tilfælde er det kun to, der kan annulleres. Linjen opdateres derefter til statussen **Modtaget**.

Hvis der føjes en leveringsrest til ordrelinjen, og den overstiger antallet på ordrelinjen, annullerer handlingen **Annuller** ikke det overskydende antal. I stedet forbliver linjen i **Åben ordre**-status, fordi den har et restantal. Det oprindelige antal på linjen er f.eks. 5, og leveringsresten er 7. Hvis ordren annulleres, annulleres fem, og et antal på 2 resterer, som du kan se i lagertransaktionerne.

Hvis du vil annullere hele antallet på en indkøbsordrelinje, skal du annullere antallet for leveringsrest på linjen. Linjen opdateres derefter til **Annulleret**-status.

Hvis en indkøbsordre er under ændringsstyring, skal enhver ændring, f.eks. annullering af ordren eller leveringsrest, sendes til arbejdsgangssystemet og godkendes, før processen kan fuldføres, og lagerposteringerne kan opdateres som annulleret.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Oversigt over indkøbsordrer](purchase-order-overview.md)

[Oprette indkøbsordrer](purchase-order-creation.md)

[Produktkvittering sammenlignet med indkøbsordrer](product-receipt-against-purchase-orders.md)

[Oversigt over kreditorfakturaer](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]