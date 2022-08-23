---
title: Forudbetalingsfakturaer vs. forudbetalinger
description: Denne artikel beskriver og sammenligner de to metoder, som organisationer kan bruge til betaling af forskud (forudbetalinger).
author: abruer
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 901683f2176189ce2f4186b4f9b3b5c64ec9f2b1
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227769"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Forudbetalingsfakturaer vs. forudbetalinger

[!include [banner](../includes/banner.md)]

Denne artikel beskriver og sammenligner de to metoder, som organisationer kan bruge til betaling af forskud (forudbetalinger). I den ene metode, kan du oprette en forudbetalingsfaktura, der er tilknyttet en indkøbsordre. I den anden metode kan du oprette kladdebilag for forudbetaling ved at oprette kladdeposteringer og markere dem som kladdebilag for forudbetaling.

Organisationer kan udstede forudbetalinger til kreditorer for varer eller tjenester, før varerne eller tjenesterne er opfyldt. To metoder kan bruges til at udstede forudbetalinger til kreditorer. Hvis du vil minimere risikoen, kan du spore forudbetalinger ved at definere forudbetalingen i en indkøbsordre. I forbindelse med denne metode skal du oprette en forudbetalingsfaktura, der er tilknyttet en indkøbsordre. Denne metode kaldes forudbetalingsfakturering. Organisationer, der ikke ønsker at spore forudbetalinger så tæt, eller som ikke modtager en forudbetalingsfaktura fra deres leverandør, kan bruge kladdebilag for forudbetaling i stedet for metoden til forudbetalingsfaktura. Du kan oprette kladdebilag for forudbetaling ved at oprette kladdeposteringer og markere dem som kladdebilag for forudbetaling. I forbindelse med denne metode kan du ikke spore, hvilke forudbetalinger der foretages til en kreditor i forhold til hvilke indkøbsordrer. Du kan dog markere en bogført forudbetaling som udlignet mod en indkøbsordre.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Hvornår skal jeg bruge forudbetalingsfakturering vs. forudbetalinger

| Forudbetalingsfakturering                                                                | Forudbetalinger                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Definer forudbetalingsværdi på en indkøbsordre.                                    | Der er ikke defineret en forudbetalingsværdi på en indkøbsordre.                    |
| En forudbetalingsfaktura og en endelig faktura skal bogføres.                       | Ingen forudbetalingsfaktura skal bogføres.                                    |
| Ansvar for forudbetalingen er på forudbetalingskontoen, ikke på kreditorkontoen. | Ansvar for forudbetalingen er på kreditorkontoen.                  |
| Kreditorsaldoen afspejler ikke forudbetalingsværdien under hele processen.     | Kreditorsaldoen afspejler forudbetalingsværdien under hele processen. |
| Forudbetalingsfakturering er kun tilgængelig i Kreditor.                         | Forudbetalinger er også tilgængelige i Debitor og Kreditor.    |

## <a name="overview-of-the-prepayment-process"></a>Oversigt over forudbetalingsprocessen
I mange lande/områder er det regnskabspraksis, at forudbetalinger fra en debitor eller til en kreditor ikke bogføres på de sædvanlige samlekonti for den pågældende debitor eller kreditor. Disse forudbetalinger bogføres i stedet på særlige finanskonti til forudbetalinger. Når der oprettes en salgsordre eller indkøbsordre, udstedes en faktura til debitoren eller fra kreditoren. Når fakturaen betales, tilbageføres kladdebilaget for forudbetaling og bilaget for forudbetalt moms på finanskontiene for forudbetalinger, og fakturabeløbene bogføres automatisk på de sædvanlige samlekonti. Benyt følgende fremgangsmåde for at oprette en forudbetaling.

1.  Konfigurer posteringsprofiler til forudbetalinger.
2.  I debitorparametre og kreditorparametre, under **Finans og moms** skal du vælge den nye posteringsprofil ved hjælp af parameteren for **posteringsprofilen til betalingskladden med forudbetaling**.
3.  Opret en betalingskladde, og opret derefter en ny betaling.
4.  Du kan markere betalingen som forudbetaling. Hvis en betaling er markeret som en forudbetaling, er betalingen bogført på finanskonti, der er defineret på den posteringsprofil, du har oprettet i trin 1 og 2. Og hvis betalingen er markeret som en forudbetaling, beregnes der moms. Nogle regeringer kræver, at momsen betales, når der registreres en forudbetaling, selvom der ikke er en faktura.
5.  Bogfør forudbetalingen.
6.  Valgfrit: Du kan udligne forudbetaling på indkøbsordren eller salgsordren, før du opretter fakturaen. På siden for salgsordren eller indkøbsordren i handlingsruden skal du bruge **Udlign transaktioner**.
7.  Når kreditoren leverer varerne eller tjenesterne, kan du registrere fakturaen. Hvis du har udlignet forudbetaling mod indkøbsordren eller salgsordren i trin 6, udlignes forudbetalingen automatisk mod den faktura, du har oprettet. Hvis du ikke har udlignet forudbetaling mod indkøbsordren eller salgsordren, kan du manuelt udligne den mod fakturaen ved hjælp af **Udlign transaktioner** på debitor- eller kreditorsider. Forudbetalingsbeløbet tilbageføres derefter fra den midlertidige debitor- eller kreditorfinanskonto. Og hvis der blev beregnet moms, ændres de, da fakturaen indeholder de faktiske momsafgifter.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Oversigt over processen for forudbetalingsfakturering
Forudbetalingsfakturaer er en del af almindelig forretningspraksis. En kreditor udsteder forudbetalingsfakturaer for at kræve et depositum for køb, før indkøbsordren er opfyldt. Nogle kreditorer kan f.eks. kræve forudbetaling for bestemte varer eller tjenester. Hvis en kreditor udsteder en faktura, der kræver forudbetaling, kan du bruge forudbetalingsfakturering. En værdi for forudbetaling kan defineres på indkøbsordren, der registreres og betales en forudbetalingsfaktura, og derefter anvendes forudbetalingsfakturaen på den endelige faktura. Benyt følgende fremgangsmåde for at oprette en forudbetaling.

1.  Indkøberen opretter, bekræfter og sender derefter en indkøbsordre, som kreditoren har anmodet om forudbetaling for. Værdien af forudbetalingen er defineret på indkøbsordren som en del af aftalen.
2.  Kreditoren sender en forudbetalingsfaktura.
3.  Kreditorkoordinatoren registrerer forudbetalingsfakturaen på indkøbsordren, og derefter betales forudbetalingsfakturaen.
4.  Kreditoren sender en anmodning om betaling, der kaldes en standardkreditorfaktura. Når kreditoren leverer varerne eller tjenesterne, og de tilhørende standardkreditorfakturaer er modtaget, anvender kreditorkoordinatoren det forudbetalingsbeløb, der allerede er betalt på standardfakturaen.
5.  Kreditorkoordinatoren betaler og udligner det resterende beløb på standardfakturaen.

## <a name="set-up-parameters-to-enable-the-prepayment-invoicing-process"></a>Konfigurere parametre for at aktivere faktureringsprocessen til forudbetaling
Der skal defineres en forudbetalingskonto under fanen **Indkøbsordre** på siden **Lagerbogføring** (**Lagerstyring \> Konfiguration \> Bogføring \> Bogføring**). Forudbetalingskontoen opdateres, normalt debiteres, når forudbetalingsfakturaen bogføres. Saldoen på forudbetalingskontoen tilbageføres, når den standardfaktura, der er anvendt på forudbetalingsfakturaen, bogføres. Hvis du ikke udligner forudbetalingsfakturaen på en betaling, før forudbetalingsfakturaen anvendes på standardfakturaen, tilbageføres regnskabsposterne fra den bogførte forudbetalingsfaktura, når standardfakturaen bogføres.

Den modkonto, der udligner kreditorkontoen, defineres i **Kreditorpostering**-profilen. Hvis du vil definere standardposteringsprofilen, skal du klikke på **Kreditor \>Konfiguration \> Kreditorparametre \>Finans og moms \> Bogføringsprofil med kreditorfaktura for forudbetaling**.

**Politikken for anvendelse af forudbetaling** angiver, om systemet automatisk vil anvende udlignede forudbetalingsfakturaer på den endelige faktura, der er oprettet manuelt. Fakturaer, der oprettes ved hjælp af en dataenhed, henviser ikke til **Politik for anvendelse af forudbetaling**. Du skal anvende udlignede forudbetalingsfakturaer manuelt på fakturaer, der er oprettet ved hjælp af en dataenhed. Hvis du vil definere politikken, skal du gå til **Kreditor \>Konfiguration \> Kreditorparametre \> Finans og moms \> Politik for anvendelse af forudbetaling**. Hvis feltet **Politik for anvendelse af forudbetaling** er angivet til **Automatisk**, markeres forudbetalingsfakturaen automatisk til udligning med den endelige faktura. Hvis feltet er angivet til **Besked**, vises en visuel angivelse af, at der er en tilgængelig forudbetalingsfaktura til anvendelse, når den endelige faktura oprettes.

## <a name="create-a-purchase-order-that-contains-prepayment-invoice-information"></a>Oprette en indkøbsordre, der indeholder oplysninger om forudbetalingsfaktura
Når en leverandør fortæller dig, at de kræver forudbetaling for varer og tjenester i en indkøbsordre, skal du definere forudbetalingsværdien for den tilknyttede indkøbsordre. Gå til **Kreditor \> Almindelige \> Indkøbsordrer \> Alle indkøbsordrer**, og find leverandørens indkøbsordre. Vælg fanen **Indkøb**, i handlingsruden, og vælg derefter **Forudbetaling**. Angiv oplysninger om forudbetalingen, herunder en beskrivelse, værdien af forudbetalingen, om forudbetalingen er et fast beløb eller en procentdel, og et id for forudbetalingskategorien. 

Bemærk, at flere forudbetalingsdefinitioner i en indkøbsordre ikke er tilladt. Hvis du vil tillade flere forudbetalinger på en indkøbsordre, skal du bogføre betalingerne ved hjælp af betalingskladden i stedet for en forudbetalingsfaktura.

Forudbetalingen kan fjernes fra indkøbsordren, medmindre du allerede har udlignet en betaling mod den bogførte forudbetalingsfaktura eller bogført standardfakturaen. Hvis du vil fjerne en forudbetalingsoplysning fra indkøbsordren, skal du vælge **Kreditor \> Almindelige \> Indkøbsordrer \> Alle indkøbsordrer** og finde kreditorens indkøbsordre. Vælg fanen **Indkøb** i handlingsruden, og vælg derefter **Fjern forudbetaling**.

## <a name="create-and-post-a-prepayment-invoice"></a>Oprette og bogføre en forudbetalingsfaktura
Hvis du vil registrere kreditorens forudbetalingsfaktura, skal du gå til siden **Kreditorfaktura** ved at vælge indstillingen **Forudbetalingsfaktura** på siden **Indkøbsordrer** (fanen **Kreditor \> Almindelige \> Indkøbsordrer \> Alle indkøbsordrer \> fanen Faktura \> Forudbetalingsfaktura**). Angiv oplysninger om forudbetalingsfakturaen, herunder fakturanummeret. Du kan ikke ændre antal i en forudbetalingsfaktura. Hvis kreditoren har faktureret et delvist beløb af den forudbetalingsværdi, der er defineret på indkøbsordren, kan du opdatere enhedsprisen, så den afspejler delværdien.

Når forudbetalingsfakturaen bogføres, opdateres kreditorsaldoen og forudbetalingskontoen. Værdien **Anvendelse af forudbetaling** i forudbetalingsdefinitionen, som findes på indkøbsordren, opdateres også. De økonomiske standarddimensionsposter for det bogførte forudbetalingsbilag tages fra overskriftsoplysningerne på indkøbsordren.

Hvis funktionen **Lås økonomiske dimensioner på fakturalinjer på kreditorforudbetalingsfaktura** på siden **Funktionsstyring** er aktiveret, kan dimensionerne i forudbetalingshovedet eller -linjerne ikke opdateres. 

## <a name="post-and-settle-payments-for-the-prepayment-invoice"></a>Bogføre og udligne betalinger for forudbetalingsfakturaen
Derefter betales forudbetalingsfakturaen fra siden **Betalingskladde**. Klik på **Kreditor \> Kladder \> Betalinger \> Betalingskladde** for at få adgang til betalingskladder. Når udligningen af betalingen er bogført på forudbetalingsfakturaen, opdateres indkøbsordrens **Restværdi for anvendelse af forudbetaling**.

Før du bogfører standardfakturaen for forudbetalingsfakturaen, kan du tilbageføre udligningen af betalingen fra forudbetalingsfakturaen. Men når der er anvendt en standardfaktura på forudbetalingsfakturaen, kan du ikke tilbageføre udligningen af betalingen fra forudbetalingsfakturaen.

## <a name="post-the-standard-vendor-invoice-for-the-purchase-order-and-apply-the-prepayment-invoice-to-the-standard-invoice"></a>Bogføre standardleverandørfakturaen for indkøbsordren og anvende forudbetalingsfakturaen på standardfakturaen
Registrer den standardfaktura, der er modtaget fra kreditoren. Som en del af denne proces kan du anvende den udlignede forudbetalingsfaktura på kreditorfakturaen, så fakturaens værdi reduceres med det beløb, der allerede er betalt. Hvis du anvender forudbetalingsfakturaen på kreditorfakturaen, sikrer du, at regnskabsposter fra forudbetalingsfakturaen tilbageføres.

## <a name="application-of-the-prepayment-invoice-after-posting-the-standard-invoice"></a>Anvendelse af forudbetalingsfakturaen efter bogføring af standardfakturaen
Hvis du glemmer at anvende forudbetalingen på standardkreditorfakturaen på tidspunktet for bogføring af kreditorfakturaen, kan den udlignede forudbetaling anvendes på andre fakturaer fra denne kreditor fra siden **Kreditorer** (**Kreditor \> Almindelige \> Kreditorer \> Alle kreditorer \> fanen Faktura \> Anvend**).

## <a name="reversal-of-the-prepayment-application-process"></a>Tilbageførsel af processen til anvendelse af forudbetaling
Hvis du har brug for at fjerne udligningen af eller tilbageføre anvendelsen af en forudbetalingsfaktura fra en standardfaktura, skal du vælge handlingen **Tilbagefør** på siden **Kreditorer** (**Kreditor \> Almindelige \> Kreditorer \> Alle kreditorer \> fanen Faktura \> Tilbagefør**). Når anvendelsen af forudbetaling er tilbageført, kan du anvende forudbetalingen på en anden standardfaktura. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
