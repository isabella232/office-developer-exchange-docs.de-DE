---
title: AdditionalProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AdditionalProperties
api_type:
- schema
ms.assetid: 7a269aed-dcfd-4c3e-9e14-094e53828101
description: Das AdditionalProperties-Element identifiziert zusätzliche Eigenschaften für die Verwendung in GetItem, UpdateItem, CreateItem, FindItem oder FindFolder anfordert.
ms.openlocfilehash: 64e4f1ee6b24cf8015b7893dc4a904ca8b32d58e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757230"
---
# <a name="additionalproperties"></a><span data-ttu-id="d5a83-103">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="d5a83-103">AdditionalProperties</span></span>

<span data-ttu-id="d5a83-104">Das **AdditionalProperties** -Element identifiziert zusätzliche Eigenschaften für die Verwendung in [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md)oder [FindFolder](findfolder.md) anfordert.</span><span class="sxs-lookup"><span data-stu-id="d5a83-104">The **AdditionalProperties** element identifies additional properties for use in [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md), or [FindFolder](findfolder.md) requests.</span></span> 
  
```xml
<AdditionalProperties>
   <ExtendedFieldURI/>
   <FieldURI/>
   <IndexedFieldURI/>
</AdditionalProperties>
```

 <span data-ttu-id="d5a83-105">**NonEmptyArrayOfPathsToElementType**</span><span class="sxs-lookup"><span data-stu-id="d5a83-105">**NonEmptyArrayOfPathsToElementType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5a83-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d5a83-106">Attributes and elements</span></span>

<span data-ttu-id="d5a83-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d5a83-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5a83-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d5a83-108">Attributes</span></span>

<span data-ttu-id="d5a83-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5a83-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5a83-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5a83-110">Child elements</span></span>

|<span data-ttu-id="d5a83-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5a83-111">**Element**</span></span>|<span data-ttu-id="d5a83-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5a83-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5a83-113">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="d5a83-113">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="d5a83-114">Bezeichnet die extended MAPI-Eigenschaften zum Abrufen oder festlegen, oder erstellen.</span><span class="sxs-lookup"><span data-stu-id="d5a83-114">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="d5a83-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="d5a83-115">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="d5a83-116">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d5a83-116">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="d5a83-117">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="d5a83-117">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="d5a83-118">Häufig referenzierten Wörterbucheigenschaften mithilfe von URI identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d5a83-118">Identifies frequently referenced dictionary properties by URI.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5a83-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5a83-119">Parent elements</span></span>

|<span data-ttu-id="d5a83-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5a83-120">**Element**</span></span>|<span data-ttu-id="d5a83-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5a83-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5a83-122">FolderShape</span><span class="sxs-lookup"><span data-stu-id="d5a83-122">FolderShape</span></span>](foldershape.md) <br/> | <span data-ttu-id="d5a83-123">Gibt die Eigenschaften des Ordners in einer Antwort [GetFolder](getfolder.md), [FindFolder](findfolder.md)oder [SyncFolderHierarchy](syncfolderhierarchy.md) aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="d5a83-123">Identifies the folder properties to include in a [GetFolder](getfolder.md), [FindFolder](findfolder.md), or [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span><br/><br/>  <span data-ttu-id="d5a83-124">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="d5a83-124">The following are the XPath expressions to this element:</span></span><br/><br/>  `/FindFolder/FolderShape` <br/>  `/GetFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[<span data-ttu-id="d5a83-125">ItemShape</span><span class="sxs-lookup"><span data-stu-id="d5a83-125">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="d5a83-126">Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort [GetItem](getitem.md), [FindItem](finditem.md)oder [SyncFolderItems](syncfolderitems.md) aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="d5a83-126">Identifies the item properties and content to include in a [GetItem](getitem.md), [FindItem](finditem.md), or [SyncFolderItems](syncfolderitems.md) response.</span></span><br/><br/>  <span data-ttu-id="d5a83-127">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="d5a83-127">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
|[<span data-ttu-id="d5a83-128">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="d5a83-128">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="d5a83-129">Zusätzliche erweiterte Elementeigenschaften in einer Antwort auf eine Anforderung [GetItem](getitem.md) zurückzugebenden identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d5a83-129">Identifies additional extended item properties to return in a response to a [GetItem](getitem.md) request.</span></span><br/><br/> <span data-ttu-id="d5a83-130">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d5a83-130">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5a83-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d5a83-131">Remarks</span></span>

<span data-ttu-id="d5a83-132">Nicht alle untergeordneten Elemente können mit [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md)oder [FindFolder](findfolder.md) Anforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5a83-132">Not all the child elements can be used with [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md), or [FindFolder](findfolder.md) requests.</span></span> <span data-ttu-id="d5a83-133">Die Eigenschaft muss auf den Ordner oder das Element, das zugegriffen wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="d5a83-133">The property must be applicable to the folder or item that is accessed.</span></span> <span data-ttu-id="d5a83-134">Verwenden Sie erweiterte Eigenschaften auf andere Eigenschaften zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="d5a83-134">Use extended properties to access other properties.</span></span> <span data-ttu-id="d5a83-135">Wenn die Eigenschaft für ein bestimmtes Element nicht vorhanden ist, wird kein entsprechendes Element in das resultierende XML ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d5a83-135">If the property does not exist for a given item, no corresponding element will be emitted into the resulting XML.</span></span> 
  
<span data-ttu-id="d5a83-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d5a83-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="d5a83-137">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5a83-137">This element is optional.</span></span>
  
## <a name="example"></a><span data-ttu-id="d5a83-138">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d5a83-138">Example</span></span>

<span data-ttu-id="d5a83-139">Im folgenden anforderungsbeispiel veranschaulicht einen Betreff des Elements abrufen, indem Sie mithilfe des **AdditionalProperties** -Elements.</span><span class="sxs-lookup"><span data-stu-id="d5a83-139">The following request example shows how to get an item subject by using the **AdditionalProperties** element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="ASkAS="/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="d5a83-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d5a83-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5a83-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5a83-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d5a83-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d5a83-142">Schema Name</span></span>  <br/> |<span data-ttu-id="d5a83-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d5a83-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="d5a83-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d5a83-144">Validation File</span></span>  <br/> |<span data-ttu-id="d5a83-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d5a83-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d5a83-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d5a83-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5a83-147">False</span><span class="sxs-lookup"><span data-stu-id="d5a83-147">False</span></span>  <br/> |
   

