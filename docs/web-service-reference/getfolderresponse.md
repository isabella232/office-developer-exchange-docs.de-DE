---
title: GetFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolderResponse
api_type:
- schema
ms.assetid: 47abeec8-78dd-4297-8525-099174ec880d
description: Das GetFolderResponse-Element definiert eine Antwort auf eine GetFolder an.
ms.openlocfilehash: 0831224f1f649f3febf20fac2d7e987de03edcb8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758685"
---
# <a name="getfolderresponse"></a><span data-ttu-id="9e3e2-103">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="9e3e2-103">GetFolderResponse</span></span>

<span data-ttu-id="9e3e2-104">Das **GetFolderResponse** -Element definiert eine Antwort auf eine GetFolder an.</span><span class="sxs-lookup"><span data-stu-id="9e3e2-104">The **GetFolderResponse** element defines a response to a GetFolder request.</span></span> 
  
```xml
<GetFolderResponse>
   <ResponseMessages/>
</GetFolderResponse>
```

 <span data-ttu-id="9e3e2-105">**GetFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="9e3e2-105">**GetFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9e3e2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9e3e2-106">Attributes and elements</span></span>

<span data-ttu-id="9e3e2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9e3e2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9e3e2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9e3e2-108">Attributes</span></span>

<span data-ttu-id="9e3e2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9e3e2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9e3e2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e3e2-110">Child elements</span></span>

|<span data-ttu-id="9e3e2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9e3e2-111">**Element**</span></span>|<span data-ttu-id="9e3e2-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e3e2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e3e2-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9e3e2-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9e3e2-114">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9e3e2-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9e3e2-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e3e2-115">Parent elements</span></span>

<span data-ttu-id="9e3e2-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="9e3e2-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9e3e2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e3e2-117">Remarks</span></span>

<span data-ttu-id="9e3e2-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9e3e2-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9e3e2-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9e3e2-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e3e2-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e3e2-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9e3e2-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9e3e2-121">Schema name</span></span>  <br/> |<span data-ttu-id="9e3e2-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9e3e2-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9e3e2-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9e3e2-123">Validation file</span></span>  <br/> |<span data-ttu-id="9e3e2-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9e3e2-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9e3e2-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9e3e2-125">Can be empty</span></span>  <br/> |<span data-ttu-id="9e3e2-126">False</span><span class="sxs-lookup"><span data-stu-id="9e3e2-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e3e2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e3e2-127">See also</span></span>



[<span data-ttu-id="9e3e2-128">GetFolder</span><span class="sxs-lookup"><span data-stu-id="9e3e2-128">GetFolder</span></span>](getfolder.md)
  
[<span data-ttu-id="9e3e2-129">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="9e3e2-129">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="9e3e2-130">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9e3e2-130">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)

