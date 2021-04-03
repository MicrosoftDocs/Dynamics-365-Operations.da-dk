---
title: A-skatopgørelse for Egypten
description: Dette emne forklarer, hvordan du konfigurerer og genererer A-skatopgørelse til Egypten.
author: sndray
manager: AnnBe
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cec903c56439957bcafb77c3da774a903d4433a1
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574318"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a>A-skatopgørelse for Egypten (EG-00005)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a>Overblik
Dette emne forklarer, hvordan du opretter og genererer A-skatteopgørelsen og formularer til A-skatteopgørelsen 41 og 11 til juridiske enheder i Egypten 

Alle egyptiske enheder skal forberede formular 41, der opsummerer al skat, der tilbageholdes fra lokale leverandører og serviceudbydere. Ud over formular 41 skal formular 11 genereres med detaljer for alle tilbageholdte skatter fra udenlandske leverandører. 

Rapporten **A-skatteopgørelse** indeholder følgende rapporter i Dynamics 365 Finance:

- Rapportformular-nr. 41
- Rapportformular-nr. 11
    
    
## <a name="prerequisites"></a>Forudsætninger
Den primære adresse for den juridiske enhed være i Egypten.
I arbejdsområdet **Funktionsstyring** skal du aktivere følgende funktion:

   - **Globalt A-skat**

Du kan finde flere oplysninger om aktivering af nye funktioner under [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

1. Gå til **Moms** > **Opsætning** > **Parametre** > **Finansparametre** og på fanen **A-skat** skal du angive **Aktiver global A-skat** til **Ja**.
2. I arbejdsområdet for **elektronisk rapportering** skal du importere følgende format for elektronisk rapportering fra lageret:

    - WHT-opgørelse Excel (EG)

    > [!NOTE]
    > Formatet ovenfor er baseret på **Momsopgørelsesmodel** og bruger **Tilknytning til momsopgørelsesmodel**. Denne ekstra konfiguration importeres automatisk.

Du kan finde flere oplysninger om, hvordan du importerer konfigurationer af elektronisk rapportering, i [Hent konfigurationer til elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Hent konfigurationer for elektronisk rapportering

Implementeringen af WHT-formularen til indberetning for Egypten er baseret på konfigurationen af Elektronisk rapportering (ER). Du kan finde flere oplysninger om egenskaberne og koncepterne ved konfigurerbar rapportering under [Elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

I forbindelse med produktions- og brugermodtagelsestestmiljøer (UAT) skal du følge vejledningen i emnet [Hent konfigurationer til elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Hvis du vil generere A-opgørelserne i en egyptisk enhed medstyring, skal du overføre følgende konfigurationer:

- Momsopgørelsesmodel.version.82.xml eller senere version
- Momsopgørelsesmodel mapping.version.82.133.xml eller senere version
- Momsopgørelse Excel (EG).version.82.21 eller en senere version

Når du har hentet ER-konfigurationerne fra Lifecycle Services (LCS) eller det globale lager, skal du gennemføre følgende trin.

1. Gå til arbejdsområdet **Elektronisk rapportering** og vælg feltet **Rapporteringskonfigurationer**.
1. Gå til siden **Konfigurationer**, og vælg **Kurs > Indlæs fra XML-fil** i handlingsruden.
1. Overfør alle filerne i den rækkefølge, som de er angivet i de forrige punkttegn. Når alle konfigurationerne er overført, skal konfigurationstræet være til stede i Finans.

## <a name="set-up-application-specific-parameters"></a>Oprette ansøgningsspecifikke parametre

Den programspecifikke indstilling giver brugerne mulighed for at opstille kriterierne for, hvordan momstransaktioner skal klassificeres og beregnes på hver linje i en genereret rapport, afhængigt af konfigurationen af **varegruppe for A-skat** eller andre kriterier, der er defineret i definitionen af opslag.

A-opgørelsesform 41 indeholder en specifik kolonne, hvor A-skatteposteringen skal klassificeres i overensstemmelse med skattemyndighedsklassifikationen med navnet **Rabatkodetype**. I stedet for at medtage disse nye klassifikationer som nye postdata, når posteringerne bogføres, vil klassifikationerne blive fastlagt på basis af forskellige opslag, der er indført i **Konfigurationer** > **Konfigurer programspecifikke parametre** > **Konfiguration** for at opfylde kravene i opgørelsesrapporter for Egypten. 

Følgende konfiguration bruges til klassificering af posteringerne i A-opgørelsesform 41-rapporten:

- **DiscountTaxTypeLookup** -> Kolonnenr. 18 

Gennemfør følgende trin for at konfigurere de forskellige opslag, der bruges til at oprette momsopgørelser og relaterede bograpporter. 

1. I arbejdsområdet for **elektronisk rapportering** skal du vælge **Konfigurationer** > **Opsætning** for at oprette regler, der identificerer hvordan transaktioner klassificeres i momsrapporteringsrapporten. 
2. Vælg den aktuelle version, og vælg opslagsnavnet på oversigtspanelet **Opslag**. F.eks. **DiscountTaxTypeLookup**. Dette opslag identificerer listen over rabattyper, der kræves af skattemyndighederne.
3. I oversigtspanelet **Betingelser** skal du vælge **Tilføj** og på den nye linje i kolonnen **Opslagsresultat** vælge den relaterede linje, der repræsenterer klassifikationen i **Kolonne 18**.
4. Vælg i kolonnen **A-skatgruppe** den kode, der bruges til at identificere klassifikationen. F.eks. **Tilladt rabat**.  
5. Gentag trin 3 og 4 for alle tilgængelige opslag.
6. Vælg **Tilføj** igen for at medtage den sidste postlinje, og vælg **Ikke relevant** i kolonnen **Opslagsresultat**. 
7. Vælg **Ikke tom** i resten af kolonnerne. 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a>Konfigurer økonomiparametre

Hvis du vil generere momsindberetningsformularrapporten i Microsoft Excel-format, skal du definere et ER-format på siden **Økonomiparametre**.

1. Gå til **Moms** > **Opsætning** > **Finansparametre**.
2. Under fanen **A-skat** skal du i feltet **Formattilknytning af WHT-opgørelse** vælge **WHT-opgørelse i Excel (EG)**. Hvis du lader feltet stå tomt, genereres standardrapporten for moms i SSRS-format.


![Rapport formular](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a>Generere A-opgørelsesformularer
Processen til forberedelse og afsendelse af en form for A-opgørelse for en bestemt periode er baseret på de posteringer for A-skat, der er bogført under afregnings- og postering af betalingsskatjobbet. Du kan finde flere oplysninger om global A-skat i [Global A-skat](../general-ledger/global-withholding-tax-overview.md).

Fuldfør følgende trin, hvis du vil generere den elektroniske momsopgørelse:

1. Gå til **Moms** > **Opgørelse** > **A-skat** > **Betaling af A-skat*.
2. Vælg afregningsperioden, og vælg fra-datoen til rapporten. 
3. Angiv transaktionsdatoen, og vælg derefter **OK**.
4. I den dialogboks, der åbnes, skal du vælge en eller flere formtyper **Formularnr. 41**, **Formular nr. 11** eller **Ingen**. Hvis du vælger **Ingen**, genereres standardrapporten. 
5. Vælg sprog. Alle rapporter oversættes i **en-us** og **ar-eg**.
6. Angiv afdelingen og navnet på den bank, hvor skattebetalingen skal betales.
7. Vælg forretningstype, og angiv derefter check- og dokumentnumrene. 
8. Angiv enhedstypen. 
9. Angiv navnet på den person, der er registreret for at tildele formen, og vælg **OK** for at bekræfte generering af rapporter. 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
