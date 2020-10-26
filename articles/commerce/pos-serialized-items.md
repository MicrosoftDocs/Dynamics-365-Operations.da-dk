---
title: Arbejde med serienummererede varer i POS
description: Dette emne forklarer, hvordan du kan håndtere serienummererede varer i POS-programmet.
author: boycezhu
manager: annbe
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 6ba01abc3d1a4496ec586a621aa03b4981f84d76
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978357"
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

## <a name="additional-resources"></a>Yderligere ressourcer

[Indgående lagerhandling i POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Udgående lagerhandling i POS](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)
