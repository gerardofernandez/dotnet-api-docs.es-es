---
ms.openlocfilehash: 733bfb4740f3f274ba9ebb396749d313907d5fa6
ms.sourcegitcommit: 1bb00d2f4343e73ae8d58668f02297a3cf10a4c1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2019
ms.locfileid: "63870371"
---
<span data-ttu-id="3119f-101">A partir de .NET Framework 4.7, este método se autentica mediante <xref:System.Security.Authentication.SslProtocols.None>, que permite al sistema operativo elegir el mejor protocolo para usar y bloquear los protocolos que no sean seguros.</span><span class="sxs-lookup"><span data-stu-id="3119f-101">Starting with .NET Framework 4.7, this method authenticates using <xref:System.Security.Authentication.SslProtocols.None>, which allows the operating system to choose the best protocol to use, and to block protocols that are not secure.</span></span> <span data-ttu-id="3119f-102">En .NET Framework 4.6 (y .NET Framework 4.5 con las revisiones de seguridad más recientes instaladas), las versiones de los protocolos TLS/SSL permitidas son 1.0, 1.1 y 1.2 (a menos que edite el Registro de Windows para deshabilitar la criptografía robusta).</span><span class="sxs-lookup"><span data-stu-id="3119f-102">In .NET Framework 4.6 (and .NET Framework 4.5 with the latest security patches installed), the allowed TLS/SSL protocols versions are 1.2, 1.1, and 1.0 (unless you disable strong cryptography by editing the Windows Registry).</span></span>
