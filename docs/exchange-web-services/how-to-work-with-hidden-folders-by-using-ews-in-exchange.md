---
title: Arbeiten Sie mit verborgene Ordner im Exchange mithilfe der Exchange-Webdienste
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7ae7c045-cd90-4c9f-baf5-0464d5058f45
description: Hier erfahren Sie, wie Sie einen Ordner ausgeblendet, und suchen Sie verborgene Ordner durch Verwenden der EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 72efc16ecc247d307b7300526e7d345fe6bdd3ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757020"
---
# <a name="work-with-hidden-folders-by-using-ews-in-exchange"></a><span data-ttu-id="2455c-103">Arbeiten Sie mit verborgene Ordner im Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="2455c-103">Work with hidden folders by using EWS in Exchange</span></span>

<span data-ttu-id="2455c-104">Hier erfahren Sie, wie Sie einen Ordner ausgeblendet, und suchen Sie verborgene Ordner durch Verwenden der EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="2455c-104">Learn how to make a folder hidden and find hidden folders by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="2455c-105">Ordner im Stamm des Exchange-Postfach (der IPM Unterstruktur) werden mit einer Ausnahme vom Benutzer ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="2455c-105">With one exception, folders in the root of an Exchange mailbox (the non-IPM subtree) are hidden from the user.</span></span> <span data-ttu-id="2455c-106">Umgekehrt sind alle Ordner in der **MsgFolderRoot** (IPM-Unterstruktur) für den Benutzer sichtbar.</span><span class="sxs-lookup"><span data-stu-id="2455c-106">Conversely, all folders in the **MsgFolderRoot** (the IPM subtree) are visible to the user.</span></span> <span data-ttu-id="2455c-107">So wie ausblenden Sie einen Ordner unterhalb der **MsgFolderRoot**?</span><span class="sxs-lookup"><span data-stu-id="2455c-107">So how do you hide a folder under the **MsgFolderRoot**?</span></span> <span data-ttu-id="2455c-108">Es ist nicht das schwierig – es darum, nur einer Eigenschaft, die [PidTagAttributeHidden](http://msdn.microsoft.com/de-de/library/cc433490%28v=exchg.80%29.aspx) (0x10F4000B) extended-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2455c-108">It's not that tricky — it comes down to just one property, the [PidTagAttributeHidden](http://msdn.microsoft.com/de-de/library/cc433490%28v=exchg.80%29.aspx) (0x10F4000B) extended property.</span></span> <span data-ttu-id="2455c-109">Wenn diese Eigenschaft auf **true**festgelegt ist, wird Outlook oder einem anderen Client, der die-Eigenschaft verwendet, um die Sichtbarkeit der Ordner bestimmen den Ordner aus Sicht der Benutzer ausblenden.</span><span class="sxs-lookup"><span data-stu-id="2455c-109">When this property is set to **true**, Outlook or another client that uses the property to determine folder visibility will hide the folder from the user's view.</span></span> <span data-ttu-id="2455c-110">Da es sich um eine erweiterte Eigenschaft handelt, ist es schwieriger zu als die durchschnittliche Ordnereigenschaft verwenden, damit Sie in diesem Artikel über die wichtigsten Szenarien durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="2455c-110">Because this is an extended property, it's more complex to use than your average folder property, so this article will walk you through the main scenarios.</span></span>
  
<span data-ttu-id="2455c-111">**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für die Arbeit mit verborgene Ordner**</span><span class="sxs-lookup"><span data-stu-id="2455c-111">**Table 1. EWS Managed API methods and EWS operations for working with hidden folders**</span></span>

|<span data-ttu-id="2455c-112">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="2455c-112">**Task**</span></span>|<span data-ttu-id="2455c-113">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="2455c-113">**EWS Managed API method**</span></span>|<span data-ttu-id="2455c-114">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="2455c-114">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2455c-115">Ausblenden eines Ordners</span><span class="sxs-lookup"><span data-stu-id="2455c-115">Hide a folder</span></span>  <br/> |<span data-ttu-id="2455c-116">[Folder.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) gefolgt von [Folder.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2455c-116">[Folder.Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) followed by [Folder.Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="2455c-117">[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) gefolgt von [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2455c-117">[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) followed by [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="2455c-118">Hier finden Sie verborgene Ordner</span><span class="sxs-lookup"><span data-stu-id="2455c-118">Find hidden folders</span></span>  <br/> |[<span data-ttu-id="2455c-119">FindFolders</span><span class="sxs-lookup"><span data-stu-id="2455c-119">FindFolders</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2455c-120">FindFolder</span><span class="sxs-lookup"><span data-stu-id="2455c-120">FindFolder</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="2455c-121">Sind Sie wissen, was die einzige Ausnahme ist – d. h., welche Ordner im Stamm für Benutzer sichtbar ist?</span><span class="sxs-lookup"><span data-stu-id="2455c-121">Are you wondering what the one exception is — that is, what folder in the root IS visible to users?</span></span> <span data-ttu-id="2455c-122">Es ist die Finder-Ordner (auch bekannt als die **SearchFolders**-[WellKnownFolder](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) -Enumerationswert ab, oder der **Searchfolders**[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) -Elementwert) der Benutzer die Suchordner enthält.</span><span class="sxs-lookup"><span data-stu-id="2455c-122">It's the Finder folder (also known as the **SearchFolders**[WellKnownFolder](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) enumeration value, or the **searchfolders**[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) element value), which contains users' search folders.</span></span> <span data-ttu-id="2455c-123">Im Ordner "Finder" erstellten Suchordner sind für Benutzer in Outlook angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2455c-123">Search folders created in the Finder folder are visible to Outlook users.</span></span> <span data-ttu-id="2455c-124">Wenn Sie müssen einen Suchordner erstellen, der für Benutzer nicht sichtbar ist, verschieben Sie es unter dem Stammordner auszublenden.</span><span class="sxs-lookup"><span data-stu-id="2455c-124">If you need to create a search folder that is not visible to users, move it under the root folder to hide it.</span></span> <span data-ttu-id="2455c-125">Im Gegensatz zu werden für andere Ordner die **PidTagAttributeHidden** -Eigenschaft auf **true** festlegen keinen Suchordner im Ordner "Finder" ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="2455c-125">Unlike for other folders, setting the **PidTagAttributeHidden** property to **true** will not hide a search folder in the Finder folder.</span></span> 
  
## <a name="hide-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="2455c-126">Ausblenden eines Ordners mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="2455c-126">Hide a folder by using the EWS Managed API</span></span>
<span data-ttu-id="2455c-127"><a name="bk_hideewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="2455c-127"></span></span>

<span data-ttu-id="2455c-128">Sie können [einen bestehenden Ordner stellen](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) einen versteckten Ordner durch Ändern der erweiterten Eigenschaft auf **true fest,** [PidTagAttributeHidden](http://msdn.microsoft.com/de-de/library/cc433490%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2455c-128">You can [make an existing folder](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) a hidden folder by changing the [PidTagAttributeHidden](http://msdn.microsoft.com/de-de/library/cc433490%28v=exchg.80%29.aspx) extended property to **true**.</span></span> <span data-ttu-id="2455c-129">Erstellen Sie zunächst eine [erweiterten Eigenschaftendefinition für die Eigenschaft](properties-and-extended-properties-in-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="2455c-129">First, create an [extended property definition for the property](properties-and-extended-properties-in-ews-in-exchange.md).</span></span> <span data-ttu-id="2455c-130">Im nächsten Schritt verwenden Sie die Methode [zu binden](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) auf den Ordner zugreifen und dann aktualisieren Sie den Wert der **PidTagAttributeHidden** -Eigenschaft auf true und die [Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) -Methode verwenden, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2455c-130">Next, use the [Bind](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method to get to the folder, then update the value of the **PidTagAttributeHidden** property to true, and use the [Update](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
  
<span data-ttu-id="2455c-131">In diesem Beispiel wird davon ausgegangen, die **Service** ist eine gültige [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) für den Postfachbesitzer-Objekt zurück, der Benutzer wurde an einen Exchange-Server authentifiziert wurden und diese **FolderId** ist eine gültige [Folder.Id](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) , der den Ordner ausblenden identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2455c-131">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, that the user has been authenticated to an Exchange server, and that **folderId** is a valid [Folder.Id](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) that identifies the folder to hide.</span></span> 
  
```cs
private static void MakeHidden(FolderId folderId, ExchangeService service)
{
    // Create an extended property definition for the PidTagAttributeHidden property.
    ExtendedPropertyDefinition isHiddenProp = new ExtendedPropertyDefinition(0x10f4, MapiPropertyType.Boolean);
    PropertySet propSet = new PropertySet(isHiddenProp);
    // Bind to a folder and retrieve the PidTagAttributeHidden property.
    Folder folder = Folder.Bind(service, folderId, propSet);
    // Set the PidTagAttributeHidden property to true.
    folder.SetExtendedProperty(isHiddenProp, true);
    // Save the changes.
    folder.Update();
}
```

## <a name="hide-a-folder-by-using-ews"></a><span data-ttu-id="2455c-132">Ausblenden eines Ordners mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="2455c-132">Hide a folder by using EWS</span></span>
<span data-ttu-id="2455c-133"><a name="bk_hideews"> </a></span><span class="sxs-lookup"><span data-stu-id="2455c-133"></span></span>

<span data-ttu-id="2455c-134">EWS können [stellen einen bestehenden Ordner](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) einen versteckten Ordner durch Ändern der erweiterten Eigenschaft auf **true fest,** [PidTagAttributeHidden](http://msdn.microsoft.com/de-de/library/cc433490%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2455c-134">You can use EWS to [make an existing folder](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) a hidden folder by changing the [PidTagAttributeHidden](http://msdn.microsoft.com/de-de/library/cc433490%28v=exchg.80%29.aspx) extended property to **true**.</span></span> <span data-ttu-id="2455c-135">Verwenden des [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) -Vorgangs, um auf den Ordner zugreifen zunächst, einschließlich des [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) -Elements und Festlegen der **' PropertyTag '** -Wert, der 4340 und die **PropertyType Abrufen der **PidTagAttributeHidden** -Eigenschaft **in einen booleschen Wert.</span><span class="sxs-lookup"><span data-stu-id="2455c-135">First, use the [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation to get to the folder, then retrieve the **PidTagAttributeHidden** property by including the [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element, and setting the **PropertyTag** value to 4340 and the **PropertyType** value to Boolean.</span></span> 
  
<span data-ttu-id="2455c-136">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Bind** -Methode verwenden, um einen Ordner, bevor [es einen versteckten Ordner](#bk_hideewsma)abrufen.</span><span class="sxs-lookup"><span data-stu-id="2455c-136">This is also the XML request that the EWS Managed API sends when you use the **Bind** method to get a folder before [making it a hidden folder](#bk_hideewsma).</span></span>
  
<span data-ttu-id="2455c-137">Der [Ordner-ID](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) -Wert wird zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="2455c-137">The [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) value is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:FolderIds>
        <t:FolderId Id="IQywAAAA==" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die Anforderung **GetFolder** mit einer [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass der Ordner erfolgreich abgerufen wurde. Die Antwort enthält auch einen [Wert](http://msdn.microsoft.com/library/196278d4-5e77-4e0a-8af6-8ac065610510%28Office.15%29.aspx) für die [ExtendedProperty](http://msdn.microsoft.com/library/f9701409-b620-4afe-b9ee-4c1e95507af7%28Office.15%29.aspx). <span data-ttu-id="2455c-140">In diesem Beispiel wird der **Wert** auf **false**festgelegt, was bedeutet, dass der Ordner derzeit nicht ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="2455c-140">In this example, the **Value** is set to **false**, which means that the folder is currently not hidden.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="898"
                         MinorBuildNumber="23"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="IQywAAAA=="
                          ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAAABED" />
              <t:ExtendedProperty>
                <t:ExtendedFieldURI PropertyTag="0x10f4"
                                    PropertyType="Boolean" />
                <t:Value>false</t:Value>
              </t:ExtendedProperty>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="2455c-141">Wenn Sie um den Wert der **ExtendedProperty** auf "true" zu ändern, verwenden Sie die [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) -Operation.</span><span class="sxs-lookup"><span data-stu-id="2455c-141">To change the value of the **ExtendedProperty** to true, use the [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="2455c-142">Enthalten Sie die **ExtendedProperty**, **ExtendedFieldURI**und **Value** -Elemente, für die **PidTagAttributeHidden** erweiterte Eigenschaft, und legen Sie das **Value** -Element auf **true fest,** um den Ordner auszublenden.</span><span class="sxs-lookup"><span data-stu-id="2455c-142">Include the **ExtendedProperty**, **ExtendedFieldURI**, and **Value** elements for the **PidTagAttributeHidden** extended property, and set the **Value** element to **true** to hide the folder.</span></span> 
  
<span data-ttu-id="2455c-143">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Update** -Methode verwenden, um einen Ordner mit dem [sie einen ausgeblendete Ordner](#bk_hideewsma)aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2455c-143">This is also the XML request that the EWS Managed API sends when you use the **Update** method to update a folder to [make it a hidden folder](#bk_hideewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="IQywAAAA=="
                      ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAAABED" />
          <t:Updates>
            <t:SetFolderField>
              <t:ExtendedFieldURI PropertyTag="4340"
                                  PropertyType="Boolean" />
              <t:Folder>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="4340"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="2455c-144">Der Server antwortet auf die Anforderung **UpdateFolder** mit einer [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass der Ordner erfolgreich aktualisiert wurde, und ist jetzt ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="2455c-144">The server responds to the **UpdateFolder** request with an [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was updated successfully, and is now hidden.</span></span>
  
## <a name="find-all-hidden-folders-by-using-the-ews-managed-api"></a><span data-ttu-id="2455c-145">Hier finden Sie alle ausgeblendeten Ordner mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="2455c-145">Find all hidden folders by using the EWS Managed API</span></span>
<span data-ttu-id="2455c-146"><a name="bk_findhiddenewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="2455c-146"></span></span>

<span data-ttu-id="2455c-147">Finden Sie unter einem übergeordneten Ordner ausgeblendete Ordner durch Erstellen einer [erweiterten Eigenschaftsdefinition](properties-and-extended-properties-in-ews-in-exchange.md) für die erweiterte Eigenschaft **PidTagAttributeHidden** , und klicken Sie dann mithilfe der Methode [FindFolders](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) Ordner mit einer **Suchen PidTagAttributeHidden** -Wert, der auf **true**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2455c-147">You can find all hidden folders under a parent folder by creating an [extended property definition](properties-and-extended-properties-in-ews-in-exchange.md) for the **PidTagAttributeHidden** extended property, and then using the [FindFolders](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) method to find folders with a **PidTagAttributeHidden** value that is set to **true**.</span></span> <span data-ttu-id="2455c-148">In diesem Beispiel wird die MsgFolderRoot, auch als die oberste Ebene des Informationsspeichers oder IPM-Unterstruktur bezeichnet, mit dem übergeordneten Ordner unter Suchen.</span><span class="sxs-lookup"><span data-stu-id="2455c-148">This example uses the MsgFolderRoot, also known as the Top of Information Store, or IPM Subtree, as the parent folder to search under.</span></span>
  
<span data-ttu-id="2455c-149">In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Besitzer des Postfachs und der Benutzer wurde an einen Exchange-Server authentifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="2455c-149">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
private static void FindHiddenFolders(ExchangeService service)
{
    // Create an extended property definition for the PidTagAttributeHidden property.
    ExtendedPropertyDefinition isHiddenProp = new ExtendedPropertyDefinition(0x10f4, MapiPropertyType.Boolean);
    // Create a folder view to retrieve up to 100 folders and 
    // retrieve only the PidTagAttributeHidden and the display name.
    FolderView folderView = new FolderView(100);
    folderView.PropertySet = new PropertySet(isHiddenProp, FolderSchema.DisplayName);
    // Indicate a Traversal value of Deep, so that all subfolders are retrieved.
    folderView.Traversal = FolderTraversal.Deep;
    // Find all hidden folders under the MsgFolderRoot.
    // This call results in a FindFolder call to EWS.
    FindFoldersResults findFolder = service.FindFolders(WellKnownFolderName.MsgFolderRoot,
            new SearchFilter.IsEqualTo(isHiddenProp, true), folderView);
    // Display the folder ID and display name of each hidden folder.
    foreach (Folder folder in findFolder)
    {
        Console.WriteLine("FolderId: {0}", folder.Id);
        Console.WriteLine("DisplayName: {0}", folder.DisplayName);
        Console.WriteLine("\r\n");
    }
}
```

## <a name="find-all-hidden-folders-by-using-ews"></a><span data-ttu-id="2455c-150">Hier finden Sie alle ausgeblendeten Ordner mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="2455c-150">Find all hidden folders by using EWS</span></span>
<span data-ttu-id="2455c-151"><a name="bk_findhiddenews"> </a></span><span class="sxs-lookup"><span data-stu-id="2455c-151"></span></span>

<span data-ttu-id="2455c-152">Verwenden von EWS ausgeblendete Ordner unter einem vorhandenen Ordner finden, indem Sie den Vorgang [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) aufrufen und Ordner gesucht, deren [PidTagAttributeHidden](http://msdn.microsoft.com/de-de/library/cc433490%28v=exchg.80%29.aspx) erweiterte Eigenschaft auf **true**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2455c-152">You can use EWS to find all hidden folders under an existing folder by calling the [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) operation and searching for folders whose [PidTagAttributeHidden](http://msdn.microsoft.com/de-de/library/cc433490%28v=exchg.80%29.aspx) extended property is set to **true**.</span></span> <span data-ttu-id="2455c-153">Dazu gehören Sie eine ["IsEqualTo"](http://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx)[Einschränkung](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) , die für das [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) -Element für die **PidTagAttributeHidden** -Eigenschaft ( **' PropertyTag '** -Wert, der 4243 und der **PropertyType** Wert in einen booleschen Wert) durchsucht wie in der folgenden Anforderung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2455c-153">To do this, include an [IsEqualTo](http://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx)[Restriction](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) that searches for the [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element for the **PidTagAttributeHidden** property ( **PropertyTag** value to 4243 and the **PropertyType** value to Boolean), as shown in the following request.</span></span> <span data-ttu-id="2455c-154">In diesem Beispiel wird die MsgFolderRoot, auch als die oberste Ebene des Informationsspeichers oder IPM-Unterstruktur bezeichnet, mit dem übergeordneten Ordner unter Suchen.</span><span class="sxs-lookup"><span data-stu-id="2455c-154">This example uses the MsgFolderRoot, also known as the Top of Information Store, or IPM Subtree, as the parent folder to search under.</span></span> 
  
<span data-ttu-id="2455c-155">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die Methode **FindFolders** , [erhalten alle ausgeblendeten Ordner](#bk_findhiddenewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="2455c-155">This is also the XML request that the EWS Managed API sends when you use the **FindFolders** method to [find all hidden folders](#bk_findhiddenewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Central Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Deep">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
          <t:FieldURI FieldURI="folder:DisplayName" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="100"
                               Offset="0"
                               BasePoint="Beginning" />
      <m:Restriction>
        <t:IsEqualTo>
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
          <t:FieldURIOrConstant>
            <t:Constant Value="true" />
          </t:FieldURIOrConstant>
        </t:IsEqualTo>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="msgfolderroot" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="2455c-156">Der Server antwortet auf die Anforderung **FindFolder** mit einer [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die Suche Ordner erfolgreich war, und alle ausgeblendeten der Ordner unter dem Stammordner der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2455c-156">The server responds to the **FindFolder** request with a [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder search was successful, as well as all the hidden folders under the root message folder.</span></span>
  
<span data-ttu-id="2455c-157">Die [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) -Werte werden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="2455c-157">The [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) values are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="898"
                         MinorBuildNumber="23"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="6"
                        TotalItemsInView="6"
                        IncludesLastItemInRange="true">
            <t:Folders>
              <t:ContactsFolder>
                <t:FolderId Id="IBHgAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAACz" />
                <t:DisplayName>{06967759-274D-40B2-A3EB-D7F9E73727D7}</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="IBHwAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAAC7" />
                <t:DisplayName>{A9E2BC46-B3A0-4243-B315-60D991004455}</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="IBIQAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAADO" />
                <t:DisplayName>GAL Contacts</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="IBHQAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAACa" />
                <t:DisplayName>Recipient Cache</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:Folder>
                <t:FolderId Id="HAAAAA=="
                            ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAAAACS" />
                <t:DisplayName>Conversation Action Settings</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
              <t:Folder>
                <t:FolderId Id="IQywAAAA=="
                            ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAeZIBf" />
                <t:DisplayName>TestFolder</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
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

## 
<span data-ttu-id="2455c-158"><a name="bk_findhiddenews"> </a></span><span class="sxs-lookup"><span data-stu-id="2455c-158"></span></span>

<span data-ttu-id="2455c-159">Erst, nachdem Sie sind ausgeblendet oder eingeblendet Ordner möglicherweise möchten Sie die Ordnerhierarchie oder [die Ordnerhierarchie synchronisieren](how-to-synchronize-folders-by-using-ews-in-exchange.md)möchten.</span><span class="sxs-lookup"><span data-stu-id="2455c-159">After you have hidden or unhidden folders, you might want to get the folder hierarchy or [synchronize the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="2455c-160">In den Beispielen, die zeigen, dass Sie wie zum [Abrufen einer Ordnerhierarchie mithilfe der EWS Managed API](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyewsma) oder [Abrufen eine Ordnerhierarchie mithilfe der Exchange-Webdienste](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyews) auch welche Ordner in der Hierarchie angeben, werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="2455c-160">The examples that show you how to [get a folder hierarchy by using the EWS Managed API](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyewsma) or [get a folder hierarchy by using EWS](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyews) also indicate which folders in the hierarchy are hidden.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2455c-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2455c-161">See also</span></span>


- [<span data-ttu-id="2455c-162">Ordner und Elemente in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2455c-162">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    
- [<span data-ttu-id="2455c-163">Arbeiten Sie mit Ordnern in Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="2455c-163">Work with folders by using EWS in Exchange</span></span>](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="2455c-164">Arbeiten Sie mit Suchordner in Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="2455c-164">Work with search folders by using EWS in Exchange</span></span>](how-to-work-with-search-folders-by-using-ews-in-exchange.md)
    

