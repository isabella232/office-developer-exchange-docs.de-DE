---
title: SetUserOofSettingsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetUserOofSettingsResponse
api_type:
- schema
ms.assetid: 8aa4025b-38df-4d63-a6a5-c3b932bec26e
description: Das SetUserOofSettingsResponse-Element enthält das Ergebnis der versucht, eine Nachricht SetUserOofSettingsRequest.
ms.openlocfilehash: ab2eaaad1b7b094baad724ec56f4c26280f1f15f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831471"
---
# <a name="setuseroofsettingsresponse"></a><span data-ttu-id="66cc6-103">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="66cc6-103">SetUserOofSettingsResponse</span></span>

<span data-ttu-id="66cc6-104">Das **SetUserOofSettingsResponse** -Element enthält das Ergebnis der versucht, eine Nachricht [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="66cc6-104">The **SetUserOofSettingsResponse** element contains the result of a [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) message attempt.</span></span> 
  
```xml
<SetUserOofSettingsResponse>
   <ResponseMessage>...</ResponseMessage>
<SetUserOofSettingsResponse>
```

 <span data-ttu-id="66cc6-105">**SetUserOofSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="66cc6-105">**SetUserOofSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66cc6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="66cc6-106">Attributes and elements</span></span>

<span data-ttu-id="66cc6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="66cc6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66cc6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="66cc6-108">Attributes</span></span>

<span data-ttu-id="66cc6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="66cc6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66cc6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66cc6-110">Child elements</span></span>

|<span data-ttu-id="66cc6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="66cc6-111">**Element**</span></span>|<span data-ttu-id="66cc6-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66cc6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66cc6-113">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="66cc6-113">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="66cc6-114">Enthält beschreibende Informationen über den Antwortstatus.</span><span class="sxs-lookup"><span data-stu-id="66cc6-114">Provides descriptive information about the response status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="66cc6-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66cc6-115">Parent elements</span></span>

<span data-ttu-id="66cc6-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="66cc6-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66cc6-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="66cc6-117">Remarks</span></span>

<span data-ttu-id="66cc6-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="66cc6-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66cc6-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="66cc6-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66cc6-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="66cc6-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="66cc6-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="66cc6-121">Schema Name</span></span>  <br/> |<span data-ttu-id="66cc6-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="66cc6-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="66cc6-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="66cc6-123">Validation File</span></span>  <br/> |<span data-ttu-id="66cc6-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="66cc6-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="66cc6-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="66cc6-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="66cc6-126">False</span><span class="sxs-lookup"><span data-stu-id="66cc6-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66cc6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66cc6-127">See also</span></span>



[<span data-ttu-id="66cc6-128">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="66cc6-128">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

