---
title: Scenarieopsætning for IoT-viden
description: Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere et scenarie i Supply Chain Management for IoT-viden.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b87a9b73f49e73fe13b98fb11da939c9b30e0f6e
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386498"
---
# <a name="scenario-setup-for-iot-intelligence"></a>Scenarieopsætning for IoT-viden

[!include [banner](../../includes/banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere et scenarie i Supply Chain Management for IoT-viden. Før du kan konfigurere scenarierne, skal du [konfigurere LCS](iot-lcs-setup.md).

I dette emne skal du konfigurere scenariet **Nedetid for udstyr** for at generere en besked i Supply Chain Management, når en maskine går ned.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Konfigurere scenariet **Nedetid for udstyr** i Supply Chain Management

Scenariet **Nedetiden for udstyr** tilknytter et del ude-signal til en maskines beskedgrænse. Maskinen overvåges kun, når maskinen er valgt til scenariet og er angivet til at køre i Supply Chain Management. Hvis tiden efter, at maskinens sidste modtagne del ude-signal er større end tærskelværdien for beskeden, udløses beskeden **Maskine nede**. Hvis maskinen stadig kører, når det næste **Del ud**-signal modtages, udløses der en besked **Maskine oppe**. Hvis en maskine er nede i 30 minutter, udløses en ny besked **Maskine nede**.

Scenariet for **nedetid for udstyr** har følgende afhængigheder:

+ En produktionsordre skal køre på en tilknyttet maskine, før der kan udløses en påmindelse.
+ Et signal, der repræsenterer en tilknyttet maskines del ud-signal, skal sendes til IoT Hub med et entydigt egenskabsnavn.
+ Der skal være en tidsstempelegenskab i millisekunder for UNIX i IoT-meddelelsen.

Hvis du vil konfigurere scenariet, skal du følge disse trin:

1. Log på Supply Chain Management.
2. Aktivér IoT-viden-funktionsflaget. Få flere oplysninger i [Oversigt over funktionsstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Konfigurer de metriske værdier. Få flere oplysninger i [Sådan konfigurer du metriske værdier](iot-metrics-setup.md#configure-metrics).
4. Gå til **Produktionsstyring**.
5. Gå til **Konfiguration \> IoT-viden \> Scenariestyring**.
6. Klik på **Opsætning** i feltet **Nedetid for udstyr**. Konfigurationsguiden starter med siden **Skemadefinition for udstyrssensor**. Målet er at angive, at skemaet i Supply Chain Management skal svare til JSON-formatet i IoT-meddelelserne. Der kan defineres flere meddelelsesskemaer. Få flere oplysninger i [Formater for meddelelsesskemaer for IoT Hub](iot-schema-format.md). I dette eksempel indeholder meddelelsesdataene en batch af meddelelser med dette format:

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. Føj en række til tabellen.

    1. Angiv **Skemanavn** til **Id**.
    2. Angiv **Skemasti** til **/payload[\*]/id**.
    3. Angiv **Beskrivelse** til **Meddelelses-id**.

8. Føj en række til tabellen.

    1. Angiv **Skemanavn** til **Tidsstempel**.
    2. Angiv **Skemasti** til **/payload[\*]/tidsstempel**.
    3. Angiv **Beskrivelse** til **Meddelelsestidsstempel**.

9. Føj en række til tabellen.

    1. Angiv **Skemanavn** til **Værdi**.
    2. Angiv **Skemasti** til **/payload[\*]/værdi**.
    3. Angiv **Beskrivelse** til **Meddelelsesværdi**.

    Du behøver ikke at definere alle egenskaberne i meddelelsen, kun dem, du skal bruge. I dette eksempel oprettede du ikke en række for **Rodtidsstempel**. Stien for et **Rodtidsstempel** ville være **/Tidsstempel**.
  
10. Klik på **Næste** for at gå til siden **Skematilknytning for udstyrssensor**.
11. I rækken for **Udstyrsressource-id** skal du angive **Skemanavn** til **Id**. De gyldige værdier vises i en rulleliste.
12. I rækken for **UTC-tid** skal du angive **Skemanavn** til **Tidsstempel**. De gyldige værdier vises i en rulleliste.
13. I rækken for **Delproduceret signal** skal du angive **Skemanavn** til **Værdi**. De gyldige værdier vises i en rulleliste.
14. Klik på **Næste** for siden **Konfiguration af udstyrsressource-id**.
15. I dette trin knytter du IoT-meddelelsesværdierne til de Supply Chain Management-ressourcerne.

    1. I tabellen **Signaldataværdier** skal du tilføje en ny række og angive **IoTInt.Machine1225.PartOut** i kolonnen **Værdi**. Værdien **IoTInt. Machine1225. PartOut** kommer fra egenskaben JSON-**id** i IOT hub-meddelelsen.
    2. Klik på **Gem**.
    3. Klik på **Ny** i tabellen **Forretningsposttilknytning**. Standardværdien for **Forretningsposttypen** udfyldes automatisk, og du behøver ikke at ændre den.
    4. I kolonnen **Forretningspost** skal du vælge den Supple Chain Management-maskinressource, denne signaværdi er blevet sendt fra.
    5. Klik på **Gem**.
    6. Gentag disse trin, og tilføj en ny forretningsposttilknytning for **Maskin1226**. Du kan knytte flere signaldataværdier til en enkelt post i Supply Chain Management.

16. Brug kolonnen **Valgt** til at vælge, hvilke maskiner du vil behandle. Du behøver ikke at definere alle signalværdier, og du behøver ikke at vælge alle maskiner.
17. Klik på **Næste** for at gå til siden **Konfiguration af delproduceret signal**.
18. I tabellen **Signaldataværdier** skal du tilføje en række og indstille **Værdi** til **Sand**. Værdien **Sand** kommer fra egenskaben JSON-**værdi** i IoT Hub-meddelelsen. Du kan tilføje lige så mange værdier, du har brug for til dit scenarie.
19. Klik på **Gem**.
20. Klik på **Næste** for at gå til siden **Tærskel for nedetid for udstyr**. De angivne maskiner er de maskiner, der tidligere er knyttet til signalværdier. I dette trin skal du definere en tærskel for at afgøre, om en maskine er nede. Hvis du f.eks. angiver tærsklen til 10, genererer Supply Chain Management en besked, hvis der ikke er en del ud-meddelelse fra en maskine i 10 minutter.
21. Klik på **Næste** for at gå til siden **Aktivér scenarie**. Slå skyderen til og fra for at aktivere scenariet.
22. Klik på **Udfør**.

Konfigurationen af scenariet er fuldført. IoT-viden vil automatisk starte behandlingen af IoT hub-meddelelserne.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Konfigurere scenariet **Produktkvalitet** i Supply Chain Management

Scenariet **Produktkvalitet** genererer en besked, hvis en attribut for en vare ligger uden for et angivet interval. En sensor kan f.eks. sende vægten af hver enkelt vare til IoT Hub. I Supply Chain Management genereres der en besked, hvis varen er for tung eller for let.

Scenariet har følgende afhængigheder:

+ En produktionsordre skal køre på en tilknyttet maskine og fremstille et produkt med en tilknyttet batchattribut, for at der kan udløses en påmindelse.
+ Et signal, der repræsenterer batchattributten skal sendes til IoT Hub med et entydigt egenskabsnavn.
+ Der skal være en tidsstempelegenskab i millisekunder for UNIX i IoT Hub-meddelelsen.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Konfigurere scenariet **Produktionsforsinkelser** i Supply Chain Management

Scenariet **Produktionsforsinkelser** genererer en besked, hvis produktions gennemløb falder under en tærskelværdi. I dette scenarie sendes et **Del ud**-signal til IoT Hub for hver fremstillet vare. I Supply Chain Management beregnes ordreforsinkelsen på basis af, hvor længe produktionsordren er planlagt til at køre, hvor mange varer der skal produceres, hvor længe jobbet har kørt, og hvor mange **Del ud**-signaler, der modtages. Der ville blive genereret en forsinkelsesbesked, hvis nummeret på **Del ud**-signalerne for jobbet falder under tærskelværdien for den forventede værdi.

Scenariet har følgende afhængigheder:

+ En produktionsordre skal køre på en tilknyttet maskine, før der kan udløses en påmindelse.
+ Et signal, der repræsenterer en tilknyttet maskines del ud-signal, skal sendes til IoT Hub med et entydigt egenskabsnavn.
+ Der skal være en tidsstempelegenskab i millisekunder for UNIX i IoT Hub-meddelelsen.

## <a name="how-to-disable-a-scenario"></a>Sådan deaktiveres et scenarie

Følg disse trin for at deaktivere et scenarie:

1. I Supply Chain Management skal du gå til **Produktionsstyring \> Konfiguration \> IoT-viden \> Scenariestyring**.
2. Klik på **Opsætning** i scenariet.
3. Klik på **Næste** for at åbne den sidste fane i guiden.
4. Slå skyderen til og fra for at deaktivere scenariet.
