---
title: UpdateDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateDelegateResponse
api_type:
- schema
ms.assetid: cd336add-fbcc-4f61-9867-d4c08a60e142
description: Das UpdateDelegateResponse-Element enthält den Status und das Ergebnis einer UpdateDelegate Vorgang Anforderung.
ms.openlocfilehash: b90dd7d8011cf75831481b8f2b92df80d9a67d31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839334"
---
# <a name="updatedelegateresponse"></a><span data-ttu-id="79583-103">UpdateDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="79583-103">UpdateDelegateResponse</span></span>

<span data-ttu-id="79583-104">Das **UpdateDelegateResponse** -Element enthält den Status und das Ergebnis einer Anforderung [UpdateDelegate Vorgang](updatedelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="79583-104">The **UpdateDelegateResponse** element contains the status and result of an [UpdateDelegate operation](updatedelegate-operation.md) request.</span></span> 
  
```xml
<UpdateDelegateResponseMessage>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UpdateDelegateResponseMessage>
```

 <span data-ttu-id="79583-105">**UpdateDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="79583-105">**UpdateDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="79583-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="79583-106">Attributes and elements</span></span>

<span data-ttu-id="79583-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="79583-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="79583-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="79583-108">Attributes</span></span>

<span data-ttu-id="79583-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="79583-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="79583-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="79583-110">Child elements</span></span>

|<span data-ttu-id="79583-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="79583-111">**Element**</span></span>|<span data-ttu-id="79583-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="79583-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79583-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="79583-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="79583-114">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Delegaten Management-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="79583-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="79583-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="79583-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="79583-116">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="79583-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="79583-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="79583-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="79583-118">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="79583-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="79583-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="79583-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="79583-120">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="79583-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="79583-121">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="79583-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="79583-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="79583-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="79583-123">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="79583-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="79583-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="79583-124">Parent elements</span></span>

<span data-ttu-id="79583-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="79583-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="79583-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="79583-126">Remarks</span></span>

<span data-ttu-id="79583-127">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="79583-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="79583-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="79583-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79583-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="79583-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="79583-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="79583-130">Schema Name</span></span>  <br/> |<span data-ttu-id="79583-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="79583-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="79583-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="79583-132">Validation File</span></span>  <br/> |<span data-ttu-id="79583-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="79583-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="79583-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="79583-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="79583-135">False</span><span class="sxs-lookup"><span data-stu-id="79583-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79583-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79583-136">See also</span></span>



[<span data-ttu-id="79583-137">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="79583-137">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="79583-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="79583-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

