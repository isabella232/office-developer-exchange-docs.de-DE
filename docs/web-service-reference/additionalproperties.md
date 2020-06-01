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
description: Das AdditionalProperties-Element identifiziert zusätzliche Eigenschaften für die Verwendung in GetItem-, UpdateItem-, CreateItem-, FindItem-oder FindFolder-Anforderungen.
ms.openlocfilehash: 90a307ba4d5ece10e15d2cec56cf5042c3d38685
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455814"
---
# <a name="additionalproperties"></a><span data-ttu-id="42d0a-103">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="42d0a-103">AdditionalProperties</span></span>

<span data-ttu-id="42d0a-104">Das **AdditionalProperties** -Element identifiziert zusätzliche Eigenschaften für die Verwendung in [GetItem](getitem.md)-, [UpdateItem](updateitem.md)-, [CreateItem](createitem.md)-, [FindItem](finditem.md)-oder [FindFolder](findfolder.md) -Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="42d0a-104">The **AdditionalProperties** element identifies additional properties for use in [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md), or [FindFolder](findfolder.md) requests.</span></span> 
  
```xml
<AdditionalProperties>
   <ExtendedFieldURI/>
   <FieldURI/>
   <IndexedFieldURI/>
</AdditionalProperties>
```

 <span data-ttu-id="42d0a-105">**NonEmptyArrayOfPathsToElementType**</span><span class="sxs-lookup"><span data-stu-id="42d0a-105">**NonEmptyArrayOfPathsToElementType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="42d0a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="42d0a-106">Attributes and elements</span></span>

<span data-ttu-id="42d0a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="42d0a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="42d0a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="42d0a-108">Attributes</span></span>

<span data-ttu-id="42d0a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="42d0a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="42d0a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="42d0a-110">Child elements</span></span>

|<span data-ttu-id="42d0a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="42d0a-111">**Element**</span></span>|<span data-ttu-id="42d0a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42d0a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42d0a-113">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="42d0a-113">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="42d0a-114">Identifiziert erweiterte MAPI-Eigenschaften zum Abrufen, festlegen oder erstellen.</span><span class="sxs-lookup"><span data-stu-id="42d0a-114">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="42d0a-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="42d0a-115">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="42d0a-116">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="42d0a-116">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="42d0a-117">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="42d0a-117">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="42d0a-118">Identifiziert häufig referenzierte Wörterbucheigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="42d0a-118">Identifies frequently referenced dictionary properties by URI.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="42d0a-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="42d0a-119">Parent elements</span></span>

|<span data-ttu-id="42d0a-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="42d0a-120">**Element**</span></span>|<span data-ttu-id="42d0a-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42d0a-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42d0a-122">FolderShape</span><span class="sxs-lookup"><span data-stu-id="42d0a-122">FolderShape</span></span>](foldershape.md) <br/> | <span data-ttu-id="42d0a-123">Identifiziert die Ordner Eigenschaften, die in eine [GetFolder](getfolder.md)-, [FindFolder](findfolder.md)-oder [SyncFolderHierarchy](syncfolderhierarchy.md) -Antwort eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="42d0a-123">Identifies the folder properties to include in a [GetFolder](getfolder.md), [FindFolder](findfolder.md), or [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span><br/><br/>  <span data-ttu-id="42d0a-124">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="42d0a-124">The following are the XPath expressions to this element:</span></span><br/><br/>  `/FindFolder/FolderShape` <br/>  `/GetFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[<span data-ttu-id="42d0a-125">ItemShape</span><span class="sxs-lookup"><span data-stu-id="42d0a-125">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="42d0a-126">Identifiziert die Elementeigenschaften und Inhalte, die in einer [GetItem](getitem.md)-, [FindItem](finditem.md)-oder [SyncFolderItems](syncfolderitems.md) -Antwort enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="42d0a-126">Identifies the item properties and content to include in a [GetItem](getitem.md), [FindItem](finditem.md), or [SyncFolderItems](syncfolderitems.md) response.</span></span><br/><br/>  <span data-ttu-id="42d0a-127">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="42d0a-127">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
|[<span data-ttu-id="42d0a-128">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="42d0a-128">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="42d0a-129">Identifiziert zusätzliche erweiterte Elementeigenschaften, die in einer Antwort auf eine [GetItem](getitem.md) -Anforderung zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="42d0a-129">Identifies additional extended item properties to return in a response to a [GetItem](getitem.md) request.</span></span><br/><br/> <span data-ttu-id="42d0a-130">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="42d0a-130">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42d0a-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42d0a-131">Remarks</span></span>

<span data-ttu-id="42d0a-132">Nicht alle untergeordneten Elemente können mit [GetItem](getitem.md)-, [UpdateItem](updateitem.md)-, [CreateItem](createitem.md)-, [FindItem](finditem.md)-oder [FindFolder](findfolder.md) -Anforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42d0a-132">Not all the child elements can be used with [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md), or [FindFolder](findfolder.md) requests.</span></span> <span data-ttu-id="42d0a-133">Die-Eigenschaft muss auf den Ordner oder das Element angewendet werden, auf das zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="42d0a-133">The property must be applicable to the folder or item that is accessed.</span></span> <span data-ttu-id="42d0a-134">Verwenden Sie erweiterte Eigenschaften, um auf andere Eigenschaften zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="42d0a-134">Use extended properties to access other properties.</span></span> <span data-ttu-id="42d0a-135">Wenn die Eigenschaft für ein bestimmtes Element nicht vorhanden ist, wird kein entsprechendes Element in den resultierenden XML-Code ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="42d0a-135">If the property does not exist for a given item, no corresponding element will be emitted into the resulting XML.</span></span> 
  
<span data-ttu-id="42d0a-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="42d0a-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="42d0a-137">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="42d0a-137">This element is optional.</span></span>
  
## <a name="example"></a><span data-ttu-id="42d0a-138">Beispiel</span><span class="sxs-lookup"><span data-stu-id="42d0a-138">Example</span></span>

<span data-ttu-id="42d0a-139">Im folgenden Anforderungs Beispiel wird gezeigt, wie ein Element Betreff mithilfe des **AdditionalProperties** -Elements abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="42d0a-139">The following request example shows how to get an item subject by using the **AdditionalProperties** element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="42d0a-140">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="42d0a-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42d0a-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="42d0a-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="42d0a-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="42d0a-142">Schema Name</span></span>  <br/> |<span data-ttu-id="42d0a-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="42d0a-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="42d0a-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="42d0a-144">Validation File</span></span>  <br/> |<span data-ttu-id="42d0a-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="42d0a-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="42d0a-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="42d0a-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="42d0a-147">False</span><span class="sxs-lookup"><span data-stu-id="42d0a-147">False</span></span>  <br/> |
   

