---
title: AddNewTelUriContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cff8ef19-3e19-4107-9b35-c8a2b87a41bc
description: Das AddNewTelUriContactToGroup-Element gibt die Eingabedaten für den AddNewTelUriContactToGroup WSDL-Vorgang.
ms.openlocfilehash: d99d557530397aa9edd2c23b595bdcb348783dd4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757234"
---
# <a name="addnewteluricontacttogroup"></a><span data-ttu-id="d9c65-103">AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="d9c65-103">AddNewTelUriContactToGroup</span></span>

<span data-ttu-id="d9c65-104">Das **AddNewTelUriContactToGroup** -Element gibt die Eingabedaten für den **AddNewTelUriContactToGroup** WSDL-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d9c65-104">The **AddNewTelUriContactToGroup** element specifies the input data for the **AddNewTelUriContactToGroup** WSDL operation.</span></span> 
  
```XML
<AddNewTelUriContactToGroup>
   <TelUriAddress/>
   <ImContactSipUriAddress/>
   <ImTelephoneNumber/>
   <GroupId/>
</AddNewTelUriContactToGroup>
```

 <span data-ttu-id="d9c65-105">**AddNewTelUriContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="d9c65-105">**AddNewTelUriContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9c65-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d9c65-106">Attributes and elements</span></span>

<span data-ttu-id="d9c65-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d9c65-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9c65-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d9c65-108">Attributes</span></span>

<span data-ttu-id="d9c65-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9c65-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9c65-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9c65-110">Child elements</span></span>

<span data-ttu-id="d9c65-111">[TelUriAddress](teluriaddress.md) | [ImContactSipUriAddress](imcontactsipuriaddress.md) | [ImTelephoneNumber](imtelephonenumber.md) | [GroupId](groupid.md)</span><span class="sxs-lookup"><span data-stu-id="d9c65-111">[TelUriAddress](teluriaddress.md) | [ImContactSipUriAddress](imcontactsipuriaddress.md) | [ImTelephoneNumber](imtelephonenumber.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d9c65-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9c65-112">Parent elements</span></span>

<span data-ttu-id="d9c65-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9c65-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9c65-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9c65-114">Remarks</span></span>

<span data-ttu-id="d9c65-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d9c65-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d9c65-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d9c65-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9c65-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d9c65-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9c65-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9c65-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d9c65-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d9c65-119">Schema name</span></span>  <br/> |<span data-ttu-id="d9c65-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d9c65-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d9c65-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d9c65-121">Validation file</span></span>  <br/> |<span data-ttu-id="d9c65-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d9c65-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d9c65-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d9c65-123">Can be empty</span></span>  <br/> |<span data-ttu-id="d9c65-124">False</span><span class="sxs-lookup"><span data-stu-id="d9c65-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9c65-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9c65-125">See also</span></span>

- [<span data-ttu-id="d9c65-126">AddNewTelUriContactToGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d9c65-126">AddNewTelUriContactToGroup operation</span></span>](addnewteluricontacttogroup-operation.md)
- [<span data-ttu-id="d9c65-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d9c65-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

