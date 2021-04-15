---
title: Angive brugerdefinerede lagersteder til oprettede dokumenter
description: I dette emne beskrives, hvordan du kan udvide listen over placering til lagring af dokumenter, som genereres ved elektronisk rapportering (ER).
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 25719de3d86785442e00f7375de525b95bdb094d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753690"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="15148-103">Angive brugerdefinerede lagersteder til oprettede dokumenter</span><span class="sxs-lookup"><span data-stu-id="15148-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="15148-104">Med API'en (application programming interface) i den elektroniske rapporteringsstruktur (ER) kan du udvide listen over lagerplaceringer til dokumenter, som ER-formater genererer.</span><span class="sxs-lookup"><span data-stu-id="15148-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="15148-105">Dette emne forklarer, hvordan du kan føje en brugerdefineret lagerplacering til genererede dokumenter ved at delegere opgaven til oprettelse af ER-destinationer til standarddestinationsfabrikken og derefter implementere en brugerdefineret klasse, der har sin egen destinationslogik.</span><span class="sxs-lookup"><span data-stu-id="15148-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="15148-106">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="15148-106">Prerequisites</span></span>

<span data-ttu-id="15148-107">Installer en topologi, der understøtter fortløbende build.</span><span class="sxs-lookup"><span data-stu-id="15148-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="15148-108">Du kan finde flere oplysninger under [Installere topologier, der understøtter fortløbende build og automatisering af test](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span><span class="sxs-lookup"><span data-stu-id="15148-108">For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="15148-109">Du skal også have adgang til denne topologi for en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="15148-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="15148-110">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="15148-110">Electronic reporting developer</span></span>
- <span data-ttu-id="15148-111">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="15148-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="15148-112">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="15148-112">System administrator</span></span>

<span data-ttu-id="15148-113">Du skal også have adgang til udviklingsmiljøet for denne topologi.</span><span class="sxs-lookup"><span data-stu-id="15148-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="15148-114">Alle opgaverne i dette emne kan fuldføres i **USMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="15148-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="15148-115">Importere ER-formatet Rul anlægsaktiver fremad</span><span class="sxs-lookup"><span data-stu-id="15148-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="15148-116">Hvis du vil generere de dokumenter, som du planlægger at tilføje en brugerdefineret lagerplacering for, skal du [importere](er-download-configurations-global-repo.md) konfigurationen af ER-formatet **Rul anlægsaktiver fremad** til den aktuelle topologi.</span><span class="sxs-lookup"><span data-stu-id="15148-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![Siden Konfigurationslager](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="15148-118">Køre rapporten Rul anlægsaktiver fremad</span><span class="sxs-lookup"><span data-stu-id="15148-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="15148-119">Gå til **Anlægsaktiver** \> **Forespørgsler og rapporter** \> **Transaktionsrapporter** \> **Rul anlægsaktiver fremad**.</span><span class="sxs-lookup"><span data-stu-id="15148-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="15148-120">I feltet **Fra dato** skal du indtaste **01-01-2017** (1. januar 2017).</span><span class="sxs-lookup"><span data-stu-id="15148-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="15148-121">I feltet **Til dato** skal du indtaste **31-01-2017** (31. januar 2017).</span><span class="sxs-lookup"><span data-stu-id="15148-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="15148-122">Vælg **Regnskabsvaluta** i feltet **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="15148-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="15148-123">Gå til feltet **Formattilknytning**, og vælg **Rul anlægsaktiver fremad**.</span><span class="sxs-lookup"><span data-stu-id="15148-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="15148-124">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="15148-124">Select **OK**.</span></span>

![Kørselsdialogboks for rapporten Rul anlægsaktiver fremad](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="15148-126">I Microsoft Excel skal du gennemse det udgående dokument, der er oprettet, og som kan hentes.</span><span class="sxs-lookup"><span data-stu-id="15148-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="15148-127">Denne funktionsmåde er [standardfunktionsmåden](electronic-reporting-destinations.md#default-behavior) for et ER-format, der ikke er konfigureret [destinationer](electronic-reporting-destinations.md) for, og som kører i interaktiv tilstand.</span><span class="sxs-lookup"><span data-stu-id="15148-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="15148-128">Gennemse kildekoden</span><span class="sxs-lookup"><span data-stu-id="15148-128">Review the source code</span></span>

<span data-ttu-id="15148-129">Gennemse koden for metoden `generateReportByGER()` i klassen `AssetRollForwardService`.</span><span class="sxs-lookup"><span data-stu-id="15148-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="15148-130">Bemærk, at metoden `Run()` bruges til at kalde ER-strukturen og generere rapporten **Rul anlægsaktiver fremad**.</span><span class="sxs-lookup"><span data-stu-id="15148-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a><span data-ttu-id="15148-131">Ændre kildekoden</span><span class="sxs-lookup"><span data-stu-id="15148-131">Modify the source code</span></span>

1. <span data-ttu-id="15148-132">I Visual Studio-projektet skal du tilføje en ny klasse (`AssetRollForwardDestination` i dette eksempel) og skrive kode for at implementere den brugerdefinerede destination for de **Rul anlægsaktiver fremad**-rapporter, der genereres.</span><span class="sxs-lookup"><span data-stu-id="15148-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="15148-133">Metoden `new()` er beregnet til at hente det oprindelige ER-destinationsobjekt og den programlogikbaserede parameter, der angiver den brugerdefinerede placering, hvor genererede rapporter skal gemmes.</span><span class="sxs-lookup"><span data-stu-id="15148-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="15148-134">I dette eksempel er den brugerdefinerede placering navnet på en mappe i det lokale filsystem på den server, der kører AOS-tjenesten (applikationsobjektserver).</span><span class="sxs-lookup"><span data-stu-id="15148-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="15148-135">Metoden `saveFile()` er udviklet til at gemme et genereret dokument i en mappe i det lokale filsystem på den server, der kører AOS-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="15148-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. <span data-ttu-id="15148-136">I Visual Studio-projektet skal du tilføje en ny klasse (`AssetRollForwardDestinationFactory` i dette eksempel) og skrive kode for at oprette en brugerdefineret destinationsfabrik, der uddelegerer oprettelsen af en destination til standarddestinationsfabrikken, og for at ombryde en destinationsfil med din egen destination.</span><span class="sxs-lookup"><span data-stu-id="15148-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. <span data-ttu-id="15148-137">Rediger den eksisterende `AssetRollForwardService`-klasse, og skriv kode for at oprette en brugerdefineret destinationsfabrik for rapportkørslen.</span><span class="sxs-lookup"><span data-stu-id="15148-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="15148-138">Bemærk, at når der er oprettet en brugerdefineret destinationsfabrik, overføres den applikationsbaserede parameter, der angiver en destinationsmappe.</span><span class="sxs-lookup"><span data-stu-id="15148-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="15148-139">På denne måde bruges denne destinationsmappe til lagring af genererede filer.</span><span class="sxs-lookup"><span data-stu-id="15148-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="15148-140">Kontroller, at den angivne mappe (**c:\\0** i dette eksempel) findes i det lokale filsystem på den server, der kører AOS-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="15148-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="15148-141">Ellers udløses der en [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1)-undtagelse ved kørsel.</span><span class="sxs-lookup"><span data-stu-id="15148-141">Otherwise, a [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. <span data-ttu-id="15148-142">Gendan dit projekt.</span><span class="sxs-lookup"><span data-stu-id="15148-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="15148-143">Køre rapporten Rul anlægsaktiver fremad igen</span><span class="sxs-lookup"><span data-stu-id="15148-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="15148-144">Gå til **Anlægsaktiver** \> **Forespørgsler og rapporter** \> **Transaktionsrapporter** \> **Rul anlægsaktiver fremad**.</span><span class="sxs-lookup"><span data-stu-id="15148-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="15148-145">Gå til feltet **Fra dato**, og indtast **01-01-2017**.</span><span class="sxs-lookup"><span data-stu-id="15148-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="15148-146">Gå til feltet **Til dato**, og indtast **31-01-2017**.</span><span class="sxs-lookup"><span data-stu-id="15148-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="15148-147">Vælg **Regnskabsvaluta** i feltet **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="15148-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="15148-148">Gå til feltet **Formattilknytning**, og vælg **Rul anlægsaktiver fremad**.</span><span class="sxs-lookup"><span data-stu-id="15148-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="15148-149">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="15148-149">Select **OK**.</span></span>
7. <span data-ttu-id="15148-150">Gennemse den lokale **C:\\0**-mappe for at søge efter den genererede fil.</span><span class="sxs-lookup"><span data-stu-id="15148-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="15148-151">Da `originDestination`-objektet ikke bruges i `AssetRollForwardDestination`-objektet i dette eksempel, ignoreres konfigurationerne for ER-formatets [destinationer](electronic-reporting-destinations.md) under kørsel.</span><span class="sxs-lookup"><span data-stu-id="15148-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15148-152">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="15148-152">Additional resources</span></span>

- [<span data-ttu-id="15148-153">Destinationer for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="15148-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="15148-154">Startside for udvidelsesmuligheder</span><span class="sxs-lookup"><span data-stu-id="15148-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]