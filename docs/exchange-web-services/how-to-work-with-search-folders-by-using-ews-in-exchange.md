---
title: Arbeiten Sie mit Suchordner in Exchange mithilfe der Exchange-Webdienste
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: abe703c5-6d85-46d9-bf20-230c34782a9f
description: Erhalten Sie Informationen zum Erstellen, abrufen, aktualisieren und Löschen von Suchordnern durch Verwenden der EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: e38ff50fcdb5e42cea3f4b2e25345375f84ae6eb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757047"
---
# <a name="work-with-search-folders-by-using-ews-in-exchange"></a><span data-ttu-id="c2661-103">Arbeiten Sie mit Suchordner in Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="c2661-103">Work with search folders by using EWS in Exchange</span></span>

<span data-ttu-id="c2661-104">Erhalten Sie Informationen zum Erstellen, abrufen, aktualisieren und Löschen von Suchordnern durch Verwenden der EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="c2661-104">Find out how to create, get, update, and delete search folders by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="c2661-105">Ein Suchordner stellt eine beständige "ständig" Suche im Postfach eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="c2661-105">A search folder represents a persistent "always-on" search in a user's mailbox.</span></span> <span data-ttu-id="c2661-106">Ein Suchordner sucht und verhält sich wie ein normales Postfach-Ordner.</span><span class="sxs-lookup"><span data-stu-id="c2661-106">A search folder looks and acts like a regular mailbox folder.</span></span> <span data-ttu-id="c2661-107">Es enthält jedoch statt, die Elemente enthält, eine "virtuelle" Kopie von Elementen aus alle Ordner in den Suchbereich, die für den Ordner festlegen den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c2661-107">However, instead of containing items, it contains a "virtual" copy of items from any folders in its search scope that match the search criteria set on the folder.</span></span> <span data-ttu-id="c2661-108">Anwendungen und Endbenutzer können Suchordner.</span><span class="sxs-lookup"><span data-stu-id="c2661-108">Both applications and end-users can use search folders.</span></span> <span data-ttu-id="c2661-109">Muss die Anwendung die gleiche Suche immer wieder ausführen?</span><span class="sxs-lookup"><span data-stu-id="c2661-109">Does your application need to perform the same search over and over?</span></span> <span data-ttu-id="c2661-110">Suchordner sind ein hervorragendes Tool für diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="c2661-110">Search folders are a great tool for this task.</span></span> <span data-ttu-id="c2661-111">Oder vielleicht Sie einfach Ihre Benutzer bieten die Möglichkeit, Zugriff auf und Verwaltung von Suchordnern in Ihrem Client möchten.</span><span class="sxs-lookup"><span data-stu-id="c2661-111">Or maybe you just want to give your users the ability to access and manage search folders in your client.</span></span> <span data-ttu-id="c2661-112">Den Inhalt des Szenarios, die EWS Managed API und EWS aktivieren Ihrer Anwendung Suchordner vollständig zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="c2661-112">Whatever your scenario, the EWS Managed API and EWS enable your application to fully interact with search folders.</span></span>
  
<span data-ttu-id="c2661-113">**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für die Arbeit mit Suchordnern**</span><span class="sxs-lookup"><span data-stu-id="c2661-113">**Table 1. EWS Managed API methods and EWS operations for working with search folders**</span></span>

|<span data-ttu-id="c2661-114">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="c2661-114">**If you want to…**</span></span>|<span data-ttu-id="c2661-115">**Verwenden Sie in die EWS Managed API...**</span><span class="sxs-lookup"><span data-stu-id="c2661-115">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="c2661-116">**Verwenden Sie in der Exchange-Webdienste...**</span><span class="sxs-lookup"><span data-stu-id="c2661-116">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c2661-117">Erstellen eines Suchordners</span><span class="sxs-lookup"><span data-stu-id="c2661-117">Create a search folder</span></span>  <br/> |[<span data-ttu-id="c2661-118">SearchFolder.Save</span><span class="sxs-lookup"><span data-stu-id="c2661-118">SearchFolder.Save</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="c2661-119">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="c2661-119">CreateFolder operation</span></span>](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="c2661-120">Abrufen von Ordnern suchen</span><span class="sxs-lookup"><span data-stu-id="c2661-120">Get a search folder</span></span>  <br/> |[<span data-ttu-id="c2661-121">SearchFolder.Bind</span><span class="sxs-lookup"><span data-stu-id="c2661-121">SearchFolder.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="c2661-122">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="c2661-122">GetFolder operation</span></span>](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="c2661-123">Aktualisieren eines Suchordners</span><span class="sxs-lookup"><span data-stu-id="c2661-123">Update a search folder</span></span>  <br/> |[<span data-ttu-id="c2661-124">SearchFolder.Update</span><span class="sxs-lookup"><span data-stu-id="c2661-124">SearchFolder.Update</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="c2661-125">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c2661-125">UpdateFolder operation</span></span>](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="c2661-126">Löschen eines Suchordners</span><span class="sxs-lookup"><span data-stu-id="c2661-126">Delete a search folder</span></span>  <br/> |[<span data-ttu-id="c2661-127">SearchFolder.Delete</span><span class="sxs-lookup"><span data-stu-id="c2661-127">SearchFolder.Delete</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="c2661-128">DeleteFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c2661-128">DeleteFolder operation</span></span>](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
   
## <a name="core-concepts-to-know-for-working-with-search-folders"></a><span data-ttu-id="c2661-129">Kernkonzepte für die Arbeit mit Suchordner</span><span class="sxs-lookup"><span data-stu-id="c2661-129">Core concepts to know for working with search folders</span></span>
<span data-ttu-id="c2661-130"><a name="bk_CoreConcepts"> </a></span><span class="sxs-lookup"><span data-stu-id="c2661-130"></span></span>

<span data-ttu-id="c2661-131">Vor Beginn der Arbeit mit Suchordnern, sollten Sie mit wie von Suchfilter vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="c2661-131">Before you start working with search folders, you'll want to be familiar with how search filters work.</span></span> <span data-ttu-id="c2661-132">Suchordner basieren auf Suchfilter, deren Kriterien express.</span><span class="sxs-lookup"><span data-stu-id="c2661-132">Search folders rely on search filters to express their criteria.</span></span> <span data-ttu-id="c2661-133">Suchfilter für Suchordner werden auf die gleiche Weise, [Suchfilter für Suchabfragen](how-to-use-search-filters-with-ews-in-exchange.md) konstruiert werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2661-133">Search filters for search folders are constructed in the same way that [search filters for search operations](how-to-use-search-filters-with-ews-in-exchange.md) are constructed.</span></span> 
  
## <a name="create-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="c2661-134">Erstellen eines Suchordners mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="c2661-134">Create a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="c2661-135"><a name="bk_CreateEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="c2661-135"></span></span>

<span data-ttu-id="c2661-136">Im Grunde, erstellen Sie einen Suchordner mit der EWS Managed API auf die gleiche Weise, die Sie einen regulären Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2661-136">Basically, you create a search folder using the EWS Managed API in the same way that you create a regular folder.</span></span> <span data-ttu-id="c2661-137">Hingegen ohne die [Ordner-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx)verwenden, verwenden Sie die [SearchFolder-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx), und legen Sie die [SearchParameters-Eigenschaft](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.searchparameters%28v=exchg.80%29.aspx) so konfigurieren Sie die Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c2661-137">However, instead of using the [Folder class](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx), you use the [SearchFolder class](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx), and set the [SearchParameters property](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.searchparameters%28v=exchg.80%29.aspx) to configure the search criteria.</span></span> 
  
<span data-ttu-id="c2661-138">Im folgenden Beispiel wird ein Suchordner erstellt, um alle Nachrichten im Posteingang und seinen Unterordnern, die vom Vorgesetzten des Benutzers, gesendet wurden suchen sadie@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c2661-138">In the following example, a search folder is created to find all messages in the Inbox and its subfolders that were sent by the user's manager, sadie@contoso.com.</span></span> <span data-ttu-id="c2661-139">Der Ordner wird als untergeordnetes Element des Ordners Durchsuchen von Ordnern im Postfach des Benutzers erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2661-139">The folder is created as a child of the Search Folders folder in the user's mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c2661-140">Sie können einen Suchordner als untergeordnetes Element des alle Ordner im Postfach des Benutzers erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2661-140">You can create a search folder as a child of any folder in the user's mailbox.</span></span> <span data-ttu-id="c2661-141">Wenn Sie den neu erstellten Ordner unter Suchordner in Outlook angezeigt werden soll, erstellen Sie es jedoch unter bekannte Ordner Suchordner, verwenden Sie den **SearchFolders** -Wert der [WellKnownFolderName-Enumeration](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c2661-141">However, if you want the newly created folder to show up under Search Folders in Outlook, create it under the Search Folders well-known folder, using the **SearchFolders** value of the [WellKnownFolderName enumeration](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx).</span></span> 
  
<span data-ttu-id="c2661-142">In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c2661-142">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void CreateSearchFolder(ExchangeService service)
{
    // Create the folder.
    SearchFolder searchFolder = new SearchFolder(service);
    searchFolder.DisplayName = "From Manager";
    // Create a search filter to express the criteria
    // for the folder.
    EmailAddress manager = new EmailAddress("sadie@contoso.com");
    SearchFilter.IsEqualTo fromManagerFilter =
        new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
    // Set the search filter.
    searchFolder.SearchParameters.SearchFilter = fromManagerFilter;
    // Set the folder to search.
    searchFolder.SearchParameters.RootFolderIds.Add(WellKnownFolderName.Inbox);
    // Set the search traversal. Deep will search all subfolders.
    searchFolder.SearchParameters.Traversal = SearchFolderTraversal.Deep;
    // Call Save to make the EWS call to create the folder.
    searchFolder.Save(WellKnownFolderName.SearchFolders);
}
```

## <a name="create-a-search-folder-by-using-ews"></a><span data-ttu-id="c2661-143">Erstellen eines Suchordners mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="c2661-143">Create a search folder by using EWS</span></span>
<span data-ttu-id="c2661-144"><a name="bk_CreateEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="c2661-144"></span></span>

<span data-ttu-id="c2661-145">Wenn Sie Exchange-Webdienste verwenden, verwenden Sie die [CreateFolder-Vorgang](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) mit einem [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) -Element zum Erstellen eines Suchordners.</span><span class="sxs-lookup"><span data-stu-id="c2661-145">If you are using EWS, use the [CreateFolder operation](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) with a [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element to create a search folder.</span></span> <span data-ttu-id="c2661-146">Im folgenden Beispiel für die Anforderung wird ein Suchordner erstellt, um alle Nachrichten im Posteingang und seinen Unterordnern, die vom Vorgesetzten des Benutzers, gesendet wurden suchen sadie@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c2661-146">In the following request example, a search folder is created to find all messages in the Inbox and its subfolders that were sent by the user's manager, sadie@contoso.com.</span></span> <span data-ttu-id="c2661-147">Der Ordner wird im Suchordner Ordner im Postfach des Benutzers erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2661-147">The folder is created in the Search Folders folder in the user's mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c2661-148">Sie können einen Suchordner als untergeordnetes Element des alle Ordner im Postfach des Benutzers erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2661-148">You can create a search folder as a child of any folder in the user's mailbox.</span></span> <span data-ttu-id="c2661-149">Wenn Sie den neu erstellten Ordner unter Suchordner in Outlook angezeigt werden soll, erstellen Sie es jedoch unter bekannte Ordner Suchordner, mit dem **Searchfolders** -Wert in das **Id** -Attribut des [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) -Elements.</span><span class="sxs-lookup"><span data-stu-id="c2661-149">However, if you want the newly created folder to show up under Search Folders in Outlook, create it under the Search Folders well-known folder, using the **searchfolders** value in the **Id** attribute of the [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateFolder>
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="searchfolders" />
      </m:ParentFolderId>
      <m:Folders>
        <t:SearchFolder>
          <t:DisplayName>From Manager</t:DisplayName>
          <t:SearchParameters Traversal="Deep">
            <t:Restriction>
              <t:IsEqualTo>
                <t:FieldURI FieldURI="message:Sender" />
                <t:FieldURIOrConstant>
                  <t:Constant Value="sadie@contoso.com" />
                </t:FieldURIOrConstant>
              </t:IsEqualTo>
            </t:Restriction>
            <t:BaseFolderIds>
              <t:DistinguishedFolderId Id="inbox" />
            </t:BaseFolderIds>
          </t:SearchParameters>
        </t:SearchFolder>
      </m:Folders>
    </m:CreateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c2661-150">Der Server antwortet mit einer [CreateFolderResponse](http://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx) -Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Wert des **NoError**, enthält die erfolgreiche Ausführung angibt.</span><span class="sxs-lookup"><span data-stu-id="c2661-150">The server responds with a [CreateFolderResponse](http://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="get-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="c2661-151">Abrufen von Ordnern suchen nach die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="c2661-151">Get a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="c2661-152"><a name="bk_RetrieveEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="c2661-152"></span></span>

<span data-ttu-id="c2661-153">Verwenden Sie die [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) EWS Managed API-Methode, um die Suchordner zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c2661-153">Use the [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) EWS Managed API method to find search folders.</span></span> <span data-ttu-id="c2661-154">Beachten Sie jedoch, Ihre Ergebnisse, um nur die Suchordner gehören zu begrenzen. Sie sollten beachten, die beim die Ergebnisse zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c2661-154">Note, however, that you can't limit your results to only include search folders; you'll want to keep that in mind when you process the results.</span></span> <span data-ttu-id="c2661-155">Verwenden Sie die [SearchFolder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) -Methode, um die Suchordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c2661-155">Use the [SearchFolder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) method to get search folders.</span></span> 
  
<span data-ttu-id="c2661-156">Im folgenden Beispiel werden die ersten 10 Ordner in dem Ordner Suchordner gesucht.</span><span class="sxs-lookup"><span data-stu-id="c2661-156">The following example finds the first 10 folders in the Search Folders folder.</span></span> <span data-ttu-id="c2661-157">Er prüft, ob jeweils ein Suchordner ist, und wenn also den Suchordner wird abgerufen, und wie viele Zielordner zeigt durchsucht.</span><span class="sxs-lookup"><span data-stu-id="c2661-157">It checks to determine whether each one is a search folder, and if so, it gets the search folder and displays how many target folders it searches.</span></span>
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void GetSearchFolders(ExchangeService service)
{
    FolderView folderView = new FolderView(10);
    folderView.PropertySet = new PropertySet(FolderSchema.DisplayName);
    try
    {
        FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.SearchFolders, folderView);
        foreach (Folder folder in findResults.Folders)
        {
            // You can't request only search folders in 
            // a FindFolders request, so other search folders might also be present.
            if (folder is SearchFolder)
            {
                Console.WriteLine("{0} is a search folder.", folder.DisplayName);
                // In order to access the SearchParameters property,
                // you have to bind to the folder. SearchParameters are not
                // returned in FindFolders results.
                SearchFolder searchFolder = SearchFolder.Bind(service, folder.Id);
                Console.WriteLine("Number of folders searched: {0}.",
                    searchFolder.SearchParameters.RootFolderIds.Count);
            }
            else
            {
                Console.WriteLine("{0} is NOT a search folder.", folder.DisplayName);
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

## <a name="get-a-search-folder-by-using-ews"></a><span data-ttu-id="c2661-158">Abrufen eines Suchordners mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="c2661-158">Get a search folder by using EWS</span></span>
<span data-ttu-id="c2661-159"><a name="bk_RetrieveEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="c2661-159"></span></span>

<span data-ttu-id="c2661-160">Wenn Sie Exchange-Webdienste verwenden, verwenden Sie die [FindFolder Vorgang](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) , um Durchsuchen von Ordnern und der [GetFolder-Vorgang](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) zum Abrufen von Suchordnern zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c2661-160">If you're using EWS, use the [FindFolder operation](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) to find search folders, and the [GetFolder operation](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) to get search folders.</span></span> <span data-ttu-id="c2661-161">Eine erfolgreiche Antwort **GetFolder** für ein Suchordner wird ein [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="c2661-161">A successful **GetFolder** response for a search folder will contain a [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="c2661-162">Im folgenden anforderungsbeispiel sucht die ersten 10 Ordnern im Ordner Suchordner.</span><span class="sxs-lookup"><span data-stu-id="c2661-162">The following request example finds the first 10 folders in the Search Folders folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Shallow">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:DisplayName" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="searchfolders" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c2661-163">Der Server gibt die folgende Antwort, die ein Suchordner zeigt.</span><span class="sxs-lookup"><span data-stu-id="c2661-163">The server returns the following response, which shows one search folder.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="3" TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Folders>
              <t:SearchFolder>
                <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
                <t:DisplayName>From Manager</t:DisplayName>
              </t:SearchFolder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </m:FindFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="c2661-164">Im folgenden Beispiel wird eine Anforderung verwendet den Wert des Elements [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) aus der vorherigen Antwort in einer **GetFolder** -Vorgang Anforderung zum Abrufen des Suchordners.</span><span class="sxs-lookup"><span data-stu-id="c2661-164">The following example of a request uses the value of the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) element from the previous response in a **GetFolder** operation request to get the search folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c2661-165">Der Server gibt die folgende Antwort mit den erstklassigen Eigenschaften für den Suchordner.</span><span class="sxs-lookup"><span data-stu-id="c2661-165">The server returns the following response with all the first-class properties for the search folder.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:SearchFolder>
              <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
              <t:ParentFolderId Id="AQMkAGM2..." ChangeKey="AQAAAA==" />
              <t:FolderClass>IPF.Note</t:FolderClass>
              <t:DisplayName>From Manager</t:DisplayName>
              <t:TotalCount>8</t:TotalCount>
              <t:ChildFolderCount>0</t:ChildFolderCount>
              <t:EffectiveRights>
                <t:CreateAssociated>true</t:CreateAssociated>
                <t:CreateContents>true</t:CreateContents>
                <t:CreateHierarchy>true</t:CreateHierarchy>
                <t:Delete>true</t:Delete>
                <t:Modify>true</t:Modify>
                <t:Read>true</t:Read>
                <t:ViewPrivateItems>true</t:ViewPrivateItems>
              </t:EffectiveRights>
              <t:UnreadCount>0</t:UnreadCount>
              <t:SearchParameters Traversal="Deep">
                <t:Restriction>
                  <t:IsEqualTo>
                    <t:FieldURI FieldURI="message:Sender" />
                    <t:FieldURIOrConstant>
                      <t:Constant Value="/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=8d84a3f4cbb34d48838a3aecf99795c0-Sadie" />
                    </t:FieldURIOrConstant>
                  </t:IsEqualTo>
                </t:Restriction>
                <t:BaseFolderIds>
                  <t:FolderId Id="AQMkAGM2..." ChangeKey="AQAAAA==" />
                </t:BaseFolderIds>
              </t:SearchParameters>
            </t:SearchFolder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

## <a name="update-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="c2661-166">Aktualisieren eines Suchordners mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="c2661-166">Update a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="c2661-167"><a name="bk_UpdateEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="c2661-167"></span></span>

<span data-ttu-id="c2661-168">Verwenden Sie die [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) EWS Managed API-Methode für ein **SearchFolder** -Objekt, um ein Suchordner zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c2661-168">Use the [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) EWS Managed API method on a **SearchFolder** object to update a search folder.</span></span> <span data-ttu-id="c2661-169">Im folgenden Beispiel werden die Suchkriterien in einem Suchordner mit dem Anzeigenamen "Vom Manager" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c2661-169">The following example updates the search criteria on a search folder with the display name "From Manager".</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void UpdateSearchFolder(ExchangeService service)
{
    FolderView folderView = new FolderView(10);
    folderView.PropertySet = new PropertySet(FolderSchema.DisplayName);
    try
    {
        FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.SearchFolders, folderView);
        foreach (Folder folder in findResults.Folders)
        {
            // You cannot request only search folders in 
            // a FindFolders request, so other search folders might also be present.
            if (folder is SearchFolder &amp;&amp; folder.DisplayName.Equals("From Manager"))
            {
                Console.WriteLine("\"{0}\" folder found.", folder.DisplayName);
                SearchFolder searchFolder = folder as SearchFolder;
                EmailAddress newManager = new EmailAddress("hope@contoso.com");
                SearchFilter.IsEqualTo newManagerFilter =
                    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, newManager);
                searchFolder.SearchParameters.SearchFilter = newManagerFilter;
                searchFolder.SearchParameters.RootFolderIds.Add(WellKnownFolderName.Inbox);
                searchFolder.SearchParameters.Traversal = SearchFolderTraversal.Deep;
                searchFolder.Update();
                Console.WriteLine("\"{0}\" folder updated.", folder.DisplayName);
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

## <a name="update-a-search-folder-by-using-ews"></a><span data-ttu-id="c2661-170">Aktualisieren eines Suchordners mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="c2661-170">Update a search folder by using EWS</span></span>
<span data-ttu-id="c2661-171"><a name="bk_UpdateEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="c2661-171"></span></span>

<span data-ttu-id="c2661-172">Wenn Sie Exchange-Webdienste verwenden, verwenden Sie die [UpdateFolder Vorgang](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) mit einem [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) -Element einen Suchordner aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c2661-172">If you're using EWS, use the [UpdateFolder operation](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) with a [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element to update a search folder.</span></span> <span data-ttu-id="c2661-173">Im folgenden anforderungsbeispiel aktualisiert die Suchkriterien auf den Ordner "Vom Manager" suchen.</span><span class="sxs-lookup"><span data-stu-id="c2661-173">The following request example updates the search criteria on the "From Manager" search folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:SearchParameters" />
              <t:SearchFolder>
                <t:SearchParameters Traversal="Deep">
                  <t:Restriction>
                    <t:IsEqualTo>
                      <t:FieldURI FieldURI="message:Sender" />
                      <t:FieldURIOrConstant>
                        <t:Constant Value="hope@contoso.com" />
                      </t:FieldURIOrConstant>
                    </t:IsEqualTo>
                  </t:Restriction>
                  <t:BaseFolderIds>
                    <t:DistinguishedFolderId Id="inbox" />
                  </t:BaseFolderIds>
                </t:SearchParameters>
              </t:SearchFolder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c2661-174">Der Server antwortet mit einer [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) -Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Wert des **NoError**, enthält die erfolgreiche Ausführung angibt.</span><span class="sxs-lookup"><span data-stu-id="c2661-174">The server responds with an [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="delete-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="c2661-175">Löschen eines Suchordners mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="c2661-175">Delete a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="c2661-176"><a name="bk_DeleteEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="c2661-176"></span></span>

<span data-ttu-id="c2661-177">Verwenden Sie die [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) EWS Managed API-Methode für ein **SearchFolder** -Objekt, um ein Suchordner löschen.</span><span class="sxs-lookup"><span data-stu-id="c2661-177">Use the [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) EWS Managed API method on a **SearchFolder** object to delete a search folder.</span></span> <span data-ttu-id="c2661-178">Im folgenden Beispiel wird einen Suchordner mit dem Anzeigenamen "Vom Manager".</span><span class="sxs-lookup"><span data-stu-id="c2661-178">The following example deletes a search folder with the display name "From Manager".</span></span> <span data-ttu-id="c2661-179">Der gelöschte Suchordner wird in den Ordner Gelöschte Objekte verschoben.</span><span class="sxs-lookup"><span data-stu-id="c2661-179">The deleted search folder is moved to the Deleted Items folder.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void DeleteSearchFolder(ExchangeService service)
{
    FolderView folderView = new FolderView(10);
    folderView.PropertySet = new PropertySet(FolderSchema.DisplayName);
    try
    {
        FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.SearchFolders, folderView);
        foreach (Folder folder in findResults.Folders)
        {
            // You cannot request only search folders in 
            // a FindFolders request, so other folders might also be present.
            if (folder is SearchFolder &amp;&amp; folder.DisplayName.Equals("From Manager"))
            {
                Console.WriteLine("\"{0}\" folder found.", folder.DisplayName);
                folder.Delete(DeleteMode.MoveToDeletedItems);
                Console.WriteLine("\"{0}\" folder deleted.", folder.DisplayName);
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

## <a name="delete-a-search-folder-by-using-ews"></a><span data-ttu-id="c2661-180">Löschen eines Suchordners mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="c2661-180">Delete a search folder by using EWS</span></span>
<span data-ttu-id="c2661-181"><a name="bk_DeleteEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="c2661-181"></span></span>

<span data-ttu-id="c2661-182">Wenn Sie Exchange-Webdienste verwenden, verwenden Sie die [DeleteFolder-Vorgang](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) zum Löschen eines Suchordners.</span><span class="sxs-lookup"><span data-stu-id="c2661-182">If you're using EWS, use the [DeleteFolder operation](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) to delete a search folder.</span></span> <span data-ttu-id="c2661-183">Im folgenden Beispiel wird einen Suchordner gelöscht und in den Ordner Gelöschte Objekte verschoben.</span><span class="sxs-lookup"><span data-stu-id="c2661-183">The following example deletes a search folder and moves it to the Deleted Items folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:DeleteFolder DeleteType="MoveToDeletedItems">
      <m:FolderIds>
        <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
      </m:FolderIds>
    </m:DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c2661-184">Der Server antwortet mit einer [DeleteFolderResponse](http://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx) -Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Wert des **NoError**, enthält die erfolgreiche Ausführung angibt.</span><span class="sxs-lookup"><span data-stu-id="c2661-184">The server responds with a [DeleteFolderResponse](http://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c2661-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2661-185">See also</span></span>


- [<span data-ttu-id="c2661-186">Suche und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="c2661-186">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c2661-187">Verwenden Sie Suchfilter mit EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="c2661-187">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)
    
- [<span data-ttu-id="c2661-188">"SearchFolder"-Klasse</span><span class="sxs-lookup"><span data-stu-id="c2661-188">SearchFolder class</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="c2661-189">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="c2661-189">CreateFolder operation</span></span>](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx)
    
- [<span data-ttu-id="c2661-190">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="c2661-190">FindFolder operation</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="c2661-191">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="c2661-191">GetFolder operation</span></span>](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)
    
- [<span data-ttu-id="c2661-192">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c2661-192">UpdateFolder operation</span></span>](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)
    
- [<span data-ttu-id="c2661-193">DeleteFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c2661-193">DeleteFolder operation</span></span>](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)
    

