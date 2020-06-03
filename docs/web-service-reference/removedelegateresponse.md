---
title: RemoveDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveDelegateResponse
api_type:
- schema
ms.assetid: eef56c53-d0a7-4342-9ce6-4dbb6b1a1369
description: Das RemoveDelegateResponse-Element enthält den Status und das Ergebnis einer RemoveDelegate-Vorgangsanforderung.
ms.openlocfilehash: 4c7a8b81528435b72576c116bc97f611544c24d6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468936"
---
# <a name="removedelegateresponse"></a><span data-ttu-id="46873-103">RemoveDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="46873-103">RemoveDelegateResponse</span></span>

<span data-ttu-id="46873-104">Das **RemoveDelegateResponse** -Element enthält den Status und das Ergebnis einer [RemoveDelegate-Vorgangs](removedelegate-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="46873-104">The **RemoveDelegateResponse** element contains the status and result of a [RemoveDelegate operation](removedelegate-operation.md) request.</span></span> 
  
```xml
<RemoveDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RemoveDelegateResponse>
```

 <span data-ttu-id="46873-105">**RemoveDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="46873-105">**RemoveDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="46873-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="46873-106">Attributes and elements</span></span>

<span data-ttu-id="46873-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="46873-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46873-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="46873-108">Attributes</span></span>

<span data-ttu-id="46873-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="46873-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46873-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46873-110">Child elements</span></span>

|<span data-ttu-id="46873-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="46873-111">**Element**</span></span>|<span data-ttu-id="46873-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46873-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46873-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="46873-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="46873-114">Enthält die Antwortnachrichten für eine Verwaltungsanforderung für Exchange Webdienste Delegate.</span><span class="sxs-lookup"><span data-stu-id="46873-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="46873-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="46873-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="46873-116">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="46873-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="46873-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="46873-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="46873-118">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="46873-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="46873-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="46873-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="46873-120">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="46873-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="46873-121">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="46873-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="46873-122">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="46873-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="46873-123">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="46873-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="46873-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46873-124">Parent elements</span></span>

<span data-ttu-id="46873-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="46873-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46873-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46873-126">Remarks</span></span>

<span data-ttu-id="46873-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="46873-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46873-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="46873-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46873-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="46873-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="46873-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="46873-130">Schema Name</span></span>  <br/> |<span data-ttu-id="46873-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="46873-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="46873-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="46873-132">Validation File</span></span>  <br/> |<span data-ttu-id="46873-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="46873-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="46873-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="46873-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="46873-135">False</span><span class="sxs-lookup"><span data-stu-id="46873-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46873-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46873-136">See also</span></span>



[<span data-ttu-id="46873-137">RemoveDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="46873-137">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="46873-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="46873-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

