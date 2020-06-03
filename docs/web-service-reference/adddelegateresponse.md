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
description: Das AddDelegateResponse-Element enthält den Status und das Ergebnis einer AddDelegate-Vorgangsanforderung.
ms.openlocfilehash: 1c38563ab38facf89fd5eab119542374949244c2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466458"
---
# <a name="adddelegateresponse"></a><span data-ttu-id="02475-103">AddDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="02475-103">AddDelegateResponse</span></span>

<span data-ttu-id="02475-104">Das **AddDelegateResponse** -Element enthält den Status und das Ergebnis einer [AddDelegate-Vorgangs](adddelegate-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="02475-104">The **AddDelegateResponse** element contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request.</span></span> 
  
```xml
<AddDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</AddDelegateResponse>
```

 <span data-ttu-id="02475-105">**AddDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="02475-105">**AddDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="02475-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="02475-106">Attributes and elements</span></span>

<span data-ttu-id="02475-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="02475-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02475-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="02475-108">Attributes</span></span>

<span data-ttu-id="02475-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="02475-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02475-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02475-110">Child elements</span></span>

|<span data-ttu-id="02475-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="02475-111">**Element**</span></span>|<span data-ttu-id="02475-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="02475-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02475-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="02475-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="02475-114">Enthält die Antwortnachrichten für eine Verwaltungsanforderung für Exchange Webdienste Delegate.</span><span class="sxs-lookup"><span data-stu-id="02475-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="02475-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="02475-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="02475-116">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="02475-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="02475-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="02475-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="02475-118">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="02475-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="02475-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="02475-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="02475-120">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="02475-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="02475-121">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="02475-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="02475-122">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="02475-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="02475-123">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="02475-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="02475-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02475-124">Parent elements</span></span>

<span data-ttu-id="02475-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="02475-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02475-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02475-126">Remarks</span></span>

<span data-ttu-id="02475-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="02475-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02475-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="02475-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02475-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="02475-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="02475-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="02475-130">Schema Name</span></span>  <br/> |<span data-ttu-id="02475-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="02475-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="02475-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="02475-132">Validation File</span></span>  <br/> |<span data-ttu-id="02475-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="02475-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="02475-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="02475-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="02475-135">False</span><span class="sxs-lookup"><span data-stu-id="02475-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02475-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02475-136">See also</span></span>

- [<span data-ttu-id="02475-137">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="02475-137">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="02475-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="02475-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="02475-139">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="02475-139">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

