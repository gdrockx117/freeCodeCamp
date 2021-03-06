---
id: 587d78a8367417b2b2512ae4
title: Make a CSS Heartbeat using an Infinite Animation Count
challengeType: 0
videoUrl: ''
localeTitle: جعل CSS نبضات باستخدام عدد الرسوم المتحركة اللانهائي
---

## Description
<section id="description"> إليك مثالًا متحركًا مستمرًا آخر مع خاصية <code>animation-iteration-count</code> التي تستخدم القلب الذي صممته في تحدٍ سابق. تتألف الرسوم المتحركة ذات نبض القلب لمدة ثانية واحدة من قطعتين متحركتين. في <code>heart</code> العناصر (بما في ذلك <code>:before</code> و <code>:after</code> قطع) والرسوم المتحركة لتغيير حجم باستخدام <code>transform</code> الملكية، والخلفية <code>div</code> والرسوم المتحركة لتغيير لونه باستخدام <code>background</code> الملكية. </section>

## Instructions
<section id="instructions"> حافظ على نبض القلب بإضافة خاصية <code>animation-iteration-count</code> لكل من الطبقة <code>back</code> وفئة <code>heart</code> وتعيين القيمة إلى غير محدود. <code>heart:before</code> <code>heart:after</code> لا يحتاج المحددون إلى أي خصائص للرسوم المتحركة. </section>

## Tests
<section id='tests'>

```yml
tests:
  - text: يجب أن تكون لقيمة <code>animation-iteration-count</code> لفئة <code>heart</code> قيمة لانهائية.
    testString: 'assert($(".heart").css("animation-iteration-count") == "infinite", "The <code>animation-iteration-count</code> property for the <code>heart</code> class should have a value of infinite.");'
  - text: يجب أن يكون <code>animation-iteration-count</code> للفئة <code>back</code> قيمة لا نهائية.
    testString: 'assert($(".back").css("animation-iteration-count") == "infinite", "The <code>animation-iteration-count</code> property for the <code>back</code> class should have a value of infinite.");'

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<style>
  .back {
    position: fixed;
    padding: 0;
    margin: 0;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: white;
    animation-name: backdiv;
    animation-duration: 1s;

  }

  .heart {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: pink;
    height: 50px;
    width: 50px;
    transform: rotate(-45deg);
    animation-name: beat;
    animation-duration: 1s;

  }
  .heart:after {
    background-color: pink;
    content: "";
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: 0px;
    left: 25px;
  }
  .heart:before {
    background-color: pink;
    content: "";
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: -25px;
    left: 0px;
  }

  @keyframes backdiv {
    50% {
      background: #ffe6f2;
    }
  }

  @keyframes beat {
    0% {
      transform: scale(1) rotate(-45deg);
    }
    50% {
      transform: scale(0.6) rotate(-45deg);
    }
  }

</style>
<div class="back"></div>
<div class="heart"></div>

```

</div>



</section>

## Solution
<section id='solution'>

```js
// solution required
```
</section>
