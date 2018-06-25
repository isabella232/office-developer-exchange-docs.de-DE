---
title: AddDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AddDelegateResponse
api_type:
- schema
ms.assetid: d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429
description: Das AddDelegateResponse-Element enthält den Status und das Ergebnis einer AddDelegate Vorgang Anforderung.
ms.openlocfilehash: a1d56e9994b3a7916fe0fbe40be1e6d8ff473730
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757218"
---
# <a name="adddelegateresponse"></a><span data-ttu-id="02b25-103">AddDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="02b25-103">AddDelegateResponse</span></span>

<span data-ttu-id="02b25-104">Das **AddDelegateResponse** -Element enthält den Status und das Ergebnis einer Anforderung [AddDelegate-Vorgang](adddelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="02b25-104">The **AddDelegateResponse** element contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request.</span></span> 
  
```xml
<AddDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</AddDelegateResponse>
```

 <span data-ttu-id="02b25-105">**AddDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="02b25-105">**AddDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="02b25-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="02b25-106">Attributes and elements</span></span>

<span data-ttu-id="02b25-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="02b25-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02b25-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="02b25-108">Attributes</span></span>

<span data-ttu-id="02b25-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="02b25-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02b25-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02b25-110">Child elements</span></span>

|<span data-ttu-id="02b25-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="02b25-111">**Element**</span></span>|<span data-ttu-id="02b25-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="02b25-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02b25-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="02b25-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="02b25-114">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Delegaten Management-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="02b25-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="02b25-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="02b25-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="02b25-116">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="02b25-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="02b25-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="02b25-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="02b25-118">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="02b25-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="02b25-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="02b25-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="02b25-120">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="02b25-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="02b25-121">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="02b25-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="02b25-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="02b25-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="02b25-123">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="02b25-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="02b25-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02b25-124">Parent elements</span></span>

<span data-ttu-id="02b25-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="02b25-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02b25-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="02b25-126">Remarks</span></span>

<span data-ttu-id="02b25-127">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="02b25-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02b25-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="02b25-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02b25-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="02b25-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="02b25-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="02b25-130">Schema Name</span></span>  <br/> |<span data-ttu-id="02b25-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="02b25-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="02b25-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="02b25-132">Validation File</span></span>  <br/> |<span data-ttu-id="02b25-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="02b25-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="02b25-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="02b25-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="02b25-135">False</span><span class="sxs-lookup"><span data-stu-id="02b25-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02b25-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02b25-136">See also</span></span>

- [<span data-ttu-id="02b25-137">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="02b25-137">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="02b25-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="02b25-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="02b25-139">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="02b25-139">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

