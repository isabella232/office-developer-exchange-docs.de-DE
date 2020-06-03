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
description: Das UpdateDelegateResponse-Element enthält den Status und das Ergebnis einer UpdateDelegate-Vorgangsanforderung.
ms.openlocfilehash: 9f11d87ac07dd51a5231d4546fac92e7ca95ad4b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465051"
---
# <a name="updatedelegateresponse"></a><span data-ttu-id="b5ca6-103">UpdateDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="b5ca6-103">UpdateDelegateResponse</span></span>

<span data-ttu-id="b5ca6-104">Das **UpdateDelegateResponse** -Element enthält den Status und das Ergebnis einer [UpdateDelegate-Vorgangs](updatedelegate-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-104">The **UpdateDelegateResponse** element contains the status and result of an [UpdateDelegate operation](updatedelegate-operation.md) request.</span></span> 
  
```xml
<UpdateDelegateResponseMessage>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UpdateDelegateResponseMessage>
```

 <span data-ttu-id="b5ca6-105">**UpdateDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b5ca6-105">**UpdateDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5ca6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b5ca6-106">Attributes and elements</span></span>

<span data-ttu-id="b5ca6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5ca6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b5ca6-108">Attributes</span></span>

<span data-ttu-id="b5ca6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b5ca6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5ca6-110">Child elements</span></span>

|<span data-ttu-id="b5ca6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5ca6-111">**Element**</span></span>|<span data-ttu-id="b5ca6-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b5ca6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b5ca6-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="b5ca6-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="b5ca6-114">Enthält die Antwortnachrichten für eine Verwaltungsanforderung für Exchange Webdienste Delegate.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="b5ca6-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="b5ca6-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b5ca6-116">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="b5ca6-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b5ca6-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="b5ca6-118">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="b5ca6-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b5ca6-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="b5ca6-120">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="b5ca6-121">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="b5ca6-122">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="b5ca6-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="b5ca6-123">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b5ca6-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5ca6-124">Parent elements</span></span>

<span data-ttu-id="b5ca6-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5ca6-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5ca6-126">Remarks</span></span>

<span data-ttu-id="b5ca6-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5ca6-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b5ca6-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5ca6-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5ca6-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b5ca6-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b5ca6-130">Schema Name</span></span>  <br/> |<span data-ttu-id="b5ca6-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b5ca6-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b5ca6-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b5ca6-132">Validation File</span></span>  <br/> |<span data-ttu-id="b5ca6-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b5ca6-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b5ca6-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b5ca6-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="b5ca6-135">False</span><span class="sxs-lookup"><span data-stu-id="b5ca6-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5ca6-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5ca6-136">See also</span></span>



[<span data-ttu-id="b5ca6-137">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b5ca6-137">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="b5ca6-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b5ca6-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

