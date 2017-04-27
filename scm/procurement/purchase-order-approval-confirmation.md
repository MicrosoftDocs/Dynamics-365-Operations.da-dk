---
title: "Godkend og bekræft indkøbsordrer"
description: "I denne artikel beskrives de statusser, som en indkøbsordre (IO) gennemgår, når det er blevet oprettet, og effekten af at aktivere ændringsstyring på IO&quot;er."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: b16092454e9637e628c8481bc471d86cf3be7bf6
ms.lasthandoff: 03/31/2017


---

# <a name="approve-and-confirm-purchase-orders"></a>Godkend og bekræft indkøbsordrer

[!include[banner](../includes/banner.md)]


I denne artikel beskrives de statusser, som en indkøbsordre (IO) gennemgår, når det er blevet oprettet, og effekten af at aktivere ændringsstyring på IO'er.

Når en købsordre (IO) er blevet oprettet, skal den evt. gennemgå en godkendelsesproces. Når leverandøren har accepteret ordren, indstilles indkøbsordrens status til **Bekræftet**.

## <a name="approval-of-purchase-orders"></a>Godkendelse af indkøbsordrer
IO'er, der ikke bruger ændringsstyring, får status som **Godkendt**, så snart de er oprettet, mens IO'er, der bruger ændringsstyring, får status som **Udkast**, når de oprettes. En indkøbsordre, der er oprettet ved autorisation af et ordreforslag fra varedisponering, får altid status **Godkendt**, uanset indstillingerne for ændringsstyring. En IO opretter kun lagertransaktioner, når den har nået status **Godkendt**. Derfor vises dette lager ikke som tilgængeligt for reservation eller mærkning, før ordren accepteres.  

Du aktiverer ændringsstyring for IO'er ved at angive indstillingen **Aktivér ændringsstyring** på siden **Indkøbs- og forsyningsparametre**. Når ændringsstyring er aktiveret, skal IO'er gennemgå et godkendelsesforløb, når de er færdige. Microsoft Dynamics 365 for Operations har en editor til arbejdsgangsprocesser, hvor du kan definere en arbejdsgang til at repræsentere godkendelsesprocessen. Denne arbejdsgang kan omfatte regler for automatisk godkendelse, regler, som bestemmer, hvem der bliver tildelt til at godkende bestemte IO'er og regler for eskalering af en arbejdsgang, der har afventet godkendelse i lang tid. Du kan aktivere ændringsstyringsprocessen for alle kreditorer eller for bestemte kreditorer. Du kan også konfigurere processen, så den kan tilsidesættes for enkelte IO'er.  

Når ændringsstyring er aktiveret, går IO'er gennem seks godkendelsesstatusser, fra **Udkast** til **Færdiggjort**. Når en ordre er blevet godkendt, skal brugere, der vil ændre den, bruge handlingen **Anmod om ændring**.

| Godkendelsesstatus | Beskrivelse                                                                      | Anmod om ændring er aktiveret |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Udkast           | Indkøbsordren er en kladde og endnu ikke sendt til godkendelse i arbejdsgangen for indkøbsordren.     | Nej                        |
| Til gennemsyn       | Indkøbsordren er sendt til godkendelse i arbejdsgangen for indkøbsordren. Der afventes godkendelse       | Nej                        |
| Afvist        | Indkøbsordren blev afvist under godkendelsesprocessen.                                 | Nej                        |
| Godkendt        | Indkøbsordren blev godkendt.                                                             | Ja                       |
| Bekræftet       | Indkøbsordren blev bekræftet. En indkøbsordre kan ikke bekræftes, før den er godkendt.        | Ja                       |
| Færdiggjort       | Indkøbsordren blev færdiggjort. Den er nu økonomisk lukket og kan ikke længere ændres. | Nej                        |

## <a name="confirming-purchase-orders"></a>Bekræftelse af indkøbsordrer
IO'er, der har godkendelsesstatus **Godkendt**, kan gennemgå flere trin, før de bliver bekræftet. For eksempel skal du muligvis sende en forespørgsel om indkøb til leverandøren for at få oplysninger om priser, rabatter eller leveringsdatoer. Skal du det, kan du give indkøbsordren statussen **Til eksternt gennemsyn** ved hjælp af handlingen **Købsforespørgsel**.  

Kreditorer, der er konfigureret til at bruge kreditorportalen, kan gennemse ordrer på portalen, og godkende eller afvise dem. Under denne revisionsproces har indkøbsordren statussen **Til eksternt gennemsyn**. Kreditorportal kan konfigureres, så en bekræftelse fra kreditoren automatisk bekræfter ordren i Dynamics 365 for Operations. Du kan også manuelt bekræfte en indkøbsordre, når du har modtaget bekræftelse fra leverandøren. Hvis en leverandør afviser en IO, modtages afvisningen samt årsagen til afvisningen og forslag til ændringer. I dette tilfælde forbliver status for indkøbsordren **Til eksternt gennemsyn**.  

Der er også mulighed for at generere en proforma bekræftelse for en ordre, før den faktiske bekræftelse er blevet behandlet. Denne indstilling opretter kun en rapport, som du kan dele med leverandøren. Der oprettes ikke nogen kladdeoplysninger.  

Når leverandøren har accepteret ordren, er næste trin at registrere IO'en som bindende. Du kan udføre dette trin, ved hjælp af handlingen **Bekræftelse** eller handlingen **Bekræft**. Begge disse handlinger indstiller godkendelsesstatus for ordren til **Bekræftet**. Bekræftelse af ordre starter to yderligere processer:

-   Der oprettes en kladde for at gemme en nøjagtig kopi af det, der blev bekræftet i systemet. Nogle gange skal ordrer ændres, og flere kladder oprettes, når den opdaterede ordre er bekræftet. I disse kladder kan du få vist en oversigt over de forskellige versioner af ordren, som blev bekræftet.
-   Regnskabsfordelinger oprettes, og der udføres evt. ordrekontrol og budgetkontrol, hvis denne funktion er aktiveret. Hvis en af kontrollerne mislykkes, vises en fejlmeddelelse, der angiver, at der skal udføres ændringer af indkøbsordren, før den kan bekræftes igen.

En kreditor kan anmode om en form for sikkerhed for, at der ydes betaling for et køb. Der findes forskellige metoder til at give denne garanti i kreditorprocesser. For eksempel reserverer handlingen **Forudbetaling** midler til indkøbsordren, og denne forudbetaling registreres på indkøbsordren.

## <a name="changing-purchase-orders"></a>Ændring af indkøbsordrer
I nogle situationer kan det være nødvendigt at ændre en indkøbsordre, når den har fået godkendelsesstatussen **Godkendt** eller **Bekræftet**.  

Hvis indkøbsordren blev oprettet ved hjælp af en ændringsstyringsproces, kan du foretage ændringer ved at tilbagekalde ordren eller, hvis ordren er allerede blevet godkendt, ved hjælp af handlingen **Anmod om ændring**. I så fald ændres godkendelsesstatussen tilbage til **Udkast**, og du kan derefter ændre ordren. Når du er færdig med at foretage ændringer, kan det være nødvendigt at sende IO'en til fornyet godkendelse. Du kan konfigurere de ændringstyper, som kræver fornyet godkendelse, ved hjælp af en **Gengodkendelsesregel for indkøbsordrer**-politikregel på siden **Indkøbspolitikker**.  

Hvis en del af det bestilte antal for en indkøbsordrelinje er leveret, kan du ikke ændre det bestilte antal. Du kan dog ændre **Levér rest**-antallet på linjen. Du kan derefter bruge handlingen **Færdiggør** til at annullere linjer og forhindre yderligere behandling. 

Når en ordre er bekræftet, kan du ikke længere slette den. Du kan dog annullere den samlede mængde eller et eventuelt restantal på en ordre, forudsat at mængden eller antallet endnu ikke er modtaget eller faktureret.

<a name="see-also"></a>Se også
--------

[Oversigt over indkøbsordrer](purchase-order-overview.md)

[Oprettelse af indkøbsordre](purchase-order-creation.md)

[Produktkvittering sammenlignet med indkøbsordrer](product-receipt-against-purchase-orders.md)

[Oversigt over kreditorfakturaer](/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)




