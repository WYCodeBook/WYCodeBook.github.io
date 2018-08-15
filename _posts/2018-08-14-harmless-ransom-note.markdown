---
layout: post
title: "Harmless Ransom Note"
date: "2018-07-11 23:33:36 -0700"
categories: [Algorithms, JavaScript]
description: Big O Notation
---

Given an arbitrary ransom note string and another string containing letters from all the magazines, write a function that will return true if the ransom note can be constructed from the magazines ; otherwise, it will return false.

Each letter in the magazine string can only be used once in your ransom note.

## Big O Notation

We use big O notation to asymptotically bound the growth of a running time to within constant factors above and below. Sometimes we want to bound from only above.

#### Constant Runtime

![Constant Runtime](/pic/constantruntime.PNG)

#### Linear Runtime

![Linear Runtime](/pic/linearruntime.PNG)

#### Exponential Runtime

![Exponential Runtime](/pic/exponentialruntime.PNG)

#### Logarithmic Runtime

![Logarithmic Runtime](/pic/logarithmicruntime.PNG)

#### Runtime Graph

![Runtime Graph](/pic/runtime.PNG)



## Codes to Solve Harmless Ransom Note

{% highlight js %}

function harmlessRansomNote(noteText, magazineText) {
  var noteArr = noteText.split(' ');
  var magazineArr = magazineText.split(' ');
  var magazineObj = {};

  magazineArr.forEach(word => {
    if (!magazineObj[word]) magazineObj[word] = 0;
    magazineObj[word]++;
  });

  var noteIsPossible = true;
  noteArr.forEach(word => {
    if (magazineObj[word]) {
      magazineObj[word]--;
      if (magazineObj[word] < 0) noteIsPossible = false;
    }
    else noteIsPossible = false;
  });

  return console.log(noteIsPossible);
}

harmlessRansomNote('this is a secret note for you from a secret admirer', 'puerto rico is a place of great wonder and excitement it has many secret waterfall locatoins that i am an admirer of you must hike quite a distance to find the secret places as they are far from populated areas but it is worth the effort a tip i have for you is to go early in the morning when it is not so hot out also note that you must wear hiking boots this is one of the best places i have ever visited');

{% endhighlight %}

💥 This code used Linear Time Complexity = O(n) + O(m) because there are two loops that are not nested together!
