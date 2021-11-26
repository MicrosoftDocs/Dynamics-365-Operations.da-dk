---
title: Tilpasse grænsefladen til produktionsudførelse
description: Dette emne forklarer, hvordan du kan udvide aktuelle formularer eller oprette nye formularer og knapper til grænsefladen for produktionsudførelse.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 414fe5d6e16ad125bc2b9bb7ed427e5db5180ec9
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790962"
---
# <a name="customize-the-production-floor-execution-interface"></a>Tilpasse grænsefladen til produktionsudførelse

[!include [banner](../includes/banner.md)]

Udviklere kan udvide aktuelle formularer eller oprette egne formularer og knapper til grænsefladen for produktionsudførelse. Når du har tilføjet koden for disse nye elementer, kan administratorer eller produktionsledere nemt føje dem til brugergrænsefladen ved at bruge standardkonfigurationens kontrolelementer.

Her er f.eks. nogle af de mulige løsninger, hvis der er brug for nye kolonner i en hovedformular:

- Udvid formularen `JmgProductionFloorExecutionMainGrid`, og tilføj de ønskede felter.
- Opret en ny formular, og tilføj den som en ny hovedvisning (fane).

## <a name="add-a-new-button-action"></a>Tilføj en ny knap (handling)

Hvis du vil tilføje en ny knap (handling), skal du udføre følgende trin for at oprette en klasse, der implementerer din egen handling.

1. Opret en ny klasse med navnet `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, hvor:

    - `<ExtensionPrefix>` identificerer løsningen entydigt, typisk ved hjælp af dit firmas navn.
    - `<ActionName>` er et entydigt navn til klassen. Det identificerer typisk handlingsmåden.

1. Den nye klasse skal udvide klassen `JmgProductionFloorExecutionAction`.
1. Tilsidesæt alle nødvendige metoder.

Du kan f.eks. se på koden for følgende klasser:

- `JmgProductionFloorExecutionBreakAction` – En klasse til en simpel handling, der ikke behøver nogen poster.
- `JmgProductionFloorExecutionReportFeedbackAction` – En klasse, der giver mere komplekse funktioner.

Når du er færdig, vises den nye knap (handling) automatisk på siden **Designfaner** i Microsoft Dynamics 365 Supply Chain Management. Her kan du (eller en administrator eller produktionsleder) nemt føje den til den primære eller sekundære værktøjslinje på samme måde, som du kan tilføje standardknapperne. Der er vejledning i [Designe grænsefladen til kørsel af produktionsudstyr](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Tilføje en ny hovedvisning

1. Opret en ny formular, der har de ønskede elementer og funktioner. Bemærk, at denne formular er en ny formular, ikke en udvidelse. Navngiv formularen `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, hvor:

    - `<ExtensionPrefix>` identificerer løsningen entydigt, typisk ved hjælp af dit firmas navn.
    - `<FormName>` er et entydigt navn til formularen.

1. Opret et menupunkt med navnet `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Opret en udvidelse med navnet `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, hvor metoden `getMainMenuItemsList` udvides ved at føje det nye menupunkt til listen. Følgende kode viser et eksempel.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionForm))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Når du er færdig, vises den nye hovedvisning automatisk i kombinationsfeltet **Hovedvisning** under **Designfaner** i Supply Chain Management. Her kan du (eller en administrator eller produktionsleder) nemt føje den til nye eller eksisterende faner på samme måde, som du kan tilføje standardhovedvisningerne. Der er vejledning i [Designe grænsefladen til kørsel af produktionsudstyr](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Tilføje en detaljevisning

1. Opret en ny formular, der har de ønskede elementer og funktioner. Bemærk, at denne formular er ny, ikke en udvidelse. Navngiv formularen `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, hvor: 

    - `<ExtensionPrefix>` identificerer løsningen entydigt, typisk ved hjælp af dit firmas navn.
    - `<FormName>` er et entydigt navn til formularen.

1. Opret et menupunkt med navnet `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Opret en udvidelse med navnet `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, hvor metoden `getDetailsMenuItemList` udvides ved at føje det nye menupunkt til listen.

Når du er færdig, vises den nye detaljevisning automatisk i kombinationsfeltet **Detaljevisning** under **Designfaner** i Supply Chain Management. Her kan du (eller en administrator eller produktionsleder) nemt føje den til nye eller eksisterende faner på samme måde, som du kan tilføje standarddetaljevisningerne. Der er vejledning i [Designe grænsefladen til kørsel af produktionsudstyr](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Føje et numerisk tastatur til en formular eller dialogboks

I følgende eksempel vises, hvordan du føjer numeriske tastaturer til en formular.

1. Antallet af numeriske tastatur-controllere, som hver formular indeholder, skal være lig med antallet af numeriske tastaturer i den pågældende formular.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Konfigurer funktionaliteten for hver numerisk tastatur-controller, og forbind hver enkelt numeriske tastatur-controller til en formulardel for numerisk tastatur.

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Bruge et numerisk tastatur som pop op-dialogboks

I følgende eksempel kan du se en måde at konfigurere en numerisk tastatur-controller til en pop op-dialogboks på.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

I følgende eksempel kan du se en måde at kalde det numeriske tastaturs pop op-dialogboks på.

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="additional-resources"></a>Yderligere ressourcer

- [Designe grænsefladen til produktionsudførelse](production-floor-execution-styles.md)
- [Designe grænsefladen til produktionsudførelse](production-floor-execution-tabs.md)
