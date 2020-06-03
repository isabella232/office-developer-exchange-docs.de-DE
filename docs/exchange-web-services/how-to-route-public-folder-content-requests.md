---
title: Weiterleiten von Inhaltsanforderungen für Öffentliche Ordner
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 59d2f05e-90fb-471e-ac06-70becc15b295
description: Alle Anforderungen für Öffentliche Ordner-Informationen, die den Inhalt des öffentlichen Ordners einbeziehen, müssen an das Postfach für Öffentliche Ordner weitergeleitet werden, das den Inhalt des Zielordners beinhaltet. Um die Anforderungen an dieses Postfach weiterzuleiten, müssen Sie die Header x-AnchorMailbox und x-PublicFolderMailbox auf bestimmte Werte festlegen.
ms.openlocfilehash: 523b9c8efc65253f7970fffeb5800e451784522d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527742"
---
# <a name="route-public-folder-content-requests"></a><span data-ttu-id="bb93e-104">Weiterleiten von Inhaltsanforderungen für Öffentliche Ordner</span><span class="sxs-lookup"><span data-stu-id="bb93e-104">Route public folder content requests</span></span>

<span data-ttu-id="bb93e-105">Alle Anforderungen für Öffentliche Ordner-Informationen, die den Inhalt des öffentlichen Ordners einbeziehen, müssen an das Postfach für Öffentliche Ordner weitergeleitet werden, das den Inhalt des Zielordners beinhaltet.</span><span class="sxs-lookup"><span data-stu-id="bb93e-105">All requests for public folder information that involve the content of the public folder need to be routed to the public folder mailbox that holds the content for the target folder.</span></span> <span data-ttu-id="bb93e-106">Um die Anforderungen an dieses Postfach weiterzuleiten, müssen Sie die Header **x-AnchorMailbox** und **x-PublicFolderMailbox** auf bestimmte Werte festlegen.</span><span class="sxs-lookup"><span data-stu-id="bb93e-106">To route the requests to that mailbox, you need to set the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers to specific values.</span></span> 
  
<span data-ttu-id="bb93e-107">Die folgende Tabelle bietet einen Überblick über den Prozess:</span><span class="sxs-lookup"><span data-stu-id="bb93e-107">The following table provides an overview of the process:</span></span>
  
<span data-ttu-id="bb93e-108">**Übersicht über öffentliche Ordner**</span><span class="sxs-lookup"><span data-stu-id="bb93e-108">**Public folder overview**</span></span>

|<span data-ttu-id="bb93e-109">Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="bb93e-109">Header</span></span>|<span data-ttu-id="bb93e-110">Was benötige ich?</span><span class="sxs-lookup"><span data-stu-id="bb93e-110">What do I need?</span></span>|<span data-ttu-id="bb93e-111">Wie erhalte ich diese?</span><span class="sxs-lookup"><span data-stu-id="bb93e-111">How do I get it?</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb93e-112">**X-AnchorMailbox**</span><span class="sxs-lookup"><span data-stu-id="bb93e-112">**X-AnchorMailbox**</span></span> <br/> |<span data-ttu-id="bb93e-113">1. [die x-AnchorMailbox-und x-PublicFolderInformation-Werte](how-to-route-public-folder-hierarchy-requests.md) für das hierarchiepostfach für Öffentliche Ordner.</span><span class="sxs-lookup"><span data-stu-id="bb93e-113">1. [The X-AnchorMailbox and X-PublicFolderInformation values ](how-to-route-public-folder-hierarchy-requests.md) for the public folder hierarchy mailbox.</span></span><br/><br/><span data-ttu-id="bb93e-114">2. die GUID des Postfachs für Öffentliche Ordner, das den Postfachinhalt enthält, der an den AutoErmittlungsdienst gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb93e-114">2. The GUID of the public folder mailbox that contains the mailbox content, which is sent to the Autodiscover service.</span></span><br/><br/>  <span data-ttu-id="bb93e-115">Das **AutoDiscoverSMTPAddress** in der nach Auto Ermittlungs-Antwort wird zum Wert des **X-AnchorMailbox-** Headers.</span><span class="sxs-lookup"><span data-stu-id="bb93e-115">The **AutoDiscoverSMTPAddress** in the Autodisover response becomes the value of the **X-AnchorMailbox** header.</span></span>  <br/> <span data-ttu-id="bb93e-116">![TODO](media/Ex15_PF_PFContent.png)</span><span class="sxs-lookup"><span data-stu-id="bb93e-116">![TODO](media/Ex15_PF_PFContent.png)</span></span>| <span data-ttu-id="bb93e-117">1. verwenden Sie das Codebeispiel in diesem Artikel, der [das verwaltete EWS-API implementiert](#bk_determineguidewsma).</span><span class="sxs-lookup"><span data-stu-id="bb93e-117">1. Use the code example in this article, which [implements the EWS Managed API](#bk_determineguidewsma).</span></span> <span data-ttu-id="bb93e-118">Oder [verwenden Sie EWS](#bk_determineguidews) , und konvertieren Sie Ihre Ergebnisse, um eine GUID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bb93e-118">Or [use EWS](#bk_determineguidews) and convert your results to obtain a GUID.</span></span><br/><br/><span data-ttu-id="bb93e-119">2. [Erstellen Sie eine Auto Ermittlungsanforderung](#bk_makeautodrequest) mithilfe der GUID und des Domänennamens.</span><span class="sxs-lookup"><span data-stu-id="bb93e-119">2. [Make an Autodiscover request](#bk_makeautodrequest) by using the GUID plus the domain name.</span></span><br/><br/><span data-ttu-id="bb93e-120">3. verwenden Sie den Wert des **AutoDiscoverSMTPAddress** -Elements, das in der AutoErmittlung-Antwort zurückgegeben wird, um [den Wert der Header aufzufüllen](#bk_setheadervalues).</span><span class="sxs-lookup"><span data-stu-id="bb93e-120">3. Use the value of the **AutoDiscoverSMTPAddress** element returned in the Autodiscover response to [populate the value of the headers](#bk_setheadervalues).</span></span>  <br/> |
|<span data-ttu-id="bb93e-121">**X-PublicFolderMailbox**</span><span class="sxs-lookup"><span data-stu-id="bb93e-121">**X-PublicFolderMailbox**</span></span> <br/> |<span data-ttu-id="bb93e-122">Ihre Arbeit ist abgeschlossen, der x-PublicFolderMailbox-Wert entspricht dem x-AnchorMailbox-Wert!</span><span class="sxs-lookup"><span data-stu-id="bb93e-122">Your work is done, the X-PublicFolderMailbox value is the same as the X-AnchorMailbox value!</span></span>  <br/> |<span data-ttu-id="bb93e-123">Sie haben Sie bereits!</span><span class="sxs-lookup"><span data-stu-id="bb93e-123">You already have it!</span></span>  <br/> |
   
<span data-ttu-id="bb93e-124">Nachdem Sie die Headerwerte bestimmt haben, schließen Sie diese ein, [Wenn Sie Inhaltsanforderungen für Öffentliche Ordner vornehmen](#bk_setheadervalues).</span><span class="sxs-lookup"><span data-stu-id="bb93e-124">After you have determined the header values, include them [when you make public folder content requests](#bk_setheadervalues).</span></span>
  
<span data-ttu-id="bb93e-125">Die Schritte in diesem Artikel gelten speziell für Inhaltsanforderungen für Öffentliche Ordner.</span><span class="sxs-lookup"><span data-stu-id="bb93e-125">The steps in this article are specific to public folder content requests.</span></span> <span data-ttu-id="bb93e-126">Informationen zum ermitteln, ob es sich bei Ihrer Anforderung um eine Hierarchie Öffentlicher Ordner oder eine Inhaltsanforderung handelt, finden Sie unter [Routing Public Folder Requests](public-folder-access-with-ews-in-exchange.md#bk_routing).</span><span class="sxs-lookup"><span data-stu-id="bb93e-126">To determine whether your request is a public folder hierarchy or content request, see [Routing public folder requests](public-folder-access-with-ews-in-exchange.md#bk_routing).</span></span>

<span data-ttu-id="bb93e-127"><a name="bk_determineguidewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="bb93e-127"><a name="bk_determineguidewsma"> </a></span></span>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-the-ews-managed-api"></a><span data-ttu-id="bb93e-128">Ermitteln der GUID des Postfachs für Öffentliche Ordner mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="bb93e-128">Determine the GUID of the public folder mailbox by using the EWS Managed API</span></span>


<span data-ttu-id="bb93e-129">Um die GUID des Inhalts Postfachs für Öffentliche Ordner zu ermitteln, verwenden Sie das folgende Codebeispiel, das Folgendes ausführt:</span><span class="sxs-lookup"><span data-stu-id="bb93e-129">To determine the GUID of the public folder content mailbox, use the following code example, which does the following:</span></span> 
  
- <span data-ttu-id="bb93e-130">Verwendet die Überschriften **x-AnchorMailbox** und **x-PublicFolderInformation** , die Sie durch das [Routing von Hierarchie Anforderungen für Öffentliche Ordner](how-to-route-public-folder-hierarchy-requests.md)abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="bb93e-130">Uses the **X-AnchorMailbox** and **X-PublicFolderInformation** headers you retrieved by [routing public folder hierarchy requests](how-to-route-public-folder-hierarchy-requests.md).</span></span>
    
- <span data-ttu-id="bb93e-131">Ruft die verwaltete EWS-API [FindFolders](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) -Methode auf und enthält eine Anforderung für die **PR_REPLICA_LIST** (0x66980102)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bb93e-131">Calls the EWS Managed API [FindFolders](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) method, and includes a request for the **PR_REPLICA_LIST** (0x66980102) property</span></span> 
    
<span data-ttu-id="bb93e-132">Der **PR_REPLICA_LIST** Wert identifiziert die Postfach-GUID des Postfachs für Öffentliche Ordner mit dem Inhalt des Ordners.</span><span class="sxs-lookup"><span data-stu-id="bb93e-132">The **PR_REPLICA_LIST** value identifies the mailbox GUID of the public folder mailbox that has the content for the folder.</span></span> <span data-ttu-id="bb93e-133">Die **PR_REPLICA_LIST** -Eigenschaft ist ein Byte-Array, wird jedoch als GUID für dieses Szenario umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="bb93e-133">The **PR_REPLICA_LIST** property is a byte array, but is cast as a GUID for this scenario.</span></span> <span data-ttu-id="bb93e-134">Die GUID und der Domänenname werden verkettet, um die Adresse zu bilden, für die die AutoErmittlung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bb93e-134">The GUID and the domain name are concatenated to form the address on which to call Autodiscover.</span></span> 
  
<span data-ttu-id="bb93e-135">In diesem Beispiel wird davon ausgegangen, dass das `service` [Datei "ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Postfachbenutzer `PFHAnchorHeader` und `PFHMailboxHeader` die Werte der **x-AnchorMailbox** -und **x-PublicFolderMailbox-** Kopfzeilen und Domäne der vom Mandanten verwendete Domänenname ist.</span><span class="sxs-lookup"><span data-stu-id="bb93e-135">This example assumes that  `service` is the [ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox user,  `PFHAnchorHeader` and  `PFHMailboxHeader` are the values of the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers, and domain is the domain name used by the tenant.</span></span> 
  
```cs
public static string GetMailboxGuidAddress(ExchangeService service, String PFHAnchorHeader, String PFHMailboxHeader, String domain)
{
    // Create a new folder view, and pass in the maximum number of folders to return.
    FolderView view = new FolderView(10);
    // Create an extended property definition for the PR_REPLICA_LIST property.
    ExtendedPropertyDefinition PR_REPLICA_LIST = new ExtendedPropertyDefinition(0x6698, MapiPropertyType.Binary);
    // As a best practice, limit the properties returned to only those required.
    // In this case, return the folder ID, the folder display name, and 
    // the value of the PR_REPLICA_LIST extended property definition.
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.DisplayName, PR_REPLICA_LIST);
    service.HttpHeaders.Add("X-AnchorMailbox", PFHAnchorHeader);
    service.HttpHeaders.Add("X-PublicFolderMailbox", PFHMailboxHeader);
    // Add a call to the CertificateValidationCallback method here if needed.
    // ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;
    // Call FindFolders to retrieve the folder hierarchy, starting with the PublicFolderRoot folder.
    // This method call results in a FindFolder call to EWS.
    FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.PublicFoldersRoot, view);
    string GuidAsString = null;
    List<string> Guids = new List<string>();
    // For each folder under the root, display the name, and copy the value of the 
    // PR_REPLICA_LIST byte array to a string value. 
    foreach (Folder folder in findResults.Folders)
    {
        Console.WriteLine("Public folder display name: {0}", folder.DisplayName);
        byte[] ByteArr = (byte[])folder.ExtendedProperties[0].Value;
        GuidAsString = System.Text.Encoding.ASCII.GetString(ByteArr, 0, 36);
        Guids.Add(GuidAsString);
        Console.WriteLine("Address for Autodiscover: {0}.{1}\r\n", GuidAsString, domain);
    }
    // Concatenate the GUID value of the PR_REPLICA_LIST with the domain name to generate the 
    // SMTP address to use for the AutoDiscover request for the public folder content mailbox.
    string AutoDSMTPAddress = GuidAsString + "@" + domain;
    // Check that all folders have the same GUID value. If they do not, use the GUID value of the
    // folder that you're requesting content for.
    string commonGuid = CompareGuidsForEquality(Guids);
    if (commonGuid == "Not Equal")
    {
        Console.WriteLine("The GUIDs for all the folders in the hierarchy are not the same. Run the Autodiscover sample using the address returned above that is associated with the folder in your hierarchy request.", AutoDSMTPAddress);
        return null;
    }
    else
    {
        Console.WriteLine("The GUIDs for all public folders in the hierarchy are the same. Run the Autodiscover sample using the {0} address.", AutoDSMTPAddress);
        return AutoDSMTPAddress;
    }
}
// Method to compare the GUID for each folder under the public folder root.
// If each GUID is the same, return the GUID.
// If the GUIDs are not the same, return "Not equal".
public static string CompareGuidsForEquality(List<string> list)
{
    string NotEqual = "Not equal";
    string first = list.First();
    return list.All(x => x == first) ? first : NotEqual;
}
```

<span data-ttu-id="bb93e-136">Wenn die Fehlermeldung "die Anforderung ist fehlgeschlagen" angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="bb93e-136">If you received the error "The request failed.</span></span> <span data-ttu-id="bb93e-137">Die zugrunde liegende Verbindung wurde geschlossen: für den sicheren SSL/TLS-Kanal konnte keine Vertrauensstellung hergestellt werden ", müssen Sie einen [Aufruf an eine Validierungsrückruf Methode hinzufügen](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="bb93e-137">The underlying connection was closed: Could not establish trust relationship for the SSL/TLS secure channel", you'll need to [add a call to a validation callback method](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span> <span data-ttu-id="bb93e-138">Im Codebeispiel ist ein Platzhalter und ein Kommentar für diese Methode enthalten.</span><span class="sxs-lookup"><span data-stu-id="bb93e-138">A placeholder and comment for that method is included in the code example.</span></span>
  
<span data-ttu-id="bb93e-139">Wenn die Postfach-GUID für alle öffentlichen Ordner unter dem Stamm des öffentlichen Ordners identisch ist, gibt das Beispiel die Adresse an, die beim [Aufruf der AutoErmittlung](#bk_makeautodrequest) in der Konsolenausgabe und als Rückgabewert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb93e-139">If the mailbox GUID is the same for all the public folders under the public folder root, the example indicates the address to use when [calling Autodiscover](#bk_makeautodrequest) in the console output and as the return value.</span></span> <span data-ttu-id="bb93e-140">Wenn die Postfach-GUID nicht für alle öffentlichen Ordner unter dem Stamm des öffentlichen Ordners identisch ist, müssen Sie [eine Auto Ermittlungsanforderung](#bk_makeautodrequest) für die Adresse vornehmen, die dem Ordner in ihrer Inhaltsanforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bb93e-140">If the mailbox GUID is not the same for all public folders under the public folder root, you need to [Make an Autodiscover request](#bk_makeautodrequest) on the address associated with the folder in your content request.</span></span> 

<span data-ttu-id="bb93e-141"><a name="bk_determineguidews"> </a></span><span class="sxs-lookup"><span data-stu-id="bb93e-141"><a name="bk_determineguidews"> </a></span></span>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-ews"></a><span data-ttu-id="bb93e-142">Ermitteln der GUID des Postfachs für Öffentliche Ordner mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="bb93e-142">Determine the GUID of the public folder mailbox by using EWS</span></span>

<span data-ttu-id="bb93e-143">Im folgenden Codebeispiel wird veranschaulicht, wie der Wert der **PR_REPLICA_LIST** -Eigenschaft (0x66980102) mithilfe der EWS- [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) -Operation abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bb93e-143">The following code example shows how retrieve the value of the **PR_REPLICA_LIST** (0x66980102) property by using the EWS [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="bb93e-144">Für das [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) -Element wird das **PropertyTag** -Attribut auf den Dezimalwert (26264) der **PR_REPLICA_LIST** -Eigenschaft festgelegt, und das **PropertyType-** Attribut ist auf **Binary**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bb93e-144">For the [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element, the **PropertyTag** attribute is set to the decimal value (26264) of the **PR_REPLICA_LIST** property, and the **PropertyType** attribute is set to **Binary**.</span></span>
  
<span data-ttu-id="bb93e-145">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die [GUID des Postfachs für Öffentliche Ordner mithilfe der verwaltete EWS-API](#bk_determineguidewsma)mithilfe der **FindFolders** -Methode ermitteln.</span><span class="sxs-lookup"><span data-stu-id="bb93e-145">This is also the XML request that the EWS Managed API sends when you use the **FindFolders** method to [determine the GUID of the public folder mailbox by using the EWS Managed API](#bk_determineguidewsma).</span></span>
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0913.015
Accept-Encoding: gzip,deflate
Authorization: Basic c29ueWFmQGNvbnRvc28xMDAwLm9ubWljcm9zb2Z0LmNvbTpFWENIIzIwMTQ=
Host: outlook.office365.com
Cookie: ClientId=KZPBLKA9ZMPXAQDW
Content-Length: 1005
Expect: 100-continue
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Shallow">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:DisplayName" />
          <t:ExtendedFieldURI PropertyTag="26264" PropertyType="Binary" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="publicfoldersroot" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="bb93e-146">Der Server antwortet auf die **FindFolder** -Anforderung mit einer [FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) -Nachricht, die den Wert der **PR_REPLICA_LIST** erweiterten Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="bb93e-146">The server responds to the **FindFolder** request with a [FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) message that includes the value of the **PR_REPLICA_LIST** extended property.</span></span> <span data-ttu-id="bb93e-147">Beachten Sie, dass der Wert der Eigenschaft in der EWS-Antwort als Zeichenfolgenformat eines codierten Base-64-Bytearrays angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bb93e-147">Note that the value of the property appears on the EWS response as the string format of a base-64 encoded byte array.</span></span> <span data-ttu-id="bb93e-148">Einige Headerwerte in der Antwort werden zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="bb93e-148">Some header values in the response are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="1019" MinorBuildNumber="15" Version="V2_17" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body>
    <m:FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="2" TotalItemsInView="2" IncludesLastItemInRange="true">
            <t:Folders>
              <t:ContactsFolder>
                <t:FolderId Id="AAEuAAAAAADL8shaNEKnQYVvRbpoY9vDAQBGDloItRzyTrAt+XVzRr/YAABdofPkAAA=" ChangeKey="AwAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/2h"/>
                <t:DisplayName>My Public Contacts</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x6698" PropertyType="Binary"/>
                  <t:Value>MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:Folder>
                <t:FolderId Id="AQEuAAADy/LIWjRCp0GFb0W6aGPbwwEARg5aCLUc8k6wLfl1c0a/2AAAAxEAAAA=" ChangeKey="AQAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/W/"/>
                <t:DisplayName>SampleFolder</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x6698" PropertyType="Binary"/>
                  <t:Value>MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </m:FindFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="bb93e-149">Um den Wert der in XML, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA = = zurückgegebenen **PR_REPLICA_LIST** zu verwenden, um die Postfach-GUID zu ermitteln, muss der Wert in eine GUID in einem Format konvertiert werden, das dem entspricht, wie der Wert im [verwaltete EWS-API Codebeispiel](#bk_determineguidewsma)konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="bb93e-149">In order to use the value of the **PR_REPLICA_LIST** returned in the XML, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==, to determine the mailbox GUID, the value must be converted into a GUID in a format similar to how the value is converted in the [EWS Managed API code example](#bk_determineguidewsma).</span></span> <span data-ttu-id="bb93e-150">Die GUID wird dann mit dem Domänennamen verkettet, um eine SMTP-Adresse zu erstellen, die in der [Auto Ermittlungsanforderung](#bk_makeautodrequest)enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="bb93e-150">The GUID is then concatenated with the domain name to create an SMTP address, which is included in the [Autodiscover request](#bk_makeautodrequest).</span></span>
  
## <a name="make-an-autodiscover-request"></a><span data-ttu-id="bb93e-151">Erstellen einer Auto Ermittlungsanforderung</span><span class="sxs-lookup"><span data-stu-id="bb93e-151">Make an Autodiscover request</span></span>
<span data-ttu-id="bb93e-152"><a name="bk_makeautodrequest"> </a></span><span class="sxs-lookup"><span data-stu-id="bb93e-152"><a name="bk_makeautodrequest"> </a></span></span>

<span data-ttu-id="bb93e-153">Verwenden Sie die von der Methode zurückgegebene Adresse `GetMailboxGuidAddress` , um die AutoErmittlung aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="bb93e-153">Use the address returned by the  `GetMailboxGuidAddress` method to call Autodiscover.</span></span> <span data-ttu-id="bb93e-154">Es wird empfohlen, die Exchange 2013 zu verwenden [: Abrufen von Benutzereinstellungen mit der Auto](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) Ermittlungs Code-Beispiel, um den AutoErmittlungsdienst aufzurufen, da dadurch der Auto Ermittlungsprozess rationalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="bb93e-154">We recommend that you use the [Exchange 2013: Get user settings with Autodiscover](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) code sample to call the Autodiscover service because it streamlines the Autodiscover process for you.</span></span> <span data-ttu-id="bb93e-155">In diesem Codebeispiel werden die in der folgenden Tabelle aufgelisteten Befehlszeilenargumente verwendet, um den POX-AutoErmittlungsdienst aufzurufen, um den [AutoDiscoverSMTPAddress](https://msdn.microsoft.com/library/office/dn750991%28v=exchg.150%29.aspx) -Wert abzurufen, der der Postfach-GUID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bb93e-155">This code sample uses the command-line arguments listed in the following table to call the POX Autodiscover service to retrieve the [AutoDiscoverSMTPAddress](https://msdn.microsoft.com/library/office/dn750991%28v=exchg.150%29.aspx) value associated with the mailbox GUID.</span></span> 

  
|<span data-ttu-id="bb93e-156">**Argument**</span><span class="sxs-lookup"><span data-stu-id="bb93e-156">**Argument**</span></span>|<span data-ttu-id="bb93e-157">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb93e-157">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb93e-158">emailAddress</span><span class="sxs-lookup"><span data-stu-id="bb93e-158">emailAddress</span></span>  <br/> |<span data-ttu-id="bb93e-159">Die von der Methode zurückgegebene Adresse `GetMailboxGuidAddress` [bestimmen Sie die GUID des Postfachs für Öffentliche Ordner](#bk_determineguidewsma).</span><span class="sxs-lookup"><span data-stu-id="bb93e-159">The address returned by the  `GetMailboxGuidAddress` method in [Determine the GUID of the public folder mailbox](#bk_determineguidewsma).</span></span>  <br/> |
|<span data-ttu-id="bb93e-160">-skipSOAP</span><span class="sxs-lookup"><span data-stu-id="bb93e-160">-skipSOAP</span></span>  <br/> |<span data-ttu-id="bb93e-161">Gibt an, dass POX-Auto Ermittlungsanforderungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="bb93e-161">Indicates that POX Autodiscover requests are required.</span></span>  <br/> |
|<span data-ttu-id="bb93e-162">-auth authEmailAddress</span><span class="sxs-lookup"><span data-stu-id="bb93e-162">-auth authEmailAddress</span></span>  <br/> |<span data-ttu-id="bb93e-163">Die e-Mail-Adresse des Postfachbenutzers, die für die Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb93e-163">The mailbox user's email address, which is used for authentication.</span></span> <span data-ttu-id="bb93e-164">Sie werden aufgefordert, das Kennwort des Postfachbenutzers einzugeben, wenn Sie das Beispiel ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb93e-164">You will be prompted to enter the mailbox user's password when you run the sample.</span></span>  <br/> |
   
<span data-ttu-id="bb93e-165">Beispielsweise sollten die Befehlszeilenargumente wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="bb93e-165">For example, the command-line arguments should look like this:</span></span>
  
`1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com -skipSOAP -auth sonyaf@contoso.com`

<span data-ttu-id="bb93e-166">Hierbei `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` handelt es sich um die von der **GetMailboxGuidAddress** -Methode zurückgegebene Adresse und `sonyaf@contoso.com` um den Postfachbenutzer.</span><span class="sxs-lookup"><span data-stu-id="bb93e-166">Where `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` is the address returned by the **GetMailboxGuidAddress** method, and `sonyaf@contoso.com` is the mailbox user.</span></span> 
  
<span data-ttu-id="bb93e-167">Wenn Sie das **Exchange 2013: Abrufen von Benutzereinstellungen mit dem Auto Ermittlungs** Beispiel ausführen, sollte die letzte Antwort auf die AutoErmittlung erfolgreich sein und alle Benutzereinstellungen einschließen, die der Postfach-GUID zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bb93e-167">When you run the **Exchange 2013: Get user settings with Autodiscover** sample, the last Autodiscover response should be successful and include all the user settings associated with the mailbox GUID.</span></span> <span data-ttu-id="bb93e-168">Speichern Sie die **AutoDiscoverSMTPAddress** -Benutzereinstellung lokal, wie Sie dies im nächsten Schritt verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="bb93e-168">Save the **AutoDiscoverSMTPAddress** user setting locally, as you'll use that in the next step.</span></span> 
  
<span data-ttu-id="bb93e-169">Wenn Sie **Exchange 2013: Abrufen von Benutzereinstellungen mit Auto Ermittlungs** Beispiel verwenden möchten, können Sie die **AutoDiscoverSMTPAddress** -Benutzereinstellung abrufen, indem Sie [eine Liste der Auto Ermittlungs Endpunkte generieren](how-to-generate-a-list-of-autodiscover-endpoints.md)und dann die folgende POX-Auto Ermittlungsanforderung an jede URL senden, bis Sie eine erfolgreiche Antwort erhalten.</span><span class="sxs-lookup"><span data-stu-id="bb93e-169">Alternatively, if you do not want to use **Exchange 2013: Get user settings with Autodiscover** sample, you can get the **AutoDiscoverSMTPAddress** user setting by [generating a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and then sending the following POX Autodiscover request to each URL until you receive a successful response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

<span data-ttu-id="bb93e-170">Weitere Informationen zum Auto Ermittlungsprozess finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md), [Generieren einer Liste mit Auto Ermittlungs Endpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md)und [Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="bb93e-170">For more information about the Autodiscover process, see [Autodiscover for Exchange](autodiscover-for-exchange.md), [Generate a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span></span>
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a><span data-ttu-id="bb93e-171">Festlegen der Werte der x-AnchorMailbox-und x-PublicFolderMailbox-Kopfzeilen</span><span class="sxs-lookup"><span data-stu-id="bb93e-171">Set the values of the X-AnchorMailbox and X-PublicFolderMailbox headers</span></span>
<span data-ttu-id="bb93e-172"><a name="bk_setheadervalues"> </a></span><span class="sxs-lookup"><span data-stu-id="bb93e-172"><a name="bk_setheadervalues"> </a></span></span>

<span data-ttu-id="bb93e-173">Legen Sie mithilfe des Werts für das **AutoDiscoverSMTPAddress** , das in [make a Auto Ermittlungsanforderung](#bk_makeautodrequest)erworben wurde, die Werte der Header **x-AnchorMailbox** und **x-PublicFolderMailbox** in der Inhaltsanforderung für Öffentliche Ordner fest.</span><span class="sxs-lookup"><span data-stu-id="bb93e-173">Using the value for the **AutoDiscoverSMTPAddress** acquired in [Make an Autodiscover request](#bk_makeautodrequest), set the values of the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers in your public folder content request.</span></span> 
  
<span data-ttu-id="bb93e-174">Geben Sie beispielsweise bei einer AutoDiscoverSMTPAddress von NewPublicFolder@contoso.com die folgenden Kopfzeilen ein, wenn Sie Aufrufe an die folgenden Methoden oder Vorgänge vornehmen.</span><span class="sxs-lookup"><span data-stu-id="bb93e-174">For example, given an AutoDiscoverSMTPAddress of NewPublicFolder@contoso.com, include the following headers when making calls to the following methods or operations.</span></span>
  
`X-AnchorMailbox: NewPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: NewPublicFolder@contoso.com`

<span data-ttu-id="bb93e-175">**Öffentliche Ordner-Aufrufe, die die Header x-AncorMailbox und x-PublicFolder erfordern**</span><span class="sxs-lookup"><span data-stu-id="bb93e-175">**Public folder calls that require the X-AncorMailbox and X-PublicFolder headers**</span></span>

|<span data-ttu-id="bb93e-176">**EWS Managed API-Methoden**</span><span class="sxs-lookup"><span data-stu-id="bb93e-176">**EWS Managed API methods**</span></span>|<span data-ttu-id="bb93e-177">**EWS-Operationen**</span><span class="sxs-lookup"><span data-stu-id="bb93e-177">**EWS operations**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb93e-178">Item.Bind</span><span class="sxs-lookup"><span data-stu-id="bb93e-178">Item.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="bb93e-179">Item.Update</span><span class="sxs-lookup"><span data-stu-id="bb93e-179">Item.Update</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="bb93e-180">Item.Copy</span><span class="sxs-lookup"><span data-stu-id="bb93e-180">Item.Copy</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="bb93e-181">Item.Move</span><span class="sxs-lookup"><span data-stu-id="bb93e-181">Item.Move</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="bb93e-182">Item.Delete</span><span class="sxs-lookup"><span data-stu-id="bb93e-182">Item.Delete</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="bb93e-183">Folder.Bind</span><span class="sxs-lookup"><span data-stu-id="bb93e-183">Folder.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="bb93e-184">Folder.FindItems</span><span class="sxs-lookup"><span data-stu-id="bb93e-184">Folder.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="bb93e-185">CreateItem</span><span class="sxs-lookup"><span data-stu-id="bb93e-185">CreateItem</span></span>](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [<span data-ttu-id="bb93e-186">GetItem</span><span class="sxs-lookup"><span data-stu-id="bb93e-186">GetItem</span></span>](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [<span data-ttu-id="bb93e-187">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="bb93e-187">UpdateItem</span></span>](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [<span data-ttu-id="bb93e-188">CopyItem</span><span class="sxs-lookup"><span data-stu-id="bb93e-188">CopyItem</span></span>](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [<span data-ttu-id="bb93e-189">MoveItem</span><span class="sxs-lookup"><span data-stu-id="bb93e-189">MoveItem</span></span>](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [<span data-ttu-id="bb93e-190">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="bb93e-190">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> [<span data-ttu-id="bb93e-191">GetFolder</span><span class="sxs-lookup"><span data-stu-id="bb93e-191">GetFolder</span></span>](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [<span data-ttu-id="bb93e-192">FindItem</span><span class="sxs-lookup"><span data-stu-id="bb93e-192">FindItem</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="bb93e-193">Verwenden Sie die [httpheaders-. Add](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) -Methode, um diese Header mithilfe der verwaltete EWS-API hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bb93e-193">To add these headers by using the EWS Managed API, use the [HttpHeaders.Add](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) method.</span></span> 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "NewPublicFolder@contoso.com");
service.HttpHeaders.Add("X-PublicFolderMailbox", "NewPublicFolder@contoso.com");
```

<span data-ttu-id="bb93e-194">Der folgende Code zeigt eine [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) -Anforderung, bei der der **x-AnchorMailbox** -und der **x-PublicFolderMailbox-** Header auf die in den Beispielen in diesem Artikel abgerufenen Werte festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="bb93e-194">The following code shows a [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request with the **X-AnchorMailbox** and **X-PublicFolderMailbox** header set to the values retrieved in the examples in this article.</span></span> 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
User-Agent: SoapSender1.0
X-AnchorMailbox: NewPublicFolder@contoso.com
X-PublicFolderMailbox: NewPublicFolder@contoso.com
Authorization: Basic c29ueWFmQGNvbnRvc28xMDAwLm9ubWljcm9zb2Z0LmNvbTpFWENIIzIwMTQ=
Host: outlook.office365.com
Content-Length: 688
Expect: 100-continue
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="publicfoldersroot" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="bb93e-195">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb93e-195">See also</span></span>

- [<span data-ttu-id="bb93e-196">Zugriff auf Öffentliche Ordner mit EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="bb93e-196">Public folder access with EWS in Exchange</span></span>](public-folder-access-with-ews-in-exchange.md)    
- [<span data-ttu-id="bb93e-197">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="bb93e-197">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)    
- [<span data-ttu-id="bb93e-198">Generieren einer Liste mit AutoErmittlungs-Endpunkten</span><span class="sxs-lookup"><span data-stu-id="bb93e-198">Generate a list of Autodiscover endpoints</span></span>](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [<span data-ttu-id="bb93e-199">Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="bb93e-199">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
  