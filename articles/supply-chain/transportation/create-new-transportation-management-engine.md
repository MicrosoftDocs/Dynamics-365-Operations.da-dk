---
title: Oprette et nyt transportstyringsprogram
description: Dette emne beskriver, hvordan du opretter et nyt transportstyringsprogram i Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be52c6afb66e88b36f3b2cdf5af14e17b3d3005f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678116"
---
# <a name="create-a-new-transportation-management-engine"></a>Oprette et nyt transportstyringsprogram

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du opretter et nyt transportstyringsprogram i Dynamics 365 Supply Chain Management. 

Transportstyringsprogrammer (TMS) definerer den logik, der bruges til at oprette og behandle transportsatser i Transportstyring. Supply Chain Management indeholder flere forskellige programtyper, der beregner forskellige parametre, f.eks. satser, transporttider og antallet af zoner, der vil blive passeret under transport. Denne artikel forklarer, hvordan du bruger Microsoft Visual Studio-udviklingsmiljøet sammen med udviklingsværktøjerne i Supply Chain Management til at oprette og installere et nyt TMS-program, og hvordan programmet konfigureres i Operations. Yderligere oplysninger om programmerne finder du i [Transportstyringsprogrammer](transportation-management-engines.md).

## <a name="create-a-new-tms-engine"></a>Oprette et nyt TMS-program

Dette afsnit indeholder en forklaring på, hvordan du opretter et klassebibliotek med en implementering af TMS-programmet, og hvordan du kan referere til det fra en Supply Chain Management-model.

1. For at installere de nye programmer skal du have en model, der indeholder programmerne. I menuen **Dynamics 365** &gt; **Modelstyring** skal du klikke på **Opret model** for at oprette en ny model. Navngiv modellen **TMSEngines** på første side i guiden **Opret model**. 

   [![Oprettelse af en model.](./media/012.png)](./media/012.png)

2. På næste side skal du vælge **Opret ny pakke**. 

   [![Oprettelse af en ny pakke.](./media/021.png)](./media/021.png)

3. På næste side skal du vælge den **ApplicationSuite**-model, du vil referere til. (Modellen **ApplicationPlatform** er valgt på forhånd.) 

   [![Valg af den model, der skal refereres til.](./media/032.png)](./media/032.png)

4. På næste side skal du klikke på **Udfør** for at bekræfte oprettelsen af en ny model. 

   [![Fuldfør modeloprettelsen.](./media/042.png)](./media/042.png)

5. I en ny løsning skal du oprette et nyt Supply Chain Management-projekt og navngive det **TMSThirdParty**. Angiv projektets model til **TMSEngines** i projektegenskaberne.
6. Føj et nyt C\#-klassebibliotek til løsningen, og navngiv det **ThirdPartyTMSEngines**.
7. I projektet ThirdPartyTMSEngines skal du tilføje referencer til Supply Chain Management-specifikke assemblyer:
   -   Applikations-assemblyer, der gør det muligt at referere til typerne X++. Disse assemblyer kan findes følgende steder. \[Pakkerod\] er stien til den placering, hvor alle implementerede assemblyer placeres, f.eks. C:\\Pakker.

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   Framework-assemblyer, der giver adgang til data, LINQ og hjælpefunktioner. Alle disse assemblyer findes i \[Pakkerod\]\\bin.

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   Kerne-TMS-assemblyen (som indeholder programmer) og TMS-basis-assembly (som indeholder hjælpere, konstanter, klassedefinitioner til dataoverførsel mm.). Disse assemblyer kan findes følgende steder.

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. Omdøb den C\#-klasse, der genereres automatisk i ThirdPartyTMSEngines-projektet, til **SampleRatingEngine**.
9. Implementer programmet. Da vi opretter et satsprogram i dette eksempel, arver vi fra basisklassen for satsprogrammer. Basisklassen implementerer det meste af satsprogrammets grænseflade (**TMSFwkIRateEngine**). Vi skal blot implementere satsmetoden. For at gøre dette eksempel simpelt vil vi få denne metode til en registrere en fastkodet sats på 100. Du kan oprette programmer, der implementerer en hvilken som helst af programgrænsefladerne, f.eks. **TMSFwkIAccessorialEngine**. Alle programgrænseflader er defineret i X++.

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. Opbyg løsningen.
11. Føj en ny reference til projektet TMSThirdParty. Referencen skal pege på projektet ThirdPartyTMSEngines. Når du er færdig, skal løsningen se sådan ud. 

    [![Løsningen, der inkluderer en reference til projektet TMSThirdParty.](./media/052.png)](./media/052.png)

12. Opbyg løsningen. Kontrollér, at det nye bibliotek vises i noden **Referencer** i Application Explorer. 

    [![Det nye bibliotek i noden Referencer i Application Explorer.](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>Implementere TMS-programmet som en pakke

En måde at implementere TMS-programmet fra en tredjepart på er ved hjælp af en installationspakke. Denne metode anbefales i et produktionsmiljø. I et udviklingsmiljø kan du manuelt kopiere assemblyerne som beskrevet i næste afsnit, "Konfigurere et TMS-program i Supply Chain Management". Du kan installere programmet som en pakke ved at gøre følgende.

1. I menuen **Dynamics 365** &gt; **Installer** skal du klikke på <strong>Opret installationspakke</strong>.
2. Vælg TMSEngines-modellen i dialogboksen **Opret installationspakke**, og angiv den sti, hvor du vil gemme pakkefilerne. 

   [![Valg af TMSEngines-modellen.](./media/071.png)](./media/071.png)

3. Du kan nu installere pakken i målmiljøet. Du kan finde et selvstudium under [Installere en installerbar pakke](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md).

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>Konfigurere TMS-programmet i Supply Chain Management

Dette afsnit indeholder en forklaring på, hvordan du konfigurerer Supply Chain Management til at bruge et TMS-program, og viser, hvordan det nye program, som vi har oprettet, bruges til indhentning og visning af forsendelsessatser. I dette afsnits eksempel bruges demodatafirmaet USMF.

1. Opret et nyt program som beskrevet i afsnittet "Oprette et nyt TMS-program".
2. Opbyg din løsning.
3. Kopiér den assembly, der oprettes, til den binære placering af Supply Chain Management-serveren, \[AOSWebRoot\]bin. **Bemærk:** Dette trin er kun relevant i et udviklingsmiljø. I et produktionsmiljø skal du installere via en installationspakke. Yderligere oplysninger finder du i forrige afsnit, "Implementere TMS-programmet som en pakke."
4. I Supply Chain Management skal du oprette et nyt satsprogram på siden **Satsprogrammer**. Programmet skal pege på den programassembly, der produceres ved at opbygge programklassebiblioteket og den programklasse, du har implementeret. 

   [![Oprettelse af et nyt satsprogram på siden Satsprogrammer.](./media/081.png)](./media/081.png)

5. Opret en fragtmand, der bruger eksempelsatsprogrammet. Da vores program ikke bruger data, behøver du ikke tildele en satsmaster. 

   [![Oprettelse af en ny fragtmand.](./media/092.png)](./media/092.png)

6. Klik på **Satsbutik** på siden **Satsrutepanel**. En sats på 100,00 fra SampleCarrier vises som på følgende skærmbillede. I dette eksempel bruger vi indhentning og visning af forsendelsessatser for en rute fra lagersted 24 til kunden US-004. Men da satsen er fastkodet, vil du altid se en sats på 100,00.

   [![Satsrutepanel.](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>Tip og trick

- Hvis du bruger udviklingsværktøjer til Supply Chain Management, er det en god ide at føje et nyt projekt til din løsning. Hvis du angiver dette projekt som startprojektet og starter en fejlfindingssession, kan du fejlfinde både X++- og C\#-kode i samme fejlfindingssession.
- Hver gang du ændrer og kompilerer dit ThirdPartyTMSEngines-projekt igen, skal du manuelt kopiere den assembly, der er resultatet, til den binære placering eller installere via en installationspakke. Ellers kan du køre ved hjælp af en gammel assembly.
- Når du har udført TMS-specifikke operationer i Supply Chain Management, vil arbejderprocessen for IIS (Internet Information Services) måske låse ThirdPartyTMSEngines-assemblyen, så assemblyen ikke kan opdateres. I dette tilfælde skal du genstarte w3svc-processen.

### <a name="whitepaper"></a>Hvidbog

Yderligere oplysninger finder du ved at downloade følgende hvidbog (skrevet som support til AX2012, men gælder stadig for Dynamics 365 Supply Chain Management)

- [Implementering og installation af programmer til transportstyring](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]