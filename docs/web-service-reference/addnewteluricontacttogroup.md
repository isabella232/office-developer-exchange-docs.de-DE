---
title: AddNewTelUriContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cff8ef19-3e19-4107-9b35-c8a2b87a41bc
description: Das AddNewTelUriContactToGroup-Element gibt die Eingabedaten für den AddNewTelUriContactToGroup-WSDL-Vorgang an.
ms.openlocfilehash: 151c5b1dab7a3ffc9630fb4e4192b90bd1d4ae38
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464931"
---
# <a name="addnewteluricontacttogroup"></a><span data-ttu-id="7d408-103">AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="7d408-103">AddNewTelUriContactToGroup</span></span>

<span data-ttu-id="7d408-104">Das **AddNewTelUriContactToGroup** -Element gibt die Eingabedaten für den **AddNewTelUriContactToGroup** -WSDL-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="7d408-104">The **AddNewTelUriContactToGroup** element specifies the input data for the **AddNewTelUriContactToGroup** WSDL operation.</span></span> 
  
```XML
<AddNewTelUriContactToGroup>
   <TelUriAddress/>
   <ImContactSipUriAddress/>
   <ImTelephoneNumber/>
   <GroupId/>
</AddNewTelUriContactToGroup>
```

 <span data-ttu-id="7d408-105">**AddNewTelUriContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="7d408-105">**AddNewTelUriContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7d408-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7d408-106">Attributes and elements</span></span>

<span data-ttu-id="7d408-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7d408-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d408-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7d408-108">Attributes</span></span>

<span data-ttu-id="7d408-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7d408-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7d408-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7d408-110">Child elements</span></span>

<span data-ttu-id="7d408-111">[TelUriAddress](teluriaddress.md)  |  [ImContactSipUriAddress](imcontactsipuriaddress.md)  |  [ImTelephoneNumber](imtelephonenumber.md)  |  [Gruppen](groupid.md) -Nr</span><span class="sxs-lookup"><span data-stu-id="7d408-111">[TelUriAddress](teluriaddress.md) | [ImContactSipUriAddress](imcontactsipuriaddress.md) | [ImTelephoneNumber](imtelephonenumber.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7d408-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7d408-112">Parent elements</span></span>

<span data-ttu-id="7d408-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="7d408-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7d408-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d408-114">Remarks</span></span>

<span data-ttu-id="7d408-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7d408-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7d408-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7d408-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7d408-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7d408-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d408-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d408-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7d408-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7d408-119">Schema name</span></span>  <br/> |<span data-ttu-id="7d408-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7d408-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7d408-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7d408-121">Validation file</span></span>  <br/> |<span data-ttu-id="7d408-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7d408-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7d408-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7d408-123">Can be empty</span></span>  <br/> |<span data-ttu-id="7d408-124">False</span><span class="sxs-lookup"><span data-stu-id="7d408-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d408-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d408-125">See also</span></span>

- [<span data-ttu-id="7d408-126">AddNewTelUriContactToGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7d408-126">AddNewTelUriContactToGroup operation</span></span>](addnewteluricontacttogroup-operation.md)
- [<span data-ttu-id="7d408-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7d408-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

