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
description: Das CreateAttachment-Element definiert eine Anforderung zum Erstellen einer Anlage für ein Element in der Exchange-Informationsspeicher.
ms.openlocfilehash: 4cba1b8865dae5da58b9617b249a29314c67331a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466437"
---
# <a name="createattachment"></a><span data-ttu-id="290c3-103">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="290c3-103">CreateAttachment</span></span>

<span data-ttu-id="290c3-104">Das **CreateAttachment** -Element definiert eine Anforderung zum Erstellen einer Anlage für ein Element in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="290c3-104">The **CreateAttachment** element defines a request to create an attachment to an item in the Exchange store.</span></span> 
  
```xml
<CreateAttachment>
   <ParentItemId/>
   <Attachments/>
</CreateAttachment>
```

 <span data-ttu-id="290c3-105">**Createattachmenttype**</span><span class="sxs-lookup"><span data-stu-id="290c3-105">**CreateAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="290c3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="290c3-106">Attributes and elements</span></span>

<span data-ttu-id="290c3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="290c3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="290c3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="290c3-108">Attributes</span></span>

<span data-ttu-id="290c3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="290c3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="290c3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="290c3-110">Child elements</span></span>

|<span data-ttu-id="290c3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="290c3-111">**Element**</span></span>|<span data-ttu-id="290c3-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="290c3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="290c3-113">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="290c3-113">ParentItemId</span></span>](parentitemid.md) <br/> |<span data-ttu-id="290c3-114">Gibt das übergeordnete Exchange-Informationsspeicher Element an, das die erstellte Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="290c3-114">Identifies the parent Exchange store item that contains the created attachment.</span></span> <span data-ttu-id="290c3-115">Das [ParentItemId](parentitemid.md) -Element muss die ID eines echten Exchange-Informationsspeicher Elements bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="290c3-115">The [ParentItemId](parentitemid.md) element must provide the ID of a real Exchange store item.</span></span> <span data-ttu-id="290c3-116">Reale Speicherelemente können mithilfe des [GetItem-Vorgangs](getitem-operation.md)abgerufen werden; Anlagen werden mithilfe des [GetAttachment-Vorgangs](getattachment-operation.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="290c3-116">Real store items can be retrieved by using the [GetItem operation](getitem-operation.md); attachments are retrieved by using the [GetAttachment operation](getattachment-operation.md).</span></span> <span data-ttu-id="290c3-117">Wenn dem [ParentItemId](parentitemid.md) die ID einer Dateianlage übergeben wird, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="290c3-117">An error occurs if the [ParentItemId](parentitemid.md) is passed the ID of a file attachment.</span></span> <span data-ttu-id="290c3-118">Wenn der [ParentItemId](parentitemid.md) die ID einer vorhandenen Elementanlage darstellt, fügt der CreateAttachment- [Vorgang](createattachment-operation.md) die neue Anlage zu der vorhandenen Anlage hinzu.</span><span class="sxs-lookup"><span data-stu-id="290c3-118">If the [ParentItemId](parentitemid.md) represents the ID of an existing item attachment, the [CreateAttachment operation](createattachment-operation.md) adds the new attachment to the existing attachment.</span></span>  <br/> <span data-ttu-id="290c3-119">Dieses Element ist für den [CreateAttachment-Vorgang](createattachment-operation.md)erforderlich.</span><span class="sxs-lookup"><span data-stu-id="290c3-119">This element is required for the [CreateAttachment operation](createattachment-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="290c3-120">Anlagen</span><span class="sxs-lookup"><span data-stu-id="290c3-120">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="290c3-121">Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="290c3-121">Contains the items or files to attach to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="290c3-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="290c3-122">Parent elements</span></span>

<span data-ttu-id="290c3-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="290c3-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="290c3-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="290c3-124">Remarks</span></span>

<span data-ttu-id="290c3-125">Eine Elementanlage ist nicht als Speicherelement vorhanden.</span><span class="sxs-lookup"><span data-stu-id="290c3-125">An item attachment does not exist as a store item.</span></span> <span data-ttu-id="290c3-126">Sie ist nur als Anlage für ein Element oder eine andere Anlage vorhanden.</span><span class="sxs-lookup"><span data-stu-id="290c3-126">It only exists as an attachment to an item or another attachment.</span></span> <span data-ttu-id="290c3-127">Element Anlagen können nur mithilfe der [GetAttachment](getattachment.md) -Anforderung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="290c3-127">Item attachments can only be retrieved by using the [GetAttachment](getattachment.md) request.</span></span> 
  
<span data-ttu-id="290c3-128">Die folgenden Element Anlagen können erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="290c3-128">The following item attachments can be created:</span></span>
  
- <span data-ttu-id="290c3-129">Element</span><span class="sxs-lookup"><span data-stu-id="290c3-129">Item</span></span>
    
- <span data-ttu-id="290c3-130">Meldung</span><span class="sxs-lookup"><span data-stu-id="290c3-130">Message</span></span>
    
- <span data-ttu-id="290c3-131">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="290c3-131">CalendarItem</span></span>
    
- <span data-ttu-id="290c3-132">Kontakt</span><span class="sxs-lookup"><span data-stu-id="290c3-132">Contact</span></span>
    
- <span data-ttu-id="290c3-133">Vorgang</span><span class="sxs-lookup"><span data-stu-id="290c3-133">Task</span></span>
    
- <span data-ttu-id="290c3-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="290c3-134">MeetingMessage</span></span>
    
- <span data-ttu-id="290c3-135">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="290c3-135">MeetingRequest</span></span>
    
<span data-ttu-id="290c3-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="290c3-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="290c3-137">Beispiel</span><span class="sxs-lookup"><span data-stu-id="290c3-137">Example</span></span>

<span data-ttu-id="290c3-138">Das folgende Beispiel zeigt, wie Sie ein Element erstellen und an ein anderes Element im Exchange-Informationsspeicher anfügen.</span><span class="sxs-lookup"><span data-stu-id="290c3-138">The following example shows how to create and attach an item to another item in the Exchange store.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="290c3-139">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="290c3-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="290c3-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="290c3-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="290c3-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="290c3-141">Schema Name</span></span>  <br/> |<span data-ttu-id="290c3-142">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="290c3-142">Messages schema</span></span>  <br/> |
|<span data-ttu-id="290c3-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="290c3-143">Validation File</span></span>  <br/> |<span data-ttu-id="290c3-144">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="290c3-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="290c3-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="290c3-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="290c3-146">False</span><span class="sxs-lookup"><span data-stu-id="290c3-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="290c3-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="290c3-147">See also</span></span>



[<span data-ttu-id="290c3-148">CreateAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="290c3-148">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="290c3-149">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="290c3-149">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
  
[<span data-ttu-id="290c3-150">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="290c3-150">GetAttachment operation</span></span>](getattachment-operation.md)

