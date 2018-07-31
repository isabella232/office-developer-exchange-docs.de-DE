---
title: Weiterleiten von Anforderungen für Inhalte öffentlicher Ordner
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 59d2f05e-90fb-471e-ac06-70becc15b295
description: Alle Anfragen für Öffentliche Ordnerinformationen, die den Inhalt der öffentlichen Ordner müssen an das Postfach für Öffentliche Ordner weitergeleitet werden betreffen, die den Inhalt für den Zielordner enthält. Um die Anforderungen an dieses Postfach weiterleiten möchten, müssen Sie die X-AnchorMailbox und X-PublicFolderMailbox-Header auf bestimmte Werte festgelegt.
ms.openlocfilehash: 64fafecb9882b17a3394e54640df78f7aa180343
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354022"
---
# <a name="route-public-folder-content-requests"></a><span data-ttu-id="e62c2-104">Weiterleiten von Anforderungen für Inhalte öffentlicher Ordner</span><span class="sxs-lookup"><span data-stu-id="e62c2-104">Route public folder content requests</span></span>

<span data-ttu-id="e62c2-105">Alle Anfragen für Öffentliche Ordnerinformationen, die den Inhalt der öffentlichen Ordner müssen an das Postfach für Öffentliche Ordner weitergeleitet werden betreffen, die den Inhalt für den Zielordner enthält.</span><span class="sxs-lookup"><span data-stu-id="e62c2-105">All requests for public folder information that involve the content of the public folder need to be routed to the public folder mailbox that holds the content for the target folder.</span></span> <span data-ttu-id="e62c2-106">Um die Anforderungen an dieses Postfach weiterleiten möchten, müssen Sie die **X-AnchorMailbox** und **X-PublicFolderMailbox-** Header auf bestimmte Werte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e62c2-106">To route the requests to that mailbox, you need to set the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers to specific values.</span></span> 
  
<span data-ttu-id="e62c2-107">Die folgende Tabelle enthält eine Übersicht über den Prozess:</span><span class="sxs-lookup"><span data-stu-id="e62c2-107">The following table provides an overview of the process:</span></span>
  
<span data-ttu-id="e62c2-108">**Übersicht über die Öffentliche Ordner**</span><span class="sxs-lookup"><span data-stu-id="e62c2-108">**Public folder overview**</span></span>

|<span data-ttu-id="e62c2-109">Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="e62c2-109">Header</span></span>|<span data-ttu-id="e62c2-110">Was muss ich?</span><span class="sxs-lookup"><span data-stu-id="e62c2-110">What do I need?</span></span>|<span data-ttu-id="e62c2-111">Wie erhalte ich es?</span><span class="sxs-lookup"><span data-stu-id="e62c2-111">How do I get it?</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e62c2-112">**X-AnchorMailbox**</span><span class="sxs-lookup"><span data-stu-id="e62c2-112">**X-AnchorMailbox**</span></span> <br/> |<span data-ttu-id="e62c2-113">1. [die X-AnchorMailbox und X PublicFolderInformation Werte](how-to-route-public-folder-hierarchy-requests.md) für das Postfach für Öffentliche Ordner-Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="e62c2-113">1. [The X-AnchorMailbox and X-PublicFolderInformation values ](how-to-route-public-folder-hierarchy-requests.md) for the public folder hierarchy mailbox.</span></span><br/><br/><span data-ttu-id="e62c2-114">2. die GUID des Postfachs für Öffentliche Ordner, die den Inhalt von Postfächern enthält, die mit dem AutoErmittlungsdienst gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e62c2-114">2. The GUID of the public folder mailbox that contains the mailbox content, which is sent to the Autodiscover service.</span></span><br/><br/>  <span data-ttu-id="e62c2-115">Die **AutoDiscoverSMTPAddress** in der Antwort Autodisover wird der Wert der **X-AnchorMailbox** Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="e62c2-115">The **AutoDiscoverSMTPAddress** in the Autodisover response becomes the value of the **X-AnchorMailbox** header.</span></span>  <br/> <span data-ttu-id="e62c2-116">![AUFGABEN](media/Ex15_PF_PFContent.png)</span><span class="sxs-lookup"><span data-stu-id="e62c2-116">![TODO](media/Ex15_PF_PFContent.png)</span></span>| <span data-ttu-id="e62c2-117">1. verwenden Sie das Codebeispiel in diesem Artikel [implementiert die EWS Managed API](#bk_determineguidewsma).</span><span class="sxs-lookup"><span data-stu-id="e62c2-117">1. Use the code example in this article, which [implements the EWS Managed API](#bk_determineguidewsma).</span></span> <span data-ttu-id="e62c2-118">Oder [Verwenden von EWS](#bk_determineguidews) und konvertieren Sie Ihre Ergebnisse, um eine GUID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e62c2-118">Or [use EWS](#bk_determineguidews) and convert your results to obtain a GUID.</span></span><br/><br/><span data-ttu-id="e62c2-119">2. [eine Anforderung für die AutoErmittlung](#bk_makeautodrequest) , über die GUID und der Domänenname.</span><span class="sxs-lookup"><span data-stu-id="e62c2-119">2. [Make an Autodiscover request](#bk_makeautodrequest) by using the GUID plus the domain name.</span></span><br/><br/><span data-ttu-id="e62c2-120">3. verwenden Sie den Wert des **AutoDiscoverSMTPAddress** -Elements in der Antwort der AutoErmittlung zum [Auffüllen des Werts der Header](#bk_setheadervalues)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e62c2-120">3. Use the value of the **AutoDiscoverSMTPAddress** element returned in the Autodiscover response to [populate the value of the headers](#bk_setheadervalues).</span></span>  <br/> |
|<span data-ttu-id="e62c2-121">**X-PublicFolderMailbox**</span><span class="sxs-lookup"><span data-stu-id="e62c2-121">**X-PublicFolderMailbox**</span></span> <br/> |<span data-ttu-id="e62c2-122">Ihre Arbeit erfolgt, der X-PublicFolderMailbox-Wert entspricht dem Wert der X-AnchorMailbox!</span><span class="sxs-lookup"><span data-stu-id="e62c2-122">Your work is done, the X-PublicFolderMailbox value is the same as the X-AnchorMailbox value!</span></span>  <br/> |<span data-ttu-id="e62c2-123">Sie haben bereits es!</span><span class="sxs-lookup"><span data-stu-id="e62c2-123">You already have it!</span></span>  <br/> |
   
<span data-ttu-id="e62c2-124">Nachdem Sie die Werte für die Kopfzeile festgelegt haben, können Sie diese, [Wenn Sie Öffentliche Ordner-inhaltsanforderungen vornehmen](#bk_setheadervalues).</span><span class="sxs-lookup"><span data-stu-id="e62c2-124">After you have determined the header values, include them [when you make public folder content requests](#bk_setheadervalues).</span></span>
  
<span data-ttu-id="e62c2-125">Die Schritte in diesem Artikel sind spezifisch für Öffentliche Ordner-inhaltsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="e62c2-125">The steps in this article are specific to public folder content requests.</span></span> <span data-ttu-id="e62c2-126">Um festzustellen, ob es sich bei Ihrer Anforderung einer Hierarchie Öffentlicher Ordner oder Content Anforderung ist, finden Sie unter [Routing für Öffentliche Ordner-Anfragen](public-folder-access-with-ews-in-exchange.md#bk_routing).</span><span class="sxs-lookup"><span data-stu-id="e62c2-126">To determine whether your request is a public folder hierarchy or content request, see [Routing public folder requests](public-folder-access-with-ews-in-exchange.md#bk_routing).</span></span>

<span data-ttu-id="e62c2-127"><a name="bk_determineguidewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e62c2-127"></span></span>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-the-ews-managed-api"></a><span data-ttu-id="e62c2-128">Bestimmen Sie die GUID des Postfachs für Öffentliche Ordner mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="e62c2-128">Determine the GUID of the public folder mailbox by using the EWS Managed API</span></span>


<span data-ttu-id="e62c2-129">Um die GUID des Postfachs für Öffentliche Ordner-Inhalt zu bestimmen, verwenden Sie im folgenden Codebeispiel wird, die Folgendes ermöglicht:</span><span class="sxs-lookup"><span data-stu-id="e62c2-129">To determine the GUID of the public folder content mailbox, use the following code example, which does the following:</span></span> 
  
- <span data-ttu-id="e62c2-130">Verwendet die **X-AnchorMailbox** und **X PublicFolderInformation** Header, die Sie von [Öffentliche Ordner-Hierarchie Routinganforderungen](how-to-route-public-folder-hierarchy-requests.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e62c2-130">Uses the **X-AnchorMailbox** and **X-PublicFolderInformation** headers you retrieved by [routing public folder hierarchy requests](how-to-route-public-folder-hierarchy-requests.md).</span></span>
    
- <span data-ttu-id="e62c2-131">Die EWS Managed API [FindFolders](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) -Methode aufgerufen, und enthält eine Anforderung für die **PR_REPLICA_LIST** (0x66980102)-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e62c2-131">Calls the EWS Managed API [FindFolders](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) method, and includes a request for the **PR_REPLICA_LIST** (0x66980102) property</span></span> 
    
<span data-ttu-id="e62c2-132">Der Wert **PR_REPLICA_LIST** identifiziert die Postfach-GUID des Postfachs für Öffentliche Ordner, die den Inhalt für den Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="e62c2-132">The **PR_REPLICA_LIST** value identifies the mailbox GUID of the public folder mailbox that has the content for the folder.</span></span> <span data-ttu-id="e62c2-133">Die **PR_REPLICA_LIST** -Eigenschaft ist ein Bytearray, aber für dieses Szenario als GUID umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="e62c2-133">The **PR_REPLICA_LIST** property is a byte array, but is cast as a GUID for this scenario.</span></span> <span data-ttu-id="e62c2-134">Die GUID und den Domänennamen werden verkettet, um die Adresse an, die für die AutoErmittlung aufrufen bilden.</span><span class="sxs-lookup"><span data-stu-id="e62c2-134">The GUID and the domain name are concatenated to form the address on which to call Autodiscover.</span></span> 
  
<span data-ttu-id="e62c2-135">In diesem Beispiel wird vorausgesetzt, dass `service` ist das [ExchangeService](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Postfachbenutzer `PFHAnchorHeader` und `PFHMailboxHeader` sind die Werte der **X-AnchorMailbox** und **X-PublicFolderMailbox** Header und Domäne ist der Domänenname wird von verwendet die Mandanten.</span><span class="sxs-lookup"><span data-stu-id="e62c2-135">This example assumes that  `service` is the [ExchangeService](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox user,  `PFHAnchorHeader` and  `PFHMailboxHeader` are the values of the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers, and domain is the domain name used by the tenant.</span></span> 
  
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

<span data-ttu-id="e62c2-136">Wenn Sie die Fehlermeldung "die Anforderung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="e62c2-136">If you received the error "The request failed.</span></span> <span data-ttu-id="e62c2-137">Die zugrunde liegende Verbindung wurde geschlossen: Vertrauensstellung für den geschützten SSL/TLS-Kanal konnte nicht hergestellt werden ", müssen Sie [einen Anruf an eine Rückrufmethode Validierung hinzufügen](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="e62c2-137">The underlying connection was closed: Could not establish trust relationship for the SSL/TLS secure channel", you'll need to [add a call to a validation callback method](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span> <span data-ttu-id="e62c2-138">Einen Platzhalter und einen Kommentar für diese Methode ist im Codebeispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="e62c2-138">A placeholder and comment for that method is included in the code example.</span></span>
  
<span data-ttu-id="e62c2-139">Wenn die Postfach-GUID für die öffentlichen Ordner unter dem Stammverzeichnis der öffentlichen Ordner identisch ist, gibt im Beispiel wird die Adresse zu verwenden, wenn in der Konsole [aufrufen AutoErmittlung](#bk_makeautodrequest) Ausgabe und als Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e62c2-139">If the mailbox GUID is the same for all the public folders under the public folder root, the example indicates the address to use when [calling Autodiscover](#bk_makeautodrequest) in the console output and as the return value.</span></span> <span data-ttu-id="e62c2-140">Wenn die Postfach-GUID nicht für alle öffentlichen Ordner unter dem Stammverzeichnis der Öffentliche Ordner ist, müssen Sie die Adresse, die dem Ordner in Ihrer Anforderung Content zugeordnet, [AutoErmittlung anzufordern](#bk_makeautodrequest) .</span><span class="sxs-lookup"><span data-stu-id="e62c2-140">If the mailbox GUID is not the same for all public folders under the public folder root, you need to [Make an Autodiscover request](#bk_makeautodrequest) on the address associated with the folder in your content request.</span></span> 

<span data-ttu-id="e62c2-141"><a name="bk_determineguidews"> </a></span><span class="sxs-lookup"><span data-stu-id="e62c2-141"></span></span>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-ews"></a><span data-ttu-id="e62c2-142">Bestimmen Sie die GUID des Postfachs für Öffentliche Ordner mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="e62c2-142">Determine the GUID of the public folder mailbox by using EWS</span></span>

<span data-ttu-id="e62c2-143">Im folgenden Code wird veranschaulicht abrufen wie den Wert der Eigenschaft **PR_REPLICA_LIST** (0x66980102) mit der EWS [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) -Operation.</span><span class="sxs-lookup"><span data-stu-id="e62c2-143">The following code example shows how retrieve the value of the **PR_REPLICA_LIST** (0x66980102) property by using the EWS [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="e62c2-144">Für das [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) -Element das Attribut **' PropertyTag '** auf den Dezimalwert (26264) der **PR_REPLICA_LIST** -Eigenschaft festgelegt ist, und das Attribut **PropertyType** auf **Binary**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e62c2-144">For the [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element, the **PropertyTag** attribute is set to the decimal value (26264) of the **PR_REPLICA_LIST** property, and the **PropertyType** attribute is set to **Binary**.</span></span>
  
<span data-ttu-id="e62c2-145">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **FindFolders** -Methode zum [Bestimmen der GUID des Postfachs für Öffentliche Ordner mithilfe der EWS Managed API](#bk_determineguidewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="e62c2-145">This is also the XML request that the EWS Managed API sends when you use the **FindFolders** method to [determine the GUID of the public folder mailbox by using the EWS Managed API](#bk_determineguidewsma).</span></span>
  
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
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="e62c2-146">Der Server antwortet auf die Anforderung **FindFolder** mit einer [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) -Meldung, die den Wert der erweiterten Eigenschaft **PR_REPLICA_LIST** enthält.</span><span class="sxs-lookup"><span data-stu-id="e62c2-146">The server responds to the **FindFolder** request with a [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) message that includes the value of the **PR_REPLICA_LIST** extended property.</span></span> <span data-ttu-id="e62c2-147">Beachten Sie, dass der Wert der Eigenschaft für die EWS-Antwort mit dem String-Format für eine Base64-codierte Bytearray zurück.</span><span class="sxs-lookup"><span data-stu-id="e62c2-147">Note that the value of the property appears on the EWS response as the string format of a base-64 encoded byte array.</span></span> <span data-ttu-id="e62c2-148">Einige Headerwerte in der Antwort werden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="e62c2-148">Some header values in the response are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="1019" MinorBuildNumber="15" Version="V2_17" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body>
    <m:FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="e62c2-149">In den XML-Code, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA, um den Wert der **PR_REPLICA_LIST** verwenden zurückgegeben ==, um die Postfach-GUID zu ermitteln, muss der Wert in einer GUID in einem Format ähnlich wie in der Wert umgewandelt wird konvertiert werden die [EWS Managed API-Codebeispiel](#bk_determineguidewsma).</span><span class="sxs-lookup"><span data-stu-id="e62c2-149">In order to use the value of the **PR_REPLICA_LIST** returned in the XML, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==, to determine the mailbox GUID, the value must be converted into a GUID in a format similar to how the value is converted in the [EWS Managed API code example](#bk_determineguidewsma).</span></span> <span data-ttu-id="e62c2-150">Die GUID wird dann verkettet wird mit dem Domänennamen, erstellen Sie eine SMTP-Adresse, die in der [Anforderung der AutoErmittlung](#bk_makeautodrequest)enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e62c2-150">The GUID is then concatenated with the domain name to create an SMTP address, which is included in the [Autodiscover request](#bk_makeautodrequest).</span></span>
  
## <a name="make-an-autodiscover-request"></a><span data-ttu-id="e62c2-151">Stellen Sie eine autoermittlungsanforderung für die</span><span class="sxs-lookup"><span data-stu-id="e62c2-151">Make an Autodiscover request</span></span>
<span data-ttu-id="e62c2-152"><a name="bk_makeautodrequest"> </a></span><span class="sxs-lookup"><span data-stu-id="e62c2-152"></span></span>

<span data-ttu-id="e62c2-153">Verwenden Sie die Adresse zurückgegeben, indem die `GetMailboxGuidAddress` Methode, die für die AutoErmittlung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e62c2-153">Use the address returned by the  `GetMailboxGuidAddress` method to call Autodiscover.</span></span> <span data-ttu-id="e62c2-154">Wir empfehlen die Verwendung der [Exchange 2013: Abrufen von benutzereinstellungen für mit der AutoErmittlung](http://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) Codebeispiel den AutoErmittlungsdienst aufgerufen, da es die AutoErmittlung für Sie vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="e62c2-154">We recommend that you use the [Exchange 2013: Get user settings with Autodiscover](http://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) code sample to call the Autodiscover service because it streamlines the Autodiscover process for you.</span></span> <span data-ttu-id="e62c2-155">In diesem Codebeispiel verwendet die in der folgenden Tabelle aufgeführten Befehlszeilenargumente zum Aufrufen des POX AutoErmittlungsdiensts zum Abrufen des [AutoDiscoverSMTPAddress](http://msdn.microsoft.com/en-us/library/office/dn750991%28v=exchg.150%29.aspx) -Werts, der die Postfach-GUID zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e62c2-155">This code sample uses the command-line arguments listed in the following table to call the POX Autodiscover service to retrieve the [AutoDiscoverSMTPAddress](http://msdn.microsoft.com/en-us/library/office/dn750991%28v=exchg.150%29.aspx) value associated with the mailbox GUID.</span></span> 
  
|<span data-ttu-id="e62c2-156">**Argument**</span><span class="sxs-lookup"><span data-stu-id="e62c2-156">**Argument**</span></span>|<span data-ttu-id="e62c2-157">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e62c2-157">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e62c2-158">emailAddress</span><span class="sxs-lookup"><span data-stu-id="e62c2-158">emailAddress</span></span>  <br/> |<span data-ttu-id="e62c2-159">Die zurückgegebene Adresse der `GetMailboxGuidAddress` -Methode in [Determine die GUID des Postfachs für Öffentliche Ordner](#bk_determineguidewsma).</span><span class="sxs-lookup"><span data-stu-id="e62c2-159">The address returned by the  `GetMailboxGuidAddress` method in [Determine the GUID of the public folder mailbox](#bk_determineguidewsma).</span></span>  <br/> |
|<span data-ttu-id="e62c2-160">-skipSOAP</span><span class="sxs-lookup"><span data-stu-id="e62c2-160">-skipSOAP</span></span>  <br/> |<span data-ttu-id="e62c2-161">Gibt an, dass POX AutoErmittlung Anforderungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e62c2-161">Indicates that POX Autodiscover requests are required.</span></span>  <br/> |
|<span data-ttu-id="e62c2-162">-Auth authEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e62c2-162">-auth authEmailAddress</span></span>  <br/> |<span data-ttu-id="e62c2-163">Das des Postfachbenutzers e-Mail-Adresse, die für die Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e62c2-163">The mailbox user's email address, which is used for authentication.</span></span> <span data-ttu-id="e62c2-164">Sie werden aufgefordert, die beim Ausführen des Beispiels den Postfachbenutzer Kennwort eingeben.</span><span class="sxs-lookup"><span data-stu-id="e62c2-164">You will be prompted to enter the mailbox user's password when you run the sample.</span></span>  <br/> |
   
<span data-ttu-id="e62c2-165">Beispielsweise sollte die Befehlszeilenargumente wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="e62c2-165">For example, the command-line arguments should look like this:</span></span>
  
`1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com -skipSOAP -auth sonyaf@contoso.com`

<span data-ttu-id="e62c2-166">Wobei `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` ist die Adresse, die von der Methode **GetMailboxGuidAddress** zurückgegeben und `sonyaf@contoso.com` der Postfachbenutzer ist.</span><span class="sxs-lookup"><span data-stu-id="e62c2-166">Where `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` is the address returned by the **GetMailboxGuidAddress** method, and `sonyaf@contoso.com` is the mailbox user.</span></span> 
  
<span data-ttu-id="e62c2-167">Beim Ausführen der **Exchange 2013: Abrufen von benutzereinstellungen für mit der AutoErmittlung** Beispiel die letzte AutoErmittlung Antwort erfolgreich und umfassen sollten alle für die Benutzer die Postfach-GUID zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e62c2-167">When you run the **Exchange 2013: Get user settings with Autodiscover** sample, the last Autodiscover response should be successful and include all the user settings associated with the mailbox GUID.</span></span> <span data-ttu-id="e62c2-168">Speichern der **AutoDiscoverSMTPAddress** Benutzer lokal festlegen wie Sie, die im nächsten Schritt verwenden.</span><span class="sxs-lookup"><span data-stu-id="e62c2-168">Save the **AutoDiscoverSMTPAddress** user setting locally, as you'll use that in the next step.</span></span> 
  
<span data-ttu-id="e62c2-169">Alternativ, wenn Sie nicht möchten, verwenden Sie **Exchange 2013: Abrufen von benutzereinstellungen für mit der AutoErmittlung** Beispiel erhalten Sie vom Benutzer **AutoDiscoverSMTPAddress** nach [generieren Sie eine Liste der AutoErmittlung](how-to-generate-a-list-of-autodiscover-endpoints.md)festlegen, und senden Sie dann die folgenden POX Anforderung der AutoErmittlung auf jede URL, bis Sie eine erfolgreiche Antwort erhalten.</span><span class="sxs-lookup"><span data-stu-id="e62c2-169">Alternatively, if you do not want to use **Exchange 2013: Get user settings with Autodiscover** sample, you can get the **AutoDiscoverSMTPAddress** user setting by [generating a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and then sending the following POX Autodiscover request to each URL until you receive a successful response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</EMailAddress>
    <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

<span data-ttu-id="e62c2-170">Weitere Informationen zu den AutoErmittlung-Prozesses finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md), [generieren eine Liste von AutoErmittlung-Endpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md)und [benutzereinstellungen aus Exchange mithilfe der AutoErmittlung erhalten möchten](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="e62c2-170">For more information about the Autodiscover process, see [Autodiscover for Exchange](autodiscover-for-exchange.md), [Generate a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span></span>
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a><span data-ttu-id="e62c2-171">Legen Sie die Werte der X-AnchorMailbox und X-PublicFolderMailbox-Header</span><span class="sxs-lookup"><span data-stu-id="e62c2-171">Set the values of the X-AnchorMailbox and X-PublicFolderMailbox headers</span></span>
<span data-ttu-id="e62c2-172"><a name="bk_setheadervalues"> </a></span><span class="sxs-lookup"><span data-stu-id="e62c2-172"></span></span>

<span data-ttu-id="e62c2-173">Verwenden den Wert für die **AutoDiscoverSMTPAddress** erworben in [AutoErmittlung anzufordern](#bk_makeautodrequest), legen Sie die Werte der **X-AnchorMailbox** und **X-PublicFolderMailbox-** Header in Ihrer öffentlichen Ordner Content-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e62c2-173">Using the value for the **AutoDiscoverSMTPAddress** acquired in [Make an Autodiscover request](#bk_makeautodrequest), set the values of the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers in your public folder content request.</span></span> 
  
<span data-ttu-id="e62c2-174">Ein AutoDiscoverSMTPAddress NewPublicFolder@contoso.com angegeben, beispielsweise die folgenden Kopfzeilen beim Aufrufen der folgenden Methoden oder Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e62c2-174">For example, given an AutoDiscoverSMTPAddress of NewPublicFolder@contoso.com, include the following headers when making calls to the following methods or operations.</span></span>
  
`X-AnchorMailbox: NewPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: NewPublicFolder@contoso.com`

<span data-ttu-id="e62c2-175">**Öffentliche Ordner-Anrufe, die die X-AncorMailbox und X-PublicFolder Header erfordern**</span><span class="sxs-lookup"><span data-stu-id="e62c2-175">**Public folder calls that require the X-AncorMailbox and X-PublicFolder headers**</span></span>

|<span data-ttu-id="e62c2-176">**EWS Managed API-Methoden**</span><span class="sxs-lookup"><span data-stu-id="e62c2-176">**EWS Managed API methods**</span></span>|<span data-ttu-id="e62c2-177">**EWS-Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="e62c2-177">**EWS operations**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e62c2-178">Item.Bind</span><span class="sxs-lookup"><span data-stu-id="e62c2-178">Item.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="e62c2-179">Item.Update</span><span class="sxs-lookup"><span data-stu-id="e62c2-179">Item.Update</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="e62c2-180">Item.Copy</span><span class="sxs-lookup"><span data-stu-id="e62c2-180">Item.Copy</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="e62c2-181">Item.Move</span><span class="sxs-lookup"><span data-stu-id="e62c2-181">Item.Move</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="e62c2-182">Item.Delete</span><span class="sxs-lookup"><span data-stu-id="e62c2-182">Item.Delete</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="e62c2-183">Folder.Bind</span><span class="sxs-lookup"><span data-stu-id="e62c2-183">Folder.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="e62c2-184">Folder.FindItems</span><span class="sxs-lookup"><span data-stu-id="e62c2-184">Folder.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="e62c2-185">CreateItem</span><span class="sxs-lookup"><span data-stu-id="e62c2-185">CreateItem</span></span>](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [<span data-ttu-id="e62c2-186">GetItem</span><span class="sxs-lookup"><span data-stu-id="e62c2-186">GetItem</span></span>](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [<span data-ttu-id="e62c2-187">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="e62c2-187">UpdateItem</span></span>](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [<span data-ttu-id="e62c2-188">CopyItem</span><span class="sxs-lookup"><span data-stu-id="e62c2-188">CopyItem</span></span>](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [<span data-ttu-id="e62c2-189">MoveItem</span><span class="sxs-lookup"><span data-stu-id="e62c2-189">MoveItem</span></span>](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [<span data-ttu-id="e62c2-190">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="e62c2-190">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> [<span data-ttu-id="e62c2-191">GetFolder</span><span class="sxs-lookup"><span data-stu-id="e62c2-191">GetFolder</span></span>](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [<span data-ttu-id="e62c2-192">FindItem</span><span class="sxs-lookup"><span data-stu-id="e62c2-192">FindItem</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="e62c2-193">Wenn diese Header mithilfe der EWS Managed API hinzufügen möchten, verwenden Sie die [HttpHeaders.Add](http://msdn.microsoft.com/en-us/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e62c2-193">To add these headers by using the EWS Managed API, use the [HttpHeaders.Add](http://msdn.microsoft.com/en-us/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) method.</span></span> 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "NewPublicFolder@contoso.com");
service.HttpHeaders.Add("X-PublicFolderMailbox", "NewPublicFolder@contoso.com");
```

<span data-ttu-id="e62c2-194">Der folgende Code zeigt eine [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) -Anforderung mit dem **X-AnchorMailbox** und **X-PublicFolderMailbox** -Header auf die Werte in den Beispielen in diesem Artikel abgerufen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e62c2-194">The following code shows a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request with the **X-AnchorMailbox** and **X-PublicFolderMailbox** header set to the values retrieved in the examples in this article.</span></span> 
  
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
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

## <a name="see-also"></a><span data-ttu-id="e62c2-195">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e62c2-195">See also</span></span>

- [<span data-ttu-id="e62c2-196">Zugriff auf Öffentliche Ordner mit EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e62c2-196">Public folder access with EWS in Exchange</span></span>](public-folder-access-with-ews-in-exchange.md)    
- [<span data-ttu-id="e62c2-197">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="e62c2-197">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)    
- [<span data-ttu-id="e62c2-198">Generieren einer Liste mit AutoErmittlungs-Endpunkten</span><span class="sxs-lookup"><span data-stu-id="e62c2-198">Generate a list of Autodiscover endpoints</span></span>](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [<span data-ttu-id="e62c2-199">Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="e62c2-199">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    

