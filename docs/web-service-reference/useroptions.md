---
title: UserOptions
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1acbb8a3-9110-4427-a06c-7e6e627e969f
description: Das Element UserOptions gibt die Liste der für eine Nachricht Abstimmungsoptionen.
ms.openlocfilehash: 8a5bdbc254e3c0bce8822633d2714bc928f15f13
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839453"
---
# <a name="useroptions"></a><span data-ttu-id="1c5c7-103">UserOptions</span><span class="sxs-lookup"><span data-stu-id="1c5c7-103">UserOptions</span></span>

<span data-ttu-id="1c5c7-104">Das Element **UserOptions** gibt die Liste der für eine Nachricht Abstimmungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="1c5c7-104">The **UserOptions** element specifies the list of voting options on a message.</span></span> 
  
```XML
<UserOptions>
   <VotingOptionData>
</UserOptions>
```

 <span data-ttu-id="1c5c7-105">**ArrayOfVotingOptionDataType**</span><span class="sxs-lookup"><span data-stu-id="1c5c7-105">**ArrayOfVotingOptionDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1c5c7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1c5c7-106">Attributes and elements</span></span>

<span data-ttu-id="1c5c7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1c5c7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c5c7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1c5c7-108">Attributes</span></span>

<span data-ttu-id="1c5c7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1c5c7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1c5c7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c5c7-110">Child elements</span></span>

[<span data-ttu-id="1c5c7-111">VotingOptionData</span><span class="sxs-lookup"><span data-stu-id="1c5c7-111">VotingOptionData</span></span>](votingoptiondata.md)
  
### <a name="parent-elements"></a><span data-ttu-id="1c5c7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c5c7-112">Parent elements</span></span>

[<span data-ttu-id="1c5c7-113">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="1c5c7-113">VotingInformation</span></span>](votinginformation.md)
  
## <a name="remarks"></a><span data-ttu-id="1c5c7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c5c7-114">Remarks</span></span>

<span data-ttu-id="1c5c7-115">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1c5c7-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="1c5c7-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1c5c7-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1c5c7-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1c5c7-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c5c7-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c5c7-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1c5c7-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1c5c7-119">Schema Name</span></span>  <br/> |<span data-ttu-id="1c5c7-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1c5c7-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="1c5c7-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1c5c7-121">Validation File</span></span>  <br/> |<span data-ttu-id="1c5c7-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1c5c7-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1c5c7-123">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1c5c7-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="1c5c7-124">True</span><span class="sxs-lookup"><span data-stu-id="1c5c7-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c5c7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c5c7-125">See also</span></span>



[<span data-ttu-id="1c5c7-126">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="1c5c7-126">VotingInformation</span></span>](votinginformation.md)


- [<span data-ttu-id="1c5c7-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1c5c7-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

