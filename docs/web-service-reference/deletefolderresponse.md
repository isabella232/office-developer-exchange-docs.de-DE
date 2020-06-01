---
title: DeleteFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolderResponse
api_type:
- schema
ms.assetid: 27578bda-ef0a-4a33-bccc-2c1bc1735424
description: Das DeleteFolderResponse-Element definiert eine Antwort auf eine DeleteFolder-Anforderung.
ms.openlocfilehash: 58b814662c769784c5fd682a9e039863a9787d8d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458488"
---
# <a name="deletefolderresponse"></a><span data-ttu-id="45d97-103">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="45d97-103">DeleteFolderResponse</span></span>

<span data-ttu-id="45d97-104">Das **DeleteFolderResponse** -Element definiert eine Antwort auf eine DeleteFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="45d97-104">The **DeleteFolderResponse** element defines a response to a DeleteFolder request.</span></span> 
  
```xml
<DeleteFolderResponse>
   <ResponseMessages/>
</DeleteFolderResponse>
```

 <span data-ttu-id="45d97-105">**DeleteFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="45d97-105">**DeleteFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="45d97-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="45d97-106">Attributes and elements</span></span>

<span data-ttu-id="45d97-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="45d97-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="45d97-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="45d97-108">Attributes</span></span>

<span data-ttu-id="45d97-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="45d97-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45d97-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45d97-110">Child elements</span></span>

|<span data-ttu-id="45d97-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="45d97-111">**Element**</span></span>|<span data-ttu-id="45d97-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="45d97-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45d97-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="45d97-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="45d97-114">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="45d97-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="45d97-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45d97-115">Parent elements</span></span>

<span data-ttu-id="45d97-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="45d97-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="45d97-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45d97-117">Remarks</span></span>

<span data-ttu-id="45d97-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="45d97-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="45d97-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="45d97-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45d97-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="45d97-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="45d97-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="45d97-121">Schema name</span></span>  <br/> |<span data-ttu-id="45d97-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="45d97-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="45d97-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="45d97-123">Validation file</span></span>  <br/> |<span data-ttu-id="45d97-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="45d97-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="45d97-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="45d97-125">Can be empty</span></span>  <br/> |<span data-ttu-id="45d97-126">False</span><span class="sxs-lookup"><span data-stu-id="45d97-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45d97-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45d97-127">See also</span></span>

- [<span data-ttu-id="45d97-128">DeleteFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="45d97-128">DeleteFolder operation</span></span>](deletefolder-operation.md) 
- [<span data-ttu-id="45d97-129">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="45d97-129">DeleteFolder</span></span>](deletefolder.md)
- [<span data-ttu-id="45d97-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="45d97-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

