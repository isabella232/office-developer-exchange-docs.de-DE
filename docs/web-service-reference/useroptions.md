---
title: User Options
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1acbb8a3-9110-4427-a06c-7e6e627e969f
description: Das UserOptions-Element gibt die Liste der Abstimmungsoptionen für eine Nachricht an.
ms.openlocfilehash: 2e0bbb373f423bbe9e913775b1f19d06dfd53f5f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526760"
---
# <a name="useroptions"></a><span data-ttu-id="dc2d8-103">User Options</span><span class="sxs-lookup"><span data-stu-id="dc2d8-103">UserOptions</span></span>

<span data-ttu-id="dc2d8-104">Das **USEROPTIONS** -Element gibt die Liste der Abstimmungsoptionen für eine Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="dc2d8-104">The **UserOptions** element specifies the list of voting options on a message.</span></span> 
  
```XML
<UserOptions>
   <VotingOptionData>
</UserOptions>
```

 <span data-ttu-id="dc2d8-105">**ArrayOfVotingOptionDataType**</span><span class="sxs-lookup"><span data-stu-id="dc2d8-105">**ArrayOfVotingOptionDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc2d8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dc2d8-106">Attributes and elements</span></span>

<span data-ttu-id="dc2d8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dc2d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc2d8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dc2d8-108">Attributes</span></span>

<span data-ttu-id="dc2d8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dc2d8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc2d8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc2d8-110">Child elements</span></span>

[<span data-ttu-id="dc2d8-111">VotingOptionData</span><span class="sxs-lookup"><span data-stu-id="dc2d8-111">VotingOptionData</span></span>](votingoptiondata.md)
  
### <a name="parent-elements"></a><span data-ttu-id="dc2d8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc2d8-112">Parent elements</span></span>

[<span data-ttu-id="dc2d8-113">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="dc2d8-113">VotingInformation</span></span>](votinginformation.md)
  
## <a name="remarks"></a><span data-ttu-id="dc2d8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc2d8-114">Remarks</span></span>

<span data-ttu-id="dc2d8-115">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dc2d8-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="dc2d8-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dc2d8-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc2d8-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="dc2d8-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc2d8-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc2d8-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dc2d8-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dc2d8-119">Schema Name</span></span>  <br/> |<span data-ttu-id="dc2d8-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="dc2d8-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="dc2d8-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dc2d8-121">Validation File</span></span>  <br/> |<span data-ttu-id="dc2d8-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dc2d8-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dc2d8-123">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dc2d8-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="dc2d8-124">True</span><span class="sxs-lookup"><span data-stu-id="dc2d8-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc2d8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc2d8-125">See also</span></span>



[<span data-ttu-id="dc2d8-126">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="dc2d8-126">VotingInformation</span></span>](votinginformation.md)


- [<span data-ttu-id="dc2d8-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dc2d8-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

