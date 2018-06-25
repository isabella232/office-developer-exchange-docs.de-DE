---
title: CreateAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e33b403a-b7d3-48ee-8d24-6b7abf0d70bc
description: Das CreateAttachment-Element definiert eine Anforderung an eine Anlage zu einem Element in der Exchange-Speicher zu erstellen.
ms.openlocfilehash: d403eb5ca15623d3a973f7b224dbcde5529cf1bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757741"
---
# <a name="createattachment"></a><span data-ttu-id="aa929-103">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="aa929-103">CreateAttachment</span></span>

<span data-ttu-id="aa929-104">Das **CreateAttachment** -Element definiert eine Anforderung an eine Anlage zu einem Element in der Exchange-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aa929-104">The **CreateAttachment** element defines a request to create an attachment to an item in the Exchange store.</span></span> 
  
```xml
<CreateAttachment>
   <ParentItemId/>
   <Attachments/>
</CreateAttachment>
```

 <span data-ttu-id="aa929-105">**CreateAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="aa929-105">**CreateAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa929-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="aa929-106">Attributes and elements</span></span>

<span data-ttu-id="aa929-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="aa929-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa929-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="aa929-108">Attributes</span></span>

<span data-ttu-id="aa929-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="aa929-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa929-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aa929-110">Child elements</span></span>

|<span data-ttu-id="aa929-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="aa929-111">**Element**</span></span>|<span data-ttu-id="aa929-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aa929-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa929-113">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="aa929-113">ParentItemId</span></span>](parentitemid.md) <br/> |<span data-ttu-id="aa929-114">Gibt das übergeordnete Exchange Store-Element, das die erstellte Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="aa929-114">Identifies the parent Exchange store item that contains the created attachment.</span></span> <span data-ttu-id="aa929-115">Das [ParentItemId](parentitemid.md) -Element muss die ID des einer realen Exchange-Datenspeicherelement bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="aa929-115">The [ParentItemId](parentitemid.md) element must provide the ID of a real Exchange store item.</span></span> <span data-ttu-id="aa929-116">Echte Store Elemente können mithilfe der [GetItem Operation](getitem-operation.md)abgerufen werden. Anlagen werden mithilfe des [Vorgangs GetAttachment](getattachment-operation.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="aa929-116">Real store items can be retrieved by using the [GetItem operation](getitem-operation.md); attachments are retrieved by using the [GetAttachment operation](getattachment-operation.md).</span></span> <span data-ttu-id="aa929-117">Ein Fehler tritt auf, wenn die [ParentItemId](parentitemid.md) die ID der Dateianlage zu einer übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="aa929-117">An error occurs if the [ParentItemId](parentitemid.md) is passed the ID of a file attachment.</span></span> <span data-ttu-id="aa929-118">Wenn die [ParentItemId](parentitemid.md) die ID der Elementanlage vorhandenes darstellt, fügt den [CreateAttachment Vorgang](createattachment-operation.md) die neue Anlage in die vorhandene Anlage.</span><span class="sxs-lookup"><span data-stu-id="aa929-118">If the [ParentItemId](parentitemid.md) represents the ID of an existing item attachment, the [CreateAttachment operation](createattachment-operation.md) adds the new attachment to the existing attachment.</span></span>  <br/> <span data-ttu-id="aa929-119">Dieses Element ist für den [Vorgang CreateAttachment](createattachment-operation.md)erforderlich.</span><span class="sxs-lookup"><span data-stu-id="aa929-119">This element is required for the [CreateAttachment operation](createattachment-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="aa929-120">Anlagen</span><span class="sxs-lookup"><span data-stu-id="aa929-120">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="aa929-121">Enthält die Elemente oder Dateien eines Elements in der Exchange-Speicher an.</span><span class="sxs-lookup"><span data-stu-id="aa929-121">Contains the items or files to attach to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aa929-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aa929-122">Parent elements</span></span>

<span data-ttu-id="aa929-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="aa929-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa929-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aa929-124">Remarks</span></span>

<span data-ttu-id="aa929-125">Elementanlage ist nicht als Store Element vorhanden.</span><span class="sxs-lookup"><span data-stu-id="aa929-125">An item attachment does not exist as a store item.</span></span> <span data-ttu-id="aa929-126">Es ist nur als Anlage zu einem Element oder eine andere Anlage vorhanden.</span><span class="sxs-lookup"><span data-stu-id="aa929-126">It only exists as an attachment to an item or another attachment.</span></span> <span data-ttu-id="aa929-127">Anlagen können nur mithilfe der [GetAttachment](getattachment.md) -Anforderung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="aa929-127">Item attachments can only be retrieved by using the [GetAttachment](getattachment.md) request.</span></span> 
  
<span data-ttu-id="aa929-128">Die folgenden elementanlagen können erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="aa929-128">The following item attachments can be created:</span></span>
  
- <span data-ttu-id="aa929-129">Element</span><span class="sxs-lookup"><span data-stu-id="aa929-129">Item</span></span>
    
- <span data-ttu-id="aa929-130">Nachricht</span><span class="sxs-lookup"><span data-stu-id="aa929-130">Message</span></span>
    
- <span data-ttu-id="aa929-131">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="aa929-131">CalendarItem</span></span>
    
- <span data-ttu-id="aa929-132">Kontakt</span><span class="sxs-lookup"><span data-stu-id="aa929-132">Contact</span></span>
    
- <span data-ttu-id="aa929-133">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="aa929-133">Task</span></span>
    
- <span data-ttu-id="aa929-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="aa929-134">MeetingMessage</span></span>
    
- <span data-ttu-id="aa929-135">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="aa929-135">MeetingRequest</span></span>
    
<span data-ttu-id="aa929-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="aa929-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="aa929-137">Beispiel</span><span class="sxs-lookup"><span data-stu-id="aa929-137">Example</span></span>

<span data-ttu-id="aa929-138">Im folgenden Beispiel wird gezeigt, wie zu erstellen, und fügen Sie ein Element mit einem anderen Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="aa929-138">The following example shows how to create and attach an item to another item in the Exchange store.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="ASkAS"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>MyAttachment</t:Name>
          <t:Message>
            <t:ItemClass>IPM>Note</t:ItemClass>
            <t:Subject>My attachment subject</t:Subject>
            <t:Body BodyType="Text">My attachment body</t:Body>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="aa929-139">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="aa929-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa929-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa929-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="aa929-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="aa929-141">Schema Name</span></span>  <br/> |<span data-ttu-id="aa929-142">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="aa929-142">Messages schema</span></span>  <br/> |
|<span data-ttu-id="aa929-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="aa929-143">Validation File</span></span>  <br/> |<span data-ttu-id="aa929-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="aa929-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="aa929-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="aa929-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="aa929-146">False</span><span class="sxs-lookup"><span data-stu-id="aa929-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa929-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa929-147">See also</span></span>



[<span data-ttu-id="aa929-148">CreateAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="aa929-148">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="aa929-149">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="aa929-149">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
  
[<span data-ttu-id="aa929-150">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="aa929-150">GetAttachment operation</span></span>](getattachment-operation.md)

