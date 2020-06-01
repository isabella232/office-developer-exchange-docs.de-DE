---
title: GetPasswordExpirationDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4f958ed-9cf4-4ebf-9b01-e2df9a7cbd63
description: Das GetPasswordExpirationDate-Element definiert eine Anforderung zum Abrufen des Kennwortablauf Datums für ein e-Mail-Konto. Dieses Element ist das Basiselement für den GetPasswordExpirationDate-Vorgangs Vorgang.
ms.openlocfilehash: ececbf51f71c7d87705d727229fce2314d922efb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456493"
---
# <a name="getpasswordexpirationdate"></a><span data-ttu-id="ff662-104">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="ff662-104">GetPasswordExpirationDate</span></span>

<span data-ttu-id="ff662-105">Das **GetPasswordExpirationDate** -Element definiert eine Anforderung zum Abrufen des Kennwortablauf Datums für ein e-Mail-Konto.</span><span class="sxs-lookup"><span data-stu-id="ff662-105">The **GetPasswordExpirationDate** element defines a request to get the password expiration date for an email account.</span></span> <span data-ttu-id="ff662-106">Dieses Element ist das Basiselement für den [GetPasswordExpirationDate-Vorgangs](getpasswordexpirationdate-operation.md) Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ff662-106">This element is the base element for the [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) operation.</span></span> 
  
```XML
<GetPasswordExpirationDate>
    <MailboxSmtpAddress/>
</GetPasswordExpirationDate>
```

 <span data-ttu-id="ff662-107">**GetPasswordExpirationDateType**</span><span class="sxs-lookup"><span data-stu-id="ff662-107">**GetPasswordExpirationDateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff662-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ff662-108">Attributes and elements</span></span>

<span data-ttu-id="ff662-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ff662-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff662-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ff662-110">Attributes</span></span>

<span data-ttu-id="ff662-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ff662-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ff662-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff662-112">Child elements</span></span>

|<span data-ttu-id="ff662-113">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="ff662-113">**Element name**</span></span>|<span data-ttu-id="ff662-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff662-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff662-115">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="ff662-115">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md) <br/> |<span data-ttu-id="ff662-116">Stellt die e-Mail-Adresse des e-Mail-Kontos dar, für das das Ablaufdatum des Kennworts zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff662-116">Represents the email address of the email account for which the password expiration date is to be returned.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ff662-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff662-117">Parent elements</span></span>

<span data-ttu-id="ff662-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="ff662-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff662-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff662-119">Remarks</span></span>

<span data-ttu-id="ff662-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ff662-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="ff662-121">Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ff662-121">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff662-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ff662-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff662-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff662-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ff662-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ff662-124">Schema Name</span></span>  <br/> |<span data-ttu-id="ff662-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ff662-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ff662-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ff662-126">Validation File</span></span>  <br/> |<span data-ttu-id="ff662-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ff662-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ff662-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ff662-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="ff662-129">False</span><span class="sxs-lookup"><span data-stu-id="ff662-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff662-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff662-130">See also</span></span>



[<span data-ttu-id="ff662-131">GetPasswordExpirationDate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ff662-131">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)


- [<span data-ttu-id="ff662-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ff662-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

