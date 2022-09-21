---
title: Scenariet for aktiv nedetid
description: I denne artikel beskrives scenariet for nedetid for aktiver, hvilket giver dig mulighed for at bruge data til at overvåge tilgængeligheden af aktiverne.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetObjectProductionStop
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 944818557deebed06c02c00fd69de6e8f08bda83
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428321"
---
# <a name="the-asset-downtime-scenario"></a>Scenariet for aktiv nedetid

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

I scenariet for nedetid for aktiver genereres en nedetidspost for vedligeholdelse, hvis der ikke er modtaget et signal fra en maskine inden for en defineret tidsgrænseværdi, siden det sidste signal blev modtaget. Scenariet kræver, at du passer maskinen med en sensor, der periodisk sender et signal til Azure IoT Hub, mens maskinen kører, men ikke sender et signal, når maskinen ikke kører.

## <a name="set-up-the-asset-downtime-scenario"></a>Konfigurere scenariet for aktiv nedetid

Hvis du vil konfigurere *aktiv nedetid*-scenariet i Supply Chain Management, skal følge disse trin.

1. Gå til **Aktivstyring \> Opsætning \> Sensordataintelligens \> Svenarier** for at åbne siden **Scenarier**.
2. I scenariefeltet **Nedetid for aktiv** skal du vælge **Konfigurer** for at åbne installationsguiden for dette scenario.
3. Vælg **Ny** på siden **Sensorer** for at føje en sensor til gitteret. Angiv følgende felter:

    - **Sensor-id** – angiv id for den bruger, du bruger. (Hvis du bruger Raspberry PI Azure IoT Online Simulator og har konfigureret den som beskrevet i [Angiv simuleret sensor til test](sdi-set-up-simulated-sensor.md), skal du angive *AssetDownTime*.)
    - **Sensor-beskrivelse** – Indtast en detaljeret beskrivelse af sensoren.

4. Gentag forrige trin for hvert ekstra sensor, du skal tilføje nu. Du kan altid vende tilbage og tilføje flere oplysninger.
5. Vælg **Næste**.
6. På siden **Tilknytning af forretningspost** i afsnittet **Sensorer** skal du vælge posten for en af de sensorer, du lige har tilføjet.
7. Vælg **Ny** i sektionen **Tilknytning af forretningspost** for at føje en række til gitteret.
8. I den nye række skal du indstille feltet **Forretningspost** til den ressource, du bruger den valgte ressource til at overvåge. (Hvis du bruger demodata, skal du vælge *AK-101, Air Knife for linje 1*.)
9. Vælg **Næste**.
10. På siden med **tærskel for aktiv nedetid** skal du angive, hvor lang tid efter det sidste signal, systemet skal vente, før der sendes en besked om nedetid for aktivet. Der er to måder at definere tærsklen på:

    - **Standardtærskel (minutter)** – Angiv dette felt for at definere standardtærsklen. Denne værdi gælder for alle ressourcer, hvor feltet **Beskedtærskel (minutter)** er angivet til to minutter eller mindre. Minimumværdien er *2* (minutter).
    - **Tærskelværdi for at bestemme, at maskinen ikke svarer (minutter)** – For hver ressource i gitteret, hvor der ikke skal bruges standardgrænseværdi, skal du angive en ændringsværdi i dette felt. Ressourcer, der er angivet til at bruge en grænse på to minutter eller mindre, bruger i stedet indstillingen **Standardgrænseværdi (minutter)**.
11. Vælg **Næste**.
12. På siden **Aktivér sensorer** i gitteret skal du vælge den sensor, du vil konfigurere, og derefter vælge **Aktivér**. For hvert aktiveret område i gitteret vises en markering i kolonnen **Aktiv**.
13. Vælg **Udfør**.

## <a name="work-with-the-asset-downtime-scenario"></a>Arbejd med scenariet for aktiv nedetid

Hvis der ikke modtages et signal fra et aktiv inden for den tærskelværdi, der er defineret i scenariokonfigurationen, opretter systemet en post for vedligeholdelses-nedetid for det pågældende aktiv. Ledere bør jævnligt gennemgå nedetidsposterne (f.eks. en gang på hvert skiftehold) og anvende relevante årsagskoder og sluttider for hver enkelt nedetidsregistrering. Benyt følgende fremgangsmåde for at få vist poster for nedetid for vedligeholdelse af et aktiv:

1. Gå til **Styring af aktiver > Aktiver > Alle aktiver**.
2. Find og vælg det aktiv, du vil inspicere. (Hvis du bruger demodata, skal du vælge *AK-101*.)
3. Åbn fanen **Aktiv** i handlingsruden, og vælg **nedetid for vedligeholdelse** fra gruppen **Arbejdsordre** for at åbne siden til poster for vedligeholdelses-nedetid for det valgte aktiv.
