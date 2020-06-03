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
description: Das SetUserOofSettingsResponse-Element enthält das Ergebnis eines SetUserOofSettingsRequest-Nachrichten Versuchs.
ms.openlocfilehash: 9b02d905f82488965f5ae0514a52eb6062aaff7d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466129"
---
# <a name="setuseroofsettingsresponse"></a><span data-ttu-id="7d919-103">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="7d919-103">SetUserOofSettingsResponse</span></span>

<span data-ttu-id="7d919-104">Das **SetUserOofSettingsResponse** -Element enthält das Ergebnis eines [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) -Nachrichten Versuchs.</span><span class="sxs-lookup"><span data-stu-id="7d919-104">The **SetUserOofSettingsResponse** element contains the result of a [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) message attempt.</span></span> 
  
```xml
<SetUserOofSettingsResponse>
   <ResponseMessage>...</ResponseMessage>
<SetUserOofSettingsResponse>
```

 <span data-ttu-id="7d919-105">**SetUserOofSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="7d919-105">**SetUserOofSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7d919-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7d919-106">Attributes and elements</span></span>

<span data-ttu-id="7d919-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7d919-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d919-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7d919-108">Attributes</span></span>

<span data-ttu-id="7d919-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7d919-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7d919-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7d919-110">Child elements</span></span>

|<span data-ttu-id="7d919-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7d919-111">**Element**</span></span>|<span data-ttu-id="7d919-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7d919-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7d919-113">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7d919-113">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="7d919-114">Enthält beschreibende Informationen zum Antwortstatus.</span><span class="sxs-lookup"><span data-stu-id="7d919-114">Provides descriptive information about the response status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7d919-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7d919-115">Parent elements</span></span>

<span data-ttu-id="7d919-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="7d919-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7d919-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d919-117">Remarks</span></span>

<span data-ttu-id="7d919-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="7d919-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7d919-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7d919-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d919-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d919-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7d919-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7d919-121">Schema Name</span></span>  <br/> |<span data-ttu-id="7d919-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7d919-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7d919-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7d919-123">Validation File</span></span>  <br/> |<span data-ttu-id="7d919-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7d919-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7d919-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7d919-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="7d919-126">False</span><span class="sxs-lookup"><span data-stu-id="7d919-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d919-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d919-127">See also</span></span>



[<span data-ttu-id="7d919-128">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7d919-128">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

