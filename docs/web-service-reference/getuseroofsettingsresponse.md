---
title: GetUserOofSettingsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserOofSettingsResponse
api_type:
- schema
ms.assetid: 011cb38b-da3c-4b1b-8836-a6b212b511f6
description: Das GetUserOofSettingsResponse-Element enthält die Antwortnachricht und die Einstellungen von Office (OOF) für einen Benutzer.
ms.openlocfilehash: dc63b6d54471973ce5961a5a5ad6a23f6521fc0e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829693"
---
# <a name="getuseroofsettingsresponse"></a><span data-ttu-id="5414c-103">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="5414c-103">GetUserOofSettingsResponse</span></span>

<span data-ttu-id="5414c-104">Das **GetUserOofSettingsResponse** -Element enthält die Antwortnachricht und die Einstellungen von Office (OOF) für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="5414c-104">The **GetUserOofSettingsResponse** element contains the response message and the Out of Office (OOF) settings for a user.</span></span> 
  
```xml
<GetUserOofSettingsResponse>
   <ResponseMessage>...</ResponseMessage>
   <OofSettings>...</OofSettings>
   <AllowExternalOof>...</AllowExternalOof>
</GetUserOofSettingsResponse>
```

 <span data-ttu-id="5414c-105">**GetUserOofSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="5414c-105">**GetUserOofSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5414c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5414c-106">Attributes and elements</span></span>

<span data-ttu-id="5414c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5414c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5414c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5414c-108">Attributes</span></span>

<span data-ttu-id="5414c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5414c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5414c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5414c-110">Child elements</span></span>

|<span data-ttu-id="5414c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5414c-111">**Element**</span></span>|<span data-ttu-id="5414c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5414c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5414c-113">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5414c-113">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="5414c-114">Enthält beschreibende Informationen über den Antwortstatus.</span><span class="sxs-lookup"><span data-stu-id="5414c-114">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="5414c-115">OofSettings</span><span class="sxs-lookup"><span data-stu-id="5414c-115">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="5414c-116">Enthält die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="5414c-116">Contains the OOF settings.</span></span>  <br/> |
|[<span data-ttu-id="5414c-117">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="5414c-117">AllowExternalOof</span></span>](allowexternaloof.md) <br/> |<span data-ttu-id="5414c-118">Enthält einen Wert, der angibt, den externe OOF Testnachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="5414c-118">Contains a value that identifies to whom external OOF messages are sent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5414c-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5414c-119">Parent elements</span></span>

<span data-ttu-id="5414c-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="5414c-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5414c-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5414c-121">Remarks</span></span>

<span data-ttu-id="5414c-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5414c-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5414c-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5414c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5414c-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="5414c-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5414c-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5414c-125">Schema Name</span></span>  <br/> |<span data-ttu-id="5414c-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5414c-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5414c-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5414c-127">Validation File</span></span>  <br/> |<span data-ttu-id="5414c-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5414c-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5414c-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5414c-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="5414c-130">False</span><span class="sxs-lookup"><span data-stu-id="5414c-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5414c-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5414c-131">See also</span></span>



[<span data-ttu-id="5414c-132">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5414c-132">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="5414c-133">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5414c-133">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

