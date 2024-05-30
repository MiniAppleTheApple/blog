---
title: "Naming Rule"
date: 2024-05-26T19:43:10-03:00
draft: false 
---

# Introduction

Many people distressed to name their varabiels, but many time, it isn't effective as expected. Sometimes too long, or maybe too short.In other hand, there are a group of people who don't care about the naming rule. They made someone mad, so the person gave you this blog post.

# 重構

名字取的不算好的話也可以進行重構。如果你並不瞭解什麼是重構，大概可以理解成把你的代碼重新整理一下。重構是一個回去看自己代碼有沒有能讓讀者更容易懂的一個過程。

## 太過執着於完美的名字

其實對程序員來說，很難在短時間內想出一個好的名字，如果太過於執着於完美的名字，則有可能在想名字這邊想太久。項目不等人，我們不會有這麼多時間來去想名字，而且很多時候就算付出了時間也很難想出一個好名字，而想到名字的時候，我們也可能把我們的靈感給忘了。所以我認爲實現功能的時候可以使用一些比較「**簡陋的名字**」，但不代表這樣就好了，你還需要在實現完一部分後回去改成「**比較好的名字**」。

## 註解

位於「**看不懂的名字**」和「**看得懂得名字**」之間，可以透過註解可以讓「**看不懂的名字**」變得更好懂，但不代表說你不需要去將他轉換成「**看得懂得名字**」。註解出了讓閱讀者理解以外，也可以讓閱讀者幫你去想名字。

# 用詞 

## 單詞量太少

這是很多非英文母語者會遇到的問題，我的解決方法是：大概列出幾個關鍵詞，對他們按照邏輯的進行組合。

## 一致性

使用相同的名詞來表示相同的概念。例如說：我用list來代表動態列陣，而不是array。這個情況下，我如果再使用不同的名詞，例如array來表示動態列陣，讀者會誤認爲是不同的東西。在這個情況下，一般會將array誤認成大小固定的列陣。

# 情景

情景有時候提供的資訊就已經足夠，並不需要提供多餘的資訊。

## 函數

在一個有回傳值函數裏面，如果存在一個變數，它名爲result的話，讀者大概就已經知道他是這個函數的回傳值，並不需要在前面加上函數的名字。舉例，在這個情況下：

```go
package array

func SumOfArray(array []int) int {
    sumOfArrayResult := 0
    for _, v := range array {
        sumOfArrayResult += v
    }
    return sumOfArrayResult
}
```

更好的方案應該會是

```go
package array

func SumOfArray(array []int) int {
    result := 0
    for _, v := range array {
        result += v
    }
    return result
}
```

這樣你在不減少資訊的情況下，簡化了變數的名字。

> 其實也可以取名爲`sum`，但爲了演示「情景」的重要性就沒有這麼做了。

## 模組/命名空間/包/類別/等等

由於類似的東西有太多名字，所以我們先用go的package（包）來舉例。如果有稍微想過的應該也會發現一件事，如果我們的package其實叫array。我們並不需要去寫`ofArray`。

```go
package array

func Sum(array []int) int {
    result := 0
    for _, v := range array {
        result += v
    }
    return result
}
```

這次我們也沒有減少任何資訊，我們光看到package的名字就知道他回傳的是什麼型別的綜合。
