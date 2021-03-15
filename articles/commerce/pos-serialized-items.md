---
title: Arbejde med serienummererede varer i POS
description: Dette emne forklarer, hvordan du kan håndtere serienummererede varer i POS-programmet.
author: boycezhu
manager: annbe
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 0431ffa45eceac5c12d8ed991b00730c50ca62f8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972549"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Arbejde med serienummererede varer i POS

[!include [banner](includes/banner.md)]

Mange detailhandlere sælger produkter, der kræver en seriel kontrol. Disse produkter kaldes *serienummererede varer*. Nogle detailhandlere kan få brug for at bevare serienumre i et lager eller lagersted til sporingsformål. Andre detailhandlere kan få brug for at registrere serienumre under salgsprocessen mht. service- og garantiformål. Dette emne forklarer, hvordan du kan håndtere serienummererede varer i Microsoft Dynamics 365 Commerce POS-programmet.

## <a name="serial-number-configurations"></a>Serienummerkonfigurationer

En vare betragtes som en serienummereret vare, hvis den er tildelt en sporingsdimensionsgruppe, der er konfigureret til at tillade serienumre. I Commerce Headquarters skal du på siden **Sporingsdimensionsgrupper** vælge indstillingen **Aktiv** for at aktivere serienumre for lagerprocessen eller vælge indstillingen **Aktiv i salgsproces** for at aktivere serienumre for salgsprocessen.

Slå parameteren **Blank tilgang tilladt** til på oversigtspanelet **Sporingsdimensioner** for at tillade, at serienummeret er et valgfrit input under lagertilgangsprocessen for en serienummereret vare. Hvis du deaktiverer denne parameter, skal serienummeret være et obligatorisk input. På samme måde styrer parameteren **Blank afgang tilladt**, om der skal angives et serienummer under processen for lagerforsendelse.

> [!NOTE]
> Hvis du vil bruge operationerne **Indgående lager** og **Udgående lager** til at registrere eller validere serienumre i forhold til en serienummereret vare, skal varen tildeles en sporingsdimensionsgruppe, der er konfigureret til at tillade serienumre for indstillingen **Aktiv** og ikke for indstillingen **Aktiv i salgsproces**.

## <a name="serial-number-management-page"></a>Siden Administration af serienumre

Hvis den vare, der vælges, modtages eller leveres, er en serienummereret vare i POS-handlingerne **Indgående lager** og **Udgående lager**, indeholder **Detaljer**-ruden indstillingen **Administrer serienummer**, der knytter sig til siden **Administration af serienumre**, hvor du kan registrere eller validere serienumre for varen. Du kan også åbne siden **Administration af serienumre** ved at vælge handlingen **Serienummer** på applinjen i visningen med ordredetaljer eller ved at vælge **Administrer serienummer** i den dialogboks, der vises under modtagelses- eller forsendelsesprocessen. 

Siden **Administration af serienumre** viser alle åbne serienummerlinjer, der afventer registrering eller validering. Der kan være to faner på denne side: en for den aktuelle vare og en anden for alle de serienummererede varer i ordren.

Feltet **Status** på siden **Administration af serienumre** indeholder oplysninger om den aktuelle status for hvert serienummer:

- **Ikke registreret** – serienummeret er ikke leveret, eller det allerede registrerede serienummer er endnu ikke valideret (i modtagelsesprocessen).
- **Registreret** – serienummeret er registreret og gemt lokalt i butikkens kanaldatabase, eller det allerede registrerede serienummer er blevet valideret. Der sendes kun serienumre, der har status som **Registreret**, til Commerce Headquarters, når du er færdig med modtagelsen eller opfyldningen.

## <a name="receive-serialized-items"></a>Modtage serienummerede varer

Operationen **Indgående lager** i POS giver brugere mulighed for at udføre følgende opgaver for serienummererede varer:

- Registrér serienumre i forhold til serienummererede varer, når disse varer modtages i butikken via en indkøbsordre.
- Valider serienumre, der er registreret på forhånd, i forhold til serienummererede varer, når disse varer modtages i butikken via en indkøbsordre eller flytteordre.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrere serienumre i forhold til serienummererede varer

I forbindelse med en indkøbsordre vises en dialogboks med indstillingen **Administrer serienummer** under tilgangsprocessen for en serienummereret vare. Du kan vælge denne indstilling for at åbne siden **Administration af serienumre** og begynde at registrere serienumre. Du kan også springe dette trin over under tilgangsprocessen og angive dette input senere, før tilgangen bogføres.

Fanen for den aktuelle vare vises som standard. Alle serienummerlinjer har en tom serienummerværdi og statussen **Ikke registreret**. Du kan scanne serienummerstregkoder, eller du kan vælge **Serienummer** på applinjen for at angive serienumre løbende. De serienumre, du angiver, vises på listen, og deres status ændres til **Registreret**. Det maksimale antal serienumre, du kan registrere på listen, er lig med tilgangsantallet. Hvis du laver en fejl, kan du vælge **Rediger** eller **Ryd** i ruden **Detaljer** for at ændre de angivne serienumre.

Du kan også registrere serienumre på fanen **Alle serienummererede varer** på siden **Administration af serienumre**. På listen skal du vælge den vare, du vil registrere serienumre for.

### <a name="validate-serial-numbers-on-serialized-items"></a>Validere serienumre for serienummererede varer

I forbindelse med en flytteordre skal den udgående side forudregistrere serienumre for de serienummerede varer under forsendelsesprocessen. For en indkøbsordre kan leverandøren levere serienummeroplysninger via en Advance Shipping Notice (ASN), og du kan forudregistrere numrene på de varer, der skal sendes. I begge tilfælde kendes serienumrene før tilgangen. På den indgående side skal du derfor blot validere, at du har modtaget det, du skulle modtage.

Hvis du vil validere serienumre, kan du åbne siden **Administration af serienumre** under tilgangsprocessen eller når som helst, før tilgangen bogføres. For hver serienummereret vare, der forudregistrerede serienumre, angives alle serienumre automatisk til den indledende status **Ikke registreret** på denne side. Hvis du vil validere serienumre, kan du scanne eller angive dem. Når serienumre angives, validerer programmet, om de stemmer overens med de forudregistrerede serienumre. Hvis de stemmer overens, ændres deres status til **Registreret**. Ellers får du en fejlmeddelelse. Du kan også vælge et serienummer direkte og derefter vælge indstillingen **Valider serienummer** i **Detaljer**-ruden for hurtigt at markere dette serienummer som valideret. Det maksimale antal serienumre, du kan validere på listen, er lig med tilgangsantallet.

Du kan også validere serienumre på fanen **Alle serienummererede varer** på siden **Administration af serienumre**. På listen skal du vælge den vare, du vil validere serienumre for.

## <a name="ship-serialized-items"></a>Afsende serienummerede varer

Du kan bruge POS-handlingen **Udgående lager** til at registrere serienumre for serienummererede varer, når du afsender dem fra den aktuelle butik via en flytteordre.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrere serienumre i forhold til serienummererede varer

I forbindelse med en flytteordre vises en dialogboks med indstillingen **Administrer serienummer** under forsendelsesprocessen for en serienummereret vare. Du kan vælge indstillingen for at åbne siden **Administration af serienumre** og begynde at registrere serienumre. Du kan også springe dette trin over under forsendelsesprocessen og angive dette input senere, før forsendelsen bogføres.

Fanen for den aktuelle vare vises som standard. Alle serienummerlinjer har en tom serienummerværdi og statussen **Ikke registreret**. Du kan scanne serienummerstregkoder, eller du kan vælge **Serienummer** på applinjen for at angive serienumre løbende. De serienumre, du angiver, vises på listen, og deres status ændres til **Registreret**. Det maksimale antal serienumre, du kan registrere på listen, er lig med forsendelsesantallet. Hvis du laver en fejl, kan du vælge **Rediger** eller **Ryd** i ruden **Detaljer** for at ændre de angivne serienumre.

Du kan også registrere serienumre på fanen **Alle serienummererede varer** på siden **Administration af serienumre**. På listen skal du vælge den vare, du vil registrere serienumre for.

Du kan også aktivere validering af tilgængelige serienumre under serienummerregistreringen i forhold til en udgående flytteordre. Hvis du med denne validering forsøger at afsende et serienummer, der ikke er tilgængeligt i lageret for afsendelseslageret, får du denne valideringsfejl meddelelse, og du skal angive et andet nummer.

Hvis du vil aktivere denne validering, skal du som en forudsætning planlægge følgende job til at køre gentagne gange:

- **Retail og Commerce** > **Retail og Commerce IT** > **Produkter og lager** > **Produkttilgængelighed med sporingsdimensioner**
- **Retail og Commerce** > **Distributionsplaner** > **1130** (**Produkttilgængelighed**)

## <a name="sell-serialized-items-in-pos"></a>Sælge serialiserede varer i POS

Mens kasseprogrammet altid har understøttet salg af serialiserede varer i Commerce version 10.0.17 og senere, kan organisationer aktivere funktioner, der forbedrer den forretningslogik, der udløses, når der sælges produkter, der er konfigureret til sporing af serienummer.

Når funktionen **Udvidet funktion til validering af serienummer i POS-ordreindlæsning og ordreopfyldning** er aktiveret, evalueres følgende produktkonfigurationer, når der sælges produkter i serier i POS:

- Opsætning af **Serietype** for produktet (**aktiv** eller **aktiv i salg**).
- **Blank afgang tilladt**-indstillinger for produktet.
- Indstillinger for **Fysisk negativt lager** for produktet og/eller salgslagerstedet.

### <a name="active-serial-configurations"></a>Aktive seriekonfigurationer

Når der sælges varer i POS, som er konfigureret med en dimension for **Aktiv**-serienummersporing, igangsætter POS valideringslogik, der forhindrer brugere i at fuldføre salget af en vare i serier med et serienummer, der ikke kan findes på salgslagerstedets aktuelle lager. Der er to undtagelser til denne valideringsregel:

- Hvis varen også er konfigureret med **Blank afgang aktiveret**, kan brugere springe indtastningen af serienummeret over, og sælge varen uden angivelse af serienummer.
- Hvis varen og/eller sælgerlagerstedet er konfigureret med **Fysisk negativt lager** aktiveret, accepterer og sælger programmet et serienummer, der ikke kan bekræftes til at være på lageret på det lagersted, hvor det bliver solgt mod. Denne konfiguration gør det muligt, at lagertransaktionen for den pågældende vare/det specifikke serienummer bliver negativ, og systemet vil derfor tillade salg af ukendte serienumre.

> [!IMPORTANT]
> For at sikre, at POS-applikationen kan gennemføre en korrekt kontrol af, om de serienumre, der sælges til varer af typen **Aktiv**, findes på salgslagerstedet, er det et krav, at organisationer ofte kører jobbet **Produkttilgængelighed med sporingsdimensioner** i Commerce Headquarters og det tilhørende distributionsjob for produkttilgængelighed **1130** via Commerce Headquarters. Når der modtages nyt lager til serier til salgslagersteder, for at POS kan kontrollere tilgængeligheden af serienumre, der bliver solgt, skal lagerchefen ofte opdatere kanaldatabasen med de mest opdaterede data til lagertilgængelighed. Jobbet **Produkttilgængelighed med sporingsdimensioner** tager et aktuelt snapshot af den samlede lagerbeholdning, herunder serienumre, for alle firmaets lagersteder. Distributionsjobbet **1130** tager dette lager-snapshot og deler det med alle konfigurerede kanaldatabaser.

### <a name="active-in-sales-process-serial-configurations"></a>Aktive seriekonfigurationer i salgsprocessen

Varer, der er konfigureret med seriedimensionen som **Aktive i salgsprocessen**, gennemgår ikke nogen lagervalideringslogik, da denne konfiguration angiver, at lagerserienumrene ikke er præ-registrerede på lager, og serienumrene kun registreres på salgstidspunktet.  

Hvis **Blank afgang tilladt** også er konfigureret for varer, der er konfigureret til **Aktiv i salgsprocessen**, kan serienummerposten springes over. Hvis **Blank afgang tilladt** ikke er konfigureret, kræver programmet, at brugeren angiver et serienummer, selvom det ikke vil blive valideret i forhold til det tilgængelige lager.

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>Anvende serienumre, når der oprettes POS-transaktioner

POS-programmet beder med det samme brugerne om at registrere serienummer, når de sælger en vare i serier, men programmet giver brugerne mulighed for at springe indtastningen af serienumre over til et bestemt tidspunkt i salgsprocessen. Når brugeren begynder at registrere betaling, gennemtvinger programmet og kræver serienummerpost for alle varer, der ikke er konfigureret til at blive opfyldt via fremtidige forsendelser eller afhentninger. Eventuelle serialiserede varer, der er konfigureret til kontantopfyldning eller carryout-opfyldelse, kræver, at brugeren registrerer serienummeret (eller indvilliger i at lade det være tomt, hvis varekonfigurationen tillader det), inden salget afsluttes.

I forbindelse med varer i serier, der sælges til fremtidig afhentning eller forsendelse, kan kassebrugere først springe angivelse af serienummeret over, og stadig fuldføre oprettelsen af kundeordren.   

> [!NOTE]
> Når du sælger eller opfylder produkter i serier via kasseprogrammet, gennemtvinges et antal på "1" for varer i serier på salgstransaktionen. Det er resultatet af, hvordan oplysningerne om serienummeret spores på salgslinjen. Når du sælger eller opfylder en transaktion for flere varer i serier via kasse, skal hver salgslinje kun konfigureres med et antal på "1". 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>Anvende serienumre under kundeordreopfyldning eller -afhentning

Når du opfylder kundeordrelinjer for produkter i serier ved hjælp af funktionen **Ordreopfyldning** i POS, gennemtvinger POS hentning af serienummeret, før den endelige opfyldelse. Hvis et serienummer derfor ikke angives under den første ordreregistrering, skal det registreres under processen til pluk, pakning eller afsendelse i POS. Der udføres validering ved hvert trin, og brugeren bliver kun bedt om at angive serienummerdata, hvis den mangler eller ikke længere er gyldig. Hvis en bruger f.eks. springer pluk- eller pakketrinnene over, og der med det samme startes en forsendelse, og der ikke er registreret et serienummer for linjen, kræver POS, at serienummeret angives, før det endelige fakturatrin er fuldført. Når du gennemtvinger hentning af serienummeret under ordreopfyldningshandlinger i POS, gælder alle de regler, der tidligere er nævnt i dette emne, stadig. Kun varer i serier, der er konfigureret som **Aktiv**, gennemgår lagervalidering for serienummer. Varer, der er konfigureret som **Aktiv i salgsprocessen**, valideres ikke. Hvis **Fysisk negativt lager** er tilladt for **Aktive** produkter, accepteres et serienummer, uanset tilgængelig beholdning. Hvis **Blank afgang tilladt** er konfigureret for varer, der både er **Aktive** og **Aktive i salgsproces**, kan en bruger lade serienumrene være tomme, hvis det ønskes under pluk-, pakke- og afsendelsestrinnene.

Validering af serienumre finder også sted, når en bruger udfører afhentningshandlingerne for kundeordrer i POS. POS-programmet tillader ikke, at en afhentning færdiggøres på et produkt i serier, medmindre det består valideringerne som nævnt tidligere. Valideringerne baseres altid på produktets sporingsdimension og konfigurationerne af salgslagersteder. 

## <a name="additional-resources"></a>Yderligere ressourcer

[Indgående lagerhandling i POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Udgående lagerhandling i POS](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)


[!INCLUDE[footer-include](../includes/footer-banner.md)]