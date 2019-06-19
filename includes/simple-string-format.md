---
ms.openlocfilehash: 483f2c83f4d55aad694ba713c787972178b19e5e
ms.sourcegitcommit: 1bb00d2f4343e73ae8d58668f02297a3cf10a4c1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2019
ms.locfileid: "63872452"
---

Pero al llamar al método **String.Format**, no es necesario centrarse en la sobrecarga concreta que se quiere llamar. En su lugar, se puede llamar al método con un [cadena de formato compuesto](~/docs/standard/base-types/composite-formatting.md) que incluya uno o varios elementos de formato. A cada elemento de formato se le asigna un índice numérico; el primer índice comienza en 0. Además de la cadena inicial, la llamada al método debe tener tantos argumentos adicionales como valores de índice. Por ejemplo, una cadena cuyos elementos de formato tienen los índices 0 y 1 debe tener dos argumentos; una con los índices de 0 a 5 debe tener seis argumentos. Después, el compilador del lenguaje resolverá la llamada de método en una sobrecarga concreta del método **String.Format**.   
 
Para obtener información más detallada sobre el uso del método **String.Format**, vea [Introducción al método String.Format](#Starting) y [¿Qué método se debe llamar?](#FTaskList).    
