---
title: Scenarieopsætning for IoT-viden
description: Dette emne forklarer, hvordan du kan konfigurere scenarier for IoT-viden i Microsoft Dynamics 365 Supply Chain Management.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a45ed57f1fb5e4d508c30b2f3a83dafacfb7dd870701a8f519bbc1e807ed982
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736787"
---
# <a name="scenario-setup-for-iot-intelligence"></a>Scenarieopsætning for IoT-viden

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du kan konfigurere scenarier for IoT-viden i Microsoft Dynamics 365 Supply Chain Management. Inden du kan konfigurere scenarier, skal du [konfigurere Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).

I dette emne skal du konfigurere scenariet **Nedetid for udstyr** for at generere en besked i Supply Chain Management, når en maskine går ned. I emnet vises også, hvordan du kan konfigurere scenariet **Produktkvalitet**, så der genereres en besked, hvis en attribut for en vare ligger uden for et angivet interval, og hvordan du kan konfigurere scenariet **Produktionsforsinkelser**, så der genereres en besked, hvis produktionshastigheden falder under en tærskelværdi.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Konfigurere scenariet Nedetid for udstyr i Supply Chain Management

Scenariet **Nedetiden for udstyr** tilknytter et **PartOut**-signal til en maskines beskedgrænse. Maskinen overvåges kun, når den er valgt til scenariet og er angivet til **Kører** i Supply Chain Management. Hvis tiden efter, at et **PartOut** sidst blev modtaget fra maskinen, overstiger tærskelværdien for beskeden, udløses beskeden **Maskine nede**. Hvis maskinen stadig kører, når det næste **PartOut**-signal modtages, udløses der en besked om **Maskine oppe**. Hvis en maskine er nede i 30 minutter, udløses en ny besked **Maskine nede**.

Scenariet **Nedetid for udstyr** har følgende afhængigheder:

+ En besked kan kun udløses, hvis en produktionsordrer kører på en tilknyttet maskine.
+ Et signal, der repræsenterer en tilknyttet maskines **PartOut**-signal, skal sendes til IoT Hub sammen med et entydigt egenskabsnavn.
+ En UNIX-egenskab for **tidsstempel**, hvor værdien angives i millisekunder (ms), skal være til stede i Azure IoT Hub-meddelelsen.

Hvis du vil konfigurere scenariet, skal du følge disse trin.

1. Log på Supply Chain Management.
2. Aktivér IoT-viden-funktionsflaget. Få flere oplysninger i [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Konfigurer de metriske værdier. Få flere oplysninger i [Sådan konfigurer du metriske værdier](iot-metrics-setup.md#configure-metrics).
4. Gå til **Produktionsstyring \> Konfiguration \> IoT-viden \> Scenariestyring**.
6. I feltet **Udstyrs nedetid** skal du vælge **Konfigurer** for at åbne konfigurationsguiden.

   Guiden starter med siden **Skemadefinition for udstyrssensor**. På denne side er dit mål at konfigurere skemaet i Supply Chain Management, så det svarer til formatet JavaScript Object Notation (JSON) i IoT Hub-meddelelser. Der kan defineres flere meddelelsesskemaer. Få flere oplysninger i [Meddelelsesskemaformater for IoT Hub](iot-schema-format.md). I dette eksempel indeholder meddelelsens nyttedata en batch af meddelelser med følgende format.

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

7. Føj en række til tabellen, og angiv følgende værdier:

    1. Angiv feltet **Skemanavn** til **Id**.
    2. Angiv feltet **Skemasti** til **/nyttedata\[\*\]/id**.
    3. Angiv feltet **Beskrivelse** til **Meddelelses-id**.

8. Føj endnu en række til tabellen, og angiv følgende værdier:

    1. Angiv feltet **Skemanavn** til **Tidsstempel**.
    2. Angiv feltet **Skemasti** til **/nyttedata\[\*\]/tidsstempel**.
    3. Angiv feltet **Beskrivelse** til **Meddelelsestidsstempel**.

9. Føj endnu en række til tabellen, og angiv følgende værdier:

    1. Angiv feltet **Skemanavn** til **Værdi**.
    2. Angiv feltet **Skemasti** til **/nyttedata\[\*\]/værdi**.
    3. Angiv feltet **Beskrivelse** til **Meddelelsesværdi**.

    > [!NOTE]
    > Du behøver ikke at definere alle egenskaberne i meddelelsen. Definer kun de egenskaber, du skal bruge. I de foregående trin har du ikke oprettet en række til **Rodtidsstempel**. Stien til et **Rodtidsstempel** skulle være **/tidsstempel**.

10. Vælg **Næste** for at gå til siden **Skematilknytning for udstyrssensor**.
11. I rækken for **Udstyrsressource-id** skal du angive feltet **Skemanavn** til **Id**.
12. I rækken for **UTC-tid** skal du angive feltet **Skemanavn** til **Tidsstempel**.
13. I rækken for **Delproduceret signal** skal du angive feltet **Skemanavn** til **Værdi**.
14. Vælg **Næste** for at gå til siden **Konfiguration af udstyrsressource-id**.
15. Følg disse trin for at knytte meddelelsesværdierne i IoT Hub til Supply Chain Management-ressourcerne:

    1. Tilføj en ny række i tabellen **Signaldataværdier**. I feltet **Værdi** skal du angive **IoTInt.Machine1225.PartOut**. Værdien kommer fra JSON-egenskaben **id** i IoT Hub-meddelelsen.
    2. Vælg **Gem**.
    3. Vælg **Ny** i tabellen **Forretningsposttilknytning**. Standardværdien for feltet **Forretningsposttype** udfyldes automatisk, og du behøver ikke at ændre den.
    4. I feltet **Forretningspost** skal du vælge den Supple Chain Management-maskinressource, som denne signaværdi er blevet sendt fra.
    5. Vælg **Gem**.
    6. Gentag disse trin for at tilføje en ny forretningsposttilknytning for **Machine1226**. Du kan knytte flere signaldataværdier til en enkelt post i Supply Chain Management.

16. Brug kolonnen **Valgt** til at vælge, hvilke maskiner du vil behandle. Du behøver ikke at definere alle signalværdier, og du behøver ikke at vælge alle maskiner.
17. Vælg **Næste** for at gå til siden **Konfiguration af delproduceret signal**.
18. I tabellen **Signaldataværdier** skal du tilføje en række og indstille feltet **Værdi** til **Sand**. Værdien kommer fra JSON-egenskaben **værdi** i IoT Hub-meddelelsen. Du kan tilføje lige så mange værdier, du har brug for til dit scenarie.
19. Vælg **Gem**.
20. Vælg **Næste** for at gå til siden **Tærskel for nedetid for udstyr**. De angivne maskiner her er dem, der tidligere er knyttet til signalværdier. På denne side skal du definere en tærskel for at afgøre, om en maskine er nede. Hvis du f.eks. angiver tærsklen til **10**, genererer Supply Chain Management en besked, hvis der ikke er modtaget et **PartOut**-signal fra en maskine i 10 minutter.
21. Vælg **Næste** for at gå til siden **Aktivér scenarie**. Angiv indstillingen for at aktivere scenariet.
22. Vælg **Udfør**.

Konfigurationen af scenariet er nu fuldført. IoT-viden vil automatisk starte behandlingen af IoT Hub-meddelelserne.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Konfigurere scenariet Produktkvalitet i Supply Chain Management

Scenariet **Produktkvalitet** genererer en besked, hvis en attribut for en vare ligger uden for et angivet interval. En sensor kan f.eks. sende vægten af hver enkelt vare til IoT Hub. I Supply Chain Management genereres der en besked, hvis varen er for tung eller for let.

Scenariet **Produktkvalitet** har følgende afhængigheder:

+ En besked kan kun udløses, hvis en produktionsordre kører på en tilknyttet maskine og fremstiller et produkt med en tilknyttet batchattribut.
+ Et signal, der repræsenterer batchattributten, skal sendes til IoT Hub sammen med et entydigt egenskabsnavn.
+ En UNIX-egenskab for **tidsstempel**, hvor værdien angives i millisekunder (ms), skal være til stede i Azure IoT Hub-meddelelsen.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Konfigurere scenariet Produktionsforsinkelser i Supply Chain Management

Scenariet **Produktionsforsinkelser** genererer en besked, hvis produktions gennemløb falder under en tærskelværdi. I dette scenarie sendes et **PartOut**-signal til IoT Hub for hver fremstillet vare. I Supply Chain Management beregnes ordreforsinkelsen på basis af den mængde tid, som produktionsordren er planlagt til at køre, det antal varer, der skal produceres, den tid, jobbet har kørt, og antallet af **PartOut**-signaler, der er modtaget. Der genereres en forsinkelsesbesked, hvis antallet af **PartOut**-signaler for jobbet falder under tærskelværdien.

Scenariet **Produktionsforsinkelser** har følgende afhængigheder:

+ En besked kan kun udløses, hvis en produktionsordrer kører på en tilknyttet maskine.
+ Et signal, der repræsenterer en tilknyttet maskines **PartOut**-signal, skal sendes til Azure IoT Hub sammen med et entydigt egenskabsnavn.
+ En UNIX-egenskab for **tidsstempel**, hvor værdien angives i millisekunder (ms), skal være til stede i Azure IoT Hub-meddelelsen.

## <a name="disable-a-scenario"></a>Deaktivere et scenarie

Følg disse trin for at deaktivere et scenarie.

1. I Supply Chain Management skal du gå til **Produktionsstyring \> Konfiguration \> IoT-viden \> Scenariestyring**.
2. I feltet til scenariet skal du vælge **Konfigurer**.
3. Vælg **Næste** for at gå til den sidste side i guiden.
4. Angiv indstillingen for at deaktivere scenariet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]