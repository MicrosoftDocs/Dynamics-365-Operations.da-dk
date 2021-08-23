---
title: Understøttelse af momsfunktion til flytteordrer
description: Dette emne forklarer den nye understøttelse af momsfunktionen til flytteordrer ved hjælp af tjenesten til beregning af moms.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1c47c327841b8c712220e440e2aa6b4fe2b31b4a1ccd03dc0a200dbeb7394071
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721683"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Understøttelse af momsfunktion til flytteordrer

[!include [banner](../../includes/banner.md)]

Dette emne indeholder oplysninger om momsberegning og bogføringsintegration i flytteordrer. Denne funktionalitet giver dig mulighed for at konfigurere momsberegning og bogføring i flytteordrer til lageroverførsler. I henhold til EU's regler om moms betragtes lageroverførsler som fællesskabsforsyninger og -anskaffelser inden for EU.

Hvis du vil konfigurere og bruge denne funktion, skal du udføre tre hovedtrin:

1. **RCS-konfiguration:** I Regulatory Configuration Service skal du konfigurere momsfunktionen, momskoder og momskoders anvendelighed for bestemmelse af momskode i flytteordrer.
2. **Finance-opsætning:** I Microsoft Dynamics 365 Finance kan du aktivere funktionen **Moms i flytteordre**, konfigurere parametrene for momstjenesten til lageret og konfigurere kernemomsparametre.
3. **Lageropsætning:** Konfigurer lagerkonfigurationen for flytteordreposteringer.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Konfigurere RCS til moms- og flytteordretransaktioner

Benyt følgende fremgangsmåde for at konfigurere momsen for en flytteordre. I det eksempel, der vises her, er flytteordren fra Nederlandene til Belgien.

1. Vælg kladdefunktionsversionen under fanen **Versioner** på siden **Momsfunktioner**, og vælg derefter **Rediger**.

    ![Vælge Rediger.](../media/tax-feature-support-01.png)

2. Vælg **Tilføj** under fanen **Momskoder** på siden **Konfiguration af momsfunktioner** for at oprette nye momskoder. I dette eksempel er der oprettet tre momskoder: **NL-Exempt**, **BE-RC-21** og **BE-RC+21**.

    - Når en flytteordre afsendes fra et lagersted i Nederlandene, anvendes Nederlandenes momsfritagelseskode (**NL-Exempt**).
      
        Opret momskoden **NL-Exempt**.
        1. Vælg **Tilføj**, og angiv **NL-Exempt** i feltet **Momskode**.
        2. Vælg **Efter nettobeløb** i feltet **Momskomponent**.
        3. Vælg **Gem**.
        4. Vælg **Tilføj** i tabellen **Sats**.
        5. Skift **Er momsfri** til **Ja** i afsnittet **Generelt**.

        ![NL-Exempt momskode.](../media/tax-feature-support-02.png)

    - Når en flytteordre modtages på et lagersted i Belgien, anvendes modtagermomsmekanismen med momskoderne **BE-RC-21** og **BE-RC+21**.
        
        Opret momskoden **BE-RC-21**.      
        1. Vælg **Tilføj**, og angiv **BE-RC-21** i feltet **Momskode**.
        2. Vælg **Efter nettobeløb** i feltet **Momskomponent**.
        3. Vælg **Gem**.
        4. Vælg **Tilføj** i tabellen **Sats**.
        5. Angiv **-21** i feltet **Momssats**.
        6. Skift **Er modtagermoms** til **Ja** i afsnittet **Generelt**.
        7. Vælg **Gem**.

        ![BE-RC-21-momskode for modtagermoms.](../media/tax-feature-support-03.png)
        
        Opret momskoden **BE-RC+21**.
        1. Vælg **Tilføj**, og angiv **BE-RC-21** i feltet **Momskode**.
        2. Vælg **Efter nettobeløb** i feltet **Momskomponent**.
        3. Vælg **Gem**.
        4. Vælg **Tilføj** i tabellen **Sats**.
        5. Angiv **21** i feltet **Momssats**.
        6. Vælg **Gem**.

        ![BE-RC+21-momskode for modtagermoms.](../media/tax-feature-support-04.png)

3. Definer anvendeligheden af momskoderne.

    1. Vælg **Administrer kolonner**, og vælg derefter kolonner, der skal bruges til at opbygge anvendelighedstabellen.

        > [!NOTE]
        > Sørg for at føje kolonnerne **Forretningsproces** og **Momsretninger** til tabellen. Begge kolonner er vigtige for momsfunktionen i flytteordrer.

    2. Tilføj anvendelighedsregler. Lad ikke felterne **Momskoder**, **Momsgruppe** og **Varemomsgruppe** være tomme.
        
        Tilføj en ny regel for forsendelse af flytteordre.
        1. Vælg **Tilføj** i tabellen **Anvendelighedsregler**.
        2. Vælg **Lager** i feltet **Forretningsproces** for at gøre reglen gældende for en flytteordre.
        3. I feltet **Afsend fra land/område** skal du angive **NLD**.
        4. I feltet **Levér til land/område** skal du angive **BEL**.
        5. Vælg **Output** i feltet **Momsretning** for at gøre reglen gældende for forsendelse af flytteordre.
        6. Vælg **NL-Exempt** i feltet **Momskoder**.
        7. Angiv den relaterede momsgruppe og varemomsgruppe, der er defineret i dit Finance-system, i feltet **Momsgruppe** og **Varemomsgruppe**.
        
        Tilføj en ny regel for modtagelse af flytteordre.
        1. Vælg **Tilføj** i tabellen **Anvendelighedsregler**.
        2. Vælg **Lager** i feltet **Forretningsproces** for at gøre reglen gældende for en flytteordre.
        3. I feltet **Afsend fra land/område** skal du angive **NLD**.
        4. I feltet **Levér til land/område** skal du angive **BEL**.
        5. Vælg **Input** i feltet **Momsretning** for at gøre reglen gældende for modtagelse af flytteordre.
        6. Vælg **BE-RC+21** og **BE-RC-21** i feltet **Momskoder**.
        7. Angiv den relaterede momsgruppe og varemomsgruppe, der er defineret i dit Finance-system, i feltet **Momsgruppe** og **Varemomsgruppe**.

        ![Anvendelighedsregler.](../media/image5.png)

4. Fuldfør og publicer den nye momsfunktionsversion.

    [![Ændre status for den nye version.](../media/image6.png)](../media/image6.png)

## <a name="set-up-finance-for-transfer-order-transactions"></a>Konfigurere Finance til moms- og flytteordretransaktioner

Hvis du vil aktivere og konfigurere moms til flytteordrer, skal du følge disse trin.

1. Gå i Finance til **Arbejdsområder** \> **Funktionsstyring**.
2. Find og vælg funktionen **Moms i flytteordre** på listen, og vælg derefter **Aktivér nu** for at aktivere den.

    > [!IMPORTANT]
    > Funktionen **Moms i flytteordre** er fuldstændig afhængig af momstjenesten. Du kan derfor kun aktivere den, når du har installeret momstjenesten.

    ![Funktionen Moms i flytteordre.](../media/image7.png)

3. Aktivér momstjenesten, og vælg forretningsprocessen **Lager**.

    > [!IMPORTANT]
    > Du skal udføre dette trin for hver juridiske enhed i Finance, hvor momstjenesten og funktionerne for moms i flytteordrer skal være tilgængelige.

    1. Gå til **Moms** \> **Konfiguration** \> **Momskonfiguration** \> **Konfiguration af momstjeneste**.
    2. Vælg **Lager** i feltet **Forretningsproces**.

    ![Angive feltet Forretningsproces.](../media/image8.png)

4. Kontrollér, at modtagermomsmekanisme er konfigureret. Gå til **Finans** \> **Konfiguration** \> **Parametre**, og sørg for, at fanen **Modtagermoms** har indstillingen **Aktivér modtagermoms** angivet til **Ja**.

    ![Aktivere indstilling for modtagermoms.](../media/image9.png)

5. Kontrollér, at de relaterede momskoder, momsgrupper, varemomsgrupper og momsregistreringsnumre er konfigureret i Finance i overensstemmelse med vejledningerne for momstjenesten.
6. Konfigurere en konto til foreløbig transit. Dette trin er kun påkrævet, når den moms, der anvendes på en flytteordre, ikke gælder for en momsfritagelses eller modtagermomsmekanisme.

    1. Gå til **Moms** \> **Konfiguration** \> **Moms** \> **Finanskonteringsgrupper**.
    2. Vælg en finanskonto i feltet **Foreløbig transit**.

    ![Vælge en konto til foreløbig transit.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Konfigurere basislager flytteordretransaktioner

Benyt følgende fremgangsmåde for at konfigurere basislager for at aktivere flytteordretransaktioner.

1. Opret afsendelse fra- og afsendelse til-steder for lagersteder i forskellige lande eller områder, og tilføj den primære adresse for hvert sted.

    1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Lagersted** \> **Sted**.
    2. Vælg **Ny** for at oprette det sted, du vil tildele et lagersted senere.
    3. Gentag trin 2 for alle de andre steder, du skal oprette.

    > [!NOTE]
    > Et af de steder, du opretter, skal kaldes **Transit**. I senere trin af denne procedure skal du tildele dette sted til transitlagerstedet, så momsrelaterede lagerbilag kan bogføres i "afsendelses"- og "modtagelses"-transaktioner for flytteordrer. Adressen på transitstedet er irrelevant for momsberegningen. Du kan derfor lade feltet være tomt.

    ![Konfigurere steder.](../media/image11.png)

2. Opret afsend fra-, transit- og afsend til-lagersteder. Alle adresseoplysninger, der vedligeholdes på et lagersted, tilsidesætter stedadressen under momsberegningen.

    1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Lagersted** \> **Lagersteder**.
    2. Vælg **Ny** for at oprette et lagersted og tildele det tilhørende sted.
    3. Gentag trin 2 for at oprette et lagersted for hvert sted efter behov.

    ![Konfigurere lagersteder.](../media/image12.png)

    > [!NOTE]
    > I forbindelse med et afsendelse fra-lagersted skal der vælges et transitlagersted i feltet **Transitlagersted** for flytteordretransaktioner.
    >
    > ![Vælge et transitlagersted.](../media/image13.png)

3. Sørg for, at lagerbogføringen er konfigureret for flytteordretransaktioner.

    1. Gå til **Lagerstyring** \> **Konfiguration** \> **Bogføring** \> **Bogføring**.
    2. Kontrollér, at der er konfigureret en finanskonto til både **Lagerafgang** og **Lagertilgang** under fanen **Lager**.

        ![Konfigurere bogføring af lagertilgang og lagerafgang.](../media/image14.png)

    3. Kontrollér, at der er konfigureret en finanskonto til bogføring af **Intern kreditor**.

        ![Konfigurere bogføring af intern kreditor.](../media/image15.png)

    4. Kontrollér, at der er konfigureret en finanskonto til bogføring af **Intern debitor**.

        ![Konfigurere bogføring af intern debitor.](../media/image16.png)
