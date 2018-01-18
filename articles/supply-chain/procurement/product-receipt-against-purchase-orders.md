---
title: "Produktkvittering sammenlignet med indkøbsordrer"
description: I denne artikel beskrives de forskellige indstillinger for registrering af produkter som modtaget.
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, Retail
ms.custom: 93113
ms.assetid: d4ec3e86-fce2-4546-911b-e0acf64c8887
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: faccf695642d236dbf74a324ccecaf91f62638be
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="product-receipt-against-purchase-orders"></a>Produktkvittering sammenlignet med indkøbsordrer

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


I denne artikel beskrives de forskellige indstillinger for registrering af produkter som modtaget.

Produktkvittering er registreringen af, at der er modtaget bestilte produkter, så indkøbsordrelinjerne (IO) derefter kan behandles med henblik på fakturering. I nogle tilfælde gennemgår produkter forudregistrering, hvor yderligere oplysninger fra leverandøren registreres, før produkterne modtages. Når produkterne ankommer, skal de først er markeret som **Registreret**. Produkterne skal derefter muligvis igennem flere processer, som kvalitetsstyring, før de endelig markeres som **Modtaget**.

## <a name="preregistration-asn"></a>Forudregistrering (ASN)
Leverandører kan dele oplysninger om produkter, der skal leveres. Du kan i dette tilfælde forudregistrere produkter for at registrere disse oplysninger, før produkterne modtages. Ved at forudregistrere produkter kan du reducere mængden af arbejde, der kræves under vareregistrering og modtagelse. Leverandører kan levere produktoplysninger elektronisk via ASN (Advance Shipment Notice), som derefter registreres automatisk i systemet. Oplysningerne i ASN omfatter antallet af produkter, der skal leveres, og den dato, hvor de skal afsendes. ASN kan også indeholde oplysninger som batch- eller serienumre. Registrering af ASN sker **Transportstyring**-modulet.

## <a name="registration"></a>Registrering
Produktregistrering sker ofte ved modtagelsesområdet på et lagersted. Den udføres ved hjælp af en håndholdt enhed eller ved hjælp af modtagelseskladder. Du kan også registrere produktkvittering manuelt ved hjælp af handlingen **Registrering** på siden **Indkøbsordre**. I begge tilfælde markeres produkterne som **Registreret**. Bemærk, at produkterne endnu ikke er markeret som **Modtaget**.  

Produkter, der modtages på et lagersted, kan passere gennem kvalitetskontrol, før de lægges på lager. Enten kvalitetsordrer eller karantæneordrer kan bruges til at udføre kvalitetskontrol. Hvis der bruges kvalitetsordrer, kan du konfigurere processen for midlertidigt at blokere produkter via en reservation, mens de undersøges. Hvis der bruges karantæneordrer, flyttes produkter til et andet lagersted til inspektion. Dette lagersted er kendt som karantænelagerstedet. I begge kvalitetsinspektionsprocesser kan nogle af varerne kasseres, enten fordi de ikke lever op til kvalitetsforventningerne, eller fordi kvalitetsinspektionen indebærer destruktive test af en stikprøve af produktet.

## <a name="product-receipt"></a>Produktkvittering
Oftest bruges handlingen **Produktkvittering** på siden **Indkøbsordrer** til at markere produkter som **Modtaget** på indkøbsordren. Siden **Konterer produktkvittering** har forskellige indstillinger for det antal, der er bogført som modtaget. For eksempel kan du indstille feltet **Antal** til **Bestilt antal** eller **Antal til modtagelse nu**. Alternativt, hvis der er brugt en lagersteds-modtagelsesproces, skal du ofte indstille feltet til **Registreret antal**. Du kan ændre antallet på hver ordrelinje, der skal markeres som **Modtaget**, for at tage højde for eventuelle uoverensstemmelser, som f.eks. underlevering og overlevering. Under produktmodtagelsen skal du angive et produktmodtagelses-id, som typisk er en reference til følgesedlen fra leverandøren. Dette id er påkrævet ved regnskabsføring, fordi det giver mulighed for kontrol eller revision af leverandørens følgesedler i forhold til, hvad der er modtaget, og de tilskrevne lager eller udgifter.  

Hvis en medarbejder har bestilt varer ved hjælp af en indkøbsrekvisition, kan medarbejderen blive anmodet om at bekræfte modtagelsen af produktet selv. Du kan konfigurere denne funktionsmåde ved hjælp af en arbejdsgang. Du kan konfigurere betingelser for arbejdsgange, så de stemmer overens med din forretningsproces.  

IO'er kan oprettes for produkter, der ikke er beregnet som lager, men betragtes som en udgift. Denne kategori omfatter ordrelinjer, hvor produkterne er markeret som **Ikke på lager** af deres lagermodelgruppe, og også linjer, der bruger indkøbskategorier. Varerne kan i så fald ikke passere gennem registrering ved ankomst og modtagelse på lagerstedet. I stedet for bruges handlingen **Produktkvittering** til at registrere modtagelsen direkte på indkøbsordren, og modtagelsen baseres på det bestilte antal og ikke et registreret antal.  

Du kan oprette indkøbsordrelinjer, hvor indstillingen **Nyt anlægsaktiv** er aktiveret. Denne indstilling angiver, at indkøbet skal betragtes som et anlægsaktiv i stedet for lager. I dette tilfælde bestemmer de regler for fastlæggelse af anlægsaktivet, der er konfigureret, om købet af produktet eller kategorien overstiger bestemte tærskler, og de skal derfor tages i betragtning som et aktiv og underlægges styring af anlægsaktiver. Indkøb kan også foretages med henblik på et eksisterende anlægsaktiv. I så fald justeres beløbet efter behov.  

Du kan vælge flere ordrer og udføre modtagelse på alle disse ordrer sammen. Denne fremgangsmåde bruges ikke ofte, men kan du bruge den, hvis en leverandør har konsolideret leverancer til dig i en enkelt belastning. Under produktkvitteringen for køb er der en funktion til at foretage samleopdateringer. Med samleopdateringer kan du bogføre en enkelt følgeseddel fra leverandøren til mere end én indkøbsordre.  

IO'er kan oprettes fra en salgsordre, hvor indstillingen **Direkte levering** er valgt. Når du bruger direkte levering, ankommer produkterne aldrig til lageret, men leveres direkte fra leverandøren til kunden. I sådanne tilfælde registreres modtagelsen normalt direkte på indkøbsordren. Modtagelsen kan ske automatisk som f.eks. via EDI-integration (Electronic Data Interchange) med leverandøren. Alternativt, hvis indkøbsordren er en intern indkøbsordre, automatiserer Microsoft Dynamics 365 for Finance and Operations modtagelsen på den interne salgsordre, når forsendelsen sker. Når du bruger direkte levering, figurerer produkter stadig som lager, selvom de ikke fysisk ankommer til lageret. Derfor, når produktkvitteringen registreres på indkøbsordren, opdateres salgsordren automatisk med en følgeseddel, så den overordnede ændring til lageret er 0 (nul). Du bør ikke kræve forudregistrering i scenarier for direkte levering. Hvis du bruger lagersteder, der er aktiveret for lagerstedsstyring, kan du omgå kravet om nummerpladeregistrering ved at angive et virtuelt lagersted i stedet. Du kan angive dette lagersted i feltet **Lagersted til direkte levering** på produktet. 

Når produktkvitteringen er blevet behandlet på indkøbsordren, indstilles indkøbsordrestatus til **Modtaget** for at angive, at fakturaen kan behandles for ordren. Du kan få vist oplysninger om produkter, der allerede er modtaget, ved hjælp af siden **Produktkvitteringskladder**.  

Du kan få adgang til denne side fra handlingsgruppen **Tilgang** på siden **Indkøbsordre**. Oplysningerne i kladderne indeholder detaljer om antal, datoer og dimensioner.

<a name="see-also"></a>Se også
--------

[Oversigt over indkøbsordrer](purchase-order-overview.md)

[Oprettelse af indkøbsordre](purchase-order-creation.md)

[Godkendelse og bekræftelse af indkøbsordre](purchase-order-approval-confirmation.md)

[Oversigt over kreditorfakturaer](../../financials/accounts-payable/vendor-invoices-overview.md)




