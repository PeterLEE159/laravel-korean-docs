---
layout: default
title: "해시(Hashing)"
permalink: /docs/5.0/hashing/
---

# 해시(Hashing)

- [소개](#introduction)
- [기본 사용법](#basic-usage)

<a name="introduction"></a>
## 소개

라라벨의 `Hash` 파사드는 사용자의 암호를 저장하는 데 필요한 안전한 Bcrypt 해싱을 제공합니다. 만약 라라벨 어플리케이션에 포함되어 있는 `AuthController` 컨트롤러를 사용하고 있다면 사용자로부터 입력받은 해시되지 않은 암호를 Bcrypt 된 암호와 비교하여 확인할 수 있습니다.

마찬가지로, 라라벨과 함께 제공되는 사용자 `Registrar` 서비스는 저장된 패스워드를 해시하기 위한 `bcrypt` 함수를 제공합니다.

<div class="chak-comment-wrap"><div class="chak-comment-widget" data-chak-group="laravel" data-chak-apikey="582898af492efbcdd53990e1c6ccb89d-laravel-korean-docs-해시(Hashing)-소개" ><i class="xi-message"></i> <strong>클릭</strong>하여 의견을 공유할 수 있습니다. ( 총 <span class="count"><i class="xi-spinner-5 xi-spin"></i></span>개의 의견이 있습니다. )</div></div>

<a name="basic-usage"></a>
## 기본 사용법

#### Bcrypt를 사용해서 패스워드를 해시하기

	$password = Hash::make('secret');

`bcrypt` 헬퍼함수를 사용할 수도 있습니다:

	$password = bcrypt('secret');

#### 패스워드에 대한 해시 확인하기

	if (Hash::check('secret', $hashedPassword))
	{
		// The passwords match...
	}

#### 패스워드가 리해시가 필요한지 확인하기

	if (Hash::needsRehash($hashed))
	{
		$hashed = Hash::make('secret');
	}

<div class="chak-comment-wrap"><div class="chak-comment-widget" data-chak-group="laravel" data-chak-apikey="582898af492efbcdd53990e1c6ccb89d-laravel-korean-docs-해시(Hashing)-기본-사용법" ><i class="xi-message"></i> <strong>클릭</strong>하여 의견을 공유할 수 있습니다. ( 총 <span class="count"><i class="xi-spinner-5 xi-spin"></i></span>개의 의견이 있습니다. )</div></div>

