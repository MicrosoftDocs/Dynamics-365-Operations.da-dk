---
title: Understøttelse af momsfunktion til flytteordrer
description: Dette emne forklarer den nye understøttelse af momsfunktionen til flytteordrer ved hjælp af tjenesten til beregning af moms.
author: Kai-Cloud
ms.date: 10/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f68a3d7ed4384fe5a97f1e59903e3191df6b741
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647707"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Understøttelse af momsfunktion til flytteordrer

[!include [banner](../../includes/banner.md)]

Dette emne indeholder oplysninger om momsberegning og bogføringsintegration i flytteordrer. Denne funktionalitet giver dig mulighed for at konfigurere momsberegning og bogføring i flytteordrer til lageroverførsler. I henhold til EU's regler om moms betragtes lageroverførsler som fællesskabsforsyninger og -anskaffelser inden for EU.

Hvis du vil konfigurere og bruge denne funktion, skal du udføre tre hovedtrin:

1. **RCS-konfiguration:** I Regulatory Configuration Service skal du konfigurere momsfunktionen, momskoder og momskoders anvendelighed for bestemmelse af momskode i flytteordrer.
2. **Dynamics 365 Finance-opsætning**: I Finance kan du aktivere funktionen **Moms i flytteordre**, konfigurere parametrene for momsberegningstjenesten til lageret og konfigurere kernemomsparametre.
3. **Lageropsætning:** Konfigurer lagerkonfigurationen for flytteordreposteringer.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Konfigurere RCS til moms- og flytteordretransaktioner

Benyt følgende fremgangsmåde for at konfigurere momsen for en flytteordre. I det eksempel, der vises her, er flytteordren fra Nederlandene til Belgien.

1. Vælg kladdefunktionsversionen under fanen **Versioner** på siden **Momsfunktioner**, og vælg derefter **Rediger**.

2. Vælg **Tilføj** under fanen **Momskoder** på siden **Konfiguration af momsfunktioner** for at oprette nye momskoder. I dette eksempel er der oprettet tre momskoder: **NL-Exempt**, **BE-RC-21** og **BE-RC+21**.

    - Når en flytteordre afsendes fra et lagersted i Nederlandene, anvendes Nederlandenes momsfritagelseskode (**NL-Exempt**).
      
        Opret momskoden **NL-Exempt**.
        1. Vælg **Tilføj**, og angiv **NL-Exempt** i feltet **Momskode**.
        2. Vælg **Efter nettobeløb** i feltet **Momskomponent**.
        3. Vælg **Gem**.
        4. Vælg **Tilføj** i tabellen **Sats**.
        5. Angiv **Er momsfri** til **Ja** i sektionen **Generelt**.
        6. Angiv **EC** i feltet **Fritagelseskode**.

    - Når en flytteordre modtages på et lagersted i Belgien, anvendes modtagermomsmekanismen med momskoderne **BE-RC-21** og **BE-RC+21**.
        
        Opret momskoden **BE-RC-21**.      
        1. Vælg **Tilføj**, og angiv **BE-RC-21** i feltet **Momskode**.
        2. Vælg **Efter nettobeløb** i feltet **Momskomponent**.
        3. Vælg **Gem**.
        4. Vælg **Tilføj** i tabellen **Sats**.
        5. Angiv **-21** i feltet **Momssats**.
        6. Angiv **Er modtagermoms** til **Ja** i sektionen **Generelt**.
        7. Vælg **Gem**.
        
        Opret momskoden **BE-RC+21**.
        1. Vælg **Tilføj**, og angiv **BE-RC-21** i feltet **Momskode**.
        2. Vælg **Efter nettobeløb** i feltet **Momskomponent**.
        3. Vælg **Gem**.
        4. Vælg **Tilføj** i tabellen **Sats**.
        5. Angiv **21** i feltet **Momssats**.
        6. Vælg **Gem**.

3. Definer momsgruppen.
    1. Vælg **Administrer kolonner**, og vælg derefter linjefeltet **Momsgruppe**.
    2. Vælg **->**, og vælg derefter **OK**.
    3. Vælg **Tilføj** for at tilføje en momsgruppe.
    4. Angiv **AR-EU** i kolonnen **Momsgruppe**, og vælg derefter momskoden **NL-Exempt**.
    5. Vælg **Tilføj** for at tilføje en momsgruppe.
    6. Angiv **RC-VAT** i kolonnen **Momsgruppe**, og vælg derefter momskoderne **BE-RC-21** og **BE-RC+21**.
4. Definer varemomsgruppen.
    1. Vælg **Administrer kolonner**, og vælg derefter linjefeltet **Varemomsgruppe**.
    2. Vælg **->**, og vælg derefter **OK**.
    3. Vælg **Tilføj** for at tilføje en varemomsgruppe.
    4. Angiv **FULL** i kolonnen **Varemomsgruppe**. Vælg momskoderne **BE-RC-21**, **BE-RC+21** og **NL-Exempt**.
5. Definer anvendeligheden af momsgruppen.

    1. Vælg **Administrer kolonner**, og vælg derefter kolonner, der skal bruges til at opbygge anvendelighedstabellen.

        > [!NOTE]
        > Sørg for at føje kolonnerne **Forretningsproces** og **Momsretninger** til tabellen. Begge kolonner er vigtige for momsfunktionen i flytteordrer.

    2. Tilføj anvendelighedsregler. Lad ikke feltet **Momsgruppe** være tomt.
        
        Tilføj en ny regel for forsendelse af flytteordre.
        1. Vælg **Tilføj** i tabellen **Anvendelighedsregler**.
        2. Vælg **Lager** i feltet **Forretningsproces** for at gøre reglen gældende for en flytteordre.
        3. I feltet **Afsend fra land/område** skal du angive **NLD**.
        4. I feltet **Levér til land/område** skal du angive **BEL**.
        5. Vælg **Output** i feltet **Momsretning** for at gøre reglen gældende for forsendelse af flytteordre.
        6. Vælg **AR-EU** i feltet **Momsgruppe**.
        
        Tilføj en ny regel for modtagelse af flytteordre.
        
        1. Vælg **Tilføj** i tabellen **Anvendelighedsregler**.
        2. Vælg **Lager** i feltet **Forretningsproces** for at gøre reglen gældende for en flytteordre.
        3. I feltet **Afsend fra land/område** skal du angive **NLD**.
        4. I feltet **Levér til land/område** skal du angive **BEL**.
        5. Vælg **Input** i feltet **Momsretning** for at gøre reglen gældende for modtagelse af flytteordre.
        6. Vælg **RC-VAT** i feltet **Momsgruppe**.

6. Definer anvendeligheden af varemomsgruppen.

    1. Vælg **Administrer kolonner**, og vælg derefter kolonner, der skal bruges til at opbygge anvendelighedstabellen.
    2. Tilføj anvendelighedsregler. Lad ikke feltet **Varemomsgruppe** være tomt.
        
        Tilføj en ny regel for forsendelse og modtagelse af flytteordre.
        1. Vælg **Tilføj** på siden **Anvendelighedsregler**.
        2. Vælg **Lager** i feltet **Forretningsproces** for at gøre reglen gældende for flytteordren.
        3. Vælg **FULL** i feltet **Varemomsgruppe**.
7. Fuldfør og publicer den nye momsfunktionsversion.


## <a name="set-up-finance-for-transfer-order-transactions"></a>Konfigurere Finance til moms- og flytteordretransaktioner

Hvis du vil aktivere og konfigurere moms til flytteordrer, skal du følge disse trin.

1. Gå i Finance til **Arbejdsområder** > **Funktionsstyring**.
2. Find og vælg funktionen **Moms i flytteordre** på listen, og vælg derefter **Aktivér nu** for at aktivere den.

    > [!IMPORTANT]
    > Funktionen **Moms i flytteordre** er fuldstændig afhængig af momsberegningstjenesten. Du kan derfor kun aktivere den, når du har installeret momsberegningstjenesten.

    ![Funktionen Moms i flytteordre.](../media/image7.png)

3. Aktivér momsberegningstjenesten, og vælg forretningsprocessen **Lager**.

    > [!IMPORTANT]
    > Du skal udføre dette trin for hver juridiske enhed i Finance, hvor momsberegningstjenesten og funktionerne for moms i flytteordrer skal være tilgængelige.

    1. Gå til **Moms** > **Konfiguration** > **Momskonfiguration** > **Parametre for momsberegning**.
    2. Vælg **Lager** i feltet **Forretningsproces**.

4. Kontrollér, at modtagermomsmekanisme er konfigureret. Gå til **Finans** \> **Konfiguration** \> **Parametre**, og sørg for, at fanen **Modtagermoms** har indstillingen **Aktivér modtagermoms** angivet til **Ja**.

    ![Aktivere indstilling for modtagermoms.](../media/image9.png)

5. Kontrollér, at de relaterede momskoder, momsgrupper, varemomsgrupper og momsregistreringsnumre er konfigureret i Finance i overensstemmelse med vejledningerne for momsberegningstjenesten.
6. Konfigurere en konto til foreløbig transit. Dette trin er kun påkrævet, når den moms, der anvendes på en flytteordre, ikke gælder for en momsfritagelses eller modtagermomsmekanisme.

    1. Gå til **Moms** > **Opsætning** > **Moms** > **Finanskonteringsgrupper**.
    2. Vælg en finanskonto i feltet **Foreløbig transit**.

       ![Vælge en konto til foreløbig transit.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Konfigurere basislager flytteordretransaktioner

Benyt følgende fremgangsmåde for at konfigurere basislager for at aktivere flytteordretransaktioner.

1. Opret afsendelse fra- og afsendelse til-steder for lagersteder i forskellige lande eller områder, og tilføj den primære adresse for hvert sted.

    1. Gå til **Lagerstedsstyring** > **Konfiguration** > **Lagersted** > **Steder**.
    2. Vælg **Ny** for at oprette det sted, du vil tildele et lagersted senere.
    3. Gentag trin 2 for alle de andre steder, du skal oprette.

    > [!NOTE]
    > Et af de steder, du opretter, skal kaldes **Transit**. I senere trin af denne procedure skal du tildele dette sted til transitlagerstedet, så momsrelaterede lagerbilag kan bogføres i "afsendelses"- og "modtagelses"-transaktioner for flytteordrer. Adressen på transitstedet er irrelevant for momsberegningen. Du kan derfor lade feltet være tomt.

    ![Konfigurere steder.](../media/image11.png)

2. Opret afsend fra-, transit- og afsend til-lagersteder. Alle adresseoplysninger, der vedligeholdes på et lagersted, tilsidesætter stedadressen under momsberegningen.

    1. Gå til **Lokationsstyring** > **Konfiguration** > **Lagersted** > **Lagersteder**.
    2. Vælg **Ny** for at oprette et lagersted og tildele det tilhørende sted.
    3. Gentag trin 2 for at oprette et lagersted for hvert sted efter behov.

       ![Konfigurere lagersteder.](../media/image12.png)

    > [!NOTE]
    > I forbindelse med et afsendelse fra-lagersted skal der vælges et transitlagersted i feltet **Transitlagersted** for flytteordretransaktioner.
    >
    > ![Vælge et transitlagersted.](../media/image13.png)

3. Sørg for, at lagerbogføringen er konfigureret for flytteordretransaktioner.

    1. Gå til **Lagerstyring** > **Konfiguration** > **Bogføring** > **Bogføring**.
    2. Kontrollér, at der er konfigureret en finanskonto til både **Lagerafgang** og **Lagertilgang** under fanen **Lager**.

        ![Konfigurere bogføring af lagertilgang og lagerafgang.](../media/image14.png)

    3. Kontrollér, at der er konfigureret en finanskonto til bogføring af **Intern kreditor**.

        ![Konfigurere bogføring af intern kreditor.](../media/image15.png)

    4. Kontrollér, at der er konfigureret en finanskonto til bogføring af **Intern debitor**.

        ![Konfigurere bogføring af intern debitor.](../media/image16.png)
        
        
  [!INCLUDE[footer-include](../../../includes/footer-banner.md)]
