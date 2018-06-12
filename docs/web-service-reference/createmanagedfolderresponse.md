---
title: CreateManagedFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolderResponse
api_type:
- schema
ms.assetid: 99062401-d356-4ce7-a5d0-c8c7aab99912
description: Das CreateManagedFolderResponse-Element definiert eine Antwort auf eine CreateManagedFolder an.
ms.openlocfilehash: fc486a197b7b0a0ed7310dda88d4bf8735f99876
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757794"
---
# <a name="createmanagedfolderresponse"></a><span data-ttu-id="a7e82-103">CreateManagedFolderResponse</span><span class="sxs-lookup"><span data-stu-id="a7e82-103">CreateManagedFolderResponse</span></span>

<span data-ttu-id="a7e82-104">Das **CreateManagedFolderResponse** -Element definiert eine Antwort auf eine CreateManagedFolder an.</span><span class="sxs-lookup"><span data-stu-id="a7e82-104">The **CreateManagedFolderResponse** element defines a response to a CreateManagedFolder request.</span></span> 
  
```xml
<CreateManagedFolderResponse>
   <ResponseMessages/>
</CreateManagedFolderResponse>
```

 <span data-ttu-id="a7e82-105">**CreateManagedFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="a7e82-105">**CreateManagedFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a7e82-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a7e82-106">Attributes and elements</span></span>

<span data-ttu-id="a7e82-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a7e82-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7e82-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a7e82-108">Attributes</span></span>

<span data-ttu-id="a7e82-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a7e82-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a7e82-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7e82-110">Child elements</span></span>

|<span data-ttu-id="a7e82-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a7e82-111">**Element**</span></span>|<span data-ttu-id="a7e82-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7e82-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7e82-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a7e82-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="a7e82-114">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a7e82-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a7e82-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7e82-115">Parent elements</span></span>

<span data-ttu-id="a7e82-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="a7e82-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7e82-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7e82-117">Remarks</span></span>

<span data-ttu-id="a7e82-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a7e82-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7e82-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a7e82-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7e82-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7e82-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a7e82-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a7e82-121">Schema name</span></span>  <br/> |<span data-ttu-id="a7e82-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a7e82-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a7e82-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a7e82-123">Validation file</span></span>  <br/> |<span data-ttu-id="a7e82-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a7e82-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a7e82-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a7e82-125">Can be empty</span></span>  <br/> |<span data-ttu-id="a7e82-126">False</span><span class="sxs-lookup"><span data-stu-id="a7e82-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7e82-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7e82-127">See also</span></span>



[<span data-ttu-id="a7e82-128">CreateManagedFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a7e82-128">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)
  
[<span data-ttu-id="a7e82-129">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="a7e82-129">CreateManagedFolder</span></span>](createmanagedfolder.md)


- [<span data-ttu-id="a7e82-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a7e82-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

