---
title: ASP.NET Core 시작
author: rick-anderson
description: ASP.NET Core를 사용하여 간단한 Hello World 앱을 만들고 실행하는 빠른 자습서입니다.
ms.author: riande
ms.custom: mvc
ms.date: 12/01/2018
uid: getting-started
ms.openlocfilehash: 29a328b610b0a6e1616cd6ebc70a8fa3e515eb92
ms.sourcegitcommit: 9bb58d7c8dad4bbd03419bcc183d027667fefa20
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/04/2018
ms.locfileid: "52861708"
---
# <a name="tutorial-get-started-with-aspnet-core"></a>자습서: ASP.NET Core 시작

이 자습서에서는 .NET Core 명령줄 인터페이스를 사용하여 ASP.NET Core 웹앱을 만드는 방법을 보여 줍니다.

다음을 수행하는 방법을 알아봅니다.

> [!div class="checklist"]
> * 웹앱 프로젝트를 만듭니다.
> * 로컬 HTTPS를 사용하도록 설정합니다.
> * 앱을 실행합니다.
> * Razor 페이지를 편집합니다.

마지막에는 로컬 머신에서 작업 웹앱이 실행됩니다.

![웹앱 홈페이지](_static/home-page.png)

## <a name="prerequisites"></a>전제 조건

[!INCLUDE [](~/includes/2.1-SDK.md)]를 설치합니다.

## <a name="create-a-web-app-project"></a>웹앱 프로젝트 만들기

명령 셸을 열고 다음 명령을 입력합니다.

```console
dotnet new webapp -o aspnetcoreapp
```

## <a name="enable-local-https"></a>로컬 HTTPS 사용

HTTPS 개발 인증서 신뢰:

# <a name="windowstabwindows"></a>[Windows](#tab/windows)

```console
dotnet dev-certs https --trust
```

이전 명령으로 인해 다음 대화 상자가 표시됩니다.

![보안 경고 대화 상자](_static/cert.png)

개발 인증서를 신뢰하는 데 동의하는 경우 **예**를 선택합니다.

# <a name="macostabmacos"></a>[macOS](#tab/macos)

```console
dotnet dev-certs https --trust
```

이전 명령으로 인해 다음 메시지가 표시됩니다.

*HTTPS 개발 인증서를 신뢰해야 합니다. 인증서를 신뢰할 수 없는 경우*  `'sudo security add-trusted-cert -d -r trustRoot -k /Library/Keychains/System.keychain <<certificate>>'` 명령을 실행합니다.  
*이 명령은 시스템 키 집합에 인증서를 설치하기 위해 암호를 묻는 메시지를 표시할 수 있습니다.

암호:*

개발 인증서를 신뢰하는 데 동의하는 경우 암호를 입력합니다.

# <a name="linuxtablinux"></a>[Linux](#tab/linux)

HTTPS 개발 인증서를 신뢰하는 방법은 Linux 배포에 대한 설명서를 참조하세요.

---

## <a name="run-the-app"></a>앱 실행

다음 명령을 실행합니다.

```console
cd aspnetcoreapp
dotnet run
```

[https://localhost:5001](https://localhost:5001)로 이동합니다. **동의**를 클릭하여 개인 정보 및 쿠키 정책에 동의합니다. 이 앱은 개인 정보를 보관하지 않습니다.

## <a name="edit-a-razor-page"></a>Razor 페이지 편집

*Pages/About.cshtml*을 열고 다음에서 강조 표시된 영역처럼 페이지를 수정합니다.

[!code-cshtml[](sample/getting-started/about.cshtml?highlight=9)]

[https://localhost:5001/About](https://localhost:5001/About)으로 이동하여 수정한 내용이 표시되는지 확인합니다.

## <a name="next-steps"></a>다음 단계

본 자습서에서는 다음 작업에 관한 방법을 학습했습니다.

> [!div class="checklist"]
> * 웹앱 프로젝트를 만듭니다.
> * 로컬 HTTPS를 사용하도록 설정합니다.
> * 프로젝트를 실행합니다.
> * 페이지를 수정합니다.

ASP.NET Core에 대한 자세한 내용은 다음을 참조하세요.

> [!div class="nextstepaction"]
> <xref:index>

> [!NOTE]
> 현재 ASP.NET Core 목차에 대해 제안된 새로운 구조의 유용성을 테스트하고 있습니다. 잠시 시간을 내어 현행 및 제안된 목차에서 7가지 항목을 찾는 연습에 참여할 의향이 있으시면 [여기를 클릭하여 연구에 참여해 주세요](https://dpk4xbh5.optimalworkshop.com/treejack/aa11wn82).
