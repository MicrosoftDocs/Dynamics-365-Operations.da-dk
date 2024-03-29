---
title: Listeside med debitortransaktioner
description: Denne artikel indeholder oplysninger om listesiden Debitorposteringer for Microsoft Dynamics 365 Finance.
author: abruer
ms.date: 08/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 2ca7aaa0ccea8f4936ae4a177ef9b9eba2282ae6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864448"
---
# <a name="customer-transactions-list-page"></a>Listeside med debitortransaktioner

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Vis udligninger

Knappen **Vis udligninger** i handlingsruden giver hurtig adgang til udligningshistorikken og detaljerede oplysninger om udligningsposteringen. Du kan også vise ekstra posteringer, der vedrører den valgte postering, enten fordi de var en del af samme udligning, eller fordi de er betalinger, der er oprettet i samme betalingskladde.

1. Vælg **Debitor \> Alle kunder**.
2. Vælg en kunde med posteringer, og brug derefter handlingsruden under fanen **Kunde** til at vælge **Posteringer**.
3. Vælg en postering til undersøgelse, og vælg derefter **Vis udligninger** i handlingsruden.

    Dialogboksen **Vis udligninger** viser den valgte postering og alle dokumenter, der er udlignet mod den. Denne dialogboks ligner udligningshistorikvisningen, men den omfatter alle relaterede dokumenter.

4. Du kan udføre forskellige opgaver i dialogboksen. Vælg et eller flere bilag, og vælg derefter en af følgende knapper:

    - **Vis relateret** – Få vist alle posteringer i betalingskladde og transaktioner i finanskladde for den debitor, der er oprettet i de kladder, som de dokumenter, der vises på listen, blev oprettet i. Hvis der f.eks. vises en betaling, vises alle betalingerne i betalingskladden, den blev oprettet i. Hvis en faktura eller betaling vises, og den blev oprettet i en finanskladde, vises alle dokumenter i finanskladden, hvor den blev oprettet. Alle de udligninger, der er knyttet til listen over dokumenter, vises også. Mens du får vist relaterede betalinger, ændres navnet på denne knap til **Vis udligninger**. Vælg **Vis udligninger** for kun at se de posteringer, der blev vist, da du åbnede dialogboksen **Vis udligninger**.
    - **Vis historik** – Få vist udligningshistorik for bilagene. Vælg **Luk** for at lukke dialogboksen.
    - **Vis regnskab** – Vis alle bilag, der har relation til de valgte dokumenter. Vælg **Luk** for at lukke dialogboksen.
    - **Eksporter** – Eksporter de valgte bilag til Microsoft Excel.
    - **Udlign posteringer** – Denne knap vises kun, hvis det oprindelige dokument, der blev valgt, ikke blev fuldt udlignet. Når du vælger denne knap, vises dialogboksen **Udlign posteringer**, hvor du kan vælge posteringer til udligning.
    - **Fortryd udligning** – Denne knap vises kun, hvis det oprindelige dokument, der blev valgt, blev fuldt udlignet. Når du vælger denne knap, vises dialogboksen **Fortryd udligning**, hvor du kan fortryde udligninger, der blev udført for det pågældende dokument.

## <a name="global-transactions"></a>Globale transaktioner

Knappen **Globale transaktioner** vises også på listesiden **Debitorposteringer**. Med denne knap kan du få vist alle posteringer for en debitor på tværs af alle juridiske enheder. **Debitorposteringer**-listesiden viser kun transaktioner for de juridiske enheder, som brugeren har adgang til, på basis af deres sikkerhedsindstillinger.

Listesiden viser alle transaktioner for debitorer, der har samme part-id som den debitor, du startede med. Hvis debitoren US-001 i én juridisk enhed f.eks. har samme part-id som debitoren DE-001 i en anden juridisk enhed, vises alle transaktioner for begge debitor-id'er.

Menuerne på **Debitorposteringer**-listesiden varierer, afhængigt af den juridiske enhed for posteringen. Hvis en funktion f.eks. kun er tilgængelig for danske juridiske enheder, vises menuindstillinger for denne funktion kun, når en dansk postering er valgt.

Følg disse trin for at få adgang til funktionen.

1. Vælg **Debitor \> Alle kunder**.
2. Vælg en debitor, og brug derefter handlingsruden under fanen **Debitor** i gruppen **Transaktioner** til at vælge **Globale transaktioner**.

## <a name="more-transaction-filters"></a>Flere transaktionsfiltre 

Filteret til at vise åbne transaktioner er blevet erstattet med et nyt filter, så du kan få vist flere kombinationer af transaktioner. Du kan vælge mellem følgende indstillinger i feltet **Vis**:

- **Alle** – Vis alle transaktioner for de valgte debitorer (åbne og lukkede).
- **Lukkede** – Vis kun de transaktioner, der er fuldt udlignet og lukket.
- **Åbne** – Vis kun de transaktioner, der ikke er fuldt udlignet.
- **Åbne, herunder lukkede på eller efter datoen** – Vis kun transaktioner, der ikke er fuldt udlignet på eller efter en dato, du angiver. Når du vælger denne indstilling, kan du ændre den dato, der vises ud for filteret. Transaktioner, der har værdien **Sidste udligningsdato** på eller efter den dato, du angiver, vises på listen, selvom disse transaktioner er fuldt udlignet pr. dags dato. Saldoen viser dog saldi pr. dags dato, ikke fra den valgte dato.

Markér afkrydsningsfeltet **Skjul værdireguleringer af valuta** for at skjule valutaomregningstransaktioner.

## <a name="modify-due-dates-and-discount-dates"></a>Redigere forfaldsdatoer og rabatdatoer

Du kan opdatere forfaldsdatoer og rabatdatoer for åbne debitorposteringer. I version 8.1 kan du nu tilføje forfaldsdatoer på listesiden **Debitorposteringer**. Ved at klikke på forfaldsdatoen på **Debitorposteringer**-listesiden kan du også ændre forfaldsdatoer, rabatdatoer, betalingsbetingelser og kasserabatvilkår i dialogboksen **Opdater forfaldsdato og kasserabatdatoer**.

### <a name="activate-the-feature"></a>Aktivér funktionen

Hvis du vil tilføje forfaldsdatoer på **Debitorposteringer**-listesiden og ændre betalingsindstillingerne for en transaktion i dialogboksen **Opdater forfaldsdato og kasserabatdatoer**, skal du følge disse trin.

1. Vælg **Debitor \> Opsætning \> Debitorparametre**.
2. På fanen **Udligninger** skal du angive indstillingen **Vis forfaldsdato, og tillad redigering** til **Ja**.
3. For at aktivere denne funktion er der tilføjet nye felter i debitorposteringer. Disse felter skal udfyldes, når en ny postering fuldføres. De vil også blive udfyldt, når du åbner dialogboksen **Opdater forfaldsdato og kasserabatdatoer**. Når du angiver indstillingen **Vis forfaldsdato, og tillad redigering** til **Ja**, kan du se dialogboksen **Opdater betalingsoplysninger**.  Hvis du vil opdatere eksisterende posteringer med det samme, skal du vælge **Opdater alle eksisterende posteringer**. Alternativt kan du vælge kun at udfylde felterne for nye posteringer ved at vælge **Fortsæt uden opdatering**.

Forfaldsdatoen er nu føjet til **Debitorposteringer**-listesiden, så du nemt kan ændre forfaldsdatoen og kasserabatdatoer for posteringer.

### <a name="modify-the-payment-settings"></a>Rediger betalingsindstillingerne

**Debitorposteringer**-listesiden indeholder alle posteringer for en debitor. Når du vælger forfaldsdatoen for en postering, vises dialogboksen **Opdater forfaldsdato og kasserabatdatoer**. Denne dialogboks viser stamdata for forfaldsdato og rabatberegninger, forfaldsdato, betalingsbetingelser, kasserabatbetingelser og kasserabatdatoer.

Hvert felt har en særskilt virkning på posteringen, når du redigerer den:

- **Rediger basisdato:** - Forfaldsdatoen og rabatdatoerne ændres, hvis basisdatoen er dokumentdatoen.
- **Rediger forfaldsdatoen:** - Kun forfaldsdatoen ændres.
- **Rediger rabatdatoerne :** - Kun rabatdatoerne ændres.
- **Rediger betalingsbetingelserne:** - Forfaldsdatoen ændres på basis af basisdatoen og betalingsbetingelserne.
- **Rediger kasserabatbetingelserne:** - Kasserabatterne ændres på basis af basisdatoen og kasserabatbetingelserne.

Når du er færdig med at redigere betalingsindstillingerne, skal du vælge **Luk** for at gemme ændringerne.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
