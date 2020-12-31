---
title: Udvidet formatopslag for elektronisk rapportering (ER)
description: Dette emne beskriver, hvordan en ER-formatreference kan konfigureres i ER-formatopslaget, når det krævede format er gemt i den globale lagermappe.
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f7c6cb99a6c5cc6fb92ce52041296af2d0c6722e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679480"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>Tillad brugere at konfigurerer en ER-formatreference, der forespørger om et format fra den globale lagermappe

[!include [banner](../includes/banner.md)]

Du kan bruge strukturen [elektronisk rapportering](general-electronic-reporting.md) (ER) til at konfigurere [formater](general-electronic-reporting.md#FormatComponentOutbound) for udgående dokumenter i overensstemmelse med de lovgivningsmæssige krav i forskellige lande/områder. Du kan også bruge ER-strukturen til at konfigurere [formater](general-electronic-reporting.md#FormatComponentInbound) til parsing af indgående dokumenter og bruge oplysningerne fra disse dokumenter til at tilføje eller opdatere programdata. Hvert af disse formater kan bruges i din Dynamics 365 Finance-forekomst til at håndtere indgående eller udgående forretningsdokumenter som del af en bestemt forretningsproces.

Normalt skal du angive, hvilket ER-format der skal bruges i en bestemt forretningsproces. Hvis du vil gøre det, skal du vælge ER-formatet i et opslagsfelt, der er konfigureret som en del af forretningsprocesspecifikke parametre. Disse opslagsfelter implementeres normalt ved hjælp af den relevante API i ER-strukturen. Du kan finde flere oplysninger i [API til ER-struktur – kode til visning af et formattilknytningopslag](er-apis-app73.md#code-to-display-a-format-mapping-lookup).

Når du f.eks. konfigurerer [udenrigshandelsparametre](https://docs.microsoft.com/dynamics365/finance/localizations/emea-intrastat#set-up-foreign-trade-parameters), skal du konfigurere referencerne til de enkelte ER-formater, der bruges til at generere Intrastat-opgørelsen og kontrolrapporten til Intrastat-opgørelsen. Skærmbillederne nedenfor viser, hvordan opslagsfeltet til ER-formater ser ud på siden **Udenrigshandelsparametre**.

Hvis den aktuelle Finance-forekomst ikke indeholder nogen Intrastat-forretningsprocesrelaterede ER-formater, er dette opslagsfelt tomt.

[![Siden Udenrigshandelsparametre](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

Hvis den aktuelle Finance-forekomst indeholder Intrastat-forretningsprocesrelaterede ER-formater, tilbydes ER-formater i dette opslagsfelt.

[![Siden Udenrigshandelsparametre](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

Dette opslag indeholder kun de ER-formater, der allerede er importeret til den aktuelle Finance-forekomst. Hvis du vil [importere](./tasks/er-import-configuration-lifecycle-services.md) ER-løsninger til den aktuelle Finance-forekomst, skal du have rettigheder til at køre den relevante funktion i den ER-struktur, der understøtter [livscyklussen](general-electronic-reporting-manage-configuration-lifecycle.md) for ER-løsninger, der indeholder ER-formater.

Fra og med Finance version 10.0.9 (april 2020 release) er brugergrænsefladen i det ER-formatopslag, der implementeres ved hjælp af API til ER-struktur, udvidet. Du kan stadig vælge de eksisterende ER-formater, som findes i oversigtspanelet **Vælg formatkonfiguration**. Derudover tilbyder det udvidede opslag den nye indstilling til søgning i den globale lagermappe (GR) for at finde bestemte ER-formater. Alle ER-formaterne for GR vises i oversigtspanelet **Indlæs fra den globale lagermappe**.

[![Siden Udenrigshandelsparametre](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

Med sin lighed med oversigtspanelet **Vælg formatkonfiguration** viser oversigtspanelet **Indlæs fra den globale lagermappe** kun de ER-formater, der gælder for den forretningsproces, som et ER-format er valgt for i dette opslagsfelt. I dette eksempel er det genereringen af Intrastat-opgørelsen. Er-formatet gælder for det firma, som brugeren aktuelt er logget på, afhængigt af firmaets landekontekst.

Når du vælger et ER-format i oversigtspanelet **Indlæs fra den globale lagermappe**, importeres det valgte ER-format [konfiguration](general-electronic-reporting.md#Configuration) fra GR til den aktuelle forekomst af Finance.

[![Siden Udenrigshandelsparametre](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

Hvis importen fuldføres korrekt, gemmes referencen til det importerede ER-format i dette opslagsfelt. Når du åbner GR første gang, skal du følge linket for at tilmelde dig den [Regulatory Configuration Service](https://aka.ms/rcs) (RCS), der bruges til at administrere adgangen til GR-lageret.

[![Siden Udenrigshandelsparametre](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

Som standard viser oversigtspanelet **Indlæs fra den globale lagermappe** listen over ER-formater fra det midlertidige lager, der automatisk oprettes ud fra GR-indholdet for at forbedre ydeevnen. Dette sker, når oversigtspanelet **Indlæs fra den globale lagermappe** åbnes for første gang, hvilket kan tage et par sekunder.

Hvis du ikke kan se det krævede ER-format i oversigtspanelet **Indlæs fra den globale lagermappe**, men du er sikker på, at dette ER-format er gemt i GR, skal du vælge indstillingen **Synkroniser**. Denne indstilling opdaterer det midlertidige lager og synkroniserer det med det aktuelle indhold af GR.

## <a name="feature-activation"></a>Funktionsaktivering

Tilgængeligheden af denne funktionalitet styres af funktionen **Udvidet opslag for ER-formatkonfigurationer med mulighed for at forespørge på den globale lagermappe** i **Funktionsstyring**. Denne funktion er som standard aktiveret.

[![Siden Funktionsstyring](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>Sikkerhedsovervejelser

Rettigheden **Vedligehold konfigurationslagre** (**ERMaintainSolutionRepositories**) styrer adgang til GR for en bruger, der åbner ER-formatopslaget med det aktiverede oversigtspanel **Indlæs fra den globale lagermappe**. Hvis du vil give brugere adgang til GR-indhold fra ER-formatopslag, skal du ændre sikkerhedsindstillingerne ved at tildele rettigheden **ERMaintainSolutionRepositories** til brugere, enten direkte eller ved at bruge allerede tildelte roller og opgaver.

Følgende skærmbillede viser, hvordan denne rettighed kan tildeles til brugere, der er tildelt rollen **Bogholder**. Denne rolle gør det muligt for brugere at konfigurere udenrigshandelsparametre og oprette referencer til ER-formaterne i felterne **Filformattilknytning** og **Rapportformattilknytning** på siden **Udenrigshandelsparametre**.

[![Siden Sikkerhedskonfiguration](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>Begrænsninger

Adgang til GR i ER-formatopslaget understøttes i øjeblikket kun for valg af ER-formater, der bruges til at generere udgående dokumenter.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>Hvorfor kan jeg ikke få adgang til den globale lagermappe fra ER-formatopslaget?

Hvis du har aktiveret funktionen **Udvidet opslag for ER-formatkonfigurationer med mulighed for at forespørge på den globale lagermappe** på siden **Funktionsstyring**, men brugere ikke kan se ER-formater i oversigtspanelet **Indlæs fra den globale lagermappe**, og indstillingen **Synkroniser** er synlig men deaktiveret, skal du kontrollere, at rettigheden **Vedligehold konfigurationslagre** (**ERMaintainSolutionRepositories**) er tildelt til brugeren. Kontakt systemadministratoren for at få denne rettighed.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [API-struktur til elektronisk rapportering (ER)](er-apis-app73.md)
- [Administrere livscyklus for konfigurationer af elektronisk rapportering (ER)](general-electronic-reporting-manage-configuration-lifecycle.md)
